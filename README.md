# Ashby (ashby-hq)

Ashby is a modern all-in-one recruiting platform combining Applicant Tracking System (ATS), sourcing / CRM, interview scheduling, structured-hiring workflows, and recruiting analytics with AI embedded throughout — including AI Application Review for criteria scoring and an AI Notetaker for interview transcripts and structured feedback. The Ashby API exposes 164 operations across 14 product modules with HTTP Basic Auth, 22 webhook event types, async reporting, public job postings for custom careers pages, and partner-implemented assessment integrations. Customers include Deel, Snowflake, Shopify, Notion, Linear, Zapier, and Replit.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/ashby-hq/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

ATS, Applicant Tracking System, Recruiting, Talent Acquisition, Sourcing, CRM, Scheduling, Analytics, Hiring, HR Tech, AI

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## At a Glance

| Property | Value |
|---|---|
| Base URL | `https://api.ashbyhq.com` |
| Authentication | HTTP Basic Auth — API key as username, blank password |
| Spec source | Per-operation OpenAPI blocks at `developers.ashbyhq.com/reference/<op>.md` (indexed by `llms.txt`) |
| Operations | 164 across 14 modules |
| Webhook events | 22 |
| Endpoint naming | `resource.verb` POST-with-JSON (e.g., `application.list`, `candidate.create`) |
| Versioning | Header `Accept: application/json; version=1` |
| Pagination | Cursor (`nextCursor`) + incremental `syncToken` |
| Hard rate limits | Reports API only (15 rpm, 3 concurrent) |
| OpenAPI spec | [`openapi/ashby-openapi.yml`](openapi/ashby-openapi.yml) — assembled from per-operation pages |

## Pricing

| Plan | Audience | Price |
|---|---|---|
| Foundations | 1-100 employees | $400/month flat (10% annual discount) |
| Plus | 101-1,000 employees | Contact sales |
| Enterprise | 1,000+ employees | Contact sales (predictable pricing model) |
| Ashby Analytics | 100+ employees with existing ATS | Contact sales (usage-based) |
| Advanced Scheduling | Add-on | Contact sales |
| AI Notetaker | Add-on | Contact sales |

## APIs

### Ashby Applications API
Create, list, transfer, update, and inspect candidate applications across jobs and stages. Includes application history, hiring team membership, source and stage changes, feedback submission, criteria evaluations from AI Application Review, and application form submission for custom careers pages.

