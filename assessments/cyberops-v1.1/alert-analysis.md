# Alert Analysis — CyberOps / CCNA Cybersecurity Operations v1.1

## Objective

Determine which Sguil events are associated with the suspected exploit and establish whether the activity represents malicious behavior.

## Detection source

The primary detection source is **Snort events displayed in Sguil**.

The investigation begins by selecting the events associated with the exploit and using the alert information as pivots into other Security Onion tools.

## Key alert findings

### Exploit identification

The Snort/Sguil evidence identifies the exploit kit as:

**Angler Exploit Kit (Angler EK)**

### Affected host

The event associated with the outdated Flash component identifies the affected internal host as:

`192.168.0.12`

The assessment evidence also identifies the host's MAC address and NIC vendor. Record the value observed during the actual assessment here:

- **MAC address:** `00:1b:21:ca:fe:d7`
- **NIC vendor:** ______________________________

### Exploit-delivery source

The Sguil investigation identifies the external host that appears to have delivered the exploit:

`192.99.198.158`

### Delivery domain

Supporting network evidence associates the delivery infrastructure with:

`qwe.mvdunalterableairreport.net`

## Alert interpretation

The alert sequence is consistent with an exploit-kit attack rather than an isolated benign event. The activity includes detection of an outdated client component, interaction with exploit-delivery infrastructure, and subsequent delivery of a payload.

## Investigation pivots

```text
Snort Alert
    ↓
Sguil Event
    ↓
Affected Host
    ↓
External Source
    ↓
ELSA / Bro-Zeek
    ↓
Wireshark
    ↓
Payload Extraction
```

## Screenshot placeholders

- `screenshots/01-sguil-overview.png`
- `screenshots/02-exploit-events.png`
- `screenshots/03-affected-host.png`
- `screenshots/04-delivery-source.png`

## TESDA relevance

**Primary domains:**

- 01 Monitoring and Alerts
- 02 Log/Event Analysis
- 07 Incident Investigation

**Primary competency:** ICT251312 — Monitor and Report Cyber Threats

**Supporting competency:** ICT251314 — Perform Threat Mitigation
