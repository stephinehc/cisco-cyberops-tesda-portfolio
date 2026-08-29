# Lab 18 — TCP and UDP Captures

**Cisco activity:** 10.4.3  
**Primary domain:** 03 Network Traffic Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Capture/analyze the supplied FTP TCP session.
2. Identify TCP header fields and operation.
3. Capture/analyze the supplied TFTP UDP session.
4. Identify UDP header fields and operation.
5. Compare TCP and UDP behavior.

**Answer / observation:** TCP provides connection-oriented transport with sequence/control information. UDP uses a compact header containing source port, destination port, length and checksum; application protocols such as TFTP handle transfer control above UDP.

## Evidence

**Figure 1 — TCP/FTP capture:** `LAB-18-01-tcp-capture.png`  
> **Attach:** `screenshots/LAB-18-01-tcp-capture.png`

**Figure 2 — UDP/TFTP capture:** `LAB-18-02-udp-capture.png`  
> **Attach:** `screenshots/LAB-18-02-udp-capture.png`

## Interpretation
Transport-layer analysis helps distinguish normal protocol behavior from suspicious traffic.
