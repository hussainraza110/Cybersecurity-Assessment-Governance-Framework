---
title: "Sample Control Assessment"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Control Assessment

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## 1. Control under assessment

**Control ID:** NS-AC-04  
**Control objective:** Privileged access is approved, restricted, periodically reviewed, and monitored.  
**Scope:** Production portal administrators and database administrators.  
**Period:** 1 July–30 September 2026 (fictional).

## 2. Criteria and test approach

Criteria were derived from the fictional Access Control Policy and Privileged Access Management Procedure. The assessor inspected privileged group membership, approvals, review records, and authentication logs; interviewed the system owner; and sampled 12 privileged identities from a defined population of 18.

## 3. Effectiveness assessment

| Dimension | Conclusion | Rationale |
|---|---|---|
| Design | Effective | Documented approval, least privilege, recertification, and monitoring requirements are defined |
| Implementation | Partially effective | Separate administrator accounts exist, but two service identities lack complete ownership metadata |
| Operating | Partially effective | 10 of 12 sampled identities had current approval evidence; two review records were overdue |

The sample is judgmental and risk-focused; results must not be statistically extrapolated to all 18 identities.

## 4. Evidence

- CA-04-01: Privileged account inventory export.
- CA-04-02: Access approvals for sampled identities.
- CA-04-03: Quarterly access review record.
- CA-04-04: Authentication log sample.
- CA-04-05: Interview notes and owner confirmation.

## 5. Finding

Two sampled privileged identities lacked current review evidence. The assessor could not conclude that all privileged access was periodically recertified. This is a control operation gap; it does not, without further evidence, prove unauthorized use.

## 6. Conclusion

The control is **partially effective** for the defined scope and period. The conclusion is limited by sample design and the two incomplete records. The owner should complete recertification, assign service identity owners, and provide evidence for independent validation.

## 7. Required follow-up

Track remediation under the security remediation procedure. Reassess operating effectiveness after sufficient operating history is available.

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
