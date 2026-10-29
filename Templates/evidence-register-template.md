# Evidence Register Template

**Document type:** Operational template  
**Template ID:** `TPL-EVD-001`  
**Version:** 1.0  
**Status:** Draft for organizational adaptation  
**Owner:** `[Document owner / function]`  
**Approved by:** `[Approver / authority]`  
**Effective date:** `[YYYY-MM-DD]`  
**Review date:** `[YYYY-MM-DD]`  
**Classification:** `[Organization-defined classification]`

> **Use note:** Adapt this template to approved organizational policies, assessment authorization, applicable law, contractual requirements, retention schedules, and the sensitivity of the evidence. This template does not itself grant authorization to collect, access, transfer, retain, or dispose of evidence. Do not place secrets, credentials, personal data, or raw sensitive evidence in a general-purpose register when a controlled evidence repository is available.

## 1. Purpose and use

Use this template to identify, track, validate, protect, reference, retain, and dispose of evidence collected during an authorized cybersecurity or governance assessment. It supports technical assessments, control reviews, risk assessments, audits, incident-related reviews, and other approved engagements.

The register provides:

1. An assessment-wide summary index.
2. A detailed record for each evidence item.
3. Validation and evidence-gap tracking.
4. Conditional transfer and chain-of-custody records.
5. Retention and disposal tracking.
6. Quality checks and traceability to checks, findings, risks, and decisions.

The register complements the evidence-handling procedure at `../docs/methodology/evidence-handling.md`. It does not replace the assessment lifecycle, risk assessment methodology, risk scoring model, or any mandatory forensic or legal procedure.

## 2. Operating instructions

### 2.1 Assign and maintain evidence identifiers

- Assign each evidence item a unique identifier, for example `EVD-001`.
- Do not reuse an identifier for an unrelated item, including after retirement or disposal.
- Assign separate identifiers to materially different artifacts. Use parent/child or related-item references when an export, working copy, redacted copy, or derived artifact must be traced to an original.
- Keep identifiers stable across the register, evidence repository, assessment checklist, report, risk register, and supporting records.
- Record the assessment ID and, where applicable, the collection authorization or scope reference.
- Identify the authoritative register and its custodian. Restrict edits to authorized roles and retain change history where required.

### 2.2 Separate metadata from evidence contents

The register should point to an approved storage reference rather than embed raw evidence. Avoid placing passwords, tokens, private keys, personal data, or unnecessary sensitive details in titles, descriptions, filenames, or free-text fields. Store sensitive artifacts in approved repositories with appropriate access controls.

### 2.3 Use controlled values consistently

Organizations should define approved classifications, roles, validation criteria, status values, retention schedules, and approval authorities. Suggested values in this template are starting points, not mandatory universal values. Record the rationale for deviations or exceptions.

### 2.4 Record timestamps precisely

Use a consistent date/time format. Include the time zone or UTC offset where timing is material, particularly for logs, event timelines, cross-system comparisons, transfers, and forensic work. Record clock source or known clock skew when it affects interpretation.

## 3. Assessment-wide evidence summary register

Use one row per evidence item. Keep sensitive content out of this table and use controlled storage references.

| Evidence ID | Assessment ID | Title / description | Evidence type | Source / asset ID | Collector | Collection date/time | Related check(s) | Finding / risk reference(s) | Validation status | Integrity status | Classification | Storage reference | Lifecycle status | Gap / exception ID |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `EVD-001` | `[ASSESS-###]` | `[Concise description]` | `[Log / config / screenshot / document / test result / other]` | `[Source / asset]` | `[Role / identifier]` | `[Timestamp + time zone]` | `[CHECK-###]` | `[FIND-### / RISK-### / N/A]` | `[Pending / validated / partial / rejected]` | `[Not assessed / verified / exception / N/A + rationale]` | `[Classification]` | `[Approved repository reference]` | `[Lifecycle state]` | `[GAP-### / EXC-### / None]` |
| `[EVD-###]` | `[ASSESS-###]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` |

