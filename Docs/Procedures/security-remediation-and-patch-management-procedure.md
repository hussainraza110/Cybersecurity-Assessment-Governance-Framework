# Security Remediation and Patch Management Procedure

## Document Control

| Field | Value |
|---|---|
| Document title | Security Remediation and Patch Management Procedure |
| Document identifier | PROC-SEC-REMED-001 |
| Version | 1.0 |
| Document owner | Information Security |
| Approving authority | [Insert approving authority] |
| Classification | [Insert classification] |
| Effective date | [Insert date] |
| Review frequency | At least annually and following material change |
| Status | Draft template pending organizational approval |

> **Implementation note:** This organization-neutral template must be tailored and approved before adoption. Assign actual roles, approval authorities, service levels, maintenance windows, technical standards and retention periods. Align risk ratings and target dates with the organization's approved risk appetite and governance requirements.

## 1. Purpose

This procedure establishes a controlled, risk-based and auditable process for remediating security vulnerabilities and managing security-related patches and corrective actions. It defines the activities required to receive, assess, prioritize, assign, plan, implement, verify and close remediation work.

It is intended to ensure that findings have accountable owners; priorities reflect technical and business risk; patches and corrective changes are deployed safely; testing, approvals and recovery safeguards are proportionate; failed, delayed or unavailable remediation is managed explicitly; exceptions are documented and reviewed; and closure is supported by evidence.

## 2. Scope

This procedure applies to security remediation affecting organization-owned, managed or formally authorized information systems and technology services, including:

- physical and virtual servers;
- workstations, laptops and other endpoints;
- network and security appliances;
- operating systems and middleware;
- databases and database platforms;
- business applications, web applications and APIs;
- containers, orchestration platforms and virtualization infrastructure;
- cloud services, hosted environments and platform services;
- firmware, device software and embedded systems; and
- third-party technology or managed services where remediation responsibilities are contractually defined.

It covers remediation arising from vulnerability assessments, penetration tests, security reviews, threat advisories, incident investigations, audit findings, vendor notifications and other approved sources.

This procedure does not replace the Security Assessment Authorization Procedure, Vulnerability Assessment Procedure, change management procedure, incident response procedures, secure development procedures or formal risk acceptance governance. Where another approved procedure imposes stricter requirements, the stricter requirement applies unless an authorized exception is documented.

## 3. Principles and Requirements

Once adopted, the following requirements apply:

1. **Accountability:** Every remediation item must have an assigned owner and an identified implementation function.
2. **Risk-based prioritization:** Priority must consider severity, exposure, exploitability, asset criticality, business impact and threat context.
3. **Controlled change:** Production remediation must follow approved change controls, including emergency change controls where applicable.
4. **Proportionate validation:** Testing and deployment safeguards must reflect the potential impact of failure and urgency of the exposure.
5. **Recoverability:** A rollback, recovery or failure-containment approach must be defined before implementation where technically feasible and proportionate.
6. **Evidence-based closure:** A deployment record or change ticket alone is insufficient evidence that a vulnerability has been remediated.
7. **Time-bound exceptions:** Deferrals and risk acceptances require an authorized decision, documented rationale, review date and expiry or reassessment condition.
8. **Traceability:** Records must link the originating finding, affected assets, change records, verification evidence and closure decision.
9. **No silent deferral:** Delayed, failed or technically unavailable remediation must be escalated and tracked.
10. **Separation of duties:** Where practicable, the person implementing a high-risk change should not be the sole person validating and approving closure.

## 4. Roles and Responsibilities

Map these functions to actual job titles and teams. One individual may perform multiple roles where segregation is impracticable, but conflicts must be identified and compensating review applied.

| Role | Core responsibilities |
|---|---|
| Information Security / Vulnerability Management | Maintains the process; receives and validates findings; coordinates prioritization; monitors overdue items; reviews evidence; challenges unsupported closure; reports status. |
| Vulnerability / Finding Owner | Maintains the finding record; coordinates triage; tracks decisions, dates, dependencies and evidence; escalates delays. |
| Asset / System Owner | Confirms ownership and business criticality; evaluates service impact; approves operational windows within authority; ensures remediation is planned and completed. |
| Technical Remediation Owner | Selects and implements patches or corrective actions; documents technical decisions, tests, deployment outcomes and rollback actions. |
| Patch / Platform Administrator | Executes approved patching; maintains deployment records; reports failures and coverage gaps. |
| Change Manager / Change Authority | Ensures changes are assessed, categorized, approved, scheduled and recorded. |
| Risk Owner | Evaluates residual risk and authorizes treatment or acceptance within delegated authority. |
| Security Reviewer | Reviews remediation design, compensating controls and verification evidence; assesses whether the exposure is adequately addressed. |
| Service / Business Owner | Confirms service requirements, operational constraints, business impact and acceptable disruption within authority. |
| Internal Audit / Assurance | Independently assesses process design, execution and evidence; does not own operational remediation. |

