# Risk Assessment Methodology

**Document type:** Operational methodology  
**Status:** Initial release  
**Applies to:** Information-security risk assessments across technology, business processes, people, governance, physical environments, third parties, and compliance  
**Primary reference:** NIST SP 800-30  
**Supporting references:** ISO/IEC 27005 and NIST Cybersecurity Framework concepts, where applicable  
**Related documents:** [Assessment Lifecycle](assessment-lifecycle.md), [Risk Scoring Model](risk-scoring-model.md), [Evidence Handling](evidence-handling.md), and [Standards and Frameworks](../../references/standards-and-frameworks.md)

> This document is a reusable, organization-neutral methodology. Organizations should adapt it to their governance, risk appetite, legal and contractual obligations, operating environment, and approved internal policies. It does not, by itself, establish compliance with any law, regulation, or external standard.

## 1. Purpose and Objectives

This methodology defines a repeatable, evidence-informed process for identifying, analyzing, evaluating, treating, and monitoring information-security risks. It is intended to support consistent decisions, traceable risk records, proportionate assurance, and practical remediation planning.

The methodology aims to:

- identify credible risk scenarios affecting information, systems, services, people, processes, third parties, and organizational objectives;
- analyze inherent risk and residual risk consistently;
- consider the design, implementation, and operating effectiveness of existing controls;
- prioritize risks using documented criteria, business context, and applicable obligations;
- assign treatment actions and risk ownership;
- support explicit, authorized residual-risk acceptance;
- document evidence, assumptions, uncertainty, and limitations; and
- support periodic and event-triggered reassessment.

## 2. Scope and Applicability

The methodology may be applied to enterprise, government, and smaller organizational environments. It covers information-security risks associated with, but not limited to:

| Risk domain | Illustrative coverage |
|---|---|
| Governance | Accountability, oversight, risk management, decision-making, and assurance |
| People | Human error, insider threats, awareness, competence, and misuse of access |
| Processes | Operational procedures, change management, continuity, and process dependencies |
| Technology | Endpoints, servers, networks, applications, data, cloud services, and infrastructure |
| Physical and environmental | Unauthorized physical access, equipment damage, and environmental disruption |
| Third-party | Suppliers, service providers, outsourced operations, and external dependencies |
| Compliance | Legal, regulatory, contractual, and internal-policy exposure |

These domains are classification aids rather than mutually exclusive categories. A single scenario may span multiple domains.

The assessment scope, exclusions, criteria, time horizon, and authorization must be established before assessment activity begins. This methodology does not authorize testing or access to any system by itself.

## 3. Principles and Terminology

Assessors should apply the following principles:

- **Contextual:** Evaluate risk in relation to organizational objectives, affected stakeholders, and operating conditions.
- **Scenario-centric:** Analyze plausible events and their consequences rather than treating a vulnerability or asset as a complete risk by itself.
- **Evidence-informed:** Support material judgments with relevant evidence and clearly identify assumptions.
- **Proportionate:** Scale assessment depth and assurance to risk, complexity, uncertainty, sensitivity, and organizational requirements.
- **Traceable:** Preserve a clear link between scenarios, evidence, ratings, treatment decisions, owners, and review outcomes.
- **Explicit about uncertainty:** Record evidence gaps and assessor confidence separately from the risk rating.
- **Adaptable:** Apply organization-defined criteria and governance without representing local choices as universal requirements.

For this methodology:

- **Risk scenario:** A description of a plausible event or sequence of events, the conditions that enable it, what may be affected, and the resulting consequences.
- **Threat source/event:** A source or event capable of contributing to a harmful scenario.
- **Vulnerability or enabling condition:** A weakness, exposure, dependency, or other condition that may allow or worsen a scenario.
- **Inherent risk:** Risk assessed before accounting for the relevant existing controls.
- **Existing control:** A control already implemented and relevant to the scenario.
- **Residual risk:** Risk remaining after the effect of relevant existing controls is considered.
- **Risk owner:** The person or role accountable for decisions about a particular risk.
- **Treatment owner:** The person or role responsible for delivering a treatment action; this may differ from the risk owner.
- **Risk acceptance:** An affirmative, documented decision by an authorized person or body to retain residual risk.
- **Evidence confidence:** An assessor's documented view of the strength and sufficiency of evidence supporting a judgment; it is not automatically part of the risk score.