- [Documentation](https://developers.ashbyhq.com/reference/applicationlist)
- [OpenAPI](openapi/ashby-openapi.yml)
- [JSON Schema — Application](json-schema/ashby-application-schema.json)
- [JSON-LD](json-ld/ashby-context.jsonld)
- [Naftiko Capability — Applications](capabilities/applications-applications.yaml)

### Ashby Candidates API
Manage candidate records — create, update, search, anonymize, merge, hire — plus candidate tags, projects, notes, messages, resume and file uploads, sourcing sequences, referrals, and fraud-check status. The candidate is the central CRM entity in Ashby's all-in-one recruiting platform.

- [Documentation](https://developers.ashbyhq.com/reference/candidatelist)
- [OpenAPI](openapi/ashby-openapi.yml)
- [JSON Schema — Candidate](json-schema/ashby-candidate-schema.json)
- [Naftiko Capability — Candidates](capabilities/candidates-candidates.yaml)

### Ashby Jobs API
Manage jobs, openings, job postings, and job boards. Includes job CRUD, compensation updates, status changes (Open / Closed / Archived / Draft), opening lifecycle (create / archive / restore / addJob / removeJob / addLocation / removeLocation), job posting publish/unpublish, job templates, and interview plan associations. Powers Ashby's dedicated partner job feeds.

- [Documentation — job.list](https://developers.ashbyhq.com/reference/joblist)
- [Documentation — jobPosting.list](https://developers.ashbyhq.com/reference/jobpostinglist)
- [OpenAPI](openapi/ashby-openapi.yml)
- [JSON Schema — Job](json-schema/ashby-job-schema.json)
- [Naftiko Capability — Jobs](capabilities/jobs-jobs.yaml)
- [Naftiko Capability — Openings](capabilities/jobs-openings.yaml)
- [Naftiko Capability — Job Postings](capabilities/jobs-job-postings.yaml)

### Ashby Interviews API
Read and manage interviews, interview schedules (create / update / cancel), interview events, interview stages and stage groups, interview plans, interview briefings, interviewer pools and pauses, and AI Notetaker transcripts. Backs Ashby's advanced scheduling and AI Notetaker add-ons.

- [Documentation](https://developers.ashbyhq.com/reference/interviewschedulelist)
- [OpenAPI](openapi/ashby-openapi.yml)
- [JSON Schema — Interview Schedule](json-schema/ashby-interview-schema.json)
- [Naftiko Capability — Interview Schedules](capabilities/interviews-interview-schedules.yaml)
- [Naftiko Capability — Interviewer Pools](capabilities/interviews-interviewer-pools.yaml)

### Ashby Offers API
Create and manage candidate offers, offer versions, the offer process (start), and approval workflows — including force-approve for individual approval steps or the entire offer (mirrors the Ashby app's admin override). Integrates with Pave for compensation and Ironclad for offer contracts.

- [Documentation](https://developers.ashbyhq.com/reference/offerlist)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — Offers](capabilities/offers-offers.yaml)

### Ashby Approvals API
Programmatically define approval definitions for entities in scope of API-managed approvals. Supports multi-step approval workflows and skip-via-empty-list semantics for routing offers and other entities through governance gates.

- [Documentation](https://developers.ashbyhq.com/reference/approvaldefinitionupdate)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — Approvals](capabilities/approvals-approvals.yaml)

### Ashby Surveys & Feedback API
Read survey form and feedback form definitions, create survey requests, list and submit survey submissions, list application feedback, and submit interviewer feedback. Powers Ashby's structured-hiring feedback loops and candidate-experience surveys.

- [Documentation](https://developers.ashbyhq.com/reference/surveyrequestlist)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — Surveys](capabilities/surveys-surveys.yaml)

### Ashby Assessments API
Partner-implemented assessment integration surface. Lists configured assessments, starts and cancels assessment instances, updates assessment status, adds completed assessments to a candidate, and syncs result-driven custom fields. Used by SHL, HackerRank, CodeSignal, and CoderPad integrations.

- [Documentation](https://developers.ashbyhq.com/reference/assessmentstart)
- [Integration Guide](https://developers.ashbyhq.com/docs/creating-an-assessments-integration)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — Assessments](capabilities/assessments-assessments.yaml)

### Ashby Custom Fields API
Define custom fields on Ashby entities, set single and batch values, and manage selectable options. Backs Ashby's structured-hiring data model and is the integration point for partner-driven field syncing (assessments, background checks, HRIS).

- [Documentation](https://developers.ashbyhq.com/reference/customfieldcreate)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — Custom Fields](capabilities/custom-fields-custom-fields.yaml)

### Ashby Organization API
Read and manage organization metadata — users (with permission roles), departments and teams, locations with hierarchical address updates, brands, hiring team roles, archive and close reasons, communication templates, sources, source tracking links, referral forms, and search across users and locations.

- [Documentation](https://developers.ashbyhq.com/reference/userlist)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — Users](capabilities/organization-users.yaml)
- [Naftiko Capability — Departments](capabilities/organization-departments.yaml)
- [Naftiko Capability — Locations](capabilities/organization-locations.yaml)

### Ashby Files API
Look up file metadata and request presigned upload URLs for candidate resumes, application attachments, and partner-provided assessment artifacts. Two-step pattern — request presigned URL, then PUT bytes — keeps payloads off Ashby's API surface.

- [Documentation](https://developers.ashbyhq.com/reference/fileinfo)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — Files](capabilities/files-files.yaml)

### Ashby Reports API
Generate Ashby Analytics reports synchronously or asynchronously. The async path is the recommended pattern for large datasets; subject to a strict 15 req/min, 3 concurrent execution cap to protect the analytics warehouse. Powers the standalone Ashby Analytics product.

- [Documentation](https://developers.ashbyhq.com/reference/reportgenerate)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — Reports](capabilities/reports-reports.yaml)

### Ashby Webhooks API
Manage outbound webhook subscriptions (`webhook.create` / `update` / `info` / `delete`) and consume 22 event types: `applicationSubmit`, `applicationUpdate`, `candidateDelete`, `candidateHire`, `candidateMerge`, `candidateStageChange`, `interviewPlanTransition`, `interviewScheduleCreate`, `interviewScheduleUpdate`, `jobCreate`, `jobUpdate`, `jobPostingPublish`, `jobPostingUnpublish`, `jobPostingUpdate`, `offerCreate`, `offerDelete`, `offerUpdate`, `openingCreate`, `ping`, `pushToHRIS`, `signatureRequestUpdate`, `surveySubmit`. HMAC-SHA256 signed via `Ashby-Signature` header; automatic retries on non-2xx responses.

- [Setting up Webhooks](https://developers.ashbyhq.com/docs/setting-up-webhooks)
- [Authenticating Webhooks](https://developers.ashbyhq.com/docs/authenticating-webhooks)
- [Common Webhook Payload Data](https://developers.ashbyhq.com/docs/common-webhook-payload-data)
- [Related Webhooks](https://developers.ashbyhq.com/docs/related-webhooks)
- [Webhook Retries](https://developers.ashbyhq.com/docs/webhook-retries)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — Webhooks](capabilities/webhooks-webhooks.yaml)

### Ashby Job Postings Public API
Public, unauthenticated job postings endpoint for building custom careers pages and partner job feeds (LinkedIn, Indeed, Otta, Built In, ZipRecruiter, Levels.fyi). Returns published job postings with structured location, compensation, employment type, and brand metadata.

- [Ashby Job Postings API](https://developers.ashbyhq.com/docs/ashby-job-postings-api)
- [Creating a Custom Careers Page](https://developers.ashbyhq.com/docs/creating-a-custom-careers-page)
- [Dedicated Partner Job Feeds](https://developers.ashbyhq.com/docs/dedicated-partner-job-feeds)

### Ashby API Keys API
Inspect the calling API key — returns the key's name, granted permission modules (Jobs, Candidates, Interviews, Offers, Approvals, Organization, Reports, API Keys), and read/write scopes. Useful for partners that need to validate permission grants before issuing dependent calls.

- [Documentation](https://developers.ashbyhq.com/reference/apikeyinfo)
- [OpenAPI](openapi/ashby-openapi.yml)
- [Naftiko Capability — API Keys](capabilities/api-keys-api-keys.yaml)

## Plans, Rate Limits, and FinOps

- [Plans (API Commons Plans 0.1)](plans/ashby-hq-plans-pricing.yml)
- [Rate Limits (API Commons Rate Limits 0.1)](rate-limits/ashby-hq-rate-limits.yml)
- [FinOps (FinOps Framework / FOCUS 1.3)](finops/ashby-hq-finops.yml)

## Integrations (selected)

- **HRIS:** Workday, Rippling, Gusto, HiBob, Deel, Paylocity, BambooHR (via `pushToHRIS` webhook + API)
- **Assessments:** SHL, CodeSignal, HackerRank, CoderPad (via Assessments API)
- **Background Checks:** HireRight, Checkr
- **Video / Comms:** Zoom, Slack, Google Workspace, Microsoft 365
- **Job Boards:** Indeed, ZipRecruiter, Levels.fyi, Otta, Built In, LinkedIn (via Job Postings public API + dedicated partner feeds)
- **Offers / Contracts:** Pave (compensation), Ironclad (contracts), Metaview (AI interview agents)
- **Automation:** Zapier

200+ integration partners total per the Ashby integrations marketplace.

## Sources

- [Ashby homepage](https://www.ashbyhq.com)
- [Ashby developer portal](https://developers.ashbyhq.com)
- [Ashby llms.txt index](https://developers.ashbyhq.com/llms.txt)
- [Ashby authentication](https://developers.ashbyhq.com/reference/authentication)
- [Ashby pricing](https://www.ashbyhq.com/pricing)
- [Ashby integrations](https://www.ashbyhq.com/integrations)
