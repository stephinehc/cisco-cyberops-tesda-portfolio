# Cisco CyberOps Associate v1.0 — Lab Evidence Guide

## Purpose

This guide provides a portfolio-ready evidence template for the **36 Cisco CyberOps Associate v1.0 hands-on labs** in the master register.

The questions/tasks and expected answers below are **paraphrased from the corresponding ITExamAnswers lab-answer material** used as a cross-check. They are not presented as a substitute for the original Cisco lab instructions or as candidate evidence.

## Controlled-environment and privacy statement

All work documented here must be performed only in a **simulated, isolated, and controlled laboratory environment** using authorized training virtual machines, simulated networks, packet captures, training datasets, and intentionally configured systems.

Do not use production systems, live organizational networks, confidential company information, personally identifiable information, production credentials, private keys, or real organizational security events.

## Evidence image naming standard

Use the following standardized naming convention for screenshots:

```text
LAB-XX-01-short-description.png
LAB-XX-02-short-description.png
LAB-XX-03-short-description.png
```

Where `XX` is the portfolio lab number in this guide, not the Cisco module number.

Example:

```text
LAB-16-01-nmap-scan-command.png
LAB-16-02-nmap-open-ports.png
```

If no screenshot is necessary, record the result as text/command output instead. Do not create placeholder images.

---

# Lab 01 — 3.0.3 Identify Running Processes

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Identify the processes running on the simulated Windows host.
2. Identify the process associated with a selected network connection.
3. Record the relevant process information.

### Expected answer/result
Use TCP/UDP Endpoint Viewer or the specified Sysinternals utility to identify active processes and their associated network endpoints. Record the process name/PID and relevant local/remote endpoint information.

### Evidence labels
```markdown
![LAB-01-01 — Running process view](../evidence-images/LAB-01-01-process-list.png)
![LAB-01-02 — Process/network endpoint information](../evidence-images/LAB-01-02-process-network-endpoint.png)
```

---

# Lab 02 — 3.2.11 Exploring Processes, Threads, Handles, and Windows Registry

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Inspect a process using Process Explorer.
2. Examine threads and handles associated with the process.
3. Examine relevant Windows Registry information.
4. Identify information useful for endpoint investigation.

### Expected answer/result
Process Explorer exposes process IDs, parent/child relationships, threads, handles, loaded modules and other process information. Registry inspection provides configuration/persistence-related context where applicable.

### Evidence labels
```markdown
![LAB-02-01 — Process Explorer](../evidence-images/LAB-02-01-process-explorer.png)
![LAB-02-02 — Threads/handles](../evidence-images/LAB-02-02-threads-handles.png)
![LAB-02-03 — Registry evidence](../evidence-images/LAB-02-03-registry.png)
```

---

# Lab 03 — 3.3.10 Create User Accounts

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Create a local user account.
2. Modify account properties/group membership.
3. Verify the account configuration.

### Expected answer/result
The account should be created successfully with the requested properties and verified through the Windows account-management interface/command output.

### Evidence labels
```markdown
![LAB-03-01 — User account creation](../evidence-images/LAB-03-01-user-account.png)
![LAB-03-02 — Account properties](../evidence-images/LAB-03-02-account-properties.png)
```

---

# Lab 04 — 3.3.11 Using Windows PowerShell

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Open PowerShell.
2. Explore basic PowerShell commands.
3. Use PowerShell to inspect the simulated host.
4. Record useful command output.

### Expected answer/result
PowerShell provides command-line access to Windows administration and investigation functions. Record the commands and outputs actually used in the laboratory.

### Evidence labels
```markdown
![LAB-04-01 — PowerShell console](../evidence-images/LAB-04-01-powershell-console.png)
![LAB-04-02 — PowerShell investigation output](../evidence-images/LAB-04-02-powershell-output.png)
```

---

