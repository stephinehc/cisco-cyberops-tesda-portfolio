# Cisco CyberOps Associate Skills Assessment → TESDA Mapping

## Purpose

This document establishes the portfolio's initial mapping for the **Cisco CyberOps Associate v1.0 and v1.1 Skills Assessments**.

The assessments are treated as practical evidence sources, not as automatic TESDA-equivalency claims.

## v1.0 — primary NC I practical evidence

The v1.0 Pushdo investigation is an alert-driven SOC exercise. Its strongest evidence sequence is:

```text
Security alert
   ↓
Alert review / triage
   ↓
Affected-host identification
   ↓
Event and traffic investigation
   ↓
Malicious file / IOC identification
   ↓
Hash and threat-intelligence verification
   ↓
Related-alert correlation
   ↓
Investigation findings
   ↓
Report
```

### Mapping

| TESDA competency | v1.0 evidence | Rating |
|---|---|---:|
| ICT251312 Monitor and report cyber threats | Alert review and investigation | 🟢 Direct |
| ICT251312 — manual verification | Alert, host, network and file analysis | 🟢 Direct |
| ICT251312 — case follow-up | Related-alert/event correlation | 🟢 Direct |
| ICT251312 — alert reporting | Investigation report | 🟡 Supporting until TESDA-format report/ticket is added |
| ICT251313 Vulnerability scanning | Not the focus of v1.0 | 🔴 Gap |
| ICT251314 Threat mitigation | Incident analysis and IOC identification | 🟡 Supporting |
| ICT251315 Vulnerability management/control | Not the focus of v1.0 | 🔴 Gap |

## v1.1 — advanced investigation evidence

Use the v1.1 Skills Assessment as an advanced practical layer after v1.0. Map only the tasks actually performed in the version of the assessment used by the learner.

### Intended evidence areas

- security monitoring
- host-based analysis
- network intrusion analysis
- threat intelligence
- malware analysis
- threat hunting
- SIEM/SOAR-related analysis where present

### Mapping approach

| TESDA competency | Expected v1.1 contribution | Rating |
|---|---|---:|
| ICT251312 Monitor and report cyber threats | Advanced monitoring, investigation and reporting | 🟢/🟡 Verify against actual assessment tasks |
| ICT251313 Vulnerability scanning | Not assumed | 🔴 Unless an actual scanning task is performed |
| ICT251314 Threat mitigation | Advanced investigation, IOC/TTP/CTI analysis | 🟢/🟡 Strong supporting evidence |
| ICT251315 Vulnerability management/control | Not assumed | 🔴 Unless actual VM activities are performed |

## Important evidence rule

The portfolio must document the **exact v1.1 assessment tasks actually completed** before assigning a Direct rating. Do not infer competency coverage from Cisco course objectives alone.

## Recommended assessment progression

```text
CyberOps laboratory practice
        ↓
CyberOps v1.0 Skills Assessment
        ↓
Alert-driven SOC investigation
        ↓
CyberOps v1.1 Skills Assessment
        ↓
Advanced investigation / threat hunting
        ↓
Containment + eradication + recovery simulation
        ↓
NC II mitigation evidence
```

## Sources

Cisco CyberOps Associate v1.1 exam objectives/release material should be retained in the portfolio's reference notes when used for mapping. TESDA competency definitions should be sourced from the applicable Training Regulations. citehttps://www.tesda.gov.ph/Downloadables/TRs/TR-Cyber%20Threat%20Monitoring%20NC%20I.pdf citehttps://www.tesda.gov.ph/Downloadables/TRs/TR-Cyber-threat-mitigation%20NC%20II.pdf
