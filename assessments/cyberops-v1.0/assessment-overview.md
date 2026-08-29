# Cisco CyberOps Associate v1.0 Skills Assessment — Overview

## Assessment Title

**CyberOps Associate v1.0 — Skills Assessment: Pushdo Trojan Investigation**

## Purpose

This assessment demonstrates SOC analyst capabilities through investigation of simulated malicious activity associated with the **Pushdo Trojan** in an isolated Security Onion training environment.

The assessment is particularly useful as portfolio evidence because it is alert-driven: the analyst begins with simulated security alerts and performs investigation, validation, threat-intelligence research, IOC analysis, and reporting.

## Assessment Environment

The assessment is performed exclusively in a **simulated, isolated, and controlled laboratory environment** using the Cisco CyberOps training VM and designated training tools.

- Cisco CyberOps Associate v1.0 Skills Assessment
- Security Onion virtual machine
- Sguil
- Kibana
- NetworkMiner / available Security Onion analysis tools
- Controlled threat-intelligence research resources
- VirusTotal for training-data verification

No live organizational network or production system is part of this assessment.

## Skills Demonstrated

The assessment exercises:

1. Evaluating simulated security event alerts using Sguil and Kibana.
2. Establishing the timeframe of a simulated security event.
3. Identifying alerts associated with the simulated incident.
4. Identifying internal and external IP addresses in the training scenario.
5. Identifying the affected training endpoint and its network-interface information.
6. Determining the simulated infection method.
7. Investigating files associated with the simulated attack.
8. Calculating SHA-256 hashes for training artifacts.
9. Verifying suspected malicious files using VirusTotal.
10. Correlating additional alerts associated with the simulated endpoint.
11. Summarizing and reporting simulated investigation findings.

## Primary Evidence Domains

| Domain | Relevance |
|---|---|
| `01-monitoring-and-alerts` | Review and evaluation of simulated IDS/SOC alerts |
| `02-log-event-analysis` | Correlation of simulated event information |
| `03-network-traffic-analysis` | IP, DNS, HTTP and simulated network-communication analysis |
| `04-endpoint-analysis` | Identification and analysis of the simulated affected endpoint |
| `05-malware-ioc-analysis` | Malware files, hashes and simulated indicators |
| `07-incident-investigation` | End-to-end simulated Pushdo investigation |
| `08-threat-intelligence` | Threat research and malware verification using training artifacts |
| `11-reporting` | Documentation of simulated investigation findings |

## TESDA Relevance

### Strongest competency

**ICT251312 — Monitor and Report Cyber Threats**

The assessment provides controlled-laboratory evidence for alert review, incident verification, investigation, IOC identification, threat intelligence and reporting.

### Supporting competency

**ICT251314 — Perform Threat Mitigation**

The assessment provides supporting evidence for incident analysis, IOC identification, threat intelligence and affected-host analysis. It does **not** by itself demonstrate the complete containment, eradication, recovery and validation workflow required for full mitigation evidence.

## Evidence Status

The assessment was performed in the **controlled Cisco CyberOps training VM**. The portfolio evidence should use the learner's actual laboratory screenshots, observations, hashes, alert information and findings.

Screenshots are maintained separately so that the evidence can be associated with the actual laboratory artifacts.

## Evidence Integrity and Privacy

Published answer material may be used only as a cross-check when preparing the portfolio. Evidence presented here must represent the assessment actually performed in the controlled training environment.

Do not include production data, confidential organizational information, personally identifiable information, credentials, private keys, or other restricted information.

Do not claim that this assessment involved a live organizational incident or production response. Do not claim containment, eradication, recovery, or vulnerability management from this assessment alone.

## Related Files

- `assessment-documentation.md`
- `alert-analysis.md`
- `incident-timeline.md`
- `ioc-analysis.md`
- `threat-intelligence.md`
- `findings-report.md`
