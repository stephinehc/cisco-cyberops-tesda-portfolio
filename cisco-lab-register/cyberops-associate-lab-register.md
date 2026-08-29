# Cisco CyberOps Associate v1.0 Lab Register

## Purpose

This is the master register for the **36 Cisco CyberOps Associate v1.0 hands-on laboratory activities** used as the primary technical evidence layer of this portfolio. The Skills Assessment is documented separately.

The activities are organized in their Cisco sequence and mapped to the portfolio's fixed 11 evidence domains. The detailed evidence guide is maintained in `cyberops-lab-evidence-guide.md`.

## Controlled-environment and data-privacy statement

All activities documented in this portfolio are performed only in **simulated, isolated, and controlled laboratory environments** using authorized training virtual machines, simulated networks, packet captures, training datasets, and intentionally configured systems.

No live organizational production systems, third-party systems, confidential company information, personally identifiable information, production credentials, private keys, or real organizational security events are intentionally accessed, monitored, scanned, modified, contained, or recovered.

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

## Evidence ratings

- **🟢 Direct:** strong technical evidence for the demonstrated activity.
- **🟡 Supporting:** useful evidence but not sufficient by itself for the complete TESDA requirement.
- **🔴 Gap:** the lab does not demonstrate the required action; a controlled supplementary simulation is needed.

## 36 hands-on labs

