# BOTS v2 Threat-Hunting Guide — Splunk 2 Workflow

## Purpose

This guide turns the supplied TryHackMe Splunk 2 walkthrough into a portfolio-friendly hunting workflow. The explanatory text is paraphrased, while the SPL commands are retained exactly as they appear in the reference material, including placeholder tokens and legacy typos. Do not silently correct a command in the evidence record: if a query fails in the lab, document the original query and then record the working variant separately.

Reference material:

- TryHackMe — Splunk 2
- jniket — TryHackMe Splunk 2 walkthrough
- Official Splunk BOTS v2 dataset

The TryHackMe room explains that the BOTS v2 dataset was produced from a lab environment containing Windows endpoints, Splunk Universal Forwarder/Stream, Sysmon and Windows Event Logging, Palo Alto Networks firewall/proxy telemetry, and Suricata IDS data. citeturn0search0

---

# 1. Initial Data Discovery

Before investigating a specific user or incident, determine what types of data are present in the `botsv2` index.

### Sourcetype inventory

```spl
| metadata type=sourcetypes index=botsv2 | eval firstTime=strftime(firstTime,"%Y-%m-%d %H:%M:%S") | eval lastTime=strftime(lastTime,"%Y-%m-%d %H:%M:%S") | eval recentTime=strftime(recentTime,"%Y-%m-%d %H:%M:%S") | sort - totalCount
```

Use the result to identify the telemetry sources that will be useful during later investigations.

---

# 2. 100-Series — Amber Turing Investigation

The first investigation follows Amber Turing and attempts to determine which competitor website she accessed, followed by the related HTTP and SMTP activity.

## Step 1 — Locate Amber's activity

Start broadly and then narrow the search to Palo Alto traffic so the internal address associated with Amber can be identified.

```spl
index="botsv2" amber
```

```spl
index"botsv2" sourcetype="pan:traffic"
```

Once Amber's IP address has been established from the event fields, use it to restrict the search to HTTP stream data.

```spl
index="botsv2" IPADDR sourcetype="stream:HTTP"
```

Replace `IPADDR` with the IP address observed in the candidate's own BOTS v2 environment.

## Step 2 — Reduce duplicate HTTP destinations

The objective is to isolate the website associated with the competitor. The original learning material uses a duplicate-removal command followed by a table command.

```spl
index="botv2" IPADDR sourcetype="stream:HTTP" | KEYWORD site | KEYWORD site
```

Replace the placeholders only when performing the exercise. Preserve the original query in the evidence notes.

The reference also demonstrates narrowing the search by the relevant industry keyword:

```spl
index="botsv2" IPADDR sourcetype="stream:HTTP" *INDUSTRY* | KEYWORD site | KEYWORD site
```

## Step 3 — Examine traffic to the competitor

Once the competitor URI/domain is identified, isolate the related HTTP events.

```spl
index="botsv2" IPADDR sourcetype="stream:HTTP" COMPETITOR_WEBSITE
```

Use the event fields to identify the image/URI associated with the executive contact information.

## Step 4 — Correlate with SMTP

Use the discovered competitor domain and Amber's email address to pivot from web activity to email communication.

```spl
index="botsv2" sourcetype="stream:smtp" AMBERS_EMAIL COMPETITOR_WEBSITE
```

The key investigation method is **pivoting from user → IP → HTTP → site → SMTP**.

---

# 3. 200-Series — Host, Web-Scan and XSS Investigation

The 200-series activities move into endpoint installation, external scanning, SQL-related web activity, XSS, and spearphishing clues.

## Step 1 — Identify Tor activity

Start with Amber and Tor as search terms.

```spl
index="botsv2" amber tor
```

The reference recommends adding another narrowing term after inspecting the returned events.

```spl
index="botsv2" amber tor KEYWORD
```

## Step 2 — Investigate the attacker IP

After determining the attacker address from the earlier questions, use it as the source address.

```spl
index="botsv2" src_ip="ATTACKER_IP"
```

Inspect Interesting Fields and event details to determine the URI path involved in the attack.

## Step 3 — Pivot to the attacked URI

Once the URI path has been identified:

```spl
index="botsv2" src_ip="ATTACKER_IP" uri_path="URI_PATH"
```

This should allow the analyst to investigate the specific web function or parameter being targeted.

## Step 4 — Investigate Kevin and the XSS activity

Start with a user-focused search:

```spl
index="botvs2" kevin
```

Use the returned fields to identify Kevin and then narrow the investigation toward HTTP events associated with the XSS activity and cookie value.

## Step 5 — Identify the spearphishing username

The reference continues the investigation using a keyword search:

```spl
index="botv2" KEYWORD
```