### 4.1 Accountability rules

- Each item must identify one accountable owner, even where several teams contribute.
- The asset owner remains accountable for ensuring remediation is addressed unless governance formally assigns accountability elsewhere.
- The technical remediation owner is accountable for accurate implementation records.
- Information Security monitors and challenges remediation; it does not automatically assume ownership of technical fixes.
- Risk acceptance must be approved by the designated risk owner or higher authority, not solely by the person implementing the fix.
- Where a third party performs remediation, the internal service or vendor owner must track the obligation and obtain adequate evidence.

## 5. Remediation Lifecycle

The standard lifecycle is:

1. Receive and register the finding.
2. Validate, consolidate and triage.
3. Assign ownership and determine priority.
4. Develop a remediation plan.
5. Assess patch or corrective-action suitability.
6. Obtain required change and deployment approvals.
7. Test and implement the remediation.
8. Verify the technical and security outcome.
9. Close, reopen, defer or escalate the item.
10. Monitor trends and reassess residual risk.

A finding may move between stages when new evidence, dependencies or technical constraints arise. The record must retain decision history and reasons for material changes.

## 6. Finding Receipt and Registration

### 6.1 Sources

Remediation items may originate from:
- vulnerability scanner results;
- penetration testing and security assessment reports;
- configuration and hardening reviews;
- vendor security advisories and product security bulletins;
- threat intelligence and known-exploited vulnerability notifications;
- incident response and forensic investigations;
- internal or external audits;
- security monitoring and operational alerts;
- application security testing and secure development reviews; and
- contractual, regulatory or management requirements.

### 6.2 Minimum registration information

The finding or remediation record must include, where available:

- unique finding or remediation identifier;
- source and source-reference identifier;
- date identified and date registered;
- affected asset identifiers, hostnames, applications or service names;
- asset owner and technical contact;
- vulnerability identifier, advisory reference or weakness description;
- affected software, component, version or configuration;
- finding description and technical evidence reference;
- initial severity and source score, if supplied;
- known exploit status and relevant threat context;
- business service and asset criticality;
- current exposure and relevant network or access conditions;
- proposed remediation or mitigation;
- assigned owner and target date;
- related risk, assessment, incident and change references; and
- current status and decision history.

Missing information must be recorded as unknown or pending validation, not silently assumed.

### 6.3 Duplicate and related findings

Information Security may consolidate duplicates representing the same underlying weakness and remediation action. Consolidation must preserve all affected assets, originating references, asset-specific risk differences, separate ownership or deployment dependencies, and the ability to report closure for each affected asset.

Do not merge similar findings if they require materially different fixes, risk decisions or verification.

## 7. Validation and Triage

Before prioritization, the finding owner and relevant technical owner must establish whether the finding is applicable and actionable.

Triage should consider:
- whether the affected asset or component exists and is in scope;
- whether the reported version or configuration is accurate;
- whether the vulnerability affects the deployed product, feature or configuration;
- whether the vulnerable component is reachable or otherwise exploitable;
- whether the finding is a duplicate, false positive or accepted limitation;
- whether the asset is internet-facing, externally reachable or exposed to untrusted networks;
- whether exploitation is known, observed or reasonably anticipated;
- whether the asset supports a critical business or safety-related service;
- whether a vendor fix, workaround or mitigation is available; and
- whether remediation could affect dependent services or data.

A finding must not be dismissed solely because exploitation has not been observed. A false-positive or not-applicable decision must include its technical basis and supporting evidence and be reviewed by an authorized security reviewer.

Where validation cannot be completed promptly, the item must remain open with an explicit uncertainty statement and an interim risk-based priority.

## 8. Risk-Based Prioritization and Remediation Targets

### 8.1 Prioritization factors

Use the organization's approved risk assessment methodology and scoring model. At minimum, consider:
- vulnerability severity and exploitability;
- availability and reliability of exploit techniques;
- known exploitation in the wild or credible threat intelligence;
- asset criticality and business service dependency;
- external exposure and attack surface;
- confidentiality, integrity and availability requirements;
- operational, financial, legal, regulatory and reputational impact;
- compensating controls and demonstrated effectiveness;
- number and distribution of affected assets;
- remediation feasibility, dependencies and deployment risk; and
- uncertainty or limitations in available evidence.

