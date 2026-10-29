# Cybersecurity Risk Register Template

> **Document type:** Reusable assessment template  
> **Suggested repository path:** `templates/risk-register-template.md`  
> **Status:** Template — tailor and approve for organizational use before operational adoption  
> **Version:** 1.0  
> **Owner:** `[Organization / function]`  
> **Last reviewed:** `[YYYY-MM-DD]`

## 1. Purpose and instructions

Use this template to record, assess, treat, monitor, and close information-security and cybersecurity risks. It supports both portfolio-level tracking and detailed, scenario-based risk records.

### How to use this template

1. Copy this file into the assessment workspace or the organization's approved risk-management system.
2. Assign each risk a stable, unique identifier (for example, `RISK-001`). Do not reuse identifiers for unrelated risks.
3. Maintain one authoritative record for each distinct risk scenario. Link related findings, assets, controls, evidence, treatment actions, and assessment records by identifier.
4. Complete the summary register and the detailed record together. The summary table is for portfolio visibility; the detailed record is the authoritative explanation of the scenario and its decisions.
5. Replace bracketed placeholders with assessment-specific information. Mark fields `Not applicable` with a rationale where the field is relevant to governance or traceability.
6. Use the associated methodology and scoring model consistently. Record assumptions, uncertainty, evidence gaps, and justified overrides rather than hiding them.
7. Do not place credentials, secrets, unnecessary personal information, or sensitive raw evidence in this Markdown file. Use approved repositories and reference evidence by ID.
8. Tailor status values, approval roles, review cadence, retention, and deadlines to approved organizational policy and applicable obligations.

### Related framework documents

- [Assessment lifecycle](../docs/methodology/assessment-lifecycle.md)
- [Risk assessment methodology](../docs/methodology/risk-assessment-methodology.md)
- [Risk scoring model](../docs/methodology/risk-scoring-model.md)
- [Evidence handling](../docs/methodology/evidence-handling.md)

This template is a practical record-keeping aid, not proof of compliance or certification. Referencing a standard or framework does not by itself establish conformity.

---

## 2. Risk register summary

Use one row per risk. Keep the summary concise and maintain detailed rationale, evidence, actions, and approvals in the detailed record.

| Risk ID | Risk title | Category | Risk owner | Inherent rating | Current rating | Target residual rating | Treatment strategy | Status | Next action / due date | Next review | Escalation / acceptance |
|---|---|---|---|---|---|---|---|---|---|---|---|
| `RISK-001` | `[Short scenario title]` | `[Category]` | `[Role / name]` | `[Score / band]` | `[Score / band]` | `[Forecast score / band]` | `[Avoid / Mitigate / Transfer-share / Accept]` | `[Status]` | `[Action and YYYY-MM-DD]` | `[YYYY-MM-DD]` | `[Not required / Pending / Approved / Escalated]` |
| `RISK-002` | `[Short scenario title]` | `[Category]` | `[Role / name]` | `[Score / band]` | `[Score / band]` | `[Forecast score / band]` | `[Strategy]` | `[Status]` | `[Action and YYYY-MM-DD]` | `[YYYY-MM-DD]` | `[State]` |

### Summary table conventions

- **Inherent risk:** estimate before crediting existing controls.
- **Current risk:** estimate after considering existing controls and evidence of their design, implementation, and operating effectiveness.
- **Target residual risk:** forecast of risk after planned treatment has been implemented and its effectiveness verified. It is not a claim about the current state.
- **Treatment strategy:** select the primary strategy, while documenting combined or supporting approaches in the detailed record.
- **Next action / due date:** identify the next material action, not necessarily the final closure date.
- **Escalation / acceptance:** state whether a decision is pending, formally approved, or escalated.

---

## 3. Detailed risk record

Copy this section for each risk and replace all bracketed placeholders. Keep a change history when a material rating, decision, owner, or treatment plan changes.

### 3.1 Identification and governance

| Field | Record |
|---|---|
| Risk ID | `[RISK-###]` |
| Risk title | `[Concise title]` |
| Record version | `[Version]` |
| Record status | `[Status from Section 7]` |
| Date identified | `[YYYY-MM-DD]` |
| Last updated | `[YYYY-MM-DD]` |
| Assessor / assessment team | `[Role / team]` |
| Assessment ID | `[Assessment identifier]` |
| Business unit / service owner | `[Unit / role]` |
| Risk owner | `[Role / person accountable for the risk]` |
| Control owner(s) | `[Roles / teams responsible for relevant controls]` |
| Treatment owner(s) | `[Roles / teams responsible for actions]` |
| Reviewer / approver | `[Role / person, as applicable]` |
| Related findings | `[Finding IDs or None]` |
| Related control IDs | `[Control IDs or None]` |
| Related risk IDs | `[Risk IDs or None]` |
| Risk category | `[Technical / operational / people / third-party / compliance / other defined category]` |
| Business objective / process | `[Objective, process, or service affected]` |

