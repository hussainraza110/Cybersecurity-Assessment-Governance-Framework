---
title: "Sample Risk Assessment"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Risk Assessment

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## 1. Scenario

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

**Risk ID:** NS-R-017  
**Scenario:** An attacker who obtains access to a general internal workstation network may reach the customer portal's administrative interface because network restrictions are broader than intended.

## 2. Context and assets

- Asset: Customer portal management interface and supporting production service.
- Business owner: Customer Services Director.
- Technical owner: Infrastructure Manager.
- Information: Customer account and service administration data.
- Security objectives: confidentiality, integrity, availability, and service continuity.
- Threat source: External attacker using a compromised internal endpoint or stolen credentials.
- Vulnerability/condition: Administrative interface reachable from broad internal network ranges; MFA coverage requires confirmation.

## 3. Risk statement

Because the administrative interface is reachable from a broad internal network, an attacker with a foothold on an internal workstation may attempt credential abuse or exploit an interface weakness, potentially leading to unauthorized administrative access, customer-data exposure, service manipulation, or outage.

## 4. Inherent risk assessment

| Dimension | Illustrative assessment |
|---|---|
| Likelihood | 4 — Likely, based on reachable attack path and plausible foothold |
| Impact | 4 — Major, considering customer data and service integrity |
| Inherent score | 16 / 25 |
| Inherent band | High, using the repository's illustrative scoring bands |

The likelihood and impact ratings are assumptions for this worked example, not measured probabilities or a universal rating.

## 5. Existing controls and effectiveness

| Control | Design | Implementation | Operation | Evidence |
|---|---|---|---|---|
| Firewall segmentation | Partial | Partial | Ineffective for intended restriction | EV-014-07 |
| MFA for administrators | Appropriate | Partial | Not fully evidenced | EV-014-10 |
| Centralized admin logging | Appropriate | Partial | Partial | EV-014-11 |

Control effectiveness is evaluated separately from the risk score. Missing evidence is not automatically proof that a control does not exist; it creates an assurance limitation requiring follow-up.

## 6. Residual risk

Illustrative residual likelihood: 3 — Possible. Impact remains 4 — Major. Residual score: 12 / 25, High. This rating assumes existing controls provide some restriction but do not eliminate the broad network path. The risk owner must independently validate this rating.

## 7. Treatment decision

**Selected treatment:** Mitigate.

Actions:
1. Restrict administrative access to the designated management subnet.
2. Enforce MFA for all administrative identities.
3. Review and remove unnecessary administrative accounts.
4. Centralize authentication and administrative activity logs.
5. Retest access from authorized and unauthorized network segments.

**Owner:** Infrastructure Manager. **Risk owner:** Customer Services Director. **Target dates:** Set according to approved risk treatment deadlines.

## 8. Acceptance and monitoring

Risk is not accepted by this example. If residual risk remains above tolerance, escalate to the authority specified by the organization's risk governance. Monitor firewall changes, privileged access, authentication alerts, and overdue remediation.

## 9. Assumptions and limitations

This example uses illustrative likelihood and impact judgments. It does not constitute a real risk decision, legal assessment, or guarantee that the scenario is exhaustive.

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
