# Mediroza General Hospital — Week 4 Penetration Testing Report & Documentation

> **Educational & Authorized Lab Documentation Only.** All activities documented in this repository were performed strictly within an authorized penetration testing lab (`medirozahospital.com` — Networkwalks Batch B083, Week 4) for educational and portfolio purposes. Written authorization was granted within defined scope rules.

---

## Overview

This repository documents the **Week 4 Black-Box Penetration Testing Project** targeting **Mediroza General Hospital** (`https://medirozahospital.com`) across Milestones **M1–M4**—covering reconnaissance and initial access, encrypted file recovery, server-side data exposure analysis, and professional security reporting.

---

## Tools & Utilities Used

| Category | Tools & Utilities | Role in Project |
| :--- | :--- | :--- |
| **Reconnaissance & Web Profiling** | `nslookup`, `dig`, `whois`, `curl`, `whatweb` | DNS resolution, domain registration lookup, HTTP header inspection, and web-stack fingerprinting |
| **Web Application & Proxy Testing** | Burp Suite (Intruder, Repeater), FoxyProxy, Web Browser / Developer Tools | Routing browser traffic, intercepting/inspecting requests, testing SQL injection/authentication entry points, and reviewing exposed paths |
| **Cryptographic & File Analysis** | Networkwalks Hash Calculator, Networkwalks Password Cracker, PDF property/metadata inspection | Extracting hashes, performing offline password recovery on encrypted patient lab PDFs, and inspecting document metadata |
| **Environment & Documentation** | Kali Linux (Oracle VirtualBox), Git & GitHub, Markdown | Command-line execution, evidence capture, and structured reporting |

---

## Repository Structure

```text
medirozahospital-pentest-wk4/
├── README.md
├── 01-reconnaissance-and-initial-access/
│   ├── recon-notes.md
│   └── findings-summary.md
├── 02-encryption-and-file-analysis/
│   ├── encryption-assessment.md
│   └── metadata-review.md
├── 03-data-exposure-analysis/
│   └── exposure-analysis.md
├── 04-final-report-and-remediation/
│   ├── executive-summary.md
│   ├── risk-matrix.md
│   └── remediation-roadmap.md
└── evidence/
    └── .gitkeep
```

---

## Milestone Workflow Summary

| Milestone | Focus Area | Summary of Work |
| :--- | :--- | :--- |
| **M1 — Initial Access** | Target reconnaissance, exposed entry points, authentication/input review | Profiled `medirozahospital.com` and identified unauthorized access paths to restricted patient PDF lab reports |
| **M2 — Data Extraction** | File encryption analysis and password recovery | Evaluated PDF protection mechanisms using Networkwalks Hash Calculator and Networkwalks Password Cracker |
| **M3 — Critical Data Exposure** | Deep file property inspection and server directory exposure | Analyzed file metadata and uncovered exposed employee salary and shareholder records on the server |
| **M4 — Pentest Report** | Executive summary, methodology, findings, risk ratings, remediation | Compiled a structured penetration testing report with Critical–Low ratings and actionable fixes |

---

## Risk Rating Scale

* **Critical:** Direct, high-impact exposure of sensitive patient, employee, or shareholder records with low barrier to exploitation; requires immediate remediation.
* **High:** Significant security weakness or unauthorized access path affecting application or data confidentiality; prioritize urgently.
* **Medium:** Security misconfiguration or defense-in-depth gap requiring coordinated remediation in the near term.
* **Low:** Minor informational finding or hardening improvement with limited standalone impact.

---

## Key Remediation Recommendations

1. **Enforce Authentication & Access Controls:** Restrict unauthorized access to patient portals, lab reports, and administrative routes.
2. **Disable Directory Listing & Remove Sensitive Files from Web Roots:** Remove exposed database backups, employee salary sheets, and shareholder documents from publicly accessible directories.
3. **Strengthen Document Encryption & Metadata Hygiene:** Use strong, unique encryption passphrases and strip sensitive internal paths or properties from PDFs before storage or distribution.
4. **Minimize Server & HTTP Banner Exposure:** Harden web server headers and restrict unnecessary information disclosure during reconnaissance.

---

## Disclaimer

This repository is strictly for educational and authorized security assessment documentation. Never test or access systems without explicit written permission from the system owner.