| # | Lab | Activity | Primary domain | Related domains | Main TESDA relevance |
|---:|---|---|---|---|---|
| 1 | 3.0.3 | Identify Running Processes | 04 Endpoint Analysis | 07 Incident Investigation | Endpoint/process analysis |
| 2 | 3.2.11 | Exploring Processes, Threads, Handles, and Windows Registry | 04 Endpoint Analysis | 05 Malware/IOC Analysis, 07 Incident Investigation | Endpoint/registry investigation |
| 3 | 3.3.10 | Create User Accounts | 04 Endpoint Analysis | 09 Containment | Account/security-control concepts |
| 4 | 3.3.11 | Using Windows PowerShell | 04 Endpoint Analysis | 02 Log/Event Analysis, 07 Incident Investigation | Endpoint investigation/CLI |
| 5 | 3.3.12 | Windows Task Manager | 04 Endpoint Analysis | 01 Monitoring and Alerts, 07 Incident Investigation | Process/resource monitoring |
| 6 | 3.3.13 | Monitor and Manage System Resources in Windows | 04 Endpoint Analysis | 01 Monitoring and Alerts | Resource monitoring |
| 7 | 4.2.6 | Working with Text Files in the CLI | 02 Log/Event Analysis | 04 Endpoint Analysis | Text/log processing |
| 8 | 4.2.7 | Getting Familiar with the Linux Shell | 04 Endpoint Analysis | 02 Log/Event Analysis | Linux CLI operations |
| 9 | 4.3.4 | Linux Servers | 04 Endpoint Analysis | 02 Log/Event Analysis | Server/service analysis |
| 10 | 4.4.4 | Locating Log Files | 02 Log/Event Analysis | 04 Endpoint Analysis, 07 Incident Investigation | Log discovery |
| 11 | 4.5.4 | Navigating the Linux Filesystem and Permission Settings | 04 Endpoint Analysis | 02 Log/Event Analysis | Filesystem/permissions |
| 12 | 5.1.5 | Tracing a Route | 03 Network Traffic Analysis | 07 Incident Investigation | Network path analysis |
| 13 | 5.3.7 | Introduction to Wireshark | 03 Network Traffic Analysis | 07 Incident Investigation | Packet analysis |
| 14 | 8.2.8 | Using Wireshark to Examine Ethernet Frames | 03 Network Traffic Analysis | 07 Incident Investigation | Ethernet/frame analysis |
| 15 | 9.2.6 | Using Wireshark to Observe the TCP 3-Way Handshake | 03 Network Traffic Analysis | 07 Incident Investigation | TCP analysis |
| 16 | 9.3.8 | Exploring Nmap | 06 Vulnerability Scanning | 03 Network Traffic Analysis, 07 Incident Investigation | Authorized lab scanning |
| 17 | 10.2.7 | Using Wireshark to Examine a UDP DNS Capture | 03 Network Traffic Analysis | 08 Threat Intelligence, 07 Incident Investigation | DNS analysis |
| 18 | 10.4.3 | Using Wireshark to Examine TCP and UDP Captures | 03 Network Traffic Analysis | 07 Incident Investigation | Protocol/packet analysis |
| 19 | 10.6.7 | Using Wireshark to Examine HTTP and HTTPS Traffic | 03 Network Traffic Analysis | 05 Malware/IOC Analysis, 07 Incident Investigation | Web traffic analysis |
| 20 | 17.1.7 | Exploring DNS Traffic | 03 Network Traffic Analysis | 08 Threat Intelligence, 07 Incident Investigation | DNS investigation |
| 21 | 17.2.6 | Attacking a mySQL Database | 07 Incident Investigation | 03 Network Traffic Analysis, 02 Log/Event Analysis | Simulated attack investigation |
| 22 | 17.2.7 | Reading Server Logs | 02 Log/Event Analysis | 07 Incident Investigation, 01 Monitoring and Alerts | Log analysis |
| 23 | 21.0.3 | Creating Codes | 05 Malware/IOC Analysis | 04 Endpoint Analysis | Cryptography/security foundation |
| 24 | 21.1.6 | Hashing Things Out | 05 Malware/IOC Analysis | 08 Threat Intelligence, 07 Incident Investigation | Hash/IOC analysis |
| 25 | 21.2.10 | Encrypting and Decrypting Data Using OpenSSL | 05 Malware/IOC Analysis | 04 Endpoint Analysis | Cryptographic analysis |
| 26 | 21.2.11 | Encrypting and Decrypting Data Using a Hacker Tool | 05 Malware/IOC Analysis | 07 Incident Investigation | Controlled security analysis |
| 27 | 21.2.12 | Examining Telnet and SSH in Wireshark | 03 Network Traffic Analysis | 05 Malware/IOC Analysis, 07 Incident Investigation | Protocol/security analysis |
| 28 | 21.4.7 | Certificate Authority Stores | 04 Endpoint Analysis | 05 Malware/IOC Analysis, 08 Threat Intelligence | Certificate/security analysis |
| 29 | 26.1.7 | Snort and Firewall Rules | 01 Monitoring and Alerts | 03 Network Traffic Analysis, 07 Incident Investigation, 09 Containment | Detection and defensive controls |
| 30 | 27.1.5 | Convert Data into a Universal Format | 02 Log/Event Analysis | 01 Monitoring and Alerts, 07 Incident Investigation | Security-data normalization |
| 31 | 27.2.9 | Regular Expression Tutorial | 02 Log/Event Analysis | 01 Monitoring and Alerts, 07 Incident Investigation | Security-data searching |
| 32 | 27.2.10 | Extract an Executable from a PCAP | 05 Malware/IOC Analysis | 03 Network Traffic Analysis, 07 Incident Investigation, 08 Threat Intelligence | Artifact extraction/IOC analysis |
| 33 | 27.2.12 | Interpret HTTP and DNS Data to Isolate Threat Actor | 07 Incident Investigation | 03 Network Traffic Analysis, 05 Malware/IOC Analysis, 08 Threat Intelligence | Threat investigation |
| 34 | 27.2.14 | Isolate Compromised Host Using 5-Tuple | 07 Incident Investigation | 01 Monitoring and Alerts, 03 Network Traffic Analysis, 09 Containment | Compromised-host identification |
| 35 | 27.2.15 | Investigating a Malware Exploit | 05 Malware/IOC Analysis | 04 Endpoint Analysis, 07 Incident Investigation, 08 Threat Intelligence | Malware/IOC investigation |
| 36 | 27.2.16 | Investigating an Attack on a Windows Host | 07 Incident Investigation | 02 Log/Event Analysis, 04 Endpoint Analysis, 05 Malware/IOC Analysis | Integrated endpoint investigation |

## Skills-Based Assessment

The **CyberOps Associate v1.0 Skills Assessment** is maintained separately under `assessments/cyberops-v1.0/`. It is not counted as another ordinary lab.

## Evidence workflow

For each lab selected for the portfolio:

```text
Lab performed in controlled environment
        ↓
Question / task
        ↓
Answer / observed result
        ↓
Screenshot(s) or command output
        ↓
Interpretation
        ↓
Primary evidence domain
        ↓
TESDA relevance
```

The detailed question/answer and screenshot-label template is in `cyberops-lab-evidence-guide.md`.

## Important limitations

- The Nmap lab demonstrates technical scanning, but it does not by itself establish the complete TESDA vulnerability-scanning workflow.
- Investigation labs do not automatically demonstrate containment, eradication, recovery, or vulnerability management.
- Labs involving attack techniques are performed only against intentionally configured training systems.
- Reference answer material is used for cross-checking; candidate evidence must come from the candidate's own controlled laboratory run.
