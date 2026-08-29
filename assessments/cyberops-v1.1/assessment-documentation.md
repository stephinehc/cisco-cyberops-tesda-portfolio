# CyberOps / CCNA Cybersecurity Operations v1.1 Skills Assessment — Documentation

## 1. Environment

The assessment is performed in the Cisco Cybersecurity Operations virtual environment using the Security Onion VM.

### Primary tools

| Tool | Purpose |
|---|---|
| Security Onion | Network Security Monitoring environment |
| Sguil | Alert/event investigation and pivot point |
| Snort | Intrusion-detection event generation |
| ELSA | Log and event searching |
| Bro/Zeek | Network metadata and protocol evidence |
| Wireshark | Packet-level investigation and file extraction |
| Web search | Exploit and threat-intelligence research |

## 2. Initial verification

1. Log into the Security Onion VM using the assessment account.
2. Open a terminal.
3. Verify that the Network Security Monitoring services are operational.
4. Open Sguil.
5. Monitor the available networks.
6. Review the event list and identify the group of events associated with the suspected exploit.

### Screenshot

Add the initial Security Onion/Sguil screenshot here.

`![Security Onion and Sguil](screenshots/01-sguil-overview.png)`

## 3. Investigation procedure

The assessment is divided into four investigation stages.

### Part 1 — Gathering basic information

The analyst identifies the exploit-related events in Sguil and establishes the set of network addresses associated with the activity.

### Part 2 — Learning about the exploit

The Snort alert identifies the exploit kit as **Angler EK**. The analyst researches the exploit kit and determines how the observed events fit the general exploit-kit lifecycle.

The investigation identifies the typical sequence as:

1. A high-traffic or compromised website is used as an entry point.
2. Malicious code profiles the visiting system.
3. Browser/plugin and operating-system information is collected.
4. The exploit server selects an appropriate exploit.
5. The exploit is delivered to the browser.
6. A payload is delivered after successful exploitation.

### Part 3 — Determining the source of the malware

The analyst records the IP addresses appearing in the related Sguil events, identifies the affected host, and pivots from the alert to supporting network records.

The compromised internal host is identified as `192.168.0.12`.

The infrastructure identified as delivering the exploit is `192.99.198.158`, associated with the domain:

`qwe.mvdunalterableairreport.net`

The affected host is identified as using an outdated Flash component, which is consistent with the exploit-kit activity observed in the event sequence.

### Part 4 — Analyzing the exploit

The analyst pivots from Sguil into packet-level evidence using Wireshark. Captured traffic is examined and the delivered object is exported for further analysis.

The extracted file is documented as:

`3xdz3bcxc8`

## 4. Evidence to capture

- Security Onion service-status output
- Sguil overview
- Exploit-related Sguil alerts
- IP-address evidence
- Host identification evidence
- ELSA/Bro-Zeek supporting records
- Wireshark packet evidence
- Exported-file evidence
- Final investigation notes

## 5. Evidence integrity

The portfolio should contain screenshots and outputs generated during the learner's own assessment run. Published answer material is used only as a cross-check during documentation preparation and is not presented as personal assessment evidence.
