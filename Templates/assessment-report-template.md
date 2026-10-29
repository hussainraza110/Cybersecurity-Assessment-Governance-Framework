# Cybersecurity Assessment Report Template

> **Document type:** Reusable assessment report template  
> **Suggested repository path:** `templates/assessment-report-template.md`  
> **Status:** Template — tailor and approve for organizational use before operational adoption  
> **Version:** 1.0  
> **Report owner:** `[Organization / function]`  
> **Report ID:** `[REPORT-YYYY-###]`  
> **Classification:** `[Organization-defined]`  
> **Date:** `[YYYY-MM-DD]`

## Instructions for use

This template supports technical, governance, policy, infrastructure, configuration, control-effectiveness, vulnerability, and risk-focused assessments. Adapt sections to the approved scope and assessment type. Mark sections that do not apply as `Not applicable` with a short rationale when needed for traceability.

- Replace bracketed placeholders with assessment-specific information.
- Distinguish verified observations from interpretation, assumptions, and recommendations.
- Reference evidence by ID and approved storage location; do not embed credentials, secrets, or unnecessary sensitive information.
- Use the organization's approved risk scoring model, finding criteria, acceptance authority, and remediation deadlines.
- Do not claim that testing was exhaustive or that compliance is established unless the scope, criteria, evidence, and authority support that conclusion.
- Apply the organization's classification, distribution, retention, and handling rules to the report and its appendices.

### Related framework documents

- [Assessment lifecycle](../docs/methodology/assessment-lifecycle.md)
- [Risk assessment methodology](../docs/methodology/risk-assessment-methodology.md)
- [Risk scoring model](../docs/methodology/risk-scoring-model.md)
- [Evidence handling](../docs/methodology/evidence-handling.md)
- [Standards and frameworks register](../references/standards-and-frameworks.md)
- [Risk register template](risk-register-template.md)

---

## 1. Document control and handling

### 1.1 Report metadata

| Field | Value |
|---|---|
| Report ID | `[Unique report identifier]` |
| Report title | `[Assessment title]` |
| Assessment ID | `[Assessment identifier]` |
| Version | `[Version]` |
| Status | `[Draft / In review / Approved / Superseded]` |
| Assessment start date | `[YYYY-MM-DD]` |
| Assessment end date | `[YYYY-MM-DD]` |
| Report date | `[YYYY-MM-DD]` |
| Report owner | `[Role / function]` |
| Lead assessor | `[Role / team]` |
| Assessment sponsor | `[Role / function]` |
| Classification | `[Organization-defined]` |
| Distribution | `[Authorized recipients / groups]` |
| Approved storage location | `[Repository / document system reference]` |
| Retention / disposal rule | `[Applicable policy or schedule]` |

### 1.2 Review and approval history

| Version | Date | Author | Reviewer / approver | Change summary | Status |
|---|---|---|---|---|---|
| `0.1` | `[YYYY-MM-DD]` | `[Role]` | `[Role / Pending]` | Initial draft | Draft |
| `[ ]` | `[YYYY-MM-DD]` | `[Role]` | `[Role]` | `[Change]` | `[Status]` |

### 1.3 Handling instructions

- **Authorized audience:** `[Who may receive or access this report]`
- **Restrictions on onward distribution:** `[Requirements or None]`
- **Sensitive annexes:** `[Annex IDs and separate access requirements, or None]`
- **Handling notes:** `[Redaction, storage, transmission, or other requirements]`

Do not include raw secrets, credentials, exploit details unnecessary for remediation, or sensitive personal information in the general report. Use appropriately restricted evidence stores and annexes where required.

---

## 2. Executive summary

> Complete this section for management readers. Keep it concise, decision-oriented, and consistent with the detailed findings and limitations.

### 2.1 Purpose and scope

`[State why the assessment was conducted, the principal objectives, and the systems, processes, controls, or organizational boundary covered.]`

### 2.2 Overall conclusion

`[Summarize what the evidence supports about the assessed scope and criteria. State material limitations. Avoid blanket claims that an organization is secure or compliant unless properly supported and authorized.]`

### 2.3 Key results

| Measure | Result |
|---|---|
| Scope items / control areas assessed | `[Count or concise description]` |
| Findings identified | `[Count]` |
| Critical findings | `[Count or N/A under approved scheme]` |
| High findings | `[Count or N/A]` |
| Moderate findings | `[Count or N/A]` |
| Low findings | `[Count or N/A]` |
| Findings requiring management decision | `[Count / summary]` |
| Material evidence gaps or scope limitations | `[Summary]` |

