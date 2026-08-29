# Phase 4 — CyberOps Associate v1.0 Skills Assessment Mapping

## Purpose

This document maps the **Cisco CyberOps Associate v1.0 Skills Assessment** to the portfolio's 11 evidence domains and the TESDA Cyber Threat Monitoring NC I / Cyber Threat Mitigation NC II core competencies.

The assessment uses a Security Onion environment and an alert-driven Pushdo Trojan investigation. Its stated assessed skills include evaluating event alerts using Sguil/Kibana, obtaining intelligence on a potential exploit using web search, and using VirusTotal to verify a threat.

## Assessment completion status

**User-reported status: COMPLETED.**

The user has already performed the v1.0 Skills Assessment in the CyberOps VM and reports that the observed results/answers match the published answer reference used as a cross-check.

Reference used for answer cross-check:



The reference confirms the same assessment structure: Security Onion service verification, Sguil/Kibana alert review, Pushdo incident timeframe, affected host identification, exploit/infection analysis, downloaded-file and hash analysis, VirusTotal verification, related-alert review, and final findings. citeturn1search0

### Evidence-integrity rule

The published answer reference is **not treated as portfolio evidence**. It is only a cross-check against the user's independently performed assessment.

The portfolio evidence must still come from the user's own CyberOps VM run, such as screenshots, command output, alert records, investigation notes, hashes, VirusTotal results, and the completed report.

## Assessment role in the portfolio

**Primary role:** high-value, alert-driven SOC investigation evidence.

**Best TESDA fit:**

- **ICT251312 — Monitor and Report Cyber Threats:** strong/direct supporting evidence
- **ICT251314 — Perform Threat Mitigation:** strong investigation/IOC/CTI supporting evidence, but not complete mitigation
- **ICT251313 — Conduct Vulnerability Scanning of Assets:** not a direct assessment activity
- **ICT251315 — Perform Vulnerability Management/Control:** not a direct assessment activity

The assessment begins with verification of Security Onion services and access to Sguil/Kibana, followed by review of alerts in the relevant time window. It then investigates the infected host, exploit, downloaded files/hashes, VirusTotal results, related alerts, and concludes with a findings report. citeturn1search0

## Task-level evidence mapping

| Assessment task | Primary domain | Related domains | TESDA relevance | Coverage | Evidence to capture |
|---|---|---|---|---|---|
| Verify Security Onion services with `so-status` | **01 Monitoring and Alerts** | 07 Incident Investigation | ICT251312: security monitoring readiness | 🟡 Supporting | Terminal screenshot; service status; lab notes |
| Open Sguil/Kibana and review alerts | **01 Monitoring and Alerts** | 02 Log/Event Analysis, 07 Incident Investigation | ICT251312: check/review alerts and validate suspicious activity | 🟢 Direct | Alert screenshot; timestamp; alert details |
| Establish Pushdo attack timeframe | **07 Incident Investigation** | 01 Monitoring and Alerts, 02 Log/Event Analysis | ICT251312: investigate/follow up an alert | 🟢 Direct | Timeline table; supporting alert screenshots |
| List alerts associated with the Trojan | **01 Monitoring and Alerts** | 07 Incident Investigation | ICT251312: alert assessment and case follow-up | 🟢 Direct | Alert inventory |
| Identify internal/external IP addresses | **07 Incident Investigation** | 03 Network Traffic Analysis | ICT251312/ICT251314: affected assets and communications | 🟢 Direct | IP table; relevant event/alert evidence |
| Identify infected host IP/MAC | **04 Endpoint Analysis** | 07 Incident Investigation | ICT251312/ICT251314: identify affected endpoint | 🟢 Direct | Host identification table; alert evidence |
| Identify NIC vendor from MAC | **04 Endpoint Analysis** | 08 Threat Intelligence | Supporting host investigation | 🟡 Supporting | Lookup result + source |
| Determine infection time and method | **07 Incident Investigation** | 03 Network Traffic Analysis, 05 Malware/IOC Analysis | ICT251312/ICT251314: establish incident timeline and attack vector | 🟢 Direct | Timeline + supporting events |
| Research how the malware/exploit infected the PC | **08 Threat Intelligence** | 05 Malware/IOC Analysis, 07 Incident Investigation | ICT251314: threat intelligence / attack analysis | 🟢 Direct | Research notes; cited sources; TTP/attack explanation |
| Identify downloaded files associated with malicious domains | **05 Malware/IOC Analysis** | 03 Network Traffic Analysis, 07 Incident Investigation | ICT251314: IOC/malware analysis | 🟢 Direct | Filename, path, domain, related alert evidence |
| Calculate SHA-256 hashes of downloaded files | **05 Malware/IOC Analysis** | 04 Endpoint Analysis | ICT251314: IOC identification / file verification | 🟢 Direct | Hash command/output; hash table |
| Submit/search hashes in VirusTotal | **08 Threat Intelligence** | 05 Malware/IOC Analysis | ICT251314: IOC counter-check/threat intelligence | 🟢 Direct | VirusTotal result screenshot; hash; date accessed |
| Record file type, size, aliases, target machine and community intelligence | **05 Malware/IOC Analysis** | 08 Threat Intelligence, 04 Endpoint Analysis | ICT251314: enrich and document IOC evidence | 🟢 Direct | IOC enrichment table |
| Examine other alerts associated with infected host | **07 Incident Investigation** | 01 Monitoring and Alerts, 02 Log/Event Analysis | ICT251312: case follow-up; ICT251314: incident analysis | 🟢 Direct | Correlated-alert table; screenshots |
| Summarize findings | **11 Reporting** | 07 Incident Investigation, 08 Threat Intelligence | ICT251312 reporting; ICT251314 incident documentation | 🟢 Direct | Final investigation report |

