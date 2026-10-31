# Technical Assessment Checklist

> **Document type:** Reusable technical assessment fieldwork checklist  
> **Suggested repository path:** `templates/technical-assessment-checklist.md`  
> **Status:** Template — tailor and approve for organizational use before operational adoption  
> **Version:** 1.1  
> **Assessment ID:** `[ASSESS-YYYY-###]`  
> **Owner:** `[Organization / function]`  
> **Classification:** `[Organization-defined]`

## Instructions for use

This modular checklist supports authorized technical assessments across twelve technical domains plus cross-cutting controls: infrastructure and asset inventory; network security; endpoints; servers and virtualization; applications; identity and access management; databases; vulnerability assessment; logging and monitoring; backup and resilience; cloud and containers; and configuration management/compliance mapping. Use only modules applicable to the approved scope and assessment objectives.

1. Confirm authorization, scope, rules of engagement, safety constraints, and escalation contacts before beginning.
2. Assign a stable assessment ID and record the applicable assets, procedures, criteria, and assessors.
3. For each applicable check, record the actual result, rationale, evidence references, limitations, and follow-up.
4. Do not treat an untested check or a lack of evidence as a pass.
5. Link substantiated issues to finding IDs, risk IDs, treatment actions, and the assessment report.
6. Do not place credentials, secrets, or unnecessary sensitive information in this checklist. Reference approved evidence storage locations.
7. Follow organizational policy for evidence handling, classification, retention, and disposal.
8. Tailor checks to the relevant technology, version, approved baseline, and authorized test methods.

### Related framework documents

- [Assessment lifecycle](../docs/methodology/assessment-lifecycle.md)
- [Risk assessment methodology](../docs/methodology/risk-assessment-methodology.md)
- [Risk scoring model](../docs/methodology/risk-scoring-model.md)
- [Evidence handling](../docs/methodology/evidence-handling.md)
- [Standards and frameworks register](../references/standards-and-frameworks.md)
- [Assessment report template](assessment-report-template.md)
- [Risk register template](risk-register-template.md)

This checklist does not grant authorization, establish compliance, or independently prove that an environment is secure.

---

## 1. Assessment identification and authorization

### 1.1 Engagement details

| Field | Value |
|---|---|
| Assessment ID | `[ASSESS-YYYY-###]` |
| Assessment title | `[Title]` |
| Assessment type | `[Infrastructure / network / endpoint / server / application / control / other]` |
| Lead assessor | `[Role / team]` |
| Assessment team | `[Roles / teams]` |
| Sponsor / requester | `[Role / function]` |
| System / service owner | `[Role / function]` |
| Start and end dates | `[YYYY-MM-DD to YYYY-MM-DD]` |
| Applicable time zone | `[Time zone]` |
| Authorization reference | `[Approval / rules-of-engagement ID]` |
| Report ID | `[REPORT-YYYY-### / Pending]` |
| Classification | `[Organization-defined]` |
| Evidence register location | `[Approved repository reference]` |

### 1.2 Authorization and rules of engagement

- [ ] Written authorization is recorded and covers the planned activity.
- [ ] In-scope assets, addresses, services, environments, and owners are identified.
- [ ] Exclusions and third-party boundaries are documented.
- [ ] Permitted and prohibited techniques are documented.
- [ ] Testing windows, availability constraints, and change-control requirements are understood.
- [ ] Required accounts, permissions, and access approvals are in place.
- [ ] Operational contacts and escalation routes are available.
- [ ] Stop conditions and incident-escalation procedures are agreed.
- [ ] Evidence collection, storage, access, transfer, and retention requirements are defined.
- [ ] Assessment criteria and applicable baseline versions are selected.

**Authorization limitations / special conditions:** `[Record details or None]`

**Stop and escalate if:** the activity exceeds scope, creates unexpected service impact, encounters an unapproved third-party asset, suggests an active incident requiring separate handling, or raises evidence-preservation concerns.

### 1.3 Scope inventory

| Asset / item ID | Description | Owner | Environment / network zone | In scope? | Approved procedures | Notes / exclusions |
|---|---|---|---|---|---|---|
| `[ASSET-###]` | `[System / service]` | `[Role]` | `[Zone / environment]` | `[Yes / No]` | `[Procedure IDs]` | `[Notes]` |

---

## 2. Result conventions and recording rules

Use one status for each check that was assessed.

| Result | Meaning |
|---|---|
| **Pass** | The stated criterion was met based on sufficient evidence for the check performed. |
| **Fail** | A material deviation from the criterion was identified. |
| **Partial** | Some requirements were met, but a gap or limitation remains. |
| **Not Tested** | The check was not performed; record the reason and follow-up decision. |
| **Not Applicable** | The check does not apply to the approved scope; record a rationale where necessary. |
| **Blocked** | The check could not proceed because of an authorization, access, dependency, safety, or operational constraint. |

Do not treat `Not Tested`, `Blocked`, or missing evidence as `Pass`. A check result describes the test performed; it does not by itself establish a risk rating or compliance conclusion.

### Standard verification record

Copy this structure for each check, or use it as the column definition for a tabular working copy.

| Field | Entry |
|---|---|
| Check ID | `[e.g., NET-001]` |
| Domain / objective | `[Control objective]` |
| Applicable assets | `[Asset IDs]` |
| Verification procedure | `[Procedure / assessor prompt]` |
| Expected condition / criterion | `[Approved baseline, policy, control objective, or other criterion]` |
| Result | `[Pass / Fail / Partial / Not Tested / Not Applicable / Blocked]` |
| Actual observation and rationale | `[What was observed and how result was determined]` |
| Evidence IDs | `[EVD-### references]` |
| Assessor / date | `[Role and YYYY-MM-DD]` |
| Limitations / confidence | `[Constraints and confidence rationale]` |
| Finding ID | `[FIND-### / None / Pending triage]` |
| Risk ID | `[RISK-### / None / Pending assessment]` |
| Follow-up / owner / due date | `[Action, role, date, or None]` |
| Reviewer | `[Role / date / Pending]` |

---

## 3. Planning and readiness checklist