Use only the severity categories adopted by the organization. If a category was not used or is not applicable, say so rather than implying a zero count.

### 2.4 Principal risks and business implications

1. **`[Risk / finding ID and title]`** — `[Concise consequence and affected objective or service]`
2. **`[Risk / finding ID and title]`** — `[Concise consequence and affected objective or service]`
3. **`[Risk / finding ID and title]`** — `[Concise consequence and affected objective or service]`

### 2.5 Recommended management priorities

| Priority | Required decision or action | Accountable role | Target date / decision point |
|---|---|---|---|
| `[Priority]` | `[Action or decision]` | `[Role]` | `[Date / TBD]` |
| `[Priority]` | `[Action or decision]` | `[Role]` | `[Date / TBD]` |

### 2.6 Decisions required

`[Identify risk acceptance, funding, resource allocation, escalation, exception approval, or other decisions. State the relevant risk IDs and delegated decision authority.]`

---

## 3. Assessment overview

### 3.1 Objectives and questions

- **Primary objective:** `[Objective]`
- **Assessment questions:** `[Questions the assessment was designed to answer]`
- **Intended use of results:** `[Decision, assurance, improvement, or other purpose]`
- **Assessment type(s):** `[Technical / governance / policy / infrastructure / configuration / vulnerability / control effectiveness / risk-focused / other]`

### 3.2 Scope and boundaries

| Scope item | Description |
|---|---|
| In-scope systems / assets / services | `[Identifiers and descriptions]` |
| In-scope business processes / control areas | `[Items]` |
| Environments / locations | `[Production / test / cloud / standalone / other]` |
| Network zones / trust boundaries | `[Where applicable]` |
| Information types | `[Data or information categories, as relevant]` |
| Third parties / dependencies | `[Included dependencies]` |
| Out-of-scope items | `[Items and rationale]` |
| Assessment period / snapshot date | `[Period or date]` |

### 3.3 Authorization and rules of engagement

- **Authorization reference:** `[Approval / engagement record ID]`
- **Authorized activities:** `[Permitted review, testing, collection, interviews, sampling, or validation]`
- **Prohibited or restricted activities:** `[Restrictions]`
- **Contacts and escalation route:** `[Roles / contact process]`
- **Safety and operational constraints:** `[Maintenance windows, availability limits, change controls, or other constraints]`

State only activities actually authorized and performed. Do not imply that invasive testing, exploitation, forensic acquisition, or production changes occurred unless documented.

### 3.4 Assessment criteria

| Criterion / reference | Version / edition | Applicability | How used |
|---|---|---|---|
| `[Policy / baseline / standard / control objective]` | `[Version / date]` | `[Scope]` | `[Assessment criterion or mapping]` |
| `[Reference]` | `[Version / date]` | `[Scope]` | `[Use]` |

Identify which criteria were mandatory, organization-defined, advisory, or used only as a comparison. Verify the applicable edition and obligations before finalizing.

---

## 4. Methodology and execution

### 4.1 Approach

`[Describe the assessment approach and why it was suitable for the objectives and risk context.]`

### 4.2 Procedures performed

| Procedure ID | Procedure / activity | Scope / sample | Date | Result reference | Limitations |
|---|---|---|---|---|---|
| `[PROC-###]` | `[Interview / document review / configuration review / authorized test / observation / other]` | `[Items or sample]` | `[Date]` | `[Evidence IDs / result IDs]` | `[Limitations or None]` |
| `[PROC-###]` | `[Procedure]` | `[Scope / sample]` | `[Date]` | `[Reference]` | `[Limitations]` |

### 4.3 Sampling and coverage

- **Population considered:** `[Population / scope items]`
- **Sample selection method:** `[Method and rationale]`
- **Items tested / reviewed:** `[Count or list reference]`
- **Items not tested / reviewed:** `[Count or list and reason]`
- **Coverage limitations:** `[How sampling or access affects conclusions]`

Do not generalize sample results to an entire population unless the sampling design and evidence justify that inference.

### 4.4 Evidence collection and validation

`[Summarize evidence sources, validation and corroboration approach, provenance records, integrity controls, and handling arrangements. Link to the evidence register and evidence-handling procedure.]`