A vendor severity or CVSS score is an input, not a complete organizational risk decision. Priority must reflect organizational context.

### 8.2 Remediation target dates

The organization must define remediation target periods for risk categories in an approved service-level schedule or supporting standard. This procedure does not impose universal deadlines.

Target periods should distinguish, as appropriate:
- actively exploited or emergency vulnerabilities;
- critical and high-risk exposures;
- moderate and low-risk findings;
- externally exposed versus internally restricted assets;
- production versus non-production environments; and
- patch availability and technical feasibility.

Record the target date and its basis, along with any approved adjustment. A target date is a management control, not evidence that risk is acceptable until that date.

### 8.3 Priority escalation

Immediately escalate to designated security and business authorities when:
- active exploitation or credible imminent exploitation is identified;
- a critical service is materially exposed;
- a vulnerability creates a plausible path to major compromise;
- a high- or critical-risk target is likely to be missed;
- a required patch is unavailable or cannot be deployed safely;
- remediation causes material service degradation or control failure; or
- risk exceeds the assigned risk owner's authority.

Information Security may recommend emergency containment or remediation. Execution and risk decisions remain with authorized roles.

## 9. Patch Identification and Assessment

### 9.1 Sources of patch information

Technical owners should monitor relevant:
- vendor security advisories and product bulletins;
- operating system and application update channels;
- package and repository metadata;
- firmware and appliance advisories;
- vulnerability scanner intelligence;
- national or sectoral cybersecurity advisories;
- trusted threat intelligence sources; and
- third-party service-provider notifications.

The organization must identify authoritative sources for its technology and define who monitors them and how frequently.

### 9.2 Patch applicability

Before deployment, determine:
- whether the patch applies to the installed product, version and configuration;
- whether the asset is affected by the vulnerability;
- whether the patch is superseded, withdrawn or subject to known issues;
- whether prerequisites, dependencies or intermediate updates are required;
- whether the patch changes functionality, interfaces or security settings;
- whether a vendor workaround or mitigation exists;
- whether the patch is supported for the deployed platform; and
- whether the patch source and package integrity can be reasonably validated.

Use vendor-supported patch sources and approved repositories wherever possible. Untrusted packages or unofficial binaries must not be deployed without explicit security and technical approval.

### 9.3 Patch assessment decision

Record one of the following decisions:
- approved for testing and deployment;
- approved for direct or expedited deployment under an authorized emergency process;
- deferred pending testing or dependency resolution;
- not applicable, with technical justification;
- unavailable or unsupported, requiring alternative treatment; or
- rejected, with documented technical and risk rationale.

Patch availability does not automatically make deployment safe or appropriate for every asset. Operational inconvenience alone is not sufficient justification for indefinite deferral.

## 10. Remediation Planning

For each item, the technical owner must prepare a plan proportionate to risk and complexity.

The plan should identify:
- affected assets and environments;
- vulnerability or control gap to be addressed;
- selected patch, configuration change, code fix or other corrective action;
- technical implementation steps;
- prerequisites and dependencies;
- expected service impact and outage requirements;
- test scope and success criteria;
- backup, snapshot or recovery requirements, where appropriate;
- rollback or failure-containment procedure;
- implementation owner and supporting teams;
- change record and required approvals;
- proposed maintenance window;
- validation and post-deployment verification steps;
- communications and stakeholder notifications; and
- contingency measures if remediation fails.

For multi-asset deployments, define deployment waves or representative pilot groups where this reduces operational risk. A successful pilot is not proof that every asset has been remediated.

## 11. Testing and Compatibility

### 11.1 Test requirements

Testing must be proportionate to:
- criticality of the affected service;
- likelihood and impact of patch failure;
- complexity of the technology stack;
- extent of the change;
- availability of a representative test environment; and
- urgency of the security exposure.

Testing may include:
- installation and package validation;
- service startup and health checks;
- application functionality and integration tests;
- database connectivity and data integrity checks;
- authentication and authorization checks;
- network and dependent-service checks;
- performance and stability checks;
- security configuration and control checks; and
- vulnerability rescanning or targeted technical validation.

### 11.2 Test evidence

Record the test environment and versions, patch or change identifier, test cases and expected outcomes, actual results, tester and date, unresolved defects and impact, approval or rejection decision, and any production deployment restrictions.

A failed or incomplete test must be resolved, mitigated or formally escalated before production deployment. Emergency deployment may follow an expedited test path only when authorized and when the decision, safeguards and post-deployment validation are documented.

### 11.3 No representative test environment