| Check ID | Verification item | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|
| PLAN-001 | Objectives and assessment questions are defined | Approved objectives and success criteria | `[Result]` | `[References]` |
| PLAN-002 | Scope and exclusions are documented | Approved scope / asset list | `[Result]` | `[References]` |
| PLAN-003 | Asset owners and business criticality are identified | Inventory and ownership records | `[Result]` | `[References]` |
| PLAN-004 | Applicable standards, policies, and baselines are selected | Versioned criteria register | `[Result]` | `[References]` |
| PLAN-005 | Permitted procedures and constraints are documented | Rules of engagement / authorization | `[Result]` | `[References]` |
| PLAN-006 | Test accounts and access rights are approved | Access approvals and role definitions | `[Result]` | `[References]` |
| PLAN-007 | Test windows and change restrictions are confirmed | Change / maintenance plan | `[Result]` | `[References]` |
| PLAN-008 | Operational contacts and stop conditions are available | Contact and escalation record | `[Result]` | `[References]` |
| PLAN-009 | Evidence repository and handling requirements are ready | Approved storage and access controls | `[Result]` | `[References]` |
| PLAN-010 | Assessment team understands incident and forensic escalation triggers | Briefing / procedure reference | `[Result]` | `[References]` |

**Readiness decision:** `[Ready / Ready with documented conditions / Not ready]`  
**Decision owner and date:** `[Role / YYYY-MM-DD]`  
**Conditions or blockers:** `[Details]`

---

## 4. Module A — Infrastructure and asset inventory

Use the applicable checks for inventory and infrastructure assessment. Adapt the criterion to the asset type and approved baseline.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| INF-001 | Inventory completeness and ownership | Compare approved inventory with authorized discovery or system records | Identified assets have owners and stable identifiers | `[Result]` | `[References]` |
| INF-002 | Asset classification and criticality | Review classification and service criticality records | Classification follows approved policy | `[Result]` | `[References]` |
| INF-003 | Environment and network-zone assignment | Compare asset records with approved architecture and network documentation | Assignment matches the documented design or an approved exception | `[Result]` | `[References]` |
| INF-004 | Hardware and software inventory | Review installed components and inventory records | Material components are recorded and maintained | `[Result]` | `[References]` |
| INF-005 | Support lifecycle | Review vendor / owner lifecycle information | Unsupported components are identified and managed under approved plans | `[Result]` | `[References]` |
| INF-006 | Secure configuration baseline | Compare relevant settings with the approved baseline | Deviations are documented and dispositioned | `[Result]` | `[References]` |
| INF-007 | Management interfaces | Review authorized management paths and access restrictions | Management access is limited to approved paths and roles | `[Result]` | `[References]` |
| INF-008 | Unidentified or unauthorized assets | Reconcile approved scope with collected inventory evidence | Discrepancies are investigated and tracked | `[Result]` | `[References]` |
| INF-009 | Configuration drift | Compare current state with approved configuration records | Material drift is detected, explained, and managed | `[Result]` | `[References]` |
| INF-010 | Inventory reconciliation | Review ownership and update history | Inventory has an accountable maintenance process | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 5. Module B — Network security