- **Evidence register:** `[Location / reference]`
- **Validation approach:** `[Approach]`
- **Integrity / custody records:** `[References, where applicable]`
- **Sensitive evidence handling:** `[Approved location and access restrictions]`

### 4.5 Risk assessment method

- **Risk methodology:** `[Approved methodology reference and version]`
- **Scoring model:** `[Approved model reference and version]`
- **Likelihood horizon:** `[Defined period]`
- **Impact dimensions:** `[Applicable dimensions]`
- **Rating bands / acceptance criteria:** `[Organization-approved criteria]`
- **Overrides or exceptions:** `[None or documented references]`

Distinguish finding severity from risk rating and remediation priority. Use the risk register for detailed scenario analysis and treatment governance.

---

## 5. Assessment results

### 5.1 Overall results summary

`[Summarize the main results, patterns, strengths, control gaps, dependencies, and recurring causes. Separate observed facts from interpretation.]`

### 5.2 Finding summary register

| Finding ID | Finding title | Category | Affected scope | Severity / priority | Related risk ID | Status | Owner | Target date |
|---|---|---|---|---|---|---|---|---|
| `[FIND-###]` | `[Title]` | `[Category]` | `[Asset / control / process]` | `[Approved classification]` | `[RISK-### / N/A]` | `[Status]` | `[Role]` | `[Date / TBD]` |
| `[FIND-###]` | `[Title]` | `[Category]` | `[Scope]` | `[Classification]` | `[Risk ID]` | `[Status]` | `[Role]` | `[Date / TBD]` |

### 5.3 Positive observations and effective practices

`[Record practices or controls that were observed and supported by evidence. State the scope of validation and avoid extrapolating beyond it.]`

### 5.4 Cross-cutting themes

| Theme | Supporting findings / evidence | Risk or operational implication | Recommended response |
|---|---|---|---|
| `[Theme]` | `[IDs]` | `[Implication]` | `[Response]` |
| `[Theme]` | `[IDs]` | `[Implication]` | `[Response]` |

---

## 6. Detailed findings

Copy the following record for each material finding. Ensure the finding ID remains consistent across the report, risk register, evidence register, and remediation tracker.

### Finding `[FIND-###]` — `[Finding title]`

#### 6.1 Identification

| Field | Value |
|---|---|
| Finding ID | `[FIND-###]` |
| Category | `[Technical / governance / policy / configuration / process / control / other]` |
| Status | `[Open / In progress / Pending validation / Remediated—awaiting verification / Verified closed / Accepted / Deferred under approved exception / Reopened]` |
| Severity / priority | `[Organization-approved category]` |
| Assessment procedure | `[Procedure ID(s)]` |
| Affected assets / processes | `[IDs and descriptions]` |
| Related risk IDs | `[IDs or Pending assessment]` |
| Related control IDs | `[IDs or N/A]` |
| Evidence IDs | `[IDs]` |
| Finding owner | `[Role]` |
| Remediation owner | `[Role]` |
| Date identified | `[YYYY-MM-DD]` |
| Target date | `[Approved date / TBD]` |

#### 6.2 Observation

**Condition observed**

`[State exactly what was identified and where. Distinguish direct observation from inference.]`

**Expected condition / criterion**

`[Identify the applicable policy, baseline, control objective, requirement, or assessment criterion. Include version or reference.]`

**Actual condition**

`[Describe the observed state and its difference from the expected condition.]`

**Cause or contributing factors**

`[State the demonstrated or plausible cause. Label hypotheses as hypotheses if not verified.]`

#### 6.3 Evidence and validation

- **Evidence references:** `[Evidence IDs and approved locations]`
- **Validation method:** `[How the condition was confirmed]`
- **Reproduction / verification steps:** `[Authorized, proportionate steps, or reference to restricted technical annex]`
- **Corroboration:** `[Independent or supporting evidence]`
- **Limitations / evidence gaps:** `[Missing access, incomplete logs, sample limitations, or None]`
- **Confidence:** `[Organization-defined scale and rationale]`

Do not include credentials, secrets, or unnecessary sensitive details in the general report. Keep raw evidence in approved storage.

#### 6.4 Risk and consequence

**Risk scenario**

> Because `[cause / weakness]`, `[event]` may occur, resulting in `[credible consequence]`.

