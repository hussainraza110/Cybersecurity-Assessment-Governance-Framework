---
title: "References and Citation Guidance"
document_type: "Guidance"
document_owner: "Information Security"
approver: "Organization-designated approving authority"
version: "1.0"
status: "Draft template"
effective_date: "[YYYY-MM-DD]"
next_review_date: "[YYYY-MM-DD]"
classification: "Internal"
---

# References and Citation Guidance

> **Instructions:** This reusable, organization-neutral template must be tailored before operational use. Replace bracketed fields, remove instructions that do not apply, retain relevant evidence references, and obtain approvals from the authority formally designated by the organization. Do not include credentials, secrets, or unnecessary personal or sensitive data.

## 1. Purpose

This guidance establishes consistent, traceable and copyright-conscious use of external standards, frameworks, laws, technical advisories and knowledge bases across the repository.

## 2. Source hierarchy

Prefer, in order appropriate to the subject:
1. Official standards publisher or issuing authority.
2. Official maintainer of a framework, specification or knowledge base.
3. Government regulator or competent public authority.
4. Original research or vendor advisory directly relevant to the claim.
5. Reputable secondary commentary only when primary material is unavailable or for contextual interpretation.

Do not cite search-result snippets as authoritative evidence. Open and verify the actual source page.

## 3. Required citation metadata

For every material reference, capture:

| Field | Required information |
|---|---|
| Title | Full source title |
| Issuer / author | Official issuing organization |
| Edition / version | Exact revision, release or specification version |
| Publication / update date | Date shown by issuer, if available |
| URL | Official stable landing page or document |
| Access date | Date the source was checked |
| Relevant section | Clause, control, chapter, page or technique identifier |
| Use in repository | Document and section informed by the source |
| Status | Current / superseded / withdrawn / status unknown |
| Reviewer | Person who verified applicability |

## 4. In-text citation format

Use a consistent Markdown reference style. For example:

> The risk assessment approach is informed by NIST SP 800-30 Rev. 1, *Guide for Conducting Risk Assessments* (2012), section [exact section verified in the source].

For standards with clause-level references, identify the edition and clause precisely. Do not quote clause text from memory or a secondary summary.

A bibliography entry should include title, issuer, edition, date and official URL. Add an access date for web-maintained sources.

## 5. Distinguish requirement types

Use explicit language:
- **Mandatory organizational requirement:** a requirement adopted by approved organizational policy or procedure.
- **External normative requirement:** a binding requirement in an applicable standard, law, regulation or contract.
- **Guidance / recommendation:** informative advice that is not automatically binding.
- **Assessment criterion:** a requirement selected for a particular authorized assessment.
- **Knowledge base / taxonomy:** a descriptive resource such as ATT&CK, CVSS or an OWASP Top 10 list.

A standard reference in a document does not make every provision mandatory for the organization.

## 6. Editions, amendments and supersession

- Cite the edition actually used, not simply the latest edition known to the author.
- Check the publisher's status page for amendments, corrigenda, errata and withdrawals.
- For continuously updated resources, record the release or retrieval date and version where available.
- Do not silently replace an edition in a previously approved assessment; document the change and assess its effect.
- When a reference is superseded, retain historical traceability and identify the successor.

## 7. Copyright and permitted use

- Do not copy substantial portions of copyrighted standards or paid publications into repository files.
- Prefer original summaries, short necessary quotations, and precise citations.
- Respect the publisher's licensing terms for standards, benchmarks, diagrams and other assets.
- Do not redistribute purchased standards or imply that a public landing page grants rights to reproduce the full document.
- Use official public documentation and open project materials where possible.

## 8. Source verification and change control

Before publication or a formal assessment:
1. Open the official source page.
2. Confirm title, issuer, edition and publication/update date.
3. Confirm the URL resolves and points to the intended source.
4. Check for current revision, errata or supersession notices.
5. Record verification date and reviewer.
6. Recheck material references during annual document review and when a source update is announced.

## 9. Citation quality checklist

- [ ] Source is primary or its secondary status is disclosed.
- [ ] Exact title and issuer are recorded.
- [ ] Edition/version is correct for the assessment period.
- [ ] Referenced clause or section was checked in the source text.
- [ ] Claim is no broader than the cited source supports.
- [ ] Guidance is not misrepresented as a mandatory requirement.
- [ ] Copyright and licensing restrictions are respected.
- [ ] Superseded sources are identified and retained only where historically relevant.

## 10. Limitations

This guidance is not legal advice and does not determine whether a standard, law or regulation applies. The organization must obtain competent legal, compliance, procurement or sector-specific advice where needed.
