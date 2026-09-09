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

<img width="1920" height="1080" alt="LAB-02-01-process-explorer png" src="https://github.com/user-attachments/assets/401e3522-839f-4732-b99f-1b4304baae5c" />


**Figure 2 — Threads and handles**  

Threads
<img width="1920" height="1080" alt="LAB-02-02-threads png" src="https://github.com/user-attachments/assets/7d05e183-7e11-4cab-866c-a3ab95ee5142" />

Handles
<img width="1920" height="1080" alt="LAB-02-02-handles png" src="https://github.com/user-attachments/assets/a4842dcc-23ec-4135-b28d-e48bcaaf4641" />


**Figure 3 — Registry inspection**  
<img width="1920" height="1080" alt="Screenshot 2026-09-09 212927" src="https://github.com/user-attachments/assets/69cfd068-5209-45ed-94b6-059312f9cff6" />
<img width="1920" height="1080" alt="Screenshot 2026-09-09 212941" src="https://github.com/user-attachments/assets/cedb1f76-9395-4df6-9e14-e3025acd2af6" />
<img width="1920" height="1080" alt="Screenshot 2026-09-09 213020" src="https://github.com/user-attachments/assets/6449896c-1013-4971-bd30-8f9a5fdb205c" />
<img width="1407" height="742" alt="Screenshot 2026-09-09 213147" src="https://github.com/user-attachments/assets/603a6864-bec1-43d8-ab4e-0f90b7d186fa" />
<img width="1920" height="1020" alt="Screenshot 2026-09-09 213217" src="https://github.com/user-attachments/assets/90f60c81-1cef-4f60-94f5-8e8c5bffc8c2" />


## Interpretation
Process, thread, handle and Registry visibility provides useful endpoint-investigation context, including potential persistence or configuration evidence.
