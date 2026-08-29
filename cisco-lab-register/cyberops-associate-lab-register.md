# Cisco CyberOps Associate Lab Register

## Purpose

This is the master register for **Cisco CyberOps Associate laboratory activities**, maintained in the original Cisco sequence. The current Cisco/NDG CyberOps Associate v1 lab catalog lists **36 hands-on labs plus the Skills-Based Assessment**; the course outline describes the overall offering as 37 labs/activities. This register records the hands-on labs first and will map the Skills Assessments separately in later phases.

Source checked: Cisco CyberOps Associate lab catalog published by Network Development Group (NDG).

## Fixed evidence domains

| ID | Evidence domain |
|---|---|
| 01 | Monitoring and Alerts |
| 02 | Log/Event Analysis |
| 03 | Network Traffic Analysis |
| 04 | Endpoint Analysis |
| 05 | Malware/IOC Analysis |
| 06 | Vulnerability Scanning |
| 07 | Incident Investigation |
| 08 | Threat Intelligence |
| 09 | Containment |
| 10 | Recovery |
| 11 | Reporting |

## Classification rules

- **Primary domain:** the best single location for the lab's main evidence.
- **Related domains:** other evidence domains materially supported by the same activity.
- **NC I / NC II:** preliminary competency relevance only. Exact TESDA performance-criterion mapping is Phase 3.
- **Direct:** strong practical evidence for the relevant cybersecurity skill.
- **Supporting:** useful technical evidence, but not sufficient by itself for the complete TESDA requirement.
- **Gap:** the lab does not demonstrate the required action; a supplementary activity is needed.

## Phase 2 master register

