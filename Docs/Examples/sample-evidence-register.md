---
title: "Sample Evidence Register"
document_type: "Illustrative Example"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Sample Evidence Register

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## Important notice

**Illustrative scenario:** Northstar Services (fictional) operates a customer portal, an internal application, a PostgreSQL database, Linux virtual machines, a Microsoft Entra ID tenant, a perimeter firewall, and a managed backup service. The organization has 420 staff and serves business customers. All names, systems, addresses, events, evidence IDs, scores, dates, and decisions below are fictional and must not be represented as real assessment results.

This document demonstrates how the framework may be applied. It is not an actual assessment, security finding, risk acceptance, incident, supplier review, or statement about a real organization. Replace all scenario details and obtain the required authorization and approvals before operational use.

## 1. Fictional evidence records

| Evidence ID | Description | Source / method | Collected by | Date/time (UTC) | Validation | Integrity reference | Classification |
|---|---|---|---|---|---|---|---|
| EV-014-07 | Firewall rule export | Approved management console export | Assessor A | 2026-10-08 09:20 | Compared to active rule ID | SHA-256 recorded in case store | Internal |
| EV-014-08 | Network reachability test | Controlled connection test from authorized test host | Assessor B | 2026-10-08 10:05 | Source and destination confirmed | Test log hash recorded | Internal |
| EV-014-09 | Network architecture diagram | Approved architecture repository | System Owner | 2026-10-08 11:10 | Version and owner confirmed | Repository version ID | Internal |
| EV-014-10 | Privileged group membership | Identity platform export | IAM Analyst | 2026-10-09 08:30 | Reconciled to group object | Export hash recorded | Confidential |
| EV-014-11 | Database audit configuration | Database audit settings export | DBA | 2026-10-09 12:00 | Compared with active configuration | Export hash recorded | Confidential |

## 2. Provenance and handling notes

These records are illustrative. In a real engagement, capture the collection tool and version where material, exact source, query or command, scope, time zone, collector, transfer history, storage location, working-copy relationship, and integrity method.

A hash can support integrity verification after collection but does not by itself prove source authenticity, completeness, or correctness.

## 3. Evidence-to-finding traceability

| Finding | Supporting evidence |
|---|---|
| NSA-F01 | EV-014-07, EV-014-08, EV-014-09 |
| NSA-F04 | EV-014-10 |
| NSA-F02 | EV-014-11 |

## 4. Handling controls

- Store evidence in an access-controlled case repository.
- Preserve originals and analyze working copies where appropriate.
- Restrict access according to classification and engagement authorization.
- Record transfers and custody where material to reliability or legal defensibility.
- Retain according to approved schedule and legal holds.
- Dispose securely when authorized retention ends.

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
