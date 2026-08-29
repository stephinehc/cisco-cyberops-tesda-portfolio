# Phase 1 — Portfolio Architecture and Evidence Strategy

**Status:** ✅ Complete

## Objective

Establish the final architecture for a TESDA-oriented cybersecurity evidence portfolio using Cisco CyberOps Associate laboratory activities as the primary technical evidence foundation, supported by the CyberOps Associate v1.0 Skills Assessment, BOTS v2, and controlled supplementary simulations.

## Final design decisions

### 1. Fixed 11 evidence domains

The portfolio uses these categories for organizing technical evidence:

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

These are **evidence domains**, not additional TESDA core competencies.

### 2. TESDA competencies remain the mapping layer

The portfolio maps evidence to the applicable TESDA Cyber Threat Monitoring NC I and Cyber Threat Mitigation NC II competency requirements. The 11 evidence domains are used to organize the technical evidence before it is mapped to the applicable TESDA performance criteria.

### 3. Primary evidence source

Cisco CyberOps Associate laboratory activities are the primary technical evidence foundation. The labs provide individual technical demonstrations across network analysis, endpoint analysis, logs, malware/IOC analysis, vulnerability scanning, monitoring and investigation.

### 4. Integrated assessment evidence

The **CyberOps Associate v1.0 Skills Assessment** is retained as an integrated simulated SOC investigation. It complements the individual laboratory activities and provides evidence across multiple evidence domains.

### 5. BOTS v2 evidence

BOTS v2 provides an additional simulated Splunk investigation/threat-hunting layer. It is used to demonstrate multi-source log analysis, investigation, IOC analysis, threat intelligence and reporting.

### 6. Controlled supplementary simulations

Supplementary simulations are used only when existing CyberOps laboratory, v1.0 assessment, and BOTS v2 evidence does not adequately demonstrate a required TESDA performance criterion.

Planned supplementary areas include:

- containment;
- eradication;
- recovery/rollback;
- secondary validation;
- vulnerability-scanning workflow;
- vulnerability-management/control workflow.

### 7. No live-production capstone

The portfolio **does not require or document a live-production cybersecurity capstone**.

All demonstrations are performed in simulated, isolated, controlled and authorized laboratory environments. The final evidence package is a collection of laboratory demonstrations, assessment evidence, BOTS v2 investigation evidence and controlled supplementary simulations.

## Environment and privacy standard

All activities documented in the portfolio must be performed using simulated, isolated and controlled laboratory environments, authorized training datasets, virtual machines, simulated network traffic and intentionally configured training systems.

The portfolio must not contain or imply access to:

- live organizational production networks;
- production servers or endpoints;
- confidential company information;
- personally identifiable information;
- production credentials or private keys;
- real organizational security incidents.

No production system is to be scanned, monitored, modified, contained, eradicated, recovered or otherwise acted upon for portfolio purposes.

## Evidence integrity standard

The portfolio distinguishes between **expected/reference results** and **candidate-generated evidence**.

Expected results and reference material may be used to understand or cross-check a laboratory activity. They are not themselves proof that the candidate performed the activity.

Candidate evidence should consist of actual outputs, screenshots, observations, reports or other artifacts generated from the candidate's own authorized laboratory work.

Do not fabricate screenshots, logs, alerts, hashes, scan results, reports or other evidence.

## Final evidence architecture

```text
TESDA COMPETENCY REQUIREMENTS
            ↓
11 EVIDENCE DOMAINS
            ↓
Cisco CyberOps Associate Labs
            ↓
CyberOps v1.0 Skills Assessment
            ↓
BOTS v2 Simulated Investigation
            ↓
Controlled Supplementary Simulations
            ↓
Evidence Artifacts
            ↓
TESDA Performance-Criterion Mapping
            ↓
Final Evidence Index / SAG Review
```

## Phase 1 deliverables

- [x] Portfolio purpose established
- [x] TESDA target qualifications established
- [x] Four core competency mapping layer established
- [x] 11 evidence domains finalized
- [x] CyberOps Associate labs established as primary technical evidence source
- [x] CyberOps v1.0 Skills Assessment retained
- [x] BOTS v2 established as supplementary investigation evidence
- [x] Controlled supplementary simulations defined for remaining gaps
- [x] Live-production capstone removed
- [x] Environment/privacy standard established
- [x] Evidence-integrity standard established
- [x] Final evidence architecture established

## Phase 1 completion criteria

Phase 1 is considered complete because the portfolio now has a stable architecture that can be populated without requiring live organizational access. Later phases should add evidence to this architecture rather than redesigning it unless a genuine TESDA requirement or evidence gap requires a documented change.

## Transition to Phase 2

Phase 2 documents the CyberOps Associate laboratory activities in sequence, assigns the primary/related evidence domains, identifies relevant TESDA areas, defines expected evidence, and establishes standardized screenshot labels for future manual evidence uploads.
