---
title: "Sample Security Incident Report"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Security Incident Report

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## 1. Incident summary

| Field | Illustrative value |
|---|---|
| Incident ID | NS-IR-2026-003 |
| Severity | High (fictional organization scale) |
| Status | Closed after review |
| Detection | 2026-10-12 08:14 UTC |
| Affected service | Customer portal administration |
| Incident lead | Security Incident Coordinator |
| Report classification | Internal |

## 2. Executive summary

Northstar Services detected unusual authentication attempts against a privileged portal account followed by a successful login from an unrecognized source. The account was disabled, active sessions revoked, and the management interface restricted while investigation proceeded. The fictional investigation found no verified evidence of customer data exfiltration, but log coverage gaps limited confidence in that conclusion.

## 3. Timeline

| Time (UTC) | Event |
|---|---|
| 08:14 | SIEM alert for unusual privileged authentication |
| 08:22 | Service desk escalated to incident coordinator |
| 08:31 | Incident declared; response lead assigned |
| 08:42 | Privileged account disabled and sessions revoked |
| 09:05 | Management interface restricted to approved subnet |
| 10:20 | Identity and endpoint evidence collected |
| 13:30 | Credential reset and endpoint review completed |
| 16:00 | Service owner validated portal operations |
| Next day | Lessons-learned review initiated |

## 4. Impact and scope

Affected: one privileged identity and customer portal management interface. No verified customer data alteration or exfiltration was identified in available evidence. The absence of evidence is not proof that no data access occurred because database audit telemetry was incomplete.

## 5. Response actions

- Containment: disable identity, revoke sessions, restrict network access.
- Investigation: review identity logs, endpoint telemetry, firewall events, and available application logs.
- Eradication: reset credentials, remove stale sessions, validate endpoint.
- Recovery: restore authorized administration through controlled access.
- Communications: notify internal stakeholders under the incident communication plan.

## 6. Notification assessment

Legal, regulatory, contractual, and privacy notification obligations must be assessed by designated Legal/Privacy roles using verified facts and applicable deadlines. This example does not make a legal determination.

## 7. Root cause and contributing factors

Likely contributing factors in the fictional scenario: broad internal network reachability, credential exposure, and incomplete centralized database audit coverage. Root cause should not be stated as confirmed without sufficient evidence.

## 8. Lessons and actions

| Action | Owner | Priority | Status |
|---|---|---|---|
| Enforce privileged MFA and separate admin accounts | IAM Owner | High | Complete |
| Restrict management interface source networks | Network Owner | High | Complete |
| Centralize database audit events | DBA | High | Open |
| Review privileged access quarterly | System Owner | Moderate | Open |
| Test alert coverage and escalation | Security Operations | Moderate | Planned |

## 9. Closure and limitations

Incident closure requires documented containment, eradication, recovery validation, evidence preservation, communications assessment, residual risk, and action ownership. The report must disclose telemetry gaps and unresolved questions.

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
