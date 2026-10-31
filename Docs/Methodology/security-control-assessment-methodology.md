---
title: "Security Control Assessment Methodology"
document_type: "Methodology"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Security Control Assessment Methodology

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## 1. Purpose

Defines a repeatable method for assessing whether security controls are appropriately designed, implemented, and operating effectively.

## 2. Applicability and principles

This methodology applies where the assessment objective and scope require it. Apply proportionality, authorization, independence where warranted, evidence traceability, risk-based depth, transparency of assumptions, and explicit disclosure of limitations. Tailor methods to the technology, business process, threat context, and applicable obligations.

## 1. Assessment objectives and assurance model

A control assessment determines whether a control is suitable for its stated objective, exists in the assessed environment, and operates consistently over the period under review. Assessments should distinguish three dimensions:

- **Design effectiveness:** whether the control, if implemented as designed, is capable of addressing the relevant risk.
- **Implementation effectiveness:** whether the control has been deployed in the assessed scope and is configured or adopted as intended.
- **Operating effectiveness:** whether the control operated consistently and produced the expected outcome during the defined assessment period.

A control may be well designed but not implemented, implemented but not operating, or operating with limitations. Do not collapse these dimensions into a single unsupported conclusion.

## 2. Scope and assessment criteria

Define the control objective, control statement, system or process boundary, population, period, locations, technology, business units, interfaces, dependencies, and exclusions. Identify the authoritative policy, procedure, standard, contract, or control framework requirement. Translate broad requirements into testable criteria and record the rationale for any tailoring.

## 3. Assessment planning

Create an assessment plan that records objectives, scope, criteria, roles, schedule, evidence needs, sampling approach, tools, access requirements, dependencies, safety constraints, and reporting expectations. Obtain authorization under `docs/procedures/security-assessment-authorization-procedure.md` before testing. Identify conflicts of interest and determine whether independent review is needed.

## 4. Evidence strategy

Use evidence appropriate to the control and assertion being tested. Evidence may include configuration exports, system-generated logs, tickets, approvals, observed demonstrations, interviews, reconciliations, test results, and independently corroborated records. Assess relevance, reliability, completeness, currency, provenance, and consistency. Interviews and policy statements alone normally do not establish technical implementation or sustained operation.

## 5. Test design and execution

For each criterion, define the assertion, test procedure, expected result, actual result, population, sample, evidence reference, and conclusion. Use inspection, inquiry, observation, reperformance, configuration review, technical testing, or data analysis as appropriate. Tests must remain within authorized scope and avoid unnecessary disruption or collection of sensitive information.

## 6. Evaluation and conclusion

Conclude separately on design, implementation, and operating effectiveness using an organization-approved rating scale. A suggested scale is Effective, Partially Effective, Ineffective, and Not Assessed; define thresholds and evidence requirements before use. Explain the basis, exceptions, period, population, and limitations. Do not infer effectiveness from the existence of a policy or a single successful test.

## 7. Deficiencies and risk linkage

Record deficiencies as findings with condition, criteria, cause where supported, consequence or risk scenario, evidence, recommendation, owner, and status. Link findings to the risk assessment methodology and scoring model. Control effectiveness is an input to risk analysis, not a substitute for direct assessment of residual risk.

## 8. Reporting and assurance

Report scope, criteria, period, methods, sampling, limitations, results by effectiveness dimension, findings, unresolved questions, and management responses. Distinguish verified facts from management representations and assessor inference. Provide traceability from each conclusion to evidence references.

## 9. Quality review

A reviewer independent of the test where proportionate should check scope, authorization, test reproducibility, evidence sufficiency, calculations, rating rationale, finding traceability, and report consistency. Resolve review comments before issuance or document accepted limitations.

## 10. Reassessment and maintenance

Reassess after material changes, incidents, control failures, significant findings, changes in threat or regulatory context, or expiration of the assurance period. Review this methodology annually and maintain version history.

## 11. Required outputs and records

- Control assessment plan
- Control-to-criteria mapping
- Test-of-design and test-of-operation worksheets
- Evidence register
- Control effectiveness conclusion
- Finding and remediation records
- Quality review checklist

## 12. Related documents

- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/security-incident-response-procedure.md`

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
