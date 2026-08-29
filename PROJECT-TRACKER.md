# Project Tracker — Cisco CyberOps → TESDA Cybersecurity Evidence Portfolio

**Project:** Cisco CyberOps Associate + BOTS v2 + supplementary cybersecurity simulations mapped to TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II

## Overall progress

| Phase | Deliverable | Status |
|---|---|---|
| **Phase 1** | Portfolio architecture and evidence strategy | ✅ Complete |
| **Phase 2** | Complete CyberOps Associate lab register in original sequence | 🟡 In progress — register populated; evidence verification pending |
| **Phase 3** | TESDA performance-criterion + master SAG mapping | ✅ Complete — master matrix established; criterion-level evidence verification continues during later phases |
| **Phase 4** | CyberOps v1.0 Skills Assessment evidence mapping | 🟢 Assessment performed; documentation created; actual artifact collection pending |
| **Phase 5** | CyberOps v1.1 Skills Assessment evidence mapping | 🟡 In progress — documentation package created; actual artifact verification pending |
| **Phase 6** | BOTS v2 threat-hunting evidence mapping | ⬜ Pending |
| **Phase 7** | Supplementary containment/eradication/recovery lab | ⬜ Pending |
| **Phase 8** | Supplementary vulnerability scanning/management lab | ⬜ Pending |
| **Phase 9** | Evidence templates and individual lab evidence folders | ⬜ Pending |
| **Phase 10** | Integrated NC I/NC II capstone and final evidence index | ⬜ Pending |

## Phase 1 — COMPLETE

- Portfolio architecture established.
- Four TESDA core competencies established.
- Fixed 11 evidence domains established.
- CyberOps labs established as the primary technical evidence source.
- Skills Assessments, BOTS v2, and supplementary simulations positioned as additional evidence layers.

## Phase 2 — IN PROGRESS

### Completed

- Verified the current Cisco/NDG CyberOps Associate v1 lab catalog.
- Registered 36 hands-on labs in original sequence.
- Assigned primary and related evidence domains.
- Added preliminary NC I/NC II relevance and coverage ratings.
- Identified major evidence gaps.

### Remaining

- Verify against the exact course/VM version used for final submission.
- Confirm which labs have actually been completed.
- Record exact evidence artifacts for completed labs.
- Finalize Phase 2 register after evidence verification.

## Phase 3 — COMPLETE

### Completed

- Retrieved current TESDA TRs and confirmed the four core units.
- Built criterion-level mapping for ICT251312, ICT251313, ICT251314 and ICT251315.
- Created the master SAG evidence matrix.
- Identified workplace-process evidence gaps and supplementary-lab requirements.

### Key decisions

1. Direct technical evidence is not automatically proof of a complete TESDA competency.
2. Final SAG Yes/Partially/No decisions require actual evidence artifacts.
3. CyberOps labs remain the primary technical foundation.
4. Containment/recovery and vulnerability-management workflows require supplementary evidence.

## Phase 4 — IN PROGRESS: CyberOps v1.0 Skills Assessment

### Completed

- Verified the v1.0 assessment workflow from available copies of the Cisco assessment document.
- Confirmed the assessment is an alert-driven Pushdo Trojan investigation using Security Onion, Sguil/Kibana, web research and VirusTotal.
- Created task-level mapping to the evidence domains.
- Mapped the assessment to the strongest relevant TESDA competency areas.
- Created the v1.0 assessment documentation package.
- User has already performed the actual v1.0 Skills Assessment in the CyberOps VM.
- Published answers are treated only as a cross-check, not as portfolio evidence.

### v1.0 assessment documentation

```text
assessments/cyberops-v1.0/
├── assessment-overview.md
├── assessment-documentation.md
├── alert-analysis.md
├── incident-timeline.md
├── ioc-analysis.md
├── threat-intelligence.md
├── findings-report.md
└── screenshots/
```

### Remaining Phase 4 tasks

