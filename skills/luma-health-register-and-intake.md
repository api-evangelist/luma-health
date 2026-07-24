---
name: Register a patient and send digital intake
description: Create a patient record and dispatch a digital intake checklist so forms are completed before the visit.
api: openapi/luma-health-openapi.yaml
operations: [createPatients, checklistTemplatesList, checklistSend, listPatientForms]
---

# Register a patient and send digital intake

## Auth
`POST /auth/token` (grant_type=client_credentials) → JWT, then `Authorization: Bearer <JWT>`.

## Steps
1. **Create the patient.** `createPatients` with demographics. Capture the returned 24-char hex patient id.
2. **Choose an intake template.** `checklistTemplatesList` to find the checklist template that bundles the required forms.
3. **Send intake.** `checklistSend` referencing the `patient` id and template — this delivers the digital intake to the patient across their preferred channel.
4. **Track completion.** `listPatientForms` (filtered by patient) to see which forms are returned and completed.

## Rules
- Writes are not idempotent — do not blindly retry `createPatients`/`checklistSend`; check for an existing patient first with `listPatients`.
- All PHI is subject to Luma's HIPAA/HITRUST controls; only send intake to the correct patient id.
- Error envelope is `{ "message": string }`; see `errors/luma-health-problem-types.yml`.