| # | Lab No. | Lab Activity | Primary Domain | Related Domains | NC I | NC II | Preliminary Coverage | Evidence / Notes |
|---:|---|---|---|---|---|---|---|---|
| 1 | 3.0.3 | Identify Running Processes | 04 Endpoint Analysis | 07 Incident Investigation | Supporting | Direct/Supporting | 🟡 | Process list, suspicious-process observations |
| 2 | 3.2.11 | Exploring Processes, Threads, Handles, and Windows Registry | 04 Endpoint Analysis | 07 Incident Investigation, 05 Malware/IOC Analysis | Supporting | Direct/Supporting | 🟡 | Process/registry findings, screenshots |
| 3 | 3.3.10 | Create User Accounts | 04 Endpoint Analysis | 09 Containment | Supporting | Supporting | 🟡 | Account configuration and security-control evidence |
| 4 | 3.3.11 | Using Windows PowerShell | 04 Endpoint Analysis | 07 Incident Investigation, 02 Log/Event Analysis | Supporting | Direct/Supporting | 🟡 | Commands, outputs, investigation notes |
| 5 | 3.3.12 | Windows Task Manager | 04 Endpoint Analysis | 01 Monitoring and Alerts, 07 Incident Investigation | Supporting | Supporting | 🟡 | Process/resource observations |
| 6 | 3.3.13 | Monitor and Manage System Resources in Windows | 04 Endpoint Analysis | 01 Monitoring and Alerts | Supporting | Supporting | 🟡 | Resource monitoring evidence |
| 7 | 4.2.6 | Working with Text Files in the CLI | 02 Log/Event Analysis | 04 Endpoint Analysis | Supporting | Supporting | 🟡 | CLI commands and text/log handling |
| 8 | 4.2.7 | Getting Familiar with the Linux Shell | 04 Endpoint Analysis | 02 Log/Event Analysis | Supporting | Supporting | 🟡 | Linux CLI evidence |
| 9 | 4.3.4 | Linux Servers | 04 Endpoint Analysis | 02 Log/Event Analysis | Supporting | Supporting | 🟡 | Server administration/security observations |
| 10 | 4.4.4 | Locating Log Files | 02 Log/Event Analysis | 04 Endpoint Analysis, 07 Incident Investigation | Direct/Supporting | Supporting | 🟢 | Log locations, commands, captured output |
| 11 | 4.5.4 | Navigating the Linux Filesystem and Permission Settings | 04 Endpoint Analysis | 02 Log/Event Analysis | Supporting | Supporting | 🟡 | Permissions and filesystem evidence |
| 12 | 5.1.5 | Tracing a Route | 03 Network Traffic Analysis | 07 Incident Investigation | Supporting | Supporting | 🟡 | Route/path output and interpretation |
| 13 | 5.3.7 | Introduction to Wireshark | 03 Network Traffic Analysis | 07 Incident Investigation | Direct/Supporting | Direct/Supporting | 🟢 | Packet captures, filters, protocol observations |
| 14 | 8.2.8 | Using Wireshark to Examine Ethernet Frames | 03 Network Traffic Analysis | 07 Incident Investigation | Supporting | Supporting | 🟡 | Frame fields and packet analysis |
| 15 | 9.2.6 | Using Wireshark to Observe the TCP 3-Way Handshake | 03 Network Traffic Analysis | 07 Incident Investigation | Supporting | Supporting | 🟡 | TCP sequence/flags and packet evidence |
| 16 | 9.3.8 | Exploring Nmap | 06 Vulnerability Scanning | 07 Incident Investigation, 03 Network Traffic Analysis | Direct/Supporting | Supporting | 🟢 | Scan commands, target scope, results; full TESDA VM workflow still required |
| 17 | 10.2.7 | Using Wireshark to Examine a UDP DNS Capture | 03 Network Traffic Analysis | 08 Threat Intelligence, 07 Incident Investigation | Direct/Supporting | Supporting | 🟢 | DNS queries/responses and packet evidence |
| 18 | 10.4.3 | Using Wireshark to Examine TCP and UDP Captures | 03 Network Traffic Analysis | 07 Incident Investigation | Direct/Supporting | Supporting | 🟢 | TCP/UDP traffic analysis |
| 19 | 10.6.7 | Using Wireshark to Examine HTTP and HTTPS Traffic | 03 Network Traffic Analysis | 07 Incident Investigation, 05 Malware/IOC Analysis | Direct/Supporting | Supporting | 🟢 | HTTP/HTTPS indicators and packet evidence |
| 20 | 17.1.7 | Exploring DNS Traffic | 03 Network Traffic Analysis | 08 Threat Intelligence, 07 Incident Investigation | Direct/Supporting | Supporting | 🟢 | DNS behavior and suspicious-domain investigation |
| 21 | 17.2.6 | Attacking a mySQL Database | 07 Incident Investigation | 03 Network Traffic Analysis, 02 Log/Event Analysis | Supporting | Direct/Supporting | 🟡 | Attack behavior, database evidence; controlled lab only |
| 22 | 17.2.7 | Reading Server Logs | 02 Log/Event Analysis | 07 Incident Investigation, 01 Monitoring and Alerts | Direct | Direct/Supporting | 🟢 | Server-log evidence and event correlation |
| 23 | 21.0.3 | Creating Codes | 05 Malware/IOC Analysis | 04 Endpoint Analysis | Supporting | Supporting | 🟡 | Security/cryptography foundation; limited direct TESDA evidence |
| 24 | 21.1.6 | Hashing Things Out | 05 Malware/IOC Analysis | 08 Threat Intelligence, 07 Incident Investigation | Supporting | Direct | 🟢 | Hash values, integrity/IOC evidence |
| 25 | 21.2.10 | Encrypting and Decrypting Data Using OpenSSL | 05 Malware/IOC Analysis | 04 Endpoint Analysis | Supporting | Supporting | 🟡 | Cryptographic operations; supporting evidence |
| 26 | 21.2.11 | Encrypting and Decrypting Data Using a Hacker Tool | 05 Malware/IOC Analysis | 07 Incident Investigation | Supporting | Supporting | 🟡 | Controlled security-analysis exercise |
| 27 | 21.2.12 | Examining Telnet and SSH in Wireshark | 03 Network Traffic Analysis | 05 Malware/IOC Analysis, 07 Incident Investigation | Direct/Supporting | Supporting | 🟢 | Protocol/security analysis and packet evidence |
| 28 | 21.4.7 | Certificate Authority Stores | 04 Endpoint Analysis | 05 Malware/IOC Analysis, 08 Threat Intelligence | Supporting | Supporting | 🟡 | Certificate/security-control evidence |
| 29 | 26.1.7 | Snort and Firewall Rules | 01 Monitoring and Alerts | 03 Network Traffic Analysis, 07 Incident Investigation, 09 Containment | Direct | Direct/Supporting | 🟢 | IDS alert, firewall rule, detection and response evidence |
| 30 | 27.1.5 | Convert Data into a Universal Format | 02 Log/Event Analysis | 01 Monitoring and Alerts, 07 Incident Investigation | Supporting | Supporting | 🟡 | Normalization/data-preparation evidence |
| 31 | 27.2.9 | Regular Expression Tutorial | 02 Log/Event Analysis | 01 Monitoring and Alerts, 07 Incident Investigation | Direct/Supporting | Supporting | 🟢 | Search/filter patterns for security data |
| 32 | 27.2.10 | Extract an Executable from a PCAP | 05 Malware/IOC Analysis | 03 Network Traffic Analysis, 07 Incident Investigation, 08 Threat Intelligence | Direct | Direct | 🟢 | Extracted artifact, hash, PCAP evidence |
| 33 | 27.2.12 | Interpret HTTP and DNS Data to Isolate Threat Actor | 07 Incident Investigation | 03 Network Traffic Analysis, 05 Malware/IOC Analysis, 08 Threat Intelligence | Direct | Direct | 🟢 | Threat-actor indicators, network evidence, investigation notes |
| 34 | 27.2.14 | Isolate Compromised Host Using 5-Tuple | 07 Incident Investigation | 03 Network Traffic Analysis, 01 Monitoring and Alerts, 09 Containment | Direct | Direct | 🟢 | Compromised-host identification and isolation evidence |
| 35 | 27.2.15 | Investigating a Malware Exploit | 05 Malware/IOC Analysis | 07 Incident Investigation, 08 Threat Intelligence, 04 Endpoint Analysis | Direct | Direct | 🟢 | Malware/IOC investigation and threat validation |
| 36 | 27.2.16 | Investigating an Attack on a Windows Host | 07 Incident Investigation | 04 Endpoint Analysis, 02 Log/Event Analysis, 05 Malware/IOC Analysis | Direct | Direct | 🟢 | Windows-host investigation, logs, artifacts and findings |

