# Lab 28 — Certificate Authority Stores

**Cisco activity:** 21.4.7  
**Primary domain:** 04 Endpoint Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Display trusted root certificates in the browser.
2. Compare browser CA stores.
3. Obtain the correct training certificate fingerprint.
4. Compare it with the fingerprint presented by the laboratory VM.
5. Determine whether the fingerprints match.

**Answer / observation:** A matching certificate fingerprint indicates that the observed certificate matches the expected training certificate. A mismatch would warrant investigation for interception or certificate substitution.

## Evidence

**Figure 1 — Browser CA store:** `LAB-28-01-ca-store.png`  
> **Attach:** `screenshots/LAB-28-01-ca-store.png`

**Figure 2 — Certificate fingerprint comparison:** `LAB-28-02-certificate-fingerprint.png`  
> **Attach:** `screenshots/LAB-28-02-certificate-fingerprint.png`

## Interpretation
Certificate and fingerprint verification supports endpoint and network-security investigation.