The task sequence and required outputs are based on the published v1.0 assessment document. citeturn1search0

## 11-domain classification

### 01 — Monitoring and Alerts

**Primary evidence:** Sguil/Kibana alert review.

The assessment is particularly strong here because it begins from an existing detection alert rather than requiring the analyst to discover the incident from an entirely unknown dataset. citeturn1search0

### 02 — Log/Event Analysis

**Supporting evidence:** event and alert review/correlation.

### 03 — Network Traffic Analysis

**Supporting evidence:** internal/external IPs, infection traffic, malicious-domain activity and attack timeline.

### 04 — Endpoint Analysis

**Direct/supporting evidence:** infected host IP/MAC, NIC vendor and downloaded-file investigation.

### 05 — Malware/IOC Analysis

**Strong evidence:** malicious files, SHA-256 hashes, file metadata and malware verification.

### 06 — Vulnerability Scanning

**No direct evidence.** The assessment investigates exploitation but does not constitute a vulnerability-scanning workflow.

### 07 — Incident Investigation

**Strong evidence:** alert → affected host → infection time/method → malicious files → related alerts → findings.

### 08 — Threat Intelligence

**Strong evidence:** web research and VirusTotal enrichment/verification. The assessment explicitly identifies these as assessed skills. citeturn1search0

### 09 — Containment

**Gap.** The assessment identifies and investigates the compromised host but does not require isolation, IOC blocking, account disablement or another containment action.

### 10 — Recovery

**Gap.** No eradication, restoration, recovery validation or secondary scan is required.

### 11 — Reporting

**Direct evidence:** final summary of findings is an explicit assessment task. citeturn1search0

## TESDA coverage summary

| TESDA core competency | v1.0 contribution | Rating |
|---|---|---|
| **ICT251312 — Monitor and Report Cyber Threats** | Alert review, alert assessment, case follow-up, investigation and reporting | 🟢 **Strong / high-value evidence** |
| **ICT251313 — Conduct Vulnerability Scanning of Assets** | No actual vulnerability scan | 🔴 **Not demonstrated** |
| **ICT251314 — Perform Threat Mitigation** | Incident analysis, IOC identification, CTI and reporting | 🟢 **Strong partial evidence** |
| **ICT251315 — Perform Vulnerability Management/Control** | Not demonstrated | 🔴 **Not demonstrated** |

## What v1.0 does NOT prove

The portfolio must not claim that completing this Skills Assessment alone proves the following:

- containment of the compromised host
- eradication of malware
- system recovery
- recovery validation
- secondary vulnerability/security scan
- vulnerability remediation/change management
- vulnerability-management lifecycle
- stakeholder escalation/ticket workflow unless separately documented

These will be handled through supplementary evidence and later phases.

## Recommended evidence package

Because the user has already completed the assessment, the next evidence-implementation task is to collect the user's actual artifacts into the following structure:

```text
v1.0-pushdo/
├── README.md
├── assessment-report.md
├── alert-analysis.md
├── incident-timeline.md
├── ioc-table.md
├── threat-intelligence.md
├── findings-report.md
└── screenshots/
    ├── 01-so-status.png
    ├── 02-sguil-kibana-alerts.png
    ├── 03-infected-host.png
    ├── 04-network-indicators.png
    ├── 05-file-hash.png
    ├── 06-virustotal-results.png
    └── 07-related-alerts.png
```

Do not create placeholder screenshots as if they were completed evidence. The screenshots and outputs must be captured from the user's actual assessment run.

## RPL/SAG use

For an eventual SAG response, v1.0 should be presented as **practical evidence for the specific monitoring, investigation, IOC/CTI and reporting criteria it actually demonstrates**, not as a blanket claim of competency.

The strongest evidence chain is:

```text
Existing Security Alert
        ↓
Alert Review / Validation
        ↓
Affected Host Identification
        ↓
Incident Timeline
        ↓
Attack / Infection Analysis
        ↓
Malware / IOC Extraction
        ↓
Hash Verification
        ↓
Threat Intelligence Enrichment
        ↓
Related-Alert Correlation
        ↓
Incident Findings Report
```

## Relationship to CyberOps labs

The v1.0 assessment should be treated as a **capstone built from previously practiced CyberOps labs**, especially the assessment's use of Security Onion, Sguil/Kibana, NetworkMiner, file/hash analysis and threat-intelligence verification. citeturn1search0

Therefore, the portfolio should retain the individual lab evidence and use the Skills Assessment as an integrated demonstration rather than replacing the lab evidence.

## Phase 4 status

**Status: 🟢 Assessment performed; results cross-checked; evidence artifact collection pending.**

Next tasks:

1. Add the user's actual v1.0 screenshots/evidence artifacts to the repository.
2. Produce the formal investigation report from the user's own results.
3. Link the completed evidence to the exact TESDA performance-criterion matrix.
4. Update the master SAG matrix with actual evidence locations.
5. Proceed to Phase 5 — CyberOps v1.1 Skills Assessment mapping.
