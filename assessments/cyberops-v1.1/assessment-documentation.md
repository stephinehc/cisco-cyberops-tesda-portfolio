# CCNA Cybersecurity Operations v1.1 — Assessment Documentation

## 1. Environment Preparation

The assessment is performed in the Cybersecurity Operations virtual environment using Security Onion.

### Initial checks

1. Log into Security Onion.
2. Verify the Network Security Monitoring services with `sudo service nsm status`.
3. Open Sguil.
4. Select the networks required by the assessment.
5. Locate the event group associated with the exploit.

**Evidence:**

`![Security Onion / Sguil](screenshots/01-sguil-overview.png)`

---

## 2. Part 1 — Gathering Basic Information

The analyst establishes the basic facts before deeper investigation.

### Recorded results

| Item | Result |
|---|---|
| Exploit-related events | **15 events** within the identified event group |
| Exploit start | **2017-09-07 15:31:12** |
| Exploit end | **2017-09-07 15:31:34** |
| Approximate duration | **22 seconds** |
| Internal host | **192.168.0.12** |
| Host MAC | **00:1b:21:ca:fe:d7** |
| Operating system | **Windows-based system** |
| NIC vendor | Record from the learner's actual evidence |

The event set contains multiple Snort/ET rule sources. The analyst should preserve the actual alert screen rather than relying on a copied answer.

### Assessment conclusion

The event sequence is suspicious because it combines an outdated client component with exploit-kit indicators and external traffic associated with exploit delivery.

---

## 3. Part 2 — Learn About the Exploit

The Snort/Sguil evidence identifies the exploit kit as **Angler EK**.

### Exploit-kit concept

An exploit kit is an attack framework that profiles a visiting client, determines whether a usable vulnerability is present, selects an appropriate exploit, and delivers a payload after successful exploitation.

### Angler EK investigation

The assessment research should explain the observed workflow:

```text
Compromised / malicious web content
            ↓
Client profiling
            ↓
Vulnerability identification
            ↓
Exploit selection
            ↓
Exploit delivery
            ↓
Payload delivery
```

### Applications commonly associated with the kit

- Adobe Flash Player
- Java Runtime Environment
- Microsoft Silverlight

The observed victim condition points specifically to an **outdated Flash component**.

### Evidence

`![Angler EK research](screenshots/05-angler-ek-research.png)`

---

## 4. Part 3 — Determining the Source of the Malware

The analyst uses the Sguil event group to correlate the internal victim with the external infrastructure involved in the exploit.

### Relevant addresses

The assessment identifies the following infrastructure among the related events:

- `192.168.0.12` — internal victim
- `93.114.64.118`
- `173.201.198.128`
- `192.99.198.158` — exploit-delivery infrastructure
- `208.113.226.171`
- `192.168.0.1`
- `209.126.97.209`

Only classify an address as an IOC when the supporting evidence establishes its role.

### Key source findings

The host associated with the outdated Flash alert is **192.168.0.12**.

The host that appears to deliver the exploit is **192.99.198.158**.

The corresponding delivery domain is:

`qwe.mvdunalterableairreport.net`

### ELSA correlation

Use ELSA to search the appropriate time range and correlate HTTP/network records with the vulnerable host and Flash-related activity. Record the actual ELSA result visible in the learner's assessment evidence.

### Assessment conclusion

The evidence supports the conclusion that the internal host was exposed to an exploit-kit chain involving an outdated Flash component and external exploit-delivery infrastructure.

---

## 5. Part 4 — Analyze Details of the Exploit

The final part moves from alert/log evidence to deeper network analysis.

### Landing-page infrastructure

The investigation identifies a landing-page component associated with:

- **Domain:** `lifeinsidetroit.com`
- **IP:** `173.201.198.128`
- **Server-side script:** `02024870e4644b68814aadfbb58a75bc.php`

The landing-page stage receives client information and is used to determine which exploit should be delivered.

### Exploit delivery

The exploit-delivery infrastructure is:

- **Domain:** `qwe.mvdunalterableairreport.net`
- **IP:** `192.99.198.158`

### Wireshark analysis

Pivot from the relevant Sguil event to the packet capture in Wireshark. Use the captured HTTP traffic to identify and export the object delivered during the exploit sequence.

The assessment identifies the recovered object as:

`3xdz3bcxc8`

The relevant Flash-related file type is **SWF**.

Record the following from the learner's actual exported object:

- File name: `3xdz3bcxc8`
- File type: `SWF`
- File size: __________________
- SHA-256: __________________
- Analysis result: __________________

**Evidence:**

`![Wireshark payload extraction](screenshots/10-wireshark-export.png)`

---

## 6. Evidence Checklist

- [ ] Security Onion service status
- [ ] Sguil exploit event group
- [ ] Event count and timestamps
- [ ] Internal host and MAC evidence
- [ ] Angler EK identification
- [ ] Exploit-kit research
- [ ] Source/delivery IP evidence
- [ ] Delivery-domain evidence
- [ ] ELSA correlation
- [ ] Landing-page evidence
- [ ] Wireshark packet evidence
- [ ] Exported SWF evidence
- [ ] Final findings

## Evidence integrity

All final screenshots and values should come from the learner's own assessment run. The public answer material is not itself evidence and is not cited in this portfolio.
