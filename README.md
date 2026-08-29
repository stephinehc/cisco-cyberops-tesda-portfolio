# Cisco CyberOps Associate → TESDA Cybersecurity Evidence Portfolio

A practical evidence portfolio mapping **Cisco CyberOps Associate laboratory activities** to the TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II core competencies.

## Purpose

This repository demonstrates practical cybersecurity skills through:

- Cisco CyberOps Associate laboratory activities
- Cisco CyberOps v1.0 and v1.1 Skills Assessments
- BOTS v2 SIEM/threat-hunting activities
- controlled supplementary cybersecurity simulations
- technical evidence
- operational/process evidence
- incident and vulnerability reports
- TESDA performance-criterion mapping

> **Important:** This portfolio is not a TESDA certification or assessment result. It is an organized evidence portfolio intended to support skills demonstration, Recognition of Prior Learning (RPL), and assessment preparation.

## TESDA target qualifications

### Cyber Threat Monitoring NC I

- ICT251312 — Monitor and Report Cyber Threats
- ICT251313 — Conduct Vulnerability Scanning of Assets

### Cyber Threat Mitigation NC II

- ICT251314 — Perform Threat Mitigation
- ICT251315 — Perform Vulnerability Management/Control

## Evidence ratings

| Rating | Meaning |
|---|---|
| 🟢 Direct | Activity can provide strong practical evidence for the relevant skill/criterion |
| 🟡 Supporting | Related evidence exists, but additional process/artifact evidence is needed |
| 🔴 Gap | Supplementary practical activity is required |

## Evidence strategy

The portfolio deliberately uses **CyberOps laboratory activities as the foundation**. The Skills Assessments and BOTS v2 are layered on top of those labs:

```text
CyberOps Associate Labs
        ↓
Technical skill development
        ↓
CyberOps v1.0 Skills Assessment
        ↓
Alert-driven SOC investigation
        ↓
CyberOps v1.1 Skills Assessment
        ↓
Advanced investigation / analysis
        ↓
BOTS v2
        ↓
Independent SIEM threat hunting
        ↓
Containment / Eradication / Recovery
        ↓
Validation + Secondary Scan
        ↓
TESDA Evidence Package
```

## Cybersecurity evidence domains

1. Monitoring and Alerts
2. Log/Event Analysis
3. Network Traffic Analysis
4. Endpoint Analysis
5. Malware/IOC Analysis
6. Vulnerability Scanning
7. Incident Investigation
8. Threat Intelligence
9. Containment
10. Recovery
11. Reporting

## Phase 1

Phase 1 establishes the competency architecture and evidence strategy. The detailed overview is available in [`tesda-mapping/cyberops-lab-to-core-competency-overview.md`](tesda-mapping/cyberops-lab-to-core-competency-overview.md).

Phase 1 confirms that the portfolio will retain the **actual CyberOps lab activities** and will not rely only on the v1.0/v1.1 Skills Assessments.

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
4. Identify relevant TESDA performance criteria.
5. Place evidence in the correct domain.
6. Complete the evidence checklist.
7. Perform supplementary labs for identified gaps.
8. Complete the integrated capstone.
9. Review the TESDA Evidence Index before assessment.

## Portfolio philosophy

The repository distinguishes **technical similarity** from **full competency evidence**. A Cisco lab, Skills Assessment, or BOTS v2 exercise is not automatically treated as proof of an entire TESDA competency. Each item will be mapped to the specific skill or performance requirement it actually demonstrates.
