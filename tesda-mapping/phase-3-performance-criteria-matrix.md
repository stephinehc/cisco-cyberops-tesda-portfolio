# Phase 3 — TESDA Performance-Criteria Mapping

## Purpose

This matrix maps the Cisco CyberOps Associate laboratory evidence to the **specific performance criteria** of the four TESDA core competencies. The TESDA Training Regulations are the controlling reference; CyberOps activities are evidence sources, not automatic proof of competence.

TESDA defines Cyber Threat Monitoring NC I with two core units: **ICT251312 Monitor and report cyber threats** and **ICT251313 Conduct vulnerability scanning of assets**. cite not stored in repo; see source notes below.

Cyber Threat Mitigation NC II contains **ICT251314 Perform threat mitigation** and **ICT251315 Perform vulnerability management/control**.

## Evidence rating

- 🟢 **Direct** — the CyberOps activity can demonstrate the technical action in the criterion when performed and documented properly.
- 🟡 **Supporting** — the activity demonstrates an important part of the criterion but does not by itself cover the complete TESDA requirement.
- 🔴 **Gap** — CyberOps alone does not demonstrate the criterion sufficiently; a supplementary activity or explicit TESDA-style evidence is required.

## A. ICT251312 — Monitor and Report Cyber Threats

TESDA's unit covers checking alerts, checking security-solution status, manual checking/verification, case follow-up and alert reporting.

| TESDA criterion | Best CyberOps evidence | Rating | Additional evidence needed |
|---|---|---:|---|
| **1.1** Detection alert received according to SOP | 26.1.7 Snort and Firewall Rules; Skills Assessment | 🟡 | SOC/SOP context and timestamped alert evidence |
| **1.2** Incident report received according to SOP | Skills Assessment; 17.2.7 Reading Server Logs | 🟡 | Incident-report/ticket artifact |
| **1.3** Red-flag detection checked according to SOP | 26.1.7 Snort and Firewall Rules | 🟢 | Document the checking procedure |
| **1.4** Alert assessed using pre-identified criteria | 26.1.7; v1.0 Skills Assessment | 🟢 | Show severity/triage criteria |
| **1.5** Ticket issued after confirmation | v1.0 Skills Assessment | 🟡 | Ticket/case record |
| **2.1** Enterprise security solution checked for installation | 26.1.7 Snort and Firewall Rules | 🟡 | Explicit solution-status checklist |
| **2.2** Security solution checked for operation | 26.1.7 Snort and Firewall Rules | 🟢 | Configuration/status evidence |
| **2.3** Security solution checked for ability to clean/delete issue | 26.1.7 | 🔴 | Add endpoint-security remediation demonstration |
| **3.1** Detection checked according to procedure | 26.1.7; v1.0 Skills Assessment | 🟢 | Procedure + screenshots |
| **3.2** Security-solution action checked according to SOP | 26.1.7 | 🟡 | Action/result evidence |
| **3.3** Security-solution updates/patches checked | CyberOps endpoint/OS labs | 🟡 | Explicit update/patch evidence |
| **3.4** Security solution used to scan infected systems | Malware/Windows investigation labs | 🟡 | Endpoint-security scan result |
| **4.1** Scan results verified with stakeholder/client | v1.0/v1.1 reporting | 🟡 | Stakeholder-facing report or simulated handoff |
| **4.2** Scan logs checked for failed actions | 17.2.7 Reading Server Logs; 26.1.7 | 🟢 | Show failed-action review |
| **4.3** Failed action escalated appropriately | v1.0 Skills Assessment | 🟡 | Escalation record/SOP |
| **5.1** High/critical threats reported to stakeholder | v1.0 Skills Assessment | 🟢 | Final alert report |
| **5.2** Threat activity reported by spread/lateral movement | 27.2.12; 27.2.14; 27.2.16 | 🟢 | Timeline and affected-host evidence |
| **5.3** Threat activity reported by egress/ingress | Wireshark/DNS/HTTP labs; 27.2.12 | 🟢 | Traffic evidence and interpretation |
| **5.4** Threats identified from exploitation/installation behavior | 27.2.15; 27.2.16 | 🟢 | Malware/host analysis evidence |

### NC I conclusion — ICT251312

