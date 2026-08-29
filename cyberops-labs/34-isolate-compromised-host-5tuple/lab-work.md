# Lab 34 — Isolate Compromised Host Using 5-Tuple

**Cisco activity:** 27.2.14  
**Primary domain:** 07 Incident Investigation  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Review the simulated alerts in Sguil.
2. Pivot to Wireshark.
3. Use the 5-tuple to identify the relevant communication.
4. Pivot to Kibana and correlate the event.
5. Identify the compromised training host and associated file.

**Answer / observation:** The 5-tuple consists of source IP, source port, destination IP, destination port and protocol. Correlating these fields across Sguil, Wireshark and Kibana helps identify the compromised host and the associated simulated file/activity.

## Evidence

**Figure 1 — Sguil alert:** `LAB-34-01-sguil-alert.png`  
> **Attach:** `screenshots/LAB-34-01-sguil-alert.png`

**Figure 2 — 5-tuple in Wireshark:** `LAB-34-02-five-tuple.png`  
> **Attach:** `screenshots/LAB-34-02-five-tuple.png`

**Figure 3 — Kibana correlation:** `LAB-34-03-kibana-correlation.png`  
> **Attach:** `screenshots/LAB-34-03-kibana-correlation.png`

## Interpretation
This lab demonstrates compromised-host identification and multi-source event correlation. It does not represent isolation of a live production endpoint.
