# Lab 17 — UDP DNS Capture

**Cisco activity:** 10.2.7  
**Primary domain:** 03 Network Traffic Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Record the laboratory host IP configuration.
2. Capture DNS traffic with Wireshark.
3. Filter for DNS/UDP traffic.
4. Inspect a DNS query and response.
5. Identify MAC/IP addresses, ports, query name and response records.

**Answer / observation:** DNS queries use UDP port 53 in the standard laboratory exchange. The response reverses the source/destination addressing relationship from the query, and DNS response records should correspond to the queried name.

## Evidence

**Figure 1 — IP configuration:** `LAB-17-01-ip-config.png`  
> **Attach:** `screenshots/LAB-17-01-ip-config.png`

**Figure 2 — DNS query:** `LAB-17-02-dns-query.png`  
> **Attach:** `screenshots/LAB-17-02-dns-query.png`

**Figure 3 — DNS response:** `LAB-17-03-dns-response.png`  
> **Attach:** `screenshots/LAB-17-03-dns-response.png`

## Interpretation
DNS packet analysis supports network monitoring, investigation and detection of unusual DNS behavior.
