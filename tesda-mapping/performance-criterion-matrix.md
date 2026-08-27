# TESDA Performance-Criterion Evidence Matrix

This is the master crosswalk. It connects the TESDA performance requirement to Cisco evidence, supplementary evidence, and the artifact that should be retained.

## ICT251312 — Monitor and Report Cyber Threats

### Element 1 — Check for Alerts

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 1.1 Detection alert received according to SOP | 26.1.7; 27.2.12 | 🟡 | Alert + SOP record |
| 1.2 Incident report received according to SOP | 27.2.x | 🟡 | Intake report/ticket |
| 1.3 Red-flag detection checked | 26.1.7; 27.2.15 | 🟡 | Red-flag checklist |
| 1.4 Alert assessed against criteria | 26.1.7; 27.2.12 | 🟢 | Alert-analysis worksheet |
| 1.5 Ticket issued after confirmation | 27.2.x | 🟡 | SOC ticket |

### Element 2 — Check Status of Third-Party Security Solution

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 2.1 Security solution installed | 26.1.7 | 🟡 | Installation/status evidence |
| 2.2 Security solution operational | 26.1.7 | 🟡 | Health/status evidence |
| 2.3 Security solution can clean/delete issue | Limited | 🔴 | Controlled remediation test |

### Element 3 — Manual Checking and Verification

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 3.1 Check detection | 26.1.7; 27.2.12 | 🟢 | Alert/log analysis |
| 3.2 Check security-solution action | 26.1.7 | 🟡 | Action/result worksheet |
| 3.3 Check/patch security-solution updates | CyberOps environment | 🟡 | Version/update evidence |
| 3.4 Scan infected systems | 27.2.15; 27.2.16 | 🟡 | Scan + result |

### Element 4 — Case Follow-up

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 4.1 Verify scan results with stakeholder | 27.2.x | 🟡 | Stakeholder verification |
| 4.2 Check failed security actions | 26.1.7 | 🟡 | Failure analysis |
| 4.3 Escalate failed action | Limited | 🔴 | Escalation record |

### Element 5 — Alert Reporting

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 5.1 Notify high/critical stakeholder | 27.2.x | 🟡 | Notification |
| 5.2 Report spread/lateral movement | 27.2.14; 27.2.16 | 🟢 | Timeline/report |
| 5.3 Report ingress/egress | 27.2.12; 27.2.14 | 🟢 | Traffic analysis |
| 5.4 Identify exploitation/installation behavior | 27.2.15; 27.2.16 | 🟢 | Investigation report |

---

## ICT251313 — Conduct Vulnerability Scanning of Assets

### Element 1 — Check Scan Schedule

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 1.1 Consult vulnerability management | Nmap | 🔴 | Authorized scan request |
| 1.2 Access scan calendar/timeline | Nmap | 🔴 | Scan calendar |
| 1.3 Identify number of assets | 9.3.8 | 🟡 | Asset inventory |
| 1.4 Signed-off scope of work | Nmap | 🔴 | Scope/authorization |

### Element 2 — Conduct Scanning

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 2.1 Verify asset list | 9.3.8 | 🟡 | Verified asset list |
| 2.2 Verify prioritized assets | 9.3.8 | 🟡 | Prioritization record |
| 2.3 Follow prescribed schedule | Nmap | 🔴 | Schedule + timestamps |
| 2.4 Scan according to NIST 800-115 | 9.3.8 | 🟡 | Methodology + output |
| 2.5 Monitor CPU/storage/latency | Nmap | 🔴 | Before/during/after metrics |
| 2.6 Terminate/report if problems occur | Nmap | 🔴 | Stop/escalation record |

### Element 3 — Provide Scan Report

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 3.1 Record failed scans | Nmap | 🟡 | Scan log |
| 3.2 Record successful scans | Nmap | 🟢 | Scan output |
| 3.3 Submit vulnerability assessment report | Nmap | 🟡 | Formal report |

---

## ICT251314 — Perform Threat Mitigation

### Element 1 — Check for Incidents

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 1.1 Validate alerts | 26.1.7; 27.2.12 | 🟢 | Validation worksheet |
| 1.2 Product detection using incident-response process | 26.1.7; 27.2.x | 🟡 | Incident worksheet |
| 1.3 Classify incident | 27.2.x | 🟡 | Classification record |
| 1.4 Prioritize incident criticality | 27.2.x | 🟡 | Criticality matrix |