# Lab 05 — 3.3.12 Windows Task Manager

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Examine the Processes tab.
2. Identify resource-intensive processes.
3. Inspect process details and resource usage.
4. Manage a process in the simulated environment as instructed.

### Expected answer/result
Task Manager provides process, performance and resource information. Record the process/resource observations required by the lab.

### Evidence labels
```markdown
![LAB-05-01 — Task Manager processes](../evidence-images/LAB-05-01-task-manager-processes.png)
![LAB-05-02 — Resource/performance view](../evidence-images/LAB-05-02-task-manager-performance.png)
```

---

# Lab 06 — 3.3.13 Monitor and Manage System Resources in Windows

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Start the specified Windows administrative/resource-monitoring tools.
2. Observe CPU, memory, disk and/or network resources.
3. Identify processes consuming resources.
4. Perform the instructed resource-management action.

### Expected answer/result
The resource-monitoring tools display current system utilization and identify processes associated with resource consumption.

### Evidence labels
```markdown
![LAB-06-01 — Resource monitoring](../evidence-images/LAB-06-01-resource-monitor.png)
![LAB-06-02 — Resource/process details](../evidence-images/LAB-06-02-resource-process-details.png)
```

---

# Lab 07 — 4.2.6 Working with Text Files in the CLI

**Primary domain:** 02 Log/Event Analysis

### Questions / tasks
1. Use Linux CLI tools to inspect text files.
2. Use a text editor to create or modify a file.
3. Inspect configuration-file content.
4. Record the commands used.

### Expected answer/result
The lab demonstrates command-line text-file handling and configuration-file inspection. Record the actual file path, command and resulting output.

### Evidence labels
```markdown
![LAB-07-01 — Text file command](../evidence-images/LAB-07-01-text-file-command.png)
![LAB-07-02 — Configuration/text file](../evidence-images/LAB-07-02-config-file.png)
```

---

# Lab 08 — 4.2.7 Getting Familiar with the Linux Shell

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Navigate directories from the Linux CLI.
2. Create, copy, move and remove files/directories as instructed.
3. Use basic administrative commands.
4. Verify command results.

### Expected answer/result
The Linux shell supports file management and administrative operations through commands. Record the commands and resulting directory/file state.

### Evidence labels
```markdown
![LAB-08-01 — Linux shell](../evidence-images/LAB-08-01-linux-shell.png)
![LAB-08-02 — File management output](../evidence-images/LAB-08-02-file-management.png)
```

---

# Lab 09 — 4.3.4 Linux Servers

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Identify services/servers running on the simulated Linux host.
2. Identify associated listening ports.
3. Determine what services are available.

### Expected answer/result
Use the specified Linux commands to identify listening services and their ports. Record service name, process and port where available.

### Evidence labels
```markdown
![LAB-09-01 — Listening services](../evidence-images/LAB-09-01-listening-services.png)
![LAB-09-02 — Server/port information](../evidence-images/LAB-09-02-server-ports.png)
```

---

# Lab 10 — 4.4.4 Locating Log Files

**Primary domain:** 02 Log/Event Analysis

### Questions / tasks
1. Locate Linux log files.
2. Identify application, service and system logs.
3. Inspect log content.
4. Determine which logs are useful for investigation.

### Expected answer/result
Linux maintains different logs for system, authentication, services and applications. The correct log path depends on the event being investigated; record the path and relevant entries found in the lab.

### Evidence labels
```markdown
![LAB-10-01 — Log file locations](../evidence-images/LAB-10-01-log-locations.png)
![LAB-10-02 — Log entries](../evidence-images/LAB-10-02-log-entries.png)
```

---

# Lab 11 — 4.5.4 Navigating the Linux Filesystem and Permission Settings

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Explore mounted filesystems.
2. Navigate the Linux directory structure.
3. Examine file ownership and permissions.
4. Modify permissions as instructed.

### Expected answer/result
Linux uses a hierarchical filesystem and permission model. Record the relevant owner/group/permission values and verify the requested change.

