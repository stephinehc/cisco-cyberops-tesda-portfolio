# Cisco CyberOps Associate Skills Assessment → TESDA Mapping

## Purpose

This document maps the **Cisco CyberOps Associate v1.0 Skills Assessment** to the TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II competencies represented in this portfolio.

The assessment is treated as a source of practical evidence from an authorized **simulated, isolated, and controlled laboratory environment**. Completion of the assessment does not automatically establish TESDA competency; the evidence must be evaluated against the applicable performance criteria.

## Controlled-environment and data-privacy statement

The assessment documented here is performed exclusively in a simulated Cisco CyberOps training environment using designated virtual machines and training data.

No live organizational network, production system, confidential company information, personally identifiable information, production credentials, private keys, or real organizational security incident is intentionally accessed or investigated.

## v1.0 — primary integrated assessment evidence

The v1.0 Pushdo investigation is an alert-driven SOC exercise. Its strongest evidence sequence is:

```text
Simulated security alert
   ↓
Alert review / triage
   ↓
Affected training endpoint identification
   ↓
Event and network-traffic investigation
   ↓
Malicious training file / IOC identification
   ↓
Hash and threat-intelligence verification
   ↓
Related-alert correlation
   ↓
Investigation findings
   ↓
Simulated incident report
```

## TESDA mapping

| TESDA competency | v1.0 evidence | Rating |
|---|---|---:|
| ICT251312 — Monitor and Report Cyber Threats | Simulated alert review and investigation | 🟢 Direct |
| ICT251312 — manual verification | Simulated alert, host, network and file analysis | 🟢 Direct |
| ICT251312 — case follow-up | Related simulated alert/event correlation | 🟢 Direct |
| ICT251312 — reporting | Investigation findings/report | 🟡 Supporting until all required reporting artifacts are verified |
| ICT251313 — Conduct Vulnerability Scanning of Assets | Vulnerability scanning is not the focus of v1.0 | 🔴 Gap |
| ICT251314 — Perform Threat Mitigation | Simulated incident analysis and IOC identification | 🟡 Supporting |
| ICT251315 — Perform Vulnerability Management/Control | Vulnerability management is not the focus of v1.0 | 🔴 Gap |

## Evidence-domain alignment

The assessment contributes evidence primarily to:

- `01-monitoring-and-alerts/` — simulated alert review and triage
- `02-log-event-analysis/` — simulated event correlation
- `03-network-traffic-analysis/` — simulated network investigation
- `04-endpoint-analysis/` — simulated affected-host analysis
- `05-malware-ioc-analysis/` — simulated malicious-file and IOC analysis
- `07-incident-investigation/` — integrated simulated investigation
- `08-threat-intelligence/` — threat-intelligence verification
- `11-reporting/` — investigation findings and reporting

## What v1.0 does not demonstrate by itself

The assessment should **not** be used as evidence that the following complete activities were performed:

- containment of a live or production endpoint;
- eradication of malware from a production system;
- recovery or rollback of a production system;
- secondary validation scanning after recovery;
- vulnerability-management lifecycle activities;
- vulnerability scanning of live organizational assets.

Where TESDA performance criteria require these activities, the portfolio will use separate **controlled and isolated simulations**.

## Evidence requirements for final RPL package

Before final submission, verify that the repository contains the candidate's own assessment artifacts for the activities claimed, such as:

1. Simulated alert evidence.
2. Simulated event/timeframe evidence.
3. Source and destination information.
4. Simulated affected-endpoint evidence.
5. Infection-method evidence.
6. Simulated malicious-file evidence.
7. Hash calculation/result evidence.
8. Threat-intelligence verification evidence.
9. Related-alert correlation evidence.
10. Investigation findings/report.

Reference answer material may be used for preparation and cross-checking but must not be represented as candidate-generated evidence.

## Assessment progression

```text
CyberOps Associate laboratory practice
        ↓
CyberOps v1.0 Skills Assessment
        ↓
Integrated simulated SOC investigation
        ↓
Controlled containment / eradication / recovery simulation
        ↓
Controlled vulnerability scanning / management simulation
        ↓
Final TESDA evidence package
```

## Sources

TESDA competency definitions should be based on the applicable Training Regulations. Cisco course/assessment material is used only to describe the assessment activities represented by the candidate's controlled laboratory evidence.
