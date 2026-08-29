# CCNA Cybersecurity Operations v1.1 Skills Assessment — Overview

## Purpose

This folder documents the completed **CCNA Cybersecurity Operations v1.1 Skills Assessment** as practical evidence for the portfolio.

The assessment places the analyst in a Security Onion environment and requires investigation of suspicious Sguil/Snort events. The investigation progresses from basic event identification to exploit research, source tracing, and packet-level analysis.

## Scenario

The investigation concerns an **Angler Exploit Kit (Angler EK)** attack against an internal Windows host with an outdated Flash component. The analyst must determine whether the activity is malicious and reconstruct how the exploit and payload reached the victim.

## Assessment parts

| Part | Focus | Main evidence |
|---|---|---|
| **1** | Gathering Basic Information | Sguil/Snort alerts, event count, timeframe, host identification |
| **2** | Learning About the Exploit | Angler EK research and exploit-kit behavior |
| **3** | Determining the Source of the Malware | Sguil, ELSA, host/IP/domain correlation |
| **4** | Analyzing Details of the Exploit | ELSA and Wireshark, landing page, exploit delivery, payload extraction |

## Main tools

- Security Onion
- Sguil
- Snort
- ELSA
- Bro/Zeek
- Wireshark
- Web-based research

## Evidence-domain coverage

Primary:

- `01-monitoring-and-alerts/`
- `02-log-event-analysis/`
- `03-network-traffic-analysis/`
- `04-endpoint-analysis/`
- `05-malware-ioc-analysis/`
- `07-incident-investigation/`
- `08-threat-intelligence/`
- `11-reporting/`

Not demonstrated by this assessment:

- `06-vulnerability-scanning/`
- `09-containment/`
- `10-recovery/`

## TESDA relevance

The strongest competency relationship is **ICT251312 — Monitor and Report Cyber Threats**. The assessment also provides supporting evidence for **ICT251314 — Perform Threat Mitigation**, particularly threat identification, investigation, IOC analysis, and attack reconstruction.

It does not by itself demonstrate the complete containment, eradication, recovery, secondary-scan, or vulnerability-management workflows required for later NC II evidence.

## Evidence rule

The answer reference used during project preparation is only a **cross-check**. The portfolio evidence must come from the learner's own assessment run. Screenshots will be attached manually under `screenshots/`.