- **Affected objectives / stakeholders:** `[Items]`
- **Impact dimensions:** `[Confidentiality / integrity / availability / operational / financial / legal-regulatory / reputation / other, as applicable]`
- **Likelihood:** `[Rating, horizon, and rationale, if assessed]`
- **Impact:** `[Rating and rationale, if assessed]`
- **Risk score / band:** `[Value and approved model reference, if assessed]`
- **Confidence / uncertainty:** `[Separate from rating]`
- **Existing controls and limitations:** `[Control IDs and evidence]`
- **Risk register reference:** `[Risk ID / location]`

If the observation is not assessed as a distinct risk scenario, explain why or record the risk assessment as pending. Do not invent a numeric score when the approved method or evidence does not support one.

#### 6.5 Recommendation and action

**Recommended corrective action**

`[Describe the desired outcome and proportionate corrective or preventive measures.]`

**Immediate containment / compensating measures**

`[Where appropriate, state authorized temporary measures, owners, and limitations.]`

| Action ID | Action / deliverable | Owner | Dependency | Target date | Verification criteria |
|---|---|---|---|---|---|
| `[ACT-###]` | `[Specific, verifiable action]` | `[Role]` | `[Dependency / None]` | `[Approved date / TBD]` | `[Evidence and test required]` |
| `[ACT-###]` | `[Action]` | `[Role]` | `[Dependency]` | `[Date / TBD]` | `[Criteria]` |

**Verification evidence required:** `[Configuration evidence, retest, approved record, control sample, or other suitable evidence]`

**Residual risk / decision:** `[Expected remaining exposure, risk-owner decision required, and acceptance authority where applicable]`

#### 6.6 Finding disposition and closure

- **Owner response:** `[Agreed / Partially agreed / Disputed / Pending, with rationale]`
- **Disposition:** `[Open / In progress / Accepted by authorized decision-maker / Deferred under approved exception / Remediated—awaiting verification / Verified closed / Reopened]`
- **Acceptance / exception reference:** `[ID, authority, date, conditions, expiry or review trigger, or None]`
- **Verification performed by / date:** `[Role and date]`
- **Verification result:** `[Effective / Partially effective / Ineffective / Not yet tested]`
- **Closure decision and authority:** `[Decision, role, date, or Pending]`
- **Closure evidence:** `[Evidence IDs]`
- **Reopening triggers:** `[Conditions requiring reassessment]`

A finding is not verified closed merely because an action is reported complete. Acceptance of risk is a separate, documented decision and does not itself prove the underlying condition was corrected.

---

## 7. Consolidated risk and remediation plan

### 7.1 Risk summary

| Risk ID | Scenario / title | Inherent rating | Current rating | Target residual rating | Treatment | Risk owner | Decision / escalation | Next review |
|---|---|---|---|---|---|---|---|---|
| `[RISK-###]` | `[Scenario title]` | `[Score / band]` | `[Score / band]` | `[Forecast score / band]` | `[Avoid / Mitigate / Transfer-share / Accept]` | `[Role]` | `[State / authority]` | `[Date]` |

Target residual ratings are forecasts until planned treatment has been implemented and effectiveness verified. Acceptance must be explicit and authorized; silence or an overdue action is not acceptance.

### 7.2 Consolidated action tracker

| Action ID | Related finding / risk | Required outcome | Priority | Owner | Target date | Status | Verification reference |
|---|---|---|---|---|---|---|---|
| `[ACT-###]` | `[IDs]` | `[Outcome]` | `[Approved priority]` | `[Role]` | `[Date / TBD]` | `[Status]` | `[Evidence ID / Pending]` |

### 7.3 Dependencies, overdue actions, and escalation

`[Describe cross-team dependencies, overdue actions, blockers, decision requests, escalation route, and the authority responsible for resolution.]`

### 7.4 Residual risk and acceptance decisions

`[List residual risks requiring owner decisions, acceptance records, compensating controls, review conditions, or escalation because they exceed delegated authority or approved tolerance.]`

---

## 8. Limitations, assumptions, and qualifications

### 8.1 Scope and access limitations

`[Document unavailable systems, inaccessible records, denied or constrained tests, unavailable personnel, or other limitations.]`

### 8.2 Sampling and coverage limitations

`[Describe sample design, untested items, and how findings may or may not generalize to the wider population.]`

