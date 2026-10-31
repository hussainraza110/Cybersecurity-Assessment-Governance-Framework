---
document_title: Evidence Register Template
document_id: ERT-001
version: 1.0
status: Template
owner: Assessment Lead
classification: Internal
---

# Evidence Register Template

## 1. Purpose

Use this register to identify, describe, classify, locate and trace evidence collected during an authorized security assessment. Each evidence item must have a unique identifier and a clear relationship to the assessment scope, test procedure, control, checklist item, finding or risk.

This register is an assessment-management record. It is not, by itself, a forensic chain-of-custody system. Apply the separate custody record where evidence is sensitive, disputed, legally significant, transferred between custodians, or collected under a formal forensic process.

## 2. Instructions

1. Create one register per assessment, or use an approved centralized register with an unambiguous assessment identifier.
2. Assign a unique Evidence ID before or at the time of collection.
3. Record timestamps with an explicit time zone and use a consistent organizational time standard.
4. Record the original source and collection method; distinguish original evidence from working copies, exports, screenshots and derived analysis.
5. Calculate a SHA-256 digest for files where integrity verification is applicable. Record the tool and time used. A hash demonstrates whether bytes match a previously hashed object; it does not establish authenticity, accuracy or completeness.
6. Store evidence only in approved repositories with access controls appropriate to its classification.
7. Do not place passwords, tokens, private keys, personal data or other secrets in this register. Reference a controlled secret store or restricted evidence object instead.
8. Record limitations, redactions, transformations and failed collection attempts.
9. Link each evidence item to the relevant checklist item, control, finding or risk.
10. Apply retention and disposal requirements defined by the organization, contract and applicable law.

## 3. Assessment details

| Field | Entry |
|---|---|
| Assessment ID | [Unique identifier] |
| Assessment title | [Title] |
| Assessed organization / business unit | [Name] |
| Assessment scope | [Systems, networks, applications, locations] |
| Authorization reference | [Approval / rules-of-engagement ID] |
| Assessment lead | [Name / role] |
| Evidence custodian | [Name / role] |
| Evidence repository | [Approved repository identifier; do not expose secrets] |
| Time standard | [e.g., UTC; state if local time is used] |
| Register version / date | [Version / date] |

## 4. Evidence register

Create one row per evidence object. Use the companion collection record when additional detail is needed.

| Evidence ID | Date/time collected (with TZ) | Collector | Source / asset | Evidence description | Type / format | Classification | Collection method / tool | Original or derived | SHA-256 / not applicable reason | Storage reference | Checklist / control reference | Finding / risk reference | Validation status | Retention / review date | Notes / limitations |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| [EVD-001] | [YYYY-MM-DD hh:mm TZ] | [Role] | [Asset ID] | [Description] | [Format] | [Class] | [Method] | [Original/Derived] | [Digest or reason] | [Restricted locator] | [ID] | [ID / none] | [Pending/Accepted/Rejected] | [Date] | [Limitations] |

## 5. Evidence status definitions

| Status | Meaning |
|---|---|
| Planned | Identified but not yet collected |
| Collected | Acquired; validation not complete |
| Pending validation | Integrity, relevance or completeness review is in progress |
| Accepted | Suitable for the stated assessment purpose, subject to recorded limitations |
| Rejected | Not suitable; reason recorded |
| Superseded | Replaced by a later or better-supported evidence item; preserve traceability |
| Restricted | Access limited due to sensitivity or legal/contractual constraints |
| Disposed | Disposed under an approved retention process; retain disposal record/metadata as permitted |

## 6. Evidence quality review

For each material evidence item, assess:

- **Relevance:** Does it address the control, test objective or assertion?
- **Reliability:** Is the source and collection method sufficiently trustworthy?
- **Integrity:** Can changes since collection be detected where applicable?
- **Completeness:** Is the evidence adequate to support the conclusion, including relevant context?
- **Timeliness:** Was it collected within a period relevant to the conclusion?
- **Reproducibility:** Can another authorized assessor understand how it was obtained?
- **Limitations:** Are sampling, access, time, tool or environmental limitations documented?

A hash match alone is not sufficient evidence quality validation.

## 7. Cross-reference and traceability

| Evidence ID | Checklist item | Control / requirement | Finding ID | Risk ID | Report section | Relationship / rationale |
|---|---|---|---|---|---|---|
| [EVD-001] | [CHK-001] | [CTRL-001] | [FND-001] | [RSK-001] | [Section] | [How evidence supports or limits the conclusion] |

Evidence may support multiple findings or controls. Record each relationship explicitly rather than relying on filenames or assessor memory.

## 8. Register reconciliation and closure

Before assessment closure, confirm:

- [ ] Every evidence item has a unique ID and description.
- [ ] Collection source, method, collector and timestamp are recorded.
- [ ] Applicable hashes have been calculated and independently checked where required.
- [ ] Evidence locations resolve for authorized reviewers.
- [ ] Classification and access restrictions are applied.
- [ ] Material evidence is linked to checklist items, findings and report sections.
- [ ] Rejected, superseded, missing and inaccessible evidence is explained.
- [ ] Retention, legal hold and disposal requirements are assigned.
- [ ] Sensitive evidence is not embedded in an unrestricted report or repository.
- [ ] Outstanding evidence gaps are disclosed in the assessment report.

## 9. Approval

| Role | Name | Decision | Date | Comments |
|---|---|---|---|---|
| Evidence custodian | [Name] | [Accepted / returned] | [Date] | [Comments] |
| Assessment lead | [Name] | [Approved / returned] | [Date] | [Comments] |
| Data / system owner, if required | [Name] | [Acknowledged / approved] | [Date] | [Comments] |

## 10. Worked example (fictional)

| Field | Example |
|---|---|
| Evidence ID | EVD-EX-001 |
| Source | APP-SRV-02 (fictional asset identifier) |
| Description | Redacted screenshot of TLS configuration showing supported protocol versions |
| Collection method | Authorized administrative review; screenshot captured by assessor |
| Collected | 2026-09-15 10:35 UTC |
| Classification | Confidential |
| Original or derived | Derived representation of observed configuration |
| SHA-256 | [Illustrative placeholder; calculate against the actual retained file] |
| Storage reference | SECURE-REPO/ASSESS-EX-01/EVD-EX-001 |
| Checklist reference | APP-TLS-004 |
| Finding reference | FND-EX-003 |
| Validation | Accepted with limitation: screenshot does not independently prove all listener configurations |

This example is fictional. Do not treat its identifiers, timestamps or storage reference as real organizational records.