Replace `KEYWORD` with the investigation term derived from the preceding evidence.

---

# 4. 300-Series — Mallory, macOS and USB Investigation

The 300-series investigation starts with Mallory and her MacBook. The objective is to correlate endpoint telemetry, encrypted files, malware activity, and USB information.

## Step 1 — Identify Mallory's endpoint

```spl
index="botsv2" mallory
```

Use the returned fields to identify the MacBook hostname.

## Step 2 — Locate the PowerPoint document

Once the hostname is known, narrow the search to common PowerPoint extensions.

```spl
index="botsv2" host="NAME_MACBOOK"
```

Then:

```spl
index="botsv2" host="NAME_MACBOOK" (*.ppt OR *.pptx)
```

Record the filename observed in the candidate's own result set.

## Step 3 — Locate the encrypted movie file

The reference method is to use the relevant sourcetype and the extension associated with the encrypted files.

```spl
index="botsv2" host="NAME_MACBOOK" sourcetype="?" *.EXT
```

Replace the placeholders using values discovered from the actual investigation.

## Step 4 — Investigate the MacBook's osquery data

Start with the endpoint name:

```spl
index="botsv2" kutekitten
```

Use the resulting events to identify Mallory's user path and the relevant osquery fields.

## Step 5 — Narrow to the user directory

```spl
index="botsv2" kutekitten "\\/PATH\\/MALLORY"
```

The path is intentionally double escaped as shown in the reference query.

## Step 6 — Correlate nearby endpoint events

The reference then uses a two-keyword query to narrow the time segment around the suspicious file.

```spl
index="botsv2" kutekitten KEYWORD KEYWORD
```

Use the event timeline to investigate activity immediately before and after the suspicious artifact.

---

# 5. 400-Series — Spearphishing, FTP and Malware Execution

The 400-series investigation focuses on email attachments, attacker infrastructure, FTP transfers, malware execution, and scheduled-task persistence.

## Step 1 — Find the suspicious email attachment

Search SMTP data for ZIP-related events:

```spl
index="botsv2" sourcetype="stream:?" *.EXT
```

Use the event details to identify the attachment and then inspect the raw email contents when appropriate.

## Step 2 — Pivot using the attacker IP

Use the attacker IP identified during the earlier web investigation and switch to TCP stream data:

```spl
index="botsv2" sourcetype="stream:?" ATTACKER_IP
```

## Step 3 — Investigate the unusual FTP download

The reference uses:

```spl
index="botsv2" sourcetype="stream:ftp" ("get" OR "retr")
```

Review the resulting filename fields and correlate them with the investigation context.

## Step 4 — Search for the DLL mentioned in the scenario

```spl
index="botsv2" winsys32.dll
```

Use the associated sourcetype to construct a more focused query:

```spl
index="botvs2" sourcetype="stream:?"
```

Then narrow the search using the relevant download method:

```spl
index="botvs2" sourcetype="stream:?" method=COMMAND
```

## Step 5 — Analyze the referenced malware sample

The original learning material uses external malware-analysis resources to understand execution behavior. For the portfolio, record the external-analysis reference as supporting intelligence and do not claim that the external analysis was performed locally.

## Step 6 — Investigate scheduled-task activity

Start with:

```spl
index"botsv2" schtasks.exe
```

Then correlate individual events with the associated host, user, process, command line, and timeline.

---

# 6. Investigation Method Used Throughout BOTS v2

The repeated pattern across the questions is more important than any single answer:

```text
Question / Objective
        ↓
Broad keyword search
        ↓
Identify user / host / IP
        ↓
Select useful sourcetype
        ↓
Narrow using fields
        ↓
Pivot to another data source
        ↓
Correlate timestamps
        ↓
Identify IOC / artifact / behavior
        ↓
Validate the finding
        ↓
Document evidence
```

This makes BOTS v2 valuable for the portfolio because it demonstrates independent SIEM investigation rather than simply following a fixed CyberOps lab procedure.

---

# 7. Evidence Capture Requirements

For each completed question or investigation:

| Evidence item | Requirement |
|---|---|
| Question/objective | Record the exact investigation objective |
| SPL | Preserve the exact query used |
| Result | Screenshot the relevant result |
| Fields | Record important fields used for the pivot |
| IOC | Record IP/domain/hash/file/user/host when applicable |
| Correlation | Record the second data source or event used for validation |
| Analysis | Explain why the evidence supports the conclusion |
| Conclusion | State the finding in analyst language |
| TESDA mapping | Link the evidence to the applicable domain/criterion |

## Important

The final repository should contain **candidate-generated screenshots and observations**. Walkthrough answers are learning references only.
