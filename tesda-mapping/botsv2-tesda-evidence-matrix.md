# BOTS v2 → TESDA Evidence Matrix

## Purpose

This document maps the completed BOTS v2 / Splunk investigation evidence to the TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II core competencies. It uses the candidate's uploaded screenshots as the evidence artifacts and the BOTS v2 investigation questions/SPL as the technical activity record.

This is an **RPL evidence-planning matrix**, not a TESDA competency determination. Final assessment decisions belong to the authorized TESDA assessor.

## Evidence source

The BOTS v2 investigation covers four question series:

- 100 Series — Amber Turing / email and web investigation
- 200 Series — TOR, DNS, web scanning, SQL injection and XSS
- 300 Series — ransomware, USB, malware and C2 analysis
- 400 Series — spearphishing, encrypted traffic, FTP malware delivery and persistence

The repository currently contains **42 uploaded screenshots** across the four series.

---

# 1. 100 Series — Amber Turing Investigation

### Primary TESDA relevance

**ICT251312 — Monitor and Report Cyber Threats**

| Question | Evidence / finding | Evidence domain | TESDA link | Coverage |
|---|---|---|---|---|
| 100-Q1 | Identified Amber's IP from PAN traffic, pivoted to HTTP traffic and identified `www.berkbeer.com` | 01, 02, 03, 07 | ICT251312 Elements 1, 3, 4 | 🟢 Supporting/Direct |
| 100-Q2 | Identified `/images/ceoberk.png` from competitor HTTP traffic | 03, 07 | ICT251312 Element 4 — manual verification/case follow-up | 🟢 |
| 100-Q3 | Identified CEO Martin Berk through SMTP traffic and raw email content | 02, 07 | ICT251312 Element 3 — manual checking and verification | 🟢 |
| 100-Q4 | Identified `mberk@berkbeer.com` from SMTP evidence | 02, 07 | ICT251312 Element 4 — case follow-up | 🟢 |
| 100-Q5 | Identified `hbernhard@berkbeer.com` through SMTP event analysis | 02, 07 | ICT251312 Element 4 | 🟢 |
| 100-Q6 | Identified `Saccharomyces_cerevisiae_patent.docx` from `attach_filename` | 02, 05, 07 | ICT251312 manual verification and threat identification | 🟢 |
| 100-Q7 | Extracted Amber's personal email from Base64 content after decoding | 02, 05, 07, 08 | ICT251312 manual verification/case follow-up | 🟢 |

### Evidence interpretation

The 100 Series demonstrates a repeatable investigation path: identify an actor/host, pivot between network and application evidence, inspect event fields, inspect raw email content, and decode embedded content. It is particularly useful for demonstrating analytical and manual-verification capability.

**Important gap:** the BOTS questions themselves do not establish company SOP use, ticket issuance, stakeholder notification, or escalation. Those process artifacts must be added separately before claiming complete coverage of ICT251312 criteria 1.1–1.5 and 1.4–1.5 reporting requirements.

---

# 2. 200 Series — Web, Vulnerability Scanning and XSS

### Primary TESDA relevance

**ICT251313 — Conduct Vulnerability Scanning of Assets** and **ICT251314 — Perform Threat Mitigation**

| Question | Evidence / finding | Evidence domain | TESDA link | Coverage |
|---|---|---|---|---|
| 200-Q1 | Identified TOR Browser version 7.0.4 installed by Amber | 04, 07 | ICT251312/314 endpoint and incident analysis | 🟢 Supporting |
| 200-Q2 | Identified public server IP `52.42.208.228` and private IP `172.31.4.249` | 03, 07 | ICT251313 asset/network identification; ICT251314 incident scope | 🟢 Supporting |
| 200-Q3 | Identified `45.77.65.211` as the likely vulnerability-scanning source | 03, 06, 07 | ICT251313 Element 2 — scanning activity analysis | 🟢 Supporting |
| 200-Q4 | Identified `/member.php` as the heavily targeted URI | 03, 07 | ICT251313 analysis/reporting support; ICT251314 incident analysis | 🟢 Supporting |
| 200-Q5 | Identified `updatexml` as the abused SQL function | 03, 05, 07 | ICT251314 incident analysis / malicious behavior | 🟢 |
| 200-Q6 | Extracted cookie value `1502408189` from XSS activity | 03, 05, 07 | ICT251314 IOC/incident analysis | 🟢 |
| 200-Q7 | Identified maliciously created username `kIagerfield` and related password evidence | 03, 04, 07 | ICT251314 incident analysis and affected-account investigation | 🟢 |