## Skills-Based Assessment

The **Skills-Based Assessment (SBA)** is listed separately from the 36 hands-on labs because it is an assessment activity rather than another ordinary lab. It will be mapped in detail in Phase 4 for v1.0 and Phase 5 for v1.1.

Expected primary domains for the CyberOps v1.0 alert-driven assessment include:

- 01 Monitoring and Alerts
- 05 Malware/IOC Analysis
- 07 Incident Investigation
- 08 Threat Intelligence
- 11 Reporting

## Important Phase 2 observations

### Strongest CyberOps evidence for NC I monitoring/reporting

- **4.4.4 Locating Log Files**
- **5.3.7 Introduction to Wireshark**
- **17.2.7 Reading Server Logs**
- **26.1.7 Snort and Firewall Rules**
- **27.2.9 Regular Expression Tutorial**
- **27.2.10 Extract an Executable from a PCAP**
- **27.2.12 Isolate Threat Actor**
- **27.2.14 Isolate Compromised Host**
- **27.2.15 Investigating a Malware Exploit**
- **27.2.16 Investigating an Attack on a Windows Host**

### Strongest CyberOps evidence for NC I vulnerability scanning

- **9.3.8 Exploring Nmap**

This is strong technical scanning evidence, but it does **not by itself prove the complete TESDA vulnerability-scanning workflow**. Phase 8 will add asset inventory, authorization/scope, scan planning, result analysis, reporting, remediation and validation.

### Strongest CyberOps evidence for NC II threat mitigation

- **26.1.7 Snort and Firewall Rules**
- **21.1.6 Hashing Things Out**
- **27.2.10 Extract an Executable from a PCAP**
- **27.2.12 Isolate Threat Actor**
- **27.2.14 Isolate Compromised Host Using 5-Tuple**
- **27.2.15 Investigating a Malware Exploit**
- **27.2.16 Investigating an Attack on a Windows Host**

These provide strong detection/investigation/IOC evidence, but dedicated containment, eradication and recovery evidence remains necessary.

### Strongest CyberOps evidence for NC II vulnerability management/control

The CyberOps Nmap activity is useful technical evidence, but the complete competency remains a **supplementary-lab requirement** until the portfolio demonstrates the full vulnerability-management lifecycle.

## Phase 2 conclusion

The **36 hands-on CyberOps Associate labs are now registered in original sequence** and classified against the 11 evidence domains. This register is the working master list for the next phases.

## Phase 2 remaining tasks

- [ ] Verify the register against the exact CyberOps course/VM version used for the final evidence submission.
- [ ] Confirm actual lab completion status for each activity.
- [ ] Capture the evidence requirements for each completed lab.
- [ ] Create the TESDA performance-criterion mapping in Phase 3.
- [ ] Create individual evidence-domain folders in Phase 9.
- [ ] Map v1.0/v1.1 Skills Assessments separately.
- [ ] Map BOTS v2 separately.
