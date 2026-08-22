# Ashby (ashby-hq)

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

Ashby is a modern all-in-one recruiting platform combining Applicant Tracking System (ATS), sourcing/CRM, interview scheduling, structured-hiring workflows, and recruiting analytics with AI embedded throughout — including AI Application Review for criteria scoring and an AI Notetaker for interview transcripts and structured feedback. The Ashby API exposes 164 operations across 14 product modules with HTTP Basic Auth, 22 webhook event types, async reporting, public job postings for custom careers pages, and partner-implemented assessment integrations. Customers include Deel, Snowflake, Shopify, Notion, Linear, Zapier, and Replit; pricing spans Foundations ($400/mo flat for sub-100 employees), Plus, and Enterprise tiers, plus a standalone Ashby Analytics product layered on existing ATS deployments.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ashby-hq/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ashby-hq/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- ATS
- Applicant Tracking System
- Recruiting
- Talent Acquisition
- Sourcing
- CRM
- Scheduling
- Analytics
- Hiring
- HR Tech
- AI

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Ashby Applications API

Create, list, transfer, update, and inspect candidate applications across jobs and stages. Includes application history, hiring team membership, source and stage changes, feedback submission, criteria evaluations from AI Application Review, and application form submission for custom careers pages.

- **Human URL:** [https://developers.ashbyhq.com/reference/applicationlist](https://developers.ashbyhq.com/reference/applicationlist)

#### Tags

- Applications
- ATS
- Recruiting
- Candidates

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/applicationlist)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/ashby-application-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/ashby-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Ashby Candidates API

Manage candidate records — create, update, search, anonymize, merge, hire — plus candidate tags, projects, notes, messages, resume and file uploads, sourcing sequences, referrals, and fraud-check status. The candidate is the central CRM entity in Ashby's all-in-one recruiting platform.

- **Human URL:** [https://developers.ashbyhq.com/reference/candidatelist](https://developers.ashbyhq.com/reference/candidatelist)

#### Tags

- Candidates
- ATS
- CRM
- Sourcing
- Recruiting

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/candidatelist)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/ashby-candidate-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/ashby-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Ashby Jobs API

Manage jobs, openings, job postings, and job boards. Includes job CRUD, compensation updates, status changes (Open / Closed / Archived / Draft), opening lifecycle (create / archive / restore / addJob / removeJob / addLocation / removeLocation), job posting publish/unpublish, job templates, and interview plan associations. Powers Ashby's dedicated partner job feeds.

