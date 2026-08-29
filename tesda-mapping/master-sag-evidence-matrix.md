# Master TESDA SAG Evidence Matrix

## Purpose

This is the master cross-reference between the four TESDA Cyber Threat Monitoring NC I / Cyber Threat Mitigation NC II core competencies, the portfolio's 11 evidence domains, Cisco CyberOps Associate laboratory activities, Skills Assessments, BOTS v2, and supplementary activities.

**Important:** This matrix is an RPL/evidence-planning document, not a TESDA assessment result. Final competency decisions belong to the authorized TESDA assessment process.

## Evidence-domain structure

```text
01-monitoring-and-alerts/
02-log-event-analysis/
03-network-traffic-analysis/
04-endpoint-analysis/
05-malware-ioc-analysis/
06-vulnerability-scanning/
07-incident-investigation/
08-threat-intelligence/
09-containment/
10-recovery/
11-reporting/
```

## Rating key

| Rating | Meaning |
|---|---|
| 🟢 Direct | Existing activity directly demonstrates the technical action; criterion-specific artifacts still need to be captured. |
| 🟡 Supporting | Activity contributes useful evidence but needs an additional process, artifact, or practical step. |
| 🔴 Gap | Existing CyberOps evidence does not adequately demonstrate the requirement; supplementary activity is required. |

---

# NC I — ICT251312 Monitor and Report Cyber Threats

**Primary evidence sources:** CyberOps monitoring/log/network labs, Snort/Security Onion activities, v1.0 Skills Assessment, v1.1 Skills Assessment, selected BOTS v2 investigations.

| TESDA performance area | Evidence domain(s) | CyberOps evidence | Additional evidence | Coverage |
|---|---|---|---|---|
| Check for alerts and identify relevant detections | 01, 07 | Snort/Security Onion labs; v1.0 Skills Assessment | Alert review record | 🟢 |
| Validate/assess alerts | 01, 02, 07 | Alert analysis, log analysis, v1.0 | Alert triage worksheet/SOP | 🟢/🟡 |
| Perform manual verification | 02, 03, 04, 05 | Logs, Wireshark, endpoint and malware labs | Investigation notes | 🟢 |
| Follow up confirmed cases | 07, 08 | v1.0, v1.1, BOTS v2 | Case/ticket record | 🟢/🟡 |
| Report threat activity and findings | 11 | CyberOps reports/Skills Assessments | TESDA-style incident report | 🟢/🟡 |
| Communicate/escalate to appropriate stakeholder | 11 | Technical findings | Escalation/notification artifact | 🟡 |

### NC I interpretation

CyberOps provides a strong technical foundation for monitoring and reporting. The main remaining evidence is **workplace-process evidence**: SOP use, ticketing, escalation and stakeholder notification where these are required by the exact criterion.

---

# NC I — ICT251313 Conduct Vulnerability Scanning of Assets

**Primary evidence sources:** CyberOps Nmap/scanning activities plus supplementary vulnerability-scanning workflow.

| TESDA performance area | Evidence domain(s) | CyberOps evidence | Additional evidence | Coverage |
|---|---|---|---|---|
| Prepare authorized scan scope/assets | 06 | Nmap/asset discovery | Scope and authorization record | 🟡 |
| Configure scanning activity | 06 | Nmap lab | Scan configuration record | 🟢/🟡 |
| Conduct vulnerability/port/service scanning | 06 | CyberOps Nmap activity | Additional scanner if required | 🟢 |
| Analyze and prioritize findings | 06, 11 | Nmap results | Vulnerability analysis/risk worksheet | 🟡 |
| Document and report scan results | 06, 11 | Lab output | TESDA-style vulnerability report | 🟡 |

### NC I interpretation

The CyberOps Nmap activity is strong **technical scanning evidence**, but the portfolio will add authorization, scope, analysis, prioritization and reporting artifacts so the evidence represents a complete workplace workflow.

---

# NC II — ICT251314 Perform Threat Mitigation

**Primary evidence sources:** CyberOps investigation/malware/IOC labs, v1.0/v1.1 Skills Assessments, BOTS v2, and the dedicated containment/recovery simulation.

