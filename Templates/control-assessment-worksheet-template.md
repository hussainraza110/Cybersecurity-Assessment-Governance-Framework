---
title: "Control Assessment Worksheet Template"
document_type: "Operational Template"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Control Assessment Worksheet Template

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Assessment identification

| Field | Entry |
|---|---|
| Assessment ID | [ID] |
| Control ID / title | [ID / title] |
| Control owner | [Name / role] |
| Assessor / reviewer | [Name / role] |
| Assessment period | [Period] |
| Scope / population | [Details] |
| Criteria source and edition | [Reference] |

## 2. Control objective and testable criteria

**Control objective:** [Desired security outcome]  
**Control statement:** [What the organization expects]  
**Applicability and boundaries:** [Systems, locations, processes, exclusions]

| Criterion ID | Testable requirement | Expected evidence |
|---|---|---|
| [C-01] | [Requirement] | [Evidence] |

## 3. Design assessment

- Is the control capable of addressing the stated risk?
- Are responsibilities, frequency, trigger, exception and escalation defined?
- Are dependencies and failure modes addressed?
- Design conclusion: [Effective / Partially effective / Ineffective / Not assessed]
- Rationale and evidence: [References]

## 4. Implementation assessment

| Test step | Procedure | Expected result | Actual result | Evidence ID | Conclusion |
|---|---|---|---|---|---|
| [Step] | [Method] | [Expected] | [Observed] | [ID] | [Result] |

Implementation conclusion: [Rating]  
Rationale and coverage limitations: [Details]

## 5. Operating effectiveness assessment

| Period / sample item | Test performed | Result | Exception / deviation | Evidence ID |
|---|---|---|---|---|
| [Item] | [Procedure] | [Pass / fail / unable] | [Details] | [ID] |

Population and sampling method: [Details]  
Operating conclusion: [Rating]  
Rationale, exceptions and expansion decision: [Details]

## 6. Overall conclusion and risk linkage

Do not combine the three dimensions without explanation.

| Dimension | Rating | Rationale |
|---|---|---|
| Design | [Rating] | [Basis] |
| Implementation | [Rating] | [Basis] |
| Operating | [Rating] | [Basis] |

Related finding IDs: [IDs]  
Related risk IDs: [IDs]  
Residual risk assessment reference: [ID]

## 7. Management response and actions

| Action | Owner | Due date | Verification evidence |
|---|---|---|---|
| [Action] | [Owner] | [Date] | [Evidence] |

## 8. Review and sign-off

Assessor: [Name / date]  
Independent reviewer: [Name / date]  
Control owner factual response: [Response / date]  
Approver, if required: [Name / authority / date]

## 9. Limitations and reassessment triggers

Record evidence gaps, scope restrictions, assumptions, material changes, incidents, control failures and date for reassessment.

## Related framework documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
