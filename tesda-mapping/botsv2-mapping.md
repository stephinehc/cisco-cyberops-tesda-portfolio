# BOTS v2 → TESDA Mapping

## Role in this portfolio

BOTS v2 is treated as an **advanced SIEM investigation and threat-hunting environment**, not as a replacement for the alert-driven CyberOps Skills Assessment.

### Simulation distinction

- **CyberOps v1.0:** an analyst receives/opens a security alert and investigates it.
- **BOTS v2:** an analyst searches and correlates a large security dataset to discover and investigate suspicious activity.
- **NC II mitigation simulation:** the analyst takes containment, eradication and recovery actions after confirming the incident.

## Initial mapping

| TESDA competency | BOTS v2 contribution | Rating |
|---|---|---:|
| ICT251312 Monitor and report cyber threats | SIEM investigation, event correlation, affected-host/account identification and reporting | 🟢 Strong |
| ICT251313 Vulnerability scanning | Not the primary purpose of BOTS v2 | 🔴 Gap |
| ICT251314 Perform threat mitigation | Incident investigation, IOC/TTP identification and CTI enrichment | 🟢 Strong supporting |
| ICT251315 Vulnerability management/control | Limited/indirect | 🟡/🔴 Supplementary lab required |

## Recommended BOTS evidence workflow

```text
Splunk / BOTS dataset
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

- vulnerability scanning
- vulnerability remediation
- network/endpoint containment
- malware eradication
- system recovery
- secondary validation scanning

Those activities belong in the supplementary practical-lab layer.

## Capstone role

Use BOTS v2 **after CyberOps v1.0/v1.1** as an independent investigation exercise. A final NC II simulation can then take the BOTS findings and require the candidate to contain, eradicate, recover, rescan and report.

## Source

Splunk BOTS v2 is an open security dataset/CTF environment used for security investigation and training. citehttps://github.com/splunk/botsv2
