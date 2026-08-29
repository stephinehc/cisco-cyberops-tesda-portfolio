# Project Tracker — Cisco CyberOps → TESDA Cybersecurity Evidence Portfolio

**Project:** Cisco CyberOps Associate + BOTS v2 + supplementary cybersecurity simulations mapped to TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II

## Overall progress

| Phase | Deliverable | Status |
|---|---|---|
| **Phase 1** | Portfolio architecture and evidence strategy | ✅ Complete |
| **Phase 2** | Complete CyberOps Associate lab register in original sequence | 🟡 In progress — register populated |
| **Phase 3** | TESDA performance-criterion mapping | 🟡 In progress |
| **Phase 4** | CyberOps v1.0 Skills Assessment evidence mapping | ⬜ Pending |
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

## Phase 3 — IN PROGRESS

### Objective

Map CyberOps lab evidence to the **exact TESDA performance criteria and evidence requirements**, not merely to competency titles.

### Source standard

Use the current TESDA Training Regulations for:

- **Cyber Threat Monitoring NC I — ICT251312 Monitor and report cyber threats**
- **Cyber Threat Monitoring NC I — ICT251313 Conduct vulnerability scanning of assets**
- **Cyber Threat Mitigation NC II — ICT251314 Perform threat mitigation**
- **Cyber Threat Mitigation NC II — ICT251315 Perform vulnerability management/control**

### Completed Phase 3 work

- Retrieved the current TESDA TRs.
- Confirmed the four core unit codes.
- Extracted the performance-criteria structure for ICT251312, ICT251313 and ICT251314.
- Started the master performance-criteria matrix.
- Mapped the strongest existing CyberOps labs to individual criteria.
- Identified criteria requiring SOP, ticketing, stakeholder, CTI, containment/recovery, and vulnerability-management wrappers.

### Phase 3 deliverable

`tesda-mapping/phase-3-performance-criteria-matrix.md`

### Key decisions

1. **Direct evidence is not the same as complete TESDA competency.** A lab can directly demonstrate a technical action while still requiring workplace-process evidence.
2. **SAG answers must be evidence-backed.** We will recommend “Yes/Partially/No” only after checking whether the portfolio contains evidence for the relevant criterion.
3. **CyberOps is strongest for technical monitoring/investigation.** SOP, ticket, stakeholder communication, containment/recovery, and vulnerability-management process evidence must be added where missing.
4. **NC II containment/recovery is a confirmed gap** until the dedicated simulation is completed.
5. **NC II vulnerability management/control is a confirmed gap** until the dedicated VM/remediation workflow is completed.

## Phase 4 — CyberOps v1.0 Skills Assessment

Map every v1.0 task to the 11 evidence domains and exact TESDA criteria. Treat it as high-value alert-driven SOC evidence.

## Phase 5 — CyberOps v1.1 Skills Assessment

Map the actual v1.1 tasks individually. Do not assume equivalence to v1.0.

## Phase 6 — BOTS v2

Map selected BOTS v2 investigations to log analysis, threat intelligence, incident investigation and reporting criteria.

## Phase 7 — Containment / Eradication / Recovery

Build and document a controlled simulation covering:

`Detect → Investigate → Contain → Eradicate → Recover → Secondary Scan → Validate → Monitor → Report`

## Phase 8 — Vulnerability Scanning / Management

Extend Nmap into:

`Asset Inventory → Scope/Authorization → Schedule → Scan → Analyze → Prioritize → Remediate → Rescan → Validate → Report`

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

Continue Phase 3 by completing the criterion-level mapping for **ICT251315 Perform vulnerability management/control**, then consolidate the four core units into the final SAG evidence matrix.