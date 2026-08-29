# Lab 32 — Extract an Executable from a PCAP

**Cisco activity:** 27.2.10  
**Primary domain:** 05 Malware/IOC Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Analyze the supplied logs and PCAP.
2. Locate the simulated malware download.
3. Export the executable object from HTTP traffic.
4. Record the file name and calculate its hash.

**Answer / observation:** The supplied training PCAP contains traffic associated with a simulated executable download. Wireshark's HTTP object export can recover the file, after which a cryptographic hash can be calculated for IOC analysis.

## Evidence

**Figure 1 — PCAP investigation:** `LAB-32-01-pcap-analysis.png`  
> **Attach:** `screenshots/LAB-32-01-pcap-analysis.png`

**Figure 2 — Exported executable:** `LAB-32-02-extracted-executable.png`  
> **Attach:** `screenshots/LAB-32-02-extracted-executable.png`

**Figure 3 — File hash:** `LAB-32-03-file-hash.png`  
> **Attach:** `screenshots/LAB-32-03-file-hash.png`

## Interpretation
This lab directly supports malware/IOC analysis through network-to-file correlation.