### 3.2 Scope, assets, and context

- **Assessment boundary:** `[Systems, services, sites, networks, processes, or organizational boundary]`
- **Affected assets and information:** `[Asset IDs, data types, information owners, and critical services]`
- **Affected stakeholders:** `[Internal and external stakeholders, where relevant]`
- **Third parties / dependencies:** `[Providers, upstream services, supply-chain dependencies, or None]`
- **Relevant network zone / environment:** `[Production / test / standalone / cloud / other, as applicable]`
- **Authorization and scope reference:** `[Approved scope / authorization record ID]`
- **Assumptions:** `[Assumptions that materially affect the analysis]`
- **Exclusions and limitations:** `[Exclusions, access limitations, sampling limits, or None]`
- **Relevant legal, contractual, regulatory, or policy obligations:** `[Applicable references or To be determined]`

### 3.3 Risk scenario

**Risk statement — cause, event, consequence**

> Because `[cause, threat condition, vulnerability, or control weakness]`, `[risk event]` may occur, resulting in `[credible consequences to the organization, its services, information, or stakeholders]`.

- **Threat source / initiating condition:** `[Describe where relevant; do not force a threat-actor attribution if unsupported]`
- **Vulnerability / weakness / control gap:** `[Describe the condition and reference supporting finding IDs]`
- **Plausible event path:** `[Explain how the event could occur]`
- **Potential consequences:** `[Describe direct and cascading effects]`
- **Existing safeguards / dependencies:** `[Controls or external conditions that affect the scenario]`
- **Risk horizon:** `[Defined period used to assess likelihood, e.g., one year, consistent with the approved model]`
- **Scenario rationale:** `[Why this is a distinct and material risk rather than only a generic finding]`

### 3.4 Impact analysis

Document credible consequences and the basis for the overall impact rating. Consider applicable dimensions; do not assume every dimension is material to every scenario.

| Impact dimension | Potential consequence | Severity rationale / evidence reference |
|---|---|---|
| Confidentiality | `[Unauthorized disclosure / exposure / None with rationale]` | `[Rationale / evidence IDs]` |
| Integrity | `[Unauthorized modification / corruption / None with rationale]` | `[Rationale / evidence IDs]` |
| Availability | `[Outage / service degradation / None with rationale]` | `[Rationale / evidence IDs]` |
| Operational continuity | `[Process disruption / recovery burden]` | `[Rationale / evidence IDs]` |
| Financial | `[Loss, response cost, recovery cost, or other exposure]` | `[Rationale / evidence IDs]` |
| Legal / regulatory / contractual | `[Potential obligation or consequence]` | `[Rationale / evidence IDs]` |
| Reputation / stakeholder trust | `[Credible consequence]` | `[Rationale / evidence IDs]` |
| Other organization-defined dimension | `[Dimension or Not applicable]` | `[Rationale / evidence IDs]` |

**Overall impact rating:** `[1–5 and label]`  
**Basis for selecting overall impact:** `[Apply the approved scoring model, including its rule for selecting the highest credible impact where applicable. Explain any departure.]`

### 3.5 Likelihood assessment

- **Likelihood rating:** `[1–5 and label from the approved scoring model]`
- **Rationale:** `[Threat capability / intent where relevant, exposure, exploitability, frequency, existing controls, historical information, and scenario-specific conditions]`
- **Assessment horizon:** `[Period]`
- **Evidence and sources:** `[Evidence IDs, incident references, test results, threat information, or other sources]`
- **Key assumptions and uncertainty:** `[State material unknowns and how they affect the rating]`
- **Confidence:** `[High / Medium / Low or organization-defined scale, separate from the risk rating]`

Do not treat absence of evidence as evidence that a threat or weakness is absent. Where evidence is incomplete, record the limitation and assess its effect on the conclusion.

### 3.6 Inherent, current, and target residual risk

Use the approved `risk-scoring-model.md`. Do not silently alter scales or thresholds within an individual record.