Where no representative test environment exists, document:
- why testing cannot be performed;
- the risk of proceeding without testing;
- alternative safeguards, such as a limited deployment wave or enhanced monitoring;
- the recovery strategy; and
- the authority approving the residual deployment risk.

## 12. Change Management and Deployment Authorization

### 12.1 Standard changes

Production remediation must follow the approved change management process. The change record must reference the remediation item and include scope and affected assets, business justification and security urgency, implementation and validation plan, testing results or limitations, service impact and communications, rollback or recovery plan, implementation schedule, required approvals and post-implementation review requirements.

The change authority must ensure that the change category and approval route are appropriate. Approval to remediate a finding does not itself authorize an otherwise uncontrolled production change.

### 12.2 Emergency changes

Emergency patching may be necessary where delay creates unacceptable exposure. Emergency changes must:
- be limited to the scope necessary to address the urgent risk;
- be authorized by the designated emergency change authority;
- include an expedited assessment of compatibility and service impact;
- define available safeguards and a recovery approach;
- record why normal lead times cannot be followed;
- identify affected assets and versions;
- include immediate post-deployment validation; and
- undergo retrospective review and completion of records within the period defined by change management.

Emergency status must not bypass accountability or leave changes undocumented.

### 12.3 Deployment controls

During deployment:
- verify the target asset and package before execution;
- use approved administrative access and deployment tooling;
- maintain an implementation log;
- monitor service and security telemetry;
- record failed, skipped or unreachable assets;
- stop or pause deployment when predefined failure thresholds or material adverse effects occur; and
- protect deployment credentials, packages and logs from unauthorized access or alteration.

If a deployment wave is stopped, assess whether remaining assets require containment or an alternative remediation plan.

## 13. Implementation Types

This procedure applies to patches and non-patch corrective actions.

### 13.1 Operating system and platform patches

Examples include kernel, operating system, middleware, hypervisor and platform updates. Consider boot requirements, compatibility, cluster behavior, service dependencies and recovery arrangements.

### 13.2 Application and database updates

Examples include application security updates, framework upgrades, database patches, drivers and supporting libraries. Consider schema changes, application compatibility, transaction integrity, backup consistency and vendor support requirements.

### 13.3 Firmware and network appliance updates

Examples include firewall, router, switch, storage, endpoint and embedded-device firmware. Consider hardware model, bootloader dependencies, configuration preservation, high-availability behavior and vendor-supported upgrade paths.

### 13.4 Configuration and code remediation

Examples include disabling vulnerable services, correcting insecure settings, changing access controls, applying secure configuration baselines, updating application code, removing vulnerable dependencies or implementing input validation.

A configuration workaround may reduce exposure without fully removing the underlying vulnerability. The record must state that distinction.

### 13.5 Third-party remediation

Where a supplier or service provider performs the work, the internal owner must establish responsibility and expected completion date; communicate the required security outcome; obtain implementation and verification evidence; assess residual exposure or service limitation; track missed commitments and escalate through vendor governance; and retain internal accountability for risk treatment and acceptance.

## 14. Failed, Delayed or Unavailable Remediation

### 14.1 Failed deployment

When a patch or corrective change fails:

1. Stop further rollout if continued deployment could increase impact.
2. Protect service availability and data integrity.
3. Execute the approved rollback or recovery plan where required.
4. Record affected assets, error messages, logs and observed impact.
5. Notify the asset owner, change authority and Information Security.
6. Determine the technical cause and whether the vulnerability remains exploitable.
7. Define a revised remediation plan or compensating control.
8. Reassess risk and target dates.
9. Reattempt only after required technical and change approvals.

A failed deployment must not be recorded as remediated merely because the change was attempted.

### 14.2 Delayed remediation

A delay must have a documented reason, accountable owner, revised target date, interim safeguards and escalation decision. Repeated extensions require review by the appropriate risk authority and must not normalize overdue high-risk findings.

### 14.3 Patch unavailable

Where no vendor patch or supported fix exists:
- confirm vendor status and available guidance;
- assess workarounds and configuration mitigations;
- evaluate exposure reduction, isolation or service restriction;
- consider replacement, upgrade or decommissioning;
- document residual risk and uncertainty;
- establish monitoring and review triggers; and
- obtain formal risk treatment or acceptance from the authorized risk owner.

### 14.4 Unsupported or end-of-life platforms

Unsupported platforms require explicit management attention because security fixes may no longer be available. The asset owner must develop a migration, upgrade, replacement, isolation or decommissioning plan. Continued operation requires documented risk acceptance within authority, time-bound review and effective compensating controls where feasible.

