---
document_title: Enterprise Cybersecurity Risk Assessment Case Study
document_id: ERACS-001
version: 1.0
status: Illustrative worked example
classification: Public portfolio example
owner: Framework maintainer
---

# Enterprise Cybersecurity Risk Assessment Case Study

> **Status and use:** This is a fictional, illustrative case study created to demonstrate application of the repository's risk assessment methodology, risk scoring model, risk register and evidence-handling practices. All organization names, assets, systems, events, values, evidence identifiers and decisions are invented. They are not findings about a real organization.
>
> **Important:** The numerical rating bands shown below are the illustrative bands in this framework's `risk-scoring-model.md`. They are not universal thresholds. An adopting organization must approve its own scales, appetite, tolerance, escalation criteria and delegated authorities before operational use.

## 1. Executive summary

Northstar Services (fictional) is a medium-sized enterprise providing customer account services through a public-facing web portal and supporting internal business systems. The assessment considers a defined set of internet-facing and supporting assets, identity services, customer information, backups and security monitoring.

The case study identifies five scenario-based risks:

1. Compromise of a public-facing application leading to unauthorized access to customer information.
2. Compromise of privileged identity credentials leading to broad enterprise access.
3. Ransomware or destructive malware disrupting critical services and recovery.
4. Exploitation of an unpatched internet-facing server.
5. Delayed detection and response due to incomplete security logging.

Using the framework's illustrative 5 × 5 model, the initial portfolio contains one Critical, three High and one Moderate current risk. These ratings are decision aids, not precise measurements of loss or probability. They must be interpreted with scenario context, evidence confidence, criticality, obligations and governance criteria.

The case study demonstrates the distinction between inherent risk, current residual risk after evidenced existing controls, and forecast target residual risk after planned treatment. Planned controls are not credited as current controls. No residual-risk acceptance is implied by the example.

## 2. Business context and assessment mandate

### 2.1 Organization profile

| Attribute | Fictional case-study context |
|---|---|
| Organization | Northstar Services |
| Industry | Business-to-business customer account services |
| Size | Medium-sized enterprise |
| Operating model | Hybrid on-premises and cloud-hosted services |
| Primary business service | Customer account portal and supporting operations |
| Data handled | Customer contact details, account records and service transaction metadata |
| Critical dependencies | Identity provider, public web tier, application services, database, network edge, backup platform and security monitoring |
| Assessment period | Illustrative assessment performed during September 2026 |
| Risk horizon | One year for likelihood assessments |
| Assessment type | Enterprise cyber risk assessment supported by technical control review |

### 2.2 Assessment objectives

- Identify material cybersecurity risk scenarios affecting defined business services and information.
- Evaluate inherent risk before crediting existing controls.
- Assess design, implementation and operating effectiveness of relevant existing controls.
- Estimate current residual risk using evidence-supported control effects.
- Define treatment options, accountable owners, milestones and verification requirements.
- Communicate material exposure and decisions to management.

### 2.3 Authorization and governance assumptions

For this fictional example, assume written authorization, scope, rules of engagement, system-owner participation and evidence-handling arrangements were approved before assessment activity. In a real engagement, reference the actual authorization and scope records.

The following roles are illustrative and must be mapped to the adopting organization's governance structure:

| Role | Responsibility in this case study |
|---|---|
| Executive risk sponsor | Provides executive oversight and resolves escalated decisions |
| Business service owner | Owns business-service context and operational priorities |
| Risk owner | Accountable for managing an assigned risk and obtaining decisions |
| Control owner | Operates and evidences relevant controls |
| Assessment lead | Coordinates assessment, analysis and reporting |
| Evidence custodian | Maintains evidence registration, access and retention records |
| Risk committee | Reviews risks or acceptance decisions beyond delegated authority |

## 3. Scope, assets and assumptions

### 3.1 In-scope assets and processes

| Asset ID | Fictional asset / service | Business role | Information / dependency | Criticality |
|---|---|---|---|---|
| NS-WEB-01 | Public web portal | Customer access channel | Customer account information; internet exposure | High |
| NS-APP-01 | Application service tier | Business logic and transactions | Web tier, identity and database dependencies | High |
| NS-DB-01 | Customer database | Stores account and transaction records | Application tier; backup platform | Critical |
| NS-ID-01 | Enterprise identity service | Workforce authentication and privileged access | Directory, MFA and administrative accounts | Critical |
| NS-EDGE-01 | Internet edge and firewall service | Network boundary and traffic control | Public portal and remote administration | High |
| NS-BKP-01 | Backup and recovery platform | Recovery of critical services and data | Identity, storage and network dependencies | Critical |
| NS-SIEM-01 | Central logging and monitoring service | Security telemetry, alerting and investigation | Logs from identity, edge, servers and applications | High |
| NS-END-01 | Managed workforce endpoints | User access and administrative workstations | Identity, endpoint protection and business data | Medium |

