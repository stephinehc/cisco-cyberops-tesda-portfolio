# BOTS v2 Investigation Report

## 1. Investigation Information

- **Investigation:** BOTS v2 / Splunk 2
- **Analyst:** ______________________________
- **Date:** ______________________________
- **Splunk environment:** ______________________________
- **Dataset:** `botsv2`
- **Evidence scope:** 100, 200, 300, and 400 Series
- **Evidence images currently catalogued:** 42

## 2. Controlled Environment and Data Privacy

All activities represented in this report are limited to a **simulated, isolated, and controlled training environment** using the BOTS v2 training dataset and designated laboratory tools.

The report does not document or imply monitoring, scanning, exploitation, investigation, containment, eradication, recovery, or other security activity against a live organizational production environment.

The values appearing in the BOTS v2 dataset—such as usernames, email addresses, IP addresses, domains, file names and other indicators—are treated as **training-dataset/simulated investigation data**. They must not be interpreted as confidential information belonging to a real organization.

No production data, confidential company information, real organizational credentials, private keys, or other restricted information should be added to this report.

## 3. Purpose

This report documents the investigation workflow across the four BOTS v2 question series. Each section records the question, the SPL used in the reference investigation, the resulting finding, and the corresponding uploaded evidence image(s).

The explanatory text is paraphrased. SPL commands are preserved as presented in the supplied walkthrough so that the investigation procedure remains reproducible for the training scenario.

> **Portfolio note:** The supplied walkthrough is used as a study and cross-check resource. The image files linked below are the uploaded screenshots associated with the investigation steps. Where screenshots originate from reference material rather than an independently captured laboratory session, they should be treated as reference/supporting material and not represented as independently performed evidence.

---

# 4. 100 Series — Amber Turing Investigation

## 100-Q1 — Competitor website visited by Amber

### Investigation approach

The PAN traffic data is searched for Amber to identify the simulated internal IP address. The investigation then pivots to HTTP traffic and filters for beer-related sites, removes duplicate sites, and presents the remaining site in a table.

### SPL

```spl
index="botsv2" sourcetype="pan:traffic" amber
```

```spl
index="botsv2" sourcetype="stream:http" "10.0.2.101"
```

```spl
index="botsv2" sourcetype="stream:http" "10.0.2.101" *beer*
| dedup site
| table site
```

### Finding

The simulated event identifies Amber's address as `10.0.2.101`. The HTTP pivot identifies **www.berkbeer.com** as the competitor website visited in the training dataset.

### Evidence

![100-Q1 — PAN traffic SPL result](../screenshots/01-100-q01-spl_result_pan_traffic.png)

![100-Q1 — Expanded event fields](../screenshots/02-100-q01-spl_result_drop_down.png)

![100-Q1 — HTTP event result](../screenshots/03-100-q01-spl_result_http_event.png)

---

## 100-Q2 — Executive contact image

### SPL

```spl
index="botsv2" sourcetype="stream:http" "10.0.2.101" "www.berkbeer.com"
```

### Finding

The relevant URI identifies the image used to display executive contact information: **`/images/ceoberk.png`**.

### Evidence

![100-Q2 — URI image-file result](../screenshots/04-100-q02-spl_result_URI_image_file.png)

---

## 100-Q3 — CEO name

### SPL

```spl
index="botsv2" sourcetype="stream:smtp" "berkbeer.com"
```

### Finding

The SMTP training event identifies the CEO as **Martin Berk**. The raw email content provides supporting identity information.

### Evidence

![100-Q3 — CEO name result](../screenshots/05-100-q03-spl_result_ceo_name.png)

![100-Q3 — Raw CEO email evidence](../screenshots/06-100-q03-spl_result_raw_ceo_name.png)

---

## 100-Q4 — CEO email address

### SPL

```spl
index="botsv2" sourcetype="stream:smtp" "berkbeer.com"
```

### Finding

The training dataset identifies the CEO email address as **mberk@berkbeer.com**.

### Evidence

![100-Q4 — CEO email result](../screenshots/07-100-q04-spl_result_ceo_email.png)

---

## 100-Q5 — Competitor employee email address

### SPL

```spl
index="botsv2" sourcetype="stream:smtp" "berkbeer.com"
```

