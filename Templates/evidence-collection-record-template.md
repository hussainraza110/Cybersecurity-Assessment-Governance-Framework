---
document_title: Evidence Collection Record
document_id: ECR-001
version: 1.0
status: Template
---

# Evidence Collection Record

## 1. Collection record

| Field | Entry |
|---|---|
| Assessment ID | [ID] |
| Evidence ID | [ID; must match Evidence Register] |
| Collection event ID | [ID] |
| Date/time started and completed | [Timestamp with time zone] |
| Collector | [Name / role / organization] |
| Witness / reviewer, if applicable | [Name / role] |
| Source system / asset | [Asset ID, hostname or controlled reference] |
| Source owner / contact | [Role or controlled contact reference] |
| Authorization / ROE reference | [Approval ID] |
| Collection purpose | [Control, test objective or finding] |

## 2. Collection method

- Method: [Administrative export / command output / screenshot / configuration backup / log export / scan result / other]
- Tool and version: [Name, version, relevant configuration]
- Collection location / interface: [Non-sensitive description]
- Scope and filters: [Exact scope, query, date range or selection criteria]
- Commands / procedure: [Record safe, reproducible steps; redact secrets]
- Clock source and time zone: [Details]
- Collection errors or interruptions: [Details or none]

## 3. Object description

| Attribute | Entry |
|---|---|
| Filename / object name | [Name] |
| Format / media type | [Type] |
| Size | [Bytes] |
| Source path / query reference | [Controlled reference] |
| Original / working copy / derived | [Select one] |
| Redactions / transformations | [Details or none] |
| SHA-256 | [Digest or not applicable with reason] |
| Hash tool / version | [Tool] |
| Hash date/time | [Timestamp with time zone] |

## 4. Validation

- [ ] Object opens or is readable using an appropriate tool.
- [ ] Expected content and scope are present.
- [ ] Source, time range and collection filters are documented.
- [ ] Hash is recorded where applicable.
- [ ] Hash has been rechecked after transfer or copy where required.
- [ ] Sensitive fields are redacted from derivative copies where appropriate.
- [ ] Original is preserved when a derivative is created.
- [ ] Limitations and collection failures are recorded.

Validation outcome: [Accepted / Accepted with limitations / Rejected / Pending]

Rationale: [Explain the outcome; do not equate a successful hash calculation with evidence authenticity.]

## 5. Storage and handling

| Field | Entry |
|---|---|
| Classification | [Classification] |
| Repository / storage reference | [Controlled locator] |
| Access group / custodian | [Role or group] |
| Encryption / protection | [Approved control reference] |
| Retention trigger / review date | [Date or event] |
| Legal hold | [Yes / No / Pending confirmation] |

## 6. Exceptions and notes

[Document missing context, sampling, access constraints, time drift, tool limitations, redactions, suspected contamination or deviations from the approved procedure.]

## 7. Sign-off

| Role | Name | Decision | Date |
|---|---|---|---|
| Collector | [Name] | [Submitted] | [Date] |
| Evidence reviewer | [Name] | [Accepted / returned] | [Date] |