### ICT251313 limitation

The 200 Series demonstrates analysis of scanning-related traffic, but **does not by itself prove the complete TESDA vulnerability-scanning workflow**. It does not show supervisor consultation, scanning calendar access, signed scope of work, asset prioritization, NIST 800-115 execution controls, resource monitoring, failed-scan handling, or a formal scan report. Those require a dedicated vulnerability-scanning practical.

---

# 3. 300 Series — Ransomware, USB and Malware Investigation

### Primary TESDA relevance

**ICT251314 — Perform Threat Mitigation**, especially incident analysis, CTI/IOC analysis and affected-system analysis.

| Question | Evidence / finding | Evidence domain | TESDA link | Coverage |
|---|---|---|---|---|
| 300-Q1 | Identified Mallory's host and encrypted PowerPoint file `Frothly_marketing_campaign_Q317.pptx.crypt_` | 04, 05, 07 | ICT251314 Elements 1 and 3 | 🟢 |
| 300-Q2 | Identified encrypted Game of Thrones file as S07E02 | 04, 05, 07 | ICT251314 affected-system/malware analysis | 🟢 |
| 300-Q3 | Correlated USB activity and vendor information to identify Alcor Micro Corp. | 04, 07, 08 | ICT251314 incident scope and CTI support | 🟢/🟡 |
| 300-Q4 | Correlated username/file event/MD5 and VirusTotal analysis to identify Perl malware | 04, 05, 08, 07 | ICT251314 Elements 1–3 | 🟢 |
| 300-Q5 | Identified first-seen date `2017-01-17` | 05, 08 | ICT251314 Element 2 — threat intelligence | 🟢 |
| 300-Q6 | Identified first C2 FQDN `eidk.duckdns.org` | 05, 08, 07 | ICT251314 Element 2 — TTP/IOC analysis | 🟢 |
| 300-Q7 | Identified second C2 FQDN `eidk.hopto.org` | 05, 08, 07 | ICT251314 Element 2 — TTP/IOC analysis | 🟢 |

### Evidence limitation

The reference includes a separate external vendor-ID lookup for Q3. The current uploaded evidence set contains the Splunk USB query/raw event but no separate vendor-lookup screenshot. This is recorded as a **supporting evidence gap**, not as a fabricated artifact.

The 300 Series strongly supports IOC enrichment and threat-intelligence analysis, but it does not demonstrate containment, eradication, recovery, or secondary scanning.

---

# 4. 400 Series — Taedonggang APT, Malware and Persistence

### Primary TESDA relevance

**ICT251314 — Perform Threat Mitigation**, particularly CTI, malware analysis, attack-path analysis and persistence investigation.