CyberOps provides strong technical evidence for alert evaluation, verification, log/traffic analysis, investigation and reporting. The major missing items are **formal SOP/ticket/stakeholder workflow artifacts** and security-product remediation actions. These should be added as portfolio wrappers around the technical labs rather than claiming that the Cisco lab alone satisfies the complete criterion.

## B. ICT251313 — Conduct Vulnerability Scanning of Assets

TESDA requires scheduling/scope control, asset scanning using an industry-standard procedure, operational monitoring, handling scan problems, and reporting scan results.

| TESDA criterion | Best CyberOps evidence | Rating | Additional evidence needed |
|---|---|---:|---|
| **1.1** Consult vulnerability management with supervisor | 9.3.8 Exploring Nmap | 🔴 | Simulated supervisor consultation record |
| **1.2** Access scanning calendar/timeline | 9.3.8 Exploring Nmap | 🔴 | Scanning schedule |
| **1.3** Identify number of assets to scan | 9.3.8 Exploring Nmap | 🟡 | Asset list/scope sheet |
| **1.4** Signed-off scope performed on timeline | 9.3.8 | 🔴 | Authorized scope/sign-off |
| **2.1** Verify asset list with supervisor/change manager | 9.3.8 | 🔴 | Asset-scope verification |
| **2.2** Verify prioritized assets | 9.3.8 | 🔴 | Prioritization worksheet |
| **2.3** Follow prescribed scan schedule | 9.3.8 | 🔴 | Scan schedule/log |
| **2.4** Scan according to NIST 800-115 | 9.3.8 | 🟡 | Explicit NIST 800-115-aligned procedure |
| **2.5** Monitor CPU/storage/network latency | 9.3.8 | 🔴 | Resource-monitoring evidence |
| **2.6** Stop/report when scan causes issues | 9.3.8 | 🔴 | Controlled interruption scenario |
| **3.1** Record failed scans | 9.3.8 | 🟡 | Failed-scan example |
| **3.2** Report failed scan according to procedure | 9.3.8 | 🔴 | Incident/ticket report |
| **3.3** Submit scanning report to supervisor | 9.3.8 | 🟡 | Formal scanning report |

### NC I conclusion — ICT251313

**Nmap is excellent technical scanning evidence, but it is not sufficient by itself for the complete TESDA unit.** The supplementary vulnerability-scanning workflow remains mandatory.

## C. ICT251314 — Perform Threat Mitigation

TESDA requires incident evaluation, CTI use, affected-system process/configuration analysis, and containment/recovery strategy and execution.

| TESDA criterion | Best CyberOps evidence | Rating | Additional evidence needed |
|---|---|---:|---|
| **1.1** Validate alerts based on report | 26.1.7; v1.0 Skills Assessment | 🟢 | Alert-to-investigation chain |
| **1.2** Perform detection using 8-point incident response | v1.0/v1.1 Skills Assessment | 🟡 | Explicit 8-point IR checklist |
| **1.3** Classify incident by environment | 27.2.16; v1.0 | 🟢 | Classification worksheet |
| **1.4** Prioritize criticality by asset impact | v1.0 Skills Assessment | 🟢 | Impact/severity matrix |
| **2.1** Use received CTI to identify attacker TTPs | 27.2.12; 27.2.15; 27.2.16 | 🟡 | Explicit CTI source and TTP mapping |
| **2.2** Counter-check IOCs with other sources | 21.1.6; 27.2.10; 27.2.15 | 🟡 | Multi-source IOC validation |
| **2.3** Check IOC applicability against infrastructure | 27.2.14; 27.2.16 | 🟢 | IOC-to-asset mapping |
| **2.4** Block identified IOCs using security appliances | 26.1.7 | 🟡 | Controlled blocking demonstration |
| **2.5** Continuously monitor for malicious IOC interaction | 26.1.7; v1.0/v1.1 | 🟡 | Post-containment monitoring |
| **2.6** Add current CTI/mitigation knowledge to knowledge systems | BOTS v2 + CTI work | 🔴 | Knowledge-base/update artifact |
| **3.1** Analyze running processes/configurations on affected systems | 3.0.3; 3.2.11; 3.3.12; 27.2.16 | 🟢 | Affected-host evidence chain |
| **3.2** Analyze endpoint/network configurations | 3.x Windows/Linux labs; 27.2.16 | 🟡 | Incident-specific configuration review |
| **3.3** Conduct in-depth threat analysis | 27.2.10; 27.2.12; 27.2.15; 27.2.16 | 🟢 | Full analytical narrative |
| **3.4** Develop containment strategy | v1.0/v1.1 | 🔴 | Dedicated containment simulation |
| **3.5** Implement containment strategy | 26.1.7 | 🟡 | Controlled containment action |
| **3.6** Recover system/infrastructure | CyberOps labs alone | 🔴 | Dedicated recovery simulation |
| **3.7** Remove malicious IOCs | 27.2.15/27.2.16 | 🟡 | Actual eradication action |
| **3.8** Perform secondary scan | Nmap + supplementary lab | 🟡 | Post-remediation verification |

