# Ashby HQ GraphQL Schema

This is a conceptual GraphQL schema for the Ashby recruiting platform, derived from the Ashby REST API documented at [https://developers.ashbyhq.com](https://developers.ashbyhq.com). Ashby does not publish a native GraphQL endpoint; this schema represents the same product surface in GraphQL terms to support code generation, tooling, and API research workflows.

## Overview

Ashby is an all-in-one recruiting platform combining ATS, CRM/sourcing, scheduling, structured hiring workflows, analytics, and AI features (AI Application Review and AI Notetaker). The REST API exposes 164 operations across 14 product modules authenticated via HTTP Basic Auth with scoped API keys.

This schema covers all 14 modules:

- Applications
- Candidates
- Jobs
- Openings
- Job Postings
- Interviews
- Offers
- Approvals
- Surveys and Feedback
- Assessments
- Custom Fields
- Organization (Users, Departments, Locations, Brands, Sources)
- Files
- Reports
- Webhooks
- API Keys

## Schema Source

- **File:** `ashby-hq-schema.graphql`
- **Derived from:** Ashby REST API — [https://developers.ashbyhq.com](https://developers.ashbyhq.com)
- **OpenAPI artifact:** `openapi/ashby-openapi.yml`
- **JSON Schema artifacts:** `json-schema/`

## Type Inventory

### Core Domain Types (65)

| Type | Description |
|---|---|
| `Organization` | Top-level tenant entity |
| `User` | Ashby user with permission module grants |
| `PermissionModuleGrant` | Module + scope pair on an API key or user |
| `Department` | Hierarchical department/team |
| `Location` | Hierarchical office or remote location with address |
| `Address` | Structured postal address |
| `Brand` | Named company brand for multi-brand job postings |
| `Source` | Candidate source (referral, job board, etc.) |
| `ArchiveReason` | Configured reason for archiving an application |
| `CloseReason` | Configured reason for closing a job |
| `CommunicationTemplate` | Email/message template |
| `HiringTeamRole` | Named hiring team role (recruiter, coordinator, etc.) |
| `HiringTeamMember` | User + role assignment on a job |
| `ReferralForm` | Employee referral intake form |
| `SourceTrackingLink` | UTM-style tracking URL tied to a source |
| `Candidate` | Central CRM entity — person being recruited |
| `CandidateTag` | Label applied to a candidate |
| `CandidateNote` | Free-text note on a candidate |
| `CandidateProject` | Sourcing project grouping candidates |
| `CandidateSequence` | Outbound sourcing sequence enrollment |
| `Job` | Open role with status, team, compensation, and interview plan |
| `Opening` | Headcount opening tied to a job |
| `JobPosting` | Published job listing for careers pages and job feeds |
| `JobTemplate` | Reusable job definition |
| `Application` | Candidate-job pairing moving through stages |
| `ApplicationHistoryEntry` | Audit trail of stage/status transitions |
| `ApplicationFeedback` | Structured interviewer feedback on an application |
| `CriteriaEvaluation` | AI Application Review scoring result per criterion |
| `InterviewPlan` | Ordered sequence of interview stages for a job |
| `InterviewStage` | Single stage within an interview plan |
| `InterviewStageGroup` | Named group of related stages |
| `Interview` | Interview definition within a stage |
| `InterviewSchedule` | Scheduled interview block with events |
| `InterviewEvent` | Calendar event within a schedule |
| `InterviewerPool` | Named group of interviewers for load balancing |
| `InterviewerPoolMember` | User membership in a pool with optional pause |
| `NotetakerTranscript` | AI Notetaker transcript and drafted feedback |
| `InterviewBriefing` | Pre-interview briefing document |
| `Offer` | Compensation offer extended to a candidate |
| `OfferVersion` | Versioned snapshot of offer terms |
| `CompensationBonus` | Bonus component of an offer |
| `EquityGrant` | Equity component of an offer |
| `CompensationRange` | Min/max salary or rate with currency and interval |
| `ApprovalDefinition` | Reusable multi-step approval workflow definition |
| `ApprovalStep` | Single approver step within a definition |
| `ApprovalWorkflow` | Running instance of an approval definition |
| `ApprovalWorkflowStep` | Step instance tracking decision state |
| `SurveyForm` | Survey or feedback form definition |
| `SurveyQuestion` | Question within a form |
| `SurveyRequest` | Request sent to a candidate or interviewer |
| `SurveySubmission` | Completed submission of a survey request |
| `SurveyAnswer` | Single question response within a submission |
| `Assessment` | Assessment definition (e.g., HackerRank challenge) |
| `AssessmentInstance` | Running instance of an assessment on a candidate |
| `CustomFieldDefinition` | Schema definition for a custom field |
| `CustomFieldSelectableValue` | Option value for select/multi-select fields |
| `CustomFieldValue` | Value set on an entity for a given definition |
| `File` | Metadata for uploaded file (resume, attachment) |
| `PresignedUploadUrl` | Short-lived S3 URL for binary upload |
| `Report` | Generated analytics report |
| `Webhook` | Outbound webhook subscription |
| `WebhookDelivery` | Delivery attempt record for a webhook event |
| `APIKey` | API key with permission module grants |
| `PageInfo` | Cursor-based pagination metadata with sync token |

### Connection Types (15)

`CandidateConnection`, `ApplicationConnection`, `JobConnection`, `OpeningConnection`, `JobPostingConnection`, `InterviewScheduleConnection`, `OfferConnection`, `SurveyRequestConnection`, `WebhookConnection`, `UserConnection`, `DepartmentConnection`, `LocationConnection`, `AssessmentConnection`, `CustomFieldDefinitionConnection`

### Enum Types (16)

`JobStatus`, `ApplicationStatus`, `OfferStatus`, `InterviewScheduleStatus`, `ApprovalStatus`, `WebhookEventType`, `CustomFieldType`, `CustomFieldEntity`, `PermissionModule`, `PermissionScope`, `EmploymentType`, `CompensationInterval`, `AssessmentStatus`, `SurveyStatus`, `ReportFormat`, `ReportStatus`, `OpeningStatus`, `FraudCheckStatus`

### Input Types (14)

`CreateCandidateInput`, `UpdateCandidateInput`, `CreateApplicationInput`, `CreateJobInput`, `CompensationRangeInput`, `CreateInterviewScheduleInput`, `CreateOfferInput`, `CreateWebhookInput`, `UpdateWebhookInput`, `CreateCustomFieldInput`, `SetCustomFieldValueInput`, `GenerateReportInput`, `CreateSurveyRequestInput`, `ApprovalDefinitionInput`, `ApprovalStepInput`, `CreateOpeningInput`

## Key Design Notes

**Pagination:** All list fields follow Relay-style cursor pagination via `PageInfo` with an additional `nextSyncToken` field, mirroring Ashby's syncToken-based incremental sync pattern for delta polling.

**Custom Fields:** The `CustomFieldValue` type appears as a list on `Candidate`, `Application`, `Job`, `Opening`, `Offer`, and `AssessmentInstance`, matching Ashby's flexible custom field data model.

**Approval Workflows:** The schema distinguishes `ApprovalDefinition` (reusable template) from `ApprovalWorkflow` (running instance), matching Ashby's approval definitions API surface.

**AI Features:** `CriteriaEvaluation` captures AI Application Review scoring (outcome + reasoning per criterion). `NotetakerTranscript` surfaces live interview transcripts and AI-drafted structured feedback.

**Webhooks:** The `WebhookEventType` enum enumerates all 22 Ashby webhook event types. Delivery state is tracked in `WebhookDelivery` including retry metadata.

**File Uploads:** The two-step upload pattern (request `PresignedUploadUrl`, then HTTP PUT bytes to S3) is represented by the `requestPresignedUploadUrl` mutation returning a `PresignedUploadUrl` scalar.

**Assessments:** The `Assessment` / `AssessmentInstance` split models Ashby's partner assessment integration surface (SHL, HackerRank, CodeSignal, CoderPad).

## Authentication

The Ashby REST API uses HTTP Basic Auth with the API key as the username and an empty password. In a GraphQL implementation this would map to an `Authorization: Basic <base64(apiKey:)>` header on every request. API keys are scoped to permission modules (Jobs, Candidates, Interviews, Offers, Approvals, Organization, Reports, API Keys) with read or write scope per module, reflected in the `PermissionModuleGrant` type.

## References

- Developer Portal: [https://developers.ashbyhq.com](https://developers.ashbyhq.com)
- API Introduction: [https://developers.ashbyhq.com/docs/introduction](https://developers.ashbyhq.com/docs/introduction)
- Authentication: [https://developers.ashbyhq.com/reference/authentication](https://developers.ashbyhq.com/reference/authentication)
- Webhooks: [https://developers.ashbyhq.com/docs/setting-up-webhooks](https://developers.ashbyhq.com/docs/setting-up-webhooks)
- Pagination and Sync: [https://developers.ashbyhq.com/docs/pagination-and-incremental-sync](https://developers.ashbyhq.com/docs/pagination-and-incremental-sync)
