# BOTS v2 Screenshot Evidence Index

This folder is structured to match **every separate investigation screenshot shown in the supplied Splunk 2 walkthrough**. A question may have multiple screenshots; each distinct result, expanded/raw view, external-analysis view, or decoded-result view receives its own evidence entry.

The labels below are portfolio labels and are not copies of source captions.

> **Evidence rule:** For the TESDA portfolio, use screenshots captured from the candidate's own BOTS v2/Splunk environment whenever possible. Reference images are used to establish the evidence sequence and expected type of visual proof, not to represent the candidate's own performance.

## 100 Series — Amber Turing Investigation

| # | Question | Image label | Filename |
|---:|---|---|---|
| 01 | 100-Q1 | Amber IP identification — PAN traffic result | `01-100-q01-pan-traffic-amber-event.png` |
| 02 | 100-Q1 | Expanded event fields — Amber IP | `02-100-q01-expanded-fields-amber-ip.png` |
| 03 | 100-Q1 | HTTP competitor-domain result | `03-100-q01-http-competitor-domain.png` |
| 04 | 100-Q2 | Executive contact image URI | `04-100-q02-executive-contact-image-uri.png` |
| 05 | 100-Q3 | CEO email SMTP event | `05-100-q03-smtp-ceo-event.png` |
| 06 | 100-Q3 | Raw email — CEO identity | `06-100-q03-raw-email-ceo-name.png` |
| 07 | 100-Q5 | Raw email — competitor employee recipient | `07-100-q05-raw-email-employee-recipient.png` |
| 08 | 100-Q6 | Expanded attachment filename field | `08-100-q06-attachment-filename.png` |
| 09 | 100-Q7 | Decoded email — Amber personal email | `09-100-q07-decoded-personal-email.png` |

## 200 Series — Web, Vulnerability Scan and XSS Investigation

| # | Question | Image label | Filename |
|---:|---|---|---|
| 10 | 200-Q1 | TOR installation search result | `10-200-q01-tor-installation-result.png` |
| 11 | 200-Q2 | DNS result — public server IP | `11-200-q02-dns-public-ip.png` |
| 12 | 200-Q2 | HTTP result — destination IP | `12-200-q02-http-destination-ip.png` |
| 13 | 200-Q3 | Source-IP statistics — vulnerability scanner | `13-200-q03-vulnerability-scan-source-ip.png` |
| 14 | 200-Q4 | URI-path frequency result | `14-200-q04-uri-path-frequency.png` |
| 15 | 200-Q5 | SQL function evidence | `15-200-q05-sql-function-result.png` |
| 16 | 200-Q6 | XSS event — stolen browser cookie | `16-200-q06-xss-cookie-event.png` |
| 17 | 200-Q7 | XSS event — malicious username creation | `17-200-q07-malicious-username-event.png` |

## 300 Series — Mallory, Ransomware, USB and Malware Investigation

| # | Question | Image label | Filename |
|---:|---|---|---|
| 18 | 300-Q1 | Mallory MacBook hostname identification | `18-300-q01-mallory-hostname.png` |
| 19 | 300-Q1 | Encrypted PowerPoint filename | `19-300-q01-encrypted-powerpoint.png` |
| 20 | 300-Q2 | Encrypted Game of Thrones file | `20-300-q02-encrypted-got-file.png` |
| 21 | 300-Q3 | USB event — device discovery | `21-300-q03-usb-event.png` |
| 22 | 300-Q3 | Raw USB details — model/serial/vendor ID | `22-300-q03-usb-raw-details.png` |
| 23 | 300-Q3 | Vendor-ID lookup — USB manufacturer | `23-300-q03-usb-vendor-lookup.png` |
| 24 | 300-Q4 | Malware file event — filename and MD5 | `24-300-q04-malware-file-md5.png` |
| 25 | 300-Q4 | VirusTotal — malware language identification | `25-300-q04-virustotal-perl.png` |
| 26 | 300-Q5 | VirusTotal — first-seen date | `26-300-q05-virustotal-first-seen.png` |
| 27 | 300-Q6 | VirusTotal Relations — first C2 domain | `27-300-q06-first-c2-domain.png` |
| 28 | 300-Q7 | VirusTotal Relations — second C2 domain | `28-300-q07-second-c2-domain.png` |

## 400 Series — Taedonggang APT, Malware and Persistence

| # | Question | Image label | Filename |
|---:|---|---|---|
| 29 | 400-Q1 | SMTP event — spearphishing ZIP attachment | `29-400-q01-zip-attachment.png` |
| 30 | 400-Q2 | Raw email — ZIP password | `30-400-q02-zip-password.png` |
| 31 | 400-Q4 | FTP event — unusual downloaded file | `31-400-q04-unusual-ftp-file.png` |
| 32 | 400-Q5 | External analysis — file metadata evidence | `32-400-q05-file-metadata-analysis.png` |
| 33 | 400-Q6 | External analysis — document finding | `33-400-q06-document-analysis.png` |
| 34 | 400-Q7 | Scheduled-task creation events | `34-400-q07-scheduled-task-events.png` |
| 35 | 400-Q7 | Decoded registry/C2 URI evidence | `35-400-q07-decoded-c2-uri.png` |

## Reference image count

**35 separate investigation screenshots** are represented in this index.

The previous index incorrectly grouped some multi-image questions and therefore understated the number of screenshots. The walkthrough shows multiple distinct images for several questions—for example, 100-Q1 has three separate investigation images, 200-Q2 has two, 300-Q1 has two, 300-Q3 has three, and 400-Q7 has two. Those are now preserved as separate evidence entries.

Questions that do not introduce a separate image in the walkthrough do not receive an artificial placeholder image. For example, some answers are derived from an event already displayed for the preceding question.

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
