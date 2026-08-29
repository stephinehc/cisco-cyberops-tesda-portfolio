# Findings Report — CyberOps Associate v1.0 Pushdo Investigation

## Executive Summary

A security investigation was conducted to determine malicious activity associated with the **Pushdo Trojan** in the CyberOps Associate v1.0 Security Onion environment.

The investigation identified an affected internal Windows host, correlated security alerts, determined the approximate infection timeframe, identified downloaded executable payloads, calculated file hashes, and used external threat intelligence to validate the malicious nature of the identified files.

## Affected Asset

| Item | Finding |
|---|---|
| Host IP | `192.168.1.96` |
| MAC | `00-15-C5-DE-C7-3B` |
| NIC Vendor | Dell Inc. |
| Operating context | Windows endpoint in the lab environment |

## Incident Timeframe

The principal Pushdo activity was observed on **27 June 2017**, approximately **13:38:34–13:44:32 UTC**.

The host infection activity is associated with approximately **13:38:32 UTC**.

## Attack Summary

The investigation indicates that the affected host interacted with malicious DNS/web infrastructure and became infected with the Pushdo downloader Trojan.

Pushdo then retrieved additional executable malware. The three files examined in the assessment were:

- `gerv.gun`
- `trow.exe`
- `wp.exe`

The files were investigated using SHA-256 hashes and external malware intelligence. The historical assessment results showed multiple detections for each sample.

## Key Indicators

### Host indicators

- `192.168.1.96`
- `00-15-C5-DE-C7-3B`

### Network indicators

- `208.67.222.222`
- `208.83.223.34`
- `198.1.85.250`
- `myip.opendns.com`

### File indicators

- `gerv.gun`
- `trow.exe`
- `wp.exe`

### Hash indicators

The actual SHA-256 values obtained during the learner's assessment should be inserted into `ioc-analysis.md` and supported by screenshots.

## Investigation Conclusion

The available evidence supports the conclusion that host `192.168.1.96` was compromised by Pushdo-related malicious activity. The attack involved suspicious DNS/network activity followed by downloader behavior and retrieval of additional executable malware.

The combination of Security Onion alerts, infected-host information, file analysis and threat-intelligence verification provides a coherent incident narrative.

## Recommended Response

For a real incident, the next steps would include:

1. Isolate the affected host.
2. Preserve relevant evidence.
3. Block confirmed malicious indicators where appropriate.
4. Identify and remove persistence/malware.
5. Reset affected credentials where required.
6. Restore the host from a known-good state if necessary.
7. Perform a secondary scan.
8. Validate that malicious communications no longer occur.
9. Continue heightened monitoring.
10. Document and close the incident according to organizational procedure.

**These response actions are recommendations for extending the lab. They were not performed as part of the original v1.0 Skills Assessment unless separately documented by the learner.**

## TESDA Evidence Mapping

| Evidence | Primary domain | TESDA relevance |
|---|---|---|
| Security alert review | Monitoring and Alerts | ICT251312 |
| Event correlation | Log/Event Analysis | ICT251312 / ICT251314 |
| Host/network investigation | Network + Endpoint Analysis | ICT251312 / ICT251314 |
| Malware/hash analysis | Malware/IOC Analysis | ICT251312 / ICT251314 |
| External verification | Threat Intelligence | ICT251312 / ICT251314 |
| Investigation narrative | Incident Investigation | ICT251312 / ICT251314 |
| Final findings | Reporting | ICT251312 |

## Evidence Status

- **Assessment performed:** Yes
- **Primary technical evidence:** Learner's actual CyberOps VM results
- **Screenshots:** To be attached manually
- **Containment:** Not demonstrated by the original assessment
- **Recovery:** Not demonstrated by the original assessment
- **Vulnerability management:** Not demonstrated by the original assessment

## Analyst Statement

> The investigation identified and analyzed malicious Pushdo-related activity affecting an internal endpoint. Security alerts were reviewed and correlated, the affected host was identified, malicious payloads were examined, and threat intelligence was used to support the malware determination. The investigation demonstrates alert-driven SOC analysis but requires supplementary practical evidence for full containment, eradication, recovery and vulnerability-management competencies.
