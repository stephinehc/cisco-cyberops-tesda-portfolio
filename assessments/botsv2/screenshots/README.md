# BOTS v2 Screenshot Evidence Index

This index cross-checks the uploaded BOTS v2 evidence against the 100-, 200-, 300-, and 400-Series questions in the supplied Splunk 2 investigation walkthrough. The **actual uploaded filenames are authoritative** and are preserved exactly. Human-readable labels describe what each image demonstrates.

> **Evidence rule:** The screenshots in this repository are candidate evidence artifacts. The reference walkthrough is used for question/SPL cross-checking and investigation structure.

## 100 Series — Amber Turing Investigation

**12 uploaded images**

| # | Question | Evidence label | Actual filename |
|---:|---|---|---|
| 01 | 100-Q1 | PAN traffic SPL result — Amber event | `01-100-q01-spl_result_pan_traffic.png` |
| 02 | 100-Q1 | Expanded event fields — Amber IP | `02-100-q01-spl_result_drop_down.png` |
| 03 | 100-Q1 | HTTP event SPL result — competitor traffic | `03-100-q01-spl_result_http_event.png` |
| 04 | 100-Q2 | URI result — executive contact image | `04-100-q02-spl_result_URI_image_file.png` |
| 05 | 100-Q3 | SPL result — CEO name | `05-100-q03-spl_result_ceo_name.png` |
| 06 | 100-Q3 | Raw SMTP event — CEO identity/email | `06-100-q03-spl_result_raw_ceo_name.png` |
| 07 | 100-Q4 | SPL result — CEO email | `07-100-q04-spl_result_ceo_email.png` |
| 08 | 100-Q5 | SPL result — competitor employee email | `08-100-q05-spl_result_employee_email.png` |
| 09 | 100-Q5 | Raw SMTP event — employee email | `09-100-q05-spl_result_raw_employee_email.png` |
| 10 | 100-Q6 | Same Q5 event — attachment filename | `10-100-q06-same_event_q05_attach_filename.png` |
| 11 | 100-Q7 | Same Q5 event — Base64 content | `11-100-q07-same_event_q05_base64_content.png` |
| 12 | 100-Q7 | Decoded Base64 content | `12-100-q07-same_event_q05_decoded_content.png` |

### 100-Series answers

- Q1: `www.berkbeer.com`
- Q2: `/images/ceoberk.png`
- Q3: Martin Berk
- Q4: `mberk@berkbeer.com`
- Q5: `hbernhard@berkbeer.com`
- Q6: `Saccharomyces_cerevisiae_patent.docx`
- Q7: `ambersthebest@yeastiebeastie.com`

### 100-Series SPL

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

```spl
index="botsv2" sourcetype="stream:http" "10.0.2.101" "www.berkbeer.com"
```

```spl
index="botsv2" sourcetype="stream:smtp" "berkbeer.com"
```

## 200 Series — Web, Vulnerability Scanning and XSS

**8 uploaded images**

| # | Question | Evidence label | Actual filename |
|---:|---|---|---|
| 13 | 200-Q1 | TOR Browser version result | `13-200-q01-spl_result_TOR_version.png` |
| 14 | 200-Q2 | Public server IPv4 result | `14-200-q02-spl_result_server_public_ip_add.png` |
| 15 | 200-Q2 | Private server IPv4 result | `15-200-q02-spl_result_server_private_ip_add.png` |
| 16 | 200-Q3 | Web vulnerability-scan source IP | `16-200-q03-spl_result_web_vulb_scan_ip.png` |
| 17 | 200-Q4 | Attacked URI path | `17-200-q04-spl_result_URI_path.png` |
| 18 | 200-Q5 | Abused SQL function | `18-200-q05-spl_result_abused_SQL_function.png` |
| 19 | 200-Q6 | XSS cookie value | `19-200-q06-spl_result_cookie_value.png` |
| 20 | 200-Q7 | Same Q6 event — malicious username/password | `20-200-q07-same_event_q06_username_n_pass.png` |

### 200-Series answers

- Q1: `7.0.4`
- Q2: `52.42.208.228`
- Q3: `45.77.65.211`
- Q4: `/member.php`
- Q5: `updatexml`
- Q6: `1502408189`
- Q7: `kIagerfield`

### 200-Series SPL

```spl
index="botsv2" "tor" "amber" "install"
| sort -_time desc
```

```spl
index="botsv2" source="stream:dns" "www.brewertalk.com"
| table host_addr{}
| dedup host_addr{}
```

```spl
index="botsv2" source="stream:http" "www.brewertalk.com"
| table dest_ip
| dedup dest_ip
```

```spl
index="botsv2" source="stream:http" "www.brewertalk.com"
| stats count by src_ip
```

```spl
index="botsv2" src_ip="45.77.65.211" dest_ip="172.31.4.249"
| stats count by uri_path
```

```spl
index="botsv2" src_ip="45.77.65.211" dest_ip="172.31.4.249" uri_path="/member.php" select
```

```spl
index="botsv2" sourcetype="stream:http" kevin "<script>"
```

## 300 Series — Ransomware, USB and Malware

**12 uploaded images**

