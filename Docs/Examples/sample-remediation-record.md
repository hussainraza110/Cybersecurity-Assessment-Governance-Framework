---
title: "Sample Remediation Record"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Remediation Record

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## 1. Record summary

| Field | Illustrative value |
|---|---|
| Remediation ID | NS-RM-021 |
| Finding | NSA-F01 |
| Risk reference | NS-R-017 |
| Asset | NS-PORTAL-ADMIN |
| Owner | Infrastructure Manager |
| Status | Verified / pending formal closure |
| Change record | CHG-2026-118 |

## 2. Remediation plan

**Condition:** Administrative interface reachable from broad internal network ranges.

**Selected treatment:** Mitigate by restricting source networks and enforcing MFA.

**Planned work:**
1. Confirm approved management subnet and support dependencies.
2. Prepare firewall change and rollback plan.
3. Validate in test environment or maintenance window.
4. Obtain change and service-owner approval.
5. Implement least-privilege source restrictions.
6. Validate authorized and unauthorized access paths.
7. Review logs and update network documentation.

## 3. Change and test record

| Activity | Result |
|---|---|
| Change approval | Approved by delegated change authority |
| Pre-change backup | Completed |
| Firewall rule update | Completed |
| Authorized management source test | Successful |
| General internal segment test | Denied |
| MFA test | Successful |
| Monitoring validation | Successful |

All values are fictional and should be replaced with actual evidence in operational use.

## 4. Risk reassessment

Reassess residual risk after validating the control's design, implementation, and operation. Do not automatically reduce the risk score merely because a change ticket is closed. Record the new likelihood and impact rationale, remaining exposure, and risk-owner decision.

## 5. Closure checklist

- [x] Change approved and recorded.
- [x] Implementation completed.
- [x] Authorized and unauthorized access paths tested.
- [x] Evidence linked to the finding.
- [ ] Risk owner confirms residual risk and treatment outcome.
- [ ] Finding closure approved by designated authority.

## 6. Reopening criteria

Reopen if unauthorized access remains possible, configuration drifts, MFA is bypassed, monitoring fails, or new evidence contradicts the closure conclusion.

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
