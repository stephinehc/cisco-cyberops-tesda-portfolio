# Cyber Threat Mitigation NC II — Core Competency Matrix

> **Status:** Phase 1 baseline mapping. CyberOps activities provide supporting evidence for several mitigation elements, but containment, eradication, recovery, and full vulnerability-management evidence require dedicated practical activities unless demonstrably performed in the selected assessment.

## Core Competencies

| Code | TESDA core competency | Primary portfolio sources | Initial coverage |
|---|---|---|---|
| ICT251314 | Perform threat mitigation | CyberOps v1.1; CyberOps v1.0; BOTS v2; supplementary containment/recovery lab | 🟢 Strong / partial until mitigation phase is added |
| ICT251315 | Perform vulnerability management/control | Nmap + supplementary vulnerability-management/remediation lab | 🟡 Partial |

## ICT251314 — Perform threat mitigation

| TESDA performance area | Best portfolio evidence | Rating | Evidence to capture |
|---|---|---:|---|
| Check/evaluate incidents | CyberOps v1.0/v1.1; BOTS v2 | 🟢 | Alert/event evidence, classification, severity notes |
| Use cyber threat intelligence | CyberOps Skills Assessment; BOTS v2 + IOC enrichment | 🟢 | IOC enrichment, source references, TTP analysis |
| Analyze affected systems/configurations | CyberOps endpoint/log/PCAP labs; Skills Assessments | 🟢 | Process, log, PCAP and configuration evidence |
| Identify/confirm malicious files, packets or activity | CyberOps malware/PCAP activities; v1.0/v1.1 | 🟢 | File evidence, hashes, packet/log findings |
| Implement containment | Dedicated Windows/network containment simulation | 🔴 | Isolation, firewall/blocking, account-control evidence |
| Eradicate threat | Dedicated mitigation lab | 🔴 | Malware/persistence removal evidence |
| Recover affected system | Dedicated recovery/snapshot/restore lab | 🔴 | Recovery steps and validation |
| Secondary scan/validate remediation | Nmap/endpoint rescan exercise | 🟡 | Before/after scan and monitoring evidence |
| Report mitigation outcome | Incident and mitigation report | 🟡 | Final report, timeline, actions, residual risk |

### Recommended NC II sequence

```text
CyberOps v1.0
    ↓
Alert-driven incident investigation
    ↓
CyberOps v1.1 / BOTS v2
    ↓
Advanced investigation + IOC/TTP/CTI
    ↓
Containment simulation
    ↓
Eradication
    ↓
Recovery
    ↓
Secondary scan + continuous monitoring
    ↓
Final mitigation report
```

## ICT251315 — Perform vulnerability management/control

| TESDA performance area | Best portfolio evidence | Rating | Evidence to capture |
|---|---|---:|---|
| Maintain/identify asset information | Supplementary asset-inventory exercise | 🔴 | Asset register and scope |
| Plan vulnerability scanning | Nmap + TESDA-style scan plan | 🟡 | Scope, authorization, schedule |
| Conduct vulnerability assessment/scanning | CyberOps Nmap lab | 🟢 | Scan commands/results |
| Analyze and prioritize vulnerabilities | Supplementary vulnerability-analysis worksheet | 🟡 | Severity/risk assessment |
| Recommend/implement remediation | Dedicated patch/configuration lab | 🔴 | Before/after configuration and remediation |
| Validate remediation | Secondary scan | 🟡 | Before/after scan comparison |
| Report vulnerability-management results | Vulnerability-management report | 🟡 | Findings, risk, remediation status |

## Key limitation

CyberOps and BOTS v2 are strongest in **detection and investigation**. They should not be presented as proof of the entire NC II mitigation competency unless the evidence actually shows the candidate performing mitigation and recovery. This portfolio therefore deliberately reserves dedicated supplementary labs for containment, eradication, recovery, remediation, and validation.

## Source

TESDA Training Regulations: Cyber Threat Mitigation NC II. citehttps://www.tesda.gov.ph/Downloadables/TRs/TR-Cyber-threat-mitigation%20NC%20II.pdf
