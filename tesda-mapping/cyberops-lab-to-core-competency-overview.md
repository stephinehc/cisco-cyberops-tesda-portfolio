# CyberOps Associate Lab Activities → TESDA Core Competency Overview

## Purpose

This document establishes the Phase 1 working model for using **Cisco CyberOps Associate laboratory activities** as practical evidence sources for the TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II qualifications.

The portfolio will use the **actual CyberOps lab activities**, not only the Cisco Skills Assessments. The Skills Assessments (v1.0 and v1.1) will be treated as higher-level assessment activities built from the skills developed through the labs.

> **Evidence rule:** A lab is not automatically equivalent to a TESDA competency. The rating indicates how strongly the activity can contribute evidence toward the competency. Additional TESDA-specific process evidence will be created where required.

## Four TESDA core competencies

| Qualification | Core competency | Portfolio role |
|---|---|---|
| Cyber Threat Monitoring NC I | **ICT251312 — Monitor and Report Cyber Threats** | Primary monitoring, alert, log, network-analysis and reporting target |
| Cyber Threat Monitoring NC I | **ICT251313 — Conduct Vulnerability Scanning of Assets** | Nmap/scanning target plus TESDA-style scanning workflow |
| Cyber Threat Mitigation NC II | **ICT251314 — Perform Threat Mitigation** | Investigation, IOC/TTP, CTI, containment, eradication and recovery target |
| Cyber Threat Mitigation NC II | **ICT251315 — Perform Vulnerability Management/Control** | Nmap plus dedicated vulnerability-management/remediation activities |

## Evidence ratings

- 🟢 **Direct** — the CyberOps activity can produce strong practical evidence for part or all of the relevant performance requirement.
- 🟡 **Supporting** — the activity develops or demonstrates a related skill, but additional evidence is needed.
- 🔴 **Gap** — the CyberOps activity does not adequately demonstrate the requirement; a supplementary practical activity is required.

## CyberOps lab activity groups

The original CyberOps sequence will be preserved in the lab register. The same lab may appear in more than one TESDA evidence domain.

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

This activity is particularly important because it provides a bridge between CyberOps technical labs and the alert-driven SOC workflow used in the v1.0 Skills Assessment.

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

### 8. CyberOps Skills Assessments

#### v1.0

Primary role:

> **Alert-driven SOC investigation and reporting**

Target competency:

- **NC I — ICT251312:** 🟢 Primary capstone
- **NC II — ICT251314:** 🟡/🟢 Strong investigation foundation

#### v1.1

Primary role:

> **Advanced security analysis and investigation**

Target competency:

- **NC I — ICT251312:** 🟢 Advanced supporting evidence
- **NC II — ICT251314:** 🟢 Advanced investigation evidence

The exact v1.1 activity-to-criterion mapping will be finalized after the actual v1.1 Skills Assessment tasks are documented in the evidence register.

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
CyberOps v1.1 Skills Assessment
        ↓
Advanced investigation / analysis
        ↓
BOTS v2 threat-hunting activities
        ↓
Independent investigation
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

The portfolio will **retain the CyberOps laboratory activities as a major evidence source**. We will not reduce the portfolio to only the v1.0/v1.1 Skills Assessments.

The final evidence architecture will therefore combine:

1. CyberOps Associate laboratory activities
2. CyberOps v1.0 Skills Assessment
3. CyberOps v1.1 Skills Assessment
4. BOTS v2 CTF/threat-hunting activities
5. Dedicated containment/eradication/recovery simulation
6. Dedicated vulnerability-management/remediation simulation
7. TESDA-format reports, checklists and evidence records

This approach provides a progression from **skill practice → guided assessment → independent investigation → mitigation → validation**.
