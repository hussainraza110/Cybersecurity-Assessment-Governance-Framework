---
title: "Third-Party Security Assessment Template"
document_type: "Operational Template"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Third-Party Security Assessment Template

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Supplier and service profile

| Field | Entry |
|---|---|
| Supplier legal name | [Name] |
| Service / product | [Description] |
| Business sponsor | [Name / role] |
| Contract / procurement ID | [Reference] |
| Assessment ID | [ID] |
| Assessment date / reviewer | [Date / name] |
| Service criticality | [Rating] |

## 2. Data, access and dependency profile

- Data categories and sensitivity: [Details]
- Data subjects / volumes: [Details]
- Processing and storage locations: [Regions]
- Access types and privileges: [Details]
- Network / API / administrative connectivity: [Details]
- Subprocessors and dependencies: [List]
- Business continuity dependency and exit complexity: [Details]

## 3. Inherent supplier risk

Assess service criticality, data sensitivity, access, external exposure, concentration, substitutability, jurisdiction and impact of compromise or outage. Record tier, rationale and approver.

## 4. Due diligence evidence

| Domain | Evidence requested | Evidence received / date | Scope and validity | Gap / conclusion |
|---|---|---|---|---|
| Governance and risk | [Policy / assurance] | [Details] | [Details] | [Result] |
| Identity and access | [MFA / privileged access] | [Details] | [Details] | [Result] |
| Vulnerability management | [Process / metrics] | [Details] | [Details] | [Result] |
| Logging and incident response | [Evidence] | [Details] | [Details] | [Result] |
| Resilience and backups | [Test results] | [Details] | [Details] | [Result] |
| Data protection | [Encryption / deletion] | [Details] | [Details] | [Result] |
| Subprocessors / location | [List / regions] | [Details] | [Details] | [Result] |

## 5. Risk and control-gap assessment

For each gap, record condition, evidence, impact scenario, likelihood, impact, existing safeguards, residual risk, proposed treatment, owner and due date. Link to the risk register.

## 6. Contractual and onboarding conditions

Assess security schedule, confidentiality, data processing, breach cooperation and notification, audit/assurance rights, vulnerability disclosure, subcontracting, data location, return/deletion, continuity and termination. Legal/Procurement validates contractual terms.

## 7. Decision

[Approve / conditional approval / reject / defer]  
Conditions precedent: [List]  
Residual risk owner and delegated authority: [Details]  
Approval evidence and date: [Reference]

## 8. Ongoing monitoring and reassessment

Review cadence, assurance expiry, material-change notification, incidents, performance indicators, remediation tracking, reassessment triggers and offboarding requirements: [Details]

## Related framework documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
