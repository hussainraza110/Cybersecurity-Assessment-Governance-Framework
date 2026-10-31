# Security Incident Response Procedure

## Document Control

| Field | Value |
|---|---|
| Document title | Security Incident Response Procedure |
| Document identifier | PROC-SEC-IR-001 |
| Version | 1.0 |
| Document owner | Information Security |
| Approving authority | [Insert approving authority] |
| Classification | [Insert classification] |
| Effective date | [Insert date] |
| Review frequency | At least annually and following material change |
| Status | Draft template pending organizational approval |

> **Implementation note:** This organization-neutral template must be tailored and approved before adoption. Assign actual roles, reporting channels, response authorities, severity criteria, escalation paths, regulatory and contractual obligations, retention periods and recovery requirements. Notification deadlines must be determined from applicable laws, regulations, contracts and organizational commitments; this procedure does not establish universal deadlines.

## 1. Purpose

This procedure establishes a controlled, repeatable and auditable process for identifying, reporting, assessing, responding to, recovering from and learning from information security incidents.

It defines the governance, roles, decision points, response activities and records required to:
- detect and report suspected security incidents;
- distinguish security events from confirmed incidents;
- assess severity, scope and business impact;
- coordinate containment, investigation, eradication and recovery;
- preserve relevant evidence and maintain appropriate records;
- coordinate internal and external communications through authorized channels;
- identify and escalate applicable legal, regulatory and contractual obligations;
- close incidents on an evidence-supported basis; and
- track lessons learned and corrective actions.

## 2. Scope

This procedure applies to suspected and confirmed information security incidents affecting organization-owned, managed or formally authorized information assets and services, including:
- information systems, servers, endpoints and mobile devices;
- networks, security appliances and telecommunications;
- business applications, web applications, APIs and databases;
- cloud services, hosted environments, containers and virtualization platforms;
- identities, credentials, privileged accounts and authentication services;
- information in physical, electronic or other supported formats;
- facilities and physical environments where information assets are affected; and
- third-party services, suppliers and managed environments where organizational information or services may be affected.

It applies to incidents involving actual or suspected compromise of confidentiality, integrity or availability, including unauthorized access, disclosure, alteration, destruction, disruption, malware, ransomware, denial of service, account compromise, data loss, fraud involving information systems, and security-control failure.

This procedure applies to employees, contractors and other parties who identify, report, investigate, respond to or manage an incident.

It does not replace:
- the Information Security Policy;
- the Evidence Handling procedure;
- the Security Assessment Authorization Procedure;
- the Vulnerability Assessment Procedure;
- the Security Remediation and Patch Management Procedure;
- business continuity and disaster recovery plans;
- privacy, legal, regulatory or contractual notification procedures; or
- law-enforcement engagement protocols.

Where another approved policy, procedure or legal obligation imposes stricter requirements, the stricter requirement applies unless an authorized decision establishes otherwise.

## 3. Definitions

| Term | Definition |
|---|---|
| Security event | An observed occurrence in a system, service or environment that may be relevant to information security but has not necessarily been assessed as an incident. |
| Suspected incident | A security event or report that reasonably indicates a possible breach or compromise and requires triage. |
| Security incident | An event, or series of events, that has been assessed as an actual or reasonably suspected compromise of information security requiring coordinated response under this procedure. |
| Major incident | An incident meeting the organization's approved high-impact or critical escalation criteria. |
| Incident commander / manager | The person assigned authority to coordinate response activities and maintain the incident action and decision record. |
| Containment | Actions taken to limit the scope, spread, impact or persistence of an incident. |
| Eradication | Actions taken to remove the cause, malicious activity, unauthorized access or other identified compromise. |
| Recovery | Actions to restore affected systems, services and business operations to an approved and monitored state. |
| Evidence | Information or material collected or preserved to support analysis, decisions, accountability or possible legal or disciplinary processes. |
| Root cause | The underlying technical, procedural, human or organizational condition that enabled or materially contributed to the incident. |
| Incident closure | The authorized decision that immediate response objectives have been met and the incident record is sufficiently complete, with remaining actions tracked separately. |

## 4. Governance and Response Principles

The following principles apply:

1. **Prompt reporting:** Personnel must report suspected incidents through approved channels without waiting to prove that an incident occurred.
2. **Defined authority:** Response actions must be directed or authorized by designated roles, with emergency authority clearly established.
3. **Proportionate response:** Actions must reflect severity, urgency, operational impact, safety, legal considerations and available evidence.
4. **Preservation:** Relevant evidence must be protected from avoidable alteration, loss or unauthorized disclosure.
5. **Containment and continuity:** Security response must consider the impact of containment on business services, safety and critical operations.
6. **Need-to-know handling:** Incident information must be shared only with authorized parties who need it to perform their responsibilities.
7. **Accurate records:** Material actions, decisions, approvals, communications and timelines must be recorded.
8. **No retaliation for good-faith reporting:** Personnel should be able to report suspected incidents through approved channels without fear of retaliation for a good-faith report.
9. **Controlled external communication:** Only authorized representatives may communicate externally on behalf of the organization.
10. **Continuous improvement:** Significant incidents and response exercises must inform corrective actions and capability improvements.

