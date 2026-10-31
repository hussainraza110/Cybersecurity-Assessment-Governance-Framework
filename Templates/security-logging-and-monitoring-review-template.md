---
title: "Security Logging and Monitoring Review Template"
document_type: "Operational Template"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Security Logging and Monitoring Review Template

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Review metadata

| Field | Entry |
|---|---|
| Review ID | [ID] |
| Period | [Start/end] |
| Reviewer | [Name / role] |
| Service / environment | [Details] |
| SIEM / platform | [Name/version] |
| Scope approval | [Reference] |

## 2. Log-source coverage

| Source ID | System / owner | Required events | Collection path | Last event | Parsing / time sync | Health status |
|---|---|---|---|---|---|---|
| [ID] | [Source] | [Events] | [Path] | [Timestamp] | [Result] | [Status] |

## 3. Security event and detection review

| Detection ID / use case | Data sources | Test date | Expected behavior | Observed result | False positive / gap | Owner |
|---|---|---|---|---|---|---|
| [ID] | [Sources] | [Date] | [Expected] | [Result] | [Details] | [Owner] |

## 4. Alert operations

| Alert ID | Severity | Detection time | Triage time | Disposition | Escalation / incident ID | Closure |
|---|---|---|---|---|---|---|
| [ID] | [Rating] | [Time] | [Time] | [Result] | [Reference] | [Date] |

## 5. Control and platform checks

Review access authorization, privileged activity, log integrity, encryption, time synchronization, retention, archival, retrieval, capacity, backup, source outage alerts, ingestion latency, parsing failures, rule changes and suppression governance.

## 6. Gaps and actions

| Gap ID | Impact / affected coverage | Risk reference | Corrective action | Owner | Due date |
|---|---|---|---|---|---|
| [ID] | [Details] | [ID] | [Action] | [Owner] | [Date] |

## 7. Metrics and conclusion

Report coverage, source freshness, ingestion health, detection test pass rate, alert volume, triage performance, overdue actions and material blind spots. Define calculation and denominator for each metric.

## 8. Review and approval

Reviewer: [Name/date]  
Service owner: [Name/date]  
Information Security approver: [Name/authority/date]

## Related framework documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
