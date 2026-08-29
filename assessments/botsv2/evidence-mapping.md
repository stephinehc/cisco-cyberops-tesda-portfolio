# BOTS v2 → TESDA Evidence Mapping

## Purpose

BOTS v2 is used as independent SIEM threat-hunting evidence. The mapping below separates what the activity can directly demonstrate from what still requires supplementary practical evidence.

## Evidence-domain mapping

| BOTS v2 activity | Primary domain | Related domains | Evidence strength |
|---|---|---|---|
| Sourcetype inventory / metadata review | 02 Log/Event Analysis | 01 Monitoring and Alerts | 🟢 Supporting |
| Amber IP identification | 02 Log/Event Analysis | 07 Incident Investigation | 🟢 Direct |
| HTTP competitor-site investigation | 03 Network Traffic Analysis | 07 Incident Investigation, 08 Threat Intelligence | 🟢 Direct |
| SMTP correlation | 02 Log/Event Analysis | 07 Incident Investigation, 08 Threat Intelligence | 🟢 Direct |
| Tor installation investigation | 04 Endpoint Analysis | 07 Incident Investigation | 🟢 Direct |
| Web vulnerability scanning investigation | 07 Incident Investigation | 03 Network Traffic Analysis, 06 Vulnerability Scanning | 🟢 Supporting |
| SQL/XSS investigation | 03 Network Traffic Analysis | 05 Malware/IOC Analysis, 07 Incident Investigation | 🟢 Direct |
| Mallory endpoint investigation | 04 Endpoint Analysis | 02 Log/Event Analysis, 07 Incident Investigation | 🟢 Direct |
| osquery / USB investigation | 04 Endpoint Analysis | 05 Malware/IOC Analysis, 07 Incident Investigation | 🟢 Direct |
| Spearphishing / SMTP investigation | 02 Log/Event Analysis | 05 Malware/IOC Analysis, 07 Incident Investigation, 08 Threat Intelligence | 🟢 Direct |
| FTP transfer investigation | 03 Network Traffic Analysis | 05 Malware/IOC Analysis, 07 Incident Investigation | 🟢 Direct |
| Malware execution correlation | 05 Malware/IOC Analysis | 04 Endpoint Analysis, 07 Incident Investigation, 08 Threat Intelligence | 🟢 Direct |
| Scheduled-task investigation | 04 Endpoint Analysis | 07 Incident Investigation, 05 Malware/IOC Analysis | 🟢 Direct |
| Final hunting report | 11 Reporting | 07 Incident Investigation, 08 Threat Intelligence | 🟢 Direct |

## TESDA core-competency relevance

### ICT251312 — Monitor and Report Cyber Threats

BOTS v2 provides strong evidence for:

- reviewing security telemetry;
- selecting appropriate log/data sources;
- searching and filtering events;
- correlating multiple event sources;
- identifying suspicious activity;
- documenting findings;
- reporting investigation results.

**Overall BOTS v2 contribution:** 🟢 Strong supporting/direct evidence, subject to the actual artifacts produced.

### ICT251313 — Conduct Vulnerability Scanning of Assets

BOTS v2 contains evidence of historical vulnerability-scanning activity, but that is not equivalent to personally performing an authorized vulnerability scan. The portfolio will therefore treat this as contextual/supporting evidence only.

**Overall contribution:** 🟡 Supporting/context only.

The dedicated vulnerability-management simulation remains necessary.

### ICT251314 — Perform Threat Mitigation

BOTS v2 is strong for the investigation side of mitigation:

- identify suspicious activity;
- identify affected users/hosts;
- correlate indicators;
- investigate attack behavior;
- analyze malware-related evidence;
- use threat intelligence to enrich findings;
- document incident findings.

However, BOTS v2 does not automatically prove that the candidate personally executed containment, eradication, recovery, or secondary scanning.

**Overall contribution:** 🟢 Strong investigation evidence + 🔴 gap for full remediation lifecycle.

### ICT251315 — Perform Vulnerability Management/Control

BOTS v2 can support understanding of vulnerability-related events and attacker behavior, but it is not a substitute for an end-to-end vulnerability-management process.

**Overall contribution:** 🟡 Supporting only.

## Recommended TESDA evidence statement

> BOTS v2 demonstrates the candidate's ability to use a SIEM to search, filter, correlate, investigate, validate, and report security events across multiple telemetry sources. It is used as independent threat-hunting evidence supporting monitoring, investigation, IOC analysis, threat intelligence, and reporting. Separate practical evidence is maintained for containment, eradication, recovery, vulnerability scanning, and vulnerability management.

## Evidence artifacts to collect

```text
assessments/botsv2/
├── README.md
├── setup.md
├── splunk-2-hunting-guide.md
├── evidence-mapping.md
├── screenshots/
│   ├── 01-sourcetype-inventory.png
│   ├── 02-amber-ip-identification.png
│   ├── 03-http-investigation.png
│   ├── 04-smtp-correlation.png
│   ├── 05-tor-investigation.png
│   ├── 06-web-scan-investigation.png
│   ├── 07-xss-investigation.png
│   ├── 08-mallory-endpoint.png
│   ├── 09-osquery-usb.png
│   ├── 10-spearphishing.png
│   ├── 11-ftp-investigation.png
│   ├── 12-malware-correlation.png
│   └── 13-scheduled-task.png
└── reports/
    └── botsv2-investigation-report.md
```

The screenshot names are evidence placeholders. Only files actually captured from the candidate's own BOTS v2 session should be committed.