### 3.1 Suggested evidence types

Select a locally approved value or document the type used:

- System or application log
- Configuration export
- Command output or diagnostic result
- Screenshot or screen recording
- File or document
- Network or protocol capture
- Scan or test result
- Interview or observation note
- Control record or approval artifact
- Forensic image or acquisition
- Other — specify

### 3.2 Suggested validation statuses

- **Pending:** Validation has not been completed.
- **Validated:** Required checks were completed with an acceptable outcome for the stated purpose.
- **Partially validated:** Some checks passed, but material limitations remain.
- **Rejected:** The item is unsuitable for the stated purpose; document why.
- **Not required:** Validation was not required under the approved procedure; record the rationale.
- **Blocked:** Validation could not be completed; link to a gap or exception record.

### 3.3 Suggested integrity statuses

- **Not assessed:** Integrity checks have not been performed.
- **Verified:** The selected integrity checks passed within their stated scope.
- **Exception:** A discrepancy or material limitation remains.
- **Not applicable:** Integrity verification is not suitable or material for this item; record the rationale.

Do not label evidence “verified” without identifying what was checked, against which reference, when, and with what result.

## 4. Detailed evidence record

Copy this section for each evidence item. Complete fields relevant to the evidence type and intended use; mark genuinely inapplicable fields as `N/A` with a brief rationale where material.

### 4.1 Identification and authorization

| Field | Record |
|---|---|
| Evidence ID | `[EVD-###]` |
| Assessment ID / name | `[ASSESS-### / name]` |
| Evidence title | `[Short, non-sensitive title]` |
| Evidence type | `[Type]` |
| Record version / status | `[Version / current, superseded, retired]` |
| Collection authorization reference | `[Authorization / scope / work order]` |
| Authorized asset / source | `[Asset ID, system, repository, or source role]` |
| Collection purpose | `[Question, control, test, or claim this item is intended to support]` |
| Related checklist / test IDs | `[CHECK-### / TEST-###]` |
| Related control IDs | `[Control references]` |
| Related finding / risk IDs | `[FIND-### / RISK-###]` |
| Evidence owner | `[Role / function]` |
| Evidence custodian | `[Role / function]` |
| Classification | `[Organization-defined classification]` |
| Access restrictions | `[Authorized roles / group / restrictions]` |

### 4.2 Provenance and collection

| Field | Record |
|---|---|
| Source description | `[System, device, person/role, document, repository, or other source]` |
| Source asset / identity | `[Asset ID or controlled source reference]` |
| Original source location | `[Approved source reference; avoid embedding secrets]` |
| Collector | `[Role / identifier]` |
| Collection date/time | `[Timestamp + time zone]` |
| Collection method | `[Procedure / tool / export method]` |
| Tool name and version | `[If applicable]` |
| Commands / query / parameters | `[Material details; sanitize secrets]` |
| Relevant environment / version | `[OS, application, firmware, configuration, or other context]` |
| Collection window / time range | `[Start/end, time zone, or N/A]` |
| Clock source / known skew | `[If timing is material]` |
| Original or derived item | `[Original / working copy / export / redacted copy / derived artifact]` |
| Parent / related evidence IDs | `[EVD-### references]` |
| Transformations performed | `[Parsing, filtering, conversion, redaction, extraction, or none]` |
| Deviations from procedure | `[Description, approval, or None]` |
| Collection limitations | `[Known constraints, exclusions, or None]` |

### 4.3 Storage and handling

| Field | Record |
|---|---|
| Approved storage reference | `[Repository ID / controlled path]` |
| Storage system / custodian | `[System and responsible role]` |
| Storage protection | `[Access control, encryption, immutability, or other applicable controls]` |
| Access group / authorized roles | `[Controlled roles or group reference]` |
| Working-copy location | `[Reference or N/A]` |
| Transfer restrictions | `[Restrictions and approved method]` |
| Redaction / sanitization requirement | `[Requirement and report-copy reference]` |
| Handling exceptions | `[Exception ID / None]` |
| Last access / review record | `[Audit reference, where available and required]` |