### Evidence labels
```markdown
![LAB-11-01 — Filesystem](../evidence-images/LAB-11-01-filesystem.png)
![LAB-11-02 — Permissions](../evidence-images/LAB-11-02-permissions.png)
```

---

# Lab 12 — 5.1.5 Tracing a Route

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Verify connectivity with ping.
2. Trace the route to a remote system.
3. Identify intermediate hops.
4. Interpret the route output.

### Expected answer/result
Ping verifies reachability; traceroute/tracert reveals the path through intermediate routers. Record the observed hop sequence and any latency/timeouts.

### Evidence labels
```markdown
![LAB-12-01 — Ping verification](../evidence-images/LAB-12-01-ping.png)
![LAB-12-02 — Route trace](../evidence-images/LAB-12-02-traceroute.png)
```

---

# Lab 13 — 5.3.7 Introduction to Wireshark

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Start the simulated Mininet topology.
2. Capture traffic in Wireshark.
3. Identify ICMP request/reply packets.
4. Inspect packet fields and filtering.

### Expected answer/result
Wireshark captures and decodes packets. ICMP request/reply traffic can be identified by protocol and packet fields; record the relevant source/destination and ICMP information.

### Evidence labels
```markdown
![LAB-13-01 — Wireshark capture](../evidence-images/LAB-13-01-wireshark-capture.png)
![LAB-13-02 — ICMP packet details](../evidence-images/LAB-13-02-icmp-details.png)
```

---

# Lab 14 — 8.2.8 Using Wireshark to Examine Ethernet Frames

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Inspect an Ethernet II frame.
2. Identify source/destination MAC addresses.
3. Identify EtherType and frame fields.
4. Capture and inspect generated traffic.

### Expected answer/result
The Ethernet frame contains MAC addressing, EtherType and other Layer 2 fields. Record the values visible in the simulated capture.

### Evidence labels
```markdown
![LAB-14-01 — Ethernet frame](../evidence-images/LAB-14-01-ethernet-frame.png)
![LAB-14-02 — Ethernet field details](../evidence-images/LAB-14-02-ethernet-fields.png)
```

---

# Lab 15 — 9.2.6 Using Wireshark to Observe the TCP 3-Way Handshake

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Capture a TCP session.
2. Identify SYN, SYN-ACK and ACK packets.
3. Record source/destination addresses and ports.
4. Explain the connection-establishment sequence.

### Expected answer/result
The TCP three-way handshake consists of SYN → SYN-ACK → ACK. Record the packet numbers, addresses, ports and TCP flags visible in the simulated capture.

### Evidence labels
```markdown
![LAB-15-01 — TCP SYN](../evidence-images/LAB-15-01-tcp-syn.png)
![LAB-15-02 — TCP SYN-ACK](../evidence-images/LAB-15-02-tcp-syn-ack.png)
![LAB-15-03 — TCP ACK](../evidence-images/LAB-15-03-tcp-ack.png)
```

---

# Lab 16 — 9.3.8 Exploring Nmap

**Primary domain:** 06 Vulnerability Scanning

### Questions / tasks
1. Explore Nmap options.
2. Perform the specified authorized scan against the simulated target.
3. Identify open ports/services.
4. Interpret the scan result.

### Expected answer/result
Nmap identifies hosts, ports and services according to the scan options used. Record the exact authorized laboratory target, command and observed open ports/services.

**Important:** This is a laboratory scan only. Do not scan production or third-party systems.

### Evidence labels
```markdown
![LAB-16-01 — Nmap command](../evidence-images/LAB-16-01-nmap-command.png)
![LAB-16-02 — Nmap scan results](../evidence-images/LAB-16-02-nmap-results.png)
```

---

# Lab 17 — 10.2.7 Using Wireshark to Examine a UDP DNS Capture

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Record the simulated host IP configuration.
2. Capture DNS traffic.
3. Identify DNS query and response packets.
4. Inspect UDP and DNS fields.

