# BOTS v2 — Splunk Threat-Hunting Evidence

## Purpose

This folder documents BOTS v2 threat-hunting activities used as higher-level evidence for the TESDA cybersecurity portfolio.

## Controlled-environment and data-privacy statement

All BOTS v2 activities documented here are performed exclusively in a **simulated, isolated, and controlled laboratory environment** using an authorized training dataset and designated virtual/training systems.

BOTS v2 evidence must not be interpreted as monitoring, scanning, investigating, or responding to a live company's production environment. No production systems, confidential organizational information, personally identifiable information, credentials, private keys, or real organizational security events are intentionally used.

## Portfolio role

BOTS v2 is positioned after the CyberOps Associate laboratory activities and the retained v1.0 Skills Assessment:

```text
CyberOps Associate Labs
        ↓
CyberOps v1.0 Skills Assessment
        ↓
BOTS v2 / Splunk Threat Hunting
        ↓
Controlled Simulated Investigation
        ↓
TESDA Evidence Package
```

The activity is especially useful for:

- Log/event analysis
- Network traffic analysis
- Threat intelligence
- Incident investigation
- Malware/IOC analysis
- Reporting

It provides supporting evidence for **ICT251312 — Monitor and Report Cyber Threats** and **ICT251314 — Perform Threat Mitigation**. It does not by itself demonstrate complete containment, eradication, recovery, or vulnerability-management workflows.

## Dataset setup

BOTS v2 is a training dataset used in a controlled Splunk environment. The dataset may contain endpoint, network, firewall/proxy, IDS, and other telemetry representing simulated security activity.

After installation, dataset verification can use:

```spl
index=botsv2 earliest=0
```

The setup must remain isolated from production infrastructure.

## Evidence rule

The walkthrough material is used only as a learning and cross-checking resource. Final portfolio evidence must come from the candidate's own authorized laboratory investigation whenever the activity is performed.

Do not present reference answers or screenshots as candidate-generated evidence.

## Working guide

See:

- `setup.md` — controlled-environment installation and verification
- `splunk-2-hunting-guide.md` — paraphrased threat-hunting workflow based on the supplied reference
- `evidence-mapping.md` — TESDA/evidence-domain mapping
- `screenshots/` — evidence screenshots associated with the BOTS v2 investigation

## Screenshot policy

Screenshots used for the portfolio should document the candidate's own controlled BOTS v2/Splunk investigation. Reference screenshots may be used for learning or cross-checking, but they should not be represented as candidate evidence unless reuse is authorized.

Do not upload screenshots containing production data, confidential company information, credentials, private keys, or other restricted information.

## References

Reference materials are used for learning and cross-checking only. The final portfolio emphasizes candidate-generated evidence from the controlled laboratory environment.
