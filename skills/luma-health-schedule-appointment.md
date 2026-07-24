---
name: Schedule a patient appointment
description: Find or create a patient, discover open availability, and book an appointment on the Luma Health platform.
api: openapi/luma-health-openapi.yaml
operations: [listPatients, createPatients, appointmentTypesList, listSchedulerAvailabilities, appointmentCreate, appointmentGet]
---

# Schedule a patient appointment

Use the Luma Health Rest-Service (v2, `https://api.lumahealth.io/api/v2`) to book a patient into an open slot.

## Auth
1. Exchange your client credentials for a JWT: `POST /auth/token` with `{ "client_id", "client_secret", "grant_type": "client_credentials" }`.
2. Send `Authorization: Bearer <JWT>` on every subsequent call. Tokens are short-lived — re-mint on `401`.

## Steps
1. **Find the patient.** `listPatients` (filter by demographics). Object ids are 24-char hex. If no match, create one with `createPatients`.
2. **Pick the appointment type.** `appointmentTypesList` to get the EHR appointment type id.
3. **Find open slots.** `listSchedulerAvailabilities` for the chosen provider/facility/appointment type to return bookable times.
4. **Book it.** `appointmentCreate` referencing `patient`, `provider`, `facility`, and `appointmentType` ids plus the chosen slot.
5. **Confirm.** `appointmentGet` on the returned id to verify status.

## Rules
- No `Idempotency-Key` is supported — dedupe on the caller side before retrying `appointmentCreate`.
- Errors return `{ "message": string }` with the class in the HTTP status (400 invalid, 401 token, 403 permission, 404 missing). See `errors/luma-health-problem-types.yml`.
- Paginate lists with `page` + `limit`.
