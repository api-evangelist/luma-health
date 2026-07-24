---
name: Send a two-way patient message
description: Look up a patient and send an omnichannel two-way message, then read the conversation thread.
api: openapi/luma-health-openapi.yaml
operations: [listPatients, getPatientById, messageCreate, messagesList]
---

# Send a two-way patient message

## Auth
`POST /auth/token` (grant_type=client_credentials) → JWT, then `Authorization: Bearer <JWT>`.

## Steps
1. **Resolve the patient.** `listPatients` to find by demographics, or `getPatientById` if you already hold the 24-char hex id.
2. **Send the message.** `messageCreate` referencing the `patient` id with the message body; Luma routes it over the patient's preferred channel (SMS/email/chat).
3. **Read the thread.** `messagesList` (filtered by patient) to retrieve the conversation and any patient replies.

## Rules
- Respect patient contact preferences — check `getPatientContactPreferences` before broadcasting.
- Not idempotent: retrying `messageCreate` sends a duplicate. Retry only after a network failure with no `200`.
- Paginate with `page` + `limit`; errors return `{ "message": string }`.
