# Luma Health

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Luma Health is a United States patient-engagement (Patient Success) platform for healthcare provider organizations, headquartered in San Francisco, California. Its operational AI platform automates the patient journey - self-service scheduling and appointment management, referral and waitlist management, intake and digital forms, omnichannel two-way messaging and broadcast, appointment reminders and recalls, insurance eligibility verification, payments and billing, and a conversational AI assistant (Navigator / lumabot) - and integrates bidirectionally with the major EHRs (Epic, Oracle Health/Cerner, MEDITECH, eClinicalWorks, athenahealth, NextGen, Greenway, Nextech). Luma exposes a documented public REST API (Rest-Service v2.0.0, OpenAPI 3.0.0) at https://api.lumahealth.io/api/v2, secured with OAuth2 client-credentials that issue JWT bearer tokens. The developer-facing surface is a REST API rather than an HL7 FHIR server; FHIR/HL7 interoperability with EHRs happens inside Luma's integration layer, not as a public FHIR endpoint.

**Areas:** Healthcare · United States · Patient Engagement · Scheduling · Referrals · Intake · Messaging · Eligibility · Electronic Health Records · Interoperability · Clinical AI · Reputation Management

## Luma Health on APIs.io

Everything profiled for Luma Health is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/luma-health/](https://apis.io/providers/luma-health/)** — or go straight to one of the APIs or properties below.

### APIs (58)

- [Luma Health Appointments API](https://apis.io/apis/luma-health/luma-health-appointments-api/) — Patient's appointments to see a doctor
- [Luma Health Assistant Actions API](https://apis.io/apis/luma-health/luma-health-assistantactions-api/) — Audit log of individual tool calls made by the Navigator AI assistant during a conversation
- [Luma Health Assistant Instances API](https://apis.io/apis/luma-health/luma-health-assistantinstances-api/) — Conversations between the Navigator AI assistant and a patient or staff member
- [Luma Health Assistant Transfer Rules API](https://apis.io/apis/luma-health/luma-health-assistanttransferrules-api/) — Transfer rules for AI assistants (Navigator) to handle call routing
- [Luma Health Auth API](https://apis.io/apis/luma-health/luma-health-auth-api/) — Luma Client Access
- [Luma Health Availabilities API](https://apis.io/apis/luma-health/luma-health-availabilities-api/) — EHR provider scheduler availability
- [Luma Health Billing Charges API](https://apis.io/apis/luma-health/luma-health-billingcharges-api/) — Financial charges tracked against a patient, such as copays and patient balances
- [Luma Health Billing Copays API](https://apis.io/apis/luma-health/luma-health-billingcopays-api/) — Copay amounts configured per source (system, EHR, or manual) and referenced by patient form templates
- [Luma Health Broadcast Templates API](https://apis.io/apis/luma-health/luma-health-broadcast-templates-api/) — The Broadcast Templates API from Luma Health — 2 operation(s) for broadcast templates.
- [Luma Health Broadcast Events API](https://apis.io/apis/luma-health/luma-health-broadcastevents-api/) — Broadcast event logs and history
- [Luma Health Broadcast Flows API](https://apis.io/apis/luma-health/luma-health-broadcastflows-api/) — Broadcast flows for mass messaging campaigns
- [Luma Health Campaigns API](https://apis.io/apis/luma-health/luma-health-campaigns-api/) — Contact preference campaigns that determine how and in what order a patient, facility, or user is contacted
- [Luma Health Chat Activities API](https://apis.io/apis/luma-health/luma-health-chatactivities-api/) — conversations with a patient
- [Luma Health Chat Activities Reasons API](https://apis.io/apis/luma-health/luma-health-chatactivitiesreasons-api/) — reason why a chatActivity was closed
- [Luma Health Chat Audits API](https://apis.io/apis/luma-health/luma-health-chataudits-api/) — Audits for message chat
- [Luma Health Checklists API](https://apis.io/apis/luma-health/luma-health-checklists-api/) — Per-appointment, per-patient instances of required pre-visit tasks generated from a checklist template
- [Luma Health Custom Web Styles API](https://apis.io/apis/luma-health/luma-health-customwebstyles-api/) — custom styles, CSS, logo images for customers
- [Luma Health Engagements API](https://apis.io/apis/luma-health/luma-health-engagements-api/) — Conversation sessions between the system and a recipient, driven by one or more AI agents
- [Luma Health Estimates API](https://apis.io/apis/luma-health/luma-health-estimates-api/) — Estimates
- [Luma Health Facilities API](https://apis.io/apis/luma-health/luma-health-facilities-api/) — Customer facilities
- [Luma Health Feedback Responses API](https://apis.io/apis/luma-health/luma-health-feedbackresponses-api/) — Patient responses to NPS feedback surveys and clicks on feedback links
- [Luma Health Feedback Responses External Review Replies API](https://apis.io/apis/luma-health/luma-health-feedbackresponsesexternalreviewreplies-api/) — AI-generated reply drafts for external reviews, with approve/reject workflow
- [Luma Health Feedback Responses External Reviews API](https://apis.io/apis/luma-health/luma-health-feedbackresponsesexternalreviews-api/) — Scraped external reviews from Google Business Profile and Yelp
- [Luma Health Feedback Responses Promoter Histories API](https://apis.io/apis/luma-health/luma-health-feedbackresponsespromoterhistories-api/) — Per-patient platform rotation history for NPS promoter review requests
- [Luma Health Groups API](https://apis.io/apis/luma-health/luma-health-groups-api/) — Group of staff users
- [Luma Health Insurance Payors API](https://apis.io/apis/luma-health/luma-health-insurancepayors-api/) — Insurance payors/carriers maintained in Luma's payor directory
- [Luma Health Insurances API](https://apis.io/apis/luma-health/luma-health-insurances-api/) — Patient insurance coverage records
- [Luma Health Knowledge Base Question Answers API](https://apis.io/apis/luma-health/luma-health-knowledgebasequestionanswers-api/) — Question and answer entries for knowledge bases
- [Luma Health Lumabot Flows API](https://apis.io/apis/luma-health/luma-health-lumabotflows-api/) — LumaBot Flows answered by patients
- [Luma Health Lumabot Flow Templates API](https://apis.io/apis/luma-health/luma-health-lumabotflowtemplates-api/) — Templates for LumaBot flows
- [Luma Health Messages API](https://apis.io/apis/luma-health/luma-health-messages-api/) — Messages (chat, sms, voice, email, whatsapp, fax, in-app)
- [Luma Health Message Template Partials API](https://apis.io/apis/luma-health/luma-health-messagetemplatepartials-api/) — Reusable partials that can be composed into message templates
- [Luma Health Offers API](https://apis.io/apis/luma-health/luma-health-offers-api/) — Offers
- [Luma Health Outbound Referrals API](https://apis.io/apis/luma-health/luma-health-outboundreferrals-api/) — Outbound Referral
- [Luma Health Patient Credit Cards API](https://apis.io/apis/luma-health/luma-health-patientcreditcards-api/) — Luma Health patient credit cards
- [Luma Health Patient Form Templates API](https://apis.io/apis/luma-health/luma-health-patientformtemplates-api/) — Templates from patient forms
- [Luma Health Patient Message Templates API](https://apis.io/apis/luma-health/luma-health-patientmessagetemplates-api/) — Message templates used to compose patient communications
- [Luma Health Patients API](https://apis.io/apis/luma-health/luma-health-patients-api/) — Customer patients
- [Luma Health Providers API](https://apis.io/apis/luma-health/luma-health-providers-api/) — Luma Health providers
- [Luma Health Provider Scheduling Groups API](https://apis.io/apis/luma-health/luma-health-providerschedulinggroups-api/) — Groups of providers configured for shared scheduling behavior, such as round-robin or waterfall assignment
- [Luma Health Queue Manager Instances API](https://apis.io/apis/luma-health/luma-health-queuemanagerinstances-api/) — Instances of queue manager templates representing items in a queue
- [Luma Health Recalls API](https://apis.io/apis/luma-health/luma-health-recalls-api/) — Recalls
- [Luma Health Referrals API](https://apis.io/apis/luma-health/luma-health-referrals-api/) — Luma Patient referrals
- [Luma Health Reminders API](https://apis.io/apis/luma-health/luma-health-reminders-api/) — Luma Reminders
- [Luma Health Reports API](https://apis.io/apis/luma-health/luma-health-reports-api/) — Luma Analytical Reports
- [Luma Health Schedulers API](https://apis.io/apis/luma-health/luma-health-schedulers-api/) — Scheduler
- [Luma Health Settings API](https://apis.io/apis/luma-health/luma-health-settings-api/) — Luma resource settings
- [Luma Health Specialties API](https://apis.io/apis/luma-health/luma-health-specialties-api/) — A Doctor's specialty
- [Luma Health Squigglies API](https://apis.io/apis/luma-health/luma-health-squigglies-api/) — Messages Squigglies
- [Luma Health Users API](https://apis.io/apis/luma-health/luma-health-users-api/) — Staff users
- [Luma Health Waitlists API](https://apis.io/apis/luma-health/luma-health-waitlists-api/) — Patients waiting for an appointment
- [Luma Health Appointment Types API](https://apis.io/apis/luma-health/luma-health-appointment-types-api/) — EHR appointment types
- [Luma Health Checklist Templates API](https://apis.io/apis/luma-health/luma-health-checklist-templates-api/) — Reusable definitions of required pre-visit tasks used to build checklists
- [Luma Health Engagement Events API](https://apis.io/apis/luma-health/luma-health-engagement-events-api/) — Append-only history of events that occurred during an engagement
- [Luma Health Engagement Settings API](https://apis.io/apis/luma-health/luma-health-engagement-settings-api/) — Reusable voice and language presets that can be attached to an engagement
- [Luma Health File Uploads API](https://apis.io/apis/luma-health/luma-health-file-uploads-api/) — File Uploads
- [Luma Health Patient Forms API](https://apis.io/apis/luma-health/luma-health-patient-forms-api/) — Patient forms answered by patients
- [Luma Health system Audits API](https://apis.io/apis/luma-health/luma-health-system-audits-api/) — Audit logs for certain system events in a given account

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [luma-health](https://apis.io/servers/luma-health/luma-health/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Luma Health Agentic Access](https://apis.io/agentic-access/luma-health/luma-health-agentic-access/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Luma Health Openapi Overlay](https://apis.io/overlays/luma-health/luma-health-openapi-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Luma Health Authentication](https://apis.io/security/luma-health/luma-health-authentication/)
- [Luma Health Domain Security](https://apis.io/security/luma-health/luma-health-domain-security/)
- [Luma Health Trust Center](https://apis.io/security/luma-health/luma-health-trust-center/)
- [Luma Health Vulnerability Disclosure](https://apis.io/security/luma-health/luma-health-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Luma Health Plans Pricing](https://apis.io/plans/luma-health/luma-health-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Luma Health Rate Limits](https://apis.io/rate-limits/luma-health/luma-health-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.lumahealth.io)
- [Documentation](https://apidocs.lumahealth.io)
- [API reference](https://apidocs.lumahealth.io)
- [Blog](https://www.lumahealth.io/blog)
- [Compliance](https://www.lumahealth.io/security-and-trust/)
- [Terms of service](https://www.lumahealth.io/terms-of-use)
- [Privacy policy](https://www.lumahealth.io/privacy-policy)
- [GitHub](https://github.com/lumahealthhq)
- [Status](https://status.lumahealth.io)

## API Evangelist rating

**Kin Score 48.4** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 74.1 |
| Contract quality | 49.6 |
| Contract governance | 4.5 |
| Operational transparency | 28.9 |
| Developer ergonomics | 36.3 |
| Access clarity | 43.4 |

**Agent readiness 29.4** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 32.0** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/luma-health/](https://apis.io/providers/luma-health/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Luma Health: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/luma-health/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