Only assess authorized network devices, segments, services, and paths. Use the agreed methods and avoid disruptive tests unless explicitly approved.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| NET-001 | Network zones and trust boundaries are documented | Compare diagrams and configurations with the approved architecture | Boundaries and permitted flows are documented | `[Result]` | `[References]` |
| NET-002 | Segmentation is implemented as intended | Review relevant rules and perform only authorized connectivity validation | Observed flows align with approved segmentation requirements | `[Result]` | `[References]` |
| NET-003 | Firewall / access-control rules have a business purpose | Sample rules, owners, justifications, and approvals | Rules are justified, authorized, and reviewable | `[Result]` | `[References]` |
| NET-004 | Administrative interfaces are appropriately restricted | Review management-plane configuration and permitted sources | Access is limited to approved management paths and roles | `[Result]` | `[References]` |
| NET-005 | Unnecessary services and ports are identified | Review approved service inventory and authorized observations | Exposure is justified and deviations are tracked | `[Result]` | `[References]` |
| NET-006 | Secure management protocols and configurations are used | Review applicable configuration and baseline | Approved secure management requirements are met | `[Result]` | `[References]` |
| NET-007 | Network-device privileged access is governed | Review accounts, roles, authentication, and approvals | Privileges and authentication follow approved requirements | `[Result]` | `[References]` |
| NET-008 | Network configuration changes are recorded | Review change records and configuration history | Material changes are authorized and traceable | `[Result]` | `[References]` |
| NET-009 | Logging and monitoring cover relevant network events | Review enabled logging, forwarding, retention rules, and samples | Required events are captured and handled under policy | `[Result]` | `[References]` |
| NET-010 | Configuration backup and recovery are addressed | Review backup evidence and approved recovery requirements | Configurations can be restored under the defined process | `[Result]` | `[References]` |
| NET-011 | Wireless controls are appropriate where in scope | Review approved wireless configuration and access controls | Wireless security follows applicable baseline | `[Result]` | `[References]` |
| NET-012 | Remote and third-party connectivity is governed | Review connection inventory, approvals, and access restrictions | Connectivity is authorized, limited, and periodically reviewed | `[Result]` | `[References]` |
| NET-013 | Rule exceptions are approved and reviewed | Review exception records, owners, expiry, and compensating controls | Exceptions are documented and governed | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 6. Module C — Endpoints and workstations

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| END-001 | Operating system is supported | Review OS version and lifecycle status | Unsupported systems are identified and managed under approved plans | `[Result]` | `[References]` |
| END-002 | Patch status meets approved requirements | Review update status and applicable exceptions | Patch state aligns with policy and risk-based requirements | `[Result]` | `[References]` |
| END-003 | Secure configuration baseline is applied | Compare selected settings with the approved baseline | Deviations are documented and dispositioned | `[Result]` | `[References]` |
| END-004 | Endpoint protection is installed and healthy where required | Review agent status, policy, and alert records | Required protection is operating and monitored | `[Result]` | `[References]` |
| END-005 | Local administrator privileges are restricted | Review local group membership and approvals | Privileges are justified, authorized, and reviewable | `[Result]` | `[References]` |
| END-006 | Authentication configuration follows policy | Review applicable authentication and lockout settings | Settings meet the approved requirements | `[Result]` | `[References]` |
| END-007 | Host firewall is configured where required | Review policy and effective state | Required rules and profiles are active | `[Result]` | `[References]` |
| END-008 | Remote-access settings are controlled | Review enabled services, access rules, and approvals | Remote access is limited to approved needs | `[Result]` | `[References]` |
| END-009 | Disk encryption is enabled where required | Review encryption state and key-management evidence without exposing keys | Required devices are protected under policy | `[Result]` | `[References]` |
| END-010 | Application installation and execution controls are applied where required | Review policy and effective configuration | Approved restrictions are implemented or exceptions documented | `[Result]` | `[References]` |
| END-011 | Security logs and time synchronization are adequate | Review logging policy, samples, and time source | Required events and reliable timestamps are available | `[Result]` | `[References]` |
| END-012 | Removable-media controls are applied where required | Review policy, configuration, and exception records | Use is governed by approved requirements | `[Result]` | `[References]` |
| END-013 | Configuration exceptions and drift are tracked | Compare observed state with baseline and exception register | Deviations have owners and disposition | `[Result]` | `[References]` |
| END-014 | Recovery requirements are addressed where applicable | Review recovery procedures and evidence | Required recovery controls are documented and tested as applicable | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 7. Module D — Servers and virtualization

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| SRV-001 | Server OS and platform are supported | Review version and lifecycle information | Unsupported components are identified and governed | `[Result]` | `[References]` |
| SRV-002 | Patching and secure configuration meet approved requirements | Review patch state and baseline comparison | Deviations are justified and tracked | `[Result]` | `[References]` |
| SRV-003 | Administrative access is limited to approved roles | Review group membership, role assignment, and approval records | Privileged access is justified and least-privilege requirements are applied | `[Result]` | `[References]` |
| SRV-004 | Privileged authentication follows policy | Review applicable configuration and authentication evidence | Approved privileged-authentication controls are applied | `[Result]` | `[References]` |
| SRV-005 | Management plane is restricted | Review management interfaces, access paths, and network restrictions | Only approved management paths and identities are permitted | `[Result]` | `[References]` |
| SRV-006 | Unnecessary services and components are identified | Compare service inventory with approved purpose | Unneeded exposure is removed or approved | `[Result]` | `[References]` |
| SRV-007 | Logging and monitoring are enabled as required | Review event configuration, forwarding, and samples | Required events are captured and reviewed | `[Result]` | `[References]` |
| SRV-008 | Backup and restoration controls are evidenced | Review backup status, recovery procedures, and authorized test records | Required recovery objectives and controls are addressed | `[Result]` | `[References]` |
| SRV-009 | Virtual machine isolation and configuration are appropriate | Review hypervisor / VM settings and architecture | Isolation and resource settings align with the approved baseline | `[Result]` | `[References]` |
| SRV-010 | Hypervisor and management-platform access is controlled | Review roles, accounts, authentication, and management exposure | Administrative access is limited and governed | `[Result]` | `[References]` |
| SRV-011 | Storage permissions and data protection are appropriate | Review access controls and applicable encryption settings | Access and protection meet approved requirements | `[Result]` | `[References]` |
| SRV-012 | Configuration backups and changes are traceable | Review backup and change records | Changes are authorized and recovery material is protected | `[Result]` | `[References]` |
| SRV-013 | Availability and recovery dependencies are documented where in scope | Review architecture and recovery evidence | Critical dependencies and recovery arrangements are understood | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 8. Module E — Applications and application services

Adapt these checks to the application architecture, technology, approved criteria, and authorized test scope.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| APP-001 | Application, owner, and environment are identified | Review application inventory and ownership records | Application and accountable owner are recorded | `[Result]` | `[References]` |
| APP-002 | Development, test, and production boundaries are controlled where applicable | Review environment design and access controls | Separation follows approved requirements | `[Result]` | `[References]` |
| APP-003 | Authentication controls meet requirements | Review configuration and authorized test evidence | Authentication behavior aligns with approved criteria | `[Result]` | `[References]` |
| APP-004 | Authorization and role boundaries are enforced | Review role definitions and authorized test results | Users and services receive only approved permissions | `[Result]` | `[References]` |
| APP-005 | Session management follows applicable requirements | Review session configuration and authorized behavior checks | Session handling meets the selected baseline | `[Result]` | `[References]` |
| APP-006 | Administrative functions are restricted | Review administrative endpoints, roles, and approvals | Privileged functions are accessible only to approved identities | `[Result]` | `[References]` |
| APP-007 | Secrets and credentials are handled securely | Review approved secret-management configuration without exposing secret values | Secrets are not unnecessarily embedded or disclosed and access is controlled | `[Result]` | `[References]` |
| APP-008 | Input validation and relevant application-security controls are addressed | Review applicable design, code, configuration, or authorized test evidence | Applicable criteria are met or deviations documented | `[Result]` | `[References]` |
| APP-009 | Dependencies and components are maintained | Review dependency inventory and vulnerability / update process | Relevant components are inventoried and maintained | `[Result]` | `[References]` |
| APP-010 | Error handling avoids unnecessary sensitive disclosure | Review authorized test outputs and application configuration | Responses do not unnecessarily expose sensitive internal details | `[Result]` | `[References]` |
| APP-011 | Security logging and monitoring are adequate | Review logging requirements, event samples, and alert handling | Relevant events are recorded and handled under policy | `[Result]` | `[References]` |
| APP-012 | Sensitive data access and protection are governed | Review authorization, data-handling controls, and applicable encryption | Access and handling align with requirements | `[Result]` | `[References]` |
| APP-013 | Deployment and configuration changes are controlled | Review deployment pipeline, approvals, and rollback arrangements | Changes are traceable and appropriately authorized | `[Result]` | `[References]` |
| APP-014 | Security testing and remediation are tracked | Review test results, finding records, and retest evidence | Findings are tracked through an approved process | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 9. Module F — Identity and access management

