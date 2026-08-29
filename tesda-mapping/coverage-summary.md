# TESDA Coverage Summary — Phase 1

## Purpose

This summary defines how the portfolio organizes evidence from **Cisco CyberOps Associate laboratory activities**, the retained Cisco CyberOps v1.0 Skills Assessment, BOTS v2, and controlled supplementary simulations.

The repository uses two separate layers:

1. **TESDA layer** — the four Cyber Threat Monitoring NC I / Cyber Threat Mitigation NC II core competencies.
2. **Evidence-domain layer** — the fixed 11-category structure used to organize technical evidence.

The 11 evidence domains are **not additional TESDA competencies**. They are portfolio categories.

## TESDA core competencies and primary evidence sources

| TESDA qualification | Core competency | Primary evidence sources | Current position |
|---|---|---|---|
| **Cyber Threat Monitoring NC I** | **ICT251312 — Monitor and Report Cyber Threats** | CyberOps labs + v1.0 Skills Assessment + BOTS v2 | 🟢 Strong |
| **Cyber Threat Monitoring NC I** | **ICT251313 — Conduct Vulnerability Scanning of Assets** | CyberOps Nmap lab + controlled scanning workflow | 🟡 Partial until full workflow is documented |
| **Cyber Threat Mitigation NC II** | **ICT251314 — Perform Threat Mitigation** | CyberOps investigation labs + v1.0 + BOTS v2 + controlled containment/recovery simulation | 🟡 Strong investigation; mitigation evidence must be completed |
| **Cyber Threat Mitigation NC II** | **ICT251315 — Perform Vulnerability Management/Control** | Nmap + controlled vulnerability-management/remediation workflow | 🔴 Gap until supplementary workflow is completed |

## Fixed 11 evidence domains

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

These domains will be used consistently throughout the repository.

## How the evidence domains relate to TESDA

| Evidence domain | Main TESDA relevance | Typical evidence sources |
|---|---|---|
| **01 Monitoring and Alerts** | NC I ICT251312; NC II ICT251314 | Snort, Security Onion, CyberOps v1.0, BOTS v2 |
| **02 Log/Event Analysis** | NC I ICT251312; NC II ICT251314 | Windows/Linux/server logs, Splunk, Security Onion |
| **03 Network Traffic Analysis** | NC I ICT251312; NC II ICT251314 | Wireshark, PCAP, TCP/UDP/DNS/HTTP analysis |
| **04 Endpoint Analysis** | NC I ICT251312; NC II ICT251314 | Windows processes, PowerShell, Task Manager, host artifacts |
| **05 Malware/IOC Analysis** | NC I ICT251312; NC II ICT251314 | Hashing, malware investigation, PCAP extraction, IOC analysis |
| **06 Vulnerability Scanning** | NC I ICT251313; NC II ICT251315 | Nmap and controlled vulnerability-scanning simulation |
| **07 Incident Investigation** | NC I ICT251312; NC II ICT251314 | CyberOps v1.0, BOTS v2, incident investigations |
| **08 Threat Intelligence** | NC I ICT251312; NC II ICT251314 | IOC enrichment, VirusTotal, external CTI, TTP analysis |
| **09 Containment** | NC II ICT251314 | Dedicated controlled containment simulation |
| **10 Recovery** | NC II ICT251314; supporting NC II ICT251315 | Eradication, restoration, validation, secondary scan |
| **11 Reporting** | NC I ICT251312; NC II ICT251314/ICT251315 | Incident reports, vulnerability reports, evidence summaries |

## Evidence-source roles

### Cisco CyberOps Associate laboratory activities

**Primary foundation.** The individual labs demonstrate technical skills that are mapped to TESDA performance requirements.

### CyberOps v1.0 Skills Assessment

**Integrated alert-driven assessment.** It provides high-value simulated investigation evidence, especially for NC I monitoring/reporting and supporting NC II incident analysis.

### BOTS v2

**Independent SIEM/threat-hunting evidence.** It complements the alert-driven assessment through simulated multi-source investigation and threat hunting.

### Controlled supplementary simulations

Used specifically to close evidence gaps, especially:

- containment;
- eradication;
- recovery;
- secondary scanning;
- vulnerability remediation;
- vulnerability-management process evidence.

## Evidence progression

```text
CYBEROPS ASSOCIATE LAB ACTIVITIES
        ↓
Technical skill development
        ↓
11 evidence domains
        ↓
CYBEROPS v1.0 SKILLS ASSESSMENT
        ↓
Alert-driven investigation
        ↓
BOTS v2
        ↓
Independent SIEM threat hunting
        ↓
CONTROLLED NC II MITIGATION SIMULATION
        ↓
Contain → Eradicate → Recover → Validate
        ↓
CONTROLLED VULNERABILITY-MANAGEMENT SIMULATION
        ↓
Scan → Assess → Remediate → Rescan → Verify
        ↓
TESDA EVIDENCE PACKAGE
```

## Controlled-environment and data-privacy rule

All portfolio activities are performed exclusively in simulated, isolated, and controlled laboratory environments using authorized training datasets, virtual machines, simulated network traffic, and designated training systems.

No production systems, live organizational networks, confidential company information, personally identifiable information, credentials, private keys, or real organizational security events are intentionally accessed, monitored, scanned, modified, contained, or recovered.

## Phase 1 decision

The portfolio will **not classify the 11 evidence domains as TESDA core competencies**. They are the practical filing and evidence structure.

The TESDA core competencies remain the assessment target, while every lab or assessment activity is mapped to the relevant evidence domain(s) and then to the applicable TESDA performance requirements.

## Phase 2

Phase 2 will create and verify the **complete Cisco CyberOps Associate lab register in the original Cisco sequence**. Each lab will receive:

- Lab number and title
- Primary evidence domain
- Related evidence domains
- CyberOps skill demonstrated
- TESDA NC I/NC II relevance
- Core competency linkage
- Direct/Supporting/Gap rating
- Evidence to capture
- Required controlled supplementary activity, if any