### Finding

The SMTP event and raw message identify the simulated employee address as **hbernhard@berkbeer.com**.

### Evidence

![100-Q5 — Employee email result](../screenshots/08-100-q05-spl_result_employee_email.png)

![100-Q5 — Raw employee email](../screenshots/09-100-q05-spl_result_raw_employee_email.png)

---

## 100-Q6 — Attachment sent by Amber

### Evidence source

The attachment is identified from the same SMTP event used for Q5 by examining the `attach_filename` field.

### Finding

The training artifact is **Saccharomyces_cerevisiae_patent.docx**.

### Evidence

![100-Q6 — Attachment filename](../screenshots/10-100-q06-same_event_q05_attach_filename.png)

---

## 100-Q7 — Amber's personal email address

### Evidence source

The same Q5 email event contains encoded content. Decoding the relevant Base64 content exposes the training-dataset email address.

### Finding

The training dataset contains **ambersthebest@yeastiebeastie.com**.

### Evidence

![100-Q7 — Base64 email content](../screenshots/11-100-q07-same_event_q05_base64_content.png)

![100-Q7 — Decoded email content](../screenshots/12-100-q07-same_event_q05_decoded_content.png)

---

# 5. 200 Series — Web, Vulnerability Scanning and XSS Investigation

## 200-Q1 — TOR Browser version

### SPL

```spl
index="botsv2" "tor" "amber" "install"
| sort -_time desc
```

### Finding

The simulated installation event identifies TOR Browser version **7.0.4**.

### Evidence

![200-Q1 — TOR version](../screenshots/13-200-q01-spl_result_TOR_version.png)

---

## 200-Q2 — Public IPv4 address of www.brewertalk.com

### SPL — DNS

```spl
index="botsv2" source="stream:dns" "www.brewertalk.com"
| table host_addr{}
| dedup host_addr{}
```

### SPL — HTTP destination address

```spl
index="botsv2" source="stream:http" "www.brewertalk.com"
| table dest_ip
| dedup dest_ip
```

### Finding

The training dataset identifies the public IPv4 address as **52.42.208.228**. The HTTP data also exposes the private server address **172.31.4.249**, which supports subsequent correlation.

### Evidence

![200-Q2 — Public server IP](../screenshots/14-200-q02-spl_result_server_public_ip_add.png)

![200-Q2 — Private server IP](../screenshots/15-200-q02-spl_result_server_private_ip_add.png)

---

## 200-Q3 — Vulnerability-scanning source IP

### SPL

```spl
index="botsv2" source="stream:http" "www.brewertalk.com"
| stats count by src_ip
```

### Finding

The source address generating the unusually high request volume is **45.77.65.211**, representing the simulated vulnerability-scanning source in the dataset.

### Evidence

![200-Q3 — Vulnerability scan source IP](../screenshots/16-200-q03-spl_result_web_vulb_scan_ip.png)

---

## 200-Q4 — Frequently attacked URI path

### SPL

```spl
index="botsv2" src_ip="45.77.65.211" dest_ip="172.31.4.249"
| stats count by uri_path
```

### Finding

The most frequently targeted URI path is **`/member.php`**.

### Evidence

![200-Q4 — URI path result](../screenshots/17-200-q04-spl_result_URI_path.png)

---

## 200-Q5 — Abused SQL function

### SPL

```spl
index="botsv2" src_ip="45.77.65.211" dest_ip="172.31.4.249" uri_path="/member.php" select
```

### Finding

The SQL function observed in the simulated malicious request is **`updatexml`**, indicating SQL-injection activity in the training scenario.

### Evidence

![200-Q5 — Abused SQL function](../screenshots/18-200-q05-spl_result_abused_SQL_function.png)

---

## 200-Q6 — Simulated browser cookie exposure

### SPL

```spl
index="botsv2" sourcetype="stream:http" kevin "<script>"
```

### Finding

The XSS-related training event contains the simulated browser cookie value **1502408189**.

### Evidence

![200-Q6 — Cookie value](../screenshots/19-200-q06-spl_result_cookie_value.png)

---

## 200-Q7 — Simulated Brewertalk username

### Evidence source

