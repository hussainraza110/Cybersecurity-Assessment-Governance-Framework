# Evidence Handling

**Document type:** Assessment procedure  
**Status:** Template for organizational review and approval  
**Version:** 1.0  
**Last updated:** 2026-10-29  
**Owner:** To be assigned by the adopting organization  
**Approval authority:** To be defined by the adopting organization

> **Important use note:** This document provides a general procedure for handling evidence collected during authorized cybersecurity and governance assessments. The adopting organization must align it with applicable law, contractual and regulatory requirements, internal classification rules, retention schedules, incident-response procedures, and any legal hold or investigative requirements. It does not replace formal forensic procedures where those are required.

## 1. Purpose and Objectives

This document establishes a repeatable approach for planning, collecting, recording, validating, protecting, transferring, preserving, using, retaining, and disposing of assessment evidence.

The objectives are to:

- Ensure evidence is collected only with appropriate authorization and within the approved scope.
- Maintain sufficient provenance and metadata to understand where evidence came from and how it was handled.
- Protect confidentiality, integrity, and availability according to evidence sensitivity and risk.
- Support reliable findings through proportionate validation, corroboration, and documented limitations.
- Preserve traceability between evidence, findings, conclusions, and decisions.
- Escalate evidence that may require formal incident-response, legal, disciplinary, regulatory, or forensic handling.
- Apply approved retention and disposal rules without imposing universal retention periods.

The procedure applies to all assessment evidence, including technical artifacts, records, policies, interviews, observations, test results, screenshots, and management attestations.

## 2. Scope and Applicability

Use this procedure for evidence created, collected, received, analyzed, or referenced during authorized information-security risk assessments, technical assessments, control reviews, governance reviews, and related assurance activities.

Evidence may be digital, physical, documentary, observational, or testimonial. The handling method should fit the evidence type, purpose, sensitivity, reliability needs, and possible consequences of loss or alteration.

This procedure is not, by itself, a forensic acquisition standard. If evidence may be needed for legal proceedings, disciplinary action, a regulatory inquiry, or an incident investigation—or if tampering is suspected—consult the relevant authorized response, legal, and forensic functions and apply the required specialized process.

## 3. Principles and Definitions

### 3.1 Principles

1. **Authorization and scope:** Collect only evidence permitted by the documented authorization and assessment scope.
2. **Purpose limitation:** Collect what is necessary to answer the assessment question; avoid unnecessary data acquisition.
3. **Provenance:** Record the source, collector or provider, collection method, timing, and relevant context.
4. **Proportionate integrity:** Use integrity verification and preservation safeguards appropriate to risk, sensitivity, and evidentiary purpose.
5. **Least privilege:** Limit access, copying, transfer, and disclosure to authorized people with a legitimate need.
6. **Traceability:** Link evidence to findings and conclusions, and retain the history needed to explain material handling or interpretation decisions.
7. **Transparency:** Record limitations, assumptions, transformations, and gaps that may affect conclusions.
8. **Escalation:** Recognize when routine assessment handling is insufficient and specialist procedures are required.
9. **Controlled lifecycle:** Retain and dispose of evidence under approved schedules, legal holds, and authorized procedures.

### 3.2 Definitions

- **Evidence:** Information or an artifact used to support, challenge, or contextualize an assessment observation, finding, or conclusion.
- **Evidence item:** A uniquely identified item or logical collection of evidence managed as a unit.
- **Provenance:** Information describing an evidence item's origin, acquisition or receipt, and relevant handling history.
- **Integrity verification:** A check intended to provide confidence that evidence has not changed unexpectedly since a defined point.
- **Working copy:** A copy used for analysis, annotation, transformation, or reporting while an original or preserved source is retained where feasible and appropriate.
- **Chain of custody:** A documented history of possession, transfer, access, and handling used when accountability for evidence movement is required.
- **Sensitive evidence:** Evidence that requires restricted handling due to classification, personal information, credentials, secrets, security details, contractual constraints, or other confidentiality concerns.
- **Finding:** A documented assessment result, including an observed condition, supporting criteria, impact or risk implications, and relevant evidence.
- **Legal hold:** A direction to preserve relevant records or evidence because of actual or reasonably anticipated proceedings, investigation, or other formal requirement.

## 4. Roles and Responsibilities

Roles may be combined in small assessments, but accountability must remain clear.

