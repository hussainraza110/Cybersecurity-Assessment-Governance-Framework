---
title: "Sample Security Assessment Report"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Security Assessment Report

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## 1. Executive summary

Northstar Services commissioned a scoped security assessment of its customer portal and supporting production environment. The illustrative assessment identified two high-priority findings, three moderate findings, and two observations. The most material issues were overly broad administrative access to a production management interface and incomplete centralized logging for a critical database tier.

The assessment was limited to configuration review, authenticated vulnerability assessment, identity review, and selected application tests. It was not a full penetration test, source-code audit, or certification audit. No destructive testing was performed.

## 2. Engagement and scope

| Attribute | Illustrative value |
|---|---|
| Assessment ID | NSA-2026-014 |
| Organization | Northstar Services (fictional) |
| Assessment period | 5–16 October 2026 |
| Scope | Customer portal, two Linux VMs, PostgreSQL production database, identity tenant, firewall rules |
| Exclusions | Corporate user endpoints, physical facilities, source-code review, supplier internal systems |
| Authorization | AUTH-2026-014 (fictional) |
| Assessment lead | Security Assurance Lead |
| Report status | Draft illustrative report |

## 3. Objectives and criteria

Assess exposure, identity controls, secure configuration, vulnerability posture, logging coverage, and remediation governance against approved organizational policies and tailored control criteria. The assessment used the Technical Security Assessment Methodology and Security Control Assessment Methodology.

## 4. Methods and limitations

Methods included configuration inspection, authenticated scanning, firewall rule review, selected authentication and authorization tests, database audit configuration review, and evidence interviews. Evidence was collected under the Evidence Handling Methodology. Sampled configurations were not a census of every production component. The application assessment did not include source-code analysis or exhaustive business-logic testing.

## 5. Results summary

| ID | Finding | Classification | Severity | Status |
|---|---|---|---|---|
| NSA-F01 | Management interface reachable from broad internal network ranges | Access / network configuration | High | Open |
| NSA-F02 | Database audit events not centrally collected | Logging / monitoring gap | High | Open |
| NSA-F03 | Two Linux packages outside approved patch target | Vulnerability | Moderate | Open |
| NSA-F04 | Quarterly privileged access review evidence incomplete | Access governance | Moderate | Open |
| NSA-F05 | Backup restore test not evidenced for one database | Resilience | Moderate | Open |
| NSA-O01 | Asset owner field missing for one non-production VM | Observation | Informational | Open |
| NSA-O02 | Security awareness completion below internal target | Process observation | Informational | Open |

## 6. Detailed finding example

### NSA-F01 — Management interface reachable from broad internal network ranges

**Condition:** The management interface for the customer portal accepted connections from a general employee network segment rather than the designated administration subnet.

**Criteria:** Administrative interfaces must be restricted to authorized management paths and least-privileged source networks.

**Evidence:** EV-014-07 firewall rule export; EV-014-08 connection test record; EV-014-09 network diagram. These are fictional references.

**Impact scenario:** A compromised workstation on the broad internal segment could reach the management interface, increasing the opportunity for credential attack or exploitation.

**Severity rationale:** High technical severity due to privileged interface exposure and broad reachable population. Organizational risk must be separately confirmed by the risk owner using the approved scoring model.

**Recommendation:** Restrict the interface to the approved administration subnet, require MFA, review administrative identities, and monitor access attempts.

**Owner:** Infrastructure Manager. **Target:** [Organization-approved date]. **Retest:** Verify network reachability from authorized and unauthorized segments and inspect the final firewall configuration.

## 7. Management response

Management agrees with NSA-F01 and NSA-F02. NSA-F03 will be addressed in the next approved maintenance window. NSA-F04 requires reconciliation with the identity governance team. NSA-F05 will be closed only after a witnessed restore test and evidence review.

## 8. Conclusion

The fictional assessment indicates that several security controls require improvement. The conclusion is limited to the scope, period, methods, and evidence described. It does not establish overall compliance or assurance over excluded systems.

## 9. Distribution and approval

Distribution: Northstar executive sponsor, IT operations, Information Security, and designated risk owners. Approval and acceptance fields must be completed by the fictional organization before this example is reused.

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
