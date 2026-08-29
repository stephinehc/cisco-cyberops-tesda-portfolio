# Findings Report — CyberOps / CCNA Cybersecurity Operations v1.1

## Executive summary

The investigation identified a sequence of exploit-related events affecting an internal Windows host. Sguil/Snort telemetry indicated activity associated with the **Angler Exploit Kit**. The affected host was identified as `192.168.0.12`, and the infrastructure associated with exploit delivery was identified as `192.99.198.158` and `qwe.mvdunalterableairreport.net`.

Packet-level analysis in Wireshark allowed the analyst to recover an object identified as `3xdz3bcxc8`, providing additional evidence that the network activity resulted in payload delivery.

## Key findings

| Finding | Result |
|---|---|
| Exploit kit | Angler EK |
| Affected host | `192.168.0.12` |
| Exploit-delivery IP | `192.99.198.158` |
| Exploit-delivery domain | `qwe.mvdunalterableairreport.net` |
| Extracted object | `3xdz3bcxc8` |
| Vulnerable client condition | Outdated Flash component |

## Investigation conclusion

The collected evidence supports the conclusion that the observed events represent malicious exploit-kit activity. The attack involved an external delivery infrastructure, exploitation of a vulnerable client component, and delivery of a payload to the affected host.

## Evidence chain

```text
Snort Detection
      ↓
Sguil Alert
      ↓
Exploit Identification
      ↓
Affected Host
      ↓
Exploit-Delivery IP / Domain
      ↓
ELSA / Bro-Zeek Correlation
      ↓
Wireshark Packet Analysis
      ↓
Payload Extraction
      ↓
Incident Finding
```

## Recommended response actions

The following are recommended for a subsequent mitigation exercise, not claimed as completed in this assessment:

1. Isolate the affected host.
2. Block the identified malicious IP/domain.
3. Preserve relevant evidence.
4. Identify and remove the delivered payload.
5. Correct the vulnerable client software condition.
6. Reset potentially exposed credentials where appropriate.
7. Perform a secondary scan.
8. Restore the host to a known-good state if required.
9. Monitor for recurrence.
10. Document the final remediation status.

## TESDA evidence mapping

### Strong evidence

**ICT251312 — Monitor and Report Cyber Threats**

- Alert evaluation
- Security-event investigation
- Case follow-up
- Threat identification
- Reporting

### Supporting evidence

**ICT251314 — Perform Threat Mitigation**

- Incident evaluation
- IOC identification
- Threat-intelligence use
- Affected-system analysis

### Not demonstrated by this assessment alone

- Full containment
- Eradication
- Recovery
- Secondary scanning after remediation
- Vulnerability-management lifecycle

These gaps will be addressed by the supplementary NC II simulations in later project phases.

## Final assessment statement

The v1.1 Skills Assessment demonstrates practical SOC investigation skills by requiring the analyst to move from an IDS alert to correlated network evidence, threat intelligence, exploit identification, and payload analysis. It therefore provides strong practical evidence for monitoring, investigation and threat-analysis capabilities.
