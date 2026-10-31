# Security Assessment Authorization Procedure

## Document Control

| Field | Value |
|---|---|
| Document owner | [Information Security / designated function] |
| Approving authority | [Authorized approving authority] |
| Version | 1.0 |
| Status | Template — requires organizational adoption |
| Effective date | [YYYY-MM-DD] |
| Review date | [YYYY-MM-DD] |
| Classification | [Organization-defined classification] |
| Related policy | `docs/policies/information-security-policy.md` |
| Related methodology | `docs/methodology/risk-assessment-methodology.md` |
| Related evidence procedure | `docs/methodology/evidence-handling.md` |

> **Adoption notice:** This organization-neutral template must be tailored, assigned approval authorities, and formally approved before operational use. No job title, system role, contract, or technical access is assumed to confer assessment-authorization authority.

## 1. Purpose

This procedure governs the request, review, authorization, preparation, execution, change, suspension, and closure of security assessments. It ensures that each assessment has a documented purpose, accountable sponsor, precise scope, explicit authorization, appropriate safeguards, auditable decisions, and controlled evidence handling.

## 2. Scope and Applicability

### 2.1 Covered activities

This procedure applies to internal and external assessments performed by employees, contractors, consultants, and other approved parties, including:

- cybersecurity and information-security risk assessments;
- vulnerability assessments and authorized scanning;
- infrastructure, network, server, endpoint, and virtualization reviews;
- application, API, database, and configuration assessments;
- cloud, hosted, and externally managed service assessments;
- security-control design, implementation, and operating-effectiveness reviews;
- authorized penetration testing and controlled proof-of-concept validation;
- internal and external assessments; and
- third-party assessments where the necessary permissions have been obtained.

### 2.2 Activities requiring specific additional approval

The following require explicit approval in the authorization and rules of engagement, and may require additional legal, privacy, safety, contractual, operational, or third-party approval:

- exploitation beyond non-destructive validation;
- privilege escalation or lateral movement;
- denial-of-service, stress, load, or resilience testing;
- activity likely to interrupt, degrade, or materially alter production services;
- access to, collection, copying, or extraction of production or personal data;
- modification or deletion of data, configurations, accounts, or system state;
- malware simulation, payload execution, persistence, or command-and-control simulation;
- phishing, social engineering, credential-harvesting simulations, or impersonation;
- physical security testing or entry into restricted premises;
- testing safety-related, operational technology, or industrial control environments;
- testing systems owned or operated by another organization; and
- any activity outside the approved scope or ordinary assessment method.

Approval of an assessment does not automatically authorize every technique that might be used.

### 2.3 Exclusions

This procedure does not independently authorize incident response, threat hunting, forensic activity outside an approved mandate, law-enforcement activity, production remediation, or access to systems and information not expressly included in the authorization. Where assessment activity overlaps with incident response, the responsible functions shall agree on command, evidence handling, and operational priorities. Incident-response authority must not be assumed to authorize penetration testing or unrelated assessment work.

## 3. Governing Principles

1. **Explicit authorization:** No assessment activity begins before the required written authorization is complete and effective.
2. **Defined scope:** Targets, locations, accounts, environments, dates, techniques, and exclusions are unambiguous.
3. **Least impact:** Use the least intrusive method capable of meeting the approved objective.
4. **Need-to-know:** Access to systems, credentials, data, and results is limited to authorized personnel.
5. **Accountability:** Approvals, decisions, scope changes, exceptions, and stop-work actions are recorded.
6. **Proportionality:** Assessment depth and safeguards reflect criticality, exposure, sensitivity, and operational context.
7. **Recovery readiness:** Where an activity may change system state, recovery arrangements and decision authority are agreed in advance.
8. **No implied permission:** Reachability, possession of credentials, prior access, or a general contract does not substitute for specific authorization.
9. **Stop-work authority:** Personnel may stop activity when safety, service, scope, or authorization conditions are uncertain or breached.
10. **Evidence integrity:** Evidence is collected and handled under the approved evidence-handling procedure.

## 4. Roles and Responsibilities

Local governance shall identify the actual authorized individuals or bodies. Functional titles alone do not establish delegated authority.

