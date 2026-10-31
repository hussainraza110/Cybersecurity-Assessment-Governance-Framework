---
title: "Sample Third-Party Security Assessment"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Third-Party Security Assessment

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## 1. Supplier profile

| Field | Illustrative value |
|---|---|
| Supplier | Contoso Backup Services (fictional) |
| Service | Managed backup and recovery |
| Business sponsor | IT Operations Manager |
| Data handled | Encrypted production backup data |
| Connectivity | Management API and support access |
| Inherent risk tier | High |
| Assessment ID | NS-TP-009 |

## 2. Inherent risk rationale

The supplier stores copies of production information, provides a critical recovery service, and has administrative connectivity. A compromise or prolonged outage could affect confidentiality, integrity, and service availability.

## 3. Due diligence evidence

| Evidence | Review result |
|---|---|
| Independent assurance report | Received; scope and reporting period reviewed |
| Vulnerability management summary | Received; remediation detail incomplete |
| Incident response summary | Received; escalation contacts provided |
| Business continuity test | Received; recovery evidence requires clarification |
| Subprocessor list | Received; one hosting region requires confirmation |
| Contract security schedule | Draft; notification and deletion clauses need strengthening |

## 4. Control assessment

| Domain | Result | Gap / action |
|---|---|---|
| Identity and privileged access | Partial | Require named support accounts and MFA evidence |
| Encryption | Partial | Confirm key ownership and separation |
| Logging and monitoring | Partial | Define customer log access and incident evidence |
| Resilience | Partial | Obtain restore test scope and results |
| Incident notification | Gap | Agree notification trigger and contractual timeframe |
| Data location / subprocessors | Gap | Confirm region and subprocessor approval rights |

## 5. Risk treatment and decision

The business sponsor proposes conditional onboarding only after contractual safeguards, MFA evidence, data-location confirmation, and recovery-test evidence are resolved. Until approved, production backup data must not be transferred and privileged connectivity must not be enabled.

**Decision:** Pending approval by the delegated risk authority. Supplier acceptance must not be inferred from completion of the questionnaire.

## 6. Ongoing assurance

Define assurance expiry, annual or risk-based review, material-change notifications, incident cooperation, vulnerability remediation evidence, and exit arrangements. Reassess after incidents, ownership changes, new subprocessors, data-location changes, or material service changes.

## 7. Offboarding

Revoke credentials and connectivity, retrieve required data, obtain deletion or return confirmation, resolve outstanding incidents, and preserve records under retention and legal-hold requirements.

## Related framework documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
- `templates/risk-register-template.md`
- `templates/assessment-report-template.md`
- `templates/evidence-register-template.md`