| Role | Responsibilities |
|---|---|
| Assessment lead | Confirms the evidence plan fits the authorization and scope; resolves handling issues; ensures material limitations and escalations are addressed. |
| Evidence collector | Collects or receives evidence using approved methods; records provenance and metadata; protects evidence during collection and transfer. |
| Assessor or analyst | Validates relevance and reliability, records analytical steps and limitations, and links evidence to findings and conclusions. |
| Evidence custodian or repository owner | Maintains approved storage, access controls, transfer records where required, retention controls, and authorized disposal records. |
| Risk or control owner | Provides evidence and context, clarifies control operation, and responds to evidence gaps or findings. |
| Security, incident-response, legal, privacy, or forensic specialist | Advises or takes ownership when evidence requires specialist handling, a legal hold, incident investigation, or formal forensic process. |
| Approving authority | Approves exceptions, access, retention or disposal decisions, or other actions where required by organizational policy. |

The organization should define who can authorize collection, approve exceptions, initiate forensic escalation, place or release a legal hold, and authorize disposal.

## 5. Evidence Planning and Authorization

Before collection, the assessment team should define:

1. The assessment objective and questions the evidence is intended to address.
2. The approved scope, systems, records, locations, people, and time period.
3. The authorization basis and any restrictions, prohibited actions, or collection windows.
4. The evidence types expected and the least intrusive suitable collection method.
5. The sensitivity and potential impact of collecting, storing, or disclosing the evidence.
6. The repository, access permissions, transfer route, and retention requirements.
7. Any special conditions, including personal information, credentials, regulated records, third-party data, or potential forensic significance.
8. The person responsible for collection, custody, analysis, and follow-up.

Do not expand collection beyond the approved scope merely because additional data is accessible. If scope or authorization is unclear, pause the affected collection and obtain clarification through the authorized process.

Collection should be limited to what is reasonably necessary. Where feasible, use targeted queries, bounded time windows, redacted exports, or other minimization methods instead of copying entire datasets or systems.

## 6. Evidence Collection Methods

Choose the method according to the evidence type, purpose, sensitivity, and required confidence. Record enough information to explain how the evidence was obtained.

Examples include:

- **System and application logs:** Record source system, relevant time range, query or export method, timezone, filtering, and known gaps.
- **Configuration and command output:** Record target, tool or command, parameters, execution context, timestamp, and any transformations needed to interpret the output.
- **Vulnerability or control test results:** Record the test scope, tool and version where material, relevant settings, date, exclusions, and validation performed.
- **Policies, procedures, and records:** Record document title or identifier, version or effective date if available, source, retrieval date, and relevant section.
- **Interviews and attestations:** Record the participant's role, date, method, topic, and whether the record is a direct quotation, notes, or a summarized statement. Follow applicable consent and privacy rules.
- **Observations and physical evidence:** Record the observer, date and location at an appropriate level of detail, context, and any limitations. Photographs should be authorized and minimized.
- **Screenshots, photographs, and recordings:** Capture the relevant state and sufficient context to interpret it. Preserve timestamps or system context when material and available.
- **Exports and data extracts:** Record source, query or extraction method, filters, date range, field selection, row counts or other completeness checks where useful, and any redaction or transformation.

Use approved collection tools and methods. Do not perform intrusive actions, alter production data, bypass safeguards, or access unrelated information unless explicitly authorized and necessary for the assessment.

## 7. Evidence Register and Metadata

Assign each evidence item a stable, unique identifier. Maintain a register in an approved system or repository. The register should include, at minimum, the fields below as applicable.

| Field | Purpose |
|---|---|
| Evidence ID | Stable identifier used in notes, findings, reports, and transfer records. |
| Title and description | Concise explanation of what the item contains. |
| Evidence type | Log, configuration, document, screenshot, interview note, test output, observation, or other type. |
| Source | System, person, repository, document, service, or other origin. |
| Scope and relevance | Assessment objective, asset, process, or question to which the item relates. |
| Collector or provider | Person or process that collected or supplied the item. |
| Collection or receipt time | Date and time, including timezone where relevant; distinguish source timestamps from collection timestamps. |
| Method and context | Tool, version, command, query, parameters, procedure, and execution context where material. |
| Authorization reference | Relevant approval, work order, or assessment-scope reference. |
| Integrity details | Hash algorithm and value, verification time, comparison point, or reason integrity verification was not performed, where applicable. |
| Sensitivity and handling | Classification or sensitivity label, restrictions, and required safeguards. |
| Storage reference | Approved repository or location reference; avoid exposing secrets in the register itself. |
| Access and transfer history | Relevant access, recipient, transfer, or custody events when required by risk or evidentiary purpose. |
| Validation and limitations | Relevance, reliability, completeness, currency, corroboration, and known gaps. |
| Transformations | Redaction, filtering, parsing, normalization, conversion, or other processing, with references to the source and resulting derivative. |
| Linked findings | Finding IDs, conclusions, or decisions supported or challenged by the evidence. |
| Retention and disposition | Applicable schedule or hold reference and any authorized disposal record. |