| Role | Responsibilities |
|---|---|
| Requestor | Submits the request, states the purpose, identifies known targets and constraints |
| Assessment sponsor | Owns the business need, secures resources, coordinates stakeholders |
| Assessment lead | Defines the approach, prepares the plan and ROE, directs the team, maintains records |
| Asset/service owner | Validates scope, ownership, dependencies, constraints, and impact considerations |
| Operations representative | Reviews windows, monitoring, backups, recovery, and change controls |
| Information security authority | Reviews objectives, methodology, risks, safeguards, and security governance |
| Formal authorizing authority | Approves or declines the assessment within documented delegated authority |
| Privacy/legal/compliance representative | Reviews applicable privacy, legal, regulatory, contractual, and records requirements |
| Third-party owner/provider | Authorizes assets and services under its control, where required |
| Safety/OT authority | Reviews safety-critical, industrial, physical, or operational technology activity |
| Assessment team member | Performs only approved activities, protects information, records evidence, escalates deviations |
| Risk owner | Owns risks arising from the assessed system or activity |
| Quality reviewer | Conducts proportionate review of scope, evidence, findings, and closure |

### 4.1 Separate owner approval from formal authorization

Asset-owner approval confirms that the owner has reviewed and agreed to the proposed assessment of assets or services under their responsibility. It does not, by itself, constitute formal organizational authorization.

Formal authorization must be issued by the person or body holding documented authority to permit the assessment. If one person legitimately holds both responsibilities, the record must evidence each approval capacity separately.

### 4.2 External assessors

External assessors shall be covered by approved contractual, confidentiality, data-protection, and security terms. Such documents supplement but do not replace the assessment-specific authorization and rules of engagement.

## 5. Assessment Request and Initiation

### 5.1 Request submission

The requestor shall submit a request before scheduling or performing assessment activity. Include, as applicable:

- assessment title and unique reference;
- requestor, sponsor, business unit, and contact details;
- business purpose, drivers, objectives, and expected outcomes;
- assessment type and desired assurance level;
- systems, services, applications, networks, locations, and environments;
- asset/service owners and affected internal or external parties;
- proposed assessment team and subcontractors;
- proposed dates, duration, time zone, and operating windows;
- dependencies, critical services, and operational constraints;
- expected access, credentials, data, and connectivity requirements;
- proposed techniques and tools, including intrusive techniques;
- known risks, previous incidents, and relevant change activity;
- required third-party, legal, privacy, safety, or regulatory approvals; and
- requested deliverables and distribution.

Incomplete requests shall be returned or marked pending. A request is not authorization to begin work.

### 5.2 Initial screening

The coordinating function shall assign a reference, confirm governance remit, identify the sponsor and owners, identify affected stakeholders, determine whether another process applies, identify specialist reviews and external permissions, and confirm whether the request is sufficiently complete.

A request may be rejected, deferred, or returned where it lacks a valid purpose, accountable ownership, feasible scope, or required information.

## 6. Scope Definition

### 6.1 Required scope elements

The assessment lead, requestor, and relevant owners shall document scope precisely enough for the team and operators to identify what is and is not authorized. Include, as applicable:

- hostnames, FQDNs, IP addresses/ranges, URLs, APIs, application identifiers, cloud account/subscription/project identifiers, database identifiers, and physical locations;
- environment designation (development, test, staging, disaster recovery, production);
- ownership and hosting/provider arrangements;
- network boundaries, trust relationships, connected systems, and dependencies;
- authorized accounts, roles, authentication methods, and access paths;
- approved source IPs, test infrastructure, and assessor locations;
- in-scope processes, data sets, and interfaces;
- explicit out-of-scope assets, tenants, services, data, and locations;
- third-party and shared-service boundaries;
- dates, time zone, permitted days/hours, and blackout periods;
- assumptions, constraints, limitations, and scope-validation method.

Avoid ambiguous descriptions such as “all servers” or “the corporate network” unless exact boundaries are attached and approved.

### 6.2 Scope register

| ID | Asset/service | Environment | Owner | Scope status | Approved activity | Constraints / notes |
|---|---|---|---|---|---|---|
| [S-001] | [Hostname / service] | [Production / test] | [Owner] | In scope | [Specific tests] | [Restrictions] |
| [S-002] | [Third-party service] | [Environment] | [Provider] | Out of scope / conditional | [None until separately approved] | [Reason / approval dependency] |

