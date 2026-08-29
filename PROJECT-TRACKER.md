# Project Tracker — Cisco CyberOps → TESDA Cybersecurity Evidence Portfolio

**Project:** Cisco CyberOps Associate + BOTS v2 + controlled cybersecurity simulations mapped to TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II

## Overall progress

| Phase | Deliverable | Status |
|---|---|---|
| **Phase 1** | Portfolio architecture and evidence strategy | ✅ Complete |
| **Phase 2** | Complete CyberOps Associate lab register, question/answer guide and individual lab evidence framework | 🟢 Framework complete; candidate evidence collection pending |
| **Phase 3** | TESDA performance-criterion + master SAG mapping | ✅ Complete — master matrix established; criterion-level evidence verification continues during later phases |
| **Phase 4** | CyberOps v1.0 Skills Assessment evidence mapping | 🟢 Assessment performed; documentation created; artifact verification pending |
| **Phase 5** | Legacy assessment review and repository cleanup | ✅ Complete |
| **Phase 6** | BOTS v2 threat-hunting evidence mapping, evidence cross-check and cleanup | ✅ Complete |
| **Phase 7** | Controlled containment/eradication/recovery simulation | ⬜ Pending |
| **Phase 8** | Controlled vulnerability scanning/management simulation | ⬜ Pending |
| **Phase 9** | Evidence-domain implementation and consolidation | ⬜ Pending |
| **Phase 10** | Final TESDA evidence index and SAG review | ⬜ Pending |

> **No live-production capstone:** The portfolio does not require or document cybersecurity activities against a company's live production environment. The v1.0 Skills Assessment, BOTS v2 investigations, CyberOps laboratory activities, and controlled supplementary simulations collectively provide the evidence package.

## Portfolio-wide environment and privacy rule

All cybersecurity activities documented in this portfolio are performed exclusively in **simulated, isolated, and controlled laboratory environments** using authorized training datasets, virtual machines, simulated network traffic, and training systems.

No production systems, live organizational networks, confidential company information, personally identifiable information, credentials, private keys, or real organizational security events are intentionally accessed, monitored, scanned, modified, contained, or recovered.

## Phase 1 — COMPLETE

- Portfolio architecture established.
- Four TESDA core competencies established.
- Fixed 11 evidence domains established.
- CyberOps labs established as the primary technical evidence source.
- Skills Assessment, BOTS v2, and controlled supplementary simulations positioned as additional evidence layers.
- Live-production capstone removed.

## Phase 2 — LAB EVIDENCE FRAMEWORK COMPLETE

### Completed

- 36 Cisco CyberOps Associate v1.0 hands-on labs registered in original sequence.
- Primary and related evidence domains assigned.
- Preliminary TESDA NC I/NC II relevance recorded.
- Evidence gaps identified.
- `cisco-lab-register/cyberops-lab-evidence-guide.md` maintained as the master documentation guide.
- Questions/tasks paraphrased and organized for each selected lab.
- Expected answer/result and observation guidance added.
- 36 individual lab-work folders created under `cyberops-labs/`.
- Standardized screenshot filename convention established:

```text
LAB-XX-01-short-description.png
LAB-XX-02-short-description.png
```

- Screenshot attachment locations placed in every individual lab record.
- `cyberops-labs/README.md` created to define the evidence workflow.

### Remaining

- Confirm which of the 36 labs have actually been completed.
- Capture actual laboratory screenshots/outputs for completed labs.
- Replace generic evidence guidance with the candidate's actual observations/results where necessary.
- Mark each lab Completed / Partially Completed / Not Performed.
- Complete final evidence-to-criterion verification after candidate evidence is available.

## Phase 3 — COMPLETE

- TESDA competency framework established.
- Criterion-level mapping created for ICT251312, ICT251313, ICT251314 and ICT251315.
- Master SAG evidence matrix created.
- Process and operational evidence gaps identified.
- Controlled supplementary simulations established as the method for closing gaps.