The organization may use a tiered register, provided core provenance is recorded for all items and additional fields are captured when sensitivity, risk, or evidentiary purpose requires them.

## 8. Validation and Corroboration

Validation should be proportionate to the significance of the conclusion, sensitivity of the evidence, and consequences of error. Assess the following where relevant:

- **Relevance:** Does the evidence address the stated assessment question or scenario?
- **Source reliability:** Is the source identifiable, appropriate, and sufficiently trustworthy for the claim?
- **Authenticity and integrity:** Is there a reasonable basis to trust that the item came from the stated source and has not changed unexpectedly?
- **Completeness:** Are there missing periods, records, fields, pages, systems, or contextual details that could alter interpretation?
- **Currency:** Does the evidence reflect the period and configuration relevant to the conclusion?
- **Consistency:** Does it agree with other evidence, or are there conflicts that require explanation?
- **Reproducibility:** Can a reviewer understand the method and, where practical, repeat the analysis?
- **Limitations:** Are there collection constraints, assumptions, biases, or transformations that affect reliability?

Corroborate material claims where practical, particularly where a single source is incomplete, self-reported, ambiguous, or consequential. Corroboration does not always require a second identical artifact; it may involve a separate source or independent observation.

Do not treat a lack of evidence as proof that a control or event does not exist. Record what was examined, what was not available, and the limits of the conclusion.

## 9. Integrity Verification and Preservation

### 9.1 Proportionate integrity controls

Apply integrity verification according to the evidence's sensitivity, risk, technical nature, and likely use.

Examples of proportionate controls include:

- Recording source, collector, time, method, and storage reference for all evidence.
- Calculating a cryptographic hash for digital artifacts when it materially helps detect later changes or establish a comparison point.
- Rechecking a hash after transfer or before analysis where integrity assurance is needed.
- Retaining original exports and using separate working copies for analysis where feasible.
- Using access-controlled repositories, versioning, audit logs, write protection, or immutable storage where justified.
- Recording why a hash or stronger preservation measure was not used when it would ordinarily be expected for the evidence's purpose.

A hash demonstrates consistency with a particular reference value; by itself, it does not prove that evidence was authentic at collection, that the collection method was correct, or that the source was complete.

### 9.2 Originals and working copies

Preserve original evidence where feasible and appropriate. Create working copies for analysis, redaction, parsing, annotation, or reporting where doing so reduces risk of altering the preserved source.

Keep derivatives linked to their source items. Record material transformations and maintain enough information to explain how the derivative was produced. If the original cannot be retained, document why, who authorized the approach, what safeguards were used, and what limitations result.

Not every routine assessment item requires immutable storage or forensic imaging. Stronger preservation measures should be used when the evidence's purpose or risk warrants them.

## 10. Chain of Custody and Transfer

### 10.1 When formal chain of custody is appropriate

Use a formal chain-of-custody record when evidence may support legal, disciplinary, regulatory, or forensic proceedings; when tampering is suspected; or when the evidence's significance makes detailed accountability for possession and transfer necessary.

The record should identify the item, person releasing it, person receiving it, date and time, purpose, transfer method, condition or integrity check, and any relevant exception. Apply the organization's approved forms and specialist procedures where available.

For routine assessment evidence that does not require formal chain of custody, maintain provenance and access or transfer history proportionate to sensitivity and risk.

### 10.2 Secure transfer

Use approved secure channels and repositories. Before transfer:

1. Confirm the recipient is authorized and has a legitimate need.
2. Confirm the transfer is permitted by scope, classification, and applicable rules.
3. Minimize the data being transferred.
4. Use approved encryption or other protective measures where required.
5. Verify receipt and integrity when warranted.
6. Record the transfer and any custody event required by the evidence's purpose.
7. Address failed transfers, unexpected recipients, or suspected exposure through the relevant incident process.

Avoid transmitting sensitive evidence through unapproved personal email, public file-sharing services, unmanaged removable media, or other channels that do not meet organizational requirements.

## 11. Sensitive Information, Secrets, and Redaction

