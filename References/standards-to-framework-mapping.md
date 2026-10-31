---
title: "Standards-to-Framework Mapping"
document_type: "Mapping Register"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# Standards-to-Framework Mapping

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Purpose and interpretation

This document provides an indicative mapping between repository document families and external standards or frameworks. It supports navigation, planning and traceability. It is not a formal control crosswalk, legal opinion, certification assessment or assertion of compliance.

A mapping indicates thematic relevance only. Clause-level or control-level equivalence requires review of the authorized source text, organizational scope, applicability, implementation evidence and edition.

## 2. Document-family mapping

| Repository document family | Primary references | Supporting references | Mapping rationale |
|---|---|---|---|
| Governance and information security policy | NIST CSF 2.0; ISO/IEC 27001:2022 | ISO/IEC 27002:2022; NIST SP 800-53 Rev. 5 (including applicable Release 5.2.0 updates) | Governance, policy, accountability and control framework themes |
| Assessment lifecycle and authorization | NIST SP 800-37 Rev. 2; NIST SP 800-115 | ISO/IEC 27001:2022 | Planning, authorization, execution and assurance lifecycle |
| Risk assessment and scoring | NIST SP 800-30 Rev. 1; ISO/IEC 27005:2022 | NIST CSF 2.0 | Risk scenarios, likelihood, impact, evaluation and treatment |
| Security control assessment | NIST SP 800-53 Rev. 5 (including applicable Release 5.2.0 updates) | ISO/IEC 27002:2022; NIST SP 800-37 Rev. 2 | Control objectives, assessment evidence and effectiveness |
| Technical security assessment | NIST SP 800-115 | OWASP WSTG; OWASP ASVS; CIS Benchmarks | Technical testing and technology-specific verification |
| Vulnerability assessment and remediation | NIST SP 800-40 Rev. 4 | CVSS 4.0; CISA KEV; CIS Controls v8.1 | Vulnerability identification, prioritization and patch management |
| Incident response | NIST SP 800-61 Rev. 3 | ISO/IEC 27035 series; MITRE ATT&CK | Incident preparation, detection, response, recovery and learning |
| Logging and monitoring | NIST SP 800-53 Rev. 5 (including applicable Release 5.2.0 updates) | CIS Controls; MITRE ATT&CK | Audit events, monitoring, detection and control visibility |
| Evidence handling | NIST SP 800-115 | Relevant forensic guidance and organizational legal requirements | Evidence collection, preservation, analysis and traceability |
| Third-party and supplier security | NIST SP 800-161 Rev. 1 | ISO/IEC 27036 series; CSA CCM | Supply-chain risk, supplier controls and assurance |
| Cloud security | ISO/IEC 27017; ISO/IEC 27018 | CSA CCM; NIST SP 800-53 | Cloud control responsibilities, service security and privacy |
| Application and API security | OWASP ASVS 5.0.0; OWASP WSTG (verify current stable release); OWASP API Security Top 10 | NIST SP 800-53 | Application verification and API risk coverage |
| Business continuity and recovery | NIST CSF 2.0 | ISO/IEC 27001 / 27002; relevant continuity standards | Resilience, recovery and service continuity themes |

## 3. Mapping status

Use the following mapping status for detailed future crosswalks:

- **Thematic:** subject matter is related, but no clause-level analysis has been completed.
- **Reviewed:** source text and repository requirement have been compared by a competent reviewer.
- **Partially aligned:** some mapped requirements are addressed; gaps or exclusions remain.
- **Not assessed:** no evidence-based conclusion has been made.
- **Not applicable:** documented rationale explains why the reference does not apply.

Do not use a status such as "compliant" based solely on this table.

## 4. Document-level traceability worksheet

| Repository document | External source and edition | Clause / control reference | Relevant repository section | Mapping status | Reviewer / date | Gap / action |
|---|---|---|---|---|---|---|
| [Path] | [Title, edition] | [Exact clause] | [Section] | [Status] | [Reviewer/date] | [Details] |

## 5. Maintaining the mapping

1. Identify the exact edition and authorized source text.
2. Confirm organizational and technical applicability.
3. Compare requirement intent, scope, roles, evidence and expected outcomes.
4. Record partial coverage, exclusions, conflicts and compensating measures.
5. Obtain review by the relevant control owner and compliance/legal function where required.
6. Reassess when either the external source or repository document changes.

## 6. Limitations

The NIST SP 800-53 reference should include applicable Release 5.2.0 changes; the OWASP ASVS reference is 5.0.0; and the CVSS reference is 4.0 as recorded in the standards register. Reconfirm versions at the date of each assessment.

This mapping is deliberately high-level. It does not claim one-to-one equivalence between standards, nor does it replace a formal Statement of Applicability, control assessment, certification audit, regulatory interpretation or legal review.
