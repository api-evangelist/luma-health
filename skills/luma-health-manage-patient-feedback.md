---
name: Review patient feedback and approve review replies
description: Read NPS feedback responses and scraped Google/Yelp reviews for a Luma account, then approve or reject the AI-drafted public reply.
api: openapi/luma-health-openapi.yaml
operations: [feedbackResponsesList, feedbackResponseGet, feedbackResponsesExternalReviewsList, feedbackResponsesExternalReviewGet, feedbackResponsesExternalReviewRepliesList, feedbackResponsesExternalReviewRepliesUpdateApproval, feedbackResponsesPromoterHistoriesList]
---

# Review patient feedback and approve review replies

## Auth
`POST /auth/token` (grant_type=client_credentials) → JWT, then `Authorization: Bearer <JWT>`.

## Steps
1. **Read survey feedback.** `feedbackResponsesList` returns NPS responses and feedback-link clicks. Each row carries `patient`, `provider`, `facility`, `appointment` (all 24-char hex ids), `npsscore`, and `response.type` — one of `npsscore`, `positive-click`, `negative-click`. `scoreSource` distinguishes a score the patient gave (`patient`) from one Luma inferred (`sentiment`); treat the two differently when reporting. Fetch a single row with `feedbackResponseGet`.
2. **Read public reviews.** `feedbackResponsesExternalReviewsList` returns reviews scraped from `platform: google | yelp` with `rating` (1–5), `reviewText`, `reviewedAt`, `sentiment` (`positive|neutral|negative`), AI-extracted `themes[]`, `replyEligible`, and `platformRepliedAt`. Use `feedbackResponsesExternalReviewGet` for one review. Only act on reviews where `replyEligible` is true and `platformRepliedAt` is unset.
3. **Pull the drafted reply.** `feedbackResponsesExternalReviewRepliesList` returns the AI-generated reply drafts awaiting a decision.
4. **Approve or reject.** `PATCH /feedbackResponsesExternalReviewReplies/{id}/approval` (`feedbackResponsesExternalReviewRepliesUpdateApproval`) records the decision. This is the ONLY write in this flow — everything else is read-only.
5. **Check platform rotation before asking again.** `feedbackResponsesPromoterHistoriesList` returns `platformsAsked[]`, `lastPlatformAsked` and `lastAskedAt` per patient, so a promoter is not repeatedly pushed to the same review site.

## Rules
- **A public reply about a patient is PHI-adjacent.** Never let an agent auto-approve. Step 4 is a human decision; the agent's job is to surface the draft, the review text and the themes, not to publish. Google and Yelp replies are world-readable and cannot be recalled.
- Collections page with `page` and `limit` and return a `{ response: [...], page, size }` envelope — different from the older Luma collections, so do not assume one shape across the API.
- No `Idempotency-Key` is supported anywhere in this API. The approval PATCH is naturally idempotent per reply id, but do not retry blind writes elsewhere.
- Errors return `{ "message": string }` with the class in the HTTP status; see `errors/luma-health-problem-types.yml`. Every operation can return 401/403.
- These operations appeared additively in the published spec between 2026-07-24 and 2026-08-15 with no version bump and no changelog — pin against a captured spec, do not assume stability.
