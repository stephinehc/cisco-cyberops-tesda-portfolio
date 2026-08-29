# Incident Timeline — Pushdo Trojan

## Overview

The timeline reconstructs the Pushdo infection and subsequent malware-delivery activity observed in the CyberOps Associate v1.0 Skills Assessment.

## Timeline

| Time (UTC) | Event | Evidence / Interpretation |
|---|---|---|
| **2017-06-27 13:38:32** | Host infection activity observed | The affected endpoint is `192.168.1.96`. |
| **~13:38:34** | Pushdo-related alert activity begins | Security Onion alerts identify suspicious activity associated with the incident. |
| **~13:38–13:44** | DNS/network activity associated with the infected host | Alerts are correlated to establish the attack sequence. |
| **~13:44:32** | End of the principal observed attack window | Final events in the assessment timeframe are reviewed. |
| **After initial compromise** | Pushdo retrieves additional executable files | `gerv.gun`, `trow.exe`, and `wp.exe` are identified for analysis. |
| **Investigation stage** | SHA-256 hashes are obtained | Hashes are used as file-level IOCs. |
| **Verification stage** | Hashes are checked against threat intelligence | VirusTotal results support the malicious classification of the files. |

## Attack Sequence

```text
User / Host Activity
        ↓
Malicious Domain / DNS Activity
        ↓
Pushdo Trojan Infection
        ↓
Pushdo Downloader Behavior
        ↓
Additional Executables Retrieved
        ↓
File / Hash Analysis
        ↓
Threat-Intelligence Verification
        ↓
Incident Findings
```

## Important Times

- **Infection activity:** approximately `2017-06-27 13:38:32 UTC`
- **Observed assessment window:** approximately `2017-06-27 13:38:34–13:44:32 UTC`

Use the learner's own Sguil/NetworkMiner screenshots as the primary evidence for timestamps.

## Timeline Evidence to Attach

- [ ] Sguil alert timestamps
- [ ] Kibana timestamps, if used
- [ ] NetworkMiner file timestamps
- [ ] Relevant DNS event
- [ ] File-download events
- [ ] Hash-analysis evidence

## TESDA Relevance

This timeline supports:

- `02-log-event-analysis/`
- `03-network-traffic-analysis/`
- `07-incident-investigation/`
- `11-reporting/`

It provides practical evidence for reconstructing and documenting a cybersecurity incident.
