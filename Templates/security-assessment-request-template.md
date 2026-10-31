---
title: "Security Assessment Request Template"
document_type: "Operational Template"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Security Assessment Request Template

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Request details

| Field | Entry |
|---|---|
| Request ID | [Unique identifier] |
| Request date | [YYYY-MM-DD] |
| Requesting business unit | [Unit] |
| Requester / role | [Name / role] |
| Business sponsor | [Name / role] |
| Assessment type | [Infrastructure / application / cloud / control / supplier / other] |
| Desired assessment window | [Start–end / time zone] |
| Business priority and rationale | [Details] |

## 2. Business objective and drivers

- Business purpose: [Why is the assessment required?]
- Trigger: [Periodic / material change / incident / regulatory / new service / other]
- Decisions the assessment must support: [Details]
- Relevant obligations or contractual requirements: [Details]

## 3. Proposed scope

| In-scope asset / service / process | Owner | Environment | Identifier / location | Criticality / data sensitivity |
|---|---|---|---|---|
| [Item] | [Owner] | [Prod / non-prod] | [ID] | [Rating] |

**Proposed exclusions:** [List and rationale]  
**Third-party involvement:** [Supplier, contact, permission evidence]  
**Dependencies and interfaces:** [Details]

## 4. Assessment objectives and criteria

| Objective | Criteria / policy / standard | Expected evidence or outcome |
|---|---|---|
| [Objective] | [Reference and edition] | [Outcome] |

## 5. Proposed methods and constraints

- Proposed methods: [Review / scan / configuration inspection / interview / testing]
- Intrusive activities requested: [Precisely describe; default is not authorized]
- Production constraints and blackout windows: [Details]
- Data access or sensitive-data considerations: [Details]
- Required accounts / connectivity: [Details]
- Safety, rollback and stop conditions: [Details]

## 6. Stakeholders and communications

| Role | Name / team | Contact route | Responsibility |
|---|---|---|---|
| Business owner | [Entry] | [Entry] | [Entry] |
| Technical owner | [Entry] | [Entry] | [Entry] |
| Information Security | [Entry] | [Entry] | [Entry] |
| Change / operations | [Entry] | [Entry] | [Entry] |

## 7. Requested outputs

[Report / findings register / risk assessment / retest / executive briefing / other]

## 8. Initial review and disposition

| Reviewer | Decision | Conditions / rationale | Date |
|---|---|---|---|
| Information Security | [Pending / accepted / returned] | [Details] | [Date] |
| Business / service owner | [Pending / accepted / returned] | [Details] | [Date] |

**Request status:** [Submitted / clarification required / approved for authorization review / rejected]

> Submission of this request does not authorize assessment activity. Written authorization and applicable rules of engagement are required before execution.

## 9. Related records

- Authorization ID: [Reference]
- Assessment plan ID: [Reference]
- Risk ID(s): [Reference]
- Change ID(s): [Reference]

## Related framework documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
