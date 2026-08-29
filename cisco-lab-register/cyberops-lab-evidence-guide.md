# Cisco CyberOps Associate v1.0 — Lab Evidence Guide

## Purpose

This guide provides a portfolio-ready evidence template for the **36 Cisco CyberOps Associate v1.0 hands-on laboratory activities** in the master register.

The questions/tasks and expected results are paraphrased from reference material used to cross-check the laboratory activities. They are provided as study and documentation guidance only and are not a substitute for the original Cisco lab instructions or candidate evidence.

## Controlled-environment and data-privacy statement

All activities documented in this portfolio must be performed only in a **simulated, isolated, and controlled laboratory environment** using authorized training virtual machines, simulated networks, packet captures, training datasets, and intentionally configured systems.

Do not use production systems, live organizational networks, confidential company information, personally identifiable information, production credentials, private keys, or real organizational security events.

## Evidence image naming standard

Use the following standardized naming convention:

```text
LAB-XX-01-short-description.png
LAB-XX-02-short-description.png
LAB-XX-03-short-description.png
```

`XX` is the portfolio lab number in this guide, not the Cisco module number.

Example:

```text
LAB-16-01-nmap-scan-command.png
LAB-16-02-nmap-scan-results.png
```

Do not create placeholder images. If an activity does not require a screenshot, record the actual command/output or observation as text.

## Evidence workflow

```text
Controlled laboratory activity
        ↓
Lab question / task
        ↓
Learner performs the activity
        ↓
Actual result / observation
        ↓
Screenshot or command output
        ↓
Interpretation
        ↓
Evidence domain
        ↓
TESDA relevance
```

The expected results below are **reference guidance only**. Final evidence must come from the learner's own controlled laboratory run.

---

# Lab 01 — 3.0.3 Identify Running Processes

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Identify running processes on the simulated Windows host.
2. Identify a process associated with a selected network connection.
3. Record the process name, PID and relevant endpoint information.

### Expected result
The process/network-viewing utility should display active processes and associated local/remote endpoints.

### Evidence labels
```markdown
![LAB-01-01 — Running process list](../evidence-images/LAB-01-01-process-list.png)
![LAB-01-02 — Process and network endpoint](../evidence-images/LAB-01-02-process-network-endpoint.png)
```

---

# Lab 02 — 3.2.11 Exploring Processes, Threads, Handles, and Windows Registry

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Inspect a process using Process Explorer.
2. Examine its threads and handles.
3. Inspect relevant Registry information.
4. Identify information useful to endpoint investigation.

### Expected result
Process Explorer provides process, thread, handle and module information; Registry inspection provides configuration and persistence-related context where applicable.

### Evidence labels
```markdown
![LAB-02-01 — Process Explorer](../evidence-images/LAB-02-01-process-explorer.png)
![LAB-02-02 — Threads and handles](../evidence-images/LAB-02-02-threads-handles.png)
![LAB-02-03 — Registry evidence](../evidence-images/LAB-02-03-registry.png)
```

---

# Lab 03 — 3.3.10 Create User Accounts

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Create the requested local user account.
2. Configure its properties/group membership.
3. Verify the resulting account configuration.

### Expected result
The requested account is created with the specified properties and can be verified through the Windows account-management interface or command output.

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
2. Execute basic PowerShell commands.
3. Use PowerShell to inspect the simulated host.
4. Record useful output.

### Expected result
PowerShell provides command-line administration and investigation functions. Record the actual commands and outputs produced in the laboratory.

### Evidence labels
```markdown
![LAB-04-01 — PowerShell console](../evidence-images/LAB-04-01-powershell-console.png)
![LAB-04-02 — PowerShell output](../evidence-images/LAB-04-02-powershell-output.png)
```

---

# Lab 05 — 3.3.12 Windows Task Manager

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Examine running processes.
2. Identify resource-intensive processes.
3. Inspect process/resource information.
4. Perform the instructed laboratory process-management action.

### Expected result
Task Manager displays process, performance and resource information needed for the assigned analysis.

### Evidence labels
```markdown
![LAB-05-01 — Task Manager processes](../evidence-images/LAB-05-01-task-manager-processes.png)
![LAB-05-02 — Task Manager performance](../evidence-images/LAB-05-02-task-manager-performance.png)
```

---

