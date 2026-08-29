# Cisco CyberOps Associate → TESDA Cybersecurity Evidence Portfolio

A practical evidence portfolio using **Cisco CyberOps Associate laboratory activities** as the primary technical evidence source, supplemented by the Cisco v1.0 Skills Assessment, BOTS v2, and dedicated mitigation/vulnerability-management simulations.

## Purpose

This repository organizes practical cybersecurity evidence for TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II assessment preparation and Recognition of Prior Learning (RPL).

The portfolio is built around a clear distinction:

- **TESDA core competencies** = the competency requirements being demonstrated.
- **11 evidence domains** = the categories used to organize laboratory evidence.
- **CyberOps labs** = the primary technical skills-development and evidence source.
- **Skills Assessment and BOTS v2** = higher-level assessment/investigation evidence.
- **Supplementary simulations** = activities that close TESDA competency gaps, particularly containment, recovery, and vulnerability management.

> **Important:** This portfolio is not a TESDA certification or assessment result. It is an organized evidence portfolio intended to support skills demonstration, RPL, and assessment preparation.

## TESDA target qualifications

### Cyber Threat Monitoring NC I

- **ICT251312 — Monitor and Report Cyber Threats**
- **ICT251313 — Conduct Vulnerability Scanning of Assets**

### Cyber Threat Mitigation NC II

- **ICT251314 — Perform Threat Mitigation**
- **ICT251315 — Perform Vulnerability Management/Control**

## 11 Evidence Domains

The following 11 categories are the **fixed evidence-domain structure for this repository**. They are intentionally separate from the TESDA core-competency names to avoid confusion.

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

Every CyberOps lab, Skills Assessment task, BOTS v2 activity, and supplementary exercise will be assigned a **primary evidence domain**. Related domains will be recorded as cross-references rather than unnecessarily duplicating the entire evidence package.

## Evidence ratings

| Rating | Meaning |
|---|---|
| 🟢 Direct | Activity can provide strong practical evidence for the relevant skill or performance requirement. |
| 🟡 Supporting | Activity demonstrates a related skill, but additional process or artifact evidence is needed. |
| 🔴 Gap | The activity does not adequately demonstrate the requirement; a supplementary activity is required. |

## Evidence architecture

```text
TESDA CORE COMPETENCIES
        │
        ▼
11 EVIDENCE DOMAINS
        │
        ▼
CYBEROPS ASSOCIATE LAB ACTIVITIES
        │
        ├── Guided technical evidence
        │
        ▼
CYBEROPS v1.0 SKILLS ASSESSMENT
        │
        ├── Alert-driven investigation
        │
        ▼
BOTS v2
        │
        ├── Independent SIEM threat hunting
        │
        ▼
SUPPLEMENTARY MITIGATION / VM LABS
        │
        ├── Containment
        ├── Eradication
        ├── Recovery
        ├── Secondary scanning
        └── Vulnerability management
        │
        ▼
TESDA EVIDENCE PACKAGE
```

## Phase 1

Phase 1 establishes the repository architecture. The portfolio will **retain the complete CyberOps laboratory activities as a major evidence source**. The v1.0 Skills Assessment and BOTS v2 will complement the labs rather than replace them.

The detailed Phase 1 overview is available at [`tesda-mapping/cyberops-lab-to-core-competency-overview.md`](tesda-mapping/cyberops-lab-to-core-competency-overview.md).

## Planned repository structure

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

cisco-lab-register/
tesda-mapping/
evidence/
supplementary-labs/
capstone/
templates/
```

## Evidence integrity

Only actual results from the lab environment should be uploaded. Never fabricate screenshots, logs, hashes, PCAPs, alerts, findings, or assessment results.

Remove credentials, private keys, personal information, and confidential organizational information before committing evidence.

## Recommended workflow

1. Perform the CyberOps lab.
2. Capture raw evidence.
3. Complete the lab report.
4. Assign the lab to its primary evidence domain.
5. Record related evidence domains.
6. Map the demonstrated skill to the relevant TESDA competency/performance requirement.
7. Complete the evidence checklist.
8. Perform supplementary labs for identified gaps.
9. Complete the integrated capstone.
10. Review the TESDA Evidence Index before assessment.

## Portfolio philosophy

The repository distinguishes **technical similarity** from **full competency evidence**. A Cisco lab, Skills Assessment, or BOTS v2 exercise is not automatically treated as proof of an entire TESDA competency. Each item will be mapped to the specific skill or performance requirement it actually demonstrates.
