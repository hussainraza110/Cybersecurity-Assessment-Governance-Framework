---
title: "Risk Assessment Workflow"
document_type: "Workflow"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Risk Assessment Workflow

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## 1. Purpose

This workflow maps the operational sequence for identify → analyze → evaluate → treat → accept → monitor. It supplements, and does not replace, the governing policy, procedure, authorization, or risk decision.

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

![Risk Assessment Model](../images/risk-assessment-model.png)

```mermaid
flowchart TD
    N1["Define context, scope and criteria"]
    N2["Identify assets, threats, vulnerabilities and scenarios"]
    N3["Estimate likelihood and impact"]
    N4["Determine inherent risk"]
    N5["Evaluate existing controls"]
    N6["Assess residual risk directly"]
    N7["Compare with appetite and tolerance"]
    N8["Select treatment and assign owner"]
    N9["Approve acceptance or escalate"]
    N10["Monitor and reassess"]
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 --> N5
    N5 --> N6
    N6 --> N7
    N7 --> N8
    N8 --> N9
    N9 --> N10
    D1{"Information sufficient?"}
    N2 --> D1
    D1 -- No --> X1["Collect more information"]
    D1 -- Yes --> N3
    D2{"Within acceptance authority?"}
    N7 --> D2
    D2 -- No --> X2["Escalate to authorized risk owner"]
    D2 -- Yes --> N9
```

## 5. Process stages

### 1. Define context, scope and criteria

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 2. Identify assets, threats, vulnerabilities and scenarios

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 3. Estimate likelihood and impact

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 4. Determine inherent risk

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 5. Evaluate existing controls

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 6. Assess residual risk directly

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 7. Compare with appetite and tolerance

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 8. Select treatment and assign owner

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 9. Approve acceptance or escalate

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

### 10. Monitor and reassess

**Expected output:** A recorded result, decision, or handoff sufficient to proceed to the next stage. If the stage fails, stop or return to the appropriate earlier stage and record the reason.

## 6. Decision points

- **Sufficient information?** Apply the governing procedure's criteria and record the decision, decision-maker, rationale, and evidence.
- **Risk within acceptance authority?** Apply the governing procedure's criteria and record the decision, decision-maker, rationale, and evidence.
- **Treatment reduces risk to approved level?** Apply the governing procedure's criteria and record the decision, decision-maker, rationale, and evidence.

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
