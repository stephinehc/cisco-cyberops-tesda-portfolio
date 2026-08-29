# Phase 2 — Cisco CyberOps Associate Lab Register and Individual Evidence Framework

**Status:** 🟢 Documentation framework complete; candidate evidence collection pending

## Objective

Document the **36 Cisco CyberOps Associate v1.0 laboratory activities selected in the master register**, classify each against the portfolio's fixed 11 evidence domains, and provide an individual workspace for the candidate's practical work.

The CyberOps labs are the primary technical evidence foundation. The retained v1.0 Skills Assessment and BOTS v2 are mapped separately as higher-level investigation evidence.

## Fixed evidence domains

1. Monitoring and Alerts
2. Log/Event Analysis
3. Network Traffic Analysis
4. Endpoint Analysis
5. Malware/IOC Analysis
6. Vulnerability Scanning
7. Incident Investigation
8. Threat Intelligence
9. Containment
10. Recovery
11. Reporting

## Completed Phase 2 deliverables

- [x] Lab-register structure created
- [x] Evidence-domain structure confirmed
- [x] 36 selected CyberOps labs entered in original course sequence
- [x] Primary evidence domain assigned to each lab
- [x] Related evidence domains assigned
- [x] CyberOps skill identified for each lab
- [x] TESDA NC I relevance identified
- [x] TESDA NC II relevance identified
- [x] Preliminary Direct/Supporting/Gap rating assigned
- [x] Evidence artifacts and standardized screenshot labels identified
- [x] Questions/tasks documented for each selected lab
- [x] Answers/expected results documented for each selected lab
- [x] Observation guidance documented for each selected lab
- [x] 36 individual lab-work folders created
- [x] Standardized `lab-work.md` template applied
- [x] Standardized screenshot attachment locations defined
- [x] Candidate screenshot workflow documented
- [x] Supplementary activity requirements identified

## Individual lab evidence structure

```text
cyberops-labs/
├── README.md
├── 01-identify-running-processes/
│   └── lab-work.md
├── 02-processes-threads-handles-registry/
│   └── lab-work.md
├── ...
└── 36-investigating-windows-host-attack/
    └── lab-work.md
```

Each lab's Markdown record contains:

```text
Lab task/question
       ↓
Reference/expected answer
       ↓
Observation guidance
       ↓
[Attach candidate screenshot here]
       ↓
Candidate interpretation
       ↓
Evidence-domain classification
       ↓
TESDA relevance
```

The `screenshots/` directories will be populated manually as the candidate performs or verifies each laboratory activity.

## Screenshot naming standard

```text
LAB-XX-01-short-description.png
LAB-XX-02-short-description.png
LAB-XX-03-short-description.png
```

`XX` is the portfolio lab number, not the Cisco module number.

## Evidence and privacy rule

All laboratory activities must be performed only in **simulated, isolated, controlled and authorized training environments**. The portfolio must not document or imply activity against live organizational production systems.

Expected/reference results are documentation guidance only. Candidate evidence must come from the candidate's own actual laboratory work. Do not fabricate screenshots, logs, hashes, alerts, PCAPs or observations.

## Phase 2 tracking log

| Date | Progress | Decision / Result |
|---|---|---|
| 2026-08-29 | Started Phase 2 | Lab register specification created; 11 evidence domains locked |
| 2026-08-30 | Register completed | 36 selected labs classified and mapped at a preliminary level |
| 2026-08-30 | Evidence framework completed | 36 individual lab folders and standardized Markdown records created |

## Remaining Phase 2 work

The framework is complete, but the following are **evidence-collection tasks**, not missing documentation:

- [ ] Verify which of the 36 labs have actually been performed by the candidate.
- [ ] Upload candidate-generated screenshots manually.
- [ ] Replace generic observation guidance with the candidate's actual observations where they differ.
- [ ] Record actual command output/results where required.
- [ ] Perform final evidence-domain and TESDA criterion linkage after candidate evidence is available.
- [ ] Mark each lab as Completed / Partially Completed / Not Performed.

## Remaining project phases

### Phase 3 — TESDA performance-criterion mapping
Map the selected CyberOps activities and their eventual candidate-generated evidence to individual TESDA performance criteria and SAG evidence requirements.

### Phase 4 — CyberOps v1.0 Skills Assessment
Finalize candidate-generated evidence and map every v1.0 task to evidence domains and TESDA criteria. Primary target: NC I monitoring/reporting, with supporting NC II investigation evidence.

### Phase 5 — Legacy assessment cleanup
Remove obsolete legacy assessment material from the active evidence architecture. **Completed.**

### Phase 6 — BOTS v2
Complete the simulated Splunk threat-hunting/investigation evidence set and final evidence cleanup. **Documentation/evidence cleanup completed.**

### Phase 7 — Containment/Eradication/Recovery
Build the supplementary NC II mitigation simulation in an isolated laboratory environment.

### Phase 8 — Vulnerability Scanning/Management
Extend authorized laboratory scanning into a complete scan → assess → remediate → rescan → validate workflow.

### Phase 9 — Evidence implementation
Build the 11 evidence-domain indexes/templates around verified candidate-generated artifacts without unnecessary duplication of complete lab reports.

### Phase 10 — Final TESDA evidence index and SAG review
Create the final NC I/NC II evidence index and review the complete evidence package against the applicable SAG/performance criteria. **There is no live-production capstone.**

## Progress rule

At the completion of every phase, update this file with completed deliverables, remaining work, decisions, gaps and the next phase. This file is the central Phase 2 progress tracker.
