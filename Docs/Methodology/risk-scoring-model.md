# Risk Scoring Model

**Document type:** Methodology  
**Status:** Template for organizational review and approval  
**Version:** 1.0  
**Last updated:** 2026-10-29  
**Owner:** To be assigned by the adopting organization  
**Approval authority:** To be defined by the adopting organization

> **Important use note:** This document provides an illustrative semi-quantitative scoring model. The adopting organization must calibrate and formally approve its likelihood and impact criteria, rating bands, risk appetite, escalation criteria, and delegated authorities before operational use. The illustrative numerical examples are not universal thresholds or guarantees of risk magnitude.

## 1. Purpose and Objectives

This document defines a repeatable method for assigning and interpreting information-security risk scores. It supports risk assessment, control evaluation, treatment prioritization, residual-risk decisions, reporting, and reassessment.

The model is designed to:
- Use a consistent five-level likelihood scale and five-level impact scale.
- Calculate a base score using likelihood multiplied by impact.
- Distinguish inherent risk from residual risk.
- Make scoring traceable to scenario context, evidence, assumptions, and control effectiveness.
- Support risk prioritization without treating a score as a substitute for professional judgment or governance.
- Provide an operational record that can be maintained in a risk register or equivalent system.

The model is semi-quantitative. Its scores are structured decision aids, not precise measurements of loss, probability, or organizational risk.

## 2. Scope and Applicability

The model may be used for information-security risk scenarios affecting systems, networks, applications, data, infrastructure, services, business processes, and supporting dependencies. It can support technical assessments, control reviews, architecture reviews, vulnerability assessments, and broader organizational risk assessments.

Each assessment must define its scope and scenario. A score assigned to an asset without a credible scenario and context is not a complete risk assessment.

The adopting organization must adapt the scales and governance rules to its operating environment, risk appetite, legal and regulatory obligations, business objectives, and available evidence. The model does not independently establish compliance with any law, regulation, contract, or external framework.

## 3. Principles and Terminology

### 3.1 Core principles

1. **Scenario-based:** Assess a defined event or sequence of events, its causes, affected assets or processes, and credible consequences.
2. **Evidence-informed:** Use relevant evidence, assumptions, incident history, threat information, exposure, vulnerabilities, and control performance.
3. **Consistent:** Apply approved scales and rating rules consistently, documenting justified exceptions.
4. **Transparent:** Retain the input values and rationale behind every score.
5. **Proportionate:** Scale evidence collection, review, and assurance to risk, uncertainty, and complexity.
6. **Governed:** Keep scoring separate from treatment selection and formal acceptance decisions.
7. **Cautious under uncertainty:** Where uncertainty could conceal material risk, document assumptions and use a defensible conservative estimate where justified.

### 3.2 Terms

- **Risk scenario:** A defined situation describing how a threat or other cause could exploit a condition or weakness and produce consequences for an asset, service, or objective.
- **Likelihood:** The assessed chance or frequency of the defined scenario occurring within the stated assessment horizon.
- **Impact:** The credible consequences if the scenario occurs.
- **Inherent risk:** Risk assessed before taking existing controls into account.
- **Residual risk:** Risk remaining after relevant existing controls and their evidenced effectiveness are considered.
- **Risk score:** The product of the selected likelihood and impact levels.
- **Risk rating:** A category assigned to the score using the organization's approved mapping, subject to documented override or escalation rules.
- **Risk priority:** The urgency of attention, considering the rating and other material factors.
- **Confidence:** The assessor's documented view of the sufficiency and reliability of evidence and assumptions. Confidence is recorded separately from the score.
- **Risk owner:** The person accountable for managing the risk and making or obtaining decisions within delegated authority.

## 4. Model Overview

The scoring process follows this sequence:

1. Define the risk scenario, scope, affected assets or processes, and assessment horizon.
2. Assess inherent likelihood and impact before existing controls are considered.
3. Calculate the inherent score and apply the organization's approved rating mapping.
4. Identify relevant controls and assess their design, implementation, and operating effectiveness.
5. Reassess likelihood and impact after considering supported control effects.
6. Calculate the residual score and assign the corresponding rating.
7. Record confidence, evidence gaps, assumptions, and any override or escalation flag.
8. Determine priority, treatment, ownership, deadlines, and required acceptance authority.
9. Review and reassess periodically and when material changes occur.

The calculated score, rating, priority, and governance disposition are related but distinct outputs. A numerical score does not by itself determine whether risk is acceptable.

## 5. Likelihood Scale and Assessment Horizon

### 5.1 Standard horizon

Use a **one-year assessment horizon** by default. State the horizon in the risk record. If a different horizon is necessary, document the alternative period and why it better fits the scenario or decision. Scores assessed over different horizons should not be compared as if the horizons were identical without explaining the difference.

Likelihood describes the defined scenario within the assessment horizon. It is not merely a statement that a threat exists or that a vulnerability has been identified.

Consider relevant factors such as:
- Threat capability, intent, opportunity, and observed activity where applicable.
- Asset exposure, accessibility, and dependency relationships.
- Vulnerability or weakness and the conditions required for exploitation.
- Existing controls and their evidenced effectiveness.
- Relevant incident history, near misses, and frequency data where meaningful.
- Changes in the operating environment or threat landscape.

### 5.2 Five-level likelihood scale

The following descriptions are illustrative. The adopting organization should add calibrated annual probability or frequency examples where suitable and supported by its data. Do not treat example anchors as universal empirical probabilities.

| Level | Label | General interpretation |
|---:|---|---|
| 1 | Rare | Exceptional under the defined scenario and context during the stated horizon. |
| 2 | Unlikely | Possible, but not expected during the stated horizon. |
| 3 | Possible | A credible occurrence during the stated horizon. |
| 4 | Likely | Expected or repeatedly plausible during the stated horizon. |
| 5 | Almost certain | Expected to occur, or occurring frequently, during the stated horizon. |

When calibrating the scale, document what each level means in the organization's context. If quantitative anchors are adopted, define the unit, period, data source, treatment of sparse data, and limits of comparability. Do not imply more precision than the evidence supports.

## 6. Impact Scale and Impact Dimensions

### 6.1 Dimensions to consider

Assess impact across dimensions relevant to the scenario, including:
- **Confidentiality:** unauthorized disclosure, access, or exposure of information.
- **Integrity:** unauthorized or erroneous alteration, destruction, or loss of trust in information or processing.
- **Availability:** loss or degradation of systems, services, information, or supporting resources.
- **Operational:** interruption of business processes, service delivery, recovery, or dependencies.
- **Financial:** direct loss, response and recovery costs, fraud, lost revenue, or other material financial effects.
- **Legal and regulatory:** consequences arising from applicable laws, regulations, contractual commitments, or formal obligations.
- **Reputational:** loss of trust or other material harm to stakeholder relationships.
- **Critical services and objectives:** consequences for essential services, safety-relevant functions where applicable, and business objectives.

Not every dimension will apply to every scenario. Record the dimensions considered and explain those that drive the result.

### 6.2 Five-level impact scale

The descriptions below are generic starting points. The adopting organization must define practical criteria for its context, including measurable thresholds where appropriate and supportable.

| Level | Label | General interpretation |
|---:|---|---|
| 1 | Negligible | Minimal, localized, and readily recoverable consequence with no material disruption or obligation breached. |
| 2 | Minor | Limited adverse effect, manageable through routine response, with restricted operational or business consequences. |
| 3 | Moderate | Material but manageable disruption, loss, or harm requiring coordinated response or recovery. |
| 4 | Major | Serious disruption, substantial loss, significant harm, or consequences requiring senior management attention. |
| 5 | Severe | Extensive or critical consequences, potentially including prolonged disruption, major loss, serious legal or regulatory implications, or failure of a critical objective. |

These labels do not replace organization-specific criteria. Monetary amounts, downtime, records affected, service criticality, and other measurable thresholds should be established by the adopting organization rather than assumed to be universal.

### 6.3 Selecting the overall impact level

When multiple dimensions apply, use the **highest credible impact level** as the overall impact input. Do not average dimensions in a way that hides a severe credible consequence.

Document:
- The dimension that determines the selected level.
- The rationale and evidence supporting the consequence.
- Any materially different consequences in other dimensions.
- Significant assumptions or uncertainty.

“Highest credible” does not mean selecting an implausible worst case without support. The assessor must explain why the consequence is credible for the defined scenario.

## 7. The 5×5 Scoring Matrix

### 7.1 Formula

Calculate the base risk score as:

**Risk score = Likelihood × Impact**

Both inputs range from 1 to 5. The resulting score ranges from 1 to 25.

### 7.2 Matrix

Likelihood is displayed as rows and impact as columns.

| Likelihood ↓ / Impact → | 1 — Negligible | 2 — Minor | 3 — Moderate | 4 — Major | 5 — Severe |
|---|---:|---:|---:|---:|---:|
| 1 — Rare | 1 | 2 | 3 | 4 | 5 |
| 2 — Unlikely | 2 | 4 | 6 | 8 | 10 |
| 3 — Possible | 3 | 6 | 9 | 12 | 15 |
| 4 — Likely | 4 | 8 | 12 | 16 | 20 |
| 5 — Almost certain | 5 | 10 | 15 | 20 | 25 |

### 7.3 Interpretation and limitations

The product is a structured prioritization aid, not a precise measure of expected financial loss or a mathematically exact expression of risk. Different likelihood-impact combinations can produce the same score while representing different risk characteristics. Therefore, retain the individual input levels, their rationales, and the scenario description.

Do not compare scores across assessments without considering differences in scenario definitions, horizons, calibration, evidence quality, and organizational context.

## 8. Inherent Risk Calculation

Assess inherent risk before crediting existing controls.

1. Define the scenario and its consequences.
2. Select the inherent likelihood level for the stated horizon.
3. Select the inherent impact level using the impact criteria.
4. Calculate the inherent score by multiplying the two levels.
5. Apply the organization's approved rating mapping.
6. Record rationale, evidence, assumptions, and confidence.

The inherent assessment should describe the risk before existing controls are considered, not a hypothetical scenario detached from the organization's actual context. State assumptions needed to make that baseline meaningful.

## 9. Control Effectiveness Assessment

### 9.1 Required dimensions

Assess each relevant control in terms of:
- **Design:** Is the control designed to address the relevant cause, pathway, or consequence?
- **Implementation:** Is the control deployed, configured, and in scope for the assets or processes concerned?
- **Operating effectiveness:** Does available evidence show that the control operates as intended and reliably enough for the scenario?

Record the evidence reviewed, its date and scope, observed limitations, and any reliance on owner statements or unverified information.

### 9.2 Effect on likelihood and impact

Consider control effects only where there is a defensible causal connection to the scenario:
- A preventive control may reduce the likelihood of a scenario if its design, implementation, and operation support that conclusion.
- A detective or response control may reduce the duration or consequence of a scenario, and may affect impact where that effect is credible.
- A recovery control may reduce availability or operational consequences if recovery capability and dependencies are evidenced.
- A control that is absent, out of scope, misconfigured, untested, or ineffective must not receive unsupported risk-reduction credit.

A control's existence alone does not justify a lower score. Do not assign arbitrary percentage reductions or numerical effectiveness multipliers unless the organization has separately established and validated a defensible quantitative method. This model uses direct reassessment of the likelihood and impact levels.

## 10. Residual Risk Calculation

Residual risk is the risk remaining after relevant existing controls are evaluated.

1. Reassess the scenario's likelihood after considering the evidenced effects of relevant controls.
2. Reassess impact after considering controls that credibly affect consequences.
3. Record the rationale for any changed input. If an input remains unchanged, retain a concise explanation where needed.
4. Calculate the residual score as residual likelihood multiplied by residual impact.
5. Map the result to the organization's approved rating bands.
6. Record confidence, remaining uncertainty, and any override or escalation flag.

Do not mechanically subtract points from the inherent score or apply a fixed percentage reduction. A control may reduce likelihood, impact, both, or neither. The residual assessment must reflect the scenario and available evidence.

## 11. Illustrative Rating Bands

The following mapping is an **illustrative starting point only**. The adopting organization must approve or customize the bands before operational use.

| Score | Illustrative rating |
|---:|---|
| 1–4 | Low |
| 5–9 | Moderate |
| 10–16 | High |
| 17–25 | Critical |

Document the approved score ranges, labels, any special matrix-cell rules, and the authority that approved them. Apply the mapping consistently. If the organization changes the bands, retain the version and effective date used for each assessment so historical results remain interpretable.

These example ranges do not establish universal acceptance criteria. A rating is not, by itself, a decision that risk is acceptable or unacceptable.

## 12. Prioritization and Override Rules

### 12.1 Prioritization

Use the calculated score and approved rating as principal inputs, then consider other material factors, including:
- Credible severity of consequences.
- Exposure and scenario urgency.
- Criticality of affected assets, services, or business processes.
- Applicable legal, regulatory, contractual, or policy obligations.
- Dependencies, concentration, and potential cascading effects.
- Active exploitation, incident evidence, or material changes in the threat environment.
- Risk appetite, tolerance, and management direction.

Record the rationale where these factors change the order or urgency of action. Avoid implying that a higher numerical score is always more urgent than every lower-scored scenario.

