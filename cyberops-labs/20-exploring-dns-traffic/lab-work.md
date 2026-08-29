# Lab 20 — Exploring DNS Traffic

**Cisco activity:** 17.1.7  
**Primary domain:** 03 Network Traffic Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Capture DNS traffic.
2. Filter DNS packets.
3. Examine query fields and source/destination information.
4. Examine response fields and answer records.

**Answer / observation:** DNS traffic can be filtered with `udp.port == 53`. A DNS query identifies the requested name; the corresponding response contains the returned records. Query and response addressing/ports reverse direction.

## Evidence

**Figure 1 — DNS query:** `LAB-20-01-dns-query.png`  
> **Attach:** `screenshots/LAB-20-01-dns-query.png`

**Figure 2 — DNS response:** `LAB-20-02-dns-response.png`  
> **Attach:** `screenshots/LAB-20-02-dns-response.png`

## Interpretation
DNS visibility supports threat hunting for unusual domains, query patterns and response behavior.
