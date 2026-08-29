# BOTS v2 Setup Guide

## 1. Choose the dataset

The official Splunk BOTS v2 repository provides:

- **Full dataset** — approximately 16.4 GB, pre-indexed Splunk data.
- **Attack-only dataset** — approximately 3.2 GB, containing the attack-focused portion of the dataset.

For this portfolio, start with the **attack-only dataset** if storage and deployment time are concerns. The official project states that the full dataset is a superset of the attack-only dataset and that both should not be installed together. citeturn1search0

## 2. Obtain the dataset

Use the official BOTS v2 project as the authoritative source for the dataset and required software versions:

https://github.com/splunk/botsv2

The official project lists the dataset download locations, MD5 values, installation process, and required Splunk add-ons. citeturn1search0

## 3. Install into Splunk

The official installation model is:

1. Install the required Splunk Enterprise version/environment.
2. Install the required apps/add-ons listed by the BOTS v2 project.
3. Extract the BOTS v2 dataset into `$SPLUNK_HOME/etc/apps`.
4. Restart Splunk.
5. Confirm the `botsv2` index is searchable.

The original BOTS v2 documentation lists Splunk Enterprise 7.2.1 and the add-on versions used to create the dataset. Because those versions are legacy, do not assume that a modern Splunk installation will behave identically; document the actual environment used for the portfolio. citeturn1search0

## 4. Verify the dataset

Run:

```spl
index=botsv2 earliest=0
```

Then inspect the available fields and sourcetypes.

A useful first inventory query from the Splunk 2 learning material is:

```spl
| metadata type=sourcetypes index=botsv2 | eval firstTime=strftime(firstTime,"%Y-%m-%d %H:%M:%S") | eval lastTime=strftime(lastTime,"%Y-%m-%d %H:%M:%S") | eval recentTime=strftime(recentTime,"%Y-%m-%d %H:%M:%S") | sort - totalCount
```

This establishes what kinds of telemetry are available before hunting.

## 5. Expected telemetry

The official BOTS v2 documentation lists sources including Palo Alto traffic/threat data, HTTP/DNS/TCP/SMTP/FTP streams, Windows Event Logs, Sysmon, osquery, Suricata, and endpoint/security telemetry. citeturn1search0

## 6. Evidence capture procedure

For every investigation:

1. Record the investigation question.
2. Record the exact SPL query.
3. Capture the resulting event/table.
4. Identify the relevant fields.
5. Correlate the result with another data source when appropriate.
6. Record the analyst interpretation.
7. Record the IOC, affected asset, user, host, domain, IP, or file where applicable.
8. Record the conclusion.
9. Save the screenshot using the naming convention in `screenshots/README.md`.
10. Do not copy answer values from walkthroughs into the final evidence record unless independently verified in the candidate's own BOTS v2 instance.

## 7. Recommended first run

Complete the following sequence before attempting the full question set:

```text
Dataset verification
      ↓
Sourcetype inventory
      ↓
100-series investigation
      ↓
200-series investigation
      ↓
300-series investigation
      ↓
400-series investigation
      ↓
Evidence consolidation
      ↓
TESDA mapping
```

## 8. Safety / evidence integrity

BOTS v2 contains realistic security-incident material. Keep analysis inside the controlled lab environment. Do not interact with live malicious infrastructure merely to reproduce a historical result.

The portfolio should contain screenshots and outputs from the local/authorized lab environment, not credentials or unrelated private data.