| Question | Evidence / finding | Evidence domain | TESDA link | Coverage |
|---|---|---|---|---|
| 400-Q1 | Identified spearphishing attachment `invoice.zip` | 02, 05, 07, 08 | ICT251314 incident/IOC/CTI analysis | 🟢 |
| 400-Q2 | Identified ZIP password `912345678` from raw email evidence | 02, 07 | ICT251314 incident analysis | 🟢 |
| 400-Q3 | Identified SSL issuer `C = US` for the attacker's traffic | 03, 07, 08 | ICT251314 network/CTI analysis | 🟢 |
| 400-Q4 | Identified unusual `.hwp` file delivered through FTP | 03, 05, 07 | ICT251314 malware and delivery analysis | 🟢 |
| 400-Q5 | Used Hybrid Analysis to identify Ryan Kovar in file metadata | 05, 08 | ICT251314 Element 2 — threat intelligence | 🟢 |
| 400-Q6 | Identified `CyberEastEgg` in document analysis | 05, 08 | ICT251314 CTI/malware analysis | 🟢 |
| 400-Q7 | Correlated scheduled-task creation, registry data and UTF-16 decoding to identify `process.php` as the C2 webpage | 02, 04, 05, 07, 08 | ICT251314 Elements 1–3; persistence/TTP analysis | 🟢 |

### Evidence interpretation

The 400 Series demonstrates multi-source correlation: email → network traffic → FTP → external malware/document analysis → Windows scheduled tasks → registry data → decoded C2 URI. This is strong evidence for investigative reasoning and CTI enrichment.

It still does not demonstrate the operational response steps required by ICT251314 Element 4.

---

# 5. ICT251312 — Monitor and Report Cyber Threats

TESDA's current TR identifies five alert-monitoring/reporting areas: receiving/handling detection alerts and incident reports, checking red flags, assessing alerts against criteria, confirming detections/ticketing, checking security-solution status, manual verification, case follow-up, and reporting threat activity. citeturn4view0turn4view1

### BOTS v2 contribution

**Strong supporting evidence:**

- repeated manual log/event analysis;
- network and application pivots;
- host/user identification;
- IOC extraction;
- threat-intelligence enrichment;
- correlation across multiple data sources;
- investigation findings suitable for reporting.

**Still required for complete criterion-level evidence:**

- SOP-based alert receipt/triage artifact;
- incident/ticket record;
- explicit severity/priority decision;
- stakeholder notification/escalation;
- formal alert report.

The BOTS v2 evidence therefore supports ICT251312 strongly but should not be represented as independently proving every workplace-process criterion.

---

# 6. ICT251313 — Conduct Vulnerability Scanning of Assets

TESDA requires schedule checking, identification of assets, signed scope, verification with supervisor/change manager, adherence to schedule, scanning using industry standards including NIST SP 800-115, resource monitoring, handling scan problems, and reporting failed/results. citeturn4view1

### BOTS v2 contribution

The 200 Series provides **supporting evidence** for recognizing vulnerability-scanning activity and analyzing its source/target behavior.

It does **not** replace the dedicated scanning practical. The portfolio should still create:

1. authorization/scope document;
2. scan calendar/schedule;
3. asset list and prioritization;
4. scanner configuration;
5. scan execution evidence;
6. resource-monitoring evidence;
7. failed-scan handling record;
8. formal vulnerability scan report.

---

# 7. ICT251314 — Perform Threat Mitigation

TESDA's current TR requires incident validation/classification/criticality, use of CTI to identify TTPs, analysis of affected systems, and implementation of containment/recovery strategies. citeturn4view2

The BOTS v2 evidence strongly supports the **investigation and intelligence** portions:

- incident/event validation;
- affected host and user identification;
- malware and IOC analysis;
- C2 identification;
- threat-intelligence enrichment;
- persistence analysis;
- attack-path reconstruction.

### Critical remaining gap

TESDA's mitigation evidence specifically includes continuous monitoring for malicious IOCs, recovery from a last-known-good image/configuration/backup, rollback where applicable, removal of malicious IOCs/files/registry entries, and a secondary scan to verify that malicious elements remain absent. citeturn4view3

Therefore:

| Threat-mitigation area | BOTS v2 |
|---|---|
| Incident validation | 🟢 |
| Incident analysis/classification | 🟢/🟡 |
| CTI/TTP analysis | 🟢 |
| Affected-system analysis | 🟢 |
| IOC enrichment | 🟢 |
| Containment | 🔴 Gap |
| Eradication/removal | 🔴 Gap |
| Recovery/rollback | 🔴 Gap |
| Secondary scan | 🔴 Gap |
| Post-recovery monitoring | 🟡 Needs supplementary evidence |
| Final mitigation report | 🟡 Can be completed through portfolio reporting |

This confirms the need for the planned dedicated containment/recovery practical.

---

# 8. ICT251315 — Perform Vulnerability Management/Control

TESDA's current TR covers vulnerability-management software/agent installation, asset inventory/control, scan scheduling, audits of servers/endpoints/applications, change management, and patch/remediation testing/reporting. citeturn4view3

BOTS v2 does not provide complete evidence for this unit. Its 200 Series can support identification and analysis of a web vulnerability/scanning activity, but the portfolio still requires a dedicated VM/control workflow.

### Required supplementary evidence

```text
Asset inventory
      ↓
Asset classification/prioritization
      ↓
Authorized scan scope
      ↓
Scan schedule
      ↓
Vulnerability scan
      ↓
Finding/risk analysis
      ↓
Change request
      ↓
Remediation/patch
      ↓
Rescan
      ↓
Validation
      ↓
Vulnerability-management report
```

---

# 9. BOTS v2 → 11 Evidence Domains

| Evidence domain | BOTS v2 contribution |
|---|---|
| **01 Monitoring and Alerts** | 🟡 Supporting — BOTS is primarily a hunting/investigation dataset rather than a workplace alert-ticket workflow |
| **02 Log/Event Analysis** | 🟢 Strong — SMTP, DNS, HTTP, FTP, Windows and other event analysis |
| **03 Network Traffic Analysis** | 🟢 Strong — PAN/HTTP/DNS/FTP/SSL traffic pivots |
| **04 Endpoint Analysis** | 🟢 Strong — hosts, users, files, USB, scheduled tasks |
| **05 Malware/IOC Analysis** | 🟢 Strong — hashes, malware files, C2 domains, decoded content |
| **06 Vulnerability Scanning** | 🟡 Supporting — web scanning activity is investigated, but BOTS is not a complete scanner workflow |
| **07 Incident Investigation** | 🟢 Strong — multi-stage investigations and correlation |
| **08 Threat Intelligence** | 🟢 Strong — VirusTotal, Hybrid Analysis, external enrichment and TTP interpretation |
| **09 Containment** | 🔴 Gap — no actual containment action is performed |
| **10 Recovery** | 🔴 Gap — no recovery/rollback is performed |
| **11 Reporting** | 🟡 Supporting — findings are documented; formal stakeholder reporting artifact still needs to be produced |

---

# 10. Overall RPL interpretation

BOTS v2 should be presented as a **major supporting practical evidence source**, not as proof of the entire Cyber Threat Monitoring NC I / Cyber Threat Mitigation NC II qualification.

Its strongest value is demonstrating the candidate's ability to:

- interrogate security telemetry;
- construct and refine SPL searches;
- pivot between data sources;
- identify affected hosts/users;
- analyze malicious behavior;
- extract and enrich IOCs;
- use external threat-intelligence sources;
- reconstruct attack activity;
- document defensible findings.

The evidence gaps are operational rather than investigative:

**containment → eradication → recovery → secondary validation** and the **formal vulnerability-management lifecycle** remain separate practical activities.

## Recommended evidence sequence

```text
CyberOps Associate Labs
        ↓
CyberOps v1.0 Skills Assessment
        ↓
BOTS v2 SIEM / Threat Hunting Evidence
        ↓
Containment + Eradication + Recovery Practical
        ↓
Vulnerability Scanning Practical
        ↓
Vulnerability Management / Remediation Practical
        ↓
Final TESDA SAG Evidence Matrix
```

This structure keeps each artifact tied to an observable skill and prevents the portfolio from overclaiming what a particular lab actually demonstrates.