### 3.2 Scope boundaries

**Included:** listed assets and their material security dependencies; identity and privileged access; vulnerability and patch management; application and database security; logging and monitoring; backup resilience; relevant third-party dependencies.

**Excluded:** physical security, detailed privacy impact assessment, full source-code audit, penetration testing beyond the assumed approved test scope, and independent assurance of every supplier. Exclusions are not evidence that these areas are secure.

### 3.3 Assumptions and limitations

- The environment and control descriptions are fictional and intentionally simplified.
- Evidence references are illustrative identifiers, not actual files.
- No actual exploit, compromise, data loss or outage is asserted to have occurred.
- Likelihood ratings use a one-year horizon, consistent with the framework model's default.
- Likelihood and impact are assessed using the five-level scales in `docs/methodology/risk-scoring-model.md`.
- Overall impact uses the highest credible impact dimension, not an average that could conceal a severe consequence.
- The illustrative rating mapping is Low 1–4, Moderate 5–9, High 10–16 and Critical 17–25.
- Risk appetite, tolerance, escalation thresholds and approval authorities are not defined by this case study. They must be approved by the adopting organization.
- The case study does not claim compliance with any law, regulation, contract or security standard.

## 4. Assessment method and scoring conventions

### 4.1 Process

1. Establish context, scope, assets, dependencies and assessment horizon.
2. Define distinct cause-event-consequence risk scenarios.
3. Assess inherent likelihood and impact before crediting existing controls.
4. Identify relevant controls and evaluate design, implementation and operating effectiveness.
5. Assess current residual likelihood and impact based only on supported control effects.
6. Calculate scores and apply the illustrative rating bands.
7. Record confidence, assumptions, evidence gaps and any escalation considerations.
8. Select treatment strategies and define measurable actions.
9. Forecast target residual risk only after specifying planned treatment and verification assumptions.
10. Assign ownership, review triggers and governance decisions.

### 4.2 Scoring model

**Score = Likelihood × Impact**

Likelihood and impact each use levels 1–5. The illustrative rating bands are:

| Score | Illustrative rating |
|---:|---|
| 1–4 | Low |
| 5–9 | Moderate |
| 10–16 | High |
| 17–25 | Critical |

Likelihood scale:

| Level | Label | Interpretation within the stated one-year horizon |
|---:|---|---|
| 1 | Rare | Exceptional under the defined scenario and context |
| 2 | Unlikely | Possible, but not expected |
| 3 | Possible | Credible occurrence |
| 4 | Likely | Expected or repeatedly plausible |
| 5 | Almost certain | Expected to occur or occurring frequently |

Impact scale:

| Level | Label | General interpretation |
|---:|---|---|
| 1 | Negligible | Minimal, localized and readily recoverable |
| 2 | Minor | Limited adverse effect manageable through routine response |
| 3 | Moderate | Material but manageable disruption, loss or harm |
| 4 | Major | Serious disruption, substantial loss or significant harm |
| 5 | Severe | Extensive or critical consequences, potentially affecting critical objectives |

### 4.3 Interpretation rules

- Inherent risk is assessed before crediting existing controls.
- Current residual risk reflects only relevant existing controls with evidence of design, implementation and operating effectiveness.
- Do not mechanically subtract points or apply a percentage reduction to represent control effectiveness.
- A control may affect likelihood, impact, both or neither; explain the scenario-specific effect.
- Planned controls are not credited in current residual risk.
- Target residual risk is a forecast, not a current-state assertion.
- Confidence is recorded separately from the score.
- A severe credible impact, legal/contractual obligation or other approved criterion may require escalation even when the numerical score is lower. Preserve the calculated score and document the escalation or authorized override separately.
- A score does not determine acceptability. Acceptance requires a risk owner, rationale and approval within delegated authority.

## 5. Risk scenario register — portfolio view