### 8.3 Evidence limitations and uncertainty

`[Identify incomplete, contradictory, stale, or uncorroborated evidence and its effect on conclusions and confidence.]`

### 8.4 Assumptions and dependencies

`[List material assumptions and dependencies that could change the results if invalidated.]`

### 8.5 Conclusion qualifications

`[State what the assessment does and does not establish. Avoid claiming exhaustive assurance, compliance, or absence of vulnerabilities beyond the scope and evidence.]`

---

## 9. Quality review and report approval

### 9.1 Quality assurance checklist

- [ ] Report scope matches the authorization and assessment records.
- [ ] Objectives and assessment criteria are explicit.
- [ ] Procedures performed and limitations are documented.
- [ ] Material findings have evidence references and validation rationale.
- [ ] Observed facts, interpretation, assumptions, and recommendations are distinguishable.
- [ ] Risk ratings follow the approved methodology and scoring model.
- [ ] Finding severity, risk rating, and remediation priority are not conflated.
- [ ] Executive summary agrees with detailed findings and risk tables.
- [ ] Recommendations are actionable and include verification criteria.
- [ ] Owners, dates, approvals, and acceptance decisions are correctly represented.
- [ ] Evidence references are valid and sensitive material is appropriately protected.
- [ ] Applicable appendices are complete or marked not applicable with rationale.
- [ ] Claims about standards or compliance are appropriately qualified.
- [ ] Required reviews and approvals are recorded.

### 9.2 Approval record

| Role | Name / identifier | Decision | Date | Comments / conditions |
|---|---|---|---|---|
| Lead assessor | `[Role / name]` | `[Submitted / Approved]` | `[YYYY-MM-DD]` | `[Comments]` |
| Technical reviewer | `[Role / name]` | `[Approved / Changes required]` | `[YYYY-MM-DD]` | `[Comments]` |
| Report owner | `[Role / name]` | `[Approved / Changes required]` | `[YYYY-MM-DD]` | `[Comments]` |
| Risk owner / management approver, where required | `[Role / name]` | `[Decision / N/A]` | `[YYYY-MM-DD]` | `[Decision reference]` |

Report approval does not automatically constitute acceptance of any risk or exception. Record those decisions separately in the appropriate risk record.

---

## 10. Appendices

Include only the appendices appropriate to the assessment. Keep restricted technical evidence in approved locations and reference it rather than duplicating sensitive content.

### Appendix A — Scope inventory

| Item ID | Asset / process / control area | Owner | Environment / location | In scope? | Procedure / evidence references |
|---|---|---|---|---|---|
| `[ITEM-###]` | `[Description]` | `[Role]` | `[Environment]` | `[Yes / No]` | `[IDs]` |

### Appendix B — Methodology and criteria

- Assessment methodology: `[Document and version]`
- Risk methodology / scoring model: `[Document and version]`
- Criteria / baselines: `[References and editions]`
- Sampling method: `[Method]`
- Rating and prioritization rules: `[Approved rules]`
- Deviations / overrides: `[References and approvals, or None]`

### Appendix C — Findings index

| Finding ID | Title | Classification | Related risk | Owner | Status | Evidence references |
|---|---|---|---|---|---|---|
| `[FIND-###]` | `[Title]` | `[Category / severity]` | `[RISK-### / N/A]` | `[Role]` | `[Status]` | `[EVD IDs]` |

### Appendix D — Risk register extract

| Risk ID | Scenario | Inherent | Current | Target residual | Treatment | Approval state |
|---|---|---|---|---|---|---|
| `[RISK-###]` | `[Scenario]` | `[Score / band]` | `[Score / band]` | `[Forecast]` | `[Strategy]` | `[State]` |

### Appendix E — Evidence index

| Evidence ID | Description | Source / collector | Collection date | Validation / integrity reference | Supports | Limitation / handling |
|---|---|---|---|---|---|---|
| `[EVD-###]` | `[Description]` | `[Source / role]` | `[YYYY-MM-DD]` | `[Reference or N/A with rationale]` | `[Finding / control / rating]` | `[Limitation / classification]` |

The index is not a substitute for the evidence register or chain-of-custody records where required. Follow the organization's evidence-handling procedure for collection, transfer, integrity, retention, and disposal.

### Appendix F — Technical results