Evidence may contain credentials, access tokens, private keys, personal information, confidential business data, network diagrams, security configurations, or other sensitive material.

Apply the organization's classification and handling rules. At minimum:

- Collect only what is necessary for the assessment.
- Restrict access to authorized personnel with a legitimate need.
- Store evidence in approved, access-controlled locations.
- Avoid placing credentials, tokens, private keys, or other secrets in filenames, general-purpose logs, finding descriptions, or report text.
- Redact secrets and unrelated personal or confidential information from report copies when they are not needed to substantiate the conclusion.
- Preserve an unredacted original in a restricted location where retention is authorized and the original is necessary.
- Record that a report copy was redacted and maintain a link to its source item without exposing the sensitive value.
- Do not include more personal or confidential information in screenshots, reports, or evidence bundles than necessary.
- Escalate suspected exposure of credentials, personal information, or other sensitive data through the applicable incident-response or privacy process.

Redaction must be effective for the output format. For example, visually covering text in a document or image may leave the underlying content recoverable. Validate redacted copies before release.

## 12. Screenshots, Images, and Screen Recordings

Capture only the information necessary to demonstrate the observation. Where material and available, preserve contextual details such as the relevant application or system, state, date and time, and steps leading to the observation.

For report use:

- Prefer a redacted derivative when unrelated secrets, personal information, or confidential details are visible.
- Preserve the original separately where necessary and authorized.
- Keep the derivative linked to the original evidence ID.
- Record material edits, crops, annotations, redactions, or conversions.
- Avoid edits that change the meaning of the evidence or remove context needed to interpret it.
- Distinguish an explanatory annotation from the original captured content.
- Follow authorization and privacy rules before recording screens, people, or third-party information.

If an image or recording may be evidentiary in a formal investigation, consult the authorized forensic or legal process before modifying or handling it in ways that could affect its evidentiary value.

## 13. Reproducibility and Analytical Processing

Record material collection and analysis details needed for a competent reviewer to understand the result. Depending on the evidence, these may include:

- Tool or application name and version.
- Commands, queries, scripts, parameters, and relevant configuration.
- Execution date and time, timezone, operator, and target scope.
- Filters, exclusions, and data ranges.
- Parsing, normalization, decoding, redaction, or conversion steps.
- Known tool limitations, errors, or incomplete results.
- Validation checks, repeat runs, or independent comparisons where performed.

Do not require scripts or exact execution logs for every evidence item. The level of detail should be sufficient for the significance of the conclusion and the need for repeatability. Avoid recording secrets or unnecessary sensitive values in execution logs.

When a transformation is material, preserve the original where feasible and authorized, identify the resulting derivative, and document the relationship between them.

## 14. Evidence Gaps, Exceptions, and Escalation

When evidence is missing, unreliable, inaccessible, incomplete, stale, or not collected, document:

- What evidence was expected or needed.
- What was unavailable or unreliable and why, if known.
- The effect on the assessment question, finding, score, or conclusion.
- Any alternative or corroborating evidence considered.
- The residual uncertainty and limitations.
- The owner and follow-up action, if applicable.
- Whether the issue requires escalation or a revised assessment plan.

Do not conceal a material evidence gap or infer that an unverified control is effective. A finding may remain provisional or be qualified where evidence is insufficient.

### 14.1 Forensic or incident escalation

Escalate through the authorized incident-response, legal, privacy, disciplinary, regulatory, or forensic process when:

- Evidence may relate to an active or suspected security incident.
- Tampering, deletion, or unauthorized alteration is suspected.
- Evidence may be used in legal, disciplinary, regulatory, or formal investigative proceedings.
- Collection or analysis could alter relevant evidence.
- A legal hold or specialist preservation requirement may apply.
- The assessment team lacks the authority, expertise, or tools needed to preserve the evidence appropriately.

Where appropriate, pause actions that could alter relevant evidence until the authorized specialist provides direction. Do not independently conduct invasive forensic acquisition outside the approved scope or authority.

Record the escalation, recipient, time, instructions received, transfer of responsibility, and any impact on the assessment.

## 15. Evidence-to-Finding Traceability and Reporting

Maintain bidirectional traceability:

- Each finding or conclusion should reference the evidence items that support, qualify, or challenge it.
- Each evidence item should identify the findings, conclusions, or decisions for which it was used, where applicable.

A finding should clearly distinguish observed facts, applicable criteria, analysis, risk implications, assumptions, and limitations. Do not state an inference as a directly observed fact.