| Risk ID | Scenario title | Category | Risk owner (role) | Inherent L×I | Current L×I | Current rating | Target L×I (forecast) | Treatment | Status |
|---|---|---|---|---:|---:|---|---:|---|---|
| NS-RISK-001 | Public application compromise exposes customer information | Application / data | Head of Applications | 4×5=20 | 3×5=15 | High | 2×5=10 | Mitigate | Treatment proposed |
| NS-RISK-002 | Privileged identity compromise enables enterprise-wide access | Identity / access | Head of IT Operations | 4×5=20 | 4×5=20 | Critical | 2×5=10 | Mitigate | Treatment proposed |
| NS-RISK-003 | Ransomware disrupts critical services and recovery | Resilience / malware | Infrastructure Manager | 4×5=20 | 3×5=15 | High | 2×5=10 | Mitigate | Treatment proposed |
| NS-RISK-004 | Exploitation of unpatched internet-facing server | Vulnerability / infrastructure | Infrastructure Manager | 4×4=16 | 3×4=12 | High | 2×4=8 | Mitigate | Treatment proposed |
| NS-RISK-005 | Incomplete telemetry delays detection and response | Monitoring / operations | SOC Manager | 3×4=12 | 3×3=9 | Moderate | 2×3=6 | Mitigate | Treatment proposed |

**Portfolio interpretation:** NS-RISK-002 is the highest current numerical risk. NS-RISK-001 and NS-RISK-003 remain High because the credible impact remains Severe even after the current controls are considered. NS-RISK-005 has a Moderate calculated rating, but management may still prioritize it based on dependencies with incident detection and response. These are illustrative prioritization judgments, not universal decisions.

## 6. Detailed risk assessments

### 6.1 NS-RISK-001 — Public application compromise exposes customer information

**Risk statement:** Because the public web portal and application tier are exposed to untrusted networks and contain application-level weaknesses, an attacker may exploit an application flaw or compromised session to access customer records, resulting in unauthorized disclosure, customer harm, response costs and potential contractual or regulatory consequences.

**Scope and affected assets:** NS-WEB-01, NS-APP-01 and NS-DB-01.

**Threat and event path:** An external attacker identifies an application weakness, bypasses or abuses an application control, obtains unauthorized application or database access, and extracts customer information.

**Impact analysis:**

| Dimension | Credible consequence | Assessed impact |
|---|---|---:|
| Confidentiality | Unauthorized disclosure of customer account records | 5 — Severe |
| Integrity | Potential unauthorized modification of customer records | 4 — Major |
| Availability | Potential service interruption during containment and recovery | 3 — Moderate |
| Financial / legal / contractual | Investigation, notification, response cost and potential obligations | 4 — Major |
| Reputation | Loss of customer and partner trust | 4 — Major |

Overall impact is 5 because the highest credible impact dimension is Severe. The case study does not assume a particular statutory threshold or monetary loss.

**Likelihood rationale:** The public attack surface and assumed application weakness make the scenario credible. Existing controls reduce exposure but do not eliminate application-layer exploitation paths.

**Existing controls and evidence:**

| Control | Design | Implementation | Operating evidence | Limitation |
|---|---|---|---|---|
| Edge web filtering | Partial | Implemented | EVD-001: sample rule review | Does not reliably prevent all application-layer abuse |
| Secure development review | Partial | Partial | EVD-002: sample review records | Coverage and remediation tracking incomplete |
| Database access restriction | Adequate | Implemented | EVD-003: access configuration review | Does not prevent all abuse through the application service identity |
| Central application logging | Partial | Partial | EVD-004: sample log review | Security-relevant events are not consistently captured |

**Scoring:**

| State | Likelihood | Impact | Score | Rating | Rationale |
|---|---:|---:|---:|---|---|
| Inherent | 4 | 5 | 20 | Critical | Public exposure and credible severe data consequence before controls |
| Current residual | 3 | 5 | 15 | High | Existing edge and database controls reduce likelihood, not the credible worst impact |
| Target residual (forecast) | 2 | 5 | 10 | High | Proposed application assurance and access improvements may reduce likelihood; impact remains severe |

**Confidence:** Medium. The example assumes representative configuration and review evidence but does not include a full independent source-code assessment or validated exploitation test.

**Treatment:** Mitigate.

| Action | Required outcome | Owner | Priority | Target date (illustrative) | Verification evidence |
|---|---|---|---|---|---|
| NS-ACT-001 | Complete risk-based application security testing and remediate validated high-risk defects | Head of Applications | High | 2026-11-30 | Retest results and finding closure records |
| NS-ACT-002 | Review application service identity permissions and reduce database privileges | Database Manager | High | 2026-11-20 | Approved access review and configuration evidence |
| NS-ACT-003 | Implement security logging for authentication, authorization and sensitive data access events | SOC Manager / Applications | High | 2026-12-15 | Log test records and SIEM validation |
| NS-ACT-004 | Establish release security gates and tracked exception approval | Head of Applications | Medium | 2027-01-15 | Pipeline/configuration evidence and approved procedure |