## 5. Roles and Responsibilities

The organization must map these functions to actual job titles, teams and on-call arrangements. One individual may perform multiple roles where necessary, but conflicts of interest and segregation-of-duty limitations must be documented.

| Role | Core responsibilities |
|---|---|
| Executive / Senior Management | Provides strategic direction and resources; receives major incident escalations; makes decisions reserved to executive authority. |
| Incident Response Authority | Authorizes response priorities and significant actions; resolves cross-functional issues; approves major incident decisions within delegated authority. |
| Incident Manager / Incident Commander | Coordinates response; establishes incident objectives; assigns actions; maintains the incident timeline, decision log and status; escalates blockers. |
| Information Security / Incident Response Team | Performs security triage, analysis, containment recommendations, investigation coordination, evidence handling oversight and security validation. |
| IT Operations / Platform Teams | Executes authorized technical actions; supports isolation, restoration, backup, system recovery and operational validation. |
| Asset / System Owner | Confirms system context and criticality; evaluates operational impact; supports containment and recovery decisions; validates service outcomes. |
| Business / Service Owner | Assesses business impact; prioritizes service restoration; coordinates business workarounds; accepts restored service within authority. |
| Legal / Compliance / Privacy | Advises on legal privilege, regulatory and contractual obligations, privacy impact, evidence handling and external notification requirements. |
| Human Resources | Advises on personnel-related matters and applicable employment processes where relevant. |
| Communications / Public Relations | Coordinates approved internal and external messaging and media handling. |
| Procurement / Vendor Management | Coordinates supplier escalation, contractual obligations and third-party response. |
| Physical Security / Facilities | Supports incidents involving facilities, physical access, equipment or physical safety. |
| Internal Audit / Assurance | May independently review response governance and records; does not direct operational response unless formally assigned. |
| All Personnel | Promptly report suspected incidents, preserve relevant information and follow response instructions. |

### 5.1 Role assignment and delegation

- An incident manager must be assigned to every incident requiring coordinated response.
- A major incident must have a clearly identified response lead and an escalation route to senior management.
- Response authority and emergency technical authority must be documented before an incident occurs.
- Where the usual approver is unavailable, the approved alternate or delegation process must be used.
- The person who reports an incident is not automatically responsible for investigating or resolving it.
- A third party may perform technical response tasks, but internal accountability for risk, business decisions and incident governance remains with the organization unless formally established otherwise.

## 6. Preparation and Readiness

The document owner, in coordination with relevant teams, must maintain incident response readiness.

Preparation should include:
- approved incident reporting channels and escalation contacts;
- current asset, service and system ownership information;
- incident severity and escalation criteria;
- on-call and out-of-hours response arrangements;
- contact details for management, legal, privacy, communications and key suppliers;
- secure incident record and evidence repositories;
- approved forensic, monitoring and response tools;
- access to relevant logs, backups and system configurations;
- emergency access and privileged-account procedures;
- business continuity and disaster recovery dependencies;
- approved containment and recovery playbooks for critical services;
- supplier incident notification and cooperation requirements;
- training and awareness for personnel with reporting duties; and
- periodic tabletop or technical response exercises.

Readiness information must be protected against unauthorized access while remaining available to authorized responders during an incident.

## 7. Incident Identification and Reporting

### 7.1 Detection sources

Incidents may be identified through:
- security monitoring and SIEM alerts;
- endpoint detection and response tools;
- network and application monitoring;
- vulnerability assessments and penetration tests;
- system, database and cloud audit logs;
- user, employee or contractor reports;
- service desk tickets;
- threat intelligence and security advisories;
- supplier or managed service provider notifications;
- customer, partner or public reports;
- physical security observations; and
- law-enforcement or regulatory communications.

### 7.2 Reporting requirement

Personnel must promptly report suspected incidents through the organization's designated channel, such as:
- [Insert security incident email / mailbox];
- [Insert service desk or incident portal];
- [Insert emergency telephone number];
- [Insert 24x7 security operations contact]; or
- [Insert alternate reporting route].

If the primary channel is unavailable or compromised, use the designated alternate route. Personnel must not delay reporting to collect proof or conduct their own investigation.

### 7.3 Minimum report information

A report should include, where known:
- reporter name and safe contact method;
- date and time detected, including time zone;
- date and time reported;
- affected asset, user, service, location or supplier;
- description of observed activity or suspected compromise;
- how the event was detected;
- known impact or unusual behavior;
- screenshots, alerts, log references or other available indicators;
- actions already taken; and
- any immediate safety, service or business concern.

Missing details must not prevent initial reporting. Record unknown information as unknown.

### 7.4 Initial acknowledgement

The receiving function should acknowledge the report through an approved channel, create or update an incident record, identify an initial owner and determine whether immediate escalation is required. Acknowledgement is not confirmation that an incident has occurred.

