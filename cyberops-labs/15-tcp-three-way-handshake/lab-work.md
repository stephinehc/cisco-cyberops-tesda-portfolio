# Lab 15 — TCP 3-Way Handshake

**Cisco activity:** 9.2.6  
**Primary domain:** 03 Network Traffic Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Capture the designated TCP session.
2. Filter the saved capture for TCP.
3. Identify SYN, SYN-ACK and ACK.
4. Record source/destination IPs and TCP ports.
5. Inspect TCP control flags.

**Answer / observation:** The connection starts with SYN, followed by SYN-ACK from the server and ACK from the client. The source port is a dynamic/private client port in the example; the training HTTP service uses destination port 80.

## Evidence

**Figure 1 — SYN:** `LAB-15-01-tcp-syn.png`  
> **Attach:** `screenshots/LAB-15-01-tcp-syn.png`

**Figure 2 — SYN-ACK:** `LAB-15-02-tcp-syn-ack.png`  
> **Attach:** `screenshots/LAB-15-02-tcp-syn-ack.png`

**Figure 3 — ACK:** `LAB-15-03-tcp-ack.png`  
> **Attach:** `screenshots/LAB-15-03-tcp-ack.png`

## Interpretation
TCP flag and port analysis supports network-session investigation.
