# Lab 21 — Attacking a MySQL Database

**Cisco activity:** 17.2.6  
**Primary domain:** 07 Incident Investigation  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Open the supplied training PCAP.
2. Identify the simulated SQL injection activity.
3. Follow the attack through its stages.
4. Identify database/system information exposed by the attack.
5. Identify table/data information and the concluding activity.

**Answer / observation:** The training capture demonstrates SQL injection as a code-injection technique in which malicious SQL statements are sent through a web application to influence the database. The investigation should identify the injected statements, returned information and affected database context.

## Evidence

**Figure 1 — SQL injection traffic:** `LAB-21-01-sql-injection.png`  
> **Attach:** `screenshots/LAB-21-01-sql-injection.png`

**Figure 2 — Database information:** `LAB-21-02-database-information.png`  
> **Attach:** `screenshots/LAB-21-02-database-information.png`

**Figure 3 — Attack conclusion:** `LAB-21-03-attack-conclusion.png`  
> **Attach:** `screenshots/LAB-21-03-attack-conclusion.png`

## Interpretation
PCAP-based SQL-injection analysis demonstrates incident investigation and network/application evidence correlation.
