# BOTS v2 → TESDA Mapping

## Role in this portfolio

BOTS v2 is treated as an **independent SIEM investigation and threat-hunting environment** that complements the alert-driven CyberOps v1.0 Skills Assessment.

### Simulation distinction

- **CyberOps v1.0:** an analyst receives/opens a simulated security alert and investigates it in the training environment.
- **BOTS v2:** an analyst searches and correlates a simulated security dataset to discover and investigate suspicious activity.
- **Controlled NC II mitigation simulation:** the analyst performs containment, eradication and recovery actions against designated simulated laboratory systems after confirming the simulated incident.

All activities are performed in simulated, isolated, and controlled environments. They do not involve live organizational production infrastructure.

## Initial mapping

| TESDA competency | BOTS v2 contribution | Rating |
|---|---|---:|
| ICT251312 Monitor and report cyber threats | SIEM investigation, event correlation, affected-host/account identification and reporting | 🟢 Strong |
| ICT251313 Vulnerability scanning | Not the primary purpose of BOTS v2 | 🔴 Gap |
| ICT251314 Perform threat mitigation | Incident investigation, IOC/TTP identification and CTI enrichment | 🟢 Strong supporting |
| ICT251315 Vulnerability management/control | Limited/indirect | 🟡/🔴 Controlled supplementary lab required |

## Recommended BOTS evidence workflow

```text
Splunk / BOTS training dataset
        ↓
Initial search
        ↓
Suspicious event discovery
        ↓
Pivot and correlate
        ↓
Affected host/account identification
        ↓
Timeline reconstruction
        ↓
IOC extraction
        ↓
TTP identification
        ↓
CTI enrichment
        ↓
Incident classification / impact
        ↓
Investigation report
```

## Evidence to capture

- Splunk search queries
- event/result screenshots
- relevant fields and timestamps
- affected hosts/accounts
- IP addresses/domains/URLs
- file names and hashes where present
- attack timeline
- IOC list
- TTP analysis
- CTI enrichment notes
- final investigation report

## What BOTS does not prove by itself

BOTS v2 should not be used as sole evidence of:

- vulnerability scanning operations;
- vulnerability remediation;
- endpoint/network containment;
- malware eradication;
- system recovery/rollback;
- secondary validation scanning.

Those activities belong in the controlled supplementary simulation layer.

## Relationship to the assessment architecture

BOTS v2 follows the retained CyberOps v1.0 Skills Assessment as an independent investigation evidence source. It is not a live-production exercise and is not a substitute for the controlled mitigation and vulnerability-management simulations required to close identified TESDA evidence gaps.

## Source

Splunk BOTS v2 is an open security dataset/CTF environment used for security investigation and training. citehttps://github.com/splunk/botsv2
