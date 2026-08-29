# BOTS v2 Setup Guide

## 1. Controlled laboratory requirement

BOTS v2 must be deployed and analyzed only in a **simulated, isolated, and controlled laboratory environment**. The environment should use designated virtual machines, an isolated virtual network where applicable, and an authorized training dataset.

Do not connect the investigation workflow to a production network or use it to scan, monitor, contact, or interact with live organizational infrastructure.

## 2. Choose the dataset

The BOTS v2 training dataset may be deployed as the full dataset or the attack-focused dataset according to the environment's storage and training requirements. Follow the dataset provider's current documentation for installation requirements.

## 3. Obtain and install the training dataset

Use the official BOTS v2 project documentation as the authoritative source for dataset files and installation requirements.

The installation should be performed inside the designated laboratory environment. Document only the laboratory configuration required to reproduce the training exercise; do not record or publish sensitive host credentials or network information.

## 4. Verify the dataset

Run:

```spl
index=botsv2 earliest=0
```

Then inspect the available fields and sourcetypes.

A useful first inventory query from the Splunk 2 learning material is:

```spl
| metadata type=sourcetypes index=botsv2 | eval firstTime=strftime(firstTime,"%Y-%m-%d %H:%M:%S") | eval lastTime=strftime(lastTime,"%Y-%m-%d %H:%M:%S") | eval recentTime=strftime(recentTime,"%Y-%m-%d %H:%M:%S") | sort - totalCount
```

This establishes what simulated telemetry is available before beginning the investigation.

## 5. Expected telemetry

The BOTS v2 dataset can provide training telemetry representing network, endpoint, firewall/proxy, IDS, Windows, Sysmon, osquery and other security-relevant activity. Treat all records as **training/simulated evidence** within the controlled environment.

## 6. Evidence capture procedure

For every investigation:

1. Record the investigation question.
2. Record the exact SPL query used in the controlled environment.
3. Capture the resulting event/table.
4. Identify the relevant fields.
5. Correlate the result with another simulated data source when appropriate.
6. Record the analyst interpretation.
7. Record the IOC, simulated affected asset, user, host, domain, IP, or file where applicable.
8. Record the conclusion.
9. Associate the screenshot with the appropriate evidence label in `screenshots/README.md`.
10. Do not present reference answers or screenshots as candidate-generated evidence.

## 7. Investigation sequence

```text
Controlled dataset verification
      ↓
Sourcetype inventory
      ↓
100-series investigation
      ↓
200-series investigation
      ↓
300-series investigation
      ↓
400-series investigation
      ↓
Evidence consolidation
      ↓
TESDA mapping
```

## 8. Safety, isolation and evidence integrity

BOTS v2 contains realistic-looking security-incident material for training purposes. Keep analysis inside the isolated laboratory environment. Do not interact with live malicious infrastructure merely to reproduce a historical result.

Do not perform scanning, exploitation, monitoring, containment, eradication, recovery, or other security actions against production or third-party systems as part of this portfolio.

The portfolio should contain only authorized training evidence. Do not publish credentials, private keys, confidential organizational information, personally identifiable information, or other restricted data.