| Risk state | Likelihood (1–5) | Impact (1–5) | Score | Rating band | Rationale / confidence |
|---|---:|---:|---:|---|---|
| Inherent | `[ ]` | `[ ]` | `[L × I]` | `[Band]` | `[Before crediting existing controls]` |
| Current | `[ ]` | `[ ]` | `[L × I]` | `[Band]` | `[After considering existing controls and evidence]` |
| Target residual (forecast) | `[ ]` | `[ ]` | `[L × I]` | `[Band]` | `[Expected after planned treatment; assumptions stated]` |

- **Risk scoring model version / reference:** `[Document version or approved model ID]`
- **Risk appetite / tolerance statement:** `[Applicable approved criterion or Not defined]`
- **Within appetite / tolerance?:** `[Yes / No / Uncertain / Not defined]`
- **Rating override or exception:** `[None, or explain rationale, approver, and date]`
- **Overall assessment confidence:** `[Organization-defined scale and rationale]`

**Illustrative rating bands only:** The associated scoring model describes Low (1–4), Moderate (5–9), High (10–16), and Critical (17–25) as illustrative bands. The organization must formally approve its bands, appetite/tolerance, and acceptance criteria before operational use. Do not use these bands as universal requirements.

### 3.7 Existing controls and effectiveness

Record controls that materially affect the scenario. Reference the evidence register rather than duplicating sensitive evidence.

| Control ID | Control description / objective | Design adequacy | Implementation status | Operating effectiveness evidence and date | Limitation / deficiency | Effect on likelihood or impact |
|---|---|---|---|---|---|---|
| `[CTRL-###]` | `[Description]` | `[Adequate / Partial / Inadequate / Unknown]` | `[Implemented / Partial / Not implemented / Unknown]` | `[Evidence IDs and date]` | `[Gap or limitation]` | `[Explain rating effect]` |
| `[CTRL-###]` | `[Description]` | `[Rating]` | `[Status]` | `[Evidence IDs and date]` | `[Gap or limitation]` | `[Effect]` |

**Control-effectiveness conclusion:** `[Explain what evidence supports crediting these controls and what uncertainty remains.]`

### 3.8 Evidence references

| Evidence ID | Description | Source / collector | Collection date | Integrity / validation reference | Supports which claim or rating? | Limitation / sensitivity |
|---|---|---|---|---|---|---|
| `[EVD-###]` | `[Description; avoid secrets or unnecessary sensitive data]` | `[Source / role]` | `[YYYY-MM-DD]` | `[Hash, validation, custody record, or N/A with rationale]` | `[Scenario / control / likelihood / impact / treatment]` | `[Limitation and handling requirements]` |

- **Evidence register location:** `[Approved repository / system reference]`
- **Evidence gaps:** `[Gap ID(s), or None]`
- **Effect of evidence gaps on conclusions:** `[Explain impact on ratings, confidence, and decisions]`
- **Additional collection / validation required:** `[Action, owner, and target date, or None]`

Follow `evidence-handling.md` for authorization, collection, integrity verification, sensitive-data handling, chain of custody where warranted, retention, and disposal. Do not embed raw credentials, secrets, or sensitive evidence in this record.

### 3.9 Treatment decision

Select the primary strategy and explain the decision.

- [ ] **Avoid** — discontinue or change the activity that creates the risk.
- [ ] **Mitigate** — implement or improve controls to reduce risk.
- [ ] **Transfer/share** — allocate or share defined aspects of exposure through suitable arrangements.
- [ ] **Accept** — formally retain the risk within delegated authority.

**Selected strategy:** `[Strategy]`  
**Decision rationale:** `[Expected risk reduction, feasibility, dependencies, cost/resource considerations, and reasons alternatives were not selected]`  
**Expected effect:** `[Likelihood / impact / both / other, with rationale]`  
**Treatment decision owner:** `[Role / person]`  
**Decision date:** `[YYYY-MM-DD]`  
**Approval status:** `[Pending / Approved / Rejected / Escalated]`  
**Related decision / exception reference:** `[ID or None]`

Transfer or sharing does not necessarily eliminate the organization's exposure, accountability, or residual risk. Document retained obligations and dependencies.

### 3.10 Treatment action plan

Create one row per action. Use unique action IDs and keep action status current.

