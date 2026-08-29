# BOTS v2 Investigation Report

## 1. Investigation Information

- **Investigation:** BOTS v2 / Splunk 2
- **Analyst:** ______________________________
- **Date:** ______________________________
- **Splunk environment:** ______________________________
- **Dataset:** `botsv2`
- **Evidence scope:** 100, 200, 300, and 400 Series
- **Evidence images currently catalogued:** 42

## 2. Purpose

This report documents the investigation workflow across the four BOTS v2 question series. Each section records the question, the SPL used in the reference investigation, the resulting finding, and the corresponding uploaded evidence image(s).

The explanatory text below is paraphrased. SPL commands are preserved exactly as presented in the supplied walkthrough so that the investigation procedure remains reproducible.

> **Portfolio note:** The reference walkthrough is used as a study and cross-check resource. The screenshots linked below are the candidate's uploaded evidence files in this repository.

---

# 3. 100 Series — Amber Turing Investigation

## 100-Q1 — Competitor website visited by Amber

### Investigation approach

The PAN traffic data is first searched for Amber to identify her internal IP address. The investigation then pivots to HTTP traffic and filters for beer-related sites, removes duplicate sites, and presents the remaining site in a table.

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

Amber's identified address is `10.0.2.101`. The HTTP pivot identifies **www.berkbeer.com** as the competitor website she visited.

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

The relevant URI identifies the image used to display the executive contact information: **`/images/ceoberk.png`**.

### Evidence

![100-Q2 — URI image-file result](../screenshots/04-100-q02-spl_result_URI_image_file.png)

---

## 100-Q3 — CEO name

### SPL

```spl
index="botsv2" sourcetype="stream:smtp" "berkbeer.com"
```

### Finding

The SMTP evidence identifies the CEO as **Martin Berk**. The raw email content provides the supporting identity/signature evidence.

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

The CEO's email address is **mberk@berkbeer.com**.

### Evidence

![100-Q4 — CEO email result](../screenshots/07-100-q04-spl_result_ceo_email.png)

---

## 100-Q5 — Competitor employee email address

### SPL

```spl
index="botsv2" sourcetype="stream:smtp" "berkbeer.com"
```

### Finding

The SMTP event and its raw message identify the employee contacted by Amber as **hbernhard@berkbeer.com**.

### Evidence

![100-Q5 — Employee email result](../screenshots/08-100-q05-spl_result_employee_email.png)

![100-Q5 — Raw employee email](../screenshots/09-100-q05-spl_result_raw_employee_email.png)

---

## 100-Q6 — Attachment sent by Amber

### Evidence source

The attachment is identified from the same SMTP event used for Q5 by examining the `attach_filename` field.

### Finding

The attachment is **Saccharomyces_cerevisiae_patent.docx**.

### Evidence

![100-Q6 — Attachment filename](../screenshots/10-100-q06-same_event_q05_attach_filename.png)

---

## 100-Q7 — Amber's personal email address

### Evidence source

The same Q5 email event contains encoded content. Decoding the relevant Base64 content exposes the personal email address.

### Finding

Amber's personal email address is **ambersthebest@yeastiebeastie.com**.

### Evidence

![100-Q7 — Base64 email content](../screenshots/11-100-q07-same_event_q05_base64_content.png)

![100-Q7 — Decoded email content](../screenshots/12-100-q07-same_event_q05_decoded_content.png)

---

# 4. 200 Series — Web, Vulnerability Scanning and XSS Investigation

## 200-Q1 — TOR Browser version

### SPL

```spl
index="botsv2" "tor" "amber" "install"
| sort -_time desc
```

### Finding

The installation event identifies TOR Browser version **7.0.4**.

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

The public IPv4 address is **52.42.208.228**. The HTTP data also exposes the private server address **172.31.4.249**, which is useful for subsequent correlation.

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

The source address generating the unusually high volume of requests is **45.77.65.211**, indicating the system used for the web vulnerability scan.

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

The SQL function observed in the malicious request is **`updatexml`**, indicating SQL injection activity against the URI.

### Evidence

![200-Q5 — Abused SQL function](../screenshots/18-200-q05-spl_result_abused_SQL_function.png)

---

## 200-Q6 — Kevin's stolen browser cookie

### SPL

