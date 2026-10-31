---
title: "Finding Classification and Severity Methodology"
document_type: "Methodology"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Finding Classification and Severity Methodology

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## 1. Purpose

Defines consistent classification, validation, severity assessment, prioritization, and reporting of security assessment findings.

## 2. Applicability and principles

This methodology applies where the assessment objective and scope require it. Apply proportionality, authorization, independence where warranted, evidence traceability, risk-based depth, transparency of assumptions, and explicit disclosure of limitations. Tailor methods to the technology, business process, threat context, and applicable obligations.

## 1. Purpose and terminology

A **finding** is an evidenced condition that does not meet an assessment criterion or creates a security concern. A **vulnerability** is a weakness that could be exploited or otherwise contribute to adverse impact. An **observation** is relevant information that does not necessarily represent a control failure. A **risk** describes the effect of uncertainty on objectives and must be assessed using the approved risk methodology.

## 2. Classification taxonomy

Classify findings using an approved taxonomy such as vulnerability, configuration weakness, access-control deficiency, process/control gap, data protection issue, resilience weakness, monitoring gap, or policy non-compliance. Record whether the condition is confirmed, probable, unverified, false positive, or not applicable. Define taxonomy values in the assessment plan before execution.

## 3. Validation threshold

A finding should be supported by evidence that identifies the affected asset or process, the observed condition, the relevant criterion, and a defensible consequence or risk scenario. Corroborate scanner output and interviews where practicable. If validation is incomplete, disclose uncertainty and do not present an assumption as a verified fact.

## 4. Severity dimensions

Assess technical severity using relevant factors such as exploitability, required privileges, user interaction, exposure, affected scope, confidentiality/integrity/availability consequences, and known exploitation. Assess organizational risk separately using the approved likelihood-impact methodology, asset context, controls, and business consequences.

## 5. Severity scale and calibration

If the organization uses Critical, High, Moderate, Low, and Informational categories, it must define explicit criteria, examples, escalation expectations, and approval authority. Do not invent universal numeric thresholds or equate a CVSS score mechanically with organizational risk. Document the scoring version and any override rationale.

## 6. Prioritization

Prioritize remediation by combining validated technical severity with asset criticality, external exposure, threat intelligence, exploitation evidence, business impact, compensating controls, and applicable deadlines. A lower technical score may still require urgent action when business context warrants it. Conversely, a high technical score may have reduced exposure but still requires documented treatment.

## 7. Finding record minimums

Record unique ID, title, date, assessor, affected assets, scope, classification, status, criterion, condition, evidence references, validation method, severity rationale, risk reference, recommendation, owner, target date, response, retest result, and closure approval.

## 8. Exceptions, disputes, and overrides

Owners may challenge factual accuracy or severity with evidence. Preserve the original assessment and record the decision, rationale, reviewer, and date. Severity overrides must be transparent, approved, and traceable; they must not silently alter the underlying evidence.

## 9. Reporting and trend analysis

Report counts by classification and severity, affected business services, aging, recurrence, overdue remediation, accepted risk, and validation status. Normalize trends by assessment scope or population where possible. Avoid presenting raw finding counts as a standalone measure of security posture.

## 10. Quality and review

Review severity calibration periodically using resolved findings, incident outcomes, threat changes, and assessor consistency. Maintain examples and decision records to improve repeatability.

## 11. Required outputs and records

- Finding taxonomy
- Severity rubric
- Finding validation record
- Severity rationale
- Finding register
- Dispute and override record

## 12. Related documents

- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/technical-security-assessment-methodology.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `templates/assessment-report-template.md`

## 13. Governance and review

The methodology owner is Information Security unless assigned otherwise. Material deviations must be documented with rationale and approval. Review at least annually and after significant changes to risk, technology, standards, incidents, or assurance objectives.

## Appendix A — Method tailoring record

| Field | Entry |
|---|---|
| Assessment / project | [Identifier] |
| Methodology version | [Version] |
| Scope and objective | [Description] |
| Tailored steps | [Description / rationale] |
| Excluded steps | [Description / rationale] |
| Assumptions and limitations | [Details] |
| Approver | [Name / role] |
| Approval date | [Date] |
