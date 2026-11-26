# Mediroza General Hospital — Security Assessment & SOC Lab Portfolio

> **Educational & Authorized Lab Documentation Only.** All activities documented in this repository were performed strictly within an authorized training/lab context (`medirozahospital.com` / Networkwalks lab exercises and SOC/SIEM defense workflows) for educational and portfolio purposes. No unauthorized testing, data exfiltration, or production disruption is included.

---

## Overview

This repository provides a clean, structured **GitHub repository README (`README.md`)** and folder layout for documenting a **Security Operations Center (SOC) & Penetration Testing / Vulnerability Assessment Lab** centered on the authorized target `medirozahospital.com` across Milestones **M1–M4** (reconnaissance & web exposure review, encrypted document handling & password recovery concepts, data exposure analysis & metadata hygiene, and structured reporting/remediation).

---

## Tools & Technologies Used

| Category | Tools & Platforms | Role in Lab & Documentation |
| :--- | :--- | :--- |
| **Reconnaissance & Web Profiling** | `whois`, `whatweb`, `nslookup`, `dig`, `curl`, `wafw00f`, `dnsrecon`, `theHarvester` | Domain registration lookup, DNS record enumeration, web/WAF fingerprinting, and OSINT gathering |
| **Network & Vulnerability Analysis** | Zenmap / Nmap, Wireshark, Nessus Essentials, Burp Suite | Host/port discovery, packet capture inspection, vulnerability scanning, and HTTP/web traffic review |
| **File & Password Assessment** | John the Ripper, Johnny GUI, file metadata inspection utilities | Authorized password/encryption assessment and file property/metadata verification |
| **SIEM & Threat Intelligence** | Wazuh (Manager, Indexer, Dashboard, Filebeat, Windows Agent), AbuseIPDB, VirusTotal | Centralized log collection, authentication/event analysis, and IOC reputation triage |
| **Lab Environment & Reporting** | Oracle VirtualBox (Windows 10 host; Kali Linux, Ubuntu, Windows 10 VMs), Git & GitHub, Markdown | Isolated virtualized lab networking, version-controlled documentation, and structured reporting |

---

## Suggested Repository Structure

```text
medirozahospital-security-lab/
├── README.md
├── 01-reconnaissance-and-access/
│   ├── recon-notes.md
│   └── findings-summary.md
├── 02-cryptography-and-file-analysis/
│   ├── encryption-assessment.md
│   └── metadata-review.md
├── 03-data-exposure-and-siem/
│   ├── exposure-analysis.md
│   └── wazuh-detection-notes.md
├── 04-final-report-and-remediation/
│   ├── executive-summary.md
│   ├── risk-matrix.md
│   └── remediation-roadmap.md
└── evidence/
    └── .gitkeep
```

---

## Milestone Workflow Summary

| Milestone | Focus Area | Key Artifacts & Documentation |
| :--- | :--- | :--- |
| **M1 — Reconnaissance & Entry Points** | Passive/active recon, DNS/web stack profiling, exposed endpoints, auth & input review | Reconnaissance logs, service/stack notes, access control observations |
| **M2 — File & Encryption Analysis** | File properties, encryption/password policy assessment, recovery methodology notes | Cipher/protection findings, metadata review, defensive hardening notes |
| **M3 — Data Exposure & Monitoring** | Sensitive data exposure review, internal file clues, log monitoring & alerting | Data classification notes, exposure impact summary, SIEM monitoring notes |
| **M4 — Reporting & Remediation** | Executive summary, methodology, severity ratings, prioritized remediation steps | Final assessment report, risk ratings (Critical–Low), fix verification checklist |

---

## Risk Rating Scale

* **Critical:** Direct, high-impact exposure of sensitive records or administrative controls with low barrier to exploitation; requires immediate remediation.
* **High:** Significant security weakness or unauthorized access path affecting core application or data confidentiality; prioritize urgently.
* **Medium:** Security misconfiguration or defense-in-depth gap requiring coordinated remediation in the near term.
* **Low:** Minor informational finding or hardening improvement with limited standalone impact.

---

## Defensive & Remediation Priorities

1. **Access Control & Authentication Hardening:** Enforce strong authentication, authorization checks on restricted routes, and principle of least privilege.
2. **Encryption & Key/Secret Hygiene:** Apply modern encryption standards, avoid weak or predictable credentials/passphrases, and audit document metadata before publishing or sharing files.
3. **Data Minimization & Exposure Prevention:** Remove sensitive files, internal reference material, and PII/financial records from web-accessible paths; restrict directory listings and internal shares.
4. **Logging, Monitoring & Incident Response:** Forward relevant authentication, web, and endpoint logs to centralized monitoring (such as Wazuh) and tune alerts for anomalous access patterns.

---

## Disclaimer

This repository template and documentation framework are intended strictly for authorized security assessments, SOC training, and defensive engineering portfolios. Always obtain explicit written authorization before testing any target system or network.
