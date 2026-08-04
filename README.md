# Luma Health (luma-health)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Luma Health is a United States patient-engagement (Patient Success) platform for healthcare provider organizations, headquartered in San Francisco, California. Its operational AI platform automates the patient journey - self-service scheduling, referral and waitlist management, digital intake and forms, omnichannel two-way messaging and broadcast, appointment reminders and recalls, insurance eligibility verification, payments and billing, and a conversational AI assistant - and integrates bidirectionally with the major EHRs (Epic, Oracle Health/Cerner, MEDITECH, eClinicalWorks, athenahealth, NextGen, Greenway, Nextech).

Luma exposes a documented public REST API (Rest-Service v2.0.0, OpenAPI 3.0.0) at `https://api.lumahealth.io/api/v2`, secured with OAuth2 client-credentials that issue JWT bearer tokens. The developer-facing surface is a REST API rather than an HL7 FHIR server; FHIR/HL7 interoperability with EHRs happens inside Luma's integration layer, not as a public FHIR endpoint.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/luma-health/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/luma-health/refs/heads/main/apis.yml)

## Home Market

United States

## Tags

- Healthcare
- United States
- Patient Engagement
- Scheduling
- Referrals
- Intake
- Messaging
- Eligibility
- EHR
- Interoperability
- Clinical AI

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

A single OpenAPI 3.0.0 specification ("Rest-Service" v2.0.0, 143 paths / 276 operations / 54 tags), harvested verbatim to [`openapi/luma-health-openapi.yaml`](openapi/luma-health-openapi.yaml) from `https://apidocs.lumahealth.io/public.yaml`, backs the following product-family APIs (all served at `https://api.lumahealth.io/api/v2`):

- **Scheduling & Appointments API** - appointments, appointment types, availabilities, schedulers, offers, recalls, waitlists.
- **Patients API** - patient records, patient forms and form templates, stored payment cards.
- **Providers & Facilities API** - providers, provider scheduling groups, facilities, specialties, groups, users.
- **Messaging & Engagement API** - two-way messaging, engagements/events/settings, reminders, message templates.
- **Broadcast & Campaigns API** - broadcast events, broadcast flows and templates, campaigns.
- **Intake & Forms API** - checklists and templates, patient forms, file uploads.
- **Billing & Payments API** - billing charges and copays, estimates, patient credit cards.
- **Eligibility & Insurance API** - insurance records with real-time eligibility verification and payors directory.
- **Referrals API** - inbound and outbound referral management.
- **Conversational AI Assistant API** - assistant instances and actions, lumabot flows and templates, knowledge base Q&A, chat activities, queue-manager routing.
- **Reporting & Audits API** - operational reports, system and chat audits.
- **Authentication API** - OAuth2 client-credentials: generate/rotate client id/secret and exchange for JWT access tokens.

## Authentication

OAuth2 client-credentials. `POST /auth/clients` provisions a client id and secret, `POST /auth/token` exchanges them for a JWT access token, and all other operations require the `Bearer` JWT. This is not SMART-on-FHIR; no `patient/*.read` or `system/*.rw` scopes are documented.

## Common Properties

- [Website](https://www.lumahealth.io)
- [Developer Portal](https://apidocs.lumahealth.io)
- [Documentation](https://apidocs.lumahealth.io)
- [OpenAPI](openapi/luma-health-openapi.yaml)
- [Integrations](https://www.lumahealth.io/integrations)
- [Blog](https://www.lumahealth.io/blog)
- [Status Page](https://status.lumahealth.io)
- [Security](https://www.lumahealth.io/security)
- [Login](https://next.lumahealth.io/login)
- [Terms of Service](https://www.lumahealth.io/terms)
- [Privacy Policy](https://www.lumahealth.io/privacy-policy)
- [GitHub Organization](https://github.com/lumahealthhq)
- [LinkedIn](https://www.linkedin.com/company/luma-health)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