The same HTTP event used in Q6 contains account-creation information in the destination content.

### Finding

The username created through the simulated malicious action is **kIagerfield**.

### Evidence

![200-Q7 — Username and password from Q6 event](../screenshots/20-200-q07-same_event_q06_username_n_pass.png)

---

# 6. 300 Series — Ransomware, USB and Malware Investigation

## 300-Q1 — Encrypted PowerPoint filename

### SPL — identify Mallory's host

```spl
index="botsv2" mallory
```

### SPL — identify PowerPoint file events

```spl
index="botsv2" mallory host="MACLORY-AIR13" *.ppt*
```

### Finding

The encrypted PowerPoint training artifact is **Frothly_marketing_campaign_Q317.pptx.crypt_**.

### Evidence

![300-Q1 — Mallory host/device name](../screenshots/21-300-q01-spl_result_host_device_name.png)

![300-Q1 — Encrypted PowerPoint filename](../screenshots/22-300-q01-spl_result_ppt_file_name.png)

---

## 300-Q2 — Encrypted Game of Thrones episode

### SPL

```spl
index="botsv2" host="maclory-air13" (got OR game OR thrones) *crypt*
```

### Finding

The encrypted movie corresponds to **Season 7, Episode 2 (S07E02)**.

### Evidence

![300-Q2 — Encrypted Game of Thrones file](../screenshots/23-300-q02-spl_result_GOT_mov_file.png)

---

## 300-Q3 — USB vendor used to transfer malware

### SPL

```spl
index="botsv2" kutekitten usb
```

### Investigation

The search identifies simulated USB hardware-monitoring events. The relevant event contains USB model, serial and vendor identifiers. The vendor ID can then be correlated with external hardware-vendor information.

### Finding

The vendor is **Alcor Micro Corp.**

### Evidence

![300-Q3 — USB query result](../screenshots/24-300-q03-spl_result_USB_query.png)

![300-Q3 — Raw USB vendor information](../screenshots/25-300-q03-same_event_raw_text_USB_vendor.png)

> **Evidence gap:** The reference walkthrough also shows a separate vendor-ID lookup image. No separate vendor-lookup screenshot is currently catalogued among the 42 uploaded files. The external lookup should therefore be treated as supporting/reference evidence unless an additional authorized screenshot is supplied.

---

## 300-Q4 — Malware programming language

### SPL — correlate the user's file events

```spl
index="botsv2" kutekitten mkraeusen
```

### SPL — narrow to file events

```spl
index="botsv2" kutekitten mkraeusen name=file_events
```

### Finding

The file evidence is associated with a **PERL** executable/component.

### Evidence

![300-Q4 — Username field](../screenshots/26-300-q04-same_event_fields_username.png)

![300-Q4 — File-events name field](../screenshots/27-300-q04-spl_result_name_field_file_events.png)

![300-Q4 — MD5 field](../screenshots/28-300-q04-spl_result_field_md5.png)

![300-Q4 — VirusTotal MD5 result](../screenshots/29-300-q04-virus_total_result_md5.png)

> **Filename note:** The original uploaded filenames are preserved even where the numbering/filename sequence does not perfectly match the final question classification.

---

## 300-Q5 — Malware first-seen date

### Evidence source

The malware MD5 is checked in VirusTotal and the Details information is used to identify the earliest observed date.

### Finding

The training artifact was first seen on **2017-01-17**.

### Evidence

![300-Q5 — VirusTotal first-seen information](../screenshots/30-300-q05-same_event_virus_total_details_first_seen.png)

---

## 300-Q6 — First C2 domain

### Evidence source

VirusTotal Relations information is used to identify the simulated dynamic-DNS destinations associated with the malware.

### Finding

The first C2 destination is **eidk.duckdns.org**.

### Evidence

![300-Q6 — First C2 domain](../screenshots/31-300-q05-same_event_relations_tab_1st_domain_C2_server.png)

---

## 300-Q7 — Second C2 domain

### Finding

The second C2 destination is **eidk.hopto.org**.

### Evidence

![300-Q7 — Second C2 domain](../screenshots/32-300-q05-same_event_relations_tab_2nd_domain_C2_server.png)

