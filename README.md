# Cisco CyberOps Associate → TESDA Cybersecurity Evidence Portfolio

A cybersecurity evidence portfolio using **Cisco CyberOps Associate laboratory activities** as the primary technical evidence source, supplemented by the Cisco v1.0 Skills Assessment, BOTS v2, and controlled simulation activities for identified competency gaps.

## Purpose

This repository organizes cybersecurity evidence for TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II assessment preparation on Recognition of Prior Learning (RPL).

## Controlled-environment and data-privacy statement

**All activities documented in this portfolio are performed exclusively in simulated, isolated, and controlled laboratory environments using authorized training datasets, virtual machines, simulated network traffic, and intentionally configured training systems.**

No production systems, live organizational networks, confidential company information, personally identifiable information, credentials, private keys, or real organizational security events are intentionally accessed, monitored, scanned, modified, contained, or recovered as part of this portfolio.

The portfolio demonstrates technical capability through authorized simulation and training environments. It must not be interpreted as documentation of cybersecurity operations performed against a live company's production infrastructure.

## TESDA target qualifications

### Cyber Threat Monitoring NC I

- **ICT251312 — Monitor and Report Cyber Threats**
- **ICT251313 — Conduct Vulnerability Scanning of Assets**

### Cyber Threat Mitigation NC II

- **ICT251314 — Perform Threat Mitigation**
- **ICT251315 — Perform Vulnerability Management/Control**

## 11 Evidence Domains

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

The 11 domains organize the type of evidence demonstrated. They are intentionally separate from the four TESDA core competencies.

## Evidence architecture

```text
TESDA CORE COMPETENCIES
        ↓
11 EVIDENCE DOMAINS
        ↓
CYBEROPS ASSOCIATE LAB ACTIVITIES
        ↓
CYBEROPS v1.0 SKILLS ASSESSMENT
        ↓
BOTS v2 / SIEM THREAT HUNTING
        ↓
CONTROLLED SUPPLEMENTARY SIMULATIONS
        ├── Containment / Eradication
        ├── Recovery / Rollback
        ├── Secondary Validation
        └── Vulnerability Scanning / Management
        ↓
TESDA EVIDENCE PACKAGE
```

## Evidence ratings

| Rating | Meaning |
|---|---|
| 🟢 Direct | The controlled laboratory activity can provide strong observable evidence for the relevant skill or requirement. |
| 🟡 Supporting | The activity demonstrates a related skill, but an additional artifact or simulation step is needed. |
| 🔴 Gap | Existing evidence does not adequately demonstrate the requirement; a separate controlled simulation is required. |

## Repository structure

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

assessments/
├── cyberops-v1.0/
└── botsv2/

cisco-lab-register/
tesda-mapping/
evidence/
supplementary-labs/
templates/
```

There is no live-production capstone. The v1.0 Skills Assessment, BOTS v2 investigations, CyberOps laboratory activities, and controlled supplementary simulations collectively provide the evidence architecture.

## Evidence integrity and privacy

Only actual results from authorized laboratory environments should be uploaded. Never fabricate screenshots, logs, hashes, PCAPs, alerts, findings, or assessment results.

Do not upload production data, confidential organizational information, personally identifiable information, credentials, private keys, or other restricted information.

If an artifact could contain sensitive information, use sanitized training evidence or omit the artifact rather than exposing real data.

## Recommended workflow

1. Perform the CyberOps activity in the controlled laboratory environment.
2. Capture the relevant laboratory evidence.
3. Document the activity and observed result.
4. Assign the activity to its primary evidence domain.
5. Record related evidence domains.
6. Map the demonstrated skill to the relevant TESDA competency/performance requirement.
7. Identify evidence gaps.
8. Use controlled supplementary simulations only where a required competency is not demonstrated by existing evidence.
9. Review the final TESDA Evidence Index before assessment.

## Portfolio philosophy

The repository distinguishes **technical similarity** from **full competency evidence**. Completing a course lab, Skills Assessment, or BOTS v2 investigation does not automatically establish an entire TESDA competency. Each item is mapped only to the skill or performance requirement that the available evidence can reasonably demonstrate.

All conclusions in this repository are based on simulated, isolated, and controlled training activities and are not claims about live organizational cybersecurity operations.
