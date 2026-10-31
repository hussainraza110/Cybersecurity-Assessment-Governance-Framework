---
title: "Sample Security Exception"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Security Exception

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## 1. Request

| Field | Illustrative entry |
|---|---|
| Exception ID | NS-EX-006 |
| Requirement | Restrict administration to management subnet |
| Requester | Infrastructure Manager |
| Asset | NS-PORTAL-ADMIN |
| Business justification | Temporary vendor support during a migration |
| Requested period | 14 calendar days |
| Risk owner | Customer Services Director |
| Status | Pending approval |

## 2. Scope and rationale

The vendor requests temporary access from a dedicated support source address while the management gateway is being configured. The exception does not authorize access from general networks or any activity outside the approved support task.

## 3. Risk assessment

**Threat scenario:** Unauthorized party compromises vendor credentials or source infrastructure and reaches the management interface.

**Potential impact:** Unauthorized administrative changes, customer data exposure, or service disruption.

**Existing controls:** Named vendor identities, MFA, restricted source address, time-limited firewall rule, session logging, and supervised maintenance window.

**Residual uncertainty:** Vendor endpoint assurance and source-address exclusivity require validation.

## 4. Compensating controls and conditions

1. Permit only the named source address and required destination/port.
2. Require MFA and named individual accounts; prohibit shared credentials.
3. Enable session logging and retain session records under approved schedule.
4. Require business owner approval for each maintenance window.
5. Disable the rule automatically at expiry and verify removal.
6. Review access logs after each session.
7. Revoke immediately if compromise or anomalous activity is suspected.

## 5. Decision

**Decision:** Pending. No exception is effective until an authorized risk owner approves it. The approver must confirm authority against the organization's risk delegation.

| Approval role | Decision | Rationale | Date |
|---|---|---|---|
| System owner | [Pending] | [Comment] | [Date] |
| Information Security | [Pending] | [Comment] | [Date] |
| Risk owner / delegated authority | [Pending] | [Acceptance or rejection] | [Date] |

## 6. Monitoring and expiry

Exception owner: Infrastructure Manager. Review trigger: each vendor session, material change, incident, and before expiry. Expiry: [date/time/time zone]. Renewal requires a fresh risk review and explicit approval; it is not automatic.

## 7. Closure

Record rule removal, account revocation, log review, residual risk status, and closure approval. If the control remains unmet, raise a new treatment decision rather than leaving an expired exception active.

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