Organizations may maintain additional terms in a controlled glossary. Where a governing standard or regulation defines a term differently, the organization should identify the terminology used for the assessment.

## 4. Roles and Responsibilities

Roles may be combined in smaller organizations, provided accountability and any required independence are documented.

| Role | Core responsibilities |
|---|---|
| Assessment lead | Plans and coordinates the assessment; confirms scope and criteria; oversees analysis; ensures findings and limitations are documented; coordinates reporting and review |
| Assessment team | Collects and analyzes information; develops scenarios; assesses controls and risk; records evidence, assumptions, and recommendations |
| Asset/system or process owner | Provides context and access to relevant records; validates factual details; explains operational dependencies; reviews impacts and proposed actions |
| Risk owner | Evaluates treatment options; owns risk-related decisions; accepts residual risk only within delegated authority; escalates decisions beyond that authority |
| Treatment/remediation owner | Plans and implements assigned actions; reports progress and obstacles; supplies remediation evidence |
| Independent reviewer/auditor | Provides review where required or warranted by risk, complexity, uncertainty, or organizational rules |
| Management/approving authority | Approves decisions and exceptions within its authority; resolves escalated risks; allocates resources and oversight as applicable |

Risk acceptance and assessment approval are separate decisions. A person who approves an assessment report does not automatically have authority to accept every risk identified in it.

## 5. Methodology Overview

The substantive risk assessment process is:

1. Establish context, scope, criteria, assumptions, and time horizon.
2. Identify relevant assets, processes, objectives, and stakeholders.
3. Identify and document risk scenarios.
4. Analyze inherent likelihood and impact.
5. Identify relevant existing controls and assess their design, implementation, and operating effectiveness.
6. Determine residual likelihood and impact, considering the evidence for existing controls.
7. Evaluate and prioritize risks against organizational criteria, obligations, and risk appetite.
8. Select and document treatment, ownership, deadlines, and any required acceptance.
9. Record results, obtain appropriate review, and monitor changes or actions.

The process is iterative. New evidence, changed assumptions, ineffective controls, or material changes to a scenario may require reassessment of earlier steps.

The broader engagement lifecycle—including planning gates, technical assessment tracks, evidence management, reporting, retesting, and closure—is addressed in the [Assessment Lifecycle](assessment-lifecycle.md).

## 6. Assessment Preparation and Context

Before analyzing risks, the assessment lead should establish and document:

- assessment objectives and decision(s) the assessment is intended to support;
- in-scope assets, services, information, processes, locations, and third parties;
- exclusions and boundaries;
- applicable assessment criteria, standards, internal policies, and obligations;
- relevant business objectives, dependencies, operating context, and stakeholder needs;
- asset or process criticality and sensitivity, where known;
- assessment roles, contacts, and risk owners;
- information sources and permitted assessment methods;
- the time horizon used to estimate likelihood;
- organization-defined risk appetite, tolerance, and acceptance criteria, where available;
- known assumptions, constraints, and evidence gaps; and
- required records, reporting, review, and approval arrangements.

The scope and authorization requirements in the assessment lifecycle must be met before assessment activity begins. If scope or authorization is unclear, the affected activity should not proceed until the issue is resolved through the appropriate authority.

Where an organization has not defined risk appetite or acceptance criteria, the assessor should record that limitation and identify the decision authority responsible for establishing or approving criteria. The assessor must not silently invent organizational thresholds.

## 7. Asset, Process, and Risk-Scenario Identification

### 7.1 Identify what may be affected

Identify relevant information, systems, services, business processes, people, facilities, suppliers, and organizational objectives. Consider dependencies and shared services, not only directly managed assets.

Use existing inventories, architecture records, business-impact analyses, service maps, interviews, technical evidence, contracts, incident records, and other relevant sources where available. Record material gaps in asset or dependency information.

### 7.2 Develop scenarios

Each material scenario should explain:

1. **Affected subject:** the asset, information, process, service, stakeholder, or objective at risk.
2. **Threat source or initiating event:** the actor, event, failure, or circumstance that could start the scenario, where known.
3. **Enabling conditions:** relevant vulnerability, exposure, dependency, process weakness, or control deficiency.
4. **Plausible event path:** how the scenario could occur, expressed at a level appropriate to the assessment.
5. **Consequences:** credible effects on security outcomes, operations, finances, legal or regulatory obligations, reputation, or other relevant objectives.
6. **Existing controls:** controls that may prevent, detect, contain, or recover from the scenario.