### Expected answer/result
DNS queries and responses can be identified by DNS message type, transaction ID, queried name, response records and UDP ports.

### Evidence labels
```markdown
![LAB-17-01 — Host IP configuration](../evidence-images/LAB-17-01-ip-config.png)
![LAB-17-02 — DNS query](../evidence-images/LAB-17-02-dns-query.png)
![LAB-17-03 — DNS response](../evidence-images/LAB-17-03-dns-response.png)
```

---

# Lab 18 — 10.4.3 Using Wireshark to Examine TCP and UDP Captures

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Analyze the provided TCP capture.
2. Analyze the provided UDP capture.
3. Identify protocols, ports, addresses and payload/application information.
4. Compare TCP and UDP behavior.

### Expected answer/result
TCP provides connection-oriented transport with sequencing/acknowledgment, while UDP is connectionless. Record the protocol-specific observations from the supplied training captures.

### Evidence labels
```markdown
![LAB-18-01 — TCP capture](../evidence-images/LAB-18-01-tcp-capture.png)
![LAB-18-02 — UDP capture](../evidence-images/LAB-18-02-udp-capture.png)
```

---

# Lab 19 — 10.6.7 Using Wireshark to Examine HTTP and HTTPS Traffic

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Capture/examine HTTP traffic.
2. Identify HTTP requests and responses.
3. Examine HTTPS/TLS traffic.
4. Compare what information is visible in HTTP versus HTTPS.

### Expected answer/result
HTTP exposes application-layer request/response information in plaintext, while HTTPS protects application content through TLS encryption. Record the visible fields and TLS information from the simulated capture.

### Evidence labels
```markdown
![LAB-19-01 — HTTP request](../evidence-images/LAB-19-01-http-request.png)
![LAB-19-02 — HTTP response](../evidence-images/LAB-19-02-http-response.png)
![LAB-19-03 — HTTPS/TLS](../evidence-images/LAB-19-03-https-tls.png)
```

---

# Lab 20 — 17.1.7 Exploring DNS Traffic

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Capture DNS query traffic.
2. Examine query fields.
3. Examine DNS responses.
4. Identify suspicious or notable DNS behavior in the supplied training traffic.

### Expected answer/result
Record queried domains, query/response types, returned addresses and other relevant DNS fields. Any suspicious finding must be based on the provided training traffic.

### Evidence labels
```markdown
![LAB-20-01 — DNS query traffic](../evidence-images/LAB-20-01-dns-query.png)
![LAB-20-02 — DNS response traffic](../evidence-images/LAB-20-02-dns-response.png)
```

---

# Lab 21 — 17.2.6 Attacking a mySQL Database

**Primary domain:** 07 Incident Investigation

### Questions / tasks
1. Perform the assigned database-security exercise against the intentionally vulnerable training database.
2. Observe the attack behavior.
3. Identify relevant network/database evidence.
4. Determine what security weakness was demonstrated.

### Expected answer/result
The lab demonstrates how database attacks appear in network/application evidence. Record the simulated attack technique, affected training service and observed evidence.

### Evidence labels
```markdown
![LAB-21-01 — Database lab setup](../evidence-images/LAB-21-01-database-lab.png)
![LAB-21-02 — Simulated attack evidence](../evidence-images/LAB-21-02-attack-evidence.png)
![LAB-21-03 — Result/analysis](../evidence-images/LAB-21-03-analysis.png)
```

---

# Lab 22 — 17.2.7 Reading Server Logs

**Primary domain:** 02 Log/Event Analysis

### Questions / tasks
1. Locate the relevant server logs.
2. Read and interpret log entries.
3. Identify notable requests/events.
4. Use log information to understand the simulated activity.

### Expected answer/result
Server logs provide timestamped records of service activity. Record the relevant event, source, destination/request information and interpretation from the supplied training data.

