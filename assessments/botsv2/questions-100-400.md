# BOTS v2 Investigation Questions — 100–400 Series

## Purpose

This file provides a complete question index for the BOTS v2 investigation used in this portfolio. The questions are **paraphrased from the supplied Splunk 2 walkthrough** rather than reproduced verbatim. The accompanying answers, SPL, and evidence screenshots are documented in the investigation report and screenshot index.

> **Environment notice:** BOTS v2 activities documented in this portfolio are performed only in a simulated, isolated, and controlled laboratory environment using authorized training data. They are not documentation of activity against a live production environment.

## 100 Series — Amber Turing

1. What website domain did Amber Turing visit while researching the executive team of a potential competitor?
2. What image file on that competitor's website displayed the executive contact information?
3. What are the CEO's first and last names?
4. What email address belongs to the CEO?
5. After contacting the CEO, what email address belongs to the other competitor employee Amber contacted?
6. What filename was attached to Amber's email to that competitor contact?
7. What personal email address for Amber can be recovered from the encoded portion of the email?

## 200 Series — Web Activity, Vulnerability Scanning and XSS

1. Which version of the TOR Browser did Amber install to hide or obfuscate her web browsing?
2. What public IPv4 address hosts `www.brewertalk.com`?
3. What IP address was responsible for the web vulnerability-scanning activity against `www.brewertalk.com`?
4. Which URI path was most heavily targeted by the attacker identified in the previous investigation?
5. Which SQL function was abused in the requests targeting that URI?
6. What numeric cookie value was transmitted from Kevin's browser to the malicious URL during the XSS activity?
7. What username was created on `brewertalk.com` as a result of the malicious activity?

## 300 Series — Ransomware, USB and Malware

1. After ransomware encrypted Mallory's critical PowerPoint presentation, what was the resulting encrypted filename?
2. Which season and episode corresponds to the encrypted Game of Thrones movie file found on Mallory's system?
3. Which vendor manufactured the USB device that Kevin likely used to transfer malware to Mallory's MacBook?
4. What programming language is represented in at least part of the malware identified in the previous investigation?
5. On what date was that malware first observed in the wild?
6. What is the first FQDN, in alphabetical order, among the dynamic-DNS destinations used by the malware to communicate with its C2 infrastructure?
7. What is the second FQDN, in alphabetical order, among those contacted C2 destinations?

## 400 Series — Taedonggang APT, Malware and Persistence

1. What ZIP attachment name was sent to Frothly as part of the simulated Taedonggang spearphishing activity?
2. What password was supplied to open that ZIP archive?
3. What exact SSL Issuer value appears most consistently in the attacker's encrypted traffic?
4. What unusual filename, inappropriate for the simulated American-company context, was downloaded through the FTP activity associated with `winsys32.dll`?
5. What first and last name appears in the metadata of the file associated with execution of PowerShell Empire on the first simulated victim workstation?
6. What text is identified inside the document during the document-analysis stage?
7. Which single webpage is contacted most often by the scheduled tasks configured to maintain persistence and beacon to the simulated C2 server?

## Evidence and investigation relationship

Each question should be treated as an investigation objective, not merely an answer-retrieval exercise:

```text
Question
   ↓
SPL / investigation action
   ↓
Simulated event or external analysis result
   ↓
Relevant field / raw content
   ↓
Finding
   ↓
Evidence screenshot
   ↓
TESDA evidence-domain mapping
```

## Answer cross-reference

The corresponding findings and SPL commands are documented in:

- `reports/botsv2-investigation-report.md`
- `screenshots/README.md`
- `evidence-mapping.md`

The screenshot index currently contains **42 uploaded evidence images** across the four series. Multiple images are retained for questions where the investigation requires an initial SPL result, expanded fields/raw event content, and/or an external analysis result.

## Source handling

The supplied Medium walkthrough was used to cross-check the question sequence, investigative approach, and SPL commands. The wording in this file is intentionally paraphrased. SPL commands in the investigation report are retained as required for the technical evidence record.
