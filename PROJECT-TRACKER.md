# Project Tracker — Cisco CyberOps → TESDA Cybersecurity Evidence Portfolio

**Project:** Cisco CyberOps Associate + BOTS v2 + supplementary cybersecurity simulations mapped to TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II

## Overall progress

| Phase | Deliverable | Status |
|---|---|---|
| **Phase 1** | Portfolio architecture and evidence strategy | ✅ Complete |
| **Phase 2** | Complete CyberOps Associate lab register in original sequence | 🟡 In progress — register populated |
| **Phase 3** | TESDA performance-criterion mapping | ⬜ Pending |
| **Phase 4** | CyberOps v1.0 Skills Assessment evidence mapping | ⬜ Pending |
| **Phase 5** | CyberOps v1.1 Skills Assessment evidence mapping | ⬜ Pending |
| **Phase 6** | BOTS v2 threat-hunting evidence mapping | ⬜ Pending |
| **Phase 7** | Supplementary containment/eradication/recovery lab | ⬜ Pending |
| **Phase 8** | Supplementary vulnerability scanning/management lab | ⬜ Pending |
| **Phase 9** | Evidence templates and individual lab evidence folders | ⬜ Pending |
| **Phase 10** | Integrated NC I/NC II capstone and final evidence index | ⬜ Pending |

## Phase 1 — COMPLETE

### Completed

- Defined the four TESDA target core competencies.
- Established the fixed 11 evidence-domain structure.
- Confirmed that **CyberOps Associate laboratory activities are the primary technical evidence source**.
- Positioned CyberOps v1.0/v1.1 Skills Assessments as higher-level assessment activities.
- Positioned BOTS v2 as independent SIEM/threat-hunting evidence.
- Identified containment, recovery, and vulnerability-management gaps requiring supplementary activities.
- Added the Phase 1 coverage summary and evidence architecture.

### Fixed evidence domains

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

## Phase 2 — IN PROGRESS

### Completed in this phase

- Verified the current Cisco/NDG CyberOps Associate v1 lab catalog.
- Registered **36 hands-on labs** in the original Cisco sequence.
- Kept the Skills-Based Assessment separate from the ordinary lab register for later v1.0/v1.1 mapping.
- Assigned a **primary evidence domain** to every hands-on lab.
- Assigned related evidence domains where appropriate.
- Added preliminary NC I / NC II relevance.
- Added preliminary Direct / Supporting / Gap ratings.
- Identified high-value labs for monitoring, vulnerability scanning, threat mitigation, and investigation.
- Documented the major gaps that require supplementary activities.

### Current Phase 2 status

- [x] Establish lab-register format
- [x] Lock 11 evidence domains
- [x] Verify current Cisco/NDG lab sequence
- [x] Document 36 hands-on CyberOps labs
- [x] Assign primary evidence domain to every lab
- [x] Assign related evidence domains
- [x] Record preliminary NC I relevance
- [x] Record preliminary NC II relevance
- [x] Record preliminary coverage rating
- [x] Identify major evidence gaps
- [ ] Verify against the exact course/VM version used for final submission
- [ ] Confirm which labs have actually been completed
- [ ] Record exact evidence artifacts to capture for each completed lab
- [ ] Finalize Phase 2 register

### Key Phase 2 decisions

1. The **11 evidence domains remain fixed** and are not renamed to match TESDA competency titles.
2. The **Cisco lab sequence remains intact**; classification does not reorder the course.
3. Each lab gets one primary domain and may have related domains.
4. TESDA criterion-level mapping is deliberately deferred to Phase 3.
5. CyberOps v1.0/v1.1 Skills Assessments are separate assessment evidence and will not be mixed into the ordinary lab sequence.
6. BOTS v2 remains a separate threat-hunting evidence source.
7. Containment, eradication, recovery, and full vulnerability-management workflows remain supplementary requirements unless actual lab evidence later proves otherwise.

## Phase 3 — TESDA performance-criterion mapping

After Phase 2, map the relevant CyberOps activities to the **specific TESDA performance criteria**, rather than mapping only at the competency-title level.

Deliverables:

- NC I criterion matrix
- NC II criterion matrix
- Lab-to-criterion cross-reference
- Direct/Supporting/Gap assessment
- SAG evidence recommendations

## Phase 4 — CyberOps v1.0 Skills Assessment

Document the v1.0 Skills Assessment as an alert-driven investigation and map each task to the applicable evidence domains and TESDA criteria.

Primary expected role:

> **NC I Monitor and Report Cyber Threats capstone evidence**

## Phase 5 — CyberOps v1.1 Skills Assessment

Document the actual v1.1 assessment tasks and map them individually. Do not assume v1.1 is equivalent to v1.0 or automatically satisfies NC II.

Primary expected role:

> **Advanced investigation/analysis evidence**

## Phase 6 — BOTS v2

Map selected BOTS v2 scenarios/questions to the evidence domains and TESDA criteria.

Primary expected role:

> **Independent SIEM investigation and threat hunting**

## Phase 7 — Containment / Eradication / Recovery

Create a controlled simulation that closes the major NC II mitigation gap.

Expected workflow:

```text
Detect → Investigate → Confirm → Contain → Preserve Evidence
→ Eradicate → Recover → Secondary Scan → Validate → Monitor → Report
```

## Phase 8 — Vulnerability Scanning / Management

Create supplementary activities that extend the CyberOps Nmap activity into a complete TESDA-oriented workflow:

```text
Asset Inventory → Scope/Authorization → Scan → Analyze
→ Prioritize → Remediate → Rescan → Validate → Report
```

## Phase 9 — Evidence implementation

Create reusable evidence templates and populate the 11 evidence-domain folders with actual lab results.

No fabricated evidence is permitted.

## Phase 10 — Final integration

Create the integrated evidence index and capstone showing how the complete portfolio supports the four TESDA core competencies.

## Project rules

- Use actual performed-lab evidence only.
- Do not fabricate screenshots, logs, hashes, alerts, PCAPs, reports, or assessment results.
- Do not claim that completing a Cisco lab automatically equals a TESDA competency.
- Keep the 11 evidence domains separate from the four TESDA core competencies.
- Update this tracker at the end of each phase.

## Next immediate task

**Phase 3: map the registered CyberOps labs to the exact TESDA performance criteria and SAG evidence requirements for NC I and NC II.**