**Residual-risk decision:** No acceptance is recorded. The target rating is forecast only and must be recalculated after implementation and effectiveness verification.

### 6.2 NS-RISK-002 — Privileged identity compromise enables enterprise-wide access

**Risk statement:** Because privileged accounts provide broad access to identity, server and security administration functions and the assumed privileged-access controls are incomplete, an attacker may compromise a privileged credential or session, resulting in enterprise-wide unauthorized access, persistence, data compromise and disruption of critical services.

**Scope and affected assets:** NS-ID-01, NS-END-01, NS-APP-01, NS-DB-01, NS-BKP-01 and administrative interfaces.

**Threat and event path:** Credential theft, phishing, endpoint compromise or session theft leads to privileged account use; insufficient separation or monitoring allows lateral movement and administrative control.

**Impact analysis:**

| Dimension | Credible consequence | Assessed impact |
|---|---|---:|
| Confidentiality | Broad access to sensitive business and customer information | 5 — Severe |
| Integrity | Unauthorized changes to identity, infrastructure and business systems | 5 — Severe |
| Availability | Disabling systems, identity services or backups | 5 — Severe |
| Operational continuity | Disruption across multiple critical services | 5 — Severe |
| Financial / legal / contractual | Potentially extensive response and recovery obligations | 4 — Major |

Overall impact is 5 — Severe.

**Existing controls and evidence:**

| Control | Design | Implementation | Operating evidence | Limitation |
|---|---|---|---|---|
| Workforce MFA | Adequate for standard users | Implemented | EVD-005: identity policy review | Privileged and emergency paths are not fully covered |
| Privileged access review | Partial | Partial | EVD-006: sample access review | Review frequency and completeness are inconsistent |
| Administrative workstation controls | Partial | Partial | EVD-007: endpoint baseline sample | Not all privileged sessions originate from managed admin workstations |
| Privileged activity monitoring | Partial | Partial | EVD-008: sample event review | Alert coverage and response linkage are incomplete |

**Scoring:**

| State | Likelihood | Impact | Score | Rating | Rationale |
|---|---:|---:|---:|---|---|
| Inherent | 4 | 5 | 20 | Critical | Privileged compromise has a credible enterprise-wide severe consequence |
| Current residual | 4 | 5 | 20 | Critical | Existing controls do not sufficiently reduce likelihood; impact remains severe |
| Target residual (forecast) | 2 | 5 | 10 | High | Phishing-resistant MFA, privileged access management and monitoring may reduce likelihood; impact remains severe |

**Confidence:** Medium-Low. The example assumes incomplete privileged access evidence and unknown coverage in some administrative paths. The uncertainty itself warrants management attention.

**Treatment:** Mitigate; escalate for executive oversight under the organization's approved governance criteria.

| Action | Required outcome | Owner | Priority | Target date (illustrative) | Verification evidence |
|---|---|---|---|---|---|
| NS-ACT-005 | Enforce phishing-resistant MFA for privileged access, including remote and emergency paths where technically feasible | Head of IT Operations | Critical | 2026-11-15 | Authentication policy and test evidence |
| NS-ACT-006 | Implement privileged access management, just-in-time elevation and session accountability | Head of IT Operations | Critical | 2027-01-31 | PAM configuration and sampled session records |
| NS-ACT-007 | Establish dedicated administrative workstations and restrict privileged logon paths | Infrastructure Manager | High | 2026-12-15 | Endpoint and identity policy evidence |
| NS-ACT-008 | Reconcile privileged identities, service accounts and emergency accounts; assign owners and review cadence | Identity Manager | Critical | 2026-11-20 | Approved inventory and access review |
| NS-ACT-009 | Implement alerting for privileged group changes, unusual administrative activity and authentication anomalies | SOC Manager | High | 2026-12-15 | SIEM use-case tests and alert records |

**Residual-risk decision:** Current Critical risk must be escalated to the designated authority. The case study does not assert acceptance. Any temporary exception must have a documented owner, rationale, compensating measures, expiry and approval.

### 6.3 NS-RISK-003 — Ransomware disrupts critical services and recovery