### Evidence labels
```markdown
![LAB-22-01 — Server log](../evidence-images/LAB-22-01-server-log.png)
![LAB-22-02 — Relevant log event](../evidence-images/LAB-22-02-log-event.png)
```

---

# Lab 23 — 21.0.3 Creating Codes

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Create/use the assigned cryptographic code examples.
2. Observe how encoding/encryption changes data.
3. Record the resulting values.

### Expected answer/result
The output depends on the assigned cryptographic operation. Record the actual controlled-lab output and explain the security property demonstrated.

### Evidence labels
```markdown
![LAB-23-01 — Code/cryptographic operation](../evidence-images/LAB-23-01-code-operation.png)
![LAB-23-02 — Result](../evidence-images/LAB-23-02-code-result.png)
```

---

# Lab 24 — 21.1.6 Hashing Things Out

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Generate hashes for the supplied training files/data.
2. Compare hash values.
3. Determine what happens when the input changes.
4. Explain the use of hashes in security investigations.

### Expected answer/result
A cryptographic hash changes substantially when the input changes and can be used to identify/verify a file or other data. Record the algorithm and resulting hash values.

### Evidence labels
```markdown
![LAB-24-01 — Hash command](../evidence-images/LAB-24-01-hash-command.png)
![LAB-24-02 — Hash results](../evidence-images/LAB-24-02-hash-results.png)
```

---

# Lab 25 — 21.2.10 Encrypting and Decrypting Data Using OpenSSL

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Encrypt the assigned training data using OpenSSL.
2. Decrypt it using the required parameters.
3. Verify the decrypted result.

### Expected answer/result
Successful decryption should reproduce the original training data when the correct key/parameters are used.

### Evidence labels
```markdown
![LAB-25-01 — OpenSSL encryption](../evidence-images/LAB-25-01-openssl-encryption.png)
![LAB-25-02 — OpenSSL decryption](../evidence-images/LAB-25-02-openssl-decryption.png)
```

---

# Lab 26 — 21.2.11 Encrypting and Decrypting Data Using a Hacker Tool

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Use the assigned training security tool to encrypt data.
2. Decrypt the data using the required procedure.
3. Compare the original and recovered data.

### Expected answer/result
The recovered training data should match the original when the correct procedure/key is used. Record the controlled-lab output.

### Evidence labels
```markdown
![LAB-26-01 — Encryption tool](../evidence-images/LAB-26-01-encryption-tool.png)
![LAB-26-02 — Decryption result](../evidence-images/LAB-26-02-decryption-result.png)
```

---

# Lab 27 — 21.2.12 Examining Telnet and SSH in Wireshark

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Capture Telnet traffic.
2. Identify information visible in the Telnet stream.
3. Capture SSH traffic.
4. Compare visibility between Telnet and SSH.

### Expected answer/result
Telnet transmits application content without the protection provided by SSH encryption; SSH encrypts the session. Record the relevant packet/stream evidence.

### Evidence labels
```markdown
![LAB-27-01 — Telnet traffic](../evidence-images/LAB-27-01-telnet.png)
![LAB-27-02 — SSH traffic](../evidence-images/LAB-27-02-ssh.png)
![LAB-27-03 — Protocol comparison](../evidence-images/LAB-27-03-protocol-comparison.png)
```

---

# Lab 28 — 21.4.7 Certificate Authority Stores

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Examine certificate stores in the simulated environment.
2. Identify trusted certificate authorities.
3. Inspect certificate details.
4. Explain why trusted CA stores matter to endpoint security.

### Expected answer/result
Certificate stores contain trusted CA certificates used to validate certificate chains. Record the relevant issuer/subject/validity information visible in the lab.

### Evidence labels
```markdown
![LAB-28-01 — Certificate store](../evidence-images/LAB-28-01-certificate-store.png)
![LAB-28-02 — Certificate details](../evidence-images/LAB-28-02-certificate-details.png)
```

---

# Lab 29 — 26.1.7 Snort and Firewall Rules

