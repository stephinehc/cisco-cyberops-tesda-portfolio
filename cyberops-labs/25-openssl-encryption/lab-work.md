# Lab 25 — Encrypting and Decrypting Data Using OpenSSL

**Cisco activity:** 21.2.10  
**Primary domain:** 05 Malware/IOC Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Create a sample text file.
2. Encrypt it using the assigned OpenSSL method.
3. Decrypt the ciphertext.
4. Verify that the recovered plaintext matches the original.

**Answer / observation:** OpenSSL can encrypt and decrypt the sample file using AES. The recovered plaintext should match the original when the correct decryption material is supplied.

**Security observation:** The demonstration method is instructional and should not be treated as a modern production data-protection design without appropriate key derivation and integrity controls.

## Evidence

**Figure 1 — OpenSSL encryption:** `LAB-25-01-openssl-encryption.png`  
> **Attach:** `screenshots/LAB-25-01-openssl-encryption.png`

**Figure 2 — OpenSSL decryption:** `LAB-25-02-openssl-decryption.png`  
> **Attach:** `screenshots/LAB-25-02-openssl-decryption.png`

## Interpretation
Cryptographic analysis helps analysts understand protected data and security controls.