**Risk statement:** Because workforce endpoints and critical infrastructure depend on shared identity and network services, and backup isolation and restoration assurance are assumed incomplete, ransomware or destructive malware may spread to critical systems and impair recovery, resulting in prolonged service disruption, data loss and substantial recovery effort.

**Scope and affected assets:** NS-END-01, NS-ID-01, NS-APP-01, NS-DB-01 and NS-BKP-01.

**Threat and event path:** Initial access through a compromised endpoint or account leads to execution and lateral movement; shared administrative paths or accessible backup services increase the potential impact.

**Impact analysis:**

| Dimension | Credible consequence | Assessed impact |
|---|---|---:|
| Availability | Prolonged outage of critical customer and internal services | 5 — Severe |
| Integrity | Loss of confidence in system and backup integrity | 4 — Major |
| Confidentiality | Potential data theft before encryption | 4 — Major |
| Operational continuity | Disruption to customer service and business operations | 5 — Severe |
| Financial | Recovery, downtime and response costs | 4 — Major |

Overall impact is 5 — Severe.

**Existing controls and evidence:**

| Control | Design | Implementation | Operating evidence | Limitation |
|---|---|---|---|---|
| Endpoint protection | Adequate | Implemented | EVD-009: endpoint policy sample | Coverage and tamper-protection exceptions require validation |
| Network segmentation | Partial | Implemented | EVD-010: network rule review | Administrative and backup paths are not fully isolated |
| Backup schedule | Adequate | Implemented | EVD-011: backup job reports | Successful jobs do not prove recoverability |
| Restore testing | Partial | Partial | EVD-012: sample restore record | Coverage and business-service recovery testing are incomplete |

**Scoring:**

| State | Likelihood | Impact | Score | Rating | Rationale |
|---|---:|---:|---:|---|---|
| Inherent | 4 | 5 | 20 | Critical | Credible malware event with severe service and recovery consequences |
| Current residual | 3 | 5 | 15 | High | Endpoint protection and backups reduce likelihood, but isolation and restoration evidence are incomplete |
| Target residual (forecast) | 2 | 5 | 10 | High | Segmentation, protected backups and tested recovery may reduce likelihood; severe impact remains credible |

**Confidence:** Medium. Backup job records exist in the fictional scenario, but they do not establish complete restoration capability.

**Treatment:** Mitigate.

| Action | Required outcome | Owner | Priority | Target date (illustrative) | Verification evidence |
|---|---|---|---|---|---|
| NS-ACT-010 | Separate backup administration and storage from standard enterprise identity and network paths | Infrastructure Manager | Critical | 2026-12-15 | Architecture, access and network test evidence |
| NS-ACT-011 | Implement immutable or offline protected copies appropriate to recovery objectives | Backup Service Owner | High | 2026-12-31 | Configuration and immutability verification |
| NS-ACT-012 | Conduct restore tests for critical applications and databases against approved recovery objectives | Business Continuity Lead | High | 2027-01-15 | Restore test report and business-owner sign-off |
| NS-ACT-013 | Validate endpoint protection coverage, tamper protection and alert handling | Endpoint Manager | High | 2026-11-30 | Coverage report and controlled test evidence |
| NS-ACT-014 | Exercise ransomware response and recovery coordination | Incident Response Lead | Medium | 2027-02-15 | Exercise report and tracked improvement actions |

**Residual-risk decision:** No acceptance is recorded. Reassess impact and likelihood after recovery exercises and control validation; do not reduce the impact score merely because backups exist.

### 6.4 NS-RISK-004 — Exploitation of an unpatched internet-facing server

**Risk statement:** Because an internet-facing server may remain exposed to a known exploitable vulnerability beyond the organization's intended remediation period, an attacker may exploit the weakness to gain unauthorized access or disrupt the hosted service, resulting in compromise, service interruption and potential pivoting into connected systems.

**Scope and affected assets:** NS-WEB-01 and supporting server infrastructure.

**Impact analysis:**

| Dimension | Credible consequence | Assessed impact |
|---|---|---:|
| Confidentiality | Access to application data or credentials available to the server | 4 — Major |
| Integrity | Unauthorized changes to hosted content or server configuration | 4 — Major |
| Availability | Service disruption or server outage | 4 — Major |
| Operational / financial | Incident response, restoration and customer service disruption | 3 — Moderate |

Overall impact is 4 — Major.

**Existing controls and evidence:**