Assess identity stores, authentication services, directories, federation, privileged access, and service identities only within the approved scope.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| IAM-001 | Identity sources and trust relationships are inventoried | Review directory, identity-provider, federation, and application integration records | Authoritative identity sources and trust relationships are documented | `[Result]` | `[References]` |
| IAM-002 | Joiner, mover, and leaver processes are effective | Sample approved lifecycle records against account state | Access changes and removals are timely, authorized, and traceable | `[Result]` | `[References]` |
| IAM-003 | Authentication requirements are enforced | Review policy and authorized configuration evidence | Authentication meets the approved assurance requirements | `[Result]` | `[References]` |
| IAM-004 | Multi-factor authentication is applied where required | Review policy coverage and sampled enforcement evidence | Required user and privileged access paths enforce MFA or approved exceptions | `[Result]` | `[References]` |
| IAM-005 | Privileged accounts are identified and controlled | Review privileged groups, role assignments, and approvals | Privileged access is limited, justified, and periodically reviewed | `[Result]` | `[References]` |
| IAM-006 | Service accounts and non-human identities are governed | Review ownership, purpose, permissions, credential lifecycle, and interactive-login restrictions | Identities have owners, least privilege, and managed credentials | `[Result]` | `[References]` |
| IAM-007 | Dormant, orphaned, and shared accounts are addressed | Review account inventory and approved exception records | Unneeded accounts are disabled or removed; shared use is controlled and attributable | `[Result]` | `[References]` |
| IAM-008 | Password, lockout, and credential controls meet policy | Review effective configuration and applicable identity-provider settings | Settings align with approved policy and current threat requirements | `[Result]` | `[References]` |
| IAM-009 | Access reviews are performed | Sample review attestations and resulting changes | Reviews occur at defined intervals and exceptions are resolved | `[Result]` | `[References]` |
| IAM-010 | Federation, SSO, and token trust are configured securely | Review trust configuration, signing/key lifecycle, audience, and redirect restrictions | Trust is explicit, scoped, and protected against unauthorized use | `[Result]` | `[References]` |
| IAM-011 | Emergency and break-glass access is controlled | Review custody, approvals, monitoring, and post-use review | Emergency access is restricted, logged, and reviewed after use | `[Result]` | `[References]` |
| IAM-012 | Authentication and authorization events are logged | Review event coverage, forwarding, and sample records | Required events are attributable and available to monitoring processes | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 10. Module G — Database security

Select checks appropriate to the database engine, deployment model, data classification, and approved configuration baseline. Do not extract or expose production data or secrets unless explicitly authorized and necessary.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| DB-001 | Database instances, versions, owners, and data classifications are inventoried | Review CMDB, platform inventory, and data-owner records | Instances have accountable owners and documented purpose/classification | `[Result]` | `[References]` |
| DB-002 | Database engine and components are supported | Review vendor lifecycle and installed component versions | Unsupported components are subject to approved risk treatment | `[Result]` | `[References]` |
| DB-003 | Administrative access is restricted | Review database roles, privileged accounts, and access paths | Administrative access is limited to approved roles and managed paths | `[Result]` | `[References]` |
| DB-004 | Application and user permissions follow least privilege | Review grants, roles, schemas, and service identities | Permissions are limited to documented business and technical requirements | `[Result]` | `[References]` |
| DB-005 | Default, dormant, and unnecessary accounts are addressed | Review account inventory and configuration | Unneeded/default accounts are disabled, removed, or governed by approved exception | `[Result]` | `[References]` |
| DB-006 | Authentication and credential storage meet requirements | Review authentication configuration and secret-management integration | Credentials are protected and authentication follows policy | `[Result]` | `[References]` |
| DB-007 | Network exposure is restricted | Review listeners, firewall rules, TLS endpoints, and authorized connectivity evidence | Database access is limited to approved application and administration paths | `[Result]` | `[References]` |
| DB-008 | Encryption in transit and at rest is applied where required | Review configuration and key-management evidence without collecting key material | Protection meets data classification and policy requirements | `[Result]` | `[References]` |
| DB-009 | Sensitive data access and privileged activity are auditable | Review audit configuration and representative records | Required access and administrative events are captured and protected | `[Result]` | `[References]` |
| DB-010 | Patching and configuration hardening are governed | Compare version/configuration with approved baseline and change records | Updates and deviations are managed through approved processes | `[Result]` | `[References]` |
| DB-011 | Backup, restore, and recovery controls are validated | Review backup protection, restore-test evidence, and recovery objectives | Backups are protected and restoration is tested at required intervals | `[Result]` | `[References]` |
| DB-012 | Database changes and schema deployments are controlled | Review change approvals, deployment records, and rollback arrangements | Material changes are authorized, traceable, and recoverable | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 11. Module H — Vulnerability assessment and security testing

