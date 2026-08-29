# Incident Timeline — CyberOps / CCNA Cybersecurity Operations v1.1

## Purpose

This timeline reconstructs the observed exploit activity from the Sguil alerts and supporting ELSA, Bro/Zeek and Wireshark evidence.

> **Note:** Insert the exact timestamps from the learner's assessment screenshots where indicated. The published answer material establishes the sequence but the portfolio should preserve the learner's actual evidence.

## Timeline

| Sequence | Event | Evidence source | Timestamp |
|---|---|---|---|
| 1 | Security monitoring detects exploit-related activity | Sguil/Snort | __________ |
| 2 | Internal host `192.168.0.12` is identified | Sguil | __________ |
| 3 | Outdated Flash-version activity is observed | Sguil | __________ |
| 4 | Victim interacts with exploit-delivery infrastructure | Sguil / Bro-Zeek | __________ |
| 5 | Exploit-delivery host `192.99.198.158` is identified | Sguil | __________ |
| 6 | Delivery domain `qwe.mvdunalterableairreport.net` is identified | ELSA / Bro-Zeek | __________ |
| 7 | Exploit traffic is examined at packet level | Wireshark | __________ |
| 8 | Payload/object is extracted from captured traffic | Wireshark | __________ |
| 9 | Extracted object is documented for analysis | Analyst notes | __________ |

## Attack sequence

```text
Victim visits/interacts with malicious web infrastructure
                    ↓
Exploit kit profiles the client
                    ↓
Client vulnerability is identified
                    ↓
Angler exploit is delivered
                    ↓
Exploit executes on the vulnerable client
                    ↓
Malware payload is delivered
                    ↓
Analyst detects and investigates the events
```

## Key infrastructure

| Role | Indicator |
|---|---|
| Affected internal host | `192.168.0.12` |
| Exploit-delivery IP | `192.99.198.158` |
| Exploit-delivery domain | `qwe.mvdunalterableairreport.net` |
| Extracted object | `3xdz3bcxc8` |

## Evidence requirements

Attach screenshots showing the event timestamps and supporting records. Do not invent timestamps if they are not visible in the learner's evidence.

## TESDA relevance

The timeline supports incident detection, case follow-up, event correlation, attack reconstruction and reporting.

Primary evidence domains:

- 02 Log/Event Analysis
- 03 Network Traffic Analysis
- 07 Incident Investigation
- 11 Reporting