| Action ID | Action / deliverable | Expected risk effect | Owner | Priority | Dependencies / resources | Target date | Status | Completion evidence | Verification result |
|---|---|---|---|---|---|---|---|---|---|
| `[ACT-###]` | `[Specific, verifiable action]` | `[Likelihood / impact / both]` | `[Role / person]` | `[Organization-defined]` | `[Dependencies]` | `[YYYY-MM-DD]` | `[Status]` | `[Evidence ID]` | `[Pending / Effective / Partially effective / Ineffective]` |
| `[ACT-###]` | `[Specific, verifiable action]` | `[Effect]` | `[Role / person]` | `[Priority]` | `[Dependencies]` | `[YYYY-MM-DD]` | `[Status]` | `[Evidence ID]` | `[Result]` |

- **Milestones and dependencies:** `[Describe sequencing or cross-team requirements]`
- **Deadline basis:** `[Policy, contract, regulation, risk decision, or approved plan]`
- **Overdue action escalation:** `[Escalation path and accountable role]`
- **Residual actions after implementation:** `[Outstanding work, compensating controls, or None]`

Set deadlines based on organizational policy, applicable obligations, risk significance, and authorized decisions. This template does not establish universal remediation deadlines.

### 3.11 Acceptance, escalation, and exception record

Complete this section whenever acceptance, an exception, or escalation is relevant.

| Field | Record |
|---|---|
| Risk owner recommendation | `[Accept / Treat / Escalate / Other]` |
| Decision / approval authority | `[Role and delegated authority reference]` |
| Decision | `[Approved / Rejected / Pending / Escalated / N/A with rationale]` |
| Decision rationale | `[Why the decision is appropriate and within authority]` |
| Approval date | `[YYYY-MM-DD or Pending]` |
| Validity / review condition | `[Date or trigger, if applicable]` |
| Conditions / compensating controls | `[Conditions and owners, or None]` |
| Appetite / tolerance comparison | `[Criterion and conclusion, or Not defined]` |
| Exception ID and scope | `[ID, scope, rationale, and limitations, or None]` |
| Escalation destination / date | `[Role or committee and date, or None]` |
| Next decision / review date | `[YYYY-MM-DD]` |

Acceptance must be affirmative and documented by an authorized decision-maker. Silence, missed deadlines, incomplete treatment, or an unapproved exception does not constitute acceptance. Escalate risks that exceed the risk owner's delegated authority.

### 3.12 Monitoring and reassessment

- **Monitoring approach / indicators:** `[Metrics, events, control checks, incidents, or other signals]`
- **Risk indicators and thresholds:** `[Organization-defined indicators / thresholds, or Not defined]`
- **Scheduled review date / cadence:** `[Date / approved cadence]`
- **Reassessment triggers:** `[Material asset, threat, vulnerability, control, business, incident, audit, or regulatory change]`
- **Latest reassessment date:** `[YYYY-MM-DD]`
- **Updated likelihood / impact / current score:** `[Values and rationale]`
- **Changes since last assessment:** `[Summary and evidence references]`
- **New evidence / findings:** `[IDs or None]`
- **Decision after reassessment:** `[Continue treatment / revise plan / accept subject to approval / escalate / close / reopen]`
- **Next review date:** `[YYYY-MM-DD]`

Reassess when material conditions change, not only when the scheduled review date arrives.

### 3.13 Closure and verification

Complete only when closure is justified under the organization's approved criteria.

- **Closure rationale:** `[Why the risk record can be closed; do not equate completed actions with eliminated risk]`
- **Treatment actions verified:** `[Action IDs and evidence IDs]`
- **Control effectiveness verified by:** `[Role / reviewer and date]`
- **Post-treatment risk rating:** `[Likelihood, impact, score, band, confidence]`
- **Residual risk decision:** `[Accepted / within approved tolerance / further treatment / escalated]`
- **Required approvals completed:** `[Yes / No, with references]`
- **Outstanding obligations / monitoring:** `[Items and owner, or None]`
- **Closure authority and date:** `[Role and YYYY-MM-DD]`
- **Reopening conditions:** `[Triggers that require reassessment]`

If the risk remains material or requires ongoing monitoring, keep it in the appropriate active state rather than marking it closed solely because a treatment action is complete.

### 3.14 Review and change history

| Date | Version | Change / reassessment summary | Rating or decision impact | Prepared by | Reviewed / approved by |
|---|---|---|---|---|---|
| `[YYYY-MM-DD]` | `[1.0]` | `[Initial record]` | `[Initial assessment]` | `[Role]` | `[Role / Pending]` |
| `[YYYY-MM-DD]` | `[ ]` | `[Change]` | `[Impact]` | `[Role]` | `[Role]` |

---

## 4. Illustrative completed risk record