**Primary domain:** 01 Monitoring and Alerts

### Questions / tasks
1. Examine Snort detection rules.
2. Examine firewall rules.
3. Generate/observe the assigned simulated traffic.
4. Identify the resulting alert or filtering behavior.
5. Explain how detection and firewall controls complement one another.

### Expected answer/result
Snort can detect matching traffic using IDS rules; firewall rules can permit/block traffic according to configured conditions. Record the simulated alert and corresponding rule/control.

### Evidence labels
```markdown
![LAB-29-01 — Snort rule](../evidence-images/LAB-29-01-snort-rule.png)
![LAB-29-02 — Simulated alert](../evidence-images/LAB-29-02-snort-alert.png)
![LAB-29-03 — Firewall rule](../evidence-images/LAB-29-03-firewall-rule.png)
```

---

# Lab 30 — 27.1.5 Convert Data into a Universal Format

**Primary domain:** 02 Log/Event Analysis

### Questions / tasks
1. Convert supplied security data into the requested normalized format.
2. Inspect the converted fields.
3. Explain why normalized data helps security analysis.

### Expected answer/result
The converted data should follow the specified universal/normalized format while preserving the required security information.

### Evidence labels
```markdown
![LAB-30-01 — Source data](../evidence-images/LAB-30-01-source-data.png)
![LAB-30-02 — Normalized data](../evidence-images/LAB-30-02-normalized-data.png)
```

---

# Lab 31 — 27.2.9 Regular Expression Tutorial

**Primary domain:** 02 Log/Event Analysis

### Questions / tasks
1. Build/test regular expressions using the supplied examples.
2. Match the required security-data patterns.
3. Extract relevant values from the supplied data.
4. Explain how regex supports security-data analysis.

### Expected answer/result
The correct expression matches the requested pattern and extracts the intended field/value from the training data. Record the expression and sample result.

### Evidence labels
```markdown
![LAB-31-01 — Regex expression](../evidence-images/LAB-31-01-regex.png)
![LAB-31-02 — Regex match/result](../evidence-images/LAB-31-02-regex-result.png)
```

---

# Lab 32 — 27.2.10 Extract an Executable from a PCAP

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Locate the relevant network session in the training PCAP.
2. Extract the transferred executable.
3. Identify the extracted file.
4. Calculate/record its hash.
5. Use the artifact for further analysis as instructed.

### Expected answer/result
The executable should be extracted from the simulated capture and identified by filename/hash. Record the artifact and hash without uploading prohibited or real-world malicious material.

### Evidence labels
```markdown
![LAB-32-01 — Relevant PCAP session](../evidence-images/LAB-32-01-pcap-session.png)
![LAB-32-02 — Extracted executable](../evidence-images/LAB-32-02-extracted-executable.png)
![LAB-32-03 — File hash](../evidence-images/LAB-32-03-file-hash.png)
```

---

# Lab 33 — 27.2.12 Interpret HTTP and DNS Data to Isolate Threat Actor

**Primary domain:** 07 Incident Investigation

### Questions / tasks
1. Analyze supplied HTTP and DNS security data.
2. Identify suspicious domains/requests/communications.
3. Correlate the network indicators.
4. Identify the simulated threat actor or relevant attack indicators.

### Expected answer/result
The answer is derived by correlating the HTTP and DNS indicators in the supplied training data. Record the relevant domain/IP/request evidence and the resulting simulated threat-actor assessment.

### Evidence labels
```markdown
![LAB-33-01 — HTTP evidence](../evidence-images/LAB-33-01-http-evidence.png)
![LAB-33-02 — DNS evidence](../evidence-images/LAB-33-02-dns-evidence.png)
![LAB-33-03 — Correlated threat indicator](../evidence-images/LAB-33-03-threat-indicator.png)
```

---

# Lab 34 — 27.2.14 Isolate Compromised Host Using 5-Tuple

**Primary domain:** 07 Incident Investigation

