# Hi, I'm Saikiran Tammali 👋

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/saikiran-tammali/) [![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SAIKIRAN-TAMMALI) [![CompTIA Security+](https://img.shields.io/badge/CompTIA_Security%2B-Certified-E2231A?style=for-the-badge&logo=comptia&logoColor=white)](https://www.comptia.org/certifications/security) [![Stevens](https://img.shields.io/badge/Stevens_Institute-8B0000?style=for-the-badge&logo=graduation-cap&logoColor=white)](https://www.stevens.edu)

---

## 🛡️ Aspiring Security & Network Analyst | SOC Analyst | Penetration Tester | M.S. in Cybersecurity

> *"Security is not a product, it's a process — and I've spent 2 years living that process at production scale during my time at HCLTech."*

I am a **cybersecurity graduate of Stevens Institute of Technology** (M.S. Cybersecurity, 2026), **CompTIA Security+ certified**, and **certified in the Advanced Executive Program in Cybersecurity at IIIT Bangalore**. I bring **2 years of 24/7 operations experience as an Analyst at HCLTech**, monitoring 5,000+ network devices for PepsiCo, triaging 200–400 ServiceNow incidents per shift, and supporting CVE remediation across 100+ global ISP partners. I am hands-on with **Splunk, Zeek, Wireshark, Nessus, Metasploit, and Nmap** through lab projects in attack simulation, threat detection, and OWASP Top 10 testing.

I am **aspiring to grow into a Security & Network Analyst, SOC Analyst, and Penetration Tester**, and I am actively seeking an **entry-level role focused on alert triage, incident response, and vulnerability management** in the United States.

---

## ⚡ What I Do

```
🔍  Threat Detection     →  Splunk SIEM, alert triage, anomaly detection, MITRE ATT&CK
🛡️  Vulnerability Mgmt  →  Nessus scanning, CVE prioritization, patch remediation, SLA tracking
🔴  Offensive Security   →  Burp Suite, Nmap, Metasploit, SHODAN, MALTEGO, VAPT
🔵  Defensive Security   →  IDS/IPS, DLP concepts, EDR/XDR, firewall workflows, SOC ops
☁️  Cloud & DevSecOps    →  Docker, GitHub Actions CI/CD, AWS fundamentals, container hardening
🐍  Scripting            →  Python, Bash, SQL — security automation & regex-based rule building
```

---

## 🎓 Education

| Degree                                     | Institution                                 | Status            |
| ------------------------------------------ | ------------------------------------------- | ----------------- |
| M.S. Cybersecurity                         | Stevens Institute of Technology, Hoboken NJ |  May 2026         |
| Advanced Executive Program — Cybersecurity | IIIT Bangalore                              |  Sept 2026        |
| B.Tech, Mechanical Engineering             | Malla Reddy College of Engineering          |  May 2022         |

**Relevant Coursework:** TCP/IP Networking · Cryptography Protocols · Security Privacy & Reliability (CS810) · Advanced UNIX Programming · Enterprise Infrastructure Security · Ethical Hacking & VAPT · Ransomware & Malware Analysis · MITRE ATT&CK · SIEM Engineering

---

## 💼 Experience

### 🏢 HCLTech — Network & Security Analyst *(Sep 2022 – Sep 2024)*

- **24/7 SOC monitoring** across 5,000+ routers and switches using Splunk, Wireshark, Nagios, and SevOne
- **CVE risk prioritization** and patch remediation coordination — 99% SLA adherence maintained
- **Incident response** and alert triage via ServiceNow with structured severity escalation workflows
- **1,000+ endpoint validation** via CLI diagnostics; built topology diagrams for audit readiness
- **Primary liaison** with 100+ Tier 1 ISPs globally for network security incident resolution

---

## 🔬 Projects

### 🖥️ [Splunk SOC Home Lab — Detecting a Live SSH Brute-Force Attack](https://github.com/SAIKIRAN-TAMMALI/splunk-soc-home-lab) - *Nov 2026 . Self-directed Home Lab*

> A three-VM home SOC: attack a Linux server from Kali, ship its logs to Splunk with a Universal Forwarder, and catch the attack with SPL and a scheduled alert. Self-directed project to practise SOC analyst and detection-engineering workflows. Work in progress: new detections are added as they are built.

### 🛡️ [Web Application VAPT — Simulated FinTech App](https://github.com/SAIKIRAN-TAMMALI/fintech-webapp-vapt) — *Jun 2026 · IIIT Bangalore*

> Black-box vulnerability assessment & penetration test of a deliberately vulnerable FinTech web app. Captured **6 hidden flags** and mapped each weakness to **OWASP Top 10 / CWE** with **CVSS** scoring and remediation guidance — covering anonymous FTP exposure (incl. a leaked PGP key), `robots.txt` data leakage, secrets in source comments, an exposed admin panel, a `phpinfo()` config dump on EOL PHP, and cleartext-HTTP transmission. Delivered a full VA report in professional format. **Tools:** Nmap · Gobuster · dirb · Burp Suite · Kali Linux · VirtualBox.

### 🖥️ [Network VAPT — SMB Exploitation & Remediation (EternalBlue)](https://github.com/SAIKIRAN-TAMMALI/Performing-Vulnerability-Exploitation-and-Remediation-Strategies) — *IIIT Bangalore*

> Full attack chain against an unpatched **Windows Server 2012 R2** host. **Nmap** recon surfaced an exposed **SMBv1** service with message signing disabled; exploited via **Metasploit EternalBlue (MS17-010)** to a **SYSTEM-level Meterpreter** session, captured the flags, then dumped **NTLM** hashes and cracked them offline with **John the Ripper** — closing with a prioritised remediation plan (patching, SMBv1 removal, signing enforcement, segmentation). **Tools:** Nmap · Metasploit · Meterpreter · John the Ripper · Kali Linux.

### 🔐 [Secure File Storage & Access Management for Project Teams](https://github.com/SAIKIRAN-TAMMALI/Secure-File-Storage-and-Access-Management-for-Project-Teams) — *IIIT Bangalore*

> Hardened a Linux shared-storage environment for finance project teams. Enforced **role-based access with POSIX ACLs** (owner-only write, read-only for everyone else), set **per-role command-history limits**, configured **auditd** watch rules to log every access to the protected directory, and served the audit log via **Apache + cron** for IT review — with all controls persisted across reboots. **Tools:** Linux · POSIX ACLs · auditd · Apache · cron.

### 🏢 [Implementing & Managing Active Directory in Windows Server](https://github.com/SAIKIRAN-TAMMALI/Implementing-and-Managing-Active-Directory-in-Windows-Server) — *IIIT Bangalore*

> Deployed and administered an **Active Directory** domain on **Windows Server 2022**. Promoted a domain controller for `mydomain.local`, structured the domain with **OUs, users, and security groups**, enforced **account-lockout and password policy via GPOs**, joined a client to the domain and verified AD authentication, then applied **logon-hour restrictions, account disabling, and lockout enforcement**. **Tools:** Windows Server 2022 · AD DS · Group Policy · PowerShell.

### 🕵️ [Digital Forensics & Steganography — Hidden-Data Recovery from a JPG](https://github.com/SAIKIRAN-TAMMALI/digital-forensics-steganography)

> Steganography-to-forensics lifecycle modelled on a **financial-institution data-breach**. Concealed text inside an ordinary JPG with **SilentEye**, stored it on a **two-disk 2 GB NTFS** volume, deleted it to mimic an attacker covering their tracks, then acquired a forensic disk image and **recovered + validated** the file with **FTK Imager** — proving evidence integrity via **MD5 + SHA1** hashing before reconstructing the full-resolution image. **Tools:** SilentEye · FTK Imager · NTFS · MD5/SHA1 · VirtualBox.

### 🎯 [Full-Chain Cyber Intrusion Simulation — Metasploit · Ngrok · Malware Analysis](https://github.com/SAIKIRAN-TAMMALI/cyber-intrusion-simulation)

> Complete **authorised** attack chain recreated in an isolated **Kali → Windows Server 2022** lab, then examined from the defender's side. Built an **msfvenom** reverse-shell payload tunnelled to the internet via **ngrok**, caught it in a Metasploit **multi/handler**, disguised it as a media file, then validated detection on **VirusTotal** (29/70 engines) and monitored the live session with **TCPView**. *No real systems involved.* **Tools:** Metasploit · msfvenom · ngrok · VirusTotal · TCPView · VirtualBox.

### 🔐 [Secure Multi-Party Computation with FRESCO — SPDZ · TinyTables](https://github.com/SAIKIRAN-TAMMALI/secure-mpc-fresco) — *Stevens Institute of Technology*

> Built the **FRESCO** secure multi-party computation framework from source (**Java, Maven**) and implemented a **two-party private sum** where each party's input stayed secret — only **secret shares** crossed the network (inputs 10 + 15 → output 25, neither party saw the other's value). Switched from **TinyTables** (semi-honest) to **SPDZ** (malicious-secure) with a one-line config change, troubleshot a network configuration issue by reading the framework source, and benchmarked FRESCO against **JIFF** and **MP-SPDZ**. **Tools:** Java 8 · Maven · Docker · Git.

### 🧩 [Non-Malleable Cryptography — Commitments & Zero-Knowledge Proofs](https://github.com/SAIKIRAN-TAMMALI/non-malleable-cryptography-analysis) — *Stevens Institute of Technology*

> Research analysis of **Dolev, Dwork & Naor's** *Non-Malleable Cryptography* (SIAM J. Computing). Covers why **semantic security** alone fails in concurrent sessions, **non-malleable string commitments**, **zero-knowledge proofs of knowledge**, and **man-in-the-middle** (transparent prover) attacks — plus a severity-rated review of the schemes' limits, including **O(n²)** communication overhead and composability gaps.

### 🐚 [Simple Unix Web Shell](https://github.com/SAIKIRAN-TAMMALI/A-simple-shell.git) — C / NetBSD

> Prototype C-based web shell with HTTP response handling, magic code validation, and dynamic directory path expansion. Demonstrates application-layer attack surface understanding and low-level systems security.

### 🔒 CI/CD Pipeline Security — Docker & GitHub Actions *(CS810, Stevens)*

> Implemented container security hardening, automated vulnerability scanning, secrets detection using Python regex patterns, and least-privilege IAM controls in a GitHub Actions pipeline. Reduces software risk pre-deployment.

### 🤖 [Facial Recognition Pipeline](https://drive.google.com/file/d/1qHC93f9Zh5zyyvk_H4_8-lbCA3s1KlqB/view) — Python

> Automated large-scale facial recognition pipeline with structured image preprocessing, vector-range computations, and feature extraction validation across LFW-style datasets.

---

## 🧰 Tech Stack

### Security Tools

[![Splunk](https://img.shields.io/badge/Splunk-000000?style=flat-square&logo=splunk&logoColor=white)](https://www.splunk.com) [![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white)](https://www.wireshark.org) [![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square&logo=burpsuite&logoColor=white)](https://portswigger.net) [![Nessus](https://img.shields.io/badge/Nessus-00C176?style=flat-square&logoColor=white)](https://www.tenable.com) [![Metasploit](https://img.shields.io/badge/Metasploit-2596CD?style=flat-square&logoColor=white)](https://www.metasploit.com) [![Nmap](https://img.shields.io/badge/Nmap-4682B4?style=flat-square&logoColor=white)](https://nmap.org) [![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white)](https://www.kali.org) [![Zeek](https://img.shields.io/badge/Zeek-777BB4?style=flat-square&logoColor=white)](https://zeek.org)

### Languages & Scripting

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org) [![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)](https://www.gnu.org/software/bash/) [![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)](https://en.wikipedia.org/wiki/C_(programming_language)) [![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)](https://www.mysql.com)

### Cloud & DevSecOps

[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com) [![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/features/actions) [![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)](https://aws.amazon.com) [![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)](https://www.linux.org)

### Platforms & Frameworks

[![ServiceNow](https://img.shields.io/badge/ServiceNow-62D84E?style=flat-square&logo=servicenow&logoColor=white)](https://www.servicenow.com) [![MITRE ATT&CK](https://img.shields.io/badge/MITRE_ATT%26CK-E00000?style=flat-square&logoColor=white)](https://attack.mitre.org) [![NIST](https://img.shields.io/badge/NIST_CSF-003087?style=flat-square&logoColor=white)](https://www.nist.gov) [![OWASP](https://img.shields.io/badge/OWASP_Top_10-000000?style=flat-square&logo=owasp&logoColor=white)](https://owasp.org)

---

## 📜 Certifications

| Certification | Issuer | Year | Credential |
| ----------------------------------- | ----------- | ---- | ---------- |
| **CompTIA Security+** | **CompTIA** | **2026** | ![CompTIA Security+](https://img.shields.io/badge/Certified-Oct_25,_2026-E2231A?style=flat-square&logo=comptia&logoColor=white) |
| Bits & Bytes of Computer Networking | Google | 2024 | — |
| Ethical Hacking with AI | Internshala | 2022 | — |

> **CompTIA Security+** — certified **October 25, 2026**. Validates baseline skills in threat detection, risk management, incident response, and secure network architecture.

---

## 📊 GitHub Stats

[![](https://github-readme-stats.vercel.app/api?username=SAIKIRAN-TAMMALI&show_icons=true&theme=dark&hide_border=true&count_private=true)](https://github.com/SAIKIRAN-TAMMALI) [![](https://github-readme-stats.vercel.app/api/top-langs/?username=SAIKIRAN-TAMMALI&layout=compact&theme=dark&hide_border=true)](https://github.com/SAIKIRAN-TAMMALI)

---

## 📚 Currently Learning

```
🔴  MITRE ATT&CK detection engineering & threat hunting
🔵  Splunk SPL — advanced query writing and detection rule development
☁️  Cloud security — AWS Security Hub, GuardDuty, CloudTrail analysis
🔴  Offensive security — deepening VAPT and exploit development skills
```

---

## 📄 Publication

**Design and Analysis of Artificial Leg Mechanism for Above Knee Amputees**
*International Journal of Research in Engineering and Science (IJRES), Vol. 10, Issue 4*
[View Journal →](https://www.ijres.org/papers/Volume-10/Issue-4/Ser-13/K10047478.pdf)

---

## 📬 Let's Connect

I am actively seeking **full-time SOC, Vulnerability Management, and Security Operations roles** in the US (OPT/STEM authorized through 2029).

[![LinkedIn](https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/saikiran-tammali-cybersec32) [![Email](https://img.shields.io/badge/Send_Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:saikiran.tammali@gmail.com)

---

[![](https://komarev.com/ghpvc/?username=SAIKIRAN-TAMMALI&color=0A66C2&style=flat-square&label=Profile+Views)](https://github.com/SAIKIRAN-TAMMALI)
