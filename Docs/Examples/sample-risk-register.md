---
title: "Sample Risk Register"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Risk Register

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## 1. Instructions

This fictional extract demonstrates use of the repository's Risk Register Template and Risk Scoring Model. The illustrative scoring bands are not universal thresholds and require organizational approval.

## 2. Fictional register

| Risk ID | Scenario summary | Asset / process | Inherent L×I | Inherent score | Existing control position | Residual L×I | Residual score | Treatment | Owner | Status |
|---|---|---|---:|---:|---|---:|---:|---|---|---|
| NS-R-017 | Broad access to portal administration may enable unauthorized control | Customer portal | 4×4 | 16 High | Partial segmentation; MFA evidence incomplete | 3×4 | 12 High | Mitigate | Customer Services Director | Open |
| NS-R-018 | Missing central database audit telemetry may delay detection | PostgreSQL service | 3×4 | 12 High | Local logs enabled; central collection incomplete | 3×4 | 12 High | Mitigate | Database Owner | Open |
| NS-R-019 | Backup restore capability may not meet recovery needs | Customer database | 3×4 | 12 High | Scheduled backup; restore evidence incomplete | 2×4 | 8 Moderate | Mitigate | IT Operations Manager | In progress |
| NS-R-020 | Supplier assurance evidence may become stale | Managed backup provider | 2×3 | 6 Moderate | Annual review process | 2×3 | 6 Moderate | Monitor | Vendor Manager | Open |

## 3. Rating interpretation

The L×I values use the existing 1–5 likelihood and impact scales. The score is a prioritization aid; it does not replace scenario analysis, documented rationale, uncertainty, control evaluation, or delegated acceptance authority.

## 4. Required register governance

For each live risk, maintain:
- Risk owner and accountable action owner.
- Scenario, cause, event, consequence, affected objectives and assets.
- Inherent and residual likelihood/impact with rationale and assessment horizon.
- Existing controls and design, implementation, and operating evidence.
- Treatment choice, actions, due dates, dependencies, and status.
- Acceptance decision, authority, conditions, expiry, and review trigger where applicable.
- Evidence and finding references, last review, and next review.

## 5. Example review note

NS-R-017 remains High after planned controls because the management interface remains reachable from broad internal ranges. The risk owner has not accepted this exposure. Escalation is required if treatment cannot meet the approved deadline.

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
