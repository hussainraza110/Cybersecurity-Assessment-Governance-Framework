---
title: "Sample Security Finding"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Security Finding

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## Finding NSA-F01 — Administrative interface exposed to broad internal network ranges

<badge>Illustrative finding</badge>

### Summary

| Field | Value |
|---|---|
| Finding ID | NSA-F01 |
| Classification | Network access-control weakness |
| Status | Confirmed / Open |
| Technical severity | High (illustrative) |
| Affected asset | NS-PORTAL-ADMIN (fictional) |
| Owner | Infrastructure Manager |
| Assessment reference | NSA-2026-014 |

### Condition

The customer portal management interface accepts connections from a general employee network segment. The approved design requires administrative access to originate only from the designated management subnet.

### Criteria

Administrative interfaces must be restricted to authorized management paths, least-privileged source networks, and strong authentication under the applicable Network Security Policy and Access Control Policy.

### Evidence

- EV-014-07: Firewall rule export showing broad source network.
- EV-014-08: Controlled connection test from a general internal test segment.
- EV-014-09: Approved network architecture diagram.

All evidence identifiers and results are fictional. A real report must include collection date, source, collector, integrity and handling details as appropriate.

### Risk scenario and impact

A compromised internal endpoint or stolen user credential may provide a path to the administrative interface. If authentication or application controls are subsequently bypassed, an attacker may alter portal configuration, access customer information, or disrupt service.

### Severity rationale

High technical severity is assigned because the interface is privileged and reachable from a broad population. Organizational likelihood and impact must be rated separately using the approved Risk Assessment Methodology and Risk Scoring Model.

### Recommendation

1. Restrict the interface to the designated management subnet or approved privileged access gateway.
2. Enforce MFA and separate administrative identities.
3. Review administrative group membership.
4. Alert on denied and successful management-interface access.
5. Retest reachability and authentication controls.

### Retest criteria

- Connection from an authorized management source succeeds.
- Connection from unauthorized segments is denied.
- Administrative authentication requires the approved MFA method.
- Firewall configuration and relevant logs corroborate the result.

### Management response

[Owner response, planned actions, target dates, and any disagreement.]

### Closure

Close only after independent retest evidence supports resolution or an authorized risk acceptance is recorded. Retain the original finding and all status transitions.

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