`[Summarize authorized test results, configuration observations, sanitized outputs, and technical details needed to reproduce or validate findings. Put sensitive details in a restricted annex when necessary.]`

### Appendix G — Remediation tracker

| Action ID | Finding / risk | Action | Owner | Target date | Status | Verification evidence |
|---|---|---|---|---|---|---|
| `[ACT-###]` | `[IDs]` | `[Action]` | `[Role]` | `[Date / TBD]` | `[Status]` | `[Evidence ID / Pending]` |

### Appendix H — Limitations and assumptions register

| ID | Limitation / assumption | Affected conclusion | Risk to confidence | Follow-up owner / action |
|---|---|---|---|---|
| `[LIM-###]` | `[Description]` | `[Finding / conclusion]` | `[Effect]` | `[Owner / action]` |

### Appendix I — Glossary and abbreviations

| Term | Definition in this report |
|---|---|
| `[Term]` | `[Definition]` |
| `[Acronym]` | `[Expansion / meaning]` |

### Appendix J — References

- Internal methodology documents: `[Titles, versions, and locations]`
- Policies and baselines: `[Applicable references]`
- External standards / frameworks: `[Title, edition, and applicable section]`
- Other source material: `[References]`

Verify current editions and applicability. A reference does not, by itself, demonstrate conformity.

### Appendix K — Approvals and distribution

- Approval records: `[Record IDs / location]`
- Authorized recipients: `[Roles / groups]`
- Distribution restrictions: `[Requirements]`
- Restricted annexes and access controls: `[References]`
- Retention / disposal requirements: `[Applicable schedule]`

---

## 11. Illustrative completed report

> **Fictional example only.** All organizations, systems, findings, evidence IDs, scores, dates, and roles in this section are invented for demonstration. They do not describe a real assessment.

### 11.1 Executive summary

**Report title:** Fictional Infrastructure Configuration and Privileged-Access Assessment  
**Report ID:** `REPORT-EX-001`  
**Assessment period:** `[Illustrative dates]`  
**Scope:** A fictional business-critical application server and its privileged-access controls  
**Conclusion:** The limited assessment identified weaknesses in privileged-access restriction and access-review evidence. The available fictional evidence supports remediation and follow-up validation. It does not establish the security posture of other systems or prove compliance with any standard.

**Illustrative results**

| Measure | Result |
|---|---|
| Scope items assessed | 1 fictional server and related access controls |
| Findings | 2 illustrative findings |
| High findings | 1 |
| Moderate findings | 1 |
| Material limitation | The example covers a narrow scope and does not include a comprehensive penetration test |

**Principal concerns**

1. `FIND-EX-001` — Excessive privileged access may permit unauthorized administrative changes.
2. `FIND-EX-002` — Periodic privileged-access review is not consistently evidenced.

**Recommended management priorities:** Restrict privileged access, verify privileged-authentication controls, establish a repeatable access-review process, and require evidence-based retesting before closure.

### 11.2 Scope and methodology

- **Authorization:** Fictional authorization record `AUTH-EX-001`.
- **Scope:** Fictional server `SRV-EX-01` and related privileged-access controls.
- **Procedures:** Review of a fictional access listing, configuration evidence, and access-review records.
- **Criteria:** Fictional organization-approved access-control baseline `BASE-EX-01`.
- **Limitations:** No production changes, intrusive testing, or forensic acquisition are represented. The example does not claim exhaustive coverage.
- **Risk method:** Fictional use of the framework's five-by-five likelihood-impact model and illustrative rating bands, subject to organizational approval.

### 11.3 Finding `FIND-EX-001` — Excessive privileged access

**Observation:** A fictional review of administrative group membership identified accounts whose recorded access did not have a documented current business justification.

**Expected condition:** Privileged access should be restricted to authorized roles, approved by the appropriate owner, and reviewed under the organization's defined process.

**Evidence:** `EVD-EX-001` — fictional administrative membership export; `EVD-EX-002` — fictional access-approval sample.

**Risk scenario:** Because privileged access is not sufficiently restricted, a compromised or misused account may enable unauthorized configuration changes or disruption of the application server.

**Illustrative risk rating**

| State | Likelihood | Impact | Score | Example band |
|---|---:|---:|---:|---|
| Inherent | 4 | 4 | 16 | High |
| Current | 3 | 4 | 12 | High |
| Target residual — forecast | 2 | 4 | 8 | Moderate |