Conditional targets remain excluded until the stated approval condition is met and recorded.

### 6.3 Scope validation

The asset/service owner or documented delegate shall validate scope accuracy and the organization's authority to permit the activity. The assessment lead shall check target identifiers and ensure test infrastructure cannot unintentionally affect excluded systems.

## 7. Methodology and Permitted Activities

### 7.1 Assessment plan

The assessment lead shall document objectives, methodology and criteria, phases and sequence, techniques/tools/automation, required privileges, expected interactions and state changes, data that may be accessed, evidence to be produced, safeguards and monitoring, contingency/recovery arrangements, and reporting/escalation arrangements.

The method shall be proportionate to the objectives, asset criticality, and approved risk limits.

### 7.2 Activity authorization matrix

Each activity must be designated permitted, prohibited, or conditional. Conditional activities require additional approval before execution.

| Activity | Default treatment | Required control |
|---|---|---|
| Passive review of supplied documentation/configuration | May be permitted | Confirm access and confidentiality |
| Non-intrusive discovery and enumeration | Conditional | Approve targets, rate limits, source addresses, window |
| Authenticated configuration review | Conditional | Approve accounts, privileges, and data access |
| Vulnerability scanning | Conditional | Approve profile, targets, rate, exclusions, monitoring |
| Active probing/service interaction | Conditional | Approve methods, limits, targets, safeguards |
| Exploit validation | Explicit approval required | Define exploit class, proof threshold, stop conditions |
| Privilege escalation/lateral movement | Explicit approval required | Define boundaries, accounts, paths, limits |
| Denial-of-service/stress testing | Prohibited unless separately approved | Dedicated impact, resilience, safety, recovery approval |
| Data extraction/bulk collection | Prohibited unless separately approved | Define data, volume, destination, protection, deletion |
| Data/configuration modification or deletion | Prohibited unless separately approved | Define changes, backup, rollback, change approval |
| Phishing/social engineering | Explicit approval required | Approve population, messages, timing, data, safeguards |
| Physical testing | Explicit approval required | Approve premises, boundaries, safety, local contacts |
| Malware/payload/persistence simulation | Explicit approval required | Approve behavior, containment, monitoring, removal |
| Third-party asset testing | Not permitted without third-party authority | Obtain written authorization from party with control |
| Safety-critical/OT testing | Not permitted without specialist approval | Obtain safety/OT approval and safe operating limits |

This matrix is a governance baseline, not automatic permission. The signed authorization and ROE must specify activities approved for the particular assessment.

### 7.3 Tool and infrastructure control

Maintain an inventory of material tools and infrastructure, including scanners, test accounts, scripts, payloads, cloud resources, remote access paths, and storage locations where relevant. Configure tools to minimize unintended impact. New tools, infrastructure, destinations, or techniques require review and authorization.

## 8. Risk and Operational Impact Review

Before authorization, the assessment lead and relevant owners shall assess foreseeable impacts and define safeguards. Consider:

- service availability, performance, and capacity;
- data confidentiality, integrity, and availability;
- system stability, failover, backups, and recovery;
- safety, physical security, and environmental impacts;
- privacy and personal-data exposure;
- legal, regulatory, contractual, and licensing restrictions;
- shared infrastructure and multi-tenant effects;
- third-party dependencies and provider notification;
- operational schedules, business peaks, and blackout periods;
- detection, alerting, and incident-response coordination;
- credential exposure and privileged access;
- evidence storage, transfer, retention, and disposal; and
- reputational or business consequences of unintended effects.

Safeguards may include target allowlists, conservative rates/concurrency, maintenance windows, dedicated least-privilege accounts, verified recovery points, monitoring, named contacts, provider coordination, data minimization, secure evidence repositories, test-environment substitution, and pre-agreed stop-work thresholds.

Risks beyond delegated authority shall be escalated to the designated risk owner or approving authority. Risk acceptance must be explicit, documented, and consistent with organizational risk governance. Assessment authorization does not automatically accept risks discovered during the assessment.

## 9. Approval Workflow

Complete the following gates in sequence unless an approved organizational workflow defines equivalent controls.

