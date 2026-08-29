# Cyber Threat Monitoring NC I — Core Competency Matrix

> **Status:** Baseline mapping. This matrix identifies where the Cisco CyberOps ecosystem can contribute evidence; it does not claim automatic TESDA equivalence.

## Core Competencies

| Code | TESDA core competency | Primary portfolio sources | Initial coverage |
|---|---|---|---|
| ICT251312 | Monitor and report cyber threats | CyberOps v1.0 Skills Assessment + CyberOps labs + BOTS v2 | 🟢 Strong |
| ICT251313 | Conduct vulnerability scanning of assets | CyberOps Nmap lab + controlled scanning/reporting activity | 🟡 Partial |

## ICT251312 — Monitor and report cyber threats

### Evidence architecture

| TESDA performance area | Best portfolio evidence | Rating | Evidence to capture |
|---|---|---:|---|
| Check for alerts | CyberOps v1.0 Skills Assessment — Security Onion/Sguil/Kibana alert review | 🟢 | Alert screen, alert details, analyst notes |
| Check status of security solutions | CyberOps monitoring environment; security-service verification | 🟡 | Service/status output, monitoring console |
| Manual checking and verification | CyberOps v1.0; Wireshark; log-analysis labs; BOTS v2 | 🟢 | Queries, packet/log analysis, validation notes |
| Conduct case follow-up | CyberOps v1.0; BOTS v2 correlation/investigation | 🟢 | Related alerts, timeline, pivots, findings |
| Perform alert reporting | CyberOps assessment report + TESDA-format simulated incident report | 🟡 | Completed report/ticket and simulated escalation record |

### Integrated assessment evidence

**CyberOps v1.0 Skills Assessment — Pushdo investigation** is the primary integrated NC I assessment evidence because its workflow begins with simulated security alerts and proceeds through validation, investigation, IOC identification, threat-intelligence verification, and reporting.

BOTS v2 provides independent simulated SIEM investigation/threat-hunting evidence.

## ICT251313 — Conduct vulnerability scanning of assets

| TESDA performance area | Best portfolio evidence | Rating | Evidence to capture |
|---|---|---:|---|
| Prepare/identify assets and scan scope | Controlled vulnerability-scanning simulation | 🔴 | Asset inventory, authorization, scope |
| Conduct vulnerability scan | CyberOps Nmap lab | 🟢 | Nmap command/output and designated lab target |
| Analyze scan results | Nmap + vulnerability-analysis worksheet | 🟡 | Open ports/services, findings, severity analysis |
| Document and report findings | TESDA-format simulated vulnerability report | 🟡 | Report, screenshots, recommendations |
| Verify remediation/secondary scan | Controlled remediation simulation | 🔴 | Before/after scan evidence |

### Important limitation

The Nmap lab demonstrates the **technical scanning activity**, but a complete TESDA competency requires a controlled workflow around asset identification, authorized scope, scanning, analysis, documentation, and follow-up. Those process artifacts will be added through controlled supplementary activities.

## Controlled-environment and data-privacy rule

All activities documented in this matrix are performed exclusively in simulated, isolated, and controlled laboratory environments. No production or live organizational systems are scanned, monitored, modified, or investigated for this portfolio.

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
Controlled scope → Scan → Analyze → Report → Rescan
        ↓
ICT251313 evidence
```

## Source

TESDA Training Regulations: Cyber Threat Monitoring NC I.