### Element 2 — Use Cyber Threat Intelligence

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 2.1 Identify TTPs using CTI | 27.2.12; 27.2.15 | 🟡 | CTI/TTP analysis |
| 2.2 Counter-check IOCs | 21.1.6; 27.2.10 | 🟡 | Multi-source IOC validation |
| 2.3 Check IOC applicability | 27.2.16 | 🟡 | Infrastructure applicability |
| 2.4 Block IOC | 26.1.7; 27.2.14 | 🟡 | Control/rule + verification |
| 2.5 Continuously monitor IOC | 26.1.7 | 🟡 | Monitoring evidence |
| 2.6 Update knowledge base | Reports | 🔴 | CTI knowledge-base entry |

### Element 3 — Check Running Processes and Configurations

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 3.1 Use security tools | 3.x; 27.2.16 | 🟢 | Tool evidence |
| 3.2 Check malicious-file locations | 3.x; 27.2.16 | 🟢 | Endpoint evidence |
| 3.3 Verify file integrity | 21.1.6; 27.2.16 | 🟢 | Hash/integrity evidence |
| 3.4 Confirm malicious files/folders/packets | 27.2.10; 27.2.15; 27.2.16 | 🟢 | Investigation evidence |

### Element 4 — Implement Containment and Recovery

| Criterion | Cisco evidence | Rating | Required artifact |
|---|---|---|---|
| 4.1 Identify TTPs/IOCs | 27.2.10/12/15/16 | 🟢 | IOC/TTP table |
| 4.2 Block/contain IOC | 26.1.7; 27.2.14 | 🟡 | Containment evidence |
| 4.3 Continuous monitoring | 26.1.7 | 🟡 | Monitoring evidence |
| 4.4 Update knowledge base | Reports | 🔴 | Knowledge-base record |
| 4.5 Recover from last-known-good | Limited | 🔴 | Snapshot/backup evidence |
| 4.6 Rollback | Limited | 🔴 | Rollback evidence |
| 4.7 Remove malicious artifacts | 27.2.16 | 🟡 | Removal evidence |
| 4.8 Secondary scan | 27.2.15/16 | 🟡 | Secondary scan |
| 4.9 Document mitigation/containment/recovery | 27.2.x | 🟡 | Final report |

---

## ICT251315 — Perform Vulnerability Management/Control

### Element 1 — Install Agent

| Criterion | Rating | Required artifact |
|---|---|---|
| 1.1 Identify VM software using applicable guidance | 🔴 | Tool-selection record |
| 1.2 Product-management training | 🔴 | Training/skills record |
| 1.3 Install product | 🔴 | Installation evidence |
| 1.4 Verify installation/configuration | 🔴 | Configuration validation |

### Element 2 — Vulnerability Asset Control

| Criterion | Rating | Required artifact |
|---|---|---|
| 2.1 Coordinate inventory with ITSM | 🔴 | Inventory request |
| 2.2 Create asset inventory | 🟡 | Asset register |
| 2.3 Sort/group inventory using applicable parameters | 🔴 | Classified inventory |

### Element 3 — Set Scan Schedule

| Criterion | Rating | Required artifact |
|---|---|---|
| 3.1 Collaborate on change management | 🔴 | Change coordination |
| 3.2 Check production/staging load schedule | 🔴 | Maintenance calendar |
| 3.3 Check IT/developer/third-party availability | 🔴 | Availability record |

### Element 4 — Check Servers/Endpoints/Applications

| Criterion | Cisco support | Rating | Required artifact |
|---|---|---|---|
| 4.1 Access management | 3.x | 🟡 | Access audit |
| 4.2 Configuration management | 3.x | 🟡 | Configuration audit |
| 4.3 Encryption | 21.x | 🟡 | Encryption check |
| 4.4 Data retention/destruction | Limited | 🔴 | Policy audit |
| 4.5 Preventive maintenance | Limited | 🔴 | Maintenance audit |

### Element 5 — VM Change Management

| Criterion | Rating | Required artifact |
|---|---|---|
| 5.1 Submit change proposal | 🔴 | Change Request |
| 5.2 CAB deliberation | 🔴 | CAB record |
| 5.3 Monitor approved change | 🔴 | Change log |
| 5.4 Execute/validate change | 🔴 | Execution evidence |
| 5.5 Analyze CAB feedback | 🔴 | CAB conclusion |
| 5.6 Scan approved scope/schedule | 🟡 | Scan output |
| 5.7 Document results | 🟡 | Vulnerability report |

### Element 6 — Patch/Remediation Testing

| Criterion | Rating | Required artifact |
|---|---|---|
| 6.1 Obtain remediation strategy | 🔴 | Remediation plan |
| 6.2 Monitor patch testing | 🔴 | Test record |
| 6.3 Document failed/adverse results | 🔴 | Failure record |
| 6.4 Deliver patch/remediation report | 🔴 | Final report |
