---
title: "Assessment Authorization and Rules of Engagement Template"
document_type: "Operational Template"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Assessment Authorization and Rules of Engagement Template

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Authorization record

| Field | Entry |
|---|---|
| Authorization ID | [Unique ID] |
| Request / assessment ID | [Reference] |
| Authorizing organization | [Legal entity / business unit] |
| Authorized assessor(s) | [Names / organization] |
| Service / system owner | [Name / role] |
| Effective period | [Start/end date, time zone] |
| Authorization status | [Draft / approved / suspended / expired / revoked] |

## 2. Explicit scope

| Asset / domain | Exact identifier, address, account or boundary | Environment | Owner |
|---|---|---|---|
| [Asset] | [Exact scope] | [Environment] | [Owner] |

**Explicit exclusions:** [Assets, tenants, networks, accounts, data, locations, third-party systems]  
**Third-party permission:** [Evidence and constraints]  
**Scope-change process:** [Who can approve and how]

## 3. Authorized activities

For each activity, specify permitted method, target, time window, intensity, source, and constraints.

| Activity | Authorized? | Limits / methods | Window | Stop condition |
|---|---|---|---|---|
| Passive discovery | [Yes / No] | [Limits] | [Window] | [Condition] |
| Vulnerability scanning | [Yes / No] | [Rate / credentials] | [Window] | [Condition] |
| Authenticated review | [Yes / No] | [Account / privilege] | [Window] | [Condition] |
| Exploitation / validation | [Yes / No] | [Exact permitted tests] | [Window] | [Condition] |
| Social engineering | [Yes / No] | [Explicit scenario] | [Window] | [Condition] |
| Denial-of-service / destructive tests | **Not authorized unless separately and explicitly approved** | [If separately approved] | [Window] | [Condition] |

## 4. Safety and operational controls

- Approved source addresses and tools: [Details]
- Rate limits and concurrency: [Details]
- Production safeguards / backups: [Details]
- Sensitive data handling: [Details]
- Emergency contacts and escalation: [Details]
- Stop-work triggers: unexpected impact, scope uncertainty, sensitive-data exposure, suspected active incident, or instruction from authorized owner.
- Stop-work notification and restart approval: [Process]

## 5. Evidence and data handling

Specify collection permissions, data minimization, storage location, access list, transfer method, retention, legal hold and disposal requirements. Reference `docs/methodology/evidence-handling.md`.

## 6. Communications

| Event | Recipient | Channel | Required timing |
|---|---|---|---|
| Start / completion | [Contact] | [Channel] | [Timing] |
| Critical finding | [Contact] | [Channel] | [Timing] |
| Service impact / stop work | [Contact] | [Channel] | Immediate / [local rule] |
| Suspected incident | [Incident route] | [Channel] | Immediate / [local rule] |

## 7. Approval

| Approver | Authority basis | Decision | Conditions | Date |
|---|---|---|---|---|
| Business / system owner | [Delegation] | [Approved / rejected] | [Details] | [Date] |
| Information Security | [Delegation] | [Approved / rejected] | [Details] | [Date] |
| Third-party owner, if required | [Contract / permission] | [Approved / rejected] | [Details] | [Date] |

**Authorization statement:** The signatories authorize only the activities, assets, personnel and period explicitly identified above. This record does not authorize activity against excluded assets or beyond its effective period.

## 8. Change, suspension and closure

Record amendments, renewed approvals, stop-work events, revocation, expiration and final closure. Retain the signed authorization and version history.

## Related framework documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
