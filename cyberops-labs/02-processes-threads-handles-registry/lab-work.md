# Lab 02 — Processes, Threads, Handles and Windows Registry

**Cisco activity:** 3.2.11  
**Primary domain:** 04 Endpoint Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

### Task 1 — Explore an active process
Use Process Explorer to inspect a running process.

**Observation:** Process Explorer provides process details including executable information, performance/security context and related objects.

### Task 2 — Explore threads
**Question:** What information is available for a process thread?

**Answer:** Thread properties can expose environment, security, performance and printable-string information.

### Task 3 — Explore handles
**Question:** What can process handles point to?

**Answer:** Handles can reference files, Registry keys, threads and other operating-system-managed objects.

### Task 4 — Examine the Registry
**Observation:** The Windows Registry is a hierarchical configuration database. Major hives include `HKEY_CLASSES_ROOT`, `HKEY_CURRENT_USER`, `HKEY_LOCAL_MACHINE`, `HKEY_USERS`, and `HKEY_CURRENT_CONFIG`.

## Evidence

**Figure 1 — Process Explorer**  
`LAB-02-01-process-explorer.png`

> **Attach screenshot here:** `screenshots/LAB-02-01-process-explorer.png`

**Figure 2 — Threads and handles**  
`LAB-02-02-threads-handles.png`

> **Attach screenshot here:** `screenshots/LAB-02-02-threads-handles.png`

**Figure 3 — Registry inspection**  
`LAB-02-03-registry.png`

> **Attach screenshot here:** `screenshots/LAB-02-03-registry.png`

## Interpretation
Process, thread, handle and Registry visibility provides useful endpoint-investigation context, including potential persistence or configuration evidence.
