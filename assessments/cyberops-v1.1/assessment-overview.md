# CyberOps / CCNA Cybersecurity Operations v1.1 Skills Assessment — Overview

## Assessment purpose

This assessment places the learner in the role of a security analyst investigating suspicious activity displayed in the **Sguil** dashboard. The objective is to determine whether the observed events represent malicious activity, investigate the associated exploit, identify the source of the malware delivery, and analyze the delivered payload.

The assessment uses the **Security Onion** virtual machine and its network-security-monitoring tools. Security Onion is the system with Internet access in the assessment environment and is used to access Sguil and related investigation tools.

## Skills demonstrated

The assessment demonstrates the ability to:

- Evaluate Snort/Sguil security events.
- Use Sguil as the starting point for investigation pivots.
- Use ELSA, Bro/Zeek and Wireshark to inspect related evidence.
- Research a suspected exploit using open-source information.
- Identify the exploit kit involved in the attack.
- Determine the source and delivery infrastructure of the exploit.
- Identify the compromised host and relevant network indicators.
- Extract a malicious file from captured network traffic.
- Correlate network-security events to determine the attack sequence.

## Assessment scenario

The analyst observes a collection of events in Sguil associated with an exploit. The investigation focuses on an **Angler exploit kit** activity affecting a host with an outdated Flash component. The exploit infrastructure uses a malicious delivery domain and ultimately provides a malware payload to the victim.

## Assessment workflow

```text
Security Onion
      ↓
Verify NSM services
      ↓
Sguil alert review
      ↓
Identify exploit-related events
      ↓
Research exploit kit
      ↓
Identify affected host
      ↓
Trace exploit-delivery source
      ↓
Pivot to ELSA / Bro-Zeek / Wireshark
      ↓
Extract payload evidence
      ↓
Analyze attack sequence
      ↓
Document findings
```

## Evidence domains

Primary domains:

- `01-monitoring-and-alerts/`
- `02-log-event-analysis/`
- `03-network-traffic-analysis/`
- `04-endpoint-analysis/`
- `07-incident-investigation/`
- `08-threat-intelligence/`
- `11-reporting/`

## TESDA relevance

The assessment provides strong supporting evidence for:

- **ICT251312 — Monitor and Report Cyber Threats**
- **ICT251314 — Perform Threat Mitigation**

The assessment does not, by itself, demonstrate complete containment, eradication, recovery, secondary scanning, or vulnerability-management processes. Those requirements will be addressed through supplementary practical activities.

## Evidence status

The learner has performed the assessment. Actual screenshots and captured outputs are to be placed in the `screenshots/` directory and referenced by the related documentation files.
