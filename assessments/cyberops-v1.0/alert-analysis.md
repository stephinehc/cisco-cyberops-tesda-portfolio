# Alert Analysis — Pushdo Trojan Investigation

## Objective

Review Security Onion alerts to establish whether the observed activity represents a malicious Pushdo Trojan infection and identify the systems and communications involved.

## Alert-Analysis Workflow

```text
Alert generated
    ↓
Review timestamp
    ↓
Review source/destination
    ↓
Identify alert type
    ↓
Correlate related alerts
    ↓
Identify affected host
    ↓
Investigate payload/file activity
    ↓
Confirm malicious behavior
```

## Initial Alert Review

The assessment begins with Sguil/Kibana alert data. The analyst focuses on the time period associated with the Pushdo activity and reviews alerts that involve the affected endpoint.

The observed incident window is approximately:

**27 June 2017, 13:38:34–13:44:32 UTC**

## Key Alert Evidence

The assessment identifies multiple alerts associated with the Pushdo activity. Alert details should be documented from the learner's actual Sguil/Kibana session.

### Alert categories of interest

- Pushdo-related activity
- DNS lookup activity
- External IP lookup/policy activity
- HTTP/file-transfer activity
- Alerts associated with the infected host

One notable event is an **ET POLICY External IP Lookup** associated with a DNS lookup for `myip.opendns.com` and destination infrastructure including `208.67.222.222`.

The policy alert is useful as contextual evidence but should be correlated with the other alerts before being treated as proof of compromise.

## Infected Endpoint

The investigation identifies:

| Field | Finding |
|---|---|
| Internal IP | `192.168.1.96` |
| MAC | `00-15-C5-DE-C7-3B` |
| NIC Vendor | Dell Inc. |

## External Infrastructure

The assessment data contains external addresses associated with the observed activity. These should be documented directly from the learner's Sguil/Kibana evidence. Known external addresses visible in the assessment material include:

- `208.67.222.222`
- `208.83.223.34`
- `198.1.85.250`

These addresses should be treated as **incident evidence for this lab dataset**, not as current malicious-IP indicators.

## Analyst Conclusion

The correlated alert activity supports the conclusion that the internal host was involved in a Pushdo Trojan infection. The analyst then pivots from alert review to host, file and threat-intelligence analysis.

## Screenshot Placeholders

Add actual screenshots manually:

- `screenshots/01-so-status.png`
- `screenshots/02-sguil-alerts.png`
- `screenshots/03-kibana-alerts.png`
- `screenshots/04-alert-details.png`
- `screenshots/05-networkminer.png`

## TESDA Relevance

**Primary:** `01-monitoring-and-alerts/`

**Related:** `02-log-event-analysis/`, `03-network-traffic-analysis/`, `07-incident-investigation/`, `11-reporting/`

Strongest TESDA relevance: **ICT251312 — Monitor and Report Cyber Threats**.