> **Illustrative example only.** The scenario, organization, system, evidence, ratings, dates, and action identifiers below are fictional. The scores demonstrate how to document a decision; they do not prescribe ratings for real environments.

### 4.1 Scenario and context

| Field | Illustrative value |
|---|---|
| Risk ID | `RISK-EX-001` |
| Risk title | Excessive administrative access to a business-critical server |
| Category | Technical / access control |
| Affected asset | `SRV-EX-01` — fictional business-critical application server |
| Risk owner | Application service owner |
| Control owner | Infrastructure security lead |
| Assessor | Cybersecurity assessment team |
| Status | In treatment |
| Risk horizon | One year, subject to the organization's approved model |
| Related finding | `FIND-EX-014` |
| Evidence references | `EVD-EX-021`, `EVD-EX-022` |

**Risk statement:** Because administrative access to a business-critical server is not sufficiently restricted and periodically reviewed, an unauthorized or compromised privileged account may be used to access or alter the server, resulting in service disruption, unauthorized access to business information, and recovery costs.

**Assumptions and limitations:** The example assumes the assessment was authorized, access records were available, and the evidence references are fictional entries in an approved evidence register. No actual production system was assessed.

### 4.2 Illustrative impact and likelihood

| Dimension | Example consequence | Basis |
|---|---|---|
| Confidentiality | Unauthorized access to business information | Privileged access could expose data available to the server account |
| Integrity | Unauthorized configuration or data modification | Privileged permissions could enable material changes |
| Availability | Application interruption | Misuse or compromise could affect service operation |
| Operational / financial | Investigation, recovery, and service-restoration effort | Depends on incident scope and recovery requirements |
| Legal / regulatory / reputation | Potential downstream consequences | Applicability requires organization-specific review |

**Inherent likelihood:** `4/5` — illustrative rationale: the hypothetical administrative access weakness creates a credible pathway, and no existing control credit is taken for the inherent assessment.

**Inherent impact:** `4/5` — illustrative rationale: compromise could materially affect a business-critical service and information.

**Inherent score:** `4 × 4 = 16`, which maps to **High** under the example bands.

### 4.3 Existing controls and current risk

| Control ID | Existing control | Example evidence | Assessment |
|---|---|---|---|
| `CTRL-EX-01` | Centralized authentication | `EVD-EX-021` | Implemented in the fictional scenario; does not by itself demonstrate least privilege |
| `CTRL-EX-02` | Administrative activity logging | `EVD-EX-022` | Provides investigative visibility; does not prevent all unauthorized privileged actions |

**Current likelihood:** `3/5` — illustrative rationale: existing authentication and logging provide some risk reduction, but privileged access restrictions remain inadequate.

**Current impact:** `4/5` — illustrative rationale: the potential consequence remains material even after accounting for the existing controls.

**Current score:** `3 × 4 = 12`, which maps to **High** under the example bands.

**Confidence:** Medium — the hypothetical evidence supports the control descriptions, but does not establish that privileged access is appropriately restricted or that monitoring is fully effective.

### 4.4 Treatment decision and actions

**Selected strategy:** Mitigate.

**Decision rationale:** Introduce least-privilege access, strengthen privileged authentication, and establish periodic access review. Validate the changes with evidence before reducing the recorded current risk rating.

| Action ID | Action | Owner | Illustrative target | Verification evidence |
|---|---|---|---|---|
| `ACT-EX-01` | Remove unnecessary privileged memberships and document approved administrator roles | Infrastructure security lead | `YYYY-MM-DD` | Updated access listing and approved access matrix |
| `ACT-EX-02` | Enforce the approved privileged-authentication requirements | Identity and access management owner | `YYYY-MM-DD` | Configuration export and test results |
| `ACT-EX-03` | Establish a documented periodic privileged-access review | Application service owner | `YYYY-MM-DD` | Signed review record and remediation tickets |

The dates are intentionally placeholders. Actual deadlines must be set according to organizational policy, obligations, risk significance, and approval authority.

### 4.5 Target residual risk forecast

| Risk state | Likelihood | Impact | Score | Example band |
|---|---:|---:|---:|---|
| Inherent | 4 | 4 | 16 | High |
| Current | 3 | 4 | 12 | High |
| Target residual — forecast | 2 | 4 | 8 | Moderate |

The forecast assumes the treatment actions are completed and evidence demonstrates that the controls operate as intended. Until verification is complete, the current rating remains the authoritative assessment of present risk. Impact remains at `4` because the potential consequence of a successful compromise may remain significant even after likelihood is reduced.