## 8. Intake, Triage and Classification

### 8.1 Initial triage

The receiving security function must:
1. Register the report and preserve the original report details.
2. Establish the reporting and detection timeline.
3. Validate available indicators and identify affected assets or accounts.
4. Determine whether the report is a security event, suspected incident or confirmed incident.
5. Assess immediate risk to confidentiality, integrity and availability.
6. Identify potential safety, operational, privacy, legal or contractual implications.
7. Determine whether urgent containment or specialist support is required.
8. Assign an incident manager or appropriate handler.
9. Record initial classification, confidence and outstanding information needs.

### 8.2 Event versus incident decision

A security event may be closed as non-incident only when an authorized reviewer records a reasoned determination, such as benign activity, duplicate alert or unsupported report. If uncertainty remains material, retain the matter as suspected incident or under investigation.

A lack of confirmed impact does not by itself establish that no incident occurred.

### 8.3 Severity classification

The organization must approve a severity model. The following is a suggested baseline and must be calibrated to its risk appetite and operational context.

| Severity | Illustrative criteria | Governance response |
|---|---|---|
| Critical / Major | Widespread or material compromise; significant sensitive-data exposure; major disruption of critical services; privileged or core infrastructure compromise; credible threat to safety; substantial legal or regulatory implications. | Immediate escalation to incident response authority and senior management; coordinated response; frequent status updates; legal/compliance involvement as appropriate. |
| High | Confirmed compromise of important systems or accounts; material but contained data exposure; significant service degradation; credible lateral movement or persistence; high business impact. | Urgent response; incident manager assigned; relevant service and security leaders engaged; documented containment and recovery decisions. |
| Moderate | Limited compromise or disruption with bounded scope; affected non-critical systems; manageable business impact; no evidence of broad propagation. | Assigned response owner; investigation and corrective actions tracked; escalation if scope or impact increases. |
| Low | Limited security event or suspected incident with low apparent impact and no confirmed material compromise. | Documented triage and proportionate handling; monitor for indicators that require reclassification. |

### 8.4 Classification considerations

Severity must consider:
- actual and potential impact on confidentiality, integrity and availability;
- sensitivity and volume of affected information;
- privilege level and identity of compromised accounts;
- criticality and exposure of affected assets;
- scope, duration and propagation;
- threat actor capability, intent and observed behavior where known;
- service disruption and recovery complexity;
- safety implications;
- privacy, legal, regulatory and contractual implications;
- third-party and supply-chain impact; and
- uncertainty and confidence in the available evidence.

Record both severity and confidence. Do not reduce severity merely because evidence is incomplete when the plausible impact is high.

### 8.5 Reclassification

Reassess severity when scope, impact, threat information or confidence changes. Record the prior and new classifications, date, decision-maker and rationale. Escalate promptly when an incident meets a higher severity threshold.

## 9. Incident Response Lifecycle

The incident manager coordinates the following lifecycle stages. Activities may overlap or be repeated as new information emerges.

1. Preparation and readiness.
2. Detection and reporting.
3. Triage and analysis.
4. Containment.
5. Evidence preservation and investigation.
6. Eradication.
7. Recovery.
8. Closure and post-incident improvement.

The sequence must be adapted to the incident. For example, urgent containment may be required before a complete investigation, provided evidence and operational considerations are addressed as far as practicable.

## 10. Containment

### 10.1 Objectives

Containment aims to limit further compromise, propagation, data loss, service disruption or unauthorized access while preserving the ability to investigate and recover.

### 10.2 Possible containment actions

Depending on the incident, authorized responders may:
- isolate affected endpoints, servers or network segments;
- disable or restrict compromised accounts and sessions;
- revoke or rotate exposed credentials, keys, tokens or certificates;
- block malicious domains, addresses, files or traffic patterns;
- restrict remote access or administrative pathways;
- disable affected services, integrations or application functions;
- apply temporary network or application controls;
- suspend suspicious transactions or data transfers;
- quarantine affected files or systems;
- preserve relevant volatile and non-volatile evidence; and
- activate business continuity or alternate operating arrangements.

### 10.3 Containment decision requirements

Before material containment actions, assess where practicable:
- expected security benefit;
- business and service availability impact;
- safety or operational technology considerations;
- potential loss of volatile evidence;
- dependencies and downstream effects;
- authority required;
- communications needed; and
- rollback or restoration approach.

Where immediate action is necessary to prevent material harm, authorized emergency responders may act under pre-approved emergency authority. They must document the action and notify the incident manager and relevant authority as soon as practicable.

### 10.4 Containment record

Record:
- action and objective;
- affected assets, accounts or services;
- decision-maker and implementer;
- authorization and time;
- expected and actual impact;
- evidence preserved before or during action, where feasible;
- validation result; and
- conditions for removal or adjustment of the control.

Containment must be reviewed regularly. Temporary controls must not remain indefinitely without ownership and reassessment.

## 11. Evidence Preservation and Investigation

