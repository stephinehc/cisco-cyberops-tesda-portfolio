# Master TESDA SAG Evidence Matrix

## Purpose

This is the master cross-reference between the four TESDA Cyber Threat Monitoring NC I / Cyber Threat Mitigation NC II core competencies, the portfolio's 11 evidence domains, Cisco CyberOps Associate laboratory activities, the completed CyberOps v1.0 Skills Assessment, BOTS v2, and the supplementary activities still required to close evidence gaps.

**Important:** This matrix is an RPL/evidence-planning document, not a TESDA assessment result. Final competency decisions belong to the authorized TESDA assessment process.

## Evidence-domain structure

```text
01-monitoring-and-alerts/
02-log-event-analysis/
03-network-traffic-analysis/
04-endpoint-analysis/
05-malware-ioc-analysis/
06-vulnerability-scanning/
07-incident-investigation/
08-threat-intelligence/
09-containment/
10-recovery/
11-reporting/
```

## Rating key

| Rating | Meaning |
|---|---|
| 🟢 Direct | Existing activity directly demonstrates the technical action; criterion-specific artifacts still need to be captured where required. |
| 🟡 Supporting | Activity contributes useful evidence but needs an additional process, artifact, or practical step. |
| 🔴 Gap | Existing evidence does not adequately demonstrate the requirement; supplementary activity is required. |

---

# NC I — ICT251312 Monitor and Report Cyber Threats

TESDA defines this unit around checking alerts, checking third-party security solutions, manual checking/verification, case follow-up, and alert reporting. citeturn4view0turn4view1

| TESDA performance area | Evidence domain(s) | CyberOps / assessment evidence | BOTS v2 contribution | Additional evidence | Coverage |
|---|---|---|---|---|---|
| Check and assess detections/alerts | 01, 07 | Snort/Security Onion labs; v1.0 Pushdo assessment | Investigation of suspicious events | SOP/triage record | 🟢/🟡 |
| Manual checking and verification | 02, 03, 04, 05, 07 | CyberOps log/network/endpoint/malware labs; v1.0 | 100–400 series multi-source investigation | Investigation notes | 🟢 |
| Conduct case follow-up | 07, 08 | v1.0 investigation | BOTS pivots and IOC enrichment | Case/ticket artifact | 🟢/🟡 |
| Report threat activity | 11 | v1.0 findings/reporting | BOTS investigation report | TESDA-style stakeholder report | 🟢/🟡 |
| Notify/escalate confirmed/high-priority threats | 11 | Technical findings | Findings suitable for escalation | Notification/escalation artifact | 🟡 |

### Interpretation

CyberOps and BOTS v2 provide strong technical evidence for detection analysis, verification, correlation and reporting. The main remaining evidence is workplace-process evidence such as SOP use, ticketing, escalation and stakeholder notification where required by the criterion. TESDA permits portfolio with interview as an assessment method for ICT251312. citeturn4view1

---

# NC I — ICT251313 Conduct Vulnerability Scanning of Assets

TESDA requires checking the scan schedule, identifying the assets in scope, signed scope of work, verification with supervisor/change manager, adherence to schedule, scanning using industry standards including NIST SP 800-115, monitoring scan impact, handling scan problems, and providing scan reports. citeturn4view1

| TESDA performance area | Evidence domain(s) | Existing evidence | Additional evidence | Coverage |
|---|---|---|---|---|
| Check schedule and scope | 06, 11 | Limited | Scan calendar, scope and authorization | 🔴 |
| Identify assets and priorities | 06 | Nmap/asset-discovery foundation; BOTS web-server analysis | Asset list and prioritization | 🟡 |
| Conduct authorized scanning | 06 | CyberOps Nmap activity; BOTS 200-Series scanning investigation | Complete scanning practical | 🟢/🟡 |
| Follow NIST 800-115-based procedure | 06 | Technical scanning foundation | Procedure/checklist | 🟡 |
| Monitor scanning impact / handle failed scans | 06, 11 | Limited | Resource-monitoring and failed-scan record | 🔴 |
| Provide scan report | 06, 11 | Lab outputs | Formal vulnerability-scan report | 🟡 |

---

# NC II — ICT251314 Perform Threat Mitigation

TESDA defines this unit around incident evaluation, CTI/TTP analysis, affected-system analysis, and containment/recovery strategy. citeturn4view2