| Gate | Required action | Evidence / output |
|---|---|---|
| 1. Request | Submit and register request | Completed request and reference |
| 2. Scope/method review | Define targets, exclusions, activities, methods | Approved scope and assessment plan |
| 3. Owner/operations review | Obtain owner and operational input | Recorded approvals and impact review |
| 4. Specialist review | Obtain privacy, legal, compliance, safety, provider approvals as needed | Written approvals or documented non-applicability |
| 5. Formal authorization | Authorizing authority approves or rejects | Authenticated authorization |
| 6. Readiness | Confirm prerequisites, contacts, access, monitoring, safeguards | Completed readiness checklist |
| 7. Execution | Conduct only approved activity | Execution log and evidence register |
| 8. Closure | Revoke access, reconcile assets/data, report and close | Closure record and deliverables |

### 9.1 Formal authorization requirements

The authorization shall identify:

- assessment and unique reference;
- authorizing authority and basis of delegated authority;
- sponsor, assessment lead, and authorized team;
- approved scope, plan, and ROE versions;
- start/end dates, time zone, and operating windows;
- permitted and prohibited activities;
- additional approvals and conditions;
- operational contacts and escalation routes;
- stop-work authority and emergency suspension arrangements;
- evidence and data-handling requirements;
- reporting, notification, and closure expectations; and
- approval date, effective date, expiry, and limitations.

Retain authorization in an auditable form. Email may be used only where organizational policy recognizes it as an authenticated approval record and it clearly identifies scope, activities, conditions, and the approving authority.

### 9.2 Validity

Authorization applies only to the named assessment, scope, team, methods, and stated period. It is not transferable, reusable, or blanket permission. Expired, withdrawn, suspended, incomplete, or ambiguous authorization is not valid authority to continue.

## 10. Rules of Engagement

An approved rules-of-engagement (ROE) document shall be in place before execution. It may be incorporated into the authorization or attached as a controlled record.

At minimum, the ROE shall define:

1. reference, purpose, objectives, and scope;
2. authorized personnel and source infrastructure;
3. targets and exclusions;
4. dates, time zone, and operating hours;
5. permitted tools, techniques, and test profiles;
6. prohibited and conditional activities;
7. credential handling and account restrictions;
8. data access, collection, storage, transfer, and deletion;
9. operational safeguards, rate and concurrency limits;
10. monitoring and coordination;
11. emergency contacts and escalation;
12. stop-work triggers and restart authority;
13. incident/suspected-compromise notification;
14. scope-change and reauthorization process;
15. evidence and reporting requirements;
16. third-party/provider coordination; and
17. completion and access-revocation steps.

Unless explicitly approved in writing, the team shall not test out-of-scope or third-party assets; disrupt services; alter or delete production data/configuration; collect data beyond the approved minimum; create persistence or backdoors; deploy uncontrolled payloads; use credentials outside the approved purpose; conduct social engineering or physical testing; bypass safety controls; conceal activity where coordination is required; share evidence with unauthorized persons; or continue after expiry or a stop-work instruction.

## 11. Pre-Assessment Readiness

The assessment lead shall complete a readiness review immediately before execution and confirm that no material condition has changed.

- [ ] Formal authorization is approved, effective, and unexpired.
- [ ] Scope register and exclusions are final and available to all team members.
- [ ] ROE is approved and understood.
- [ ] Owner, operations, third-party, privacy, legal, compliance, and safety approvals are recorded as applicable.
- [ ] Team identities and contact details are confirmed.
- [ ] Access and test accounts are approved, tested, and least-privileged.
- [ ] Source IPs, tools, scripts, and infrastructure are approved.
- [ ] Monitoring and operational contacts are available.
- [ ] Backup, recovery, and rollback arrangements are confirmed where relevant.
- [ ] Rate limits, concurrency, and safeguards are configured.
- [ ] Evidence storage and transfer locations are approved and access-controlled.
- [ ] Data-handling, privacy, and retention instructions are understood.
- [ ] Emergency contacts and stop-work process are confirmed.
- [ ] Change freezes, blackout periods, and dependencies have been checked.
- [ ] No material system, scope, threat, or operational change invalidates the review.

