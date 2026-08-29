# Threat Intelligence — CyberOps / CCNA Cybersecurity Operations v1.1

## Objective

Use external information and Security Onion telemetry to understand the exploit mechanism, validate the observed activity, and explain how the indicators relate to the attack.

## Exploit kit

**Angler Exploit Kit (Angler EK)** is the exploit framework identified by the Snort/Sguil events.

An exploit kit is a collection of server-side components used to profile visitors, identify client-side vulnerabilities, deliver an appropriate exploit, and provide a payload after successful exploitation.

## Observed attack logic

The assessment evidence is consistent with the following sequence:

1. A user reaches malicious or compromised web infrastructure.
2. The exploit infrastructure profiles the client environment.
3. The infrastructure identifies a suitable client-side vulnerability.
4. An exploit is selected and delivered.
5. Successful exploitation provides an opportunity to execute code.
6. A malware payload is delivered to the victim.

## Exploit-delivery infrastructure

The investigation identifies:

- **IP:** `192.99.198.158`
- **Domain:** `qwe.mvdunalterableairreport.net`

These indicators should be treated as malicious indicators within the context of this controlled assessment.

## Vulnerability context

The affected host is reported as using an outdated Flash component. The exploit kit is associated with attacks against client-side technologies such as Flash, Java and Silverlight.

## Intelligence questions answered

### What exploit kit is involved?

Angler EK.

### What is an exploit kit?

A server-side exploitation framework that profiles client systems, selects exploits based on detected weaknesses, delivers the exploit, and may subsequently deliver a payload.

### Why is the observed activity suspicious?

The activity combines an outdated client component, exploit-related Snort alerts, external exploit-delivery infrastructure, and a payload delivered through captured network traffic.

## Intelligence sources used during the assessment

- Sguil/Snort alert metadata
- ELSA records
- Bro/Zeek network records
- Wireshark packet evidence
- Web-based research on the exploit kit

## Analyst conclusion

The combined telemetry and external intelligence support classification of the observed activity as a malicious exploit-kit infection attempt involving Angler EK.

## TESDA relevance

This evidence supports:

- IOC enrichment
- threat identification
- attack-method analysis
- incident investigation
- intelligence-based validation

Primary evidence domains:

- 05 Malware/IOC Analysis
- 07 Incident Investigation
- 08 Threat Intelligence