This module addresses the governance and quality of vulnerability identification and validation. Technical exploitation, intrusive validation, and authenticated testing require explicit authorization and agreed safety controls.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| VUL-001 | Assessment coverage is mapped to the approved asset scope | Compare scanner targets and manual test scope with authorized inventory | In-scope assets are covered; exclusions and unreachable assets are recorded | `[Result]` | `[References]` |
| VUL-002 | Scanner profiles and credentials are approved and appropriate | Review configuration, credential handling, and authorization | Profiles match objectives; credentials are protected and least-privileged | `[Result]` | `[References]` |
| VUL-003 | Scanner engines and detection content are current | Review engine, plugin, signature, and feed status | Tooling is maintained and version details are recorded | `[Result]` | `[References]` |
| VUL-004 | Scan windows and operational safeguards are defined | Review rules of engagement, schedules, exclusions, and stop conditions | Testing is scheduled and constrained to approved conditions | `[Result]` | `[References]` |
| VUL-005 | Discovery and scan coverage limitations are documented | Review logs, authentication status, reachability, and coverage reports | Failed authentication, excluded checks, and blind spots are disclosed | `[Result]` | `[References]` |
| VUL-006 | Findings are deduplicated and normalized | Review asset identifiers, plugin IDs, and finding records | Duplicate observations are consolidated without losing affected-asset detail | `[Result]` | `[References]` |
| VUL-007 | Material findings are validated proportionately | Review manual validation records or corroborating evidence | False positives are assessed; validation does not exceed authorization | `[Result]` | `[References]` |
| VUL-008 | Severity reflects technical and business context | Review CVSS or other scoring, exposure, exploitability, asset criticality, and compensating controls | Severity rationale follows the approved classification methodology | `[Result]` | `[References]` |
| VUL-009 | Known exploited and actively exploited issues are considered | Review authoritative threat intelligence and applicable organizational criteria | Relevant exploitation context informs prioritization | `[Result]` | `[References]` |
| VUL-010 | Vulnerability exceptions and risk acceptance are governed | Review approval, rationale, compensating controls, owner, and expiry | Exceptions are explicit, time-bound where appropriate, and reviewed | `[Result]` | `[References]` |
| VUL-011 | Remediation is tracked to verified closure | Sample remediation records and retest evidence | Closure is based on verification, not ticket status alone | `[Result]` | `[References]` |
| VUL-012 | Assessment output is reproducible and retained appropriately | Review report metadata, tool versions, timestamps, and evidence references | Results can be interpreted and traced subject to evidence-handling rules | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 12. Module I — Security logging and monitoring

Assess the controls that generate, transport, protect, retain, monitor, and respond to security-relevant events. Avoid collecting unnecessary personal or sensitive content.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| LOG-001 | Logging requirements are defined for critical assets and services | Review logging standards, asset tiers, and use cases | Required event sources and minimum coverage are documented | `[Result]` | `[References]` |
| LOG-002 | Security-relevant events are generated | Review source configuration and representative event samples | Required authentication, privilege, configuration, and security events are captured | `[Result]` | `[References]` |
| LOG-003 | Event timestamps are reliable and synchronized | Review time-source configuration and timestamp samples | Time synchronization supports reliable event correlation | `[Result]` | `[References]` |
| LOG-004 | Logs are centrally collected where required | Review forwarding configuration, ingestion status, and source coverage | Required sources reach approved collection and monitoring platforms | `[Result]` | `[References]` |
| LOG-005 | Log integrity and access are protected | Review access controls, administrative separation, and integrity safeguards | Unauthorized alteration or deletion is restricted and detectable | `[Result]` | `[References]` |
| LOG-006 | Retention and disposal meet requirements | Review retention configuration, legal/contractual obligations, and disposal controls | Retention is approved, enforced, and appropriate to classification | `[Result]` | `[References]` |
| LOG-007 | Alerts and detection use cases address relevant threats | Review use-case catalogue, alert logic, and test evidence | Priority threats have proportionate, maintained detections | `[Result]` | `[References]` |
| LOG-008 | Alert triage and escalation are defined | Sample alert records and escalation procedures | Alerts have ownership, triage criteria, and escalation paths | `[Result]` | `[References]` |
| LOG-009 | Monitoring coverage gaps are identified and managed | Compare source inventory with SIEM/monitoring coverage | Missing, delayed, or unhealthy sources are detected and tracked | `[Result]` | `[References]` |
| LOG-010 | Monitoring platform access and administration are governed | Review roles, privileged access, change history, and service accounts | Access is restricted, attributable, and reviewed | `[Result]` | `[References]` |
| LOG-011 | Detection rules and dashboards are maintained | Review ownership, change approvals, tuning, and periodic review | Content is versioned, tested, and updated as threats and systems change | `[Result]` | `[References]` |
| LOG-012 | Monitoring performance and service health are measured | Review ingestion delay, source availability, alert backlog, and service metrics | Operational issues are visible and managed against defined objectives | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 13. Module J — Backup, recovery, and resilience

Assess backup and recovery controls against approved recovery objectives, data criticality, and business continuity requirements. A backup job marked successful is not sufficient evidence of recoverability.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| BCP-001 | Critical services and recovery requirements are identified | Review business impact analysis, service inventory, RTO/RPO, and owner approvals | Recovery requirements are approved and traceable to business needs | `[Result]` | `[References]` |
| BCP-002 | Backup scope covers required systems and data | Compare backup policy and job coverage with asset/data inventory | Required assets, configurations, and data are included | `[Result]` | `[References]` |
| BCP-003 | Backup frequency and retention meet approved objectives | Review schedules, retention settings, and policy | Frequency and retention align with approved RPO and obligations | `[Result]` | `[References]` |
| BCP-004 | Backup repositories and management planes are protected | Review access, network isolation, encryption, and administrative controls | Backups are protected against unauthorized access and common compromise paths | `[Result]` | `[References]` |
| BCP-005 | Immutable/offline or equivalent resilience controls are applied where required | Review configuration and evidence of protection against alteration/deletion | Required resilience controls are implemented and independently governed | `[Result]` | `[References]` |
| BCP-006 | Backup failures and anomalies are monitored | Review job failures, alerts, escalation, and corrective actions | Failures are detected, assigned, and resolved | `[Result]` | `[References]` |
| BCP-007 | Restore tests are performed and documented | Review test scope, results, integrity checks, and lessons learned | Restoration is demonstrated at defined intervals and against requirements | `[Result]` | `[References]` |
| BCP-008 | Recovery procedures and dependencies are maintained | Review runbooks, contacts, credentials custody, and dependencies | Procedures are current, accessible, and assigned to responsible roles | `[Result]` | `[References]` |
| BCP-009 | Disaster recovery arrangements are exercised | Review exercise plans, outcomes, and tracked improvements | Exercises validate relevant scenarios and actions are tracked | `[Result]` | `[References]` |
| BCP-010 | Backup and recovery exceptions are approved | Review exception rationale, owner, compensating controls, and expiry | Exceptions are documented and accepted by authorized roles | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 14. Module K — Cloud, containers, and hosted platforms