If a required condition is not met, do not begin until resolved or formally addressed by the appropriate authority without waiving mandatory authorization requirements.

## 12. Execution Controls

The assessment lead shall ensure that:

- work remains within approved targets, methods, windows, and limits;
- team members understand scope and ROE;
- material actions and events are logged with timestamps and context;
- unexpected systems or data are not pursued without approval;
- evidence is handled under the evidence-handling procedure;
- credentials and sensitive information are protected;
- operational contacts are informed of material events as agreed;
- unexpected degradation or security events are escalated promptly;
- changes to tools, techniques, infrastructure, or personnel are reviewed;
- deviations are recorded and assessed for reauthorization; and
- activity ceases at authorization expiry or on a stop-work instruction.

Maintain an execution log sufficient to reconstruct material actions, decisions, interruptions, and communications. Detail should be proportionate to intrusiveness and risk.

## 13. Stop-Work and Emergency Suspension

### 13.1 Triggers

Any team member may call for an immediate pause if they reasonably believe that:

- an out-of-scope asset or unauthorized data has been accessed;
- a service is degraded, unstable, or unavailable;
- activity is producing unexpected or potentially harmful effects;
- a safety, physical security, privacy, or legal concern has arisen;
- credentials, evidence, or sensitive information may be exposed;
- required monitoring or operational contacts are unavailable;
- activity conflicts with scope or ROE;
- authorization is expired, withdrawn, or in doubt;
- an actual security incident is suspected; or
- an owner or authorized operational representative requests suspension.

### 13.2 Immediate response

The team shall stop the relevant activity, avoid further interaction with affected targets, preserve relevant logs/evidence without expanding access or impact, notify the assessment lead and operational contact, record time/trigger/assets/actions/effects, and follow emergency or incident-response instructions.

Where immediate action is necessary to prevent harm, prioritize safety and containment and notify the responsible authority as soon as practicable.

### 13.3 Restart

The ROE shall identify who may authorize restart. Restart requires confirmation that the cause is understood, safeguards are adequate, authorization remains valid, and additional approvals are complete. Material changes may require amended or new authorization.

## 14. Scope Changes and Reauthorization

Document and review a scope or method change before the changed activity begins. Changes requiring review include adding/removing assets or locations; changing dates or windows; adding personnel or source infrastructure; introducing tools or techniques; increasing test intensity; moving from passive to active testing; increasing privileges or data access; changing data-handling arrangements; changing safeguards/recovery assumptions; or changes in ownership, provider terms, criticality, or operating conditions.

The assessment lead shall pause or avoid the affected activity, describe the change and rationale, assess risks and approvals, obtain updated owner/specialist approvals, obtain formal authorization, update scope/plan/ROE/readiness records, and communicate the approved change.

Verbal direction may initiate an immediate safety pause but is not sufficient approval for expanded testing. Emergency verbal approval for a change is acceptable only where an approved emergency process expressly permits it and the decision is promptly authenticated and documented.

## 15. Assessment Closure

### 15.1 Closure requirements

At completion or termination, the assessment lead shall:

- stop assessment activity and confirm the authorization period has ended;
- remove or disable temporary accounts, keys, tokens, agents, services, and access paths;
- decommission or secure temporary test infrastructure and scripts;
- reconcile collected data/evidence against the approved handling plan;
- transfer deliverables to approved recipients;
- delete temporary copies and working data when authorized and no longer required;
- report retained data, unresolved access, unexpected changes, and deviations;
- notify owners and operational contacts;
- document incidents, stop-work events, changes, and exceptions;
- record findings, risks, limitations, and follow-up actions;
- obtain required quality review and closure acknowledgement; and
- close the assessment record in the designated repository.

### 15.2 Closure record

Record the assessment reference, scope, dates, team, completed and uncompleted activities, approved deviations, service impacts/incidents, evidence and deliverable locations, access/resource revocation, data disposition, unresolved issues and owners, findings/risk references, limitations, notifications, and closure approval.

Do not mark an assessment fully closed while material access, evidence, data-disposition, or safety issues remain unresolved unless the closure authority documents outstanding items, owners, and approved disposition.

## 16. Exceptions and Emergency Authorization

### 16.1 Exceptions

