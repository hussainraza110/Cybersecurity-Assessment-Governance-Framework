---
title: "Security Remediation Plan and Verification Template"
document_type: "Operational Template"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Security Remediation Plan and Verification Template

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Remediation record

| Field | Entry |
|---|---|
| Remediation ID | [ID] |
| Finding ID(s) | [IDs] |
| Risk ID(s) | [IDs] |
| Asset / service | [Details] |
| Accountable owner | [Name / role] |
| Priority / target date | [Rating / date] |
| Status | [Status] |

## 2. Risk and treatment decision

- Validated condition: [Summary]
- Current organizational risk and rationale: [Reference]
- Selected treatment: [Mitigate / avoid / share / accept]
- Alternatives considered: [Details]
- Residual risk target and constraints: [Details]

## 3. Remediation actions

| Action ID | Corrective / compensating action | Owner | Dependency | Target date | Completion evidence |
|---|---|---|---|---|---|
| [ID] | [Action] | [Owner] | [Dependency] | [Date] | [Reference] |

## 4. Change and implementation controls

- Change record and approval: [Reference]
- Test plan and acceptance criteria: [Details]
- Backup / rollback: [Details]
- Maintenance window and communications: [Details]
- Emergency change basis, if applicable: [Details]
- Implementation result and deviations: [Details]

## 5. Verification and retest

| Criterion | Verification method | Expected result | Actual result | Evidence ID | Pass / fail |
|---|---|---|---|---|---|
| [Criterion] | [Method] | [Result] | [Result] | [ID] | [Status] |

Verifier independent of implementer, where proportionate: [Name / role]  
Retest limitations: [Details]

## 6. Residual risk reassessment

Record updated likelihood, impact, rationale, control evidence, remaining exposure, uncertainty and risk owner decision. Do not lower a rating solely because a change ticket is closed.

## 7. Closure or reopening

Closure criteria: [Criteria]  
Finding status: [Closed / pending / reopened]  
Closure approver and authority: [Name / role / basis]  
Reopening triggers: failed validation, configuration drift, recurrence, new exposure or contradictory evidence.

## 8. Exception linkage

If remediation is deferred, attach an approved time-bound exception and risk acceptance record. A target date change alone is not risk acceptance.

## Related framework documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