- **Human URL:** [https://developers.ashbyhq.com/reference/joblist](https://developers.ashbyhq.com/reference/joblist)

#### Tags

- Jobs
- Openings
- Job Postings
- Job Boards
- ATS

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/joblist)
- [Documentation](https://developers.ashbyhq.com/reference/jobpostinglist)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/ashby-job-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Ashby Interviews API

Read and manage interviews, interview schedules (create / update / cancel), interview events, interview stages and stage groups, interview plans, interview briefings, interviewer pools and pauses, and AI Notetaker transcripts. Backs Ashby's advanced scheduling and AI Notetaker add-ons.

- **Human URL:** [https://developers.ashbyhq.com/reference/interviewschedulelist](https://developers.ashbyhq.com/reference/interviewschedulelist)

#### Tags

- Interviews
- Scheduling
- Recruiting
- Calendar
- Notetaker

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/interviewschedulelist)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/ashby-interview-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Ashby Offers API

Create and manage candidate offers, offer versions, the offer process (start), and approval workflows — including force-approve for individual approval steps or the entire offer (mirrors the Ashby app's admin override). Integrates with Pave for compensation and Ironclad for offer contracts.

- **Human URL:** [https://developers.ashbyhq.com/reference/offerlist](https://developers.ashbyhq.com/reference/offerlist)

#### Tags

- Offers
- Approvals
- Recruiting
- Hiring

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/offerlist)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Approvals API

Programmatically define approval definitions for entities in scope of API-managed approvals. Supports multi-step approval workflows and skip-via-empty-list semantics for routing offers and other entities through governance gates.

- **Human URL:** [https://developers.ashbyhq.com/reference/approvaldefinitionupdate](https://developers.ashbyhq.com/reference/approvaldefinitionupdate)

#### Tags

- Approvals
- Workflow
- Governance
- Recruiting

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/approvaldefinitionupdate)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Surveys & Feedback API

Read survey form and feedback form definitions, create survey requests, list and submit survey submissions, list application feedback, and submit interviewer feedback. Powers Ashby's structured-hiring feedback loops and candidate-experience surveys.

- **Human URL:** [https://developers.ashbyhq.com/reference/surveyrequestlist](https://developers.ashbyhq.com/reference/surveyrequestlist)

#### Tags

- Surveys
- Feedback
- Forms
- Recruiting

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/surveyrequestlist)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Assessments API

Partner-implemented assessment integration surface. Lists configured assessments, starts and cancels assessment instances, updates assessment status, adds completed assessments to a candidate, and syncs result-driven custom fields. Used by SHL, HackerRank, CodeSignal, and CoderPad integrations.

- **Human URL:** [https://developers.ashbyhq.com/reference/assessmentstart](https://developers.ashbyhq.com/reference/assessmentstart)

#### Tags

- Assessments
- Integrations
- Partner API
- Recruiting

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/assessmentstart)
- [Documentation](https://developers.ashbyhq.com/docs/creating-an-assessments-integration)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Custom Fields API

Define custom fields on Ashby entities, set single and batch values, and manage selectable options. Backs Ashby's structured-hiring data model and is the integration point for partner-driven field syncing (assessments, background checks, HRIS).

- **Human URL:** [https://developers.ashbyhq.com/reference/customfieldcreate](https://developers.ashbyhq.com/reference/customfieldcreate)

#### Tags

- Custom Fields
- Configuration
- Recruiting

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/customfieldcreate)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Organization API

Read and manage organization metadata — users (with permission roles), departments and teams, locations with hierarchical address updates, brands, hiring team roles, archive and close reasons, communication templates, sources, source tracking links, referral forms, and search across users and locations. The reference data plane for every other Ashby resource.

- **Human URL:** [https://developers.ashbyhq.com/reference/userlist](https://developers.ashbyhq.com/reference/userlist)

#### Tags

- Organization
- Users
- Departments
- Locations
- Brands
- Sources

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/userlist)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Files API

Look up file metadata and request presigned upload URLs for candidate resumes, application attachments, and partner-provided assessment artifacts. Two-step pattern — request presigned URL, then PUT bytes — keeps payloads off Ashby's API surface.

- **Human URL:** [https://developers.ashbyhq.com/reference/fileinfo](https://developers.ashbyhq.com/reference/fileinfo)

#### Tags

- Files
- Uploads
- Recruiting

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/fileinfo)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Reports API

Generate Ashby Analytics reports synchronously or asynchronously. The async path is the recommended pattern for large datasets; subject to a strict 15 req/min, 3 concurrent execution cap to protect the analytics warehouse. Powers the standalone Ashby Analytics product.

- **Human URL:** [https://developers.ashbyhq.com/reference/reportgenerate](https://developers.ashbyhq.com/reference/reportgenerate)

#### Tags

- Reports
- Analytics
- Recruiting
- Async

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/reportgenerate)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Webhooks API

Manage outbound webhook subscriptions (webhook.create / update / info / delete) and consume 22 event types: applicationSubmit, applicationUpdate, candidateDelete, candidateHire, candidateMerge, candidateStageChange, interviewPlanTransition, interviewScheduleCreate, interviewScheduleUpdate, jobCreate, jobUpdate, jobPostingPublish, jobPostingUnpublish, jobPostingUpdate, offerCreate, offerDelete, offerUpdate, openingCreate, ping, pushToHRIS, signatureRequestUpdate, surveySubmit. HMAC-SHA256 signed via Ashby-Signature header; automatic retries on non-2xx responses.

- **Human URL:** [https://developers.ashbyhq.com/docs/setting-up-webhooks](https://developers.ashbyhq.com/docs/setting-up-webhooks)

#### Tags

- Webhooks
- Events
- Eventing
- Recruiting

#### Properties

- [Documentation](https://developers.ashbyhq.com/docs/setting-up-webhooks)
- [Documentation](https://developers.ashbyhq.com/docs/authenticating-webhooks)
- [Documentation](https://developers.ashbyhq.com/docs/common-webhook-payload-data)
- [Documentation](https://developers.ashbyhq.com/docs/related-webhooks)
- [Documentation](https://developers.ashbyhq.com/docs/webhook-retries)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby Job Postings Public API

Public, unauthenticated job postings endpoint for building custom careers pages and partner job feeds (LinkedIn, Indeed, Otta, Built In, ZipRecruiter, Levels.fyi). Returns published job postings with structured location, compensation, employment type, and brand metadata.

- **Human URL:** [https://developers.ashbyhq.com/docs/ashby-job-postings-api](https://developers.ashbyhq.com/docs/ashby-job-postings-api)

#### Tags

- Job Postings
- Careers Page
- Public

#### Properties

- [Documentation](https://developers.ashbyhq.com/docs/ashby-job-postings-api)
- [Documentation](https://developers.ashbyhq.com/docs/creating-a-custom-careers-page)
- [Documentation](https://developers.ashbyhq.com/docs/dedicated-partner-job-feeds)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Ashby API Keys API

Inspect the calling API key — returns the key's name, granted permission modules (Jobs, Candidates, Interviews, Offers, Approvals, Organization, Reports, API Keys), and read/write scopes. Useful for partners that need to validate permission grants before issuing dependent calls.

- **Human URL:** [https://developers.ashbyhq.com/reference/apikeyinfo](https://developers.ashbyhq.com/reference/apikeyinfo)

#### Tags

- API Keys
- Authentication
- Administration

#### Properties

- [Documentation](https://developers.ashbyhq.com/reference/apikeyinfo)
- [OpenAPI](openapi/ashby-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/ashby.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/ashby.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.ashbyhq.com)
- [Portal](https://developers.ashbyhq.com)
- [Getting Started](https://developers.ashbyhq.com/docs/getting-started-with-ashby)
- [Documentation](https://developers.ashbyhq.com/reference/authentication)
- [Documentation](https://developers.ashbyhq.com/docs/introduction)
- [Documentation](https://developers.ashbyhq.com/docs/endpoint-naming)
- [Documentation](https://developers.ashbyhq.com/docs/pagination)
- [Documentation](https://developers.ashbyhq.com/docs/pagination-and-incremental-sync)
- [Documentation](https://developers.ashbyhq.com/docs/expansions)
- [Errors](https://developers.ashbyhq.com/docs/responses-and-errors)
- [Documentation](https://developers.ashbyhq.com/docs/syncing-records)
- [Support](https://developers.ashbyhq.com/docs/support)
- [Changelog](https://developers.ashbyhq.com/changelog)
- [Documentation](https://developers.ashbyhq.com/llms.txt)
- [Plans](https://www.ashbyhq.com/pricing)
- [Case Studies](https://www.ashbyhq.com/customers)
- [Blog](https://www.ashbyhq.com/blog)
- [Integrations](https://www.ashbyhq.com/integrations)
- [About Us](https://www.ashbyhq.com/about)
- [Jobs](https://www.ashbyhq.com/careers)
- [Sign Up](https://app.ashbyhq.com/signup)
- [Login](https://app.ashbyhq.com/login)
- [Documentation](https://docs.ashbyhq.com)
- [Documentation](https://docs.ashbyhq.com/user-permissions)
- [Support](https://app.ashbyhq.com/support)
- [Terms of Service](https://www.ashbyhq.com/legal/terms)
- [Privacy Policy](https://www.ashbyhq.com/legal/privacy)
- [Security](https://www.ashbyhq.com/security)
- [Trust Center](https://www.ashbyhq.com/trust)
- [Status Page](https://www.ashbyhq.com/status)
- [GitHub Organization](https://github.com/ashbyhq)
- [LinkedIn](https://www.linkedin.com/company/ashbyhq)
- [Twitter](https://twitter.com/ashbyhq)
- [Base U R L](https://api.ashbyhq.com)
- [Plans](plans/ashby-hq-plans-pricing.yml)
- [Rate Limits](rate-limits/ashby-hq-rate-limits.yml)
- [Fin Ops](finops/ashby-hq-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