### 12.2 Overrides and escalation flags

Where a severe credible impact, obligation, or other approved criterion warrants escalation despite the numerical result, the organization may use a documented rating override or a separate escalation flag.

Every override must retain:
- The original likelihood, impact, score, and rating.
- The adjusted rating or escalation flag.
- The reason for the exception and the criterion invoked.
- Supporting evidence and assumptions.
- The implications for treatment, reporting, and acceptance authority.
- The approver or authorized decision-maker.
- The review date or reassessment trigger.

An override must not overwrite or conceal the calculated score. An escalation flag may preserve the calculated rating while requiring additional review or action. The organization should define when each mechanism is appropriate and apply it consistently.

Neither a score nor an override can waive applicable law or non-waivable obligations.

## 13. Risk Appetite and Acceptance

### 13.1 Organization-defined appetite and tolerance

The adopting organization must document its risk appetite, tolerance, acceptance criteria, escalation thresholds, and decision authorities. These should reflect its objectives, obligations, operating context, and capacity to manage risk.

External standards can inform the process but do not supply universal numerical bands or acceptance thresholds for this model.

### 13.2 Residual-risk acceptance

Residual-risk acceptance requires an identified risk owner, a documented rationale, and approval within delegated authority. Where the risk exceeds that authority, escalate it to the designated higher authority or governance body.

The record should include:
- The scenario and residual rating.
- Reasons for accepting rather than further treating the risk.
- Remaining uncertainty and relevant evidence gaps.
- Applicable constraints or obligations.
- The accepting person or body and authority basis.
- Any conditions, compensating actions, review date, or reassessment trigger.

Silence, inaction, an overdue task, or an expired review date does not constitute acceptance. Acceptance cannot override applicable law or non-waivable obligations.

## 14. Treatment and Remediation Deadlines

The model supports four treatment options:
- **Mitigate:** introduce or improve controls to reduce likelihood or impact.
- **Avoid:** discontinue or change the activity that creates the risk.
- **Transfer/share:** allocate or share some consequences or responsibilities through an appropriate arrangement, recognizing that accountability and residual exposure may remain.
- **Accept:** formally retain the residual risk within the applicable authority and constraints.

The treatment choice must be recorded with its rationale, owner, planned actions, target dates, dependencies, and expected effect on residual risk.

Remediation deadlines are organization-defined and risk-based. Consider rating, exposure, obligations, business criticality, potential consequences, feasibility, and compensating measures. This document does not prescribe universal remediation windows.

Overdue treatment actions must be escalated according to documented governance rules. Where delay, changed exposure, an incident, or control degradation could materially change the risk, reassess the likelihood, impact, and residual score. Overdue status must never be interpreted as risk acceptance.

## 15. Uncertainty and Evidence Confidence

### 15.1 Separate confidence from the score

Record confidence separately from likelihood, impact, and score. Confidence concerns the sufficiency and reliability of the evidence and assumptions; it is not an extra multiplier in this model.

Describe relevant uncertainty, such as:
- Missing or stale evidence.
- Limited visibility or incomplete scope.
- Conflicting sources.
- Unverified control operation.
- Sparse or non-comparable incident data.
- Assumptions about threat capability, exposure, or consequences.

### 15.2 Conservative assumptions

Where uncertainty could conceal material risk, use a documented conservative assumption when justified. Explain why it is reasonable, which rating inputs it affects, and what evidence could resolve it. Do not automatically assign the maximum level simply because some uncertainty exists.

If evidence is too weak to support a reliable conclusion, identify the result as provisional, specify the limitation, and assign follow-up evidence collection or reassessment actions. A numerical result must not be represented as more certain than its basis supports.

## 16. Operational Scoring Worksheet

Use a risk register or equivalent record to retain, at minimum, the following fields. Organizations may add fields appropriate to their context.

| Category | Minimum fields |
|---|---|
| Identification | Risk ID, scenario, affected assets/processes, risk owner |
| Context | Assessment date, assessor, scope, assessment horizon |
| Inherent assessment | Inherent likelihood, impact, rationale, score, rating |
| Controls | Relevant controls, design and implementation status, operating evidence, effectiveness rationale |
| Residual assessment | Residual likelihood, impact, rationale, score, rating |
| Assurance | Evidence references, assumptions, confidence, limitations |
| Exceptions | Override or escalation flag, rationale, evidence, approver |
| Treatment | Treatment option, actions, responsible parties, deadlines |
| Governance | Acceptance decision, approving authority, escalation status |
| Lifecycle | Review date, reassessment triggers, change history, closure status |

