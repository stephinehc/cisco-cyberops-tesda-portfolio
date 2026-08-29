# BOTS v2 Screenshot Evidence Index

This folder is structured around the investigation evidence used in the BOTS v2 portfolio. A single question may contain multiple screenshots, including the SPL query/result, expanded event fields, raw content, decoded content, or external-analysis result. Each distinct image receives its own evidence entry.

The labels below are portfolio labels. The filenames for the 100 Series are the **actual filenames uploaded to the GitHub repository** and must be preserved exactly.

> **Evidence rule:** For the TESDA portfolio, screenshots should represent the candidate's own BOTS v2/Splunk investigation whenever possible. Reference material is used only to establish the investigation sequence and evidence type.

## 100 Series — Amber Turing Investigation

**Uploaded image count: 12**

| # | Question | Image label | Actual uploaded filename |
|---:|---|---|---|
| 01 | 100-Q1 | PAN traffic SPL result — Amber event | `01-100-q01-spl_result_pan_traffic.png` |
| 02 | 100-Q1 | Expanded SPL result — Amber event fields | `02-100-q01-spl_result_drop_down.png` |
| 03 | 100-Q1 | HTTP event SPL result — competitor traffic | `03-100-q01-spl_result_http_event.png` |
| 04 | 100-Q2 | URI image-file SPL result | `04-100-q02-spl_result_URI_image_file.png` |
| 05 | 100-Q3 | SPL result — CEO name | `05-100-q03-spl_result_ceo_name.png` |
| 06 | 100-Q3 | Raw event — CEO identity/email evidence | `06-100-q03-spl_result_raw_ceo_name.png` |
| 07 | 100-Q4 | SPL result — CEO email address | `07-100-q04-spl_result_ceo_email.png` |
| 08 | 100-Q5 | SPL result — employee email | `08-100-q05-spl_result_employee_email.png` |
| 09 | 100-Q5 | Raw event — employee email content | `09-100-q05-spl_result_raw_employee_email.png` |
| 10 | 100-Q6 | Same Q5 event — attachment filename | `10-100-q06-same_event_q05_attach_filename.png` |
| 11 | 100-Q7 | Same Q5 event — Base64 content | `11-100-q07-same_event_q05_base64_content.png` |
| 12 | 100-Q7 | Decoded Base64 content | `12-100-q07-same_event_q05_decoded_content.png` |

### 100-Series evidence notes

Unlike the earlier reference-matched index, this table reflects the **actual 12 files you uploaded**. The uploaded evidence includes a dedicated Q4 screenshot, so Q4 is now represented as an independent evidence item rather than only as a cross-reference to Q3.

The evidence chain is:

```text
100-Q1 → PAN traffic → expanded event → HTTP pivot
100-Q2 → URI/image-file evidence
100-Q3 → CEO name → raw event
100-Q4 → CEO email
100-Q5 → employee email → raw event
100-Q6 → attachment filename from the Q5 event
100-Q7 → Base64 content from the Q5 event → decoded content
```

## 200 Series

The 200-Series entries will be updated **only after the corresponding images have been uploaded and the filenames are provided/verified**. Do not rename or replace them with the previously generated filenames.

## 300 Series

The 300-Series entries will be updated **only after the corresponding images have been uploaded and the filenames are provided/verified**. Do not rename or replace them with the previously generated filenames.

## 400 Series

The 400-Series entries will be updated **only after the corresponding images have been uploaded and the filenames are provided/verified**. Do not rename or replace them with the previously generated filenames.

## Screenshot naming and evidence standard

The filename identifies the uploaded artifact; the image label explains its evidentiary purpose. The repository should preserve the actual uploaded filename exactly as stored in GitHub.

For every completed series, the final evidence chain should be:

```text
Question → SPL/action → Uploaded screenshot → Finding → TESDA evidence domain → TESDA criterion
```

When a question has multiple uploaded screenshots, all relevant screenshots should be retained rather than reducing the evidence to a single final-answer image.