Use only for cloud services, container platforms, managed services, and hosted environments included in the approved scope. Establish the applicable shared-responsibility boundary before testing.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| CLD-001 | Cloud services, subscriptions, accounts, and owners are inventoried | Review provider inventories, billing/management records, and ownership | Services and accountable owners are known and classified | `[Result]` | `[References]` |
| CLD-002 | Shared-responsibility boundaries are documented | Review provider terms, architecture, and service model | Customer and provider control responsibilities are clear | `[Result]` | `[References]` |
| CLD-003 | Organization/account hierarchy and guardrails are governed | Review tenant, organization, subscription, project, and policy configuration | Central guardrails restrict risky configurations and unauthorized deployments | `[Result]` | `[References]` |
| CLD-004 | Cloud IAM roles and trust policies follow least privilege | Review role bindings, federation, service identities, and privilege escalation paths | Permissions are justified, scoped, and periodically reviewed | `[Result]` | `[References]` |
| CLD-005 | Public exposure and network paths are controlled | Review security groups, routes, gateways, endpoints, and public-access settings | Exposure is intentional, approved, and minimized | `[Result]` | `[References]` |
| CLD-006 | Storage services enforce access and data protection | Review bucket/container policies, public access, encryption, and logging | Data access is restricted and protection follows classification | `[Result]` | `[References]` |
| CLD-007 | Cloud secrets and keys are governed | Review secret/key-management configuration, rotation, access, and audit | Secrets and keys are centrally protected and access is attributable | `[Result]` | `[References]` |
| CLD-008 | Container images and registries are secured | Review image provenance, scanning, registry access, and lifecycle | Images are trusted, assessed, and maintained under policy | `[Result]` | `[References]` |
| CLD-009 | Container runtime and orchestration controls are appropriate | Review admission controls, workload identity, isolation, privileges, and API access | Workloads run with least privilege and approved isolation controls | `[Result]` | `[References]` |
| CLD-010 | Cloud audit and security telemetry are enabled | Review provider audit logs, control-plane events, and central forwarding | Required events are retained and monitored | `[Result]` | `[References]` |
| CLD-011 | Cloud configuration posture and drift are monitored | Review posture-management findings, policy compliance, and remediation | Misconfigurations and drift are detected and managed | `[Result]` | `[References]` |
| CLD-012 | Hosted service resilience and exit dependencies are understood | Review backup, recovery, portability, and provider dependency records | Availability, recovery, and material exit risks are addressed | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 15. Module L — Configuration management and compliance mapping

This module verifies the governance and evidence behind configuration baselines and control claims. A checklist result is not, by itself, a formal certification or legal compliance opinion.

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| CFG-001 | Applicable security baselines are selected and version-controlled | Review baseline register, scope, version, and approval | Baselines are approved, current, and applicable to assessed technologies | `[Result]` | `[References]` |
| CFG-002 | Baseline ownership and exception authority are assigned | Review governance records and responsibility matrix | Owners and approval authorities are explicit | `[Result]` | `[References]` |
| CFG-003 | Baseline settings are mapped to technical configuration | Sample baseline requirements against effective system settings | Requirements have testable implementation criteria | `[Result]` | `[References]` |
| CFG-004 | Configuration changes are authorized and traceable | Sample change requests, approvals, deployment, and rollback records | Material changes are controlled and auditable | `[Result]` | `[References]` |
| CFG-005 | Configuration drift is detected and triaged | Review compliance scans, configuration monitoring, and exceptions | Drift is identified, assigned, and dispositioned | `[Result]` | `[References]` |
| CFG-006 | Deviations have documented risk treatment | Review exception/risk records, compensating controls, and expiry | Deviations are approved by authorized risk owners | `[Result]` | `[References]` |
| CFG-007 | Control mappings preserve source and scope | Review mapping between internal controls and external frameworks | Mappings identify the source requirement and do not imply equivalence without analysis | `[Result]` | `[References]` |
| CFG-008 | Compliance evidence is current and attributable | Sample evidence owner, date, scope, and validity | Evidence supports only the control assertion and period stated | `[Result]` | `[References]` |
| CFG-009 | Control design and operating effectiveness are distinguished | Review test method and evidence for design vs operation | Conclusions distinguish documented design from demonstrated operation | `[Result]` | `[References]` |
| CFG-010 | Corrective actions from control reviews are tracked | Review findings, owners, due dates, and verification records | Gaps are tracked through verified closure or approved acceptance | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 16. Module M — Cross-cutting security controls

| Check ID | Verification item | Verification approach | Expected evidence / criterion | Result | Evidence IDs / notes |
|---|---|---|---|---|---|
| CTRL-001 | Identity lifecycle is governed | Review joiner, mover, leaver, and access-review evidence | Access changes are authorized and timely under policy | `[Result]` | `[References]` |
| CTRL-002 | Privileged accounts are identified and governed | Review privileged-account inventory, approvals, and reviews | Privileged identities have accountable owners and suitable controls | `[Result]` | `[References]` |
| CTRL-003 | Authentication requirements are applied | Review relevant configuration and approved test evidence | Controls meet applicable requirements | `[Result]` | `[References]` |
| CTRL-004 | Vulnerability management is operating | Review scanning / assessment records, triage, and remediation tracking | Vulnerabilities are assessed and managed under policy | `[Result]` | `[References]` |
| CTRL-005 | Security logging and monitoring requirements are met | Review logging coverage, alert handling, and retention rules | Required events and response processes are evidenced | `[Result]` | `[References]` |
| CTRL-006 | Configuration baselines and exceptions are governed | Review baseline versions, drift records, and approvals | Deviations have documented decisions and owners | `[Result]` | `[References]` |
| CTRL-007 | Backup and recovery controls are evidenced | Review policy, backup results, and applicable restoration tests | Recovery requirements are addressed | `[Result]` | `[References]` |
| CTRL-008 | Incident escalation pathways are understood | Review procedures, contacts, and relevant exercise / incident records | Escalation and responsibilities are documented | `[Result]` | `[References]` |
| CTRL-009 | Security policies and procedures are implemented in the assessed technical scope | Compare technical state with relevant approved requirements | Implementation evidence supports the conclusion | `[Result]` | `[References]` |
| CTRL-010 | Third-party access and dependencies are governed where applicable | Review access agreements, permissions, and monitoring | Access and dependencies are approved and managed | `[Result]` | `[References]` |
| CTRL-011 | Control owners and review responsibilities are identified | Review control register and assignment records | Accountability and review arrangements are documented | `[Result]` | `[References]` |
| CTRL-012 | Remediation and exceptions are tracked | Review action, exception, and acceptance records | Decisions and follow-up are traceable | `[Result]` | `[References]` |