### Questions / tasks
1. Use the supplied network-security data to identify the relevant 5-tuple.
2. Identify the simulated compromised host.
3. Correlate source/destination IPs and ports.
4. Determine which host should be isolated in the training scenario.

### Expected answer/result
The compromised host is identified by correlating source IP, source port, destination IP, destination port and protocol. The exercise demonstrates identification for simulated isolation; it is not production containment.

### Evidence labels
```markdown
![LAB-34-01 — 5-tuple evidence](../evidence-images/LAB-34-01-five-tuple.png)
![LAB-34-02 — Compromised host](../evidence-images/LAB-34-02-compromised-host.png)
```

---

# Lab 35 — 27.2.15 Investigating a Malware Exploit

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Investigate the simulated malware exploit using the supplied evidence.
2. Identify the exploited service/host or relevant attack vector.
3. Identify malicious artifacts/indicators.
4. Correlate the evidence and determine what occurred.

### Expected answer/result
The answer is obtained by correlating the supplied network/endpoint/security evidence to identify the exploit path, affected simulated system and malware indicators.

### Evidence labels
```markdown
![LAB-35-01 — Exploit evidence](../evidence-images/LAB-35-01-exploit-evidence.png)
![LAB-35-02 — Malware indicator](../evidence-images/LAB-35-02-malware-indicator.png)
![LAB-35-03 — Investigation result](../evidence-images/LAB-35-03-investigation-result.png)
```

---

# Lab 36 — 27.2.16 Investigating an Attack on a Windows Host

**Primary domain:** 07 Incident Investigation

### Questions / tasks
1. Investigate the simulated Windows-host attack using Sguil and/or the specified analysis tools.
2. Identify the relevant alerts/events.
3. Determine the affected host and attack timeframe.
4. Identify files, hashes, network indicators and other relevant evidence.
5. Correlate the evidence and summarize the incident.

### Expected answer/result
The investigation should establish the simulated incident timeline, affected Windows host, attack indicators, relevant files/hashes and supporting network/security evidence. The final answer is the evidence-supported incident finding.

### Evidence labels
```markdown
![LAB-36-01 — Initial alert](../evidence-images/LAB-36-01-initial-alert.png)
![LAB-36-02 — Affected Windows host](../evidence-images/LAB-36-02-affected-host.png)
![LAB-36-03 — Network/event evidence](../evidence-images/LAB-36-03-network-event.png)
![LAB-36-04 — Malware/file evidence](../evidence-images/LAB-36-04-malware-file.png)
![LAB-36-05 — Investigation conclusion](../evidence-images/LAB-36-05-investigation-conclusion.png)
```

---

# Evidence completion checklist

For each lab that the candidate actually completes:

- [ ] Lab performed in the authorized simulated/isolated environment.
- [ ] Question/task answered from the actual lab result.
- [ ] Actual command/output recorded where applicable.
- [ ] Screenshot captured only when it provides useful evidence.
- [ ] Screenshot renamed using the `LAB-XX-NN-description.png` standard.
- [ ] Screenshot label inserted into the relevant Markdown evidence file.
- [ ] Observation written in the candidate's own words.
- [ ] Interpretation written in the candidate's own words.
- [ ] Primary evidence domain recorded.
- [ ] TESDA relevance recorded without overclaiming competency.
- [ ] No production/confidential/PII evidence included.

## Evidence principle

The ITExamAnswers material is a **reference/cross-check source**. It must not be represented as the candidate's own completed lab evidence. The candidate's actual laboratory screenshots, commands, outputs and observations are the portfolio evidence.

## Source basis

The activity sequence and answer cross-checks are based on the CyberOps Associate v1.0 lab catalog and the corresponding ITExamAnswers CyberOps lab-answer pages. The catalog identifies the 36 hands-on labs used in this portfolio. citehttps://itexamanswers.net/ccna-cyberops-associate-version-1-0-exam-answers.html
