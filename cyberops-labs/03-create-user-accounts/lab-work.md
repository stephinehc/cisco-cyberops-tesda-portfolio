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
`LAB-03-01-user-account.png`

> **Attach screenshot here:** `screenshots/LAB-03-01-user-account.png`

**Figure 2 — Account properties and group membership**  
`LAB-03-02-account-properties.png`

> **Attach screenshot here:** `screenshots/LAB-03-02-account-properties.png`

## Interpretation
Account configuration and least-privilege verification are useful endpoint-security evidence.