**Module notes / exclusions:** `[Details]`

---

## 17. Evidence register and evidence-gap tracking

### 10.1 Evidence register

Use the organization's authoritative evidence register where one exists. The table below is a working index, not a substitute for approved evidence storage.

| Evidence ID | Related check / finding | Asset ID | Description / source | Collector | Collection date / time zone | Tool / procedure | Validation / integrity reference | Sensitivity / location | Limitations |
|---|---|---|---|---|---|---|---|---|---|
| `[EVD-###]` | `[Check / finding IDs]` | `[Asset ID]` | `[Description]` | `[Role]` | `[Timestamp]` | `[Tool / version / procedure]` | `[Validation, hash, custody reference, or N/A with rationale]` | `[Classification and approved location]` | `[Limitations]` |

### 10.2 Evidence-gap register

| Gap ID | Related check / finding | Missing / contradictory evidence | Effect on conclusion / confidence | Alternative validation | Owner | Follow-up date / status |
|---|---|---|---|---|---|---|
| `[GAP-###]` | `[IDs]` | `[Description]` | `[Effect]` | `[Alternative or None]` | `[Role]` | `[Date / status]` |

### 10.3 Evidence quality prompts

- [ ] Collection was authorized and within the approved scope.
- [ ] Source, collector, date/time, and method are recorded where material.
- [ ] Material results are validated or corroborated proportionately.
- [ ] Original evidence and working copies are distinguished where relevant.
- [ ] Integrity verification and chain-of-custody records are applied where justified or required.
- [ ] Sensitive data and secrets are not unnecessarily copied into this checklist.
- [ ] Missing, incomplete, stale, or contradictory evidence is recorded.
- [ ] Evidence is stored, transferred, retained, and disposed of under approved requirements.
- [ ] Evidence references support the specific observation, control conclusion, or risk judgment claimed.

Follow `evidence-handling.md` for the full procedure, including preservation, secure transfer, chain of custody where warranted, and escalation for potential incident, legal, disciplinary, regulatory, forensic, or tampering concerns.

---

## 18. Findings, risk, and remediation linkage

### 11.1 Triage rules

A `Fail` or `Partial` result is a prompt for review, not an automatic separate finding. Consider materiality, context, evidence quality, duplicate observations, control intent, and risk implications.

For each material issue:

1. Record the observation against the relevant check ID.
2. Validate the condition and supporting evidence.
3. Create or reference a finding ID.
4. Determine whether a risk scenario should be recorded or updated.
5. Apply the approved scoring model where appropriate.
6. Define a proportionate recommendation and verification criteria.
7. Assign ownership and an organization-approved target date.
8. Link the item to the assessment report and risk register.

### 11.2 Findings index

| Finding ID | Check ID(s) | Title | Classification | Evidence IDs | Related risk ID | Owner | Status | Target date |
|---|---|---|---|---|---|---|---|---|
| `[FIND-###]` | `[Check IDs]` | `[Title]` | `[Approved category / severity]` | `[EVD IDs]` | `[RISK-### / Pending / N/A]` | `[Role]` | `[Status]` | `[Date / TBD]` |

### 11.3 Risk linkage

| Risk ID | Scenario | Inherent rating | Current rating | Target residual forecast | Treatment | Decision / escalation state |
|---|---|---|---|---|---|---|
| `[RISK-###]` | `[Cause → event → consequence]` | `[Score / band]` | `[Score / band]` | `[Forecast score / band]` | `[Avoid / Mitigate / Transfer-share / Accept]` | `[State]` |

Use the approved `risk-scoring-model.md`. Target residual risk remains a forecast until treatment is implemented and effectiveness verified. Confidence and uncertainty should be documented separately from the rating.

### 11.4 Remediation and verification tracker

| Action ID | Finding / risk IDs | Required outcome | Owner | Dependency | Approved target date | Status | Verification evidence / result |
|---|---|---|---|---|---|---|---|
| `[ACT-###]` | `[IDs]` | `[Specific, verifiable outcome]` | `[Role]` | `[Dependency / None]` | `[Date / TBD]` | `[Status]` | `[Evidence ID / Pending]` |

Do not impose universal remediation deadlines. Use approved organizational policy, applicable obligations, risk significance, and delegated authority. Risk acceptance must be explicit and documented by an authorized decision-maker; an overdue action or silence is not acceptance.

---

## 19. Consolidated results summary

### 12.1 Overall results

| Metric | Count / value |
|---|---:|
| Applicable checks | `[Count]` |
| Pass | `[Count]` |
| Fail | `[Count]` |
| Partial | `[Count]` |
| Not Tested | `[Count]` |
| Not Applicable | `[Count]` |
| Blocked | `[Count]` |
| Evidence gaps requiring follow-up | `[Count]` |
| Findings raised | `[Count]` |
| Risks created or updated | `[Count]` |
| Actions requiring owner / management decision | `[Count]` |

Counts must reflect the defined scope and applicability decisions. A high pass count alone does not establish that an environment is secure or compliant.

### 12.2 Domain completion

| Domain | Applicable checks | Completed checks | Findings | Evidence gaps | Reviewer status |
|---|---:|---:|---:|---:|---|
| Infrastructure / asset inventory | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Network security | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Endpoints / workstations | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Servers / virtualization | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Applications / application services | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Identity and access management | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Database security | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Vulnerability assessment / security testing | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Security logging and monitoring | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Backup / recovery / resilience | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Cloud / containers / hosted platforms | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Configuration management / compliance mapping | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |
| Cross-cutting security controls | `[ ]` | `[ ]` | `[ ]` | `[ ]` | `[Status]` |

