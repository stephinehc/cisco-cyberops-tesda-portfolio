# BOTS v2 Screenshot Evidence Index

This folder is structured to match the investigation evidence shown in the supplied Splunk 2 walkthrough. A single question may contain multiple screenshots, including the SPL query/result, expanded event fields, raw content, decoded content, or external-analysis result. Each distinct image receives its own evidence entry.

The labels below are portfolio labels and are not copies of source captions.

> **Evidence rule:** For the TESDA portfolio, use screenshots captured from the candidate's own BOTS v2/Splunk environment whenever possible. Reference images are used to establish the evidence sequence and expected type of visual proof, not to represent the candidate's own performance.

## 100 Series — Amber Turing Investigation

**Reference-matched image count: 11**

| # | Question | Image label | Filename |
|---:|---|---|---|
| 01 | 100-Q1 | Amber IP — PAN traffic query/result | `01-100-q01-pan-traffic-result.png` |
| 02 | 100-Q1 | Amber IP — expanded event fields | `02-100-q01-amber-ip-expanded-fields.png` |
| 03 | 100-Q1 | Amber HTTP traffic — competitor-domain result | `03-100-q01-http-competitor-result.png` |
| 04 | 100-Q2 | Competitor website — executive contact image URI | `04-100-q02-executive-contact-image.png` |
| 05 | 100-Q3 | BerkBeer SMTP query/result — CEO email event | `05-100-q03-smtp-ceo-result.png` |
| 06 | 100-Q3 | CEO email — raw message content and identity | `06-100-q03-ceo-raw-email.png` |
| 07 | 100-Q5 | Amber-to-employee SMTP query/result | `07-100-q05-employee-email-result.png` |
| 08 | 100-Q5 | Employee email — raw message content | `08-100-q05-employee-raw-email.png` |
| 09 | 100-Q6 | Attachment field — `attach_filename` | `09-100-q06-attachment-filename.png` |
| 10 | 100-Q7 | Base64-encoded email content | `10-100-q07-base64-email-content.png` |
| 11 | 100-Q7 | Decoded email content — Amber personal email | `11-100-q07-decoded-personal-email.png` |

### 100-Q4 — CEO email address

**No separate reference image is assigned to Q4.** The answer is derived from the CEO SMTP evidence already displayed for Q3. Therefore, do not create an artificial Q4 screenshot.

Evidence relationship:

```text
100-Q3 SMTP evidence
        ↓
CEO identity + email address
        ↓
100-Q4 answer
```

If your own BOTS v2 session produces a separate useful screenshot while answering Q4, it may be captured as **candidate-generated supplementary evidence**, but it should not be counted as a reference-matched image.

## 200 Series — Web, Vulnerability Scan and XSS Investigation

| # | Question | Image label | Filename |
|---:|---|---|---|
| 12 | 200-Q1 | TOR installation search result | `12-200-q01-tor-installation-result.png` |
| 13 | 200-Q2 | DNS result — public server IP | `13-200-q02-dns-public-ip.png` |
| 14 | 200-Q2 | HTTP result — destination IP | `14-200-q02-http-destination-ip.png` |
| 15 | 200-Q3 | Source-IP statistics — vulnerability scanner | `15-200-q03-vulnerability-scan-source-ip.png` |
| 16 | 200-Q4 | URI-path frequency result | `16-200-q04-uri-path-frequency.png` |
| 17 | 200-Q5 | SQL function evidence | `17-200-q05-sql-function-result.png` |
| 18 | 200-Q6 | XSS event — stolen browser cookie | `18-200-q06-xss-cookie-event.png` |
| 19 | 200-Q7 | XSS event — malicious username creation | `19-200-q07-malicious-username-event.png` |

## 300 Series — Mallory, Ransomware, USB and Malware Investigation

| # | Question | Image label | Filename |
|---:|---|---|---|
| 20 | 300-Q1 | Mallory MacBook hostname identification | `20-300-q01-mallory-hostname.png` |
| 21 | 300-Q1 | Encrypted PowerPoint filename | `21-300-q01-encrypted-powerpoint.png` |
| 22 | 300-Q2 | Encrypted Game of Thrones file | `22-300-q02-encrypted-got-file.png` |
| 23 | 300-Q3 | USB event — device discovery | `23-300-q03-usb-event.png` |
| 24 | 300-Q3 | Raw USB details — model/serial/vendor ID | `24-300-q03-usb-raw-details.png` |
| 25 | 300-Q3 | Vendor-ID lookup — USB manufacturer | `25-300-q03-usb-vendor-lookup.png` |
| 26 | 300-Q4 | Malware file event — filename and MD5 | `26-300-q04-malware-file-md5.png` |
| 27 | 300-Q4 | VirusTotal — malware language identification | `27-300-q04-virustotal-perl.png` |
| 28 | 300-Q5 | VirusTotal — first-seen date | `28-300-q05-virustotal-first-seen.png` |
| 29 | 300-Q6 | VirusTotal Relations — first C2 domain | `29-300-q06-first-c2-domain.png` |
| 30 | 300-Q7 | VirusTotal Relations — second C2 domain | `30-300-q07-second-c2-domain.png` |

## 400 Series — Taedonggang APT, Malware and Persistence

| # | Question | Image label | Filename |
|---:|---|---|---|
| 31 | 400-Q1 | SMTP event — spearphishing ZIP attachment | `31-400-q01-zip-attachment.png` |
| 32 | 400-Q2 | Raw email — ZIP password | `32-400-q02-zip-password.png` |
| 33 | 400-Q4 | FTP event — unusual downloaded file | `33-400-q04-unusual-ftp-file.png` |
| 34 | 400-Q5 | Supporting external analysis — file metadata evidence | `34-400-q05-file-metadata-analysis.png` |
| 35 | 400-Q6 | Supporting external analysis — document finding | `35-400-q06-document-analysis.png` |
| 36 | 400-Q7 | Scheduled-task creation events | `36-400-q07-scheduled-task-events.png` |
| 37 | 400-Q7 | Decoded registry/C2 URI evidence | `37-400-q07-decoded-c2-uri.png` |

## Reference image count

**37 separate investigation screenshots are currently represented in this index**, with the 100 Series corrected to **11 images**.

The 100 Series was previously under-counted. It is now explicitly represented as 11 image entries, while Q4 remains a cross-reference to the Q3 SMTP evidence because the walkthrough does not introduce a separate Q4 screenshot.

The same principle applies throughout the remaining series: if a question contains multiple distinct evidence views, each receives a separate filename and label; if a question derives its answer from an already displayed event, no artificial duplicate image is created.

## Screenshot naming and capture standard

Each candidate screenshot should show enough context to establish:

- the SPL query or investigation action;
- the relevant time range when applicable;
- the result/event used as evidence;
- important fields used for the pivot;
- the information supporting the answer.

For external-analysis screenshots, label them clearly as **supporting external analysis** rather than implying that the result was generated by Splunk/BOTS v2 locally.

Keep the numbering above when replacing the reference sequence with your own screenshots. This provides a traceable chain:

```text
Question → SPL/action → Screenshot → Finding → TESDA evidence domain → TESDA criterion
```
