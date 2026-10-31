---
title: "Assessment Sampling Methodology"
document_type: "Methodology"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Assessment Sampling Methodology

> **Implementation note:** This organization-neutral framework document must be tailored, reviewed, and approved before operational adoption. Replace bracketed fields and validate applicable legal, regulatory, contractual, and sector-specific requirements.

## 1. Purpose

Provides a defensible approach to selecting and evaluating samples when testing populations of users, assets, transactions, configurations, or control activities.

## 2. Applicability and principles

This methodology applies where the assessment objective and scope require it. Apply proportionality, authorization, independence where warranted, evidence traceability, risk-based depth, transparency of assumptions, and explicit disclosure of limitations. Tailor methods to the technology, business process, threat context, and applicable obligations.

## 1. Purpose and limitations

Sampling is used when testing every item is impractical or unnecessary. A sample supports conclusions only about the defined population, selection method, period, and test objective. A sample does not prove that untested items are compliant. Sampling risk and non-sampling limitations must be disclosed.

## 2. Define the population

Specify the complete population, source system, extraction date, period, inclusion/exclusion criteria, unit of analysis, and total population size. Reconcile population completeness to an independent source where feasible. If the population cannot be established reliably, report that limitation and avoid statistical claims.

## 3. Select the sampling method

Use random sampling when each unit should have a known selection chance; systematic sampling when a stable ordered population exists and periodicity is understood; stratified sampling when materially different risk or asset classes require representation; judgmental sampling for targeted high-risk or unusual cases; and full-population testing when feasible or warranted. Document why the method fits the objective.

## 4. Sample size rationale

Determine sample size based on assurance objective, population characteristics, expected deviation, tolerable deviation, confidence needs, control frequency, risk, and available resources. Do not use an arbitrary universal sample size. For statistical sampling, use a documented statistical method and assumptions; for judgmental sampling, do not claim statistical representativeness.

## 5. Risk-based selection

Consider criticality, privilege, internet exposure, sensitive data, geography, technology diversity, recent changes, prior failures, and unusual activity. A targeted risk sample can improve detection of high-risk exceptions but may not represent the full population. Use separate strata or disclose the selection bias.

## 6. Execution and replacement rules

Preserve the original population and selection record. Do not replace inconvenient or failed samples without rationale. If an item is unavailable, record the reason, assess whether it indicates a control weakness, and apply a pre-defined replacement rule. Maintain traceability from sample item to evidence and test result.

## 7. Evaluate deviations

Record each deviation, severity, cause where supported, and whether it is isolated or potentially systemic. Expand testing when deviations are material, clustered, unexplained, or indicate population-level control failure. Define expansion criteria before or during testing and document the decision.

## 8. Extrapolation and conclusion

Do not extrapolate sample exceptions to the entire population unless the sampling design and statistical assumptions support it. Judgmental sample results should be stated as observations about tested items. Explain confidence, limitations, coverage, and any inability to generalize.

## 9. Documentation

Retain population source, extraction details, reconciliation, selection method, random seed where applicable, sample list, exclusions, replacements, test results, deviations, expansion decisions, and conclusion.

## 10. Quality review

A reviewer should confirm population completeness, selection reproducibility, sample rationale, test execution, deviation evaluation, and whether conclusions overstate what the sample supports.

## 11. Required outputs and records

- Population definition record
- Sampling plan
- Sample selection register
- Deviation log
- Sample expansion decision
- Sampling conclusion

## 12. Related documents

- `docs/methodology/security-control-assessment-methodology.md`
- `docs/methodology/technical-security-assessment-methodology.md`
- `docs/methodology/evidence-handling.md`
- `templates/technical-assessment-checklist.md`
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
