# TESDA Competency Mapping

This directory is the control point for the portfolio's TESDA evidence architecture.

## Target core competencies

### Cyber Threat Monitoring NC I

- **ICT251312 — Monitor and report cyber threats**
- **ICT251313 — Conduct vulnerability scanning of assets**

### Cyber Threat Mitigation NC II

- **ICT251314 — Perform threat mitigation**
- **ICT251315 — Perform vulnerability management/control**

## Evidence-rating rule

A Cisco or CTF activity is **not automatically equivalent to a TESDA competency**. The portfolio distinguishes:

- 🟢 **Direct** — strong observable evidence for the criterion.
- 🟡 **Supporting** — develops part of the criterion; additional evidence is needed.
- 🔴 **Gap** — a dedicated controlled supplementary activity is required.

## Assessment architecture

```text
Cisco CyberOps Associate Labs
        |
        +--> CyberOps v1.0 Skills Assessment
        |       +--> Alert-driven investigation / NC I focus
        |
        +--> BOTS v2
        |       +--> SIEM investigation / threat hunting
        |
        +--> Controlled supplementary simulations
                +--> Vulnerability scanning
                +--> Containment
                +--> Eradication
                +--> Recovery
                +--> Secondary validation scan
                +--> Vulnerability management
```

There is no live-production capstone. The retained v1.0 Skills Assessment, BOTS v2, CyberOps laboratory activities, and controlled supplementary simulations collectively form the evidence architecture.

## Files in this directory

- `nc1-core-competency-matrix.md` — NC I element/performance-criterion mapping.
- `nc2-core-competency-matrix.md` — NC II element/performance-criterion mapping.
- `cyberops-skills-assessment-mapping.md` — CyberOps v1.0 assessment mapping.
- `cyberops-v1.0-skills-assessment-mapping.md` — detailed v1.0 assessment mapping.
- `botsv2-mapping.md` — BOTS v2 mapping.
- `botsv2-tesda-evidence-matrix.md` — BOTS v2 evidence-to-TESDA matrix.
- `coverage-summary.md` — consolidated coverage and evidence gaps.
- `evidence-index.md` — navigation index for evidence.
- `gap-analysis.md` — remaining competency/evidence gaps.
- `ict251315-vulnerability-management-control-matrix.md` — ICT251315 criterion-level mapping.
- `master-sag-evidence-matrix.md` — consolidated TESDA evidence matrix.

## Controlled-environment and data-privacy statement

All cybersecurity activities documented in this portfolio are performed exclusively in **simulated, isolated, and controlled laboratory environments** using authorized training datasets, virtual machines, simulated network traffic, and designated training systems.

No production systems, live organizational networks, confidential company information, personally identifiable information, credentials, private keys, or real organizational security events are intentionally accessed, monitored, scanned, modified, contained, or recovered.

## Evidence principle

Only evidence actually produced in the controlled lab environment should be included: screenshots, logs, PCAPs, hashes, reports, tickets, configurations, command output, and related artifacts. Never fabricate evidence or assessment results. Remove credentials, private keys, and personal/confidential information before committing.

Reference materials may be used for learning and cross-checking, but they are not substitutes for candidate-generated evidence.
