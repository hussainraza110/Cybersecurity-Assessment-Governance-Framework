---
title: "Security Incident Record Template"
document_type: "Operational Template"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Security Incident Record Template

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Incident identification

| Field | Entry |
|---|---|
| Incident ID | [Unique ID] |
| Reported / detected | [Date/time/time zone] |
| Reporter / source | [Details] |
| Incident coordinator | [Name / role] |
| Severity | [Organization-approved scale] |
| Status | [Reported / triage / active / contained / recovery / closed] |
| Classification | [Approved classification] |

## 2. Initial report and triage

- What happened / observed indicators: [Details]
- Affected assets, accounts, services and locations: [Details]
- Initial scope and confidence: [Details]
- Potential confidentiality, integrity and availability impact: [Details]
- Safety, operational and business impact: [Details]
- Event or incident decision and rationale: [Details]
- Immediate actions and decision-maker: [Details]

## 3. Timeline

| Date/time/time zone | Event / action | Actor | Evidence reference | Decision / result |
|---|---|---|---|---|
| [Time] | [Event] | [Actor] | [ID] | [Result] |

## 4. Response actions

| Phase | Action | Owner | Start/end | Outcome / evidence |
|---|---|---|---|---|
| Containment | [Action] | [Owner] | [Times] | [Result] |
| Investigation | [Action] | [Owner] | [Times] | [Result] |
| Eradication | [Action] | [Owner] | [Times] | [Result] |
| Recovery | [Action] | [Owner] | [Times] | [Result] |

## 5. Evidence and investigation

Evidence register / case reference: [ID]  
Collection authority and scope: [Reference]  
Preservation, integrity, access and custody details: [Reference]  
Findings, indicators, root-cause confidence and unresolved questions: [Details]

## 6. Impact and notification assessment

Affected data subjects / records / services: [Details]  
Business and operational impact: [Details]  
Legal, regulatory, contractual and privacy assessment owner: [Role]  
Notification decision, basis and deadlines: [Record validated by Legal/Privacy]  
Communications and recipients: [Details]

## 7. Recovery validation

- Recovery acceptance criteria: [Criteria]
- Service / data integrity validation: [Evidence]
- Monitoring and heightened observation: [Period]
- Residual risk and owner: [Details]

## 8. Lessons learned and actions

| Action | Priority | Owner | Target date | Tracking ID | Status |
|---|---|---|---|---|---|
| [Action] | [Priority] | [Owner] | [Date] | [ID] | [Status] |

## 9. Closure approval

Closure rationale, outstanding actions, evidence retention, notification completion and residual risk: [Details]  
Incident lead: [Name/date]  
Service owner: [Name/date]  
Approver: [Name / authority / date]

## Related framework documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