> **Filename note:** The uploaded filenames for images 31 and 32 contain `q05`; their evidence labels are based on the investigation content. The original filenames are intentionally preserved.

---

# 7. 400 Series — Taedonggang APT, Malware and Persistence

## 400-Q1 — Spearphishing ZIP attachment

### SPL

```spl
index="botsv2" sourcetype="stream:smtp" .zip
```

### Finding

The training email contains the attachment **invoice.zip**.

### Evidence

![400-Q1 — ZIP attachment query](../screenshots/33-400-q01-spl_query_attachment.png)

---

## 400-Q2 — ZIP password

### Evidence source

The raw text of the same training email event contains the password supplied by the sender.

### Finding

The ZIP password is **912345678**.

### Evidence

![400-Q2 — Raw email password/attachment evidence](../screenshots/34-400-q02-same_event_raw_pass_attachment.png)

---

## 400-Q3 — SSL issuer used by the attacker

### SPL

```spl
index="botsv2" dest_ip="45.77.65.211" SSL
```

### Finding

The relevant issuer value is **C = US**.

### Evidence

![400-Q3 — SSL issuer field](../screenshots/35-400-q03-spl_query_SSL_issuer_field.png)

---

## 400-Q4 — Unusual file downloaded through FTP

### SPL — locate winsys32.dll activity

```spl
index="botsv2" winsys32.dll
```

### SPL — narrow to FTP download activity

```spl
index="botsv2" sourcetype="stream:ftp" ("get" OR "retr")
```

### Finding

The unusual downloaded file is **나는_데이비드를_사랑한다.hwp**.

### Evidence

![400-Q4 — Unusual Windows/System32 file](../screenshots/36-400-q04-spl_query_unsual_file_winsys32.png)

![400-Q4 — Retrieved filename field](../screenshots/37-400-q04-spl_query_get_retr_filename_field.png)

---

## 400-Q5 — Person identified in file metadata

### Evidence source

The supplied malware-analysis result identifies **Ryan Kovar** in the training artifact's metadata.

### Finding

The person identified by the training artifact metadata is **Ryan Kovar**.

### Evidence

![400-Q5 — Hybrid Analysis file details](../screenshots/38-400-q05-hybrid_analysis_result_file_details.png)

---

## 400-Q6 — Text identified inside the document

### Evidence source

The document-analysis result identifies the text **CyberEastEgg**.

### Finding

The requested text is **CyberEastEgg**.

### Evidence

![400-Q6 — Document analysis](../screenshots/39-400-q06-analysis_invoice_doc.png)

---

## 400-Q7 — Scheduled-task C2 webpage

### SPL — identify newly created scheduled tasks

```spl
index="botsv2" schtasks.exe sourcetype=wineventlog create
```

### SPL — locate the registry hive value used by the task

```spl
index="botsv2" HKLM\\Software\\Microsoft\\Network
```

### Investigation

The scheduled-task events show PowerShell activity that modifies the `HKLM:\Software\Microsoft\Network` registry hive. The relevant data value is encoded and requires decoding to reveal the C2 URL.

### Finding

The scheduled task references **`process.php`** in the simulated C2 URL path.

### Evidence

![400-Q7 — New scheduled task](../screenshots/40-400-q07-spl_result_new_sched_task.png)

![400-Q7 — HKLM data field](../screenshots/41-400-q07-spl_result_HKLM_data_field.png)

![400-Q7 — UTF-16 little-endian decoded data](../screenshots/42-400-q07-decoding_to_UTF_16_little_endian.png)

---

# 8. Consolidated Investigation Findings

| Series | Primary investigation themes | Major findings |
|---|---|---|
| 100 | User activity, web traffic, SMTP and encoded email content | Simulated competitor reconnaissance, executive contact, attachment and encoded-email evidence |
| 200 | Web reconnaissance, vulnerability scanning, SQL injection and XSS | Simulated TOR use, Brewertalk infrastructure, scanner source, `/member.php`, `updatexml`, cookie exposure and account creation |
| 300 | Ransomware, endpoint activity, USB correlation, malware and C2 | Simulated ransomware artifacts, USB vendor, Perl malware, first-seen date and C2 domains |
| 400 | APT phishing, SSL, FTP, malware/document analysis and persistence | Simulated ZIP phishing, password, SSL issuer, unusual file, document metadata, scheduled-task persistence and C2 URI |

