# Master TESDA SAG Evidence Matrix

## Purpose

This is the master cross-reference between the four TESDA Cyber Threat Monitoring NC I / Cyber Threat Mitigation NC II core competencies, the portfolio's 11 evidence domains, Cisco CyberOps Associate laboratory activities, the completed CyberOps v1.0 Skills Assessment, BOTS v2, and the controlled supplementary simulations still required to close evidence gaps.

**Important:** This matrix is an RPL/evidence-planning document, not a TESDA assessment result. Final competency decisions belong to the authorized TESDA assessment process.

## Controlled-environment and data-privacy statement

All cybersecurity activities represented by this portfolio are performed exclusively in **simulated, isolated, and controlled laboratory environments** using authorized training datasets, virtual machines, simulated network traffic, and designated training systems.

No production systems, live organizational networks, confidential company information, personally identifiable information, credentials, private keys, or real organizational security events are intentionally accessed, monitored, scanned, modified, contained, or recovered.

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
| 🟢 Direct | Existing controlled laboratory activity directly demonstrates the technical action; criterion-specific artifacts may still be required. |
| 🟡 Supporting | Activity demonstrates a related capability but needs another artifact or controlled simulation step. |
| 🔴 Gap | Existing evidence does not adequately demonstrate the requirement; a controlled supplementary simulation is required. |

---

# NC I — ICT251312 Monitor and Report Cyber Threats

| TESDA performance area | Evidence domain(s) | CyberOps / assessment evidence | BOTS v2 contribution | Additional evidence | Coverage |
|---|---|---|---|---|---|
| Check and assess detections/alerts | 01, 07 | Snort/Security Onion labs; v1.0 assessment | Investigation of simulated suspicious events | SOP/triage simulation record | 🟢/🟡 |
| Manual checking and verification | 02, 03, 04, 05, 07 | CyberOps log/network/endpoint/malware labs; v1.0 | 100–400 series simulated multi-source investigation | Investigation notes | 🟢 |
| Conduct case follow-up | 07, 08 | v1.0 simulated investigation | BOTS pivots and IOC enrichment | Simulated case/ticket artifact | 🟢/🟡 |
| Report threat activity | 11 | v1.0 findings/reporting | BOTS investigation report | Simulated TESDA-style report | 🟢/🟡 |
| Notify/escalate confirmed/high-priority threats | 11 | Technical findings | Findings suitable for simulated escalation | Simulated notification/escalation artifact | 🟡 |

### Interpretation

CyberOps and BOTS v2 provide strong technical evidence for detection analysis, verification, correlation and reporting within controlled training environments. Workplace-process elements such as SOP use, ticketing, escalation and stakeholder notification will be represented only through controlled simulations or training artifacts.

---

# NC I — ICT251313 Conduct Vulnerability Scanning of Assets

| TESDA performance area | Evidence domain(s) | Existing evidence | Additional controlled evidence | Coverage |
|---|---|---|---|---|
| Check schedule and scope | 06, 11 | Limited | Simulated scan calendar, scope and authorization | 🔴 |
| Identify assets and priorities | 06 | Nmap/asset-discovery foundation; BOTS web-server analysis | Simulated asset list and prioritization | 🟡 |
| Conduct authorized scanning | 06 | CyberOps Nmap activity; BOTS 200-Series scanning investigation | Complete isolated scanning simulation | 🟢/🟡 |
| Follow NIST 800-115-based procedure | 06 | Technical scanning foundation | Controlled procedure/checklist | 🟡 |
| Monitor scanning impact / handle failed scans | 06, 11 | Limited | Simulated resource-monitoring and failed-scan record | 🔴 |
| Provide scan report | 06, 11 | Lab outputs | Formal simulated vulnerability-scan report | 🟡 |

**Boundary:** All scanning activities in this portfolio must target only explicitly authorized laboratory assets. No live organizational or third-party production systems are to be scanned.

---

# NC II — ICT251314 Perform Threat Mitigation

