# Lab 27 — Examining Telnet and SSH in Wireshark

**Cisco activity:** 21.2.12  
**Primary domain:** 03 Network Traffic Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Capture a local Telnet session.
2. Inspect the Telnet stream in Wireshark.
3. Capture a local SSH session.
4. Follow the SSH TCP stream and compare visibility.

**Answer / observation:** Telnet transmits session data in readable form in the training capture, whereas SSH traffic is encrypted and the application data is not readable in the same way.

**Reflection answer:** SSH is preferred because it encrypts remote-session communication and protects sensitive information such as credentials from simple packet inspection.

## Evidence

**Figure 1 — Telnet capture:** `LAB-27-01-telnet-capture.png`  
> **Attach:** `screenshots/LAB-27-01-telnet-capture.png`

**Figure 2 — Telnet readable stream:** `LAB-27-02-telnet-stream.png`  
> **Attach:** `screenshots/LAB-27-02-telnet-stream.png`

**Figure 3 — SSH encrypted stream:** `LAB-27-03-ssh-stream.png`  
> **Attach:** `screenshots/LAB-27-03-ssh-stream.png`

## Interpretation
Comparing plaintext and encrypted remote sessions demonstrates the importance of secure protocols during network analysis.