| Control | Design | Implementation | Operating evidence | Limitation |
|---|---|---|---|---|
| Vulnerability scanning | Adequate | Implemented | EVD-013: scan output | Scan cadence and asset coverage are not fully reconciled |
| Patch management | Partial | Implemented | EVD-014: patch status sample | Exceptions and remediation aging require improvement |
| Edge filtering | Partial | Implemented | EVD-015: firewall rule review | Does not eliminate exploitation of exposed service flaws |

**Scoring:**

| State | Likelihood | Impact | Score | Rating | Rationale |
|---|---:|---:|---:|---|---|
| Inherent | 4 | 4 | 16 | High | Internet exposure and an exploitable weakness create a credible path |
| Current residual | 3 | 4 | 12 | High | Scanning and edge controls reduce exposure but patch governance remains incomplete |
| Target residual (forecast) | 2 | 4 | 8 | Moderate | Timely remediation, verified asset coverage and exception governance may reduce likelihood |

**Confidence:** Medium. The example assumes scan and patch records are representative but not fully reconciled.

**Treatment:** Mitigate.

| Action | Required outcome | Owner | Priority | Target date (illustrative) | Verification evidence |
|---|---|---|---|---|---|
| NS-ACT-015 | Validate affected asset and vulnerability exposure; apply vendor-supported remediation or approved compensating controls | Infrastructure Manager | High | 2026-11-10 | Rescan and configuration evidence |
| NS-ACT-016 | Reconcile vulnerability scan coverage against the authoritative asset inventory | Vulnerability Management Lead | High | 2026-11-20 | Coverage reconciliation |
| NS-ACT-017 | Establish risk-based remediation SLAs and documented exception approvals | CISO / Risk Governance | High | 2026-12-01 | Approved policy and exception records |

**Residual-risk decision:** Target Moderate is a forecast only. Any remediation deadline or SLA must come from approved organizational policy and applicable obligations; the dates above are fictional planning assumptions.

### 6.5 NS-RISK-005 — Incomplete telemetry delays detection and response

**Risk statement:** Because security-relevant events from identity, application and infrastructure systems are not consistently collected, normalized or alerted on, malicious activity may remain undetected for an extended period, increasing the scale and duration of compromise and delaying containment and recovery.

**Scope and affected assets:** NS-SIEM-01 and telemetry sources across NS-ID-01, NS-WEB-01, NS-APP-01, NS-DB-01 and NS-EDGE-01.

**Impact analysis:**

| Dimension | Credible consequence | Assessed impact |
|---|---|---:|
| Operational | Delayed triage and containment, increasing incident duration | 3 — Moderate |
| Confidentiality / integrity | Greater extent of compromise before detection | 4 — Major |
| Availability | Longer disruption if destructive activity is not detected | 4 — Major |
| Legal / contractual | Potential inability to investigate or demonstrate required monitoring | 3 — Moderate |

Overall impact is 4 — Major.

**Existing controls and evidence:**

| Control | Design | Implementation | Operating evidence | Limitation |
|---|---|---|---|---|
| Central SIEM | Adequate | Implemented | EVD-016: source inventory | Several important sources have incomplete coverage |
| Alert triage | Partial | Implemented | EVD-017: ticket sample | Use-case coverage and response timing are inconsistent |
| Log retention | Partial | Partial | EVD-018: retention configuration | Retention and integrity vary by source |

**Scoring:**

| State | Likelihood | Impact | Score | Rating | Rationale |
|---|---:|---:|---:|---|---|
| Inherent | 3 | 4 | 12 | High | Without reliable telemetry, detection delay is a credible consequence of security events |
| Current residual | 3 | 3 | 9 | Moderate | Existing SIEM and triage provide some detection capability and reduce expected operational impact, but gaps remain |
| Target residual (forecast) | 2 | 3 | 6 | Moderate | Source coverage and tested detection use cases may reduce likelihood of prolonged undetected activity |

**Confidence:** Medium. The scenario assumes partial source coverage and sampled operational records; full detection engineering effectiveness is not established.

**Treatment:** Mitigate.

| Action | Required outcome | Owner | Priority | Target date (illustrative) | Verification evidence |
|---|---|---|---|---|---|
| NS-ACT-018 | Define critical log-source requirements and reconcile them against deployed telemetry | SOC Manager | High | 2026-11-20 | Approved source matrix and SIEM status |
| NS-ACT-019 | Implement and test detection use cases for privileged changes, suspicious authentication and critical system events | SOC Manager | High | 2026-12-20 | Controlled test results and alert tickets |
| NS-ACT-020 | Define log retention, time synchronization, access and integrity requirements by source | Security Architect | Medium | 2027-01-15 | Approved standard and configuration evidence |