## 15. Compensating Controls and Interim Mitigation

Compensating controls may be used when immediate remediation is infeasible, a patch is unavailable, or a permanent fix is being tested or scheduled.

Examples include:
- restricting network reachability or access paths;
- isolating the affected system or segment;
- disabling a vulnerable feature or service;
- enforcing additional authentication or privileged-access restrictions;
- applying web application or network-layer protections;
- increasing monitoring and alerting;
- limiting data access or functionality; and
- temporarily replacing an exposed service with a safer alternative.

For each control, document:
- vulnerability and assets addressed;
- threat or attack path being reduced;
- control owner and implementation date;
- configuration and operational details;
- evidence that the control is active;
- limitations and residual exposure;
- monitoring method and review frequency;
- conditions that would invalidate the control; and
- planned permanent remediation or risk decision.

Do not describe a compensating control as eliminating the vulnerability unless evidence supports that conclusion. Reassess its effectiveness when the environment, threat or control configuration changes.

## 16. Exceptions and Risk Acceptance

### 16.1 When an exception is required

A formal exception or risk acceptance is required when:
- a remediation target cannot be met;
- a patch is deferred beyond the approved target period;
- a vulnerability cannot be fixed or adequately mitigated;
- a platform is unsupported;
- a business or technical constraint prevents approved remediation;
- a compensating control is relied upon for an extended period; or
- the organization elects to retain residual risk.

### 16.2 Minimum exception record

The exception record must include:
- unique exception identifier;
- related finding and affected assets;
- risk rating and rationale;
- reason remediation is not being completed;
- alternatives considered;
- compensating controls and evidence;
- residual risk and uncertainty;
- accountable asset and risk owners;
- approval authority and approval date;
- expiry or mandatory review date;
- conditions and monitoring requirements;
- permanent remediation plan, if applicable; and
- escalation and revocation conditions.

### 16.3 Approval and review

Acceptance must be affirmative, documented and granted by an authorized risk owner. The requester or technical implementer must not self-approve acceptance unless explicitly authorized under the governance model and independently reviewed. Risks beyond delegated authority must be escalated.

Exceptions must be time-bound or subject to a defined mandatory review cycle. Material changes in exploitability, exposure, asset criticality, control effectiveness or business context trigger reassessment. Expired exceptions must be escalated and must not silently renew. Risk acceptance does not remove the obligation to monitor the vulnerability or reconsider remediation.

## 17. Post-Deployment Verification

### 17.1 Verification requirements

After implementation, verify that:
- the intended patch or corrective change was applied to each target asset;
- the installed version, package level or configuration is correct;
- relevant services and business functions remain operational;
- the original vulnerability or weakness is no longer present, or exposure is reduced as documented;
- no material security control was disabled or weakened;
- deployment failures, skipped assets and exceptions are accounted for; and
- monitoring shows no unresolved adverse effect attributable to the change.

### 17.2 Verification methods

Use methods appropriate to the remediation:
- authenticated vulnerability rescan;
- targeted scanner validation;
- package, version or patch-level inspection;
- configuration comparison;
- service and application health checks;
- code or dependency analysis;
- vendor or platform status confirmation;
- controlled technical testing; and
- review of deployment logs and system evidence.

A scanner result alone may be insufficient where detection is unreliable or remediation is a configuration, code or compensating-control change. A version check alone may not prove that the vulnerable feature is no longer exposed.

### 17.3 Verification evidence

Identify the verification date and reviewer, affected assets and coverage, method and tool/version where relevant, evidence references, expected and actual results, unresolved limitations or exceptions, and closure recommendation.

Where verification is incomplete, the finding must remain open, partially remediated or otherwise accurately classified under the organization's status model.

## 18. Closure Criteria and Reopening

### 18.1 Closure criteria

A remediation item may be closed only when one of the following outcomes is supported and authorized.

**Remediated**
- corrective action is implemented on all in-scope affected assets;
- verification supports that the identified weakness is addressed;
- failed or skipped assets are separately tracked;
- required change and implementation records are complete; and
- the security reviewer or designated closure authority accepts the evidence.

**Not applicable / false positive**
- technical evidence demonstrates that the finding does not apply;
- the rationale is recorded; and
- required security review is complete.

**Risk accepted / exception approved**
- the authorized risk owner formally accepts residual risk;
- the exception is current and includes required safeguards and review conditions; and
- the record remains visible in exception and risk reporting.

Accepted risk is not technical remediation. Reporting must preserve this distinction.

### 18.2 Reopening