# 9. Key Indicators of Compromise

The following indicators are **training-dataset indicators** and should not be interpreted as indicators from a live organization:

| Type | Indicator |
|---|---|
| Internal IP | `10.0.2.101` |
| Web server public IP | `52.42.208.228` |
| Web server private IP | `172.31.4.249` |
| Vulnerability scanner IP | `45.77.65.211` |
| Target URI | `/member.php` |
| First C2 domain | `eidk.duckdns.org` |
| Second C2 domain | `eidk.hopto.org` |
| C2 IP | `45.77.65.211` |
| C2 URI | `process.php` |
| Malware language | Perl |
| ZIP attachment | `invoice.zip` |
| Unusual downloaded document | `나는_데이비드를_사랑한다.hwp` |

# 10. Attack Techniques Observed

The simulated investigation provides evidence of:

- Reconnaissance and competitor targeting
- Web browsing and proxy activity
- Vulnerability-scanning activity
- SQL injection
- Cross-site scripting (XSS)
- Credential/session-data exposure
- Spearphishing with a malicious attachment
- Ransomware-style file encryption
- USB-associated malware transfer
- Malware execution and C2 communication
- Dynamic-DNS-based C2
- Scheduled-task persistence
- Registry-based C2 configuration
- Encoded payload/configuration data

# 11. Evidence-to-Finding Method

```text
Question
   ↓
SPL query / investigation action
   ↓
Relevant simulated event
   ↓
Field expansion / raw data / external analysis
   ↓
Finding
   ↓
Correlation
   ↓
Security interpretation
```

Multiple screenshots are retained when they represent different investigation stages or evidence views.

# 12. TESDA Evidence Relevance

The BOTS v2 investigation is particularly useful as controlled-laboratory evidence for:

- **02-log-event-analysis** — searching, filtering, correlating and interpreting event data;
- **03-network-traffic-analysis** — PAN, HTTP, DNS, SMTP and FTP investigation;
- **04-endpoint-analysis** — host, user, USB and Windows-event investigation;
- **05-malware-ioc-analysis** — hashes, malware characteristics, C2 domains and malicious files;
- **06-vulnerability-scanning** — identification and analysis of vulnerability-scanning activity represented in the training dataset;
- **07-incident-investigation** — correlation of multiple events into simulated attack narratives;
- **08-threat-intelligence** — VirusTotal and malware/document-analysis pivots;
- **11-reporting** — documenting evidence, findings, IOCs and investigative conclusions.

BOTS v2 is **not by itself sufficient evidence for complete containment, eradication, recovery, or vulnerability-management workflows**. Those gaps remain addressed by controlled supplementary simulations.

# 13. Evidence Limitations

1. Some questions use external-analysis platforms. These results should be clearly labeled as supporting external analysis.
2. The uploaded screenshots are associated with the investigation steps, but their provenance must be distinguished from independently captured candidate evidence when preparing the final RPL package.
3. The reference walkthrough includes a separate vendor-ID lookup image for 300-Q3. No separate vendor-lookup screenshot is currently catalogued among the 42 uploaded files.
4. Images 31 and 32 contain `q05` in their original filenames although their evidence labels correspond to Q6 and Q7. The filenames are preserved intentionally and should be cleaned only during a later controlled repository cleanup if desired.
5. The final RPL package should use independently captured laboratory evidence wherever possible and should not represent reference material as personally performed activity.

# 14. Conclusion

The BOTS v2 investigation demonstrates a broad simulated SOC workflow: identify suspicious activity, pivot across data sources, extract relevant fields, correlate events, validate indicators through additional evidence, and document the resulting attack narrative.

For the TESDA RPL portfolio, the strongest value of this activity is the demonstrated investigation methodology across **log/event analysis, network traffic analysis, endpoint analysis, malware/IOC analysis, threat intelligence, incident investigation, and reporting**.

Containment, eradication, recovery and formal vulnerability-management processes are intentionally not inferred from BOTS v2. They will be demonstrated separately, if required, through controlled and isolated supplementary simulations.