| # | Question | Evidence label | Actual filename |
|---:|---|---|---|
| 21 | 300-Q1 | Mallory host/device identification | `21-300-q01-spl_result_host_device_name.png` |
| 22 | 300-Q1 | Encrypted PowerPoint filename | `22-300-q01-spl_result_ppt_file_name.png` |
| 23 | 300-Q2 | Encrypted Game of Thrones file | `23-300-q02-spl_result_GOT_mov_file.png` |
| 24 | 300-Q3 | USB device query | `24-300-q03-spl_result_USB_query.png` |
| 25 | 300-Q3 | Same USB event — raw/vendor data | `25-300-q03-same_event_raw_text_USB_vendor.png` |
| 26 | 300-Q4 | Same event — username field | `26-300-q04-same_event_fields_username.png` |
| 27 | 300-Q4 | File-events name field | `27-300-q04-spl_result_name_field_file_events.png` |
| 28 | 300-Q4 | Malware MD5 field | `28-300-q04-spl_result_field_md5.png` |
| 29 | 300-Q4 | VirusTotal MD5 result | `29-300-q04-virus_total_result_md5.png` |
| 30 | 300-Q5 | VirusTotal first-seen details | `30-300-q05-same_event_virus_total_details_first_seen.png` |
| 31 | 300-Q6 | VirusTotal Relations — first C2 domain | `31-300-q05-same_event_relations_tab_1st_domain_C2_server.png` |
| 32 | 300-Q7 | VirusTotal Relations — second C2 domain | `32-300-q05-same_event_relations_tab_2nd_domain_C2_server.png` |

### 300-Series answers

- Q1: `Frothly_marketing_campaign_Q317.pptx.crypt_`
- Q2: `S07E02`
- Q3: Alcor Micro Corp.
- Q4: PERL
- Q5: `2017-01-17`
- Q6: `eidk.duckdns.org`
- Q7: `eidk.hopto.org`

### 300-Series SPL

```spl
index="botsv2" mallory
```

```spl
index="botsv2" mallory host="MACLORY-AIR13" *.ppt*
```

```spl
index="botsv2" host="maclory-air13" (got OR game OR thrones) *crypt*
```

```spl
index="botsv2" kutekitten usb
```

```spl
index="botsv2" kutekitten mkraeusen
```

```spl
index="botsv2" kutekitten mkraeusen name=file_events
```

> **Cross-check note:** The reference includes a separate external vendor-ID lookup image for Q3. No separate vendor-lookup screenshot is present in the 42 uploaded files currently catalogued.

> **Filename note:** Images 31 and 32 contain `q05` in their uploaded filenames, but their evidence content corresponds to the reference's Q6 and Q7 C2-domain questions. The original filenames are intentionally preserved.

## 400 Series — Taedonggang APT, Malware and Persistence

**10 uploaded images**

| # | Question | Evidence label | Actual filename |
|---:|---|---|---|
| 33 | 400-Q1 | ZIP attachment query | `33-400-q01-spl_query_attachment.png` |
| 34 | 400-Q2 | Same event — raw ZIP password/attachment | `34-400-q02-same_event_raw_pass_attachment.png` |
| 35 | 400-Q3 | SSL issuer field | `35-400-q03-spl_query_SSL_issuer_field.png` |
| 36 | 400-Q4 | Unusual Windows/System32 file query | `36-400-q04-spl_query_unsual_file_winsys32.png` |
| 37 | 400-Q4 | FTP retrieved filename field | `37-400-q04-spl_query_get_retr_filename_field.png` |
| 38 | 400-Q5 | Hybrid Analysis file details | `38-400-q05-hybrid_analysis_result_file_details.png` |
| 39 | 400-Q6 | Document analysis — invoice document | `39-400-q06-analysis_invoice_doc.png` |
| 40 | 400-Q7 | New scheduled-task result | `40-400-q07-spl_result_new_sched_task.png` |
| 41 | 400-Q7 | HKLM registry data field | `41-400-q07-spl_result_HKLM_data_field.png` |
| 42 | 400-Q7 | UTF-16 little-endian decoded data | `42-400-q07-decoding_to_UTF_16_little_endian.png` |

### 400-Series answers

- Q1: `invoice.zip`
- Q2: `912345678`
- Q3: `C = US`
- Q4: `나는_데이비드를_사랑한다.hwp`
- Q5: Ryan Kovar
- Q6: `CyberEastEgg`
- Q7: `process.php`

### 400-Series SPL

```spl
index="botsv2" sourcetype="stream:smtp" .zip
```

```spl
index="botsv2" dest_ip="45.77.65.211" SSL
```

```spl
index="botsv2" winsys32.dll
```

```spl
index="botsv2" sourcetype="stream:ftp" ("get" OR "retr")
```

```spl
index="botsv2" schtasks.exe sourcetype=wineventlog create
```

```spl
index="botsv2" HKLM\\Software\\Microsoft\\Network
```

## Consolidated evidence count

| Series | Uploaded images |
|---|---:|
| 100 | 12 |
| 200 | 8 |
| 300 | 12 |
| 400 | 10 |
| **Total** | **42** |

## Evidence handling rule

The final report should distinguish between:

1. **SPL-generated evidence** — directly produced by the BOTS v2/Splunk environment;
2. **Expanded/raw event evidence** — additional fields or message content from the same event;
3. **External-analysis evidence** — VirusTotal, Hybrid Analysis, document-analysis or vendor-lookup results used to validate a finding.

The final RPL evidence package should prioritize screenshots from the candidate's own BOTS v2 environment. Reference-derived answers are useful for cross-checking, but they are not substitutes for the candidate's practical evidence.