| TESDA performance area | Evidence domain(s) | Existing evidence | Required supplementary evidence | Coverage |
|---|---|---|---|---|
| Evaluate and validate incidents | 01, 02, 07 | v1.0/v1.1, CyberOps investigations | Incident classification record | 🟢 |
| Prioritize incident criticality | 07, 11 | Incident investigation | Severity/prioritization matrix | 🟡 |
| Identify IOCs | 05, 08 | Malware/IOC labs, v1.0, BOTS v2 | IOC worksheet | 🟢 |
| Identify/analyze TTPs | 07, 08 | v1.1/BOTS v2 and investigation labs | MITRE/kill-chain mapping where required | 🟡 |
| Analyze affected hosts/processes/configurations | 04, 05, 07 | Endpoint/process/malware labs | Host-analysis report | 🟢 |
| Counter-check/enrich IOCs | 05, 08 | Hashing, VirusTotal, CTI exercises | CTI evidence record | 🟢/🟡 |
| Contain threat | 09 | Limited existing lab support | Dedicated containment practical | 🔴 |
| Eradicate threat | 09, 10 | Limited existing lab support | Eradication practical | 🔴 |
| Recover system/infrastructure | 10 | No complete existing evidence | Clean image/configuration recovery practical | 🔴 |
| Remove/verify malicious IOCs | 05, 09, 10 | IOC analysis | Post-eradication validation | 🟡 |
| Perform secondary scan/validation | 06, 10 | Nmap/scanning foundation | Post-recovery scan | 🟡 |
| Monitor after recovery | 01, 10 | Monitoring labs | Recovery monitoring record | 🟡 |
| Document mitigation and report | 11 | Reporting labs/assessments | Full incident response report | 🟢/🟡 |

### NC II interpretation

The portfolio already has substantial **detection, investigation, IOC and CTI evidence**. The major gap is operational mitigation: **containment → eradication → recovery → secondary validation**. A controlled supplementary simulation will close this gap.

---

# NC II — ICT251315 Perform Vulnerability Management/Control

**Primary evidence sources:** CyberOps Nmap/scanning activities plus a dedicated vulnerability-management/remediation workflow.

| TESDA performance area | Evidence domain(s) | Existing CyberOps evidence | Required supplementary evidence | Coverage |
|---|---|---|---|---|
| Install/configure vulnerability-management software/agent where applicable | 06 | Limited | Scanner/agent setup practical | 🔴/🟡 |
| Schedule vulnerability scans | 06, 11 | Limited | Scheduled-scan plan/configuration | 🔴 |
| Maintain asset inventory/control | 06, 11 | Nmap discovery | Asset inventory and classification | 🟡 |
| Audit servers/endpoints/applications | 04, 06 | Endpoint/network labs | Structured audit checklist | 🟡 |
| Manage vulnerability findings/changes | 06, 11 | Scan outputs | Change request/CAB workflow | 🔴 |
| Test patches/remediation | 06, 10 | Limited | Patch/remediation lab | 🔴 |
| Rescan and verify remediation | 06, 10 | Nmap foundation | Before/after scan comparison | 🟡 |
| Report vulnerability-management results | 11 | Lab reporting | Formal VM report/dashboard | 🟡 |

### NC II interpretation

CyberOps provides useful technical foundations, particularly scanning and endpoint/network analysis. It does **not** by itself establish a complete vulnerability-management/control process. The portfolio therefore requires a dedicated VM/remediation practical.

---

# Evidence-source strategy

| Evidence source | Best role in the portfolio |
|---|---|
| **CyberOps Associate labs** | Primary technical skills evidence and foundation |
| **CyberOps v1.0 Skills Assessment** | Alert-driven investigation and NC I monitoring/reporting capstone |
| **CyberOps v1.1 Skills Assessment** | Advanced investigation/analysis; exact task mapping to follow |
| **BOTS v2** | Independent SIEM investigation and threat hunting |
| **Containment/Recovery simulation** | NC II threat-mitigation operational evidence |
| **Vulnerability-management simulation** | NC I scanning process + NC II VM/control evidence |

# SAG evidence decision model

For every SAG item, the final portfolio review will use:

```text
TESDA SAG / Performance Criterion
            ↓
What exactly must be demonstrated?
            ↓
Existing CyberOps lab evidence
            ↓
Skills Assessment / BOTS v2 evidence
            ↓
Supplementary evidence if required
            ↓
Artifact checklist
            ↓
YES / PARTIALLY / NO
```

A **YES** recommendation should only be made when the repository contains observable evidence for the required action, not merely a related course/lab title.

# Phase 3 conclusion

The master mapping confirms the strategic use of the portfolio:

- **CyberOps labs** provide the technical foundation.
- **v1.0** strengthens alert-driven monitoring/investigation evidence.
- **v1.1** adds advanced analysis evidence after its actual tasks are mapped.
- **BOTS v2** adds independent SIEM/threat-hunting evidence.
- **Supplementary mitigation and vulnerability-management labs** close the operational/process gaps.

## Remaining work before Phase 4

1. Verify the exact CyberOps v1.0 Skills Assessment used by the user.
2. Map every v1.0 task to the 11 evidence domains and the master TESDA matrix.
3. Capture the exact evidence artifacts that will be produced by each task.
4. Identify any v1.0-specific TESDA criteria that remain gaps.
5. Then repeat the process for v1.1.
