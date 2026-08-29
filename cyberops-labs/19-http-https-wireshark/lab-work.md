# Lab 19 — HTTP and HTTPS Traffic

**Cisco activity:** 10.6.7  
**Primary domain:** 03 Network Traffic Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Capture and inspect HTTP traffic.
2. Locate the HTTP POST request and inspect form data.
3. Capture and inspect HTTPS traffic.
4. Compare HTTP and HTTPS application visibility.

**Answer:** In the training HTTP capture, the POST form exposes the simulated `uid` and `passw` values. In HTTPS, the application data is protected by TLS and is not readable in plaintext.

**Observation:** HTTPS replaces the directly visible HTTP application content with encrypted TLS application data.

## Evidence

**Figure 1 — HTTP request:** `LAB-19-01-http-request.png`  
> **Attach:** `screenshots/LAB-19-01-http-request.png`

**Figure 2 — HTTP form data:** `LAB-19-02-http-form-data.png`  
> **Attach:** `screenshots/LAB-19-02-http-form-data.png`

**Figure 3 — HTTPS/TLS encrypted data:** `LAB-19-03-https-tls.png`  
> **Attach:** `screenshots/LAB-19-03-https-tls.png`

## Interpretation
Comparing plaintext HTTP with TLS-protected HTTPS demonstrates why encrypted transport reduces exposure of application data.