# Lab 06 — 3.3.13 Monitor and Manage System Resources in Windows

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Open the specified resource-monitoring tools.
2. Observe CPU, memory, disk and/or network utilization.
3. Identify processes associated with resource consumption.
4. Perform the instructed laboratory management action.

### Expected result
The Windows resource-monitoring tools display current utilization and process/resource relationships.

### Evidence labels
```markdown
![LAB-06-01 — Resource monitoring](../evidence-images/LAB-06-01-resource-monitor.png)
![LAB-06-02 — Resource/process details](../evidence-images/LAB-06-02-resource-process-details.png)
```

---

# Lab 07 — 4.2.6 Working with Text Files in the CLI

**Primary domain:** 02 Log/Event Analysis

### Questions / tasks
1. Inspect text files using Linux CLI tools.
2. Create or modify a text file as instructed.
3. Inspect configuration-file content.
4. Record commands and results.

### Expected result
The required text/configuration files can be located and processed from the Linux command line.

### Evidence labels
```markdown
![LAB-07-01 — Text-file command](../evidence-images/LAB-07-01-text-file-command.png)
![LAB-07-02 — Configuration/text file](../evidence-images/LAB-07-02-config-file.png)
```

---

# Lab 08 — 4.2.7 Getting Familiar with the Linux Shell

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Navigate the Linux filesystem.
2. Create, copy, move and remove files/directories as instructed.
3. Use basic shell commands.
4. Verify the resulting state.

### Expected result
The requested filesystem and shell operations complete successfully and the resulting state can be verified.

### Evidence labels
```markdown
![LAB-08-01 — Linux shell](../evidence-images/LAB-08-01-linux-shell.png)
![LAB-08-02 — File-management output](../evidence-images/LAB-08-02-file-management.png)
```

---

# Lab 09 — 4.3.4 Linux Servers

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Identify services running on the simulated Linux host.
2. Identify associated listening ports.
3. Determine available services.

### Expected result
Linux commands identify listening services, processes and ports in the training environment.

### Evidence labels
```markdown
![LAB-09-01 — Listening services](../evidence-images/LAB-09-01-listening-services.png)
![LAB-09-02 — Server and port information](../evidence-images/LAB-09-02-server-ports.png)
```

---

# Lab 10 — 4.4.4 Locating Log Files

**Primary domain:** 02 Log/Event Analysis

### Questions / tasks
1. Locate Linux log files.
2. Identify system, authentication, service and application logs.
3. Inspect relevant entries.
4. Determine which logs support investigation.

### Expected result
The relevant log locations and entries are identified according to the activity being investigated.

### Evidence labels
```markdown
![LAB-10-01 — Log-file locations](../evidence-images/LAB-10-01-log-locations.png)
![LAB-10-02 — Relevant log entries](../evidence-images/LAB-10-02-log-entries.png)
```

---

# Lab 11 — 4.5.4 Navigating the Linux Filesystem and Permission Settings

**Primary domain:** 04 Endpoint Analysis

### Questions / tasks
1. Navigate the Linux filesystem.
2. Inspect ownership and permissions.
3. Modify permissions as instructed.
4. Verify the resulting settings.

### Expected result
The relevant owner, group and permission values are identified and the requested change is verified.

### Evidence labels
```markdown
![LAB-11-01 — Linux filesystem](../evidence-images/LAB-11-01-filesystem.png)
![LAB-11-02 — File permissions](../evidence-images/LAB-11-02-permissions.png)
```

---

# Lab 12 — 5.1.5 Tracing a Route

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Verify connectivity.
2. Trace the route to the assigned laboratory destination.
3. Identify intermediate hops.
4. Interpret the route output.

### Expected result
Ping verifies reachability and traceroute/tracert displays the observed path and hop information.

### Evidence labels
```markdown
![LAB-12-01 — Ping verification](../evidence-images/LAB-12-01-ping.png)
![LAB-12-02 — Route trace](../evidence-images/LAB-12-02-traceroute.png)
```

---

# Lab 13 — 5.3.7 Introduction to Wireshark

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Start the simulated topology.
2. Capture traffic with Wireshark.
3. Identify ICMP request/reply packets.
4. Inspect packet fields and filters.

### Expected result
Wireshark captures and decodes the generated traffic, allowing ICMP packets and their relevant fields to be identified.

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
3. Identify EtherType and other Layer 2 fields.
4. Interpret the frame.

### Expected result
The selected frame exposes the expected MAC addresses, EtherType and Layer 2 fields.

