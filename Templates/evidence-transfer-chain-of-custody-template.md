---
document_title: Evidence Transfer and Chain-of-Custody Record
document_id: COC-001
version: 1.0
status: Template
---

# Evidence Transfer and Chain-of-Custody Record

## 1. Applicability

Use this record when formal custody continuity is required, including forensic acquisition, potentially disputed evidence, legally significant material, sensitive evidence transferred between custodians, or explicit contractual/regulatory requirements. Routine screenshots and ordinary assessment exports may be managed through the Evidence Register and Collection Record when organizational policy permits.

This record documents handling; it does not independently establish that the evidence was authentic at source or that collection was lawful. Confirm authorization, privacy, legal and organizational requirements before collection or transfer.

## 2. Evidence identification

| Field | Entry |
|---|---|
| Assessment / case ID | [ID] |
| Evidence ID | [ID] |
| Object description | [Description] |
| Original / forensic image / copy | [Type] |
| Media / file format | [Type] |
| Size / serial number | [Value] |
| Classification | [Class] |
| Initial SHA-256 | [Digest / reason not applicable] |
| Collection record | [Reference] |
| Authorization | [Reference] |

## 3. Custody event log

Record each custody change, access, movement, seal change, or other material handling event. Do not leave unexplained gaps.

| Event no. | Date/time (TZ) | Released by | Received by | From / to location | Purpose | Package / seal state | SHA-256 before / after, if applicable | Signatures / acknowledgement | Notes |
|---|---|---|---|---|---|---|---|---|---|
| 001 | [Timestamp] | [Name] | [Name] | [Location] | [Purpose] | [Intact / N/A] | [Digest] | [References] | [Notes] |

## 4. Transfer verification

Before transfer:
- [ ] Transfer is authorized and necessary.
- [ ] Recipient identity and authority are verified.
- [ ] Evidence ID and object description match the register.
- [ ] Packaging, encryption and transport controls are appropriate.
- [ ] Current hash is recorded where applicable.
- [ ] Transfer method and expected receipt are agreed.

On receipt:
- [ ] Recipient records receipt date/time and condition.
- [ ] Package/seal condition is recorded.
- [ ] Hash is recalculated for file-based evidence where applicable.
- [ ] Any discrepancy is documented and escalated.
- [ ] Evidence is placed in approved storage with access restricted.

## 5. Discrepancy / incident record

| Field | Entry |
|---|---|
| Discrepancy ID | [ID] |
| Date/time discovered | [Timestamp] |
| Description | [Missing item, broken seal, hash mismatch, unexplained access, etc.] |
| Immediate containment | [Action] |
| Persons notified | [Roles] |
| Impact assessment | [Effect on reliability, admissibility or assessment conclusion] |
| Resolution / disposition | [Action and approval] |
| Related incident / finding | [Reference] |

A hash mismatch must be treated as an integrity exception. Preserve both versions where authorized, avoid overwriting the original, restrict access, and escalate to the evidence custodian and incident/legal contacts as applicable. Do not assume the cause.

## 6. Closure

| Role | Name | Confirmation | Date |
|---|---|---|---|
| Current custodian | [Name] | [Custody accepted] | [Date] |
| Evidence custodian | [Name] | [Record reviewed] | [Date] |
| Case / assessment lead | [Name] | [Approved closure / further action] | [Date] |