Do not expose restricted repository paths or sensitive metadata in public reports. Record an approved reference that authorized personnel can resolve.

### 4.4 Integrity verification

Select verification methods proportionate to the evidence type, consequence of misuse, sensitivity, and applicable requirements.

| Field | Record |
|---|---|
| Verification required? | `[Yes / No / Conditional]` |
| Rationale and criteria | `[Why this level of verification is appropriate]` |
| Method | `[Cryptographic hash / source validation / corroboration / signature / comparison / other]` |
| Hash algorithm | `[e.g., SHA-256, where applicable]` |
| Hash value | `[Value or protected record reference; N/A with rationale if unsuitable]` |
| Hash calculated at | `[Timestamp + time zone]` |
| Calculated by | `[Role / identifier]` |
| Comparison reference | `[Original, acquisition log, transfer record, or other reference]` |
| Verification result | `[Passed / exception / not performed / N/A]` |
| Source authenticity checks | `[Checks and results]` |
| Corroborating evidence IDs | `[EVD-### references]` |
| Discrepancies / anomalies | `[Details or None]` |
| Integrity exception ID | `[EXC-### / None]` |

**Interpretation safeguard:** A matching hash supports a conclusion that the compared byte sequences match. It does not, by itself, establish source authenticity, authorized collection, completeness, correct interpretation, or truth of the underlying content. Hashes are not mandatory for every evidence type; record a reasoned decision.

### 4.5 Validation and suitability for use

| Field | Record |
|---|---|
| Claim / proposition being evaluated | `[Specific claim the evidence may support]` |
| Validation objective | `[What must be established]` |
| Validation procedure / criteria | `[Procedure reference and acceptance criteria]` |
| Provenance checks | `[Checks and results]` |
| Completeness / relevance | `[Assessment]` |
| Context and time validity | `[Assessment where material]` |
| Corroboration performed | `[Other evidence and results]` |
| Contradictory evidence | `[References and explanation / None identified]` |
| Validation outcome | `[Validated / partially validated / rejected / blocked / not required]` |
| Confidence / uncertainty | `[Assessment and rationale; keep separate from risk rating]` |
| Limitations | `[What cannot safely be inferred]` |
| Validator | `[Role / identifier]` |
| Validation date | `[YYYY-MM-DD]` |
| Independent review required? | `[Yes / No + rationale]` |
| Reviewer / review date | `[Role / date / N/A]` |
| Approved for stated use? | `[Yes / Conditional / No / Pending]` |
| Conditions on use | `[Scope, caveats, redactions, or None]` |
| Gap / exception references | `[GAP-### / EXC-### / None]` |

### 4.6 Chain-of-custody decision

| Field | Record |
|---|---|
| Formal custody tracking required? | `[Yes / No]` |
| Reason | `[Legal / forensic / disciplinary / regulatory / suspected tampering / policy / other]` |
| Decision maker / role | `[Role]` |
| Decision date | `[YYYY-MM-DD]` |
| Applicable requirement / policy | `[Reference or N/A]` |
| Custody record ID | `[CUST-### / N/A]` |
| Rationale if not required | `[Why routine tracking is proportionate for this item]` |

Formal chain-of-custody tracking is conditional unless applicable requirements or material integrity concerns demand it. If the decision changes, update the record and create or link the appropriate custody record.

### 4.7 Retention and disposal

| Field | Record |
|---|---|
| Retention schedule / rule | `[Policy or schedule reference]` |
| Retention trigger / start date | `[Event / date / N/A]` |
| Review or disposal eligibility date | `[Date / event]` |
| Legal hold / preservation restriction | `[Yes / No / Unknown + reference]` |
| Hold owner / authority | `[Role / reference]` |
| Disposal approval required from | `[Authorized role]` |
| Disposal status | `[Not eligible / due for review / on hold / authorized / completed]` |
| Disposal method | `[Approved method when authorized]` |
| Disposal date | `[Timestamp + time zone / pending]` |
| Disposal performer | `[Role / service]` |
| Completion evidence | `[Certificate / audit event / record reference]` |
| Copies / replicas / derivatives considered | `[Locations and actions]` |
| Exception / deferred action | `[Reason and owner / None]` |

Do not set a universal retention duration in this template. Follow the applicable schedule, legal and contractual obligations, preservation requirements, and organizational approval process. A legal hold or other preservation restriction takes precedence over routine disposal eligibility.

### 4.8 Lifecycle history and changes

| Date/time + zone | Event / field changed | Previous value | New value | Person / role | Reason / approval / ticket |
|---|---|---|---|---|---|
| `[Timestamp]` | `[Created / updated / validated / transferred / restricted / disposed]` | `[Value / N/A]` | `[Value]` | `[Role]` | `[Reason / reference]` |
| `[Timestamp]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` | `[Enter]` |

Retain history in the register or the approved system of record where auditability is required. Do not silently overwrite material validation, integrity, custody, or disposal decisions.

## 5. Supporting record: evidence-gap register

Create a gap record when evidence is missing, incomplete, unavailable, contradictory, stale, or insufficient for the intended conclusion.

| Field | Record |
|---|---|
| Gap ID | `[GAP-###]` |
| Assessment ID | `[ASSESS-###]` |
| Related evidence IDs | `[EVD-### references / None]` |
| Related check / finding / risk | `[CHECK-### / FIND-### / RISK-###]` |
| Gap type | `[Missing / incomplete / unavailable / contradictory / stale / insufficient / other]` |
| Description | `[What is missing or unreliable]` |
| Reason | `[Known reason / Unknown]` |
| Effect on conclusion | `[How the gap affects the finding or risk assessment]` |
| Confidence / uncertainty impact | `[Explanation; do not silently imply certainty]` |
| Alternative sources / validation considered | `[Methods and outcomes]` |
| Required follow-up | `[Collection, corroboration, escalation, or other action]` |
| Owner | `[Role]` |
| Target date | `[Organization-approved date]` |
| Status | `[Open / in progress / resolved / accepted limitation / closed]` |
| Acceptance authority / reference | `[If a limitation is formally accepted]` |
| Closure evidence | `[EVD-### / record reference]` |
| Reviewer / closure date | `[Role / date]` |

### Evidence-gap handling checklist

- [ ] The gap is described specifically.
- [ ] Affected checks, findings, risks, and evidence are linked.
- [ ] The effect on the assessment conclusion is documented.
- [ ] Alternative evidence or validation approaches were considered where proportionate.
- [ ] Follow-up has an owner and target date, or the limitation has been formally accepted by an authorized role.
- [ ] Resolution or acceptance is supported by a record.

## 6. Supporting record: validation record

Use this record when validation needs a distinct audit trail or multiple validation activities occur for one evidence item.

| Field | Record |
|---|---|
| Validation record ID | `[VAL-###]` |
| Evidence ID | `[EVD-###]` |
| Validation objective / claim | `[Claim being evaluated]` |
| Procedure / criteria | `[Reference and acceptance criteria]` |
| Reviewer / validator | `[Role / identifier]` |
| Date/time | `[Timestamp + time zone where material]` |
| Source / provenance checks | `[Procedure and results]` |
| Integrity checks | `[Method, comparison reference, result, or rationale for omission]` |
| Completeness / relevance checks | `[Results]` |
| Corroborating evidence | `[EVD-### references]` |
| Conflicts / anomalies | `[Details / None]` |
| Outcome | `[Validated / partially validated / rejected / blocked / not required]` |
| Confidence / uncertainty | `[Rationale]` |
| Limitations | `[What remains unproven]` |
| Follow-up / gap ID | `[Action / GAP-### / None]` |
| Independent reviewer | `[Role / N/A + rationale]` |
| Approval for use | `[Yes / Conditional / No / Pending]` |
| Review / approval date | `[Date]` |