These scores are illustrative. The target is a forecast and must not replace the current rating until corrective actions are verified.

**Recommendation:** Remove unjustified privileged memberships, document approved administrator roles, and validate privileged-authentication requirements.

| Action ID | Action | Owner | Target date | Verification |
|---|---|---|---|---|
| `ACT-EX-001` | Review and remove unapproved privileged access | Infrastructure security lead | `[Approved date]` | Updated membership export and approved access matrix |
| `ACT-EX-002` | Validate privileged-authentication controls | Identity and access management owner | `[Approved date]` | Configuration evidence and test results |

**Disposition:** Open — remediation and verification pending.

### 11.4 Finding `FIND-EX-002` — Inconsistent evidence of access reviews

**Observation:** The fictional evidence sample did not contain a complete, current record showing that all relevant privileged access had been reviewed by accountable owners.

**Expected condition:** Privileged-access reviews should be completed at the cadence required by approved policy, with exceptions and resulting actions tracked.

**Evidence:** `EVD-EX-003` — fictional access-review records sample.

**Risk implication:** Unnecessary or inappropriate access may persist if review coverage and follow-up are not demonstrated. The example does not assert that unauthorized access was exploited.

**Recommendation:** Define the review population, assign accountable reviewers, record decisions, track removals and exceptions, and retain verification evidence.

| Action ID | Action | Owner | Target date | Verification |
|---|---|---|---|---|
| `ACT-EX-003` | Establish a documented privileged-access review process | Application service owner | `[Approved date]` | Approved procedure and completed review record |
| `ACT-EX-004` | Track and verify review exceptions | Control owner | `[Approved date]` | Exception register and evidence of resolution |

**Disposition:** Open — process implementation and verification pending.

### 11.5 Illustrative consolidated action plan

| Action | Related finding | Owner | Priority | Status |
|---|---|---|---|---|
| Remove unjustified privileged access | `FIND-EX-001` | Infrastructure security lead | High, under fictional criteria | Planned |
| Validate privileged-authentication controls | `FIND-EX-001` | Identity and access management owner | High, under fictional criteria | Planned |
| Establish documented access reviews | `FIND-EX-002` | Application service owner | Moderate, under fictional criteria | Planned |
| Track review exceptions | `FIND-EX-002` | Control owner | Moderate, under fictional criteria | Planned |

Actual priorities and dates must be assigned using approved organizational criteria. The table does not constitute a formal acceptance of risk.

### 11.6 Illustrative closure requirements

The findings may be considered for closure only after the relevant actions are completed and verified, evidence references are recorded, current risk is reassessed, and required approvals are obtained. If the weakness remains or the evidence is insufficient, the finding remains open or is assigned an explicitly approved disposition.

### 11.7 Example evidence index

| Evidence ID | Description | Supports | Limitation |
|---|---|---|---|
| `EVD-EX-001` | Fictional administrative membership export | `FIND-EX-001` | Snapshot only |
| `EVD-EX-002` | Fictional access-approval sample | `FIND-EX-001` | Sample may not represent all accounts |
| `EVD-EX-003` | Fictional access-review records sample | `FIND-EX-002` | Limited to the stated sample |

All IDs above are placeholders for fictional evidence entries. A real report must reference evidence actually collected and validated within the authorized scope.

---

## 12. Document control and review

| Field | Value |
|---|---|
| Document | Cybersecurity Assessment Report Template |
| Version | 1.0 |
| Owner | `[Organization / function]` |
| Approval authority | `[Role / committee]` |
| Approval date | `[YYYY-MM-DD]` |
| Review date | `[YYYY-MM-DD]` |
| Classification | `[Organization-defined]` |
| Change history | `[Record approved changes]` |

### Final report release checklist

- [ ] All placeholders have been completed or intentionally marked not applicable.
- [ ] Scope and authorization match the work performed.
- [ ] Conclusions are supported by the available evidence.
- [ ] Material limitations and uncertainty are visible.
- [ ] Finding and risk identifiers are consistent across registers.
- [ ] Ratings use the approved model and are explained.
- [ ] Recommendations have owners, due dates, and verification criteria where applicable.
- [ ] Risk acceptance and exceptions have separate, valid decision records.
- [ ] Sensitive material is protected and distribution is authorized.
- [ ] Required quality review and approvals are complete.