Reopen the item when verification fails or is invalidated; the vulnerability remains on an affected asset; new assets are identified; the patch is withdrawn or found ineffective; a compensating control fails; the exception expires or its conditions are breached; or new threat information materially changes risk.

Preserve the previous closure decision and record the reason, date and new owner.

## 19. Status Model

The following suggested baseline may be adapted, but implementation, verification, exception and final closure states must remain distinguishable.

| Status | Meaning |
|---|---|
| New | Registered and awaiting triage. |
| Under Validation | Applicability, scope or evidence is being confirmed. |
| Assigned | Owner identified; remediation plan not yet approved. |
| Planned | Remediation approach and target date documented. |
| Awaiting Change Approval | Change request submitted and pending authorization. |
| Scheduled | Approved remediation scheduled for implementation. |
| In Progress | Implementation is underway. |
| Failed | Attempted remediation failed and requires further action. |
| Partially Remediated | Some affected assets or components are fixed; others remain open. |
| Pending Verification | Implementation reported complete; security verification outstanding. |
| Exception Pending | Formal exception or risk acceptance awaiting decision. |
| Deferred / Exception Approved | Remediation deferred under a current approved decision. |
| Closed - Remediated | Evidence supports successful remediation and closure approval. |
| Closed - Not Applicable | Applicability decision approved with evidence. |
| Reopened | Previously closed item requires renewed action. |

## 20. Reporting and Metrics

Information Security should provide periodic reporting to the designated governance forum. The organization must define reporting frequency and recipients.

Useful measures include:
- open findings by risk rating, age and business unit;
- remediation completion against approved target dates;
- overdue findings by owner and risk category;
- median and percentile remediation time by severity;
- number and age of approved exceptions;
- expired or repeatedly extended exceptions;
- patch deployment coverage across eligible assets;
- patch failure and rollback rates;
- assets missing from patch or vulnerability coverage;
- percentage of remediations with completed verification evidence;
- recurring vulnerabilities and repeat findings;
- unsupported and end-of-life assets;
- emergency patch volume and retrospective review completion; and
- remediation backlog trends.

### 20.1 Metric interpretation

Metrics must include definitions, data sources, reporting period and exclusions. A high closure count is not proof of effective remediation if findings are closed through exceptions, not-applicable decisions or incomplete verification. Report technical remediation separately from accepted risk.

Targets must be approved and must not encourage unsafe deployment, suppression of findings or premature closure.

## 21. Records and Auditability

Retain records in approved repositories with access controls and retention periods consistent with organizational policy and applicable obligations.

Records should include:
- originating finding and assessment reports;
- risk prioritization and decisions;
- ownership and target-date history;
- patch advisories and applicability assessments;
- remediation and deployment plans;
- test and compatibility results;
- change requests and approvals;
- implementation logs and deployment outcomes;
- rollback and failure records;
- compensating-control evidence;
- exceptions and risk acceptance;
- post-deployment verification;
- closure and reopening decisions;
- reporting outputs; and
- supplier communications and service evidence.

Protect records against unauthorized access, alteration and premature disposal. Handle sensitive technical details, credentials, exploit information and system configuration data under the organization's information classification and evidence-handling requirements.

## 22. Quality Assurance and Process Effectiveness

Information Security or an assigned assurance function should periodically sample records to determine whether:
- findings are complete, accurately prioritized and assigned;
- risk decisions are supported by evidence;
- target dates and extensions are justified;
- patch assessments address applicability and known issues;
- test and change approvals are present;
- deployment evidence identifies actual affected assets;
- failures and exceptions are properly escalated;
- compensating controls operate as intended;
- verification is sufficient and independent where appropriate;
- closure states accurately represent outcomes; and
- metrics reconcile to source records.

Recurring weaknesses should result in corrective actions, process updates, training or technical improvements. High-risk remediation should receive proportionate independent review.

## 23. Exceptions to This Procedure

Any exception to this procedure must identify the specific requirement being varied, explain the operational or technical reason, assess resulting security and operational risk, define compensating safeguards, identify the approving authority, specify an expiry or review date, and be retained in the approved exception repository.

An exception to a procedural requirement does not automatically constitute acceptance of the underlying security risk. Record both decisions where applicable.

## 24. Review and Maintenance

The document owner must review this procedure at least annually and when material changes occur, including:
- changes to risk appetite or governance structure;
- significant changes in infrastructure, cloud or application architecture;
- changes to vulnerability management or patching capabilities;
- material security incidents or failed remediation events;
- changes to applicable legal, regulatory or contractual requirements; or
- audit findings indicating that the procedure is ineffective.

Revisions must be version-controlled, reviewed and approved under the organization's document governance process.

