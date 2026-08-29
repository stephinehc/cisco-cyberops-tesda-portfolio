# Lab 36 — Investigating an Attack on a Windows Host

**Cisco activity:** 27.2.16  
**Primary domain:** 07 Incident Investigation  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

### Part 1 — Sguil investigation
Locate the simulated alerts for the assigned date and review the transcript.

**Answer:** In the training scenario, the source is `10.0.90.215:49204` and the destination is `209.141.34.8:80`. The request is `GET /test1.exe`. The downloaded file begins with the `MZ` signature, indicating a Windows executable format such as `.exe` or `.dll`.

### Part 2 — Kibana investigation
Narrow the time range and correlate the alerts associated with the affected Windows training host.

**Observation:** Sguil and Kibana provide complementary alert/event views for reconstructing the simulated attack timeline.

### Part 3 — File and IOC analysis
Export the simulated executable from the HTTP traffic and calculate its SHA-256 hash.

**Observation:** The resulting hash provides a stable identifier for subsequent IOC/threat-intelligence checks.

## Evidence

**Figure 1 — Initial Sguil alert:** `LAB-36-01-sguil-alert.png`  
> **Attach:** `screenshots/LAB-36-01-sguil-alert.png`

**Figure 2 — HTTP request/file:** `LAB-36-02-http-file.png`  
> **Attach:** `screenshots/LAB-36-02-http-file.png`

**Figure 3 — Windows executable signature:** `LAB-36-03-mz-signature.png`  
> **Attach:** `screenshots/LAB-36-03-mz-signature.png`

**Figure 4 — Kibana correlation:** `LAB-36-04-kibana-correlation.png`  
> **Attach:** `screenshots/LAB-36-04-kibana-correlation.png`

**Figure 5 — SHA-256 result:** `LAB-36-05-sha256.png`  
> **Attach:** `screenshots/LAB-36-05-sha256.png`

## Interpretation
This integrated simulated investigation strongly supports incident investigation, endpoint analysis, malware/IOC analysis and reporting. It does not by itself demonstrate live containment, eradication or recovery.
