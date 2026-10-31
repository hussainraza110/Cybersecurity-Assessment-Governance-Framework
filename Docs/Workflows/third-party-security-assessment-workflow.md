---
title: "Third-Party Security Assessment Workflow"
document_type: "Workflow"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Third-Party Security Assessment Workflow

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## 1. Purpose

This workflow maps the operational sequence for intake → tier → assess → contract → approve → monitor → exit. It supplements, and does not replace, the governing policy, procedure, authorization, or risk decision.

## 2. Applicability and governing documents

Use this workflow only within approved organizational scope. Relevant governing documents include:

- `docs/policies/information-security-policy.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`

The process owner must identify the specific subject policy and procedure applicable to the activity before use.

## 3. Inputs and prerequisites

- Approved request, business purpose, and scope.
- Identified assets, systems, records, stakeholders, and dependencies.
- Applicable criteria, policy requirements, and procedures.
- Assigned owner, competent personnel, and required access.
- Authorization, change approval, communications, and safety controls where required.

## 4. Workflow diagram

```mermaid
flowchart TD
    N1["Business sponsor submits supplier intake"]
    N2["Characterize service, data and access"]
    N3["Assign inherent risk tier"]
    N4["Collect due diligence and assurance evidence"]
    N5["Assess control gaps and dependencies"]
    N6["Agree contract safeguards and remediation"]
    N7["Approve or reject residual risk"]
    N8["Onboard least-privilege access"]
    N9["Monitor assurance and material changes"]
    N10["Offboard, revoke access and verify data disposition"]
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 --> N5
    N5 --> N6
    N6 --> N7
    N7 --> N8
    N8 --> N9
    N9 --> N10
    D1{"Evidence sufficient for risk tier?"}
    N4 --> D1
    D1 -- No --> X1["Request further assurance"]
    D1 -- Yes --> N5
    D2{"Residual risk approved?"}
    N7 --> D2
    D2 -- No --> X2["Reject, restrict or renegotiate"]
    D2 -- Yes --> N8
```

## 5. Process stages

### 1. Business sponsor submits supplier intake

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 2. Characterize service, data and access

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 3. Assign inherent risk tier

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 4. Collect due diligence and assurance evidence

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 5. Assess control gaps and dependencies

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 6. Agree contract safeguards and remediation

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 7. Approve or reject residual risk

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 8. Onboard least-privilege access

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 9. Monitor assurance and material changes

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 10. Offboard, revoke access and verify data disposition

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

## 6. Decision points

- **Assessment sufficient for tier?** Apply the governing procedure's criteria and record the decision, decision-maker, rationale, and evidence.
- **Residual risk approved?** Apply the governing procedure's criteria and record the decision, decision-maker, rationale, and evidence.
- **Material change or incident?** Apply the governing procedure's criteria and record the decision, decision-maker, rationale, and evidence.

## 7. Roles and accountability

- **Process owner:** maintains the workflow and ensures process steps are implemented.
- **Business / service owner:** confirms business need, scope, dependencies, and operational impact.
- **Information Security:** advises on security requirements, risk, evidence, and escalation.
- **Technical / operational team:** executes assigned activities and records results.
- **Risk owner / approving authority:** makes risk decisions within delegated authority.

Specific role assignment must be documented for each execution. Workflow arrows do not themselves confer approval authority.

## 8. Outputs and records

Maintain the applicable request, authorization, assessment or activity record, decisions, evidence references, exceptions, risk treatment, notifications, and closure record. Protect records under the evidence-handling and retention requirements.

## 9. Exceptions and escalation

If scope, authorization, safety, integrity, or service availability is in doubt, pause the activity and escalate to the accountable owner. Suspected incidents must be handled under the Security Incident Response Procedure. Exceptions require documented risk assessment and authorized acceptance; workflow completion does not imply risk acceptance.

## 10. Review

The process owner must review this workflow with the governing procedure at least annually and after significant process changes, incidents, audit findings, or lessons learned.
