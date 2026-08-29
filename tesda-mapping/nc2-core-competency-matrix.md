# Cyber Threat Mitigation NC II — Core Competency Matrix

> **Status:** Baseline mapping. CyberOps activities provide supporting evidence for several mitigation elements, but containment, eradication, recovery, and full vulnerability-management evidence require dedicated controlled practical activities unless demonstrably performed in an existing assessment.

## Core Competencies

| Code | TESDA core competency | Primary portfolio sources | Initial coverage |
|---|---|---|---|
| ICT251314 | Perform threat mitigation | CyberOps v1.0; BOTS v2; controlled containment/recovery simulation | 🟢 Strong / partial until mitigation phase is added |
| ICT251315 | Perform vulnerability management/control | Nmap + controlled vulnerability-management/remediation simulation | 🟡 Partial |

## ICT251314 — Perform threat mitigation

| TESDA performance area | Best portfolio evidence | Rating | Evidence to capture |
|---|---|---:|---|
| Check/evaluate incidents | CyberOps v1.0; BOTS v2 | 🟢 | Simulated alert/event evidence, classification, severity notes |
| Use cyber threat intelligence | CyberOps v1.0; BOTS v2 + IOC enrichment | 🟢 | IOC enrichment, source references, TTP analysis |
| Analyze affected systems/configurations | CyberOps endpoint/log/PCAP labs; v1.0; BOTS v2 | 🟢 | Process, log, PCAP and configuration evidence |
| Identify/confirm malicious files, packets or activity | CyberOps malware/PCAP activities; v1.0; BOTS v2 | 🟢 | File evidence, hashes, packet/log findings |
| Implement containment | Dedicated controlled containment simulation | 🔴 | Simulated isolation, firewall/blocking, account-control evidence |
| Eradicate threat | Dedicated controlled mitigation simulation | 🔴 | Simulated malware/persistence removal evidence |
| Recover affected system | Dedicated controlled recovery/snapshot/restore simulation | 🔴 | Recovery steps and validation |
| Secondary scan/validate remediation | Nmap/endpoint rescan simulation | 🟡 | Before/after scan and monitoring evidence |
| Report mitigation outcome | Simulated incident and mitigation report | 🟡 | Final report, timeline, actions, residual risk |

### Recommended NC II sequence

```text
CyberOps v1.0
    ↓
Alert-driven simulated incident investigation
    ↓
BOTS v2
    ↓
Independent simulated investigation + IOC/TTP/CTI
    ↓
Controlled containment simulation
    ↓
Controlled eradication
    ↓
Controlled recovery
    ↓
Secondary scan + continuous simulated monitoring
    ↓
Final simulated mitigation report
```

## ICT251315 — Perform vulnerability management/control

| TESDA performance area | Best portfolio evidence | Rating | Evidence to capture |
|---|---|---:|---|
| Maintain/identify asset information | Controlled asset-inventory simulation | 🔴 | Asset register and scope |
| Plan vulnerability scanning | Nmap + controlled scan plan | 🟡 | Scope, authorization, schedule |
| Conduct vulnerability assessment/scanning | CyberOps Nmap lab | 🟢 | Scan commands/results against designated lab assets |
| Analyze and prioritize vulnerabilities | Controlled vulnerability-analysis worksheet | 🟡 | Severity/risk assessment |
| Recommend/implement remediation | Controlled patch/configuration simulation | 🔴 | Before/after configuration and remediation |
| Validate remediation | Secondary controlled scan | 🟡 | Before/after scan comparison |
| Report vulnerability-management results | Simulated vulnerability-management report | 🟡 | Findings, risk, remediation status |

## Key limitation

CyberOps and BOTS v2 are strongest in **detection and investigation**. They should not be presented as proof of the entire NC II mitigation competency unless the evidence actually shows the required mitigation actions. This portfolio therefore reserves dedicated controlled simulations for containment, eradication, recovery, remediation, and validation.

## Controlled-environment and data-privacy rule

All activities documented in this matrix are performed exclusively in simulated, isolated, and controlled laboratory environments. No production or live organizational systems are used for monitoring, scanning, containment, eradication, recovery, or vulnerability management.

## Source

TESDA Training Regulations: Cyber Threat Mitigation NC II.
