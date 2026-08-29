# CyberOps Associate Lab Activities → TESDA Core Competency Overview

## Purpose

This document establishes the working model for using **Cisco CyberOps Associate laboratory activities** as practical evidence sources for the TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II qualifications.

The portfolio uses the **actual CyberOps lab activities**, not only the Skills Assessment. The retained v1.0 Skills Assessment is treated as a higher-level alert-driven assessment, while BOTS v2 provides independent SIEM threat-hunting evidence.

> **Evidence rule:** A lab is not automatically equivalent to a TESDA competency. The rating indicates how strongly the activity can contribute evidence toward the competency. Additional TESDA-specific process evidence will be created where required.

## Four TESDA core competencies

| Qualification | Core competency | Portfolio role |
|---|---|---|
| Cyber Threat Monitoring NC I | **ICT251312 — Monitor and Report Cyber Threats** | Primary monitoring, alert, log, network-analysis and reporting target |
| Cyber Threat Monitoring NC I | **ICT251313 — Conduct Vulnerability Scanning of Assets** | Nmap/scanning target plus TESDA-style scanning workflow |
| Cyber Threat Mitigation NC II | **ICT251314 — Perform Threat Mitigation** | Investigation, IOC/TTP, CTI, containment, eradication and recovery target |
| Cyber Threat Mitigation NC II | **ICT251315 — Perform Vulnerability Management/Control** | Nmap plus dedicated vulnerability-management/remediation activities |

## Evidence ratings

- 🟢 **Direct** — the activity can produce strong practical evidence for part or all of the relevant performance requirement.
- 🟡 **Supporting** — the activity develops or demonstrates a related skill, but additional evidence is needed.
- 🔴 **Gap** — the activity does not adequately demonstrate the requirement; a supplementary practical activity is required.

## CyberOps lab activity groups

The original CyberOps sequence is preserved in the lab register. The same lab may contribute to more than one evidence domain.

### 1. Host and operating-system analysis

Representative activities:

- Identify Running Processes
- Processes, Threads, Handles and Windows Registry
- Windows PowerShell
- Windows Task Manager
- Monitor and Manage System Resources
- Linux shell and filesystem activities
- Locating Log Files
- Linux server activities

Primary contribution:

- **NC I — ICT251312:** 🟡 Supporting
- **NC II — ICT251314:** 🟢/🟡 Strong supporting evidence for affected-host and process analysis

### 2. Network traffic analysis

Representative activities:

- Introduction to Wireshark
- Ethernet frame analysis
- TCP three-way handshake
- DNS traffic analysis
- TCP/UDP analysis
- HTTP/HTTPS analysis
- Telnet/SSH traffic analysis

Primary contribution:

- **NC I — ICT251312:** 🟢 Direct/supporting depending on the performance criterion
- **NC II — ICT251314:** 🟢 Strong investigation evidence

### 3. Vulnerability scanning

Representative activity:

- **Exploring Nmap**

Primary contribution:

- **NC I — ICT251313:** 🟢 Strong technical scanning evidence
- **NC II — ICT251315:** 🟡 Supporting technical evidence

Important limitation: the Nmap lab must be supplemented with asset scope, authorization, scan planning, result interpretation, reporting, remediation and validation evidence to demonstrate the broader TESDA vulnerability workflow.

### 4. Logs and security-event analysis

Representative activities:

- Locating Log Files
- Reading Server Logs
- DNS traffic investigation
- Security-event and packet analysis activities

Primary contribution:

- **NC I — ICT251312:** 🟢 Strong
- **NC II — ICT251314:** 🟢 Strong supporting/incident-investigation evidence

### 5. Detection and alert evaluation

Representative activity:

- **Snort and Firewall Rules**

Primary contribution:

- **NC I — ICT251312:** 🟢 Direct/high-value evidence
- **NC II — ICT251314:** 🟢 Strong detection and initial mitigation evidence

This activity provides a bridge between CyberOps technical labs and the alert-driven workflow used in the retained v1.0 Skills Assessment.

### 6. Malware and IOC analysis

Representative activities:

- Hashing Things Out
- Extract an Executable from a PCAP
- Investigate a Malware Exploit
- Investigate an Attack on a Windows Host

Primary contribution:

- **NC I — ICT251312:** 🟢 Strong investigation/reporting support
- **NC II — ICT251314:** 🟢 Strong IOC, malware and affected-host analysis

### 7. Incident investigation and threat hunting

Representative activities:

- Interpret HTTP/DNS Data to Isolate Threat Actor
- Isolate Compromised Host Using 5-Tuple
- Investigate a Malware Exploit
- Investigate an Attack on a Windows Host

Primary contribution:

- **NC I — ICT251312:** 🟢 Strong
- **NC II — ICT251314:** 🟢 Strong

## Higher-level investigation activities

### CyberOps v1.0 Skills Assessment

Primary role:

> **Alert-driven SOC investigation and reporting**

Target competency:

- **NC I — ICT251312:** 🟢 Primary assessment evidence
- **NC II — ICT251314:** 🟡/🟢 Strong investigation foundation

### BOTS v2

Primary role:

> **Independent SIEM threat hunting and multi-source investigation**

Target competency:

- **NC I — ICT251312:** 🟢 Strong monitoring, log-analysis and reporting evidence
- **NC II — ICT251314:** 🟢 Strong investigation, IOC and threat-intelligence evidence

BOTS v2 does not replace the dedicated containment/eradication/recovery or vulnerability-management simulations.

## Recommended evidence progression

```text
CyberOps Associate Labs
        ↓
Technical skill development
        ↓
Guided lab evidence
        ↓
CyberOps v1.0 Skills Assessment
        ↓
Alert-driven SOC investigation
        ↓
BOTS v2 threat-hunting activities
        ↓
Independent SIEM investigation
        ↓
Supplementary containment / eradication / recovery lab
        ↓
NC II mitigation evidence
        ↓
Supplementary vulnerability-management lab
        ↓
NC I + NC II vulnerability evidence
```

## Phase 1 decision

The portfolio retains the CyberOps laboratory activities as a major evidence source and does not reduce the portfolio to a single assessment.

The evidence architecture combines:

1. CyberOps Associate laboratory activities
2. CyberOps v1.0 Skills Assessment
3. BOTS v2 SIEM threat-hunting activities
4. Dedicated containment/eradication/recovery simulation
5. Dedicated vulnerability-management/remediation simulation
6. TESDA-format reports, checklists and evidence records

This provides a progression from **skill practice → guided assessment → independent investigation → mitigation → validation**.