A vulnerability finding may be an input to a scenario, but a vulnerability alone does not necessarily describe the event, affected objective, or consequence needed for risk analysis.

### 7.3 Sources for scenario identification

Use a combination of sources as appropriate:

- established threat catalogues and scenario libraries;
- interviews and workshops with knowledgeable stakeholders;
- technical assessment findings and configuration evidence;
- incident, near-miss, and loss history;
- threat intelligence, where available and relevant;
- prior risk registers, audit reports, and control assessments; and
- changes in business context, technology, dependencies, or threat exposure.

No single source should be treated as complete. The absence of known incidents does not, by itself, establish that a scenario is unlikely.

### 7.4 Classification and traceability

Assign each scenario a unique identifier and one or more relevant risk domains. Link it to affected assets/processes, relevant controls, evidence, treatment actions, and owners. Avoid duplicate records where the same underlying scenario is already tracked; where records are consolidated, preserve traceability to distinct consequences and accountable owners.

## 8. Inherent-Risk Analysis

Assess inherent risk before taking credit for the effect of relevant existing controls.

For each scenario:

1. Describe the credible event path and consequences.
2. Estimate likelihood over the defined time horizon.
3. Estimate impact across relevant dimensions.
4. Record the rationale, supporting evidence, assumptions, and important limitations.
5. Determine the inherent rating using the approved scoring model.

Inherent risk is an analytical baseline, not a claim that an organization can or should remove all controls before making a decision. It should be estimated consistently and should not include unverified benefits from planned controls.

## 9. Existing-Control Assessment

Identify controls relevant to the scenario and assess, as applicable:

- **Design:** whether the control is suitably designed to address the relevant cause or consequence.
- **Implementation:** whether the control is present and configured or established as intended.
- **Operating effectiveness:** whether available evidence indicates that the control operates as intended over the relevant period.

Evidence may include configuration records, policies and procedures, system logs, test results, interviews, observation, access reviews, incident records, and other relevant artifacts. The appropriate evidence depends on the control and the decision being supported.

Control existence alone does not establish effectiveness. Where controls are absent, ineffective, partially implemented, not tested, or supported by insufficient evidence, record the condition and its likely effect on the scenario analysis.

Distinguish clearly between:

- existing and evidenced controls;
- existing controls whose effectiveness is only partially known;
- ineffective or deficient controls; and
- planned or proposed controls.

Planned controls may be considered in a treatment proposal, but their expected effect must not be represented as verified current risk reduction.

## 10. Residual-Risk Analysis

Estimate residual risk after considering the relevant existing controls and the evidence about their effectiveness.

For each scenario:

1. Identify how existing controls affect the event path, likelihood, impact, or both.
2. Explain which controls support the residual-risk estimate and how.
3. Reassess likelihood and impact using the same approved scales and time horizon, unless a documented reason requires a different basis.
4. Determine the residual rating using the approved scoring model.
5. Record uncertainty, evidence gaps, assumptions, and control limitations.

Do not apply a mechanical reduction merely because a control is listed. If evidence does not support a claimed control effect, do not assume that effect without documenting the uncertainty and rationale.

Where inherent and residual ratings are identical, document why existing controls do not materially change the estimate or why evidence is insufficient to justify a reduction.

## 11. Likelihood and Impact Analysis

### 11.1 Likelihood

Estimate the likelihood of the complete scenario over a defined time horizon. Consider relevant evidence about:

- threat capability or intent, where applicable;
- exposure and accessibility;
- vulnerabilities and other enabling conditions;
- existing control design and operating effectiveness;
- relevant incident history and observed frequency, where meaningful; and
- environmental, operational, and business context.

Historical frequency may inform the estimate but should not automatically replace scenario analysis. Lack of historical incidents is not, by itself, evidence of low likelihood. State the time horizon and explain material assumptions.

### 11.2 Impact

Assess credible consequences across the dimensions relevant to the scenario, including:

- confidentiality, integrity, and availability;
- operational disruption and service degradation;
- financial loss;
- legal, regulatory, and contractual exposure;
- reputational harm; and
- other business or stakeholder impacts identified by the organization.

Consider the scale, duration, recoverability, and reach of consequences where relevant. Use the organization's approved impact criteria where available. Do not invent financial thresholds or universal impact bands in the absence of approved criteria.

When multiple assets or processes are affected, use the **highest credible impact** as the scenario-level impact basis. Document materially different consequences so that a single rating does not conceal important effects or dependencies.

### 11.3 Evidence and uncertainty

Record evidence quality and assessor confidence separately from the risk rating. Identify:

- facts supported by evidence;
- assumptions and analytical judgments;
- missing, stale, contradictory, or incomplete information;
- limitations in scope or access; and
- how uncertainty may affect the result or decision.

Where incomplete evidence could materially affect a decision, a conservative assumption may be appropriate. The assessor should justify the assumption, identify its effect on the rating, and state what evidence or follow-up would reduce uncertainty.

Do not introduce an unapproved confidence multiplier or automatically fold confidence into the risk score. If uncertainty is material, escalate or qualify the decision rather than presenting an unsupported level of precision.

## 12. Risk Scoring and Evaluation

### 12.1 Apply the approved scoring model

This methodology uses semi-quantitative analysis: defined likelihood and impact scales are combined into a risk rating according to the organization's approved scoring model.

The companion [Risk Scoring Model](risk-scoring-model.md) is intended to specify the exact scales, matrix or calculation, rating bands, and interpretation rules. Until that model is established and approved, this document does not prescribe a numerical formula, universal threshold, or fixed rating boundary.

Apply the same approved model consistently across comparable scenarios. Record the selected levels and rationale rather than recording only a score.

### 12.2 Evaluate against organizational criteria

A risk score informs evaluation but does not replace it. Compare the rating and rationale with:

- organization-defined acceptance criteria and risk appetite/tolerance;
- legal, regulatory, contractual, and internal-policy obligations;
- business objectives, service requirements, and operational dependencies;
- the credibility and severity of potential consequences; and
- relevant uncertainty and evidence limitations.

Where an obligation prohibits a particular condition or requires action, a low calculated score does not override that obligation. Where credible severe consequences warrant attention beyond the score-based result, document the rationale and escalate as appropriate.

If the organization has not established applicable criteria, record the gap and seek direction from the appropriate decision authority. Do not represent assessor-selected thresholds as formally approved organizational risk appetite.

### 12.3 Prioritization

Prioritize scenarios based on their evaluated risk, applicable obligations, credible consequences, exposure, dependencies, and the urgency of available treatment. The order of work may differ from a simple numerical ranking where a documented obligation, critical dependency, or time-sensitive exposure warrants earlier action.

Document material departures from score-based ordering and the authority responsible for the decision.

## 13. Risk Treatment Planning

Select one or more treatment approaches for each risk, as appropriate:

| Treatment | Description |
|---|---|
| Mitigate | Implement or improve controls or other measures to reduce likelihood, impact, or both |
| Avoid | Stop, discontinue, or change the activity that creates the risk |
| Transfer/share | Allocate or share part of the risk through suitable contractual, insurance, service, or other arrangements; assess any residual exposure |
| Accept | Formally retain residual risk through a documented decision by an authorized risk owner or approving authority |

Treatment decisions should record:

- selected option and rationale;
- intended outcome and expected risk change;
- actions, milestones, and dependencies;
- accountable treatment owner;
- target dates established under applicable policy and risk considerations;
- resources or approvals required;
- residual risk expected after treatment, where it can reasonably be estimated; and
- how and when effectiveness will be validated.

Do not assume that transfer eliminates the organization's risk or accountability. Do not treat proposed controls as effective until implementation and relevant effectiveness have been verified.

### 13.1 Remediation deadlines and overdue actions

Remediation deadlines should be established under organizational policy, taking account of risk rating, exposure, potential impact, applicable obligations, operational feasibility, and available compensating measures.

This methodology does not prescribe universal remediation windows. If an action becomes overdue, record the reason, notify the accountable owner, document interim measures where relevant, and escalate according to policy and delegated authority. An overdue action does not itself constitute risk acceptance.

## 14. Risk Ownership, Acceptance, and Escalation

Each material risk should have a designated risk owner accountable for risk-related decisions. Treatment actions should also have accountable owners; these roles may be different.

### 14.1 Acceptance requirements

A residual-risk acceptance record should identify:

- the risk and its current residual rating;
- the rationale for acceptance;
- relevant evidence, assumptions, and limitations;
- the accepting risk owner or approving authority;
- the basis for that person's delegated authority;
- the decision date and any conditions;
- any expiry or review date, where applicable; and
- required monitoring or compensating measures.

Risk acceptance must be affirmative, documented, and traceable. Silence, a missed deadline, lack of response, or failure to complete remediation does not constitute acceptance.

### 14.2 Delegated authority and escalation

The risk owner may accept residual risk only within delegated authority. Risks exceeding that authority must be escalated to the appropriate approving authority under the organization's governance arrangements.

This methodology does not impose a universal management hierarchy or require a particular committee structure. The organization should identify who can accept which categories or levels of risk and how decisions are recorded.

Risk acceptance cannot override applicable law, binding contractual obligations, or non-waivable organizational requirements. Where a risk cannot lawfully or contractually be accepted, escalate it and determine the required action.

### 14.3 Review of accepted risks

Accepted risks should remain visible in the risk register and be reviewed at defined intervals or when relevant conditions change. Acceptance should be reconsidered if exposure, impact, threat conditions, control effectiveness, business context, or applicable obligations materially change.

## 15. Risk Register and Required Records

Maintain a risk register that supports traceability from scenario identification through analysis, treatment, acceptance, and reassessment.

A comprehensive record should include, as applicable:

| Record area | Minimum information |
|---|---|
| Identification | Unique risk ID, assessment reference, title, domain, status |
| Scenario | Affected assets/processes/objectives, threat or initiating event, causes, vulnerabilities, enabling conditions, event path, consequences |
| Context | Scope, time horizon, relevant criteria, assumptions, and dependencies |
| Inherent risk | Likelihood, impact, rating, scoring-model reference, and rationale |
| Controls | Relevant existing controls, design/implementation/effectiveness evidence, gaps, and limitations |
| Residual risk | Likelihood, impact, rating, rationale, and control effect considered |
| Evidence and confidence | Source/provenance, evidence references, material assumptions, confidence, gaps, and uncertainty |
| Evaluation | Acceptance criteria, risk appetite/tolerance where defined, applicable obligations, priority, and rationale |
| Treatment | Selected option, actions, expected outcome, treatment owner, dependencies, target dates, and status |
| Acceptance | Decision, rationale, accepting authority, delegated-authority basis, conditions, and review/expiry date where applicable |
| Monitoring and history | Escalations, review dates, reassessment results, treatment validation, decision changes, and closure/disposition records |

Organizations may add fields required by their governance, technology, industry, or obligations. A tiered implementation may use a core set for low-complexity cases, but substantive risk decisions should retain enough information to explain and reproduce the reasoning.

## 16. Evidence, Information Protection, and Review

### 16.1 Evidence handling

Handle evidence in proportion to assessment purpose, sensitivity, criticality, and the consequences of an incorrect or disputed decision.

Appropriate measures may include:

- recording the source, collection context, and provenance of evidence;
- retaining sufficient support for material risk judgments;
- restricting access to sensitive records;
- using approved storage and transfer methods;
- applying cryptographic hashes when integrity verification is justified;
- using formal chain-of-custody records when forensic, legal, investigative, or other traceability requirements warrant them; and
- applying organizational retention, disposition, and investigation-hold requirements.

The methodology does not require forensic-grade chain of custody for every routine assessment. Evidence handling should be consistent with the assessment lifecycle and any applicable evidence-handling procedure.

### 16.2 Review independence and quality

Review depth and independence should be proportionate to risk, complexity, uncertainty, and organizational requirements.

Where independent review is unavailable, the assessment lead should document self-review, its limitations, and any additional assurance measures considered. High-risk, disputed, or consequential conclusions should receive additional scrutiny where feasible and appropriate.

Review should consider whether scenarios are coherent, evidence supports material judgments, controls have been evaluated appropriately, scoring rules have been applied consistently, and conclusions and treatment recommendations follow from the analysis.

## 17. Reporting and Approval

Provide an executive summary for decision-makers alongside a technical report and comprehensive risk register. Tailor detail to the audience while preserving traceability and material limitations.

Reports should include, as applicable:

1. Executive summary and material decisions required.
2. Assessment objectives, scope, dates, participants, and criteria.
3. Methodology, sources, and activities.
4. Coverage, exclusions, assumptions, and limitations.
5. Material scenarios, affected assets/processes, and supporting evidence.
6. Inherent and residual ratings with rationale.
7. Control effectiveness observations and evidence gaps.
8. Prioritized treatment recommendations, owners, and target dates.
9. Accepted risks, approval records, unresolved actions, and escalations.
10. Review and approval records.

Restrict distribution to authorized recipients under applicable classification and access requirements. Sensitive evidence may be separated from the general report where appropriate.

Assessment approval and risk acceptance must remain distinct. The assessment lead and relevant asset/system or process owner should review factual accuracy and scope as appropriate. Management or other approving-authority review should occur where policy, risk, or delegated authority requires it. A report signature must not be interpreted as blanket acceptance of every risk in the report.

## 18. Monitoring and Reassessment

Reassess risks periodically and when material changes make existing conclusions unreliable. Frequency should be proportionate to risk, asset or process criticality, change rate, exposure, and applicable obligations.

Event-triggered reassessment may be warranted by:

- material system, architecture, process, supplier, or dependency changes;
- a significant new vulnerability, threat, or exposure;
- a security incident or suspected compromise;
- a material change in business objectives, impact, or risk exposure;
- changes to applicable legal, regulatory, contractual, or policy requirements;
- control failure or evidence that a prior control-effectiveness assumption is no longer valid; or
- a treatment, acceptance, or review condition reaching its defined review point.

After assessment, accountable owners should track treatment actions and accepted risks. Reassess ratings and decisions when evidence, conditions, controls, or obligations change. Record material changes and the rationale for retaining or changing prior decisions.

## 19. Limitations and Adaptation Guidance

This methodology provides a common process, not a universal risk appetite, scoring formula, legal interpretation, or organizational governance structure.

Organizations must define or approve, as appropriate:

- risk appetite, tolerance, and acceptance criteria;
- likelihood and impact scales and scoring rules;
- authority for treatment and risk acceptance;
- remediation deadlines and escalation arrangements;
- evidence retention, classification, and access rules;
- assessment frequency and reporting requirements; and
- applicable legal, regulatory, contractual, and sector-specific requirements.

Where a criterion or governance arrangement is missing, document the gap and seek an authorized decision rather than silently substituting an assessor's preference. Adaptations should preserve traceability, clear accountability, and explicit treatment of uncertainty.

External framework references are methodological reference points, not proof that the organization complies with those frameworks. Any mapping between this methodology and a standard should identify its basis and limitations.

## 20. Related Documents and References

### Related repository documents

- [Assessment Lifecycle](assessment-lifecycle.md) — overall engagement lifecycle, roles, stage gates, reporting, and closure.
- [Risk Scoring Model](risk-scoring-model.md) — intended companion specification for likelihood/impact scales, score calculation or matrix, and rating interpretation.
- [Evidence Handling](evidence-handling.md) — intended companion procedure for evidence provenance, integrity, protection, custody, and retention.
- [Standards and Frameworks](../../references/standards-and-frameworks.md) — reference register for external standards and guidance.

Some companion documents may be developed separately. Links should be verified as those files are added to the repository.

### Primary and supporting references

Consult the applicable edition and any current errata, amendments, or updates before relying on a reference:

- NIST SP 800-30 Rev. 1, *Guide for Conducting Risk Assessments*.
- NIST Cybersecurity Framework (CSF) 2.0.
- ISO/IEC 27005, *Information security risk management* (use the applicable current edition).
- ISO/IEC 27001, *Information security management systems — Requirements*, where an ISMS context is relevant.

This document is an independently authored methodology. It is not an official NIST or ISO publication and does not claim endorsement by those organizations.

---

## Document Control

| Field | Value |
|---|---|
| Document | Risk Assessment Methodology |
| Repository path | `docs/methodology/risk-assessment-methodology.md` |
| Version | 1.0.0 |
| Status | Initial release |
| Owner | Repository maintainer |
| Review cycle | Organization-defined; review sooner when material references, methodology assumptions, or requirements change |
| Change control | Record substantive revisions in the repository changelog |
