# Lab 30 — Convert Data into a Universal Format

**Cisco activity:** 27.1.5  
**Primary domain:** 02 Log/Event Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Normalize timestamps in a log file.
2. Normalize timestamps in an Apache log.
3. Inspect Zeek logs in Security Onion.
4. Inspect Snort and other available logs.
5. Compare normalized fields.

**Answer / observation:** Security data from different sources can use different timestamp formats and structures. Normalization makes events easier to correlate and analyze consistently.

## Evidence

**Figure 1 — Normalized log:** `LAB-30-01-normalized-log.png`  
> **Attach:** `screenshots/LAB-30-01-normalized-log.png`

**Figure 2 — Security Onion logs:** `LAB-30-02-security-logs.png`  
> **Attach:** `screenshots/LAB-30-02-security-logs.png`

## Interpretation
Data normalization supports correlation across multiple security telemetry sources.
