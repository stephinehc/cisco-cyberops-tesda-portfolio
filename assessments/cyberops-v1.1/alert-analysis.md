# Alert Analysis — CCNA Cybersecurity Operations v1.1

## Objective

Analyze the Sguil/Snort events that belong to the multi-stage exploit and determine whether the activity is suspicious.

## Detection source

The primary detection point is the **Snort event set displayed in Sguil**.

The analyst should first establish the relevant event group, then use the alerts as pivots into ELSA, Bro/Zeek and Wireshark.

## Part 1 results

| Question area | Assessment result |
|---|---|
| Exploit-related events | **15 events** |
| Start time | **2017-09-07 15:31:12** |
| End time | **2017-09-07 15:31:34** |
| Duration | **22 seconds** |
| Internal host | **192.168.0.12** |
| MAC address | **00:1b:21:ca:fe:d7** |
| Operating system | **Windows-based** |
| Exploit kit | **Angler EK** |

## Alert interpretation

The events should be treated as suspicious because the alert set combines:

- an outdated Flash component;
- exploit-kit detection;
- external exploit infrastructure; and
- subsequent payload-delivery evidence.

The evidence is stronger when the alerts are correlated rather than interpreted individually.

## Investigation pivots

```text
Sguil / Snort
      ↓
Event group
      ↓
Victim host
      ↓
External infrastructure
      ↓
ELSA / Bro-Zeek
      ↓
Wireshark
```

## Screenshot placeholders

- `screenshots/01-sguil-overview.png`
- `screenshots/02-exploit-event-group.png`
- `screenshots/03-host-identification.png`

## TESDA relevance

**Primary:**

- `01-monitoring-and-alerts/`
- `02-log-event-analysis/`
- `07-incident-investigation/`

**Primary competency:** ICT251312 — Monitor and Report Cyber Threats

**Supporting competency:** ICT251314 — Perform Threat Mitigation
