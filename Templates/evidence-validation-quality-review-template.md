---
document_title: Evidence Validation and Quality Review
document_id: EVQ-001
version: 1.0
status: Template
---

# Evidence Validation and Quality Review

## 1. Review details

| Field | Entry |
|---|---|
| Assessment ID | [ID] |
| Evidence ID(s) | [IDs] |
| Reviewer | [Name / role] |
| Review date/time | [Timestamp with time zone] |
| Related checklist / control | [Reference] |
| Related finding / risk | [Reference] |
| Review objective | [Question the evidence is intended to answer] |

## 2. Quality criteria

Rate each criterion as Satisfactory, Partially satisfactory, Unsatisfactory or Not applicable. Explain any partial or unsatisfactory rating.

| Criterion | Review question | Rating | Rationale / limitation |
|---|---|---|---|
| Relevance | Does the evidence address the stated control or test objective? | [Rating] | [Rationale] |
| Reliability | Is the source and collection method sufficiently trustworthy? | [Rating] | [Rationale] |
| Integrity | Is the object protected against or checked for unauthorized change? | [Rating] | [Rationale] |
| Completeness | Is sufficient context included to support the conclusion? | [Rating] | [Rationale] |
| Timeliness | Is the evidence current for the period being assessed? | [Rating] | [Rationale] |
| Accuracy | Does the evidence accurately represent the observed condition? | [Rating] | [Rationale] |
| Reproducibility | Are steps, tools, versions and parameters recorded sufficiently? | [Rating] | [Rationale] |
| Provenance | Can source, collector and transformations be traced? | [Rating] | [Rationale] |
| Confidentiality | Is access and disclosure proportionate to sensitivity? | [Rating] | [Rationale] |

## 3. Technical validation

- File/object readable: [Yes / No / N/A]
- Expected system and scope confirmed: [Yes / No / N/A]
- Collection time and time zone confirmed: [Yes / No / N/A]
- Hash verified against recorded value: [Yes / No / N/A]
- Hash algorithm: [SHA-256 or approved alternative]
- Tool and version: [Details]
- Transfer/copy validation: [Details]
- Redaction or transformation reviewed: [Details]
- Sampling or selection bias considered: [Details]
- Corroborating evidence identified: [References]

A cryptographic digest can detect byte-level changes relative to a known digest. It cannot prove that a screenshot is truthful, a log source is correctly configured, a scan covered every asset, or a source system's clock was accurate.

## 4. Conclusion

Decision:
- [ ] Accepted
- [ ] Accepted with limitations
- [ ] Rejected
- [ ] Further evidence required

Reasoning: [Explain how the evidence supports, contradicts or fails to support the assessment assertion.]

Permitted use: [Specific checklist item, finding, report section or other purpose.]

Limitations / caveats: [State explicitly.]

Required follow-up: [Owner, action and due date.]

## 5. Review approval

| Role | Name | Decision | Date |
|---|---|---|---|
| Reviewer | [Name] | [Decision] | [Date] |
| Assessment lead | [Name] | [Approved / returned] | [Date] |
