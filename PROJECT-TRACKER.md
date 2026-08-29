# Project Tracker — Cisco CyberOps → TESDA Cybersecurity Evidence Portfolio

**Project:** Cisco CyberOps Associate + BOTS v2 + supplementary cybersecurity simulations mapped to TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II

## Overall progress

| Phase | Deliverable | Status |
|---|---|---|
| **Phase 1** | Portfolio architecture and evidence strategy | ✅ Complete |
| **Phase 2** | Complete CyberOps Associate lab register in original sequence | 🟡 In progress — register populated; evidence verification pending |
| **Phase 3** | TESDA performance-criterion + master SAG mapping | ✅ Complete — master matrix established; criterion-level evidence verification continues during later phases |
| **Phase 4** | CyberOps v1.0 Skills Assessment evidence mapping | 🟢 Assessment performed; documentation created; actual artifact collection pending |
| **Phase 5** | Legacy assessment review and repository cleanup | ✅ Complete — obsolete legacy materials removed |
| **Phase 6** | BOTS v2 threat-hunting evidence mapping and setup | 🟢 Started — repository package created; lab execution/evidence capture pending |
| **Phase 7** | Supplementary containment/eradication/recovery lab | ⬜ Pending |
| **Phase 8** | Supplementary vulnerability scanning/management lab | ⬜ Pending |
| **Phase 9** | Evidence templates and individual lab evidence folders | ⬜ Pending |
| **Phase 10** | Integrated NC I/NC II capstone and final evidence index | ⬜ Pending |

## Phase 1 — COMPLETE

- Portfolio architecture established.
- Four TESDA core competencies established.
- Fixed 11 evidence domains established.
- CyberOps labs established as the primary technical evidence source.
- Skills Assessment, BOTS v2, and supplementary simulations positioned as additional evidence layers.

## Phase 2 — IN PROGRESS

### Completed

- Verified the current Cisco/NDG CyberOps Associate lab catalog.
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

### Remaining Phase 4 tasks

- [ ] Collect the user's actual v1.0 screenshots/artifacts.
- [ ] Replace placeholders with actual observed values where required.
- [ ] Link actual evidence artifacts to the master SAG matrix.
- [ ] Finalize the v1.0 RPL evidence package.

## Phase 5 — COMPLETE: Legacy Assessment Cleanup

The obsolete legacy assessment package was removed from the portfolio. The repository now retains the current CyberOps Associate lab pathway and the v1.0 assessment that the candidate actually performed.

### Actions completed

- Removed the legacy assessment evidence package.
- Removed its Markdown files and placeholder screenshot directory.
- Removed it from the assessment index and evidence architecture.
- Removed legacy-specific project tracking and findings.
- Kept the retained v1.0 Skills Assessment because it represents the assessment already performed for this portfolio.

## Phase 6 — BOTS v2

### Current status

**🟢 Setup started.**

The BOTS v2 evidence package now contains:

```text
assessments/botsv2/
├── README.md
├── setup.md
├── splunk-2-hunting-guide.md
├── evidence-mapping.md
├── screenshots/README.md
└── reports/botsv2-investigation-report.md
```

### Reference basis

The hunting guide is based on the supplied TryHackMe Splunk 2 reference and the linked jniket walkthrough. Explanatory material is paraphrased. SPL commands requested by the user are retained as written in the source material, including placeholder tokens and legacy typos.

The official BOTS v2 dataset documentation is the authoritative source for dataset installation and environment requirements.

### Completed

- Created BOTS v2 assessment directory.
- Created dataset/setup guide.
- Created paraphrased Splunk 2 hunting guide.
- Preserved source SPL commands without silently correcting them.
- Created TESDA/evidence-domain mapping.
- Created screenshot evidence standards.
- Created investigation-report template.

### Remaining

- [ ] Obtain/install the BOTS v2 dataset in the chosen controlled Splunk environment.
- [ ] Verify `index=botsv2 earliest=0` returns data.
- [ ] Run the sourcetype inventory query.
- [ ] Complete selected 100-series investigations.
- [ ] Complete selected 200-series investigations.
- [ ] Complete selected 300-series investigations.
- [ ] Complete selected 400-series investigations.
- [ ] Capture candidate-generated screenshots.
- [ ] Write investigation reports from actual results.
- [ ] Link the evidence to the master TESDA SAG matrix.

### Screenshot decision

The screenshots from the supplied Medium article are retained as **visual references only**. For RPL evidence, screenshots captured from the candidate's own BOTS v2 session are preferred and should be used unless the candidate has permission to reuse the original images.

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

**Set up the controlled BOTS v2 Splunk environment, verify the dataset, then begin the 100-series threat-hunting investigations and capture the candidate's own evidence.**
