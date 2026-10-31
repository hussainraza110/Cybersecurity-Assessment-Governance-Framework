---
title: "Security Remediation Workflow"
document_type: "Workflow"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Security Remediation Workflow

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## 1. Purpose

This workflow maps the operational sequence for finding → risk decision → plan → change → validate → closure. It supplements, and does not replace, the governing policy, procedure, authorization, or risk decision.

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
    N1["Receive validated finding"]
    N2["Link to risk and affected assets"]
    N3["Prioritize using approved risk criteria"]
    N4["Assign accountable owner and due date"]
    N5["Select corrective or compensating treatment"]
    N6["Test and approve change"]
    N7["Implement remediation"]
    N8["Validate effectiveness"]
    N9["Update finding and risk records"]
    N10["Close or reopen"]
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 --> N5
    N5 --> N6
    N6 --> N7
    N7 --> N8
    N8 --> N9
    N9 --> N10
    D1{"Treatment approved?"}
    N5 --> D1
    D1 -- No --> X1["Reassess options / escalate risk"]
    D1 -- Yes --> N6
    D2{"Validation passed?"}
    N8 --> D2
    D2 -- No --> X2["Reopen remediation"]
    D2 -- Yes --> N9
```

## 5. Process stages

### 1. Receive validated finding

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 2. Link to risk and affected assets

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 3. Prioritize using approved risk criteria

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 4. Assign accountable owner and due date

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 5. Select corrective or compensating treatment

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 6. Test and approve change

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 7. Implement remediation

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 8. Validate effectiveness

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 9. Update finding and risk records

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 10. Close or reopen

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

## 6. Decision points

- **Treatment approved?** Apply the governing procedure's criteria and record the decision, decision-maker, rationale, and evidence.
- **Change successful?** Apply the governing procedure's criteria and record the decision, decision-maker, rationale, and evidence.
- **Residual risk accepted by authorized owner?** Apply the governing procedure's criteria and record the decision, decision-maker, rationale, and evidence.

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
