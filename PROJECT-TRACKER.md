# Project Tracker — Cisco CyberOps → TESDA Cybersecurity Evidence Portfolio

**Project:** Cisco CyberOps Associate + BOTS v2 + supplementary cybersecurity simulations mapped to TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II

## Overall progress

| Phase | Deliverable | Status |
|---|---|---|
| **Phase 1** | Portfolio architecture and evidence strategy | ✅ Complete |
| **Phase 2** | Complete CyberOps Associate lab register in original sequence | 🟡 In progress — register populated; evidence verification pending |
| **Phase 3** | TESDA performance-criterion + master SAG mapping | ✅ Complete — master matrix established; criterion-level evidence verification continues during later phases |
| **Phase 4** | CyberOps v1.0 Skills Assessment evidence mapping | 🟡 In progress — task-level mapping complete; practical evidence capture pending |
| **Phase 5** | CyberOps v1.1 Skills Assessment evidence mapping | ⬜ Pending |
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
- Confirmed the assessment is an **alert-driven Pushdo Trojan investigation** using Security Onion, Sguil/Kibana, web research and VirusTotal. citeturn0search0turn0search3
- Created task-level mapping to all 11 evidence domains.
- Mapped the assessment to the strongest relevant TESDA competency areas.
- Identified direct evidence, supporting evidence and gaps.
- Defined the evidence package that must be captured during the user's actual assessment run.

### Phase 4 deliverable

- `tesda-mapping/cyberops-v1.0-skills-assessment-mapping.md`

### Core finding

The v1.0 Skills Assessment is especially strong for **ICT251312 — Monitor and Report Cyber Threats** because the candidate begins with existing Security Onion alerts and performs alert review, investigation, IOC/malware analysis, threat-intelligence verification, related-alert correlation and reporting. citeturn0search0turn0search11

It also provides strong **partial evidence for ICT251314 — Perform Threat Mitigation**, particularly incident analysis, IOC identification, threat intelligence and reporting. It does **not** by itself demonstrate containment, eradication, recovery or secondary scanning.

### v1.0 11-domain mapping status

| Domain | Status |
|---|---|
| 01 Monitoring and Alerts | 🟢 Strong |
| 02 Log/Event Analysis | 🟡 Supporting |
| 03 Network Traffic Analysis | 🟡 Supporting/Direct for specific indicators |
| 04 Endpoint Analysis | 🟢 Strong |
| 05 Malware/IOC Analysis | 🟢 Strong |
| 06 Vulnerability Scanning | 🔴 Not demonstrated |
| 07 Incident Investigation | 🟢 Strong |
| 08 Threat Intelligence | 🟢 Strong |
| 09 Containment | 🔴 Gap |
| 10 Recovery | 🔴 Gap |
| 11 Reporting | 🟢 Strong |

### Remaining Phase 4 tasks

- [ ] Perform the actual v1.0 Skills Assessment in the user's CyberOps VM.
- [ ] Capture real screenshots and command outputs.
- [ ] Record alert/timeframe/IP/host findings.
- [ ] Record malicious file and SHA-256 evidence.
- [ ] Record VirusTotal enrichment evidence.
- [ ] Correlate related alerts.
- [ ] Produce the final investigation report.
- [ ] Link actual evidence artifacts to the master SAG matrix.

**Do not fabricate or pre-fill assessment results.** The repository contains the mapping and evidence checklist now; actual results will be added only after the assessment is performed.

## Phase 5 — CyberOps v1.1 Skills Assessment

Map the actual v1.1 tasks individually. Do not assume equivalence to v1.0.

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

Finish the practical v1.0 evidence capture, then proceed to **Phase 5 — CyberOps v1.1 Skills Assessment mapping**.