```spl
index="botsv2" sourcetype="stream:http" kevin "<script>"
```

### Finding

The XSS-related event contains the stolen browser cookie value **1502408189**.

### Evidence

![200-Q6 — Cookie value](../screenshots/19-200-q06-spl_result_cookie_value.png)

---

## 200-Q7 — Maliciously created Brewertalk username

### Evidence source

The same HTTP event used in Q6 contains the account-creation information in the destination content. The username created through the malicious action is **kIagerfield**.

### Evidence

![200-Q7 — Username and password from Q6 event](../screenshots/20-200-q07-same_event_q06_username_n_pass.png)

---

# 5. 300 Series — Ransomware, USB and Malware Investigation

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

The encrypted PowerPoint filename is **Frothly_marketing_campaign_Q317.pptx.crypt_**.

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

The search identifies USB hardware-monitoring events. The relevant event contains the USB model, serial and vendor identifiers. The vendor ID is then correlated with external hardware-vendor information.

### Finding

The vendor is **Alcor Micro Corp.**

### Evidence

![300-Q3 — USB query result](../screenshots/24-300-q03-spl_result_USB_query.png)

![300-Q3 — Raw USB vendor information](../screenshots/25-300-q03-same_event_raw_text_USB_vendor.png)

> **Evidence gap:** The reference walkthrough also shows a separate vendor-ID lookup image. No separate uploaded vendor-lookup screenshot is currently catalogued for Q3, so the final portfolio should either add that screenshot or explicitly mark the external lookup as supporting evidence.

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

The file identified through the event data is associated with a **PERL executable**. The malware therefore contains at least a Perl component.

### Evidence

![300-Q4 — Username field](../screenshots/26-300-q04-same_event_fields_username.png)

![300-Q4 — File-events name field](../screenshots/27-300-q04-spl_result_name_field_file_events.png)

![300-Q4 — MD5 field](../screenshots/28-300-q04-spl_result_field_md5.png)

![300-Q4 — VirusTotal MD5 result](../screenshots/29-300-q04-virus_total_result_md5.png)

> **Filename note:** The uploaded filename sequence contains additional Q4 evidence views. The report labels them according to the investigation step they support while preserving the original uploaded filenames.

---

## 300-Q5 — Malware first-seen date

### Evidence source

The malware's MD5 is checked in VirusTotal and the Details information is used to identify its earliest observed date.

### Finding

The malware was first seen in the wild on **2017-01-17**.

### Evidence

![300-Q5 — VirusTotal first-seen information](../screenshots/30-300-q05-same_event_virus_total_details_first_seen.png)

---

## 300-Q6 — First C2 domain

### Evidence source

The VirusTotal Relations information is used to identify the dynamic DNS destinations contacted by the malware.

### Finding

The first C2 destination alphabetically is **eidk.duckdns.org**.

### Evidence

![300-Q6 — First C2 domain](../screenshots/31-300-q05-same_event_relations_tab_1st_domain_C2_server.png)

---

## 300-Q7 — Second C2 domain

### Finding

The second C2 destination alphabetically is **eidk.hopto.org**.

### Evidence

![300-Q7 — Second C2 domain](../screenshots/32-300-q05-same_event_relations_tab_2nd_domain_C2_server.png)

> **Filename note:** The uploaded filename says `q05` for images 31 and 32. The investigation content corresponds to the reference's Q6 and Q7. The filename itself is preserved and should not be renamed during this stage.

---

# 6. 400 Series — Taedonggang APT, Malware and Persistence

## 400-Q1 — Spearphishing ZIP attachment

### SPL

```spl
index="botsv2" sourcetype="stream:smtp" .zip
```

### Finding

The malicious email contains the attachment **invoice.zip**.

### Evidence

![400-Q1 — ZIP attachment query](../screenshots/33-400-q01-spl_query_attachment.png)

---

## 400-Q2 — ZIP password

### Evidence source

The raw text of the same email event contains the password supplied by the sender.

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

The consistent SSL issuer value is **C = US**.

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

The malware/document sample is examined through the supplied malware-analysis evidence. The metadata identifies **Ryan Kovar**.

### Finding

The person implicated in the document metadata is **Ryan Kovar**.

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

The scheduled task contacts **`process.php`** at the C2 URL path.

### Evidence

