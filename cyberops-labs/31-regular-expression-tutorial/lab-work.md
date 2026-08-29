# Lab 31 — Regular Expression Tutorial

**Cisco activity:** 27.2.9  
**Primary domain:** 02 Log/Event Analysis  
**Environment:** Simulated, isolated, controlled laboratory only.

## Tasks, Answers and Observations

1. Complete the assigned regular-expression exercises.
2. Record the function of key metacharacters.
3. Describe the supplied patterns.
4. Verify the patterns against the provided training text.

### Reference answers

| Pattern | Meaning |
|---|---|
| `^83` | String begins with `83` |
| `[A-Z]{2,4}` | Two to four consecutive uppercase letters |
| `2015` | Contains the sequence `2015` |
| `05:22:2[0-9]` | Contains a time from 05:22:20 through 05:22:29 |
| `\.com` | Contains `.com` |
| `complete|GET` | Matches either `complete` or `GET` |
| `0{4}` | Contains four consecutive zeros |

**Observation:** Regex patterns provide a repeatable method for locating structured strings in security data.

## Evidence

**Figure 1 — Regex exercise:** `LAB-31-01-regex-exercise.png`  
> **Attach:** `screenshots/LAB-31-01-regex-exercise.png`

**Figure 2 — Pattern verification:** `LAB-31-02-regex-verification.png`  
> **Attach:** `screenshots/LAB-31-02-regex-verification.png`

## Interpretation
Regex is useful for searching and extracting indicators from logs and other security data.
