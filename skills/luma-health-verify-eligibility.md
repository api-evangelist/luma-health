---
name: Verify patient insurance eligibility
description: Run a real-time insurance eligibility check for a patient before an appointment.
api: openapi/luma-health-openapi.yaml
operations: [getPatientById, insuranceCheckEligibility]
---

# Verify patient insurance eligibility

## Auth
`POST /auth/token` (grant_type=client_credentials) → JWT, then `Authorization: Bearer <JWT>`.

## Steps
1. **Load the patient.** `getPatientById` with the 24-char hex id to confirm the insurance record on file.
2. **Check eligibility.** `insuranceCheckEligibility` for the patient's insurance record — Luma runs a real-time payor eligibility verification and returns coverage status. For batches use `insuranceCheckEligibilityBulk`.

## Rules
- Eligibility results reflect the payor response at call time; re-run close to the appointment date.
- Payor directory is available via `insurancePayorsList` if you need to resolve a payor id.
- Errors return `{ "message": string }` with the class in the HTTP status; see `errors/luma-health-problem-types.yml`.