![400-Q7 — New scheduled task](../screenshots/40-400-q07-spl_result_new_sched_task.png)

![400-Q7 — HKLM data field](../screenshots/41-400-q07-spl_result_HKLM_data_field.png)

![400-Q7 — UTF-16 little-endian decoded data](../screenshots/42-400-q07-decoding_to_UTF_16_little_endian.png)

---

# 7. Consolidated Investigation Findings

The four series demonstrate several related defensive investigation activities:

| Series | Primary investigation themes | Major findings |
|---|---|---|
| 100 | User activity, web traffic, SMTP and encoded email content | Amber's competitor reconnaissance, executive contact, attachment and personal-email evidence |
| 200 | Web reconnaissance, vulnerability scanning, SQL injection and XSS | TOR use, Brewertalk infrastructure, scanner source, `/member.php`, `updatexml`, stolen cookie and malicious account creation |
| 300 | Ransomware, endpoint activity, USB correlation, malware and C2 | Ransomware artifacts, USB vendor, Perl malware, first-seen date and two C2 domains |
| 400 | APT phishing, SSL, FTP, malware/document analysis and persistence | ZIP phishing, password, SSL issuer, unusual HWP file, document metadata, scheduled-task persistence and C2 URI |

# 8. Key Indicators of Compromise

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

# 9. Attack Techniques Observed

The investigation provides evidence of:

- Reconnaissance and competitor targeting
- Web browsing and proxy activity
- Vulnerability scanning
- SQL injection
- Cross-site scripting (XSS)
- Credential/session-data exposure
- Spearphishing with malicious attachments
- Ransomware file encryption
- USB-based malware transfer
- Malware execution and C2 communication
- Dynamic DNS-based C2
- Scheduled-task persistence
- Registry-based C2 configuration
- Encoded payload/configuration data

# 10. Evidence-to-Finding Method

The evidence chain used throughout the investigation is:

```text
Question
   ↓
SPL query / investigation action
   ↓
Relevant event
   ↓
Field expansion / raw data / external analysis
   ↓
Finding
   ↓
Correlation
   ↓
Security interpretation
```

The multiple screenshots for several questions are intentionally retained because they demonstrate the investigative process rather than only the final answer.

# 11. TESDA Evidence Relevance

The BOTS v2 investigation is particularly useful as evidence for:

- **02-log-event-analysis** — searching, filtering, correlating and interpreting event data;
- **03-network-traffic-analysis** — PAN, HTTP, DNS, SMTP and FTP investigation;
- **04-endpoint-analysis** — host, user, USB and Windows-event investigation;
- **05-malware-ioc-analysis** — hashes, malware characteristics, C2 domains and malicious files;
- **06-vulnerability-scanning** — identification and analysis of web vulnerability-scanning activity;
- **07-incident-investigation** — correlation of multiple events into attack narratives;
- **08-threat-intelligence** — VirusTotal and malware/document-analysis pivots;
- **11-reporting** — documenting evidence, findings, IOCs and investigative conclusions.

BOTS v2 is **not by itself sufficient evidence for complete containment, eradication, recovery, or vulnerability-management workflows**. Those gaps remain addressed by the supplementary practical labs in the portfolio.

# 12. Evidence Limitations

1. Some reference questions use external analysis platforms. Such results should be clearly labeled as supporting external analysis.
2. The uploaded screenshots are the candidate's evidence artifacts; filenames are preserved even when a filename's question number does not perfectly correspond to the final evidence classification.
3. The 300-Q3 vendor lookup is described by the reference but no separate vendor-lookup screenshot is currently included in the uploaded set.
4. The final portfolio should replace any remaining reference-derived assumptions with the candidate's own observed results where the environment permits.

# 13. Conclusion

The BOTS v2 investigation demonstrates a broad SOC workflow: identify suspicious activity, pivot across data sources, extract relevant fields, correlate events, validate indicators through additional evidence, and document the resulting attack narrative.

For the TESDA RPL portfolio, the strongest value of this activity is the demonstrated ability to perform **log/event analysis, network traffic analysis, endpoint investigation, malware/IOC analysis, threat intelligence correlation, incident investigation, and security reporting**. Containment, recovery and formal vulnerability-management processes should be demonstrated separately rather than inferred from this investigation alone.
