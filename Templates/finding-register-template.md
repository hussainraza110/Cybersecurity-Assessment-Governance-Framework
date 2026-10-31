---
title: "Security Finding Register Template"
document_type: "Operational Template"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Security Finding Register Template

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Register metadata

| Field | Entry |
|---|---|
| Assessment / engagement ID | [ID] |
| Register owner | [Name / role] |
| Reporting period | [Period] |
| Last updated | [Date/time/time zone] |
| Classification | [Approved classification] |

## 2. Finding register

| Finding ID | Title | Asset / process | Classification | Validation status | Technical severity | Risk ID | Owner | Due date | Status |
|---|---|---|---|---|---|---|---|---|---|
| [ID] | [Title] | [Asset] | [Type] | [Confirmed / probable / unverified / false positive] | [Rating] | [ID] | [Owner] | [Date] | [Status] |

## 3. Detailed finding record

Repeat for each finding.

- **Finding ID and title:** [ID / title]
- **Condition:** [Observed state]
- **Criteria:** [Requirement and source]
- **Cause:** [Only where supported]
- **Consequence / risk scenario:** [Plausible effect]
- **Affected assets and scope:** [Details]
- **Evidence references:** [IDs]
- **Validation method and confidence:** [Details]
- **Technical severity rationale:** [Factors and rubric version]
- **Organizational risk reference:** [Risk ID and current rating]
- **Recommendation:** [Actionable treatment]
- **Compensating controls:** [Details]
- **Owner / target date:** [Details]
- **Management response:** [Details]
- **Retest criteria and result:** [Details]
- **Closure decision / authority:** [Details]

## 4. Status definitions

Use organization-approved values. Suggested lifecycle: Draft → Under validation → Confirmed → Assigned → In remediation → Pending retest → Closed. Other states may include Disputed, False positive, Not applicable, Risk accepted, Deferred under approved exception, or Reopened. Record status history rather than overwriting material decisions.

## 5. Aging and escalation

| Finding ID | Days open | Target date | Overdue? | Escalation owner | Latest action |
|---|---:|---|---|---|---|
| [ID] | [Number] | [Date] | [Yes / no] | [Owner] | [Action] |

## 6. Register reconciliation

Reconcile counts by severity, status and owner to the assessment report and remediation records. Explain duplicates, reopened findings, merged records, exclusions and rating changes.

## Related framework documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
