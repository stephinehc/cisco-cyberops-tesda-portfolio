# CyberOps Associate v1.0 — Assessment Documentation

## 1. Scenario

The analyst is assigned to determine malicious activity associated with a **Pushdo Trojan** attack observed in a Security Onion environment.

The investigation begins with alerts and proceeds through host identification, exploit research, malware-file analysis, threat verification and final reporting.

## 2. Assessment Workflow

```text
Security Onion
      ↓
Verify monitoring services
      ↓
Sguil / Kibana
      ↓
Review alerts
      ↓
Establish attack timeframe
      ↓
Identify internal/external IPs
      ↓
Identify infected host
      ↓
Determine infection method
      ↓
Identify downloaded files
      ↓
Calculate SHA-256 hashes
      ↓
Threat-intelligence verification
      ↓
Correlate additional alerts
      ↓
Prepare findings report
```

## 3. Part 1 — Gather Basic Information

### 3.1 Verify Security Onion services

The analyst verifies that the required Security Onion services are operational before beginning the investigation.

**Evidence to attach:**

- Screenshot of the service-status output.
- Screenshot showing access to Sguil/Kibana.

### 3.2 Establish the attack timeframe

The Pushdo activity occurs on **27 June 2017**, with the observed attack window approximately **13:38:34–13:44:32 UTC**.

The exact displayed timestamps should be confirmed against the learner's own assessment evidence.

### 3.3 Identify related alerts and IP addresses

The analyst reviews the alerts generated during the relevant timeframe and identifies internal and external systems associated with the activity.

The investigation identifies the affected internal host as **192.168.1.96**. External communications include the DNS/service infrastructure visible in the assessment alerts.

**Evidence to attach:**

- Sguil alert list.
- Kibana alert view, if used.
- Relevant alert details.

## 4. Part 2 — Learn About the Exploit

### 4.1 Identify the infected host

The infected endpoint is identified as:

- **IP address:** `192.168.1.96`
- **MAC address:** `00-15-C5-DE-C7-3B`
- **NIC vendor:** Dell Inc.

NetworkMiner or equivalent host/network evidence can be used to establish the MAC address and vendor.

### 4.2 Determine infection time and method

The observed infection time is approximately:

**2017-06-27 13:38:32 UTC**

The investigation indicates that the host became infected after accessing a malicious domain. The Pushdo Trojan acted as a downloader, retrieving additional executable malware from attacker-controlled infrastructure.

### 4.3 Examine downloaded files

The investigation identifies three downloaded executable files associated with the incident:

- `gerv.gun`
- `trow.exe`
- `wp.exe`

The analyst obtains the files' SHA-256 hashes from the available Security Onion evidence and uses those hashes for threat verification.

## 5. Part 3 — Report Findings

The final report should explain:

1. Which host was compromised.
2. When the compromise occurred.
3. How the infection began.
4. Which alerts supported the conclusion.
5. Which files were downloaded.
6. How the files were verified as malicious.
7. What additional alerts were associated with the infected host.
8. The likely sequence of malicious activity.

## 6. Evidence Attachment Checklist

- [ ] Security Onion service-status screenshot
- [ ] Sguil/Kibana alert screenshot
- [ ] Attack timeframe screenshot
- [ ] Infected host IP/MAC screenshot
- [ ] NetworkMiner/host evidence
- [ ] Downloaded-file evidence
- [ ] SHA-256 evidence
- [ ] Malware-verification evidence
- [ ] Related-alert evidence
- [ ] Final investigation report

## 7. TESDA Evidence Domains

This assessment contributes primarily to:

- Monitoring and Alerts
- Log/Event Analysis
- Network Traffic Analysis
- Endpoint Analysis
- Malware/IOC Analysis
- Incident Investigation
- Threat Intelligence
- Reporting

## 8. Assessment Limitation

This assessment demonstrates investigation and reporting. It does not demonstrate actual host isolation, IOC blocking, eradication, system restoration, secondary scanning or recovery validation. Those activities will be demonstrated through supplementary NC II mitigation exercises.
