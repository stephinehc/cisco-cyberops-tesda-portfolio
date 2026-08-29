# Cyber Threat Monitoring NC I — Core Competency Matrix

> **Status:** Phase 1 baseline mapping. This matrix identifies where the Cisco CyberOps ecosystem can contribute evidence; it does not claim automatic TESDA equivalence.

## Core Competencies

| Code | TESDA core competency | Primary portfolio sources | Initial coverage |
|---|---|---|---|
| ICT251312 | Monitor and report cyber threats | CyberOps v1.0 Skills Assessment; CyberOps v1.1; BOTS v2 | 🟢 Strong |
| ICT251313 | Conduct vulnerability scanning of assets | CyberOps Nmap lab + supplementary scanning/reporting activity | 🟡 Partial |

## ICT251312 — Monitor and report cyber threats

### Evidence architecture

| TESDA performance area | Best portfolio evidence | Rating | Evidence to capture |
|---|---|---:|---|
| Check for alerts | CyberOps v1.0 Skills Assessment — Security Onion/Sguil/Kibana alert review | 🟢 | Alert screen, alert details, analyst notes |
| Check status of third-party security solutions | CyberOps monitoring environment; security-service verification | 🟡 | Service/status output, monitoring console |
| Manual checking and verification | CyberOps v1.0/v1.1; Wireshark; log-analysis labs | 🟢 | Queries, packet/log analysis, validation notes |
| Conduct case follow-up | CyberOps v1.0; BOTS v2 correlation/investigation | 🟢 | Related alerts, timeline, pivots, findings |
| Perform alert reporting | CyberOps assessment report + TESDA-format incident report | 🟡 | Completed report/ticket and escalation record |

### Recommended capstone evidence

**CyberOps v1.0 Skills Assessment — Pushdo investigation** should be the primary NC I practical evidence because its workflow begins with security alerts and proceeds through validation, investigation, IOC identification, threat-intelligence verification, and reporting.

BOTS v2 can then provide independent SIEM investigation/threat-hunting evidence, while v1.1 can provide additional advanced analyst evidence.

## ICT251313 — Conduct vulnerability scanning of assets

| TESDA performance area | Best portfolio evidence | Rating | Evidence to capture |
|---|---|---:|---|
| Prepare/identify assets and scan scope | Supplementary vulnerability-scanning exercise | 🔴 | Asset inventory, authorization, scope |
| Conduct vulnerability scan | CyberOps Nmap lab | 🟢 | Nmap command/output and scan target |
| Analyze scan results | Nmap + vulnerability-analysis worksheet | 🟡 | Open ports/services, findings, severity analysis |
| Document and report findings | TESDA-format vulnerability report | 🟡 | Report, screenshots, recommendations |
| Verify remediation/secondary scan | Supplementary remediation lab | 🔴 | Before/after scan evidence |

### Important limitation

The Nmap lab demonstrates the **technical scanning activity**, but a complete TESDA competency requires a controlled workflow around asset identification, authorized scope, scanning, analysis, documentation, and follow-up. Those process artifacts must be added to the portfolio.

## NC I evidence strategy

```text
CyberOps foundational labs
        ↓
CyberOps v1.0 Skills Assessment
        ↓
Alert → Validate → Investigate → IOC → Verify → Report
        ↓
ICT251312 evidence

CyberOps Nmap lab
        ↓
Asset scope → Scan → Analyze → Report → Rescan
        ↓
ICT251313 evidence
```

## Source

TESDA Training Regulations: Cyber Threat Monitoring NC I. citehttps://www.tesda.gov.ph/Downloadables/TRs/TR-Cyber%20Threat%20Monitoring%20NC%20I.pdf