**Residual-risk decision:** No acceptance is recorded. Management may prioritize this risk because it affects detection and response across the broader risk portfolio.

## 7. Portfolio prioritization and management decisions

### 7.1 Current risk priorities

| Priority order (illustrative) | Risk ID | Current rating | Primary driver | Management attention |
|---:|---|---|---|---|
| 1 | NS-RISK-002 | Critical | Enterprise-wide privileged access compromise | Immediate executive oversight and treatment tracking |
| 2 | NS-RISK-001 | High | Severe customer information exposure | Application security and data access treatment |
| 3 | NS-RISK-003 | High | Critical service disruption and uncertain recovery | Backup isolation and restore assurance |
| 4 | NS-RISK-004 | High | Exploitable internet-facing exposure | Validate and remediate affected assets |
| 5 | NS-RISK-005 | Moderate | Detection and response coverage gaps | Improve telemetry; consider dependency-based priority |

This ordering is an example of management prioritization. An organization may change action order based on active exploitation, time-sensitive exposure, critical dependencies, legal obligations, incident intelligence or other approved criteria. Record the rationale.

### 7.2 Decisions required from management

1. Confirm risk owners and control owners for all five scenarios.
2. Direct immediate governance review of NS-RISK-002.
3. Approve or challenge proposed treatment plans and resource requirements.
4. Confirm remediation priorities and target dates against approved organizational policy.
5. Decide whether any risk requires temporary exception handling; do not infer acceptance from this case study.
6. Require evidence-based verification before changing current residual ratings.
7. Confirm appetite, tolerance, escalation thresholds and delegated authorities if not already approved.

### 7.3 Illustrative executive dashboard

| Measure | Case-study result |
|---|---:|
| Risks assessed | 5 |
| Current Critical | 1 |
| Current High | 3 |
| Current Moderate | 1 |
| Current Low | 0 |
| Risks with treatment proposed | 5 |
| Risks formally accepted | 0 |
| Risks requiring executive escalation | At least 1, subject to approved governance criteria |
| Evidence confidence | Medium to Medium-Low across scenarios |

Do not interpret this small fictional sample as a statistically meaningful enterprise risk distribution.

## 8. Evidence and traceability register

The following evidence identifiers are illustrative. They show how evidence should link to risk analysis without embedding sensitive artifacts in the case study.

| Evidence ID | Fictional evidence description | Source / method | Related risks | Quality limitation |
|---|---|---|---|---|
| EVD-001 | Web filtering rule review | Authorized configuration review | NS-RISK-001 | Sampled rules only |
| EVD-002 | Secure development review records | Process and ticket review | NS-RISK-001 | Coverage incomplete |
| EVD-003 | Database access configuration review | Read-only configuration inspection | NS-RISK-001 | Does not prove all runtime access paths |
| EVD-004 | Application logging sample | Approved log review | NS-RISK-001 | Partial event coverage |
| EVD-005 | Workforce MFA policy review | Identity configuration review | NS-RISK-002 | Privileged paths not fully covered |
| EVD-006 | Privileged access review sample | Access certification records | NS-RISK-002 | Inconsistent review coverage |
| EVD-007 | Administrative endpoint baseline sample | Endpoint configuration review | NS-RISK-002 | Not all admin endpoints assessed |
| EVD-008 | Privileged activity event sample | SIEM review | NS-RISK-002 | Alert coverage incomplete |
| EVD-009 | Endpoint protection policy sample | Endpoint management console | NS-RISK-003 | Coverage exceptions require validation |
| EVD-010 | Network segmentation rule review | Network configuration review | NS-RISK-003 | Some administrative paths not tested |
| EVD-011 | Backup job status reports | Backup platform export | NS-RISK-003 | Job success does not prove restoration |
| EVD-012 | Sample restoration record | Controlled restore test record | NS-RISK-003 | Limited application coverage |
| EVD-013 | Vulnerability scan output | Authorized vulnerability scan | NS-RISK-004 | Asset coverage not fully reconciled |
| EVD-014 | Patch status sample | Configuration / patch management review | NS-RISK-004 | Exceptions and aging require reconciliation |
| EVD-015 | Firewall rule review | Authorized configuration review | NS-RISK-004 | Filtering is not a substitute for patching |
| EVD-016 | SIEM source inventory | SIEM configuration export | NS-RISK-005 | Inventory completeness requires owner validation |
| EVD-017 | Alert triage ticket sample | SOC workflow review | NS-RISK-005 | Sample may not represent all shifts or event types |
| EVD-018 | Log retention configuration sample | Logging platform review | NS-RISK-005 | Source-specific variation remains |

