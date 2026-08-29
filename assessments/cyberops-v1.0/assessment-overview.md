# Cisco CyberOps Associate v1.0 Skills Assessment — Overview

## Assessment Title

**CyberOps Associates v1.0 — Skills Assessment: Pushdo Trojan Investigation**

## Purpose

This assessment demonstrates practical SOC analyst skills through the investigation of malicious activity associated with the **Pushdo Trojan** in a Security Onion environment.

The assessment is particularly valuable as evidence for the portfolio because it is **alert-driven**: the analyst starts with security alerts and performs investigation, validation, threat-intelligence research, IOC analysis, and reporting.

## Assessment Environment

- Cisco CyberOps Associate v1.0 Skills Assessment
- Security Onion virtual machine
- Sguil
- Kibana
- NetworkMiner / available Security Onion analysis tools
- Internet-based threat intelligence research
- VirusTotal for malware verification

## Skills Demonstrated

The assessment exercises:

1. Evaluating security event alerts using Sguil and Kibana.
2. Establishing the time frame of a suspected attack.
3. Identifying alerts associated with the incident.
4. Identifying internal and external IP addresses.
5. Identifying the infected host and its network-interface information.
6. Determining how the host became infected.
7. Investigating files delivered during the attack.
8. Calculating SHA-256 hashes.
9. Verifying suspected malicious files using VirusTotal.
10. Correlating additional alerts associated with the infected host.
11. Summarizing and reporting the investigation findings.

## Primary Evidence Domains

| Domain | Relevance |
|---|---|
| `01-monitoring-and-alerts` | Review and evaluation of IDS/SOC alerts |
| `02-log-event-analysis` | Correlation of event information |
| `03-network-traffic-analysis` | IP, DNS, HTTP and network-communication analysis |
| `04-endpoint-analysis` | Identification of the infected endpoint |
| `05-malware-ioc-analysis` | Malware files, hashes and indicators |
| `07-incident-investigation` | End-to-end Pushdo investigation |
| `08-threat-intelligence` | Exploit research and malware verification |
| `11-reporting` | Final incident findings |

## TESDA Relevance

### Strongest competency

**ICT251312 — Monitor and Report Cyber Threats**

The assessment provides strong practical evidence for alert review, incident verification, investigation, IOC identification, threat intelligence and reporting.

### Supporting competency

**ICT251314 — Perform Threat Mitigation**

The assessment provides supporting evidence for incident analysis, IOC identification, threat intelligence and affected-host analysis. It does **not** by itself demonstrate the complete containment, eradication, recovery and validation workflow required for a full mitigation competency.

## Evidence Status

The assessment was **performed in the CyberOps VM**. The portfolio evidence should use the learner's actual screenshots, observations, hashes, alert information and final findings.

Screenshots are intentionally not embedded in this Markdown file. They will be added manually to the `screenshots/` directory.

## Evidence Integrity

Published answer material may be used only as a cross-check when preparing this portfolio. The evidence presented here should represent the actual assessment performed by the learner.

Do not claim containment, eradication, recovery or vulnerability management from this assessment alone.

## Related Files

- `assessment-documentation.md`
- `alert-analysis.md`
- `incident-timeline.md`
- `ioc-analysis.md`
- `threat-intelligence.md`
- `findings-report.md`