### NC II conclusion — ICT251314

CyberOps is **strongest for detection, investigation, IOC analysis, host analysis and threat intelligence foundations**. The portfolio must add a dedicated **containment → eradication → recovery → secondary scan** simulation to close the NC II mitigation gap.

## D. ICT251315 — Perform Vulnerability Management/Control

TESDA extends scanning into product installation/configuration, asset inventory, scheduling/change management, server/endpoint/application checking, VM change management, and remediation testing/reporting.

| TESDA criterion group | Best CyberOps evidence | Rating | Additional evidence needed |
|---|---|---:|---|
| **1. Install/configure vulnerability-management agent/software** | 9.3.8 Nmap | 🔴 | Dedicated VM solution/agent demonstration |
| **2. Perform vulnerability asset control** | 9.3.8 Nmap | 🟡 | Formal asset inventory and grouping |
| **3. Set scanning schedule/change coordination** | 9.3.8 | 🔴 | ITIL/NIST-aligned change/scheduling simulation |
| **4. Check servers/endpoints/applications** | Windows/Linux labs + Nmap | 🟡 | Formal audit checklist |
| **5. Perform VM change management** | Nmap | 🔴 | Change proposal/CAB simulation |
| **6. Perform patch/remediation testing** | CyberOps OS labs | 🔴 | Patch → rescan → validation lab |
| **7. Deliver vulnerability-management report** | 9.3.8 + reporting evidence | 🟡 | TESDA-format VM report |

### NC II conclusion — ICT251315

CyberOps provides useful technical foundations, especially Nmap and endpoint/network knowledge, but **vulnerability management/control is a major supplementary-lab requirement**.

## Master evidence priorities

### Highest-value existing CyberOps activities

1. **26.1.7 — Snort and Firewall Rules** → alert/detection/security-control evidence
2. **27.2.10 — Extract an Executable from a PCAP** → malware/IOC evidence
3. **27.2.12 — Interpret HTTP and DNS Data to Isolate Threat Actor** → threat investigation/CTI evidence
4. **27.2.14 — Isolate Compromised Host Using 5-Tuple** → network/incident investigation
5. **27.2.15 — Investigating a Malware Exploit** → malware/incident investigation
6. **27.2.16 — Investigating an Attack on a Windows Host** → endpoint/incident investigation
7. **17.2.7 — Reading Server Logs** → log analysis
8. **9.3.8 — Exploring Nmap** → vulnerability scanning
9. **3.0.3 / 3.2.11 / 3.3.12 / 3.3.13** → endpoint/process/system analysis
10. **10.x / 17.1.7 Wireshark/DNS/HTTP labs** → network traffic analysis

## Required supplementary evidence

The mapping confirms four major additions:

1. **SOC alert/SOP/ticket/report wrapper** — strengthens NC I monitoring evidence.
2. **TESDA-style vulnerability scanning workflow** — closes ICT251313 gaps.
3. **Containment/eradication/recovery simulation** — closes ICT251314 gaps.
4. **Vulnerability management/control simulation** — closes ICT251315 gaps.

## Source references

- TESDA, **Training Regulations for Cyber Threat Monitoring NC I**, promulgated November 13, 2024.
- TESDA, **Training Regulations for Cyber Threat Mitigation NC II**, promulgated November 13, 2024.
- NDG, **CyberOps Associate v1.0 supported labs** — used to verify Cisco lab numbers/titles.

The final RPL/SAG submission must use the official TESDA TR/CAT wording applicable at the time of assessment and should not treat this portfolio mapping as a substitute for TESDA assessment.