Exceptions must be justified, risk-assessed, documented, time-limited where appropriate, and approved by an authority with explicit delegated power. An exception cannot authorize unlawful activity or override mandatory external requirements.

Record the requirement, justification, affected assessment/assets/parties, risks and compensating controls, duration/expiry, accountable owner, approving authority, and review/closure conditions.

### 16.2 Emergency authorization

Emergency status does not remove the need for accountable authorization. The organization shall define who may request and approve emergency activity, minimum scope and methods, operational/incident-response coordination, safeguards and stop-work triggers, maximum validity, authentication/recording, and the owner/deadline for retrospective documentation.

If valid authority cannot be established, the activity shall not proceed. Emergency incident-response authority must not be assumed to include penetration testing or unrelated assessment activity.

## 17. Records, Evidence, and Retention

Store assessment records in an approved repository with access controls appropriate to classification and sensitivity. Records may include the request, scope and owner validation, plan/methodology, impact review, specialist and third-party approvals, authorization and ROE, readiness checklist, execution logs, communications, changes, exceptions, stop-work records, evidence register/items, findings, risk records, reports, access-revocation and data-disposition records, closure, and quality review.

Retention periods, legal holds, archival requirements, and secure disposal shall follow organizational records-management and legal requirements. This procedure establishes no universal retention period.

Handle evidence under the approved evidence-handling procedure. Restrict raw evidence to personnel with a defined need. Do not place sensitive evidence in public repositories, personal storage, or unapproved collaboration platforms.

## 18. Compliance and Quality Review

The coordinating function or quality reviewer shall conduct proportionate checks that authorization preceded activity; scope and exclusions were precise; approvals came from appropriate authorities; ROE reflected approved activity; readiness prerequisites were met; execution stayed within scope; deviations and stop-work events were handled; evidence was protected; temporary access/resources were revoked; closure records were complete; and lessons learned were captured where useful.

Record and escalate non-compliance through organizational governance. Material unauthorized activity may require incident handling, legal review, personnel/supplier escalation, and suspension of further assessment work.

## 19. Review and Maintenance

The document owner shall review this procedure at an organization-defined interval and after material changes to delegated authority, law/regulation/contracts/standards, significant incidents, technology/hosting/provider arrangements, audit findings, or related policies and methodologies. Changes shall be version-controlled, reviewed, approved, and communicated before taking effect.

---

# Appendix A — Assessment Request Form

| Field | Entry |
|---|---|
| Assessment reference | [Assigned by coordinating function] |
| Assessment title / request date | [Title] / [Date] |
| Requestor / business unit | [Name / unit] |
| Sponsor | [Name / role] |
| Business purpose and objectives | [Purpose, drivers, questions] |
| Assessment type | [Risk / vulnerability / technical / application / penetration / control review / other] |
| Proposed dates and time zone | [Details] |
| Proposed assessment lead/team | [Names / organization] |
| Target systems/services | [List or attachment] |
| Asset/service owners | [Names / roles] |
| Third parties involved | [Providers / dependencies] |
| Proposed methods and tools | [Summary] |
| Intrusive activities requested | [List or none] |
| Data access anticipated | [Types and sensitivity] |
| Operational constraints | [Windows, blackouts, dependencies] |
| Specialist reviews required | [Privacy / legal / safety / compliance / provider / other] |
| Requested deliverables | [Reports, findings, evidence] |
| Sponsor acknowledgement | [Name, date, approval reference] |

# Appendix B — Scope Register Template

| ID | Asset/service identifier | Description | Environment | Owner | Scope status | Permitted activity | Exclusions / constraints | Owner validation |
|---|---|---|---|---|---|---|---|---|
| [S-001] | [FQDN/IP/URL/resource ID] | [Description] | [Prod/test/etc.] | [Owner] | [In/out/conditional] | [Specific activity] | [Limits] | [Name/date] |

**Scope notes:** Approved source IPs/test infrastructure: [Details]. Authorized accounts/roles: [Details]. Network/trust boundaries: [Details]. Third-party boundaries/approvals: [Details]. Time zone/windows: [Details]. Explicit exclusions: [Details]. Assumptions/limitations: [Details].

# Appendix C — Formal Authorization Record

| Field | Entry |
|---|---|
| Assessment reference / title | [Reference / title] |
| Sponsor / assessment lead | [Names / roles] |
| Authorized team | [Names / organization] |
| Scope attachment/version | [Reference/version] |
| Assessment plan/version | [Reference/version] |
| ROE/version | [Reference/version] |
| Permitted activities | [Explicit list] |
| Prohibited activities | [Explicit list] |
| Conditional approvals | [Conditions and evidence] |
| Start/end date, time, and zone | [Details] |
| Approved windows | [Details] |
| Operational safeguards | [Summary/reference] |
| Emergency contacts | [Names/channels] |
| Stop-work / restart authority | [Roles/names] |
| Evidence/data handling | [Reference] |
| Reporting/notification | [Requirements] |
| Conditions/limitations | [Details] |
| Authorizing authority | [Name/role] |
| Delegated authority reference | [Policy/delegation] |
| Decision | [Approved / rejected / deferred] |
| Approval date/authentication | [Date/record] |
| Expiry/withdrawal conditions | [Details] |

# Appendix D — Rules of Engagement Template

## D1. Engagement details

- Assessment reference and objectives: [Details]
- Assessment lead and team: [Names/organizations]
- Approved targets and scope version: [Reference]
- Excluded targets: [List]
- Approved source infrastructure: [Details]
- Dates, time zone, and windows: [Details]

## D2. Permitted techniques

| Technique | Permitted? | Limits / conditions | Additional approval |
|---|---|---|---|
| Passive review | [Yes/No] | [Limits] | [Reference] |
| Discovery/enumeration | [Yes/No] | [Limits] | [Reference] |
| Vulnerability scanning | [Yes/No] | [Profile/rate/targets] | [Reference] |
| Authenticated testing | [Yes/No] | [Accounts/privileges] | [Reference] |
| Exploit validation | [Yes/No] | [Proof/restrictions] | [Reference] |
| Privilege escalation | [Yes/No] | [Limits] | [Reference] |
| Data access/extraction | [Yes/No] | [Data/volume/destination] | [Reference] |
| Social engineering | [Yes/No] | [Population/limits] | [Reference] |
| Physical testing | [Yes/No] | [Premises/limits] | [Reference] |
| DoS/stress testing | [Yes/No] | [Dedicated safeguards] | [Reference] |

## D3. Operations and communications

- Rate/concurrency limits: [Details]
- Monitoring arrangements: [Details]
- Primary operational contact: [Name/channel]
- Escalation and emergency contacts: [Name/channel]
- Stop-work triggers and restart authority: [Details]
- Incident notification process: [Details]
- Backup/recovery arrangements: [Details]

## D4. Data and evidence

- Data permitted/prohibited: [Details]
- Evidence repository and authorized recipients: [Details]
- Transfer method: [Approved method]
- Retention/disposal: [Policy/reference]
- Sensitive-data handling: [Requirements]

## D5. Acknowledgement

| Party | Name / role | Approval / acknowledgement | Date |
|---|---|---|---|
| Assessment lead | [Name] | [Record] | [Date] |
| Asset/service owner | [Name] | [Record] | [Date] |
| Operations representative | [Name] | [Record] | [Date] |
| Formal authorizing authority | [Name] | [Record] | [Date] |

# Appendix E — Risk and Operational Impact Review

| Risk / impact scenario | Affected asset/service | Likelihood/impact | Safeguard | Owner | Residual concern / approval |
|---|---|---|---|---|---|
| [Example: scan causes service degradation] | [Target] | [Assessment] | [Rate limit/window/monitoring] | [Owner] | [Decision] |

Review the impact areas in Section 8. Record any non-applicable area and the reason.

# Appendix F — Readiness Checklist

- [ ] Authorization valid and complete
- [ ] Scope and exclusions distributed
- [ ] ROE approved and understood
- [ ] Owner and specialist approvals complete
- [ ] Third-party permissions verified
- [ ] Team and contacts confirmed
- [ ] Accounts/access validated
- [ ] Tools and source infrastructure approved
- [ ] Monitoring and operational contacts available
- [ ] Safeguards, backups, and recovery confirmed
- [ ] Evidence repository and handling ready
- [ ] Time window and blackout checks complete
- [ ] Stop-work/restart process understood
- [ ] No material change invalidates approval

Readiness decision: [Ready / Not ready]  
Assessment lead: [Name]  
Date/time/time zone: [Details]  
Outstanding conditions: [Details]

# Appendix G — Scope Change / Reauthorization Request

| Field | Entry |
|---|---|
| Assessment reference | [Reference] |
| Requested by / date | [Name / date] |
| Existing authorization version | [Reference/version] |
| Proposed change and reason | [Description] |
| Affected assets/methods/dates | [Details] |
| New risks and impacts | [Assessment] |
| Required owner/specialist approvals | [List] |
| Updated scope/ROE/plan references | [References] |
| Formal decision | [Approved / rejected / deferred] |
| Authorizing authority | [Name/role] |
| Effective date/time | [Details] |

**Control:** Do not execute changed activity until required approvals and formal reauthorization are effective.

# Appendix H — Stop-Work Record

| Field | Entry |
|---|---|
| Assessment reference | [Reference] |
| Date/time/time zone | [Details] |
| Raised by | [Name/role] |
| Trigger/reason | [Description] |
| Affected assets/activities | [Details] |
| Immediate actions | [Details] |
| Potential impact | [Details] |
| Notifications | [Names/times] |
| Evidence preserved | [References] |
| Incident process invoked? | [Yes/No/reference] |
| Corrective actions/conditions | [Details] |
| Restart decision and authority | [Decision/name/date] |

# Appendix I — Closure Record

| Field | Entry |
|---|---|
| Assessment reference/title | [Reference/title] |
| Execution period | [Start/end] |
| Assessment lead | [Name] |
| Activities completed/not completed | [Summary/reasons] |
| Scope changes/deviations | [References] |
| Stop-work events/incidents | [References] |
| Findings/risk-register references | [References] |
| Deliverables/repository locations | [References] |
| Temporary access revoked | [Yes/No/details] |
| Temporary resources removed | [Yes/No/details] |
| Evidence reconciled/transferred | [Yes/No/details] |
| Data disposition completed | [Yes/No/details] |
| Outstanding issues and owners | [Details] |
| Quality review | [Name/outcome] |
| Closure decision | [Closed / conditionally closed / open] |
| Approver/date | [Name/date] |

# Appendix J — Emergency Authorization Record

| Field | Entry |
|---|---|
| Emergency reference / requestor | [Reference / name] |
| Emergency rationale | [Description] |
| Threat/urgency | [Description] |
| Minimum required scope | [Targets] |
| Proposed activity and exclusions | [Details] |
| Risks and safeguards | [Details] |
| Incident-response coordination | [Details] |
| Authorizing authority and basis | [Name/delegation] |
| Approval authentication | [Record] |
| Effective period/expiry | [Details] |
| Required notifications | [Details] |
| Retrospective documentation owner/deadline | [Details] |
| Closure/review outcome | [Details] |

## Appendix K — Related Repository Documents

- `docs/policies/information-security-policy.md`
- `docs/methodology/assessment-lifecycle.md`
- `docs/methodology/risk-assessment-methodology.md`
- `docs/methodology/risk-scoring-model.md`
- `docs/methodology/evidence-handling.md`
- `templates/risk-register-template.md`
- `templates/assessment-report-template.md`
- `templates/technical-assessment-checklist.md`
- `templates/evidence-register-template.md`

## Appendix L — Reference Frameworks

Potential reference material includes NIST CSF 2.0; NIST SP 800-30; NIST SP 800-37; NIST SP 800-53; NIST SP 800-115; NIST SP 800-61; ISO/IEC 27001, 27002, and 27005; CIS Critical Security Controls; and applicable OWASP testing guidance.

Confirm the current edition, organizational adoption, and applicability before relying on a reference. Referencing a standard does not establish certification, compliance, or conformity.

## Document Approval

| Approval role | Name | Decision | Signature / authenticated record | Date |
|---|---|---|---|---|
| Document owner | [Name] | [Recommend / other] | [Record] | [Date] |
| Information security authority | [Name] | [Approve / reject] | [Record] | [Date] |
| Formal approving authority | [Name] | [Approve / reject] | [Record] | [Date] |