### 12.3 Outstanding items and limitations

- **Not tested / blocked checks:** `[Check IDs, reasons, and follow-up decisions]`
- **Scope exclusions:** `[Items and rationale]`
- **Evidence gaps:** `[Gap IDs and effect on conclusions]`
- **High-priority findings / risks:** `[IDs and required decisions]`
- **Required escalation:** `[Role / process / date]`
- **Assessment conclusion limitations:** `[What the evidence does not establish]`

### 12.4 Review and handover

| Role | Name / identifier | Review status | Date | Notes |
|---|---|---|---|---|
| Lead assessor | `[Role / name]` | `[Complete / Pending]` | `[YYYY-MM-DD]` | `[Notes]` |
| Technical reviewer | `[Role / name]` | `[Complete / Pending]` | `[YYYY-MM-DD]` | `[Notes]` |
| System / control owner | `[Role / name]` | `[Acknowledged / Pending]` | `[YYYY-MM-DD]` | `[Notes]` |
| Risk owner, where applicable | `[Role / name]` | `[Decision / Pending / N/A]` | `[YYYY-MM-DD]` | `[Notes]` |

---

## 20. Illustrative completed checklist section

> **Fictional example only.** The system, identities, evidence, finding, risk, and result below are invented for demonstration and do not describe a real environment.

| Field | Illustrative entry |
|---|---|
| Check ID | `SRV-EX-001` |
| Domain / objective | Server privileged access — verify access is limited to approved roles |
| Asset | `SRV-EX-01` — fictional business-critical application server |
| Verification procedure | Compare an authorized privileged-group listing with approved role and access records |
| Expected condition | Privileged memberships have a documented business justification and appropriate approval |
| Result | **Fail — illustrative only** |
| Observation | One fictional account appears in the reviewed privileged-group listing without a current approval record in the sample examined |
| Evidence IDs | `EVD-EX-001`, `EVD-EX-002` |
| Assessor / date | `[Fictional assessor / date]` |
| Limitations | The example covers only the stated sample and does not establish the status of all accounts |
| Finding ID | `FIND-EX-001` |
| Risk ID | `RISK-EX-001` |
| Follow-up | Validate business need, remove unauthorized access where confirmed, and update the approved access record |
| Verification criteria | Updated membership listing and documented access approval review |

### Illustrative evidence entries

| Evidence ID | Description | Supports | Limitation |
|---|---|---|---|
| `EVD-EX-001` | Fictional administrative membership export | `SRV-EX-001`, `FIND-EX-001` | Snapshot of the reviewed system |
| `EVD-EX-002` | Fictional access-approval sample | `SRV-EX-001`, `FIND-EX-001` | Sample may not represent every account |

### Illustrative risk linkage

**Scenario:** Because privileged access is not sufficiently restricted, a compromised or misused account may enable unauthorized configuration changes or service disruption.

| Risk state | Likelihood | Impact | Score | Illustrative band |
|---|---:|---:|---:|---|
| Inherent | 4 | 4 | 16 | High |
| Current | 3 | 4 | 12 | High |
| Target residual — forecast | 2 | 4 | 8 | Moderate |

These scores use illustrative bands only. The target residual rating must not replace the current rating until treatment is completed and effectiveness is verified. An organization must approve its own rating bands and acceptance criteria before operational use.

### Illustrative remediation

| Action ID | Action | Owner | Target date | Verification |
|---|---|---|---|---|
| `ACT-EX-001` | Validate and remove unjustified privileged memberships | Infrastructure security lead | `[Approved date]` | Updated membership listing and approved access matrix |
| `ACT-EX-002` | Validate privileged-access approval and review process | Application service owner | `[Approved date]` | Completed review record and exception tracking |

**Disposition:** Open — remediation and verification pending.

---

## 21. Quality review checklist

- [ ] Every activity was within documented authorization and scope.
- [ ] Applicable modules and exclusions are recorded.
- [ ] Each completed check has a result and rationale.
- [ ] `Not Tested`, `Blocked`, and `Not Applicable` are not represented as passes.
- [ ] Material observations are supported by evidence references.
- [ ] Evidence gaps and their effects on conclusions are recorded.
- [ ] Finding and risk IDs are consistent across linked records.
- [ ] Risk scores use the approved scoring model and include rationale.
- [ ] Recommendations are proportionate and include verification criteria.
- [ ] Sensitive evidence is stored and handled appropriately.
- [ ] Outstanding items, dependencies, and escalations are documented.
- [ ] Required technical review and handover are recorded.
- [ ] Conclusions are limited to the scope and evidence actually assessed.

---

## 22. References and document control

### Internal references

- [Assessment lifecycle](../docs/methodology/assessment-lifecycle.md)
- [Risk assessment methodology](../docs/methodology/risk-assessment-methodology.md)
- [Risk scoring model](../docs/methodology/risk-scoring-model.md)
- [Evidence handling](../docs/methodology/evidence-handling.md)
- [Standards and frameworks register](../references/standards-and-frameworks.md)
- [Assessment report template](assessment-report-template.md)
- [Risk register template](risk-register-template.md)

### External framework alignment

This checklist is designed to support evidence-informed technical assessment and control verification using organization-selected criteria. Relevant NIST and ISO/IEC publications, CIS Controls, and OWASP materials may inform specific checks where applicable. Confirm the current edition, scope, and applicability in the standards register before relying on a reference.

Referencing a standard does not independently establish compliance or certification.

### Document control

| Field | Value |
|---|---|
| Document | Technical Assessment Checklist |
| Version | 1.1 |
| Owner | `[Organization / function]` |
| Approval authority | `[Role / committee]` |
| Approval date | `[YYYY-MM-DD]` |
| Review date | `[YYYY-MM-DD]` |
| Classification | `[Organization-defined]` |
| Change history | `1.1 — Expanded to twelve technical domains; added IAM, database, vulnerability, logging, resilience, cloud/container, and configuration/compliance modules; expanded domain completion tracking.` |