| TESDA performance area | Evidence domain(s) | Existing evidence | Required controlled supplementary evidence | Coverage |
|---|---|---|---|---|
| Validate and classify incidents | 01, 02, 07 | v1.0; CyberOps investigations; BOTS v2 | Simulated incident classification/prioritization record | 🟢/🟡 |
| Prioritize incident criticality | 07, 11 | Investigation findings | Simulated severity/impact matrix | 🟡 |
| Use CTI to identify TTPs | 05, 08 | CyberOps malware/IOC labs; v1.0; BOTS v2 | Formal simulated CTI/TTP mapping | 🟢 |
| Analyze affected processes/configurations | 04, 05, 07 | Endpoint/process/malware labs; BOTS 300/400 | Controlled host-analysis report where required | 🟢 |
| Enrich/counter-check IOCs | 05, 08 | Hashing, VirusTotal and BOTS evidence | IOC worksheet | 🟢 |
| Contain threat | 09 | Limited existing evidence | Isolated containment simulation | 🔴 |
| Eradicate/remove malicious artifacts | 09 | Limited existing evidence | Isolated eradication simulation | 🔴 |
| Recover/rollback system or infrastructure | 10 | No complete existing evidence | Last-known-good image/configuration recovery simulation | 🔴 |
| Remove/verify malicious IOCs | 05, 09, 10 | IOC analysis | Post-eradication validation in isolated lab | 🟡 |
| Secondary scan | 06, 10 | Nmap/scanning foundation | Post-recovery isolated security scan | 🟡 |
| Continuous monitoring after mitigation | 01, 10 | Monitoring labs | Controlled recovery-monitoring record | 🟡 |
| Document mitigation/report | 11 | Assessment and lab reporting | Simulated incident-response report | 🟢/🟡 |

### Interpretation

The strongest existing evidence is **investigation + IOC/CTI + affected-system analysis**. BOTS v2 strengthens this portion but does not itself perform containment, eradication, recovery or secondary validation. Those will be demonstrated only through controlled supplementary simulations.

---

# NC II — ICT251315 Perform Vulnerability Management/Control

| TESDA performance area | Evidence domain(s) | Existing evidence | Required controlled supplementary evidence | Coverage |
|---|---|---|---|---|
| Install/configure vulnerability-management product/agent | 06 | Limited | Scanner/agent installation simulation | 🔴 |
| Maintain vulnerability asset inventory | 06, 11 | Nmap discovery | Simulated asset inventory/classification workflow | 🟡 |
| Set scanning schedule | 06, 11 | Limited | Simulated scheduled-scan plan | 🔴 |
| Audit servers/endpoints/applications | 04, 06 | Endpoint/network labs | Controlled audit checklist | 🟡 |
| Perform VM change/configuration management | 06, 11 | Limited | Simulated change request/CAB workflow | 🔴 |
| Perform patch/remediation testing | 06, 10 | Limited | Isolated patch/remediation simulation | 🔴 |
| Rescan and verify remediation | 06, 10 | Nmap foundation | Before/after isolated scan comparison | 🟡 |
| Report VM results | 11 | Lab reporting | Formal simulated VM report/dashboard | 🟡 |

### Boundary

The vulnerability-management workflow must use only designated laboratory assets. It must never be performed against a live organizational environment as part of this portfolio.

---

# Evidence-source strategy

| Evidence source | Best role in the portfolio |
|---|---|
| **CyberOps Associate labs** | Primary technical foundation across the 11 evidence domains |
| **CyberOps v1.0 Skills Assessment** | Integrated alert-driven simulated investigation |
| **BOTS v2** | Independent simulated SIEM investigation, threat hunting, IOC enrichment and multi-source correlation |
| **Controlled containment/recovery simulation** | NC II operational mitigation evidence |
| **Controlled vulnerability-scanning simulation** | NC I scanning workflow evidence |
| **Controlled vulnerability-management simulation** | NC II VM/control evidence |

---

# No live-production capstone

The portfolio intentionally does **not** include a live-production capstone. The evidence package is built from:

```text
CyberOps Associate laboratory activities
            +
CyberOps v1.0 Skills Assessment
            +
BOTS v2 simulated investigations
            +
Controlled supplementary simulations
            ↓
TESDA Evidence Package
```

This structure provides observable evidence without requiring access to, monitoring of, scanning of, or modification of a company's production environment.

---

# SAG evidence decision model

For every SAG item, the final portfolio review will use:

```text
TESDA SAG / Performance Criterion
            ↓
What exactly must be demonstrated?
            ↓
Existing CyberOps laboratory evidence
            ↓
CyberOps v1.0 / BOTS v2 evidence
            ↓
Controlled supplementary simulation if required
            ↓
Artifact checklist
            ↓
YES / PARTIALLY / NO
```

A **YES** recommendation should only be made when the repository contains observable evidence for the required action. A related course or lab title alone is insufficient.

# Current conclusion

The portfolio uses three principal practical evidence layers:

1. **CyberOps Associate labs** — technical skills foundation;
2. **CyberOps v1.0 Skills Assessment** — integrated simulated alert-driven investigation;
3. **BOTS v2** — independent simulated SIEM/threat-hunting and multi-source investigation.

Controlled supplementary simulations are reserved for the remaining operational gaps:

- containment;
- eradication;
- recovery/rollback;
- secondary validation scan;
- vulnerability scanning workflow;
- vulnerability-management/control lifecycle.

This architecture keeps the portfolio evidence-based while maintaining a strict simulated, isolated, controlled, and privacy-conscious environment.
