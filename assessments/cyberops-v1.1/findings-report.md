# Findings Report — CCNA Cybersecurity Operations v1.1

## Executive summary

The assessment investigated a multi-stage exploit observed in Security Onion. Sguil/Snort alerts identified activity consistent with the **Angler Exploit Kit** and an outdated Flash component on the internal host `192.168.0.12`.

The investigation then correlated the victim with exploit-delivery infrastructure, identified a landing-page stage, and used Wireshark to recover the delivered object `3xdz3bcxc8`.

## Consolidated findings

| Item | Finding |
|---|---|
| Exploit kit | Angler EK |
| Exploit-related events | 15 |
| Activity window | 2017-09-07 15:31:12–15:31:34 |
| Internal victim | `192.168.0.12` |
| MAC address | `00:1b:21:ca:fe:d7` |
| Vulnerable component | Outdated Flash |
| Landing-page IP | `173.201.198.128` |
| Landing-page domain | `lifeinsidetroit.com` |
| Exploit-delivery IP | `192.99.198.158` |
| Exploit-delivery domain | `qwe.mvdunalterableairreport.net` |
| Recovered object | `3xdz3bcxc8` |
| Recovered object type | SWF |

## Evidence chain

```text
Snort / Sguil Detection
        ↓
Exploit Event Group
        ↓
Victim Identification
        ↓
Angler EK Identification
        ↓
Exploit-Source Correlation
        ↓
ELSA / Bro-Zeek Investigation
        ↓
Landing-Page Identification
        ↓
Exploit Delivery Infrastructure
        ↓
Wireshark Packet Analysis
        ↓
SWF Object Extraction
        ↓
Final Assessment Finding
```

## Analyst conclusion

The correlated evidence supports classification of the activity as a malicious exploit-kit attack against the internal host. The investigation demonstrates how an analyst can move from an IDS alert to host identification, exploit research, infrastructure tracing and payload extraction.

## Recommended follow-up

The following actions are **not claimed as performed in this assessment**. They belong to the later mitigation phase:

1. Isolate the affected host.
2. Block malicious infrastructure.
3. Preserve forensic evidence.
4. Remove the malicious payload.
5. Correct the vulnerable software condition.
6. Perform a secondary scan.
7. Restore the host if required.
8. Monitor for recurrence.
9. Document remediation.

## TESDA evidence mapping

### Strongest evidence

**ICT251312 — Monitor and Report Cyber Threats**

- Evaluate security alerts.
- Investigate suspicious events.
- Correlate network-security information.
- Identify the affected asset.
- Research the threat/exploit.
- Document findings.

### Supporting evidence

**ICT251314 — Perform Threat Mitigation**

- Identify the threat.
- Identify affected assets.
- Identify relevant IOCs and infrastructure.
- Analyze the attack method.

### Not demonstrated by v1.1 alone

- Containment
- Eradication
- Recovery
- Secondary scanning after remediation
- Full vulnerability-management lifecycle

## Portfolio evidence domains

- `01-monitoring-and-alerts/`
- `02-log-event-analysis/`
- `03-network-traffic-analysis/`
- `04-endpoint-analysis/`
- `05-malware-ioc-analysis/`
- `07-incident-investigation/`
- `08-threat-intelligence/`
- `11-reporting/`

## Evidence integrity

The assessment results recorded here are intended to document the learner's practical assessment. Screenshots and exported evidence will be attached manually. The external answer reference is not included as a portfolio citation.
