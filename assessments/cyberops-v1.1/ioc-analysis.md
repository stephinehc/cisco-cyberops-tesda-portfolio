# IOC Analysis — CyberOps / CCNA Cybersecurity Operations v1.1

## Objective

Identify the indicators associated with the exploit and malware-delivery activity and classify their role in the incident.

## IOC table

| IOC type | Indicator | Role / interpretation |
|---|---|---|
| Internal IP | `192.168.0.12` | Compromised/victim host |
| External IP | `192.99.198.158` | Exploit-delivery infrastructure |
| Domain | `qwe.mvdunalterableairreport.net` | Exploit/payload delivery domain |
| Extracted object | `3xdz3bcxc8` | Object recovered from captured traffic |
| Client condition | Outdated Flash component | Vulnerable software condition exploited by the kit |
| Exploit kit | Angler EK | Exploitation infrastructure/toolset |

## Targeted applications

The Angler exploit kit is associated with vulnerabilities in commonly targeted client applications including:

- Adobe Flash Player
- Java Runtime Environment
- Microsoft Silverlight

The observed host condition points to an outdated Flash component.

## Extracted payload

The assessment requires the analyst to pivot from Sguil into Wireshark and export the object delivered through the captured traffic.

**Recovered object:** `3xdz3bcxc8`

Document the following from the actual assessment:

- File type: __________________
- File size: __________________
- SHA-256: __________________
- Detection result: __________________

## IOC validation

Where practical, validate extracted indicators using the assessment's available evidence and trusted threat-intelligence sources. Preserve screenshots showing the exact values checked.

## IOC handling recommendations

For a subsequent mitigation exercise, these indicators can be used to demonstrate:

- malicious-domain blocking
- IP blocking
- network isolation
- endpoint investigation
- malware removal
- post-remediation verification

These actions are **not claimed as completed by this assessment** unless supported by separate evidence.

## TESDA relevance

Primary evidence domains:

- 03 Network Traffic Analysis
- 05 Malware/IOC Analysis
- 07 Incident Investigation
- 08 Threat Intelligence

Strong supporting competency:

**ICT251314 — Perform Threat Mitigation**