### 16.1 Recordkeeping expectations

- Keep the scenario and scoring rationale understandable to a reviewer who was not the original assessor.
- Reference evidence using stable identifiers or repository references.
- Protect sensitive evidence and restrict access according to organizational requirements.
- Record material changes to scores, rating mappings, assumptions, controls, and acceptance decisions.
- Preserve enough history to explain why a risk rating changed.
- Apply evidence retention and integrity measures according to the organization's evidence-handling requirements and the sensitivity of the assessment.

## 17. Worked Examples

The following examples illustrate how to apply the model. They are hypothetical and are not universal thresholds or conclusions about any particular organization. The example rating bands are those in Section 11 solely for demonstration.

### 17.1 Example A — Inherent versus residual risk

**Scenario:** An internet-facing business application has a credible scenario involving unauthorized access through a software weakness, potentially exposing sensitive business information.

**Inherent assessment**
- Likelihood: 4 — Likely.
- Impact: 4 — Major, based on the scenario's credible consequences.
- Inherent score: \(4 \times 4 = 16\).
- Illustrative rating: High.

**Control review:** The organization verifies that a relevant preventive control is deployed and reviews evidence that it operates. The evidence supports a reduction in likelihood, but does not support a lower impact level if the scenario succeeds.

**Residual assessment**
- Likelihood: 2 — Unlikely, based on the documented control evidence and scenario conditions.
- Impact: 4 — Major, unchanged.
- Residual score: \(2 \times 4 = 8\).
- Illustrative rating: Moderate.

**Interpretation:** The lower residual score is justified by a reassessment of likelihood, not an arbitrary deduction. The organization must record the control evidence, assumptions, remaining exposure, and whether the residual risk is acceptable under its approved criteria.

### 17.2 Example B — Severe-impact override

**Scenario:** A disruption affecting a critical service has a low assessed likelihood but could credibly produce severe consequences.

- Likelihood: 2 — Unlikely.
- Impact: 5 — Severe.
- Calculated score: \(2 \times 5 = 10\).
- Illustrative rating: High.

Suppose the organization's approved governance criteria require elevated review for this class of critical-service consequence. The risk record retains the score of 10 and the calculated High rating, while adding the required escalation flag or approved override.

**Interpretation:** The escalation does not alter the multiplication. It records a governance requirement arising from credible impact and organizational criteria. The record must identify the criterion, evidence, approver, treatment implications, and review arrangements.

### 17.3 Example C — Uncertain evidence

**Scenario:** A system's exposure is incompletely documented, and available evidence is insufficient to confirm whether a relevant protective control operates reliably.

The assessor provisionally assigns:
- Likelihood: 3 — Possible, using a documented conservative assumption.
- Impact: 4 — Major.
- Provisional score: \(3 \times 4 = 12\).
- Illustrative rating: High.
- Confidence: Low, recorded separately.

**Follow-up:** The risk owner assigns an action to verify exposure and control operation by an organization-defined date. The record explains why the likelihood assumption was selected and what evidence would support a revised assessment.

**Interpretation:** Low confidence does not produce an automatic numeric multiplier. It limits the strength of the conclusion and may justify a conservative provisional score, additional evidence collection, escalation, or reassessment.

### 17.4 Example D — Overdue treatment action

**Scenario:** A High-rated residual risk has an approved mitigation action, but the action passes its due date.

The risk record must show the overdue status, accountable owner, reason for delay if known, current compensating measures, and escalation according to the organization's governance rules.

The assessor determines whether the delay or changed exposure affects likelihood, impact, or control effectiveness. If material, the scenario is reassessed and a new residual score is calculated. If there is no evidence of a changed input, the existing score may remain while the overdue action and escalation are documented.

**Interpretation:** The missed deadline does not mean the risk has been accepted. Escalation and reassessment are separate requirements; reassessment is particularly important when the delay changes the actual risk.

## 18. Calibration and Quality Assurance

Before operational use, the organization should conduct a documented calibration exercise with representative stakeholders, including risk owners and relevant technical, business, security, compliance, and governance personnel as appropriate.

The calibration process should:

1. Approve definitions for each likelihood and impact level.
2. Establish any quantitative anchors using relevant organizational data where available.
3. Approve the score-to-rating mapping and any matrix-cell exceptions.
4. Define risk appetite, tolerance, escalation criteria, acceptance authority, and deadline-setting rules.
5. Score representative scenarios and compare assessor results.
6. Resolve or document material differences in interpretation.
7. Define how uncertainty, overrides, and low-confidence assessments are handled.
8. Record approval, version, effective date, and review arrangements.