## 25. Adoption Checklist

Before this procedure becomes operational, the organization should:

- [ ] Assign the document owner and approving authority.
- [ ] Map procedure roles to actual teams and named positions.
- [ ] Approve risk categories and remediation target periods.
- [ ] Define escalation paths and risk acceptance authorities.
- [ ] Identify authoritative vendor and threat advisory sources.
- [ ] Define patch monitoring responsibilities and cadence.
- [ ] Align patch deployment with change management.
- [ ] Define standard and emergency change approval routes.
- [ ] Establish testing, backup, rollback and recovery requirements.
- [ ] Define verification methods and closure authority.
- [ ] Configure the remediation register and status model.
- [ ] Establish exception expiry and review controls.
- [ ] Define reporting metrics, recipients and frequency.
- [ ] Establish record storage, access and retention requirements.
- [ ] Communicate responsibilities to asset owners and technical teams.

---

# Appendix A - Remediation Action Record

| Field | Entry |
|---|---|
| Remediation ID | [Unique identifier] |
| Finding ID / source reference | [Identifier] |
| Date identified / registered | [Date] |
| Affected assets / services | [Asset IDs and service names] |
| Vulnerability / weakness | [Description and identifiers] |
| Initial severity / risk | [Rating and rationale] |
| Exploitability / threat context | [Details] |
| Asset owner | [Role / name] |
| Technical remediation owner | [Role / name] |
| Remediation action | [Patch, configuration, code, replacement, isolation, etc.] |
| Target date | [Date and basis] |
| Change reference | [Change ID] |
| Dependencies / constraints | [Details] |
| Interim controls | [Controls and evidence] |
| Current status | [Status] |
| Verification method | [Method] |
| Verification evidence | [References] |
| Residual risk | [Rating and rationale] |
| Closure decision / approver | [Decision, role, date] |

# Appendix B - Patch Assessment and Deployment Plan

| Field | Entry |
|---|---|
| Patch / advisory reference | [Vendor, identifier, date] |
| Product / component | [Name and version] |
| Affected assets | [Asset IDs] |
| Applicability assessment | [Applicable / not applicable / uncertain] |
| Patch source and integrity check | [Approved source and validation] |
| Known issues / prerequisites | [Details] |
| Dependencies | [Details] |
| Proposed deployment wave | [Pilot / staged / full] |
| Test scope and results | [Reference] |
| Service impact | [Expected impact] |
| Backup / recovery approach | [Details] |
| Rollback plan | [Steps or reference] |
| Maintenance window | [Date/time] |
| Change record | [Identifier] |
| Approvals | [Roles, decisions, dates] |
| Post-deployment verification | [Method and owner] |
| Contingency | [Failure response] |

# Appendix C - Patch Testing and Compatibility Record

| Field | Entry |
|---|---|
| Test record ID | [Identifier] |
| Patch / change reference | [Identifier] |
| Test environment | [Environment and similarity to production] |
| Product / platform versions | [Versions] |
| Test cases | [References] |
| Expected results | [Criteria] |
| Actual results | [Results] |
| Functional / integration impact | [Details] |
| Security validation | [Details] |
| Defects or limitations | [Details] |
| Tester / date | [Role, name, date] |
| Decision | [Pass / conditional pass / fail] |
| Conditions for deployment | [Conditions] |
| Reviewer / approval | [Role, name, date] |

# Appendix D - Change and Deployment Approval Record

| Field | Entry |
|---|---|
| Change ID | [Identifier] |
| Related remediation IDs | [Identifiers] |
| Change category | [Standard / normal / emergency / other] |
| Scope and assets | [Details] |
| Security justification | [Details] |
| Implementation plan | [Reference] |
| Test evidence | [Reference or limitation] |
| Service impact | [Details] |
| Rollback / recovery | [Reference] |
| Deployment window | [Date/time] |
| Approver(s) | [Roles and decisions] |
| Approval date | [Date] |
| Deployment owner | [Role / name] |
| Post-change review | [Outcome and date] |

# Appendix E - Emergency Patch Authorization

| Field | Entry |
|---|---|
| Emergency request ID | [Identifier] |
| Vulnerability / advisory | [Identifier] |
| Reason for emergency | [Active exploitation, imminent threat, etc.] |
| Affected assets | [Scope] |
| Risk of delay | [Assessment] |
| Expedited compatibility assessment | [Results / limitations] |
| Deployment safeguards | [Details] |
| Recovery approach | [Details] |
| Authorized scope | [Assets and actions] |
| Emergency approver | [Role / name] |
| Authorization date/time | [Date/time] |
| Implementer | [Role / name] |
| Immediate verification | [Results] |
| Retrospective review | [Reference and completion date] |

