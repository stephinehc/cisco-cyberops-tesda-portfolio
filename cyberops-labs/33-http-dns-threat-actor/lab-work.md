# Lab 33 — Interpret HTTP and DNS Data to Isolate Threat Actor

**Cisco activity:** 27.2.12  
**Primary domain:** 07 Incident Investigation  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

### Part 1 — HTTP investigation
Identify the simulated SQL-injection activity and record the source/destination information.

**Answer:** Source IP `209.165.200.227`; destination IP `209.165.200.235`; destination port `80`. The first result in the training data occurs on June 12, 2020 at approximately 21:30:09.445 and uses the `bro_http` event type.

### Part 2 — DNS exfiltration
Investigate unusually long DNS subdomains.

**Answer:** DNS client `192.168.0.11`; DNS server `209.165.200.235`. The suspicious subdomains contain hexadecimal-encoded content.

### Decoded result
The training data decodes to:

`CONFIDENTIAL DOCUMENT`

`DO NOT SHARE`

`This document contains information about the last security breach.`

**Observation:** The pattern indicates coordinated DNS queries carrying hidden data. DNS can be abused for exfiltration because DNS traffic commonly leaves a network and may receive less scrutiny than other protocols.

## Evidence

**Figure 1 — HTTP investigation:** `LAB-33-01-http-investigation.png`  
> **Attach:** `screenshots/LAB-33-01-http-investigation.png`

**Figure 2 — DNS suspicious queries:** `LAB-33-02-dns-exfiltration.png`  
> **Attach:** `screenshots/LAB-33-02-dns-exfiltration.png`

**Figure 3 — Decoded content:** `LAB-33-03-decoded-content.png`  
> **Attach:** `screenshots/LAB-33-03-decoded-content.png`

## Interpretation
The activity demonstrates correlation of HTTP/DNS evidence to identify simulated threat activity and possible data exfiltration.