### 4.6 Illustrative decision and closure conditions

- **Risk owner recommendation:** Continue mitigation.
- **Acceptance:** Not recorded in this example; formal acceptance would require a documented decision by an authorized approver.
- **Closure conditions:** Treatment actions verified, control effectiveness reviewed, post-treatment risk reassessed, residual-risk decision recorded, and required approvals completed.
- **Reopening triggers:** Privileged access expands materially, controls fail, a relevant incident occurs, or evidence shows that the risk rating is no longer valid.

---

## 5. Risk review and maintenance checklist

Use this checklist during quality review or reassessment.

- [ ] The risk has a unique ID and a clear, scenario-based title.
- [ ] The cause, event, and consequence are documented.
- [ ] Scope, affected assets, stakeholders, and material dependencies are identified.
- [ ] Inherent, current, and target residual risk are clearly distinguished.
- [ ] Likelihood, impact, time horizon, and rating rationale follow the approved scoring model.
- [ ] Confidence and material uncertainty are recorded separately from the score.
- [ ] Existing control effectiveness is supported by evidence, not assumed.
- [ ] Evidence IDs are traceable to the evidence register and relevant claims.
- [ ] Evidence gaps and their effects on the conclusion are documented.
- [ ] The treatment decision is recorded and appropriate to delegated authority.
- [ ] Each material treatment action has an owner, due date, status, and verification method.
- [ ] Acceptance, escalation, and exceptions are documented where applicable.
- [ ] The target residual rating is treated as a forecast until verified.
- [ ] Review dates and event-triggered reassessment conditions are defined.
- [ ] Closure is supported by verification and an authorized decision.
- [ ] Sensitive evidence and secrets are stored only in approved locations.
- [ ] Applicable retention, legal hold, and disposal requirements are followed.
- [ ] Material changes are recorded in the review history.

---

## 6. Practical configuration guidance

Before operational use, the organization should define and approve:

1. The scoring model version, rating bands, risk appetite/tolerance, and acceptance criteria.
2. Roles and delegated authorities for ownership, treatment decisions, acceptance, escalation, review, and closure.
3. Required fields, allowed status values, review cadence, and reassessment triggers.
4. Treatment deadlines and overdue-action escalation based on policy and applicable obligations.
5. Approved locations for the register and evidence, access controls, retention, and disposal.
6. Quality-review requirements and any independence requirements for higher-significance risks.

Do not add universal thresholds or deadlines merely to make the template appear complete. Document organization-specific decisions and exceptions.

## 7. Suggested status vocabulary

| Status | Meaning |
|---|---|
| Identified | Risk recorded; assessment not yet complete |
| Under assessment | Scenario, evidence, and rating are being evaluated |
| Awaiting decision | Treatment or acceptance decision is pending |
| Treatment planned | Actions agreed; work has not materially started |
| In treatment | One or more treatment actions are in progress |
| Monitoring | Risk is monitored under an approved decision or control plan |
| Accepted | Risk formally accepted by an authorized decision-maker, subject to any conditions |
| Closed | Closure criteria satisfied and documented |
| Reopened | A previously closed risk requires renewed assessment |

Organizations may tailor these values while preserving unambiguous status definitions, transition accountability, and an auditable decision history.

---

## 8. References and document control

### Related internal documents

- [Assessment lifecycle](../docs/methodology/assessment-lifecycle.md)
- [Risk assessment methodology](../docs/methodology/risk-assessment-methodology.md)
- [Risk scoring model](../docs/methodology/risk-scoring-model.md)
- [Evidence handling](../docs/methodology/evidence-handling.md)
- [Standards and frameworks register](../references/standards-and-frameworks.md)

### External framework alignment

This template is designed to support a scenario-based, evidence-informed risk process consistent with concepts commonly addressed by NIST risk-management publications, NIST Cybersecurity Framework, and ISO/IEC information-security risk-management standards. Consult the repository's standards register and verify current editions and applicable organizational obligations before use.

References to standards are contextual guidance only. This template does not independently establish compliance, certification, or legal sufficiency.

### Document control

| Field | Value |
|---|---|
| Document | Cybersecurity Risk Register Template |
| Version | 1.0 |
| Owner | `[Organization / function]` |
| Approval authority | `[Role / committee]` |
| Approval date | `[YYYY-MM-DD]` |
| Review date | `[YYYY-MM-DD]` |
| Classification | `[Organization-defined]` |
| Change history | `[Record approved changes]` |