Quality review should check that the scenario is defined, the horizon is stated, impact dimensions are considered, controls receive only evidence-supported credit, arithmetic is correct, rating bands are current, overrides are traceable, and governance decisions are properly authorized.

Review independence should be proportionate to risk, complexity, and uncertainty. Where independent review is unavailable, document the limitation and any compensating review.

## 19. Monitoring and Reassessment

Set a periodic review frequency based on the organization's context and the risk's materiality. Reassess when a material event or change may affect the scenario or the basis of the score.

Triggers include, but are not limited to:
- Changes in threats, vulnerabilities, exposure, or active exploitation.
- Changes to assets, applications, business processes, dependencies, or criticality.
- Changes to control design, implementation, configuration, or operating effectiveness.
- Incidents, near misses, or material new threat intelligence.
- Changes in legal, regulatory, contractual, or policy obligations.
- Changes in business objectives, operating context, risk appetite, or risk tolerance.
- Material delays in treatment or failure of planned controls.

When reassessing, retain the prior score and rationale, explain the changed inputs, and record the new decision and approval where required. Do not silently replace historical assessments.

## 20. Limitations and Customization

This model has important limitations:
- Multiplying ordinal scales does not produce a precise probability or expected-loss value.
- Equal products can represent materially different combinations of likelihood and impact.
- Likelihood estimates may be limited by sparse, biased, or non-comparable data.
- Impact judgments depend on scenario context, business objectives, dependencies, and applicable obligations.
- Control effectiveness conclusions depend on evidence quality, scope, and timing.
- A rating band cannot replace professional judgment, legal review, or authorized governance.
- Scores should not be compared across organizations or differently calibrated assessments without appropriate context.
- The model does not itself demonstrate compliance with an external standard or regulation.

The adopting organization must document its approved scales, rating bands, appetite and tolerance, escalation rules, delegated authorities, deadlines, and review arrangements. Any changes to the model should be version-controlled and applied consistently.

## 21. Related Documents and References

### 21.1 Related project documents

Use this model alongside the project's supporting methodology and evidence guidance:
- `assessment-lifecycle.md` — assessment phases, stage gates, responsibilities, and closure.
- `risk-assessment-methodology.md` — end-to-end risk assessment method and risk-register requirements.
- `evidence-handling.md` — evidence provenance, integrity, protection, and handling practices, when available.

Related-document links should be checked against the repository structure when those documents are added or renamed.

### 21.2 Reference frameworks and standards

The following publications and frameworks may inform organizational calibration and implementation. Verify current editions, amendments, and applicability before relying on them:

- **NIST Cybersecurity Framework (CSF) 2.0** — cybersecurity risk outcomes and governance context.
- **NIST SP 800-30 Rev. 1** — guidance for conducting risk assessments.
- **NIST SP 800-37 Rev. 2** — risk management framework and authorization context.
- **NIST SP 800-53 Rev. 5**, including applicable updates — security and privacy control catalog.
- **NIST SP 800-115** — technical information-security testing and assessment guidance.
- **NIST SP 800-61 Rev. 3** — incident response recommendations integrated with cybersecurity risk management.
- **ISO/IEC 27001, ISO/IEC 27002, and ISO/IEC 27005** — information-security management, controls, and information-security risk management.
- **CIS Critical Security Controls v8.1** — prioritized safeguards.
- **OWASP Application Security Verification Standard (ASVS)** and **OWASP Web Security Testing Guide (WSTG)** — application security verification and testing.

These sources inform different aspects of cybersecurity risk management and assessment. They do not prescribe the illustrative score bands in this document as universal thresholds. This document does not claim certification, compliance, or equivalence to any referenced standard.

## 22. Document Control

| Field | Value |
|---|---|
| Document title | Risk Scoring Model |
| File | `docs/methodology/risk-scoring-model.md` |
| Version | 1.0 |
| Status | Template for organizational review and approval |
| Document owner | To be assigned by the adopting organization |
| Approval authority | To be defined by the adopting organization |
| Effective date | To be set on approval |
| Review cycle | To be defined by the adopting organization |
| Change history | Record revisions, rationale, approver, and effective date |

**Implementation condition:** Before this model is used to make operational risk decisions, the adopting organization must approve and document the likelihood and impact criteria, score-to-rating mapping, appetite and tolerance, override and escalation criteria, delegated authorities, and remediation deadline rules.
