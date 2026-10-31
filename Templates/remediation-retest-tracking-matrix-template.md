---
document_title: Remediation and Retest Tracking Matrix
document_id: RRT-001
version: 1.0
status: Template
---

# Remediation and Retest Tracking Matrix

## 1. Tracking record

| Field | Entry |
|---|---|
| Assessment ID | [ID] |
| Finding ID | [ID] |
| Asset ID | [ID] |
| Finding / affected version | [Description] |
| Priority and rationale | [Priority / context] |
| Risk owner | [Role] |
| Technical owner | [Role] |
| Change / ticket reference | [ID] |
| Target date | [Approved date] |

## 2. Remediation plan

| Action ID | Corrective action | Expected secure state | Dependencies / outage window | Rollback / contingency | Owner | Due date | Status |
|---|---|---|---|---|---|---|---|
| [ID] | [Patch/configure/upgrade/isolate] | [Measurable outcome] | [Details] | [Details] | [Role] | [Date] | [Status] |

## 3. Retest plan and results

| Retest ID | Date/time (TZ) | Assessor | Method / tool version | Exact asset / version / image digest | Test criteria | Result | Evidence IDs | Limitations |
|---|---|---|---|---|---|---|---|---|
| [ID] | [Timestamp] | [Role] | [Method] | [Identity] | [Criteria] | [Pass/Fail/Partial] | [IDs] | [Details] |

## 4. Closure criteria

- [ ] Corrective change is implemented and approved.
- [ ] Actual deployed asset, package, configuration or image digest is verified.
- [ ] Retest uses a method capable of testing the original condition.
- [ ] Relevant scan/manual check passes.
- [ ] Service functionality and operational health are confirmed.
- [ ] Evidence is registered and validated.
- [ ] Residual exposure and limitations are documented.
- [ ] Any remaining issue is kept open or split into a traceable finding.
- [ ] Exception, if any, is separately approved and time-bound.
- [ ] Assessment lead and relevant owner approve closure.

## 5. Retest disposition

Decision: [Closed / Remains open / Partially remediated / False positive / Exception requested]

Rationale: [Explain the evidence and criteria supporting the decision.]

Next action, owner and due date: [Details]

| Role | Name | Decision | Date |
|---|---|---|---|
| Technical owner | [Name] | [Submitted] | [Date] |
| Independent assessor | [Name] | [Verified / returned] | [Date] |
| Risk owner | [Name] | [Acknowledged / decision] | [Date] |