| TESDA performance area | Evidence domain(s) | Existing evidence | Required supplementary evidence | Coverage |
|---|---|---|---|---|
| Validate and classify incidents | 01, 02, 07 | v1.0 Pushdo; CyberOps investigations; BOTS v2 | Incident classification/prioritization record | 🟢/🟡 |
| Prioritize incident criticality | 07, 11 | Investigation findings | Severity/impact matrix | 🟡 |
| Use CTI to identify TTPs | 05, 08 | CyberOps malware/IOC labs; v1.0; BOTS v2 | Formal CTI/TTP mapping | 🟢 |
| Analyze affected processes/configurations | 04, 05, 07 | Endpoint/process/malware labs; BOTS 300/400 | Host-analysis report where required | 🟢 |
| Enrich/counter-check IOCs | 05, 08 | Hashing, VirusTotal and BOTS evidence | IOC worksheet | 🟢 |
| Contain threat | 09 | Limited existing evidence | Dedicated containment practical | 🔴 |
| Eradicate/remove malicious artifacts | 09 | Limited existing evidence | Eradication practical | 🔴 |
| Recover/rollback system or infrastructure | 10 | No complete existing evidence | Last-known-good image/configuration recovery practical | 🔴 |
| Remove/verify malicious IOCs | 05, 09, 10 | IOC analysis | Post-eradication validation | 🟡 |
| Secondary scan | 06, 10 | Nmap/scanning foundation | Post-recovery security scan | 🟡 |
| Continuous monitoring after mitigation | 01, 10 | Monitoring labs | Recovery monitoring record | 🟡 |
| Document mitigation/report | 11 | Assessment and lab reporting | Full incident response report | 🟢/🟡 |

TESDA's performance criteria include continuous monitoring, recovery from a last-known-good image/configuration/backup, rollback, removal of malicious IOCs/files/registry entries, and a secondary scan. citeturn4view3

### Interpretation

The strongest existing evidence is **investigation + IOC/CTI + affected-system analysis**. BOTS v2 substantially strengthens this portion but does not perform containment, eradication, recovery or secondary validation. Those remain dedicated supplementary practicals.

---

# NC II — ICT251315 Perform Vulnerability Management/Control

TESDA covers vulnerability-management software/agent installation, asset inventory/control, scanning schedules, audits, change/configuration management, and patch/remediation testing and reporting. citeturn4view3

| TESDA performance area | Evidence domain(s) | Existing evidence | Required supplementary evidence | Coverage |
|---|---|---|---|---|
| Install/configure vulnerability-management product/agent | 06 | Limited | Scanner/agent installation practical | 🔴 |
| Maintain vulnerability asset inventory | 06, 11 | Nmap discovery | Asset inventory/classification workflow | 🟡 |
| Set scanning schedule | 06, 11 | Limited | Scheduled-scan plan | 🔴 |
| Audit servers/endpoints/applications | 04, 06 | Endpoint/network labs | Structured audit checklist | 🟡 |
| Perform VM change/configuration management | 06, 11 | Limited | Change request/CAB simulation | 🔴 |
| Perform patch/remediation testing | 06, 10 | Limited | Patch/remediation practical | 🔴 |
| Rescan and verify remediation | 06, 10 | Nmap foundation | Before/after scan comparison | 🟡 |
| Report VM results | 11 | Lab reporting | Formal VM report/dashboard | 🟡 |

### Interpretation

BOTS v2 contributes useful vulnerability-analysis context through its 200-Series investigation, but it is not a substitute for the complete vulnerability-management lifecycle. A dedicated VM/remediation practical remains necessary.

---

# Evidence-source strategy

| Evidence source | Best role in the portfolio |
|---|---|
| **CyberOps Associate labs** | Primary technical foundation across the 11 evidence domains |
| **CyberOps v1.0 Skills Assessment** | Integrated alert-driven investigation and strong NC I/NC II investigation evidence |
| **BOTS v2** | Independent SIEM investigation, threat hunting, IOC enrichment and multi-source correlation |
| **Containment/Recovery simulation** | NC II operational mitigation evidence |
| **Vulnerability-scanning practical** | NC I scanning workflow evidence |
| **Vulnerability-management/remediation practical** | NC II VM/control evidence |

---

# BOTS v2 evidence package

The detailed BOTS v2 mapping is maintained separately in:

`tesda-mapping/botsv2-tesda-evidence-matrix.md`

It maps the 100–400 Series questions, the 42 uploaded screenshots, SPL-based investigation steps, evidence domains, and TESDA core-competency relevance.

---

# SAG evidence decision model

For every SAG item, the final portfolio review will use:

```text
TESDA SAG / Performance Criterion
            ↓
What exactly must be demonstrated?
            ↓
Existing CyberOps lab evidence
            ↓
CyberOps v1.0 / BOTS v2 evidence
            ↓
Supplementary evidence if required
            ↓
Artifact checklist
            ↓
YES / PARTIALLY / NO
```

A **YES** recommendation should only be made when the repository contains observable evidence for the required action, not merely a related course/lab title.

# Current conclusion

The portfolio now uses three principal practical evidence layers:

1. **CyberOps Associate labs** — technical skills foundation;
2. **CyberOps v1.0 Skills Assessment** — integrated alert-driven investigation;
3. **BOTS v2** — independent SIEM/threat-hunting and multi-source investigation.

The remaining operational gaps are deliberately separated into supplementary practicals rather than being overclaimed from existing activities:

- containment;
- eradication;
- recovery/rollback;
- secondary validation scan;
- vulnerability scanning workflow;
- vulnerability-management/control lifecycle.

This architecture is intended to make the eventual SAG responses evidence-based and auditable.