### 11.1 Evidence handling

Evidence must be collected and handled in accordance with the organization's Evidence Handling procedure and any applicable legal or regulatory requirements.

Responders must:
- obtain required authorization for collection and access;
- identify the source, custodian and collection context;
- record collection date and time, including time zone;
- preserve original evidence where feasible;
- use working copies for analysis where appropriate;
- record tools, methods and relevant versions;
- verify integrity using proportionate methods, such as cryptographic hashes, where appropriate;
- restrict access to authorized personnel;
- document transfers and custody where evidential integrity requires it;
- protect sensitive, personal and privileged information; and
- retain evidence in approved repositories.

Do not unnecessarily power off, reboot, modify or clean a potentially compromised system before considering volatile evidence and investigation needs. Any urgent operational action must be documented.

### 11.2 Investigation objectives

Investigation should establish, to the extent reasonably possible:
- what happened and how it was detected;
- when the activity began, was detected and was contained;
- which systems, accounts, services and information were affected;
- the initial access vector and likely attack path;
- whether unauthorized access, disclosure, alteration or destruction occurred;
- whether the attacker or malicious process remains present;
- whether persistence, lateral movement or privilege escalation occurred;
- whether data was accessed, transferred or exfiltrated;
- which controls failed, were bypassed or were absent;
- the likely root cause and contributing conditions;
- what remains unknown; and
- what actions are needed to contain, eradicate, recover and prevent recurrence.

### 11.3 Investigation methods

Depending on scope and authorization, investigation may include:
- review of endpoint, network, application, database, identity and cloud logs;
- endpoint and server forensic examination;
- analysis of malware, scripts, binaries or suspicious artifacts;
- review of authentication, privilege and access records;
- network traffic and DNS analysis;
- cloud control-plane and workload activity review;
- timeline reconstruction and event correlation;
- review of configuration, vulnerability and change history; and
- interviews with relevant personnel or suppliers.

Investigation must remain within approved authority and applicable law. Activities that could disrupt services, alter evidence or exceed authorized scope require appropriate approval.

### 11.4 Specialist and external support

Engage qualified forensic, legal, privacy, insurance, law-enforcement or specialist response support when the incident's complexity, evidential requirements, potential litigation, regulatory implications or business impact warrants it. Record the engagement authority, scope and handling arrangements.

### 11.5 Investigation findings and uncertainty

Maintain an investigation record that distinguishes:
- confirmed facts;
- supported conclusions;
- working hypotheses;
- unverified reports; and
- unresolved questions.

Do not present an attribution, data-exfiltration conclusion or root cause as confirmed unless the evidence supports it. Record limitations and confidence.

## 12. Eradication

Eradication removes the identified cause, malicious activity, unauthorized access or persistence, and addresses the conditions that enabled the incident.

Depending on the incident, actions may include:
- removing malware, unauthorized tools and persistence mechanisms;
- rebuilding compromised systems from trusted sources;
- patching exploited vulnerabilities;
- correcting insecure configurations;
- disabling unauthorized accounts and access paths;
- rotating credentials, keys, certificates and tokens;
- removing unauthorized changes and scheduled tasks;
- correcting application or code weaknesses;
- updating detection and prevention controls;
- replacing compromised devices or components; and
- addressing supplier or third-party weaknesses.

Eradication must be based on an adequate understanding of the compromise. Removing an observed malicious file alone may be insufficient if persistence, credential compromise or lateral movement has not been addressed.

Where remediation involves patches or corrective changes, follow the Security Remediation and Patch Management Procedure and applicable change controls.

## 13. Recovery

### 13.1 Recovery planning

The incident manager coordinates recovery with IT operations, asset owners and business owners. The plan should identify:
- systems and services to restore;
- trusted recovery sources and backup integrity;
- restoration sequence and dependencies;
- required configuration and security baselines;
- validation and acceptance criteria;
- access restoration and credential changes;
- heightened monitoring requirements;
- business workarounds and service communications;
- recovery risks and residual exposure; and
- the authority approving return to normal operation.

### 13.2 Recovery validation

Before returning a system or service to normal operation, verify as appropriate:
- the identified compromise and persistence have been addressed;
- required patches and configuration corrections are applied;
- privileged and user access is appropriate;
- backups or recovery images are trustworthy;
- critical security controls are functioning;
- application and service health is acceptable;
- data integrity and availability are validated;
- monitoring and alerting are active; and
- unresolved risks and limitations are documented.

### 13.3 Heightened monitoring

For a period determined by incident severity and residual risk, apply enhanced monitoring to affected systems, accounts, services and attack paths. Define monitoring owner, scope, duration or review date, alert thresholds and escalation path.

### 13.4 Return to service

The designated service or business owner must approve business service restoration within delegated authority. Security must review relevant security validation and residual exposure. Major incidents or high-risk recoveries require approval by the designated incident response authority or other authorized governance body.

Restoration does not automatically mean the incident is closed.

## 14. Communications and Escalation

### 14.1 Internal communications