### Evidence labels
```markdown
![LAB-14-01 — Ethernet frame](../evidence-images/LAB-14-01-ethernet-frame.png)
![LAB-14-02 — Ethernet fields](../evidence-images/LAB-14-02-ethernet-fields.png)
```

---

# Lab 15 — 9.2.6 Using Wireshark to Observe the TCP 3-Way Handshake

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Capture a TCP session.
2. Identify SYN, SYN-ACK and ACK packets.
3. Record addresses and ports.
4. Explain the connection-establishment sequence.

### Expected result
The simulated TCP session demonstrates the sequence SYN → SYN-ACK → ACK with the associated addresses, ports and flags.

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
2. Scan the authorized simulated target.
3. Identify open ports/services.
4. Interpret the scan result.

### Expected result
Nmap reports hosts, ports and services according to the options used against the intentionally configured laboratory target.

**Laboratory-only requirement:** Never scan production or third-party systems.

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
3. Identify DNS queries and responses.
4. Inspect UDP/DNS fields.

### Expected result
The capture exposes the relevant DNS transaction, queried name, response records and UDP information.

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
1. Analyze the supplied TCP capture.
2. Analyze the supplied UDP capture.
3. Identify protocols, addresses, ports and application information.
4. Compare TCP and UDP behavior.

### Expected result
The captures demonstrate the relevant differences between connection-oriented TCP and connectionless UDP traffic.

### Evidence labels
```markdown
![LAB-18-01 — TCP capture](../evidence-images/LAB-18-01-tcp-capture.png)
![LAB-18-02 — UDP capture](../evidence-images/LAB-18-02-udp-capture.png)
```

---

# Lab 19 — 10.6.7 Using Wireshark to Examine HTTP and HTTPS Traffic

**Primary domain:** 03 Network Traffic Analysis

### Questions / tasks
1. Examine HTTP traffic.
2. Identify HTTP requests/responses.
3. Examine HTTPS/TLS traffic.
4. Compare visible information between HTTP and HTTPS.

### Expected result
HTTP exposes application-layer information in the capture, while HTTPS protects application content through TLS. Relevant visible fields and TLS information should be recorded.

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
1. Capture DNS queries.
2. Examine query fields.
3. Examine DNS responses.
4. Identify notable behavior in the supplied training traffic.

### Expected result
The investigation records queried domains, query/response types, returned addresses and other relevant DNS fields.

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
2. Observe the simulated attack.
3. Identify relevant database/network evidence.
4. Determine the demonstrated security weakness.

### Expected result
The activity demonstrates how simulated database attacks can appear in network and application evidence.

### Evidence labels
```markdown
![LAB-21-01 — Database lab setup](../evidence-images/LAB-21-01-database-lab.png)
![LAB-21-02 — Simulated attack evidence](../evidence-images/LAB-21-02-attack-evidence.png)
![LAB-21-03 — Result and analysis](../evidence-images/LAB-21-03-analysis.png)
```

---

# Lab 22 — 17.2.7 Reading Server Logs

**Primary domain:** 02 Log/Event Analysis

### Questions / tasks
1. Locate the relevant server logs.
2. Read and interpret entries.
3. Identify notable requests/events.
4. Use the logs to understand the simulated activity.

### Expected result
The relevant timestamped server events are identified and interpreted in the context of the training scenario.

### Evidence labels
```markdown
![LAB-22-01 — Server log](../evidence-images/LAB-22-01-server-log.png)
![LAB-22-02 — Relevant log event](../evidence-images/LAB-22-02-log-event.png)
```

---

# Lab 23 — 21.0.3 Creating Codes

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Perform the assigned cryptographic coding activity.
2. Observe how the data changes.
3. Record the resulting values.

### Expected result
The assigned coding/cryptographic operation produces the expected controlled-lab output.

### Evidence labels
```markdown
![LAB-23-01 — Code/cryptographic operation](../evidence-images/LAB-23-01-code-operation.png)
![LAB-23-02 — Result](../evidence-images/LAB-23-02-code-result.png)
```

---

# Lab 24 — 21.1.6 Hashing Things Out

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Generate hashes for supplied training data.
2. Compare hash values.
3. Change the input and observe the result.
4. Explain how hashes support security investigations.

### Expected result
A changed input produces a different cryptographic hash, demonstrating how hashes can support file/data identification and verification.

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
3. Verify the recovered content.

