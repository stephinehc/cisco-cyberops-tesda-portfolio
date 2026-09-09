# Lab 03 — Create User Accounts

**Cisco activity:** 3.3.10  
**Primary domain:** 04 Endpoint Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

### Task 1 — Create a local account
Create the assigned local account and verify its properties.

**Answer / observation:** The created account is a local standard account without administrative rights unless the lab explicitly changes its type.

### Task 2 — Review folder permissions
**Question:** Which principals have full control of the new user's folder?

**Answer:** `SYSTEM`, `Administrators`, and the user account itself have full control in the standard laboratory configuration.

**Question:** Can the standard user access another administrator user's protected profile folder?

**Answer:** No. Access is denied unless appropriate permissions are granted.

### Task 3 — Review group membership
**Answer:** The newly created standard user belongs to the `Users` group. The administrative training account belongs to `Users` and `Administrators`.

### Task 4 — Modify and remove the account
Changing the account type to Administrator adds the `Administrators` group. Removing that membership returns the account to standard-user status; the account can then be deleted.

## Evidence

**Figure 1 — User account creation**  
<img width="1352" height="1000" alt="Screenshot 2026-09-09 213637" src="https://github.com/user-attachments/assets/6f31dc99-0a2b-430e-bd2d-56784d5a2389" />


**Figure 2 — Account properties and group membership**  
<img width="527" height="665" alt="Screenshot 2026-09-09 215359" src="https://github.com/user-attachments/assets/4005089e-79df-4f17-a40f-e429147de5bb" />
<img width="597" height="670" alt="Screenshot 2026-09-09 215450" src="https://github.com/user-attachments/assets/b33aec41-461f-409b-ab30-0506abc06196" />
<img width="527" height="665" alt="Screenshot 2026-09-09 215521" src="https://github.com/user-attachments/assets/282cbd68-f0bf-46b8-85a1-043f5f2a5fd8" />


## Interpretation
Account configuration and least-privilege verification are useful endpoint-security evidence.