For a real assessment, each evidence object should have a corresponding entry in the Evidence Register and, where needed, a Collection Record, Validation Review, Access/Disclosure Record or Chain-of-Custody Record. Record SHA-256 for applicable file objects and preserve the digest, tool, version and timestamp. A matching hash supports integrity comparison; it does not prove source authenticity or completeness.

## 9. Risk treatment roadmap

The roadmap below consolidates actions by time horizon for management tracking. Dates are illustrative and must be replaced with dates approved by the adopting organization.

| Horizon | Focus | Key actions | Accountable coordination |
|---|---|---|---|
| First 30 days | Reduce immediate exposure | Validate internet-facing vulnerability; privileged account inventory; confirm critical log-source gaps; assign risk owners | Assessment lead and relevant control owners |
| 31–60 days | Strengthen foundational controls | Privileged MFA coverage; patch governance; application access review; backup isolation design | IT Operations and Applications |
| 61–90 days | Validate operating effectiveness | PAM implementation milestones; application security retesting; SIEM use-case testing; restore exercises | Control owners and independent reviewers |
| 90+ days | Sustain and improve | Periodic access certification; continuous vulnerability coverage; recurring recovery exercises; risk reassessment | Risk owners and governance forum |

## 10. Residual-risk reassessment and closure criteria

Do not mark a risk closed merely because an action is reported complete. The risk owner and assessor should verify that:

- The planned control or action has been implemented.
- Design, implementation and operating effectiveness have been evaluated as appropriate.
- Evidence is registered, validated and linked to the action and risk.
- The scenario, likelihood and impact have been reassessed.
- Current residual risk is recalculated using the approved model.
- Remaining uncertainty, dependencies and evidence gaps are recorded.
- Any required acceptance is explicit, current and approved by the correct authority.
- Follow-up monitoring and review triggers are assigned.

Reassess when there is a material system or business change, new threat information, a security incident, control degradation, significant vulnerability disclosure, overdue treatment, changed obligation or new evidence that could alter the scenario.

## 11. Assumptions, limitations and quality review

### 11.1 Limitations

- All facts and evidence are fictional and are used only to demonstrate method.
- The case study does not establish that Northstar Services or any similar organization has these risks.
- Scores are semi-quantitative and depend on scenario definition, assessment horizon, organizational calibration and evidence quality.
- The illustrative rating bands are not an approved risk appetite or acceptance policy.
- Target residual ratings are forecasts and must not be reported as achieved results.
- The example does not determine legal notification obligations or prescribe regulatory interpretations.
- Treatment dates and priority labels are fictional planning examples, not universal remediation SLAs.

### 11.2 Quality review checklist

- [ ] Each risk is expressed as cause, event and consequence.
- [ ] Scope, affected assets, dependencies and one-year horizon are stated.
- [ ] Inherent risk is assessed before crediting existing controls.
- [ ] Existing controls are evaluated for design, implementation and operating effectiveness.
- [ ] Control credit is evidence-supported and not mechanically deducted.
- [ ] Overall impact uses the highest credible impact dimension.
- [ ] Arithmetic and illustrative rating bands are applied consistently.
- [ ] Confidence, assumptions and evidence limitations are separate from the score.
- [ ] Planned controls are not represented as existing controls.
- [ ] Target residual ratings are clearly labeled as forecasts.
- [ ] Treatment actions have owners, outcomes, dates and verification evidence.
- [ ] Acceptance and escalation are not implied; required decisions are explicitly authorized.
- [ ] Evidence IDs map to a controlled evidence register.
- [ ] Sensitive evidence and secrets are not embedded in the report.
- [ ] Review triggers and closure criteria are defined.

## 12. Related framework documents

Paths below are repository-relative:

- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/methodology/assessment-lifecycle.md`
- `templates/risk-register-template.md`
- `templates/evidence-register-template.md`
- `templates/technical-assessment-checklist.md`
- `templates/assessment-report-template.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`

## 13. Document control

| Field | Value |
|---|---|
| Document ID | ERACS-001 |
| Version | 1.0 |
| Status | Illustrative worked example |
| Owner | Framework maintainer |
| Approval | Not an organizational risk approval |
| Review trigger | Material changes to linked framework methodology or scoring model |
| Last updated | 2026-10-31 |
