# Standards and Frameworks Reference Register

**Purpose:** Identify authoritative external resources that may inform this repository's assessment methodology, governance documents, technical procedures, and control mappings.

**Status:** Initial reference list. Verify the current edition, publication status, applicable amendments, and terms of use before using a reference in a deliverable. Inclusion does not mean this project conforms to it or is endorsed by its publisher.

## How references are used

For each future methodology or control document, record:
- External source and edition/version
- Specific concept, requirement, control, or recommendation applied
- Tailoring, interpretation, exclusions, and assumptions
- Date the source was checked
- Whether a mapping is independent interpretation or publisher-provided

Do not claim compliance, certification, or an official mapping solely because a checklist refers to a framework.

## Core references

| Source | Edition / version | Primary relevance | Official source |
|---|---|---|---|
| NIST Cybersecurity Framework (CSF) | CSF 2.0 (2024) | Cybersecurity governance and risk outcomes; organizing and communicating a cybersecurity program | https://www.nist.gov/cyberframework |
| NIST SP 800-30 | Revision 1 (2012) | Risk assessment concepts, threat and vulnerability analysis, likelihood, impact, and risk | https://csrc.nist.gov/pubs/sp/800/30/r1/final |
| NIST SP 800-37 | Revision 2 (2018) | Risk Management Framework and system life-cycle risk management | https://csrc.nist.gov/pubs/sp/800/37/r2/final |
| NIST SP 800-53 | Revision 5, with applicable updates | Security and privacy control catalogue for information systems and organizations | https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final |
| NIST SP 800-115 | Final (2008) | Technical information security testing and assessment planning, execution, analysis, and mitigation | https://csrc.nist.gov/pubs/sp/800/115/final |
| NIST SP 800-61 | Revision 3 (2025) | Cybersecurity incident response recommendations and integration with risk management | https://csrc.nist.gov/pubs/sp/800/61/r3/final |
| ISO/IEC 27001 | 2022 edition; check current amendments | Requirements for an information security management system (ISMS) | https://www.iso.org/standard/27001 |
| ISO/IEC 27002 | 2022 edition; verify current status | Information security controls and implementation guidance | https://www.iso.org/standard/75652.html |
| ISO/IEC 27005 | Verify current edition | Information security risk management guidance | https://www.iso.org/search.html?q=ISO%2FIEC%2027005 |
| CIS Critical Security Controls | Version 8.1 (2024) | Prioritized safeguards for common cybersecurity risks and implementation planning | https://www.cisecurity.org/controls/v8-1 |
| OWASP Application Security Verification Standard (ASVS) | Verify current release | Verifiable application security requirements and assessment criteria | https://owasp.org/www-project-application-security-verification-standard/ |
| OWASP Web Security Testing Guide (WSTG) | Verify current release | Structured methodology and test guidance for web application security testing | https://owasp.org/www-project-web-security-testing-guide/ |

## Selection guidance

### Governance and program structure
Use NIST CSF 2.0 to organize cybersecurity outcomes and communicate program-level priorities. Use ISO/IEC 27001 when discussing ISMS requirements. These sources serve different purposes and are not interchangeable.

### Risk assessment
Use NIST SP 800-30 as a principal reference for risk assessment concepts. The project's scoring model should define scales, calculation rules, assumptions, uncertainty handling, and acceptance thresholds explicitly. Do not imply that a locally designed numeric score is a NIST-mandated formula.

### Controls and control assessment
NIST SP 800-53 and CIS Controls provide different control structures and levels of prescription. Select and tailor controls based on context, risk, obligations, and scope. Record the source and version used for each mapping.

### Technical testing
NIST SP 800-115 and OWASP testing resources can inform assessment planning and test design. Technical activities must remain within written authorization and approved scope. Testing guidance does not itself grant authorization.

### Incident response
NIST SP 800-61 Rev. 3 can inform future incident-response material. Incident response is related to, but distinct from, routine risk assessment or configuration review.

## Reference maintenance procedure

1. Visit the publisher's official page.
2. Verify title, edition/version, publication date, current status, and any amendment or superseding publication.
3. Update the table and record the verification date in the commit or changelog.
4. Replace superseded references only after checking whether older editions remain operationally relevant.
5. Do not copy substantial copyrighted text into this repository.
6. Check publisher terms before reproducing figures, tables, control text, or mappings.

## Intellectual property and disclaimer

Names of standards and frameworks are used for identification and reference. All rights in third-party publications remain with their respective owners. This register is an independent index and is not an official publication of, or endorsed by, the referenced organizations.

The list is not exhaustive. Inclusion does not constitute legal, regulatory, audit, or certification advice.