## Phase 4 — CyberOps v1.0 Skills Assessment

### Completed

- User performed the v1.0 Skills Assessment in the CyberOps laboratory environment.
- Assessment documentation created.
- Alert-driven investigation and evidence-domain mapping established.
- Reference answer material is treated only as a cross-check, not as candidate evidence.

### Remaining

- Verify the candidate's actual screenshots/artifacts.
- Link actual evidence artifacts to the master SAG matrix.
- Finalize the v1.0 RPL evidence package.

## Phase 5 — COMPLETE: Legacy Assessment Cleanup

Obsolete assessment material was removed from the portfolio architecture. The portfolio now focuses on the retained CyberOps v1.0 Skills Assessment, CyberOps Associate laboratory activities, BOTS v2, and controlled supplementary simulations.

## Phase 6 — COMPLETE: BOTS v2 Evidence Cleanup

### Completed

- BOTS v2 assessment directory established.
- Splunk 2 hunting workflow documented.
- SPL commands retained according to the agreed reference/cross-check workflow.
- Actual uploaded screenshot filenames recorded and preserved.
- 100–400 Series questions and evidence images cross-checked.
- Screenshot index updated.
- BOTS v2 investigation report updated with the four-series evidence chain.
- Controlled-environment and data-privacy language added.
- Evidence provenance distinction added.
- BOTS v2 → TESDA evidence mapping maintained only where justified.
- Missing 300-Q3 vendor-lookup image documented as an evidence limitation.
- 42-image inventory recorded.

## Phase 7 — Controlled Containment / Eradication / Recovery Simulation

Create an **isolated training scenario only** covering:

`Detect → Investigate → Contain → Eradicate → Recover → Secondary Scan → Validate → Monitor → Report`

The scenario must use simulated endpoints, authorized training data, and a controlled virtual/network environment. It must not involve live organizational infrastructure or production data.

This phase addresses the mitigation evidence gaps not demonstrated by the CyberOps labs or BOTS v2.

## Phase 8 — Controlled Vulnerability Scanning / Management Simulation

Create an **isolated authorized training scenario only** covering:

`Asset Inventory → Scope/Authorization → Schedule → Scanner Configuration → Scan → Analyze → Prioritize → Change Request → Remediate → Rescan → Validate → Report`

All targets must be explicitly designated laboratory assets.

## Phase 9 — Evidence-domain implementation

Populate the 11 evidence domains with verified laboratory artifacts and reusable evidence indexes/templates. This includes selected evidence from the individual CyberOps lab folders, v1.0 assessment, BOTS v2 and controlled supplementary simulations.

## Phase 10 — Final TESDA evidence review

Create the final TESDA evidence index and SAG review package from the completed laboratory, assessment, BOTS v2 and supplementary simulation evidence.

There will be **no live-production capstone**.

## Project rules

- Perform cybersecurity activities only in simulated, isolated, controlled and authorized laboratory environments.
- Never perform scanning, monitoring, exploitation, containment, eradication, recovery or other security actions against live organizational production systems for this portfolio.
- Do not upload production data, confidential company information, PII, credentials, private keys or restricted information.
- Use actual performed laboratory evidence only.
- Do not fabricate screenshots, logs, hashes, alerts, PCAPs, reports or assessment results.
- Do not claim that completing a Cisco lab automatically equals a TESDA competency.
- Keep the 11 evidence domains separate from the four TESDA core competencies.
- Treat reference walkthroughs as preparation/cross-checking material, not as substitutes for candidate evidence.
- Do not identify external answer sources in portfolio documentation.
- Update this tracker at the end of each phase.

## Current next task

**Confirm the CyberOps labs you have actually completed, then begin collecting their real laboratory screenshots using the standardized evidence filenames. Phase 7 should follow after the lab evidence framework is populated sufficiently.**