### Validation decision guide

- **Validated:** The evidence meets documented criteria for the stated claim and scope; limitations remain documented.
- **Partially validated:** Some criteria are met, but one or more material uncertainties remain.
- **Rejected:** A material defect makes the item unsuitable for the intended claim.
- **Blocked:** Validation could not be completed because a dependency, authorization, or source was unavailable.
- **Not required:** The approved process explicitly permits omission, and the reason is recorded.

## 7. Supporting record: transfer and chain of custody

Use this record when formal custody tracking is required by policy, law, engagement conditions, forensic needs, or material integrity concerns.

| Field | Record |
|---|---|
| Custody record ID | `[CUST-###]` |
| Evidence ID(s) | `[EVD-### references]` |
| Assessment / case reference | `[ASSESS-### / case ID]` |
| Reason custody tracking is required | `[Legal / forensic / disciplinary / regulatory / suspected tampering / policy / other]` |
| Authorization reference | `[Approved authority / case reference]` |
| Releasing custodian | `[Role / controlled identifier]` |
| Receiving custodian | `[Role / controlled identifier]` |
| Transfer date/time + zone | `[Timestamp]` |
| Source location | `[Approved reference]` |
| Destination location | `[Approved reference]` |
| Transfer purpose | `[Reason]` |
| Transfer method | `[Approved secure method]` |
| Item condition / packaging | `[Condition and seal reference, if applicable]` |
| Integrity verification | `[Method, reference, and result where appropriate]` |
| Transfer acknowledgement | `[Approved acknowledgement mechanism / reference]` |
| Discrepancy / exception | `[Details / None]` |
| Escalation / incident reference | `[Reference / N/A]` |
| Releasing / receiving confirmation | `[Record references and timestamps]` |
| Reviewer / approval | `[Role / date, if required]` |

### Custody event log

Record each handover as a separate event; do not overwrite previous events.

| Event ID | Evidence ID(s) | From custodian | To custodian | Date/time + zone | Purpose | Source → destination | Integrity / condition check | Acknowledgement reference | Exception |
|---|---|---|---|---|---|---|---|---|---|
| `[CUST-EVT-###]` | `[EVD-###]` | `[Role]` | `[Role]` | `[Timestamp]` | `[Purpose]` | `[Locations]` | `[Result]` | `[Reference]` | `[None / EXC-###]` |

## 8. Supporting checklist: evidence release and quality review

Complete before evidence is used to support a material finding, risk conclusion, formal report, or external decision. Tailor the checklist to the assessment and applicable requirements.

- [ ] Collection was within approved authorization and scope.
- [ ] Source, collector, collection method, and relevant time context are documented.
- [ ] The evidence is relevant to the specific claim being made.
- [ ] The evidence is sufficiently complete for its intended use, or limitations are explicit.
- [ ] Integrity checks were selected and performed where appropriate.
- [ ] Provenance and source authenticity were considered.
- [ ] Material claims were corroborated proportionately.
- [ ] Conflicting results, anomalies, and evidence gaps are documented.
- [ ] Confidence and uncertainty are stated separately from the risk rating.
- [ ] Sensitive content is protected; report copies are appropriately sanitized or redacted.
- [ ] Evidence is traceable to checks, findings, risks, and decisions.
- [ ] Required validation and independent review are recorded.
- [ ] Any conditional chain-of-custody requirements have been evaluated and fulfilled.
- [ ] Use restrictions and limitations are visible to the report author and reviewer.

| Review field | Record |
|---|---|
| Evidence ID(s) | `[EVD-### references]` |
| Intended use | `[Finding / report / decision]` |
| Reviewer | `[Role / identifier]` |
| Review date | `[YYYY-MM-DD]` |
| Decision | `[Approved / approved with limitations / rejected / pending]` |
| Conditions / limitations | `[Details]` |
| Follow-up / exception | `[GAP-### / EXC-### / None]` |

## 9. Supporting checklist: retention and disposal

Before disposing of evidence, verify and record the following.

- [ ] The applicable retention schedule and obligations have been reviewed.
- [ ] No legal hold, investigation, incident response, or preservation requirement prevents disposal.
- [ ] Disposal has been approved by the authorized role.
- [ ] The selected disposal method is suitable for the media, storage system, and sensitivity.
- [ ] Copies, replicas, exports, backups, and derived artifacts have been considered.
- [ ] Any third-party storage or service requirements have been addressed.
- [ ] Disposal was completed by an authorized person or service.
- [ ] Completion evidence, audit event, or certificate is recorded where appropriate.
- [ ] The register and lifecycle history have been updated.
- [ ] Exceptions, inaccessible copies, and deferred actions are documented.
- [ ] Required review or approval of the disposal record is complete.

| Disposal record field | Record |
|---|---|
| Disposal record ID | `[DISP-###]` |
| Evidence ID(s) | `[EVD-### references]` |
| Retention rule / schedule | `[Reference]` |
| Legal hold check | `[Result / reviewer / date]` |
| Authorization | `[Approver / reference / date]` |
| Media / storage type | `[Type]` |
| Approved disposal method | `[Method]` |
| Copies / derivatives considered | `[Locations and outcome]` |
| Completion date/time + zone | `[Timestamp]` |
| Performed by | `[Role / service]` |
| Completion evidence | `[Certificate / audit record / reference]` |
| Exceptions / remaining copies | `[Details / None]` |
| Register updated by / date | `[Role / date]` |
| Final review | `[Role / date / N/A + rationale]` |

## 10. Worked example (fictional)

> All names, IDs, systems, locations, and outcomes below are fictional. Replace them with authorized assessment records before use.

### 10.1 Summary row

| Evidence ID | Assessment ID | Title | Type | Source | Related check / finding / risk | Validation | Integrity | Classification | Lifecycle |
|---|---|---|---|---|---|---|---|---|---|
| `EVD-EX-001` | `ASSESS-EX-001` | Administrative group membership export | Configuration export | `SRV-EX-01` | `CHECK-EX-001` / `FIND-EX-001` / `RISK-EX-001` | Partially validated | Verified for the compared export bytes; scope limited | Fictional organization-defined classification | Approved for stated use with limitations |

### 10.2 Detailed record highlights

| Field | Fictional entry |
|---|---|
| Purpose | Review privileged group membership against approved access records |
| Authorization | `AUTH-EX-001` |
| Collection method | Approved read-only export under a documented procedure |
| Collection time | `[Fictional timestamp and time zone]` |
| Storage reference | `[Fictional controlled repository reference]` |
| Integrity approach | Hash recorded for the retained export and compared with the working copy; hash algorithm and values would be entered in the actual record |
| Validation | Source and export context reviewed; selected memberships compared with approved access records |
| Outcome | Partially validated |
| Limitation | The export is a snapshot of the reviewed system. It does not establish the state of every account or historical membership outside the collection window. |
| Custody decision | Formal custody tracking not required for this routine fictional review; rationale recorded |
| Retention | Governed by the applicable organizational schedule and any preservation requirements |

### 10.3 Related evidence gap

| Field | Fictional entry |
|---|---|
| Gap ID | `GAP-EX-001` |
| Related evidence | `EVD-EX-001` |
| Description | Approval for one listed administrative account could not be located in the reviewed records |
| Effect | The reviewer cannot conclude from the export alone that the account's current access is authorized |
| Follow-up | Obtain the approval record or request confirmation from the authorized access owner |
| Status | Open |
| Reporting treatment | State the limitation and avoid treating the absence of a located approval as conclusive proof that no approval exists |

This example illustrates the expected traceability between evidence, validation, gaps, findings, and risks without treating an evidence artifact as conclusive beyond its documented scope.

## 11. Lifecycle status guidance

Organizations may tailor the following suggested states. Record material transitions in the history section or the approved system of record.

| State | Meaning |
|---|---|
| Planned | Collection is expected but has not occurred |
| Collected | Obtained and registered |
| Under validation | Provenance, integrity, relevance, or content is being reviewed |
| Validated | Required validation checks passed for the stated purpose |
| Partially validated | Some checks passed but material limitations remain |
| Restricted | Access or use is limited by sensitivity, legal, or handling requirements |
| Approved for use | Reviewed as suitable for the stated purpose, subject to recorded limitations |
| Exception | A material collection, integrity, access, or handling exception remains open |
| Retained | Held under applicable retention requirements |
| Disposed | Authorized disposal was completed and recorded |

Use separate fields for lifecycle status, validation status, integrity status, and approval for use. They represent different decisions and should not be collapsed into a single status.

## 12. Configuration and governance guidance

Before adopting this template, define:

1. **Identifiers:** Assessment, evidence, check, finding, risk, gap, exception, custody, validation, and disposal ID conventions.
2. **Classification:** Approved labels, handling rules, and access restrictions.
3. **Repository:** Approved evidence storage, access controls, backup, audit logging, and secure transfer mechanisms.
4. **Validation criteria:** Minimum checks by evidence type and intended use.
5. **Integrity rules:** When hashes, signatures, corroboration, source validation, or other checks are expected.
6. **Custody rules:** Triggers for formal chain-of-custody tracking and required approvals.
7. **Retention:** Applicable schedules, legal holds, review triggers, and disposal authorities.
8. **Review independence:** When an independent reviewer is required based on significance, risk, or policy.
9. **Reporting:** How to reference evidence without exposing restricted content.
10. **Exceptions:** How to document, escalate, approve, and close material gaps or deviations.
11. **Auditability:** Where record changes, access, transfer, validation, and disposal events are logged.
12. **Periodic review:** How the template and related procedures are reviewed and updated.

Do not assume that using this template establishes compliance with a standard, law, or regulatory obligation. Assess applicability and compliance against the actual requirements and the organization's approved procedures.

## 13. Related framework documents

Expected repository-relative references:

- [Evidence handling procedure](../docs/methodology/evidence-handling.md)
- [Assessment lifecycle](../docs/methodology/assessment-lifecycle.md)
- [Risk assessment methodology](../docs/methodology/risk-assessment-methodology.md)
- [Risk scoring model](../docs/methodology/risk-scoring-model.md)
- [Standards and frameworks register](../references/standards-and-frameworks.md)
- [Technical assessment checklist](technical-assessment-checklist.md)
- [Assessment report template](assessment-report-template.md)
- [Risk register template](risk-register-template.md)

These links are intended for the proposed repository structure and may not resolve when this file is viewed outside that structure.

## 14. Document control

| Field | Value |
|---|---|
| Template ID | `TPL-EVD-001` |
| Version | `1.0` |
| Status | Draft for organizational adaptation |
| Owner | `[Document owner / function]` |
| Approved by | `[Approver / authority]` |
| Effective date | `[YYYY-MM-DD]` |
| Next review date | `[YYYY-MM-DD]` |
| Change history | `[Record changes in the repository changelog or below]` |

| Version | Date | Author / role | Change summary | Reviewer / approver |
|---|---|---|---|---|
| `1.0` | `[YYYY-MM-DD]` | `[Role]` | Initial template | `[Role / pending]` |

---

**End of template.**
