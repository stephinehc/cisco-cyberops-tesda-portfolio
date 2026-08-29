# Lab 24 — Hashing Things Out

**Cisco activity:** 21.1.6  
**Primary domain:** 05 Malware/IOC Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Hash a text file using OpenSSL.
2. Record the resulting digest.
3. Change the file and hash it again.
4. Compare the hashes.

**Answer / observation:** A cryptographic hash produces a fixed-length digest. A change to the input changes the resulting digest, demonstrating why hashes are useful for integrity checking and IOC identification.

## Evidence

**Figure 1 — Hash command/result:** `LAB-24-01-hash-result.png`  
> **Attach:** `screenshots/LAB-24-01-hash-result.png`

**Figure 2 — Hash comparison:** `LAB-24-02-hash-comparison.png`  
> **Attach:** `screenshots/LAB-24-02-hash-comparison.png`

## Interpretation
Hash comparison is directly applicable to malware and IOC analysis.