When evidence conflicts, document the conflict, the evaluation performed, and why one interpretation was preferred or why the conclusion remains uncertain.

Reports should include enough evidence references and context to make findings reviewable without unnecessarily reproducing sensitive source material. Place detailed or sensitive artifacts in an appropriately restricted evidence repository and use controlled references in broader reports.

Before releasing a report or evidence package, verify that:
- Recipients are authorized.
- Sensitive details have been minimized or redacted as appropriate.
- Redactions are effective and do not misrepresent the evidence.
- Evidence references resolve to the intended items.
- Material limitations and assumptions are disclosed.
- Any required review or approval has occurred.

## 16. Storage, Access, Retention, and Disposal

### 16.1 Storage and access

Store evidence in approved repositories that meet organizational requirements for classification, confidentiality, integrity, availability, backup, and auditability as appropriate.

Apply least-privilege access. Review access when roles change, the assessment ends, or a special access need expires. Avoid uncontrolled local copies and unmanaged removable media. Protect repository indexes and metadata as well as the evidence itself, because metadata may reveal sensitive systems, people, or findings.

### 16.2 Retention

Follow applicable legal, regulatory, contractual, investigative, and organizational retention schedules. This document does not establish a universal retention period.

Before deleting or disposing of evidence, verify whether:
- A legal hold, incident investigation, audit, or other preservation requirement applies.
- The assessment or finding remains open.
- The evidence is subject to a contract, regulation, or approved retention schedule.
- The appropriate authority has approved the action under organizational procedures.

If requirements conflict or are unclear, pause disposal and consult the designated records, legal, compliance, privacy, or investigation authority.

### 16.3 Authorized disposal

Dispose of evidence only through approved procedures and with required authorization. Use a method appropriate to the storage medium, sensitivity, and organizational requirements. Where warranted, record the evidence IDs, disposition date, method, authorizer, responsible person, and any exceptions.

Ensure that disposal addresses controlled copies and derivatives to the extent required by policy and applicable obligations. Do not destroy evidence subject to a legal hold or other preservation direction.

## 17. Quality Assurance and Review

Review effort should be proportionate to the significance of the evidence, the risk of error, sensitivity, and potential consequences.

Quality checks may include:
- Confirming authorization and scope.
- Checking required metadata and stable identifiers.
- Verifying integrity where required.
- Reviewing source reliability, completeness, currency, and relevance.
- Checking material analytical steps and transformations.
- Confirming finding-to-evidence and evidence-to-finding links.
- Checking access, transfer, and custody records where required.
- Reviewing redactions and report disclosure.
- Confirming gaps, exceptions, and escalations are documented.
- Confirming retention and disposal requirements are identified.

Where independent review is warranted but unavailable, document the limitation and any compensating review. Do not imply that a review occurred when it did not.

## 18. Practical Templates and Checklists

The following reusable structures may be implemented in a spreadsheet, ticketing system, evidence repository, or assessment platform.

### 18.1 Evidence register template

| Evidence ID | Title / Type | Source | Collector / Provider | Collected / Received (with timezone) | Method / Authorization | Sensitivity | Integrity Reference | Storage Reference | Validation / Limitations | Linked Findings | Retention / Disposition |
|---|---|---|---|---|---|---|---|---|---|---|---|
| E-001 | Example: configuration export | Example system | Assessor role | YYYY-MM-DD HH:MM TZ | Approved export; authorization ID | Organization-defined | Hash or N/A with rationale | Restricted repository reference | Scope and completeness checked; limitations noted | F-001 | Schedule / hold reference |

The example row is illustrative only. Do not use it as a real record.

### 18.2 Collection checklist

- [ ] Assessment objective and collection question documented.
- [ ] Authorization and scope confirmed.
- [ ] Source, target, time range, and method identified.
- [ ] Collection minimized to necessary information.
- [ ] Sensitivity and handling requirements identified.
- [ ] Approved destination and access permissions confirmed.
- [ ] Collector, date/time, timezone, and method recorded.
- [ ] Relevant tools, versions, commands, queries, and parameters recorded.
- [ ] Integrity verification performed where appropriate, or reason for omission recorded.
- [ ] Evidence ID assigned and register updated.
- [ ] Evidence linked to relevant findings or follow-up questions.
- [ ] Special handling or escalation needs considered.

### 18.3 Transfer and custody record template