The incident manager must establish a communication approach proportionate to severity. Relevant recipients may include:
- incident response personnel;
- senior management and the incident response authority;
- affected system and business owners;
- IT operations and service desk;
- legal, compliance and privacy functions;
- human resources, where relevant;
- communications or public relations;
- physical security and facilities; and
- supplier or vendor management.

Updates should communicate confirmed facts, current impact, actions underway, decisions required, risks, next steps and next update timing. Avoid unnecessary distribution of sensitive technical details.

### 14.2 External communications

Only authorized representatives may communicate with:
- customers, users or business partners;
- suppliers and service providers;
- regulators or government authorities;
- law enforcement;
- insurers;
- media; and
- other external stakeholders.

Information Security must coordinate with Legal, Compliance, Privacy and Communications as applicable before external notification, unless an emergency or legal requirement dictates a different authorized route.

### 14.3 Regulatory, privacy and contractual obligations

As soon as a potential obligation is identified, refer it to Legal, Compliance and Privacy for assessment. They must determine:
- whether a legal, regulatory, contractual or policy notification obligation applies;
- the relevant triggering event and applicable deadline;
- the information required for notification;
- the authorized notifying party and approval route;
- whether phased or supplemental notification is permitted or required;
- recordkeeping requirements; and
- whether law-enforcement or regulator engagement is appropriate.

Do not assume that every security incident is a reportable breach, or that the same deadline applies across jurisdictions and contracts. Preserve the decision and rationale, including a determination that no notification is required.

### 14.4 Communication record

Record significant communications, including date and time, sender, recipients, channel, purpose, approved content or reference, decisions, and follow-up actions. Protect legally privileged or otherwise restricted communications appropriately.

## 15. Third-Party and Supply-Chain Incidents

Where an incident involves a supplier, cloud provider, managed service provider or other third party:
- identify the affected service, data, assets and contractual relationship;
- activate the applicable supplier incident escalation route;
- request timely facts, scope, containment status and relevant evidence;
- determine whether the incident affects other organizational services or suppliers;
- coordinate containment and recovery responsibilities;
- assess contractual, privacy, regulatory and customer implications;
- preserve supplier communications and evidence references;
- track supplier corrective actions and assurance evidence; and
- retain internal ownership of organizational risk and notification decisions.

Supplier statements must be assessed in context and should not be treated as independently verified facts without supporting evidence.

## 16. Incident Closure

### 16.1 Closure criteria

An incident may be proposed for closure when:
- immediate malicious or unauthorized activity is contained;
- investigation has reached a reasonable conclusion or remaining uncertainty is explicitly documented;
- eradication has been completed or remaining work is covered by an approved plan and risk decision;
- affected services are restored or formally transitioned to an approved recovery or continuity state;
- relevant evidence and records are preserved;
- required internal and external communications or notifications have been assessed and actioned;
- residual risks are documented and assigned;
- corrective actions have owners and target dates;
- required incident reviews and approvals are complete; and
- the incident record is sufficiently complete for audit and future reference.

### 16.2 Closure approval

The incident manager recommends closure. The designated incident response authority or assigned closure approver approves closure according to severity and governance rules. Major incidents should receive explicit management or delegated authority review.

### 16.3 Open corrective actions

Long-term improvements need not all be completed before incident closure if immediate response objectives have been met and each remaining action is:
- separately recorded;
- assigned to an accountable owner;
- risk-prioritized;
- given a target date;
- linked to the incident; and
- monitored through the appropriate remediation or risk process.

### 16.4 Reopening

Reopen or link a new incident when new evidence indicates that the original incident remains active, containment failed, compromise recurred, recovery was unsafe, scope was materially understated or a related threat remains unresolved. Preserve the previous closure decision and document the reason for reopening.

## 17. Post-Incident Review and Lessons Learned

A post-incident review must be conducted for major incidents and should be considered for other incidents based on severity, recurrence, novelty or learning value.

The review should examine:
- incident chronology and key decisions;
- detection effectiveness and time to detect;
- reporting and escalation effectiveness;
- containment speed and effectiveness;
- investigation and evidence quality;
- eradication and recovery effectiveness;
- business and customer impact;
- communication and coordination;
- supplier performance where relevant;
- root cause and contributing factors;
- control gaps and failed safeguards;
- response capability and resource adequacy; and
- opportunities to prevent recurrence or reduce impact.

The review must focus on factual analysis and improvement rather than unsupported blame. It should distinguish root causes from contributing conditions and symptoms.

### 17.1 Corrective action tracking

Each corrective action must have:
- a unique identifier;
- a clear description and intended outcome;
- an accountable owner;
- a risk-based priority and target date;
- dependencies and required resources;
- evidence of completion;
- an effectiveness review where appropriate; and
- linkage to the originating incident.

Actions involving vulnerability remediation must be tracked under the Security Remediation and Patch Management Procedure. Material residual risks must be recorded and governed under the risk management process.

## 18. Incident Register and Status Model

