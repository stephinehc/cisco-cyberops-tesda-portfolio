# IOC Analysis — Pushdo Trojan Investigation

## Objective

Identify indicators of compromise (IOCs) associated with the Pushdo infection and organize them into network, host and file-based indicators.

## Affected Host

| IOC Type | Value | Significance |
|---|---|---|
| Internal IP | `192.168.1.96` | Compromised endpoint |
| MAC | `00-15-C5-DE-C7-3B` | Network identifier of affected endpoint |
| NIC Vendor | Dell Inc. | Host attribution/context |

## Network Indicators

| IOC Type | Value | Notes |
|---|---|---|
| External IP | `208.67.222.222` | Seen in assessment DNS/policy activity |
| External IP | `208.83.223.34` | External infrastructure visible in assessment data |
| External IP | `198.1.85.250` | External infrastructure visible in assessment data |
| Domain | `myip.opendns.com` | Appears in related DNS/policy activity |

These values are retained as evidence from the historical assessment dataset and should not be interpreted as current threat-intelligence verdicts.

## Malware/File Indicators

Three executable files are identified for investigation:

1. `gerv.gun`
2. `trow.exe`
3. `wp.exe`

### gerv.gun

- File type: Win32 EXE
- File size: 236.00 KB (241,664 bytes)
- Associated names in the assessment's threat-intelligence results include `gerv.gun`, `test`, `tmp523799.697`, `tmp246975.343`, `tmp213582.420`, `vector.tui`, and other observed names.
- Target architecture: Intel 386 or later compatible processors.

### trow.exe

- File type: Win32 EXE
- File size: 323.00 KB (330,752 bytes)
- Associated names include `Pedals`, `Pedals.exe`, `trow.exe`, `test3`, and other observed names.
- Target architecture: Intel 386 or later compatible processors.

### wp.exe

- File type: Win32 EXE
- File size: 300.50 KB (307,712 bytes)
- Associated names include `wp.exe`, `test2`, `test_3`, and other observed names.
- Target architecture: Intel 386 or later compatible processors.

## Hash Evidence

The assessment requires obtaining the SHA-256 hash for the identified files and using the hashes to perform malware verification.

Record the learner's actual hash values here:

| File | SHA-256 | Verification |
|---|---|---|
| `gerv.gun` | **Add actual hash from lab** | VirusTotal result |
| `trow.exe` | **Add actual hash from lab** | VirusTotal result |
| `wp.exe` | **Add actual hash from lab** | VirusTotal result |

Do not replace these fields with values from an external answer key. Use the hash values generated/observed during the learner's own assessment.

## IOC Classification

```text
HOST IOC
 └── 192.168.1.96

NETWORK IOC
 ├── External IP addresses
 └── DNS/domain indicators

FILE IOC
 ├── gerv.gun
 ├── trow.exe
 └── wp.exe

HASH IOC
 └── SHA-256 values obtained during analysis
```

## TESDA Relevance

Primary evidence domains:

- `05-malware-ioc-analysis/`
- `07-incident-investigation/`
- `08-threat-intelligence/`

This evidence supports IOC identification, correlation and threat verification under the portfolio's TESDA mapping.