### Expected result
Correct decryption reproduces the original training data.

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
2. Decrypt it using the required procedure.
3. Compare original and recovered data.

### Expected result
The recovered training data matches the original when the correct procedure is used.

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
2. Examine information visible in the Telnet stream.
3. Capture SSH traffic.
4. Compare Telnet and SSH visibility.

### Expected result
Telnet exposes session content without the protection provided by SSH, while SSH encrypts the session.

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
1. Examine certificate stores.
2. Identify trusted certificate authorities.
3. Inspect certificate details.
4. Explain their endpoint-security relevance.

### Expected result
The certificate store contains trusted CA certificates and associated issuer, subject and validity information.

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
4. Identify resulting detection/filtering behavior.
5. Explain the role of the controls.

### Expected result
Snort identifies traffic matching configured detection rules while firewall rules enforce configured traffic-control conditions.

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
1. Convert supplied security data into the required normalized format.
2. Inspect the resulting fields.
3. Explain the value of normalized data for analysis.

### Expected result
The converted data follows the requested format while preserving the required security information.

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
3. Extract relevant values.
4. Explain the use of regex in security analysis.

### Expected result
The expression matches the intended pattern and extracts the required value from the training data.

### Evidence labels
```markdown
![LAB-31-01 — Regex expression](../evidence-images/LAB-31-01-regex.png)
![LAB-31-02 — Regex result](../evidence-images/LAB-31-02-regex-result.png)
```

---

# Lab 32 — 27.2.10 Extract an Executable from a PCAP

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Locate the relevant session in the training PCAP.
2. Extract the transferred executable.
3. Identify the file.
4. Calculate/record its hash.

### Expected result
The assigned executable is extracted from the simulated capture and can be identified by filename/hash for further controlled analysis.

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
1. Analyze supplied HTTP and DNS data.
2. Identify suspicious domains/requests/communications.
3. Correlate the network indicators.
4. Identify the simulated threat actor or relevant attack indicators.

### Expected result
The relevant HTTP and DNS indicators are correlated to produce an evidence-supported assessment of the simulated threat activity.

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
1. Identify the relevant 5-tuple from the supplied training data.
2. Identify the simulated compromised host.
3. Correlate source/destination addresses and ports.
4. Determine which host would be isolated in the scenario.

### Expected result
The compromised host is identified by correlating source IP, source port, destination IP, destination port and protocol.

**Scope note:** This demonstrates identification for a simulated scenario; it is not evidence of production containment.

### Evidence labels
```markdown
![LAB-34-01 — 5-tuple evidence](../evidence-images/LAB-34-01-five-tuple.png)
![LAB-34-02 — Compromised host](../evidence-images/LAB-34-02-compromised-host.png)
```

---

# Lab 35 — 27.2.15 Investigating a Malware Exploit

**Primary domain:** 05 Malware/IOC Analysis

### Questions / tasks
1. Investigate the simulated malware exploit.
2. Identify the exploited service/host or attack vector.
3. Identify malicious artifacts/indicators.
4. Correlate the evidence and determine what occurred.

### Expected result
The evidence identifies the simulated exploit path, affected training system and relevant malware indicators.

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
1. Investigate the simulated Windows-host attack using the assigned analysis tools.
2. Identify relevant alerts/events.
3. Determine the affected host and timeframe.
4. Identify files, hashes, network indicators and supporting evidence.
5. Correlate the evidence and summarize the incident.

### Expected result
The investigation establishes a simulated incident timeline, affected Windows host, attack indicators, relevant files/hashes and supporting network/security evidence.

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

For each laboratory activity actually completed:

- [ ] Activity performed in the authorized simulated/isolated environment.
- [ ] Lab question/task answered from the actual laboratory result.
- [ ] Actual command/output recorded where applicable.
- [ ] Useful screenshot(s) captured.
- [ ] Screenshot renamed using the `LAB-XX-##-description.png` standard.
- [ ] Screenshot label inserted into the relevant Markdown evidence file.
- [ ] Observation written in the learner's own words.
- [ ] Interpretation written in the learner's own words.
- [ ] Primary evidence domain recorded.
- [ ] TESDA relevance recorded without overclaiming competency.
- [ ] No production/confidential/PII evidence included.

## Evidence principle

Reference material is used only to cross-check the laboratory questions and expected results. It must not be represented as the learner's own completed practical evidence. The candidate's actual laboratory screenshots, commands, outputs and observations are the portfolio evidence.