# Appendix F - Failed Deployment Record

| Field | Entry |
|---|---|
| Failure record ID | [Identifier] |
| Related finding / change | [Identifiers] |
| Affected assets | [Assets] |
| Deployment date/time | [Date/time] |
| Failure description | [Details] |
| Logs / evidence | [References] |
| Service or security impact | [Details] |
| Rollback / recovery performed | [Details] |
| Root cause / current hypothesis | [Details] |
| Vulnerability status after failure | [Present / mitigated / unknown] |
| Interim safeguards | [Details] |
| Revised action and target date | [Details] |
| Escalation / approvals | [Details] |

# Appendix G - Compensating Control Record

| Field | Entry |
|---|---|
| Control record ID | [Identifier] |
| Related finding / assets | [Identifiers] |
| Reason permanent remediation is pending | [Details] |
| Threat or attack path addressed | [Details] |
| Control description | [Configuration / operational details] |
| Control owner | [Role / name] |
| Implementation date | [Date] |
| Effectiveness evidence | [References] |
| Residual exposure and limitations | [Details] |
| Monitoring and review cadence | [Details] |
| Failure / invalidation trigger | [Conditions] |
| Permanent remediation plan | [Details] |
| Security reviewer | [Role / name / date] |

# Appendix H - Remediation Exception and Risk Acceptance

| Field | Entry |
|---|---|
| Exception ID | [Identifier] |
| Related finding / assets | [Identifiers] |
| Requested deviation | [Requirement / target date] |
| Reason and alternatives considered | [Details] |
| Inherent and residual risk | [Ratings and rationale] |
| Compensating controls | [Details and evidence] |
| Accountable asset owner | [Role / name] |
| Risk owner | [Role / name] |
| Approval authority | [Role / name] |
| Decision and date | [Approved / rejected / conditional] |
| Conditions | [Requirements] |
| Expiry / review date | [Date] |
| Reassessment triggers | [Conditions] |
| Permanent remediation plan | [Details] |

# Appendix I - Post-Deployment Verification Record

| Field | Entry |
|---|---|
| Verification ID | [Identifier] |
| Related finding / remediation / change | [Identifiers] |
| Verification date | [Date] |
| Reviewer | [Role / name] |
| Assets in scope | [Assets] |
| Assets verified | [Count and identifiers] |
| Method and tool/version | [Details] |
| Package / version / configuration evidence | [References] |
| Vulnerability validation result | [Result] |
| Service health result | [Result] |
| Exceptions / skipped assets | [Details] |
| Limitations | [Details] |
| Closure recommendation | [Close / remain open / reopen] |
| Approval | [Role / name / date] |

# Appendix J - Remediation Closure Checklist

- [ ] Originating finding and all affected assets are identified.
- [ ] Remediation owner and asset owner are recorded.
- [ ] Approved remediation action is documented.
- [ ] Required change approvals are retained.
- [ ] Implementation outcome is recorded for each affected asset.
- [ ] Failed, skipped and unreachable assets are separately tracked.
- [ ] Verification evidence supports the claimed security outcome.
- [ ] Service health and relevant control operation are checked.
- [ ] Compensating controls and exceptions are current where applicable.
- [ ] Residual risk and remaining limitations are documented.
- [ ] Closure status distinguishes remediation from risk acceptance.
- [ ] Security review and closure approval are recorded.
- [ ] Related registers, dashboards and reports are updated.
- [ ] Evidence and records are stored in approved repositories.

# Appendix K - Related Repository Documents

Read this procedure with the applicable current versions of:
- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/policies/information-security-policy.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `templates/risk-register-template.md`
- `templates/assessment-report-template.md`
- `templates/technical-assessment-checklist.md`
- `templates/evidence-register-template.md`

# Appendix L - Reference Frameworks

The organization may use relevant editions and updates of:
- NIST Cybersecurity Framework (CSF) 2.0.
- NIST SP 800-40, Guide to Enterprise Patch Management Planning.
- NIST SP 800-53, Security and Privacy Controls for Information Systems and Organizations.
- NIST SP 800-61, Computer Security Incident Handling Guide.
- ISO/IEC 27001 and ISO/IEC 27002.
- ISO/IEC 27005, Information security risk management.
- CIS Critical Security Controls.
- Relevant vendor security advisories and product lifecycle documentation.

References provide guidance and do not, by themselves, establish organizational compliance or replace applicable legal, regulatory, contractual or internal requirements.

---

**End of document**