- [ ] Collect the user's actual v1.0 screenshots/artifacts.
- [ ] Replace placeholders with actual observed values where required.
- [ ] Link actual evidence artifacts to the master SAG matrix.
- [ ] Finalize the v1.0 RPL evidence package.

## Phase 5 — IN PROGRESS: CyberOps / CCNA Cybersecurity Operations v1.1 Skills Assessment

### Assessment basis

The v1.1 assessment is the legacy **CCNA Cybersecurity Operations v1.1 Skills Assessment** and is documented separately from the newer CyberOps Associate assessment. It uses the Security Onion environment and focuses on Sguil/Snort event evaluation, investigation pivots through ELSA, Bro/Zeek and Wireshark, and exploit intelligence research.

### Assessment scenario

The assessment investigates exploit-related activity associated with the **Angler Exploit Kit**, an affected internal host, an external exploit-delivery infrastructure, and a payload recovered from captured traffic.

### Documentation package created

```text
assessments/cyberops-v1.1/
├── assessment-overview.md
├── assessment-documentation.md
├── alert-analysis.md
├── incident-timeline.md
├── ioc-analysis.md
├── threat-intelligence.md
├── findings-report.md
└── screenshots/
```

### Key assessment findings documented

- Exploit kit: **Angler EK**
- Affected host: `192.168.0.12`
- Exploit-delivery IP: `192.99.198.158`
- Exploit-delivery domain: `qwe.mvdunalterableairreport.net`
- Extracted object: `3xdz3bcxc8`
- Vulnerable client condition: outdated Flash component

### Primary evidence domains

- 01 Monitoring and Alerts
- 02 Log/Event Analysis
- 03 Network Traffic Analysis
- 04 Endpoint Analysis
- 05 Malware/IOC Analysis
- 07 Incident Investigation
- 08 Threat Intelligence
- 11 Reporting

### TESDA relevance

The v1.1 assessment provides strong practical evidence for **ICT251312 — Monitor and Report Cyber Threats**, especially alert evaluation, event investigation, case follow-up, threat identification and reporting.

It provides supporting evidence for **ICT251314 — Perform Threat Mitigation**, especially incident evaluation, IOC identification, intelligence use and affected-system analysis.

It does not by itself demonstrate complete containment, eradication, recovery, secondary scanning or vulnerability-management processes.

### Remaining Phase 5 tasks

- [ ] Confirm whether the user has performed the v1.1 assessment.
- [ ] Collect actual v1.1 screenshots/artifacts if performed.
- [ ] Replace documentation placeholders with actual observed values.
- [ ] Verify the exact assessment version/environment used.
- [ ] Create task-level TESDA criterion mapping for v1.1.
- [ ] Link actual evidence to the master SAG matrix.

## Phase 6 — BOTS v2

Map selected BOTS v2 investigations to log analysis, threat intelligence, incident investigation and reporting criteria.

## Phase 7 — Containment / Eradication / Recovery

Build and document a controlled simulation covering:

`Detect → Investigate → Contain → Eradicate → Recover → Secondary Scan → Validate → Monitor → Report`

## Phase 8 — Vulnerability Scanning / Management

Build the dedicated ICT251315 simulation:

`Asset Inventory → Scope/Authorization → Schedule → Scanner Configuration → Scan → Analyze → Prioritize → Change Request/CAB → Remediate → Rescan → Validate → Report`

## Phase 9 — Evidence implementation

Populate the 11 evidence domains with actual artifacts and reusable evidence templates.

## Phase 10 — Final integration

Create the final TESDA evidence index, SAG evidence guide, and integrated capstone.

## Project rules

- Use actual performed-lab evidence only.
- Do not fabricate screenshots, logs, hashes, alerts, PCAPs, reports, or assessment results.
- Do not claim that completing a Cisco lab automatically equals a TESDA competency.
- Keep the 11 evidence domains separate from the four TESDA core competencies.
- Update this tracker at the end of each phase.

## Current next task

**Confirm/collect the user's actual v1.1 assessment evidence, then complete the task-level TESDA mapping before proceeding to Phase 6 — BOTS v2.**