| Field | Record |
|---|---|
| Evidence ID(s) | Stable IDs |
| Transfer purpose | Why the transfer is required |
| Released by / received by | Names or approved role identifiers |
| Date and time | Include timezone |
| Approved transfer method | Approved channel or repository |
| Integrity check | Method, result, or reason not applicable |
| Condition or exception | Relevant observations or issues |
| Authorization / case reference | Applicable approval, investigation, or hold reference |
| Acknowledgment | Required confirmation under organizational procedure |

Use this formal record when the evidence's risk or purpose requires it. Routine evidence may use a lighter documented transfer history where appropriate.

### 18.4 Evidence-gap record template

| Field | Record |
|---|---|
| Evidence ID or expected item | Identifier or description |
| Gap or limitation | What is missing, incomplete, or unreliable |
| Reason | Known cause, or “unknown” |
| Assessment impact | Effect on finding, score, or conclusion |
| Alternative evidence | Corroborating source or “none available” |
| Confidence and assumptions | Remaining uncertainty |
| Follow-up owner and action | Responsible person and next step |
| Escalation | Whether escalated, to whom, and when |
| Review date | Organization-defined target |

### 18.5 Evidence release checklist

- [ ] Recipient and purpose authorized.
- [ ] Scope and disclosure restrictions checked.
- [ ] Unnecessary sensitive data removed from the release copy.
- [ ] Redactions tested for effectiveness.
- [ ] Source item preserved where required.
- [ ] Evidence references and linked findings checked.
- [ ] Transfer method approved and suitable for sensitivity.
- [ ] Required approval, transfer record, or acknowledgment completed.

## 19. Limitations and Organizational Customization

Evidence handling depends on the assessment purpose, applicable obligations, evidence type, technology, and organizational environment. No single procedure can guarantee authenticity, completeness, or admissibility in every context.

The adopting organization must define or reference:
- Authorization and scope approval.
- Classification and handling rules.
- Approved repositories, transfer channels, and access-control requirements.
- Retention schedules, legal-hold procedures, and disposal authority.
- Incident-response and forensic escalation paths.
- Requirements for personal information, regulated records, and third-party data.
- Chain-of-custody forms and specialist procedures where needed.
- Review, exception, and approval responsibilities.

This document does not replace applicable law, regulatory or contractual requirements, legal advice, incident-response plans, or specialist forensic standards. It does not guarantee that evidence will be admissible in proceedings.

## 20. Related Documents and References

### 20.1 Related project documents

- `assessment-lifecycle.md` — assessment phases, authorization, stage gates, responsibilities, and closure.
- `risk-assessment-methodology.md` — risk assessment process, evidence use, and risk-register requirements.
- `risk-scoring-model.md` — likelihood, impact, scoring, rating, and uncertainty treatment.
- `references/standards-and-frameworks.md` — project reference register, when available in the repository.

Check repository paths when companion documents are added or renamed.

### 20.2 Reference frameworks and standards

The following may inform evidence handling, assessment, records management, or incident response. Verify current editions and applicability before use:

- **NIST SP 800-86** — guidance on integrating forensic techniques into incident response.
- **NIST SP 800-101 Rev. 1** — guidelines for mobile device forensics, where applicable.
- **NIST SP 800-72** — guidelines on evidence collection and archiving, where applicable; verify current status and relevance.
- **NIST SP 800-61 Rev. 3** — incident response recommendations integrated with cybersecurity risk management.
- **NIST SP 800-115** — technical information-security testing and assessment guidance.
- **ISO/IEC 27001 and ISO/IEC 27002** — information-security management and controls.
- **ISO/IEC 27037** — identification, collection, acquisition, and preservation of digital evidence.
- **ISO/IEC 27041, ISO/IEC 27042, and ISO/IEC 27043** — guidance relevant to assurance of digital-evidence methods, analysis and interpretation, and incident investigation principles.

These references are context, not a declaration of compliance. Confirm current editions, status, and organizational applicability before citing them in formal procedures.

## 21. Document Control

| Field | Value |
|---|---|
| Document title | Evidence Handling |
| File | `docs/methodology/evidence-handling.md` |
| Version | 1.0 |
| Status | Template for organizational review and approval |
| Document owner | To be assigned by the adopting organization |
| Approval authority | To be defined by the adopting organization |
| Effective date | To be set on approval |
| Review cycle | To be defined by the adopting organization |
| Change history | Record revisions, rationale, approver, and effective date |

**Implementation condition:** Before operational use, the adopting organization must approve the applicable authorization workflow, classification and access rules, retention and disposal schedule, forensic escalation path, and any mandatory chain-of-custody requirements.
