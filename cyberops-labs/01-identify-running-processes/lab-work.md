# Lab 01 — Identify Running Processes

**Cisco activity:** 3.0.3 Identify Running Processes  
**Primary domain:** 04 Endpoint Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

### Task 1 — Identify running processes
Use the process/network viewer to inspect active processes and endpoints.

**Answer / observation:** The utility lists active Windows processes together with process and connection information. A newly opened browser creates additional process entries; closing it removes the corresponding entries.

### Task 2 — Identify `lsass.exe`
**Question:** What is `lsass.exe` and where is it normally located?

**Answer:** `lsass.exe` is the Local Security Authority Subsystem Service and is normally located in `C:\Windows\System32\`.

### Task 3 — Observe a user-started process
**Observation:** Opening a browser adds its processes to the process/endpoint viewer; closing the browser removes those processes.

## Evidence

**Figure 1 — Running-process view**  
`LAB-01-01-process-list.png`

> **Attach screenshot here:** `screenshots/LAB-01-01-process-list.png`

**Figure 2 — Process properties / endpoint information**  
`LAB-01-02-process-network-endpoint.png`

> **Attach screenshot here:** `screenshots/LAB-01-02-process-network-endpoint.png`

## Interpretation
Process and endpoint visibility supports endpoint monitoring and investigation by associating applications with network activity.
