# TESDA Competency Mapping

This directory is the control point for the portfolio's TESDA evidence architecture.

## Target core competencies

### Cyber Threat Monitoring NC I

- **ICT251312 — Monitor and report cyber threats**
- **ICT251313 — Conduct vulnerability scanning of assets**

### Cyber Threat Mitigation NC II

- **ICT251314 — Perform threat mitigation**
- **ICT251315 — Perform vulnerability management/control**

The TESDA Training Regulations identify these as the four core competencies of the two target qualifications. The NC I TR covers monitoring/reporting and vulnerability scanning; the NC II TR covers threat mitigation and vulnerability management/control. citehttps://www.tesda.gov.ph/Downloadables/TRs/TR-Cyber%20Threat%20Monitoring%20NC%20I.pdf citehttps://www.tesda.gov.ph/Downloadables/TRs/TR-Cyber-threat-mitigation%20NC%20II.pdf

## Evidence-rating rule

A Cisco or CTF activity is **not automatically equivalent to a TESDA competency**. The portfolio distinguishes:

- 🟢 **Direct** — strong observable practical evidence for the criterion.
- 🟡 **Supporting** — develops part of the criterion; additional process, documentation, or practical evidence is needed.
- 🔴 **Gap** — a dedicated supplementary activity is required.

## Assessment architecture

```text
Cisco CyberOps Associate Labs
        |
        +--> CyberOps v1.0 Skills Assessment
        |       +--> Alert-driven investigation / NC I focus
        |
        +--> CyberOps v1.1 Skills Assessment
        |       +--> Advanced investigation / NC II support
        |
        +--> BOTS v2
        |       +--> SIEM investigation / threat hunting
        |
        +--> Supplementary labs
                +--> Vulnerability scanning
                +--> Containment
                +--> Eradication
                +--> Recovery
                +--> Secondary scan
                +--> Vulnerability management
```

## Files in this directory

- `nc1-core-competency-matrix.md` — NC I element/performance-criterion mapping.
- `nc2-core-competency-matrix.md` — NC II element/performance-criterion mapping.
- `cyberops-skills-assessment-mapping.md` — v1.0/v1.1 assessment mapping.
- `botsv2-mapping.md` — BOTS v2 mapping.
- `coverage-summary.md` — consolidated coverage and evidence gaps.

## Evidence principle

Only evidence actually produced in the controlled lab environment should be included: screenshots, logs, PCAPs, hashes, reports, tickets, configurations, command output, and related artifacts. Never fabricate evidence or assessment results. Remove credentials, private keys, and personal/confidential information before committing.