Maintain a central incident register or approved equivalent. At minimum, it should record:
- incident identifier;
- reported and detected dates/times;
- source and reporter, subject to privacy restrictions;
- incident description and category;
- affected assets, services and business units;
- severity and confidence history;
- incident manager and accountable owner;
- key milestones and decisions;
- containment, eradication and recovery status;
- evidence references;
- legal, privacy and contractual assessment status;
- communication and notification status;
- residual risk;
- corrective actions;
- closure decision and date; and
- reopening or related incident references.

Suggested statuses:

| Status | Meaning |
|---|---|
| Reported | Received and registered; initial triage pending. |
| Triage | Validity, scope and severity are being assessed. |
| Suspected Incident | Credible concern exists; investigation or validation is ongoing. |
| Confirmed Incident | Incident criteria have been met and coordinated response is active. |
| Containment | Containment actions are being implemented or validated. |
| Investigation | Evidence analysis and scope determination are underway. |
| Eradication | Cause, malicious activity or unauthorized access is being removed. |
| Recovery | Services are being restored and validated. |
| Monitoring | Recovery is complete or substantially complete; heightened monitoring continues. |
| Pending Closure | Closure criteria and approvals are being reviewed. |
| Closed | Closure approved and remaining actions tracked separately. |
| Reopened | Previously closed incident requires renewed response. |
| Non-Incident | Authorized triage determined that the report does not meet incident criteria; rationale retained. |

The organization may adapt these statuses but must preserve clear distinctions between suspected, confirmed, active response, recovery and closed states.

## 19. Metrics and Management Reporting

Information Security should provide periodic incident reporting to the designated governance forum. Frequency, recipients and thresholds must be approved by the organization.

Possible measures include:
- incident count by category, severity and business unit;
- suspected versus confirmed incident volumes;
- time from detection to reporting;
- time from reporting to triage and assignment;
- time to containment;
- time to eradication and recovery;
- incidents involving sensitive information or critical services;
- recurring incidents and repeat root causes;
- incidents involving third parties;
- incidents with assessed notification obligations;
- evidence and record completeness;
- corrective actions open, overdue and completed;
- incident exercise findings and improvement closure; and
- response coverage and on-call readiness.

### 19.1 Metric interpretation

Define each metric, data source, reporting period, exclusions and calculation method. Report severity changes and material data limitations. Metrics must not create incentives to suppress reporting, downgrade incidents prematurely or close incidents before response objectives are met.

## 20. Records, Confidentiality and Retention

Incident records must be stored in approved repositories with access restricted to authorized personnel. Retention must follow the organization's records management policy and applicable legal, regulatory, contractual and litigation-hold requirements.

Records may include:
- original reports and intake records;
- triage and classification decisions;
- incident timeline and action log;
- investigation notes and technical findings;
- evidence register and custody records;
- system, network and application log references;
- forensic reports and specialist advice;
- containment, eradication and recovery approvals;
- change and remediation records;
- legal, privacy and notification assessments;
- internal and external communications;
- management updates and decisions;
- closure approval;
- post-incident review; and
- corrective action records.

Protect credentials, personal data, sensitive system details, exploit information, legal advice and privileged communications. Do not place passwords, private keys or other secrets in general incident reports. Use approved secure channels and repositories.

## 21. Quality Assurance and Exercises

The document owner or designated assurance function should periodically assess:
- compliance with reporting and escalation requirements;
- completeness and consistency of incident records;
- appropriateness of severity and reclassification decisions;
- authority and documentation for emergency actions;
- evidence handling and access controls;
- containment and recovery validation;
- notification assessment and approval records;
- closure quality and corrective-action tracking; and
- lessons learned from actual incidents and exercises.

Conduct periodic tabletop or technical exercises proportionate to the organization's risk and capabilities. Exercises should test contact routes, decision authority, incident classification, communications, evidence preservation, containment coordination, recovery dependencies and escalation. Record observations, gaps, owners and target dates. Exercise results must be clearly distinguished from actual incident records.

## 22. Exceptions to This Procedure

An exception must identify the specific requirement being varied, the reason, the resulting security and operational risk, compensating safeguards, approving authority, expiry or review date and record location.

An exception to a procedural requirement does not automatically constitute acceptance of the underlying security risk. Both decisions must be documented where applicable. Emergency actions taken under pre-approved authority are not procedural exceptions when they comply with the defined emergency process.

## 23. Review and Maintenance

The document owner must review this procedure at least annually and following material changes, including:
- changes to organizational structure or response authority;
- changes to critical systems, cloud services or business operations;
- changes to legal, regulatory or contractual requirements;
- material incidents or significant exercise findings;
- changes to threat environment or response capabilities; and
- audit findings indicating that the procedure is ineffective.

Revisions must be version-controlled, reviewed and approved under the organization's document governance process.

## 24. Adoption Checklist

Before this procedure becomes operational, the organization should:

- [ ] Assign the document owner and approving authority.
- [ ] Map response roles to actual teams and named positions.
- [ ] Establish primary and alternate reporting channels.
- [ ] Approve incident severity criteria and escalation thresholds.
- [ ] Define incident manager and emergency response authority.
- [ ] Establish on-call and out-of-hours response arrangements.
- [ ] Identify legal, privacy, compliance and communications contacts.
- [ ] Define supplier incident notification and escalation routes.
- [ ] Establish secure incident and evidence repositories.
- [ ] Align evidence collection with the Evidence Handling procedure.
- [ ] Align remediation with the Security Remediation and Patch Management Procedure.
- [ ] Define recovery approval and heightened monitoring requirements.
- [ ] Establish notification assessment and decision workflows.
- [ ] Configure the incident register and status model.
- [ ] Define retention, access and confidentiality requirements.
- [ ] Establish reporting metrics and governance cadence.
- [ ] Schedule response exercises and corrective-action reviews.
- [ ] Communicate reporting obligations to all relevant personnel.

---

# Appendix A - Security Incident Reporting Form

| Field | Entry |
|---|---|
| Report reference | [Assigned by receiving function] |
| Reporter name / role | [Details] |
| Safe contact method | [Contact details] |
| Date/time detected | [Date, time, time zone] |
| Date/time reported | [Date, time, time zone] |
| Affected asset / service / account | [Identifiers] |
| Location / business unit | [Details] |
| Description of observed activity | [Facts and observations] |
| Detection source | [Alert, user report, supplier, etc.] |
| Potential information affected | [Type and sensitivity, if known] |
| Known operational impact | [Details] |
| Evidence or alert references | [References] |
| Actions already taken | [Details] |
| Immediate safety or business concern | [Details] |
| Receiving person / date | [Details] |

# Appendix B - Initial Incident Triage Record

| Field | Entry |
|---|---|
| Incident ID | [Identifier] |
| Report reference | [Identifier] |
| Triage date/time | [Date/time/time zone] |
| Triage analyst | [Role / name] |
| Event description | [Summary] |
| Validation performed | [Checks and results] |
| Affected assets / accounts | [Known scope] |
| Potential CIA impact | [Confidentiality / integrity / availability] |
| Potential business / privacy / safety impact | [Details] |
| Initial classification | [Event / suspected / confirmed] |
| Severity and confidence | [Rating and rationale] |
| Immediate actions required | [Actions] |
| Incident manager | [Role / name] |
| Escalation made | [Recipient, time, outcome] |
| Outstanding questions | [Details] |
| Triage decision and reviewer | [Decision, role, date] |

# Appendix C - Incident Classification and Severity Assessment

| Dimension | Assessment |
|---|---|
| Confidentiality impact | [None / limited / material / severe / unknown] |
| Integrity impact | [None / limited / material / severe / unknown] |
| Availability impact | [None / limited / material / severe / unknown] |
| Information sensitivity / volume | [Details] |
| Asset and service criticality | [Details] |
| Privilege / account impact | [Details] |
| Scope and propagation | [Details] |
| External / third-party impact | [Details] |
| Safety implications | [Details] |
| Legal / regulatory / contractual implications | [Details] |
| Threat context | [Details] |
| Evidence confidence | [High / medium / low and rationale] |
| Overall severity | [Organization-approved category] |
| Escalation decision | [Details] |
| Decision-maker and date | [Details] |

# Appendix D - Incident Response Action and Decision Log

| Date/time and time zone | Action / decision | Objective / rationale | Affected assets | Authorized by | Implemented by | Outcome / evidence reference |
|---|---|---|---|---|---|---|
| [Timestamp] | [Details] | [Details] | [Assets] | [Role] | [Role] | [Outcome] |

# Appendix E - Containment Decision Record

| Field | Entry |
|---|---|
| Incident ID | [Identifier] |
| Proposed containment action | [Details] |
| Threat or impact addressed | [Details] |
| Scope and affected services | [Details] |
| Expected security benefit | [Details] |
| Business / safety impact | [Details] |
| Evidence preservation considerations | [Details] |
| Dependencies and alternatives | [Details] |
| Rollback / removal criteria | [Details] |
| Approval / emergency authority | [Role, name, date/time] |
| Implementer | [Role / name] |
| Actual result and validation | [Details] |
| Review date / owner | [Details] |

# Appendix F - Evidence Collection and Preservation Checklist

- [ ] Collection is within approved incident response authority.
- [ ] Source system, custodian and collection context are identified.
- [ ] Date/time and time zone are recorded.
- [ ] Volatile evidence implications are considered before shutdown or reboot.
- [ ] Original evidence is preserved where feasible.
- [ ] Working copies are used where appropriate.
- [ ] Collection tools, methods and versions are recorded.
- [ ] Integrity verification is applied proportionately.
- [ ] Evidence is labeled and linked to the incident.
- [ ] Transfers and custody are recorded where required.
- [ ] Access is restricted and logged where supported.
- [ ] Sensitive, personal and privileged information is protected.
- [ ] Evidence is stored in an approved repository.
- [ ] Limitations and collection gaps are documented.

