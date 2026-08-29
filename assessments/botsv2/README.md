# BOTS v2 — Splunk Threat-Hunting Evidence

## Purpose

This folder documents the BOTS v2 threat-hunting work used as higher-level evidence for the TESDA cybersecurity portfolio.

BOTS v2 is the Splunk Boss of the SOC version 2 dataset. The official dataset is a public security dataset designed for security professionals, researchers, students, and enthusiasts. It contains endpoint, network, firewall/proxy, IDS, and other telemetry and is indexed in Splunk under `botsv2`.

## Portfolio role

BOTS v2 is positioned after the CyberOps Associate labs and the retained v1.0 Skills Assessment:

```text
CyberOps Associate Labs
        ↓
CyberOps v1.0 Skills Assessment
        ↓
BOTS v2 / Splunk Threat Hunting
        ↓
Independent Investigation
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

It provides supporting evidence for **ICT251312 — Monitor and Report Cyber Threats** and **ICT251314 — Perform Threat Mitigation**. It does not by itself demonstrate the complete containment, eradication, recovery, or vulnerability-management workflows.

## Dataset setup

The official BOTS v2 repository provides both a full dataset and an attack-only dataset. The attack-only dataset is smaller and is appropriate when the objective is focused threat-hunting practice. Only one of the two should be installed at a time.

The official documentation states that after installation the dataset can be searched with:

```spl
index=botsv2 earliest=0
```

The original dataset was generated from a realistic lab environment containing Windows endpoints, Sysmon and Windows Event Logging, Palo Alto Networks firewall/proxy telemetry, Splunk Stream, and Suricata network IDS data.

## Evidence rule

The walkthrough material is a learning guide only. The final portfolio must contain the candidate's own Splunk searches, screenshots, observations, analysis, and conclusions.

Do not present answers from walkthroughs as personal evidence.

## Working guide

See:

- `setup.md` — installation and verification
- `splunk-2-hunting-guide.md` — paraphrased threat-hunting workflow based on the supplied TryHackMe Splunk 2 reference and the linked walkthrough
- `evidence-mapping.md` — TESDA/evidence-domain mapping
- `screenshots/` — candidate-generated screenshots only

## Screenshot policy

The supplied Medium article contains screenshots that belong to its original publication. They should be treated as visual references, not automatically copied into this repository. If the user provides the images or has permission to reuse them, they can be placed in `screenshots/` with attribution. Otherwise, capture equivalent screenshots from the candidate's own Splunk/BOTS v2 session.

## References

- TryHackMe — Splunk 2: https://tryhackme.com/room/splunk2
- jniket — TryHackMe Splunk 2 walkthrough: https://medium.com/@johnniketas/tryhackme-splunk-2-e86081dbc7ce
- Official Splunk BOTS v2 dataset: https://github.com/splunk/botsv2