# Appendix G - Incident Communication and Escalation Log

| Date/time | Sender | Recipient(s) | Channel | Purpose / approved message reference | Decision / response | Follow-up owner |
|---|---|---|---|---|---|---|
| [Timestamp] | [Role] | [Roles] | [Channel] | [Reference] | [Details] | [Owner] |

# Appendix H - Recovery Validation Checklist

- [ ] Scope of affected systems and services is understood.
- [ ] Malicious activity and known persistence have been addressed.
- [ ] Recovery source and backup integrity are assessed.
- [ ] Required patches and configuration corrections are applied.
- [ ] Credentials, keys, tokens and certificates are addressed as required.
- [ ] Access rights and privileged access are reviewed.
- [ ] Security controls are operational.
- [ ] Application and service health checks pass.
- [ ] Data integrity and availability are validated.
- [ ] Monitoring and alerting are active.
- [ ] Residual risks and limitations are documented.
- [ ] Heightened monitoring owner and review period are assigned.
- [ ] Business / service owner approval is recorded.
- [ ] Required security and incident authority approvals are recorded.

# Appendix I - Incident Closure Checklist

- [ ] Incident classification and severity history are recorded.
- [ ] Incident scope and impact are documented, including uncertainties.
- [ ] Containment actions are complete or transitioned to an approved control.
- [ ] Investigation findings and evidence references are retained.
- [ ] Eradication outcome is documented.
- [ ] Recovery validation and service approval are recorded.
- [ ] Legal, privacy, regulatory and contractual obligations were assessed.
- [ ] Required communications and notifications were actioned or dispositioned.
- [ ] Residual risks are recorded and assigned.
- [ ] Corrective actions have owners and target dates.
- [ ] Incident records are complete and stored appropriately.
- [ ] Closure recommendation and approval are recorded.
- [ ] Related incidents and findings are linked.

# Appendix J - Post-Incident Review and Lessons-Learned Report

| Field | Entry |
|---|---|
| Incident ID / title | [Identifier] |
| Severity | [Rating] |
| Review date | [Date] |
| Review facilitator / participants | [Roles] |
| Executive summary | [Summary] |
| What happened | [Factual chronology] |
| Detection and reporting | [Effectiveness and gaps] |
| Containment | [Effectiveness and gaps] |
| Investigation and evidence | [Effectiveness and gaps] |
| Eradication and recovery | [Effectiveness and gaps] |
| Business / customer impact | [Details] |
| Root cause | [Evidence-supported conclusion] |
| Contributing factors | [Details] |
| What worked well | [Details] |
| What did not work well | [Details] |
| Lessons learned | [Details] |
| Corrective actions | [Action IDs, owners, target dates] |
| Residual risk | [Details] |
| Reviewer / approval | [Role, name, date] |

# Appendix K - Incident Register Template

| Incident ID | Reported date | Category | Affected service / asset | Severity | Status | Incident manager | Business owner | Containment date | Recovery date | Notification assessment | Corrective actions | Closure date |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| [ID] | [Date] | [Category] | [Asset/service] | [Rating] | [Status] | [Owner] | [Owner] | [Date] | [Date] | [Pending / assessed / notified / not required] | [References] | [Date] |

# Appendix L - Incident Response Exercise Record

| Field | Entry |
|---|---|
| Exercise ID / title | [Identifier] |
| Exercise type | [Tabletop / technical / simulation] |
| Date and scope | [Details] |
| Scenario objectives | [Details] |
| Participants and roles | [Details] |
| Capabilities tested | [Reporting, triage, escalation, containment, evidence, recovery, etc.] |
| Decisions and observations | [Details] |
| Gaps identified | [Details] |
| Corrective actions and owners | [References] |
| Target dates | [Dates] |
| Exercise outcome | [Summary] |
| Approver | [Role / name / date] |

# Appendix M - Related Repository Documents

Read this procedure with the applicable current versions of:
- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `docs/policies/information-security-policy.md`
- `docs/procedures/security-assessment-authorization-procedure.md`
- `docs/procedures/vulnerability-assessment-procedure.md`
- `docs/procedures/security-remediation-and-patch-management-procedure.md`
- `templates/risk-register-template.md`
- `templates/assessment-report-template.md`
- `templates/technical-assessment-checklist.md`
- `templates/evidence-register-template.md`

# Appendix N - Reference Frameworks

The organization may use relevant editions and updates of:
- NIST Cybersecurity Framework (CSF) 2.0.
- NIST SP 800-61, Computer Security Incident Handling Guide.
- NIST SP 800-53, Security and Privacy Controls for Information Systems and Organizations.
- ISO/IEC 27001 and ISO/IEC 27002.
- ISO/IEC 27035 series, Information security incident management.
- CIS Critical Security Controls.
- Relevant national cybersecurity, privacy and sectoral guidance.
- Applicable legal, regulatory, contractual and supplier requirements.

References provide guidance and do not, by themselves, establish organizational compliance or replace applicable obligations.

---

**End of document**
