# Hi, I'm Saikiran Tammali 👋

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/saikiran-tammali-cybersec32) [![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SAIKIRAN-TAMMALI) [![Stevens](https://img.shields.io/badge/Stevens_Institute-8B0000?style=for-the-badge&logo=graduation-cap&logoColor=white)](https://www.stevens.edu)

---

## 🛡️ Cybersecurity Graduate | Network Analyst | SOC Engineer | Vulnerability Management

> *"Security is not a product, it's a process — and I've spent 2 years living that process at production scale during my time at HCLTech."*

I am a **cybersecurity graduate student at Stevens Institute of Technology** (M.S. Cybersecurity, May 2026), simultaneously completing an **Advanced Executive Program in Cybersecurity at IIIT Bangalore**. Before graduate school, I spent **2 years as a Network Analyst at HCLTech** — monitoring 5,000+ enterprise devices 24/7, triaging CVE exposures, managing incident response workflows, and enforcing SLA-driven remediation across 100+ global ISP partners.

I am actively pursuing roles in **SOC Engineering**, **Vulnerability Management**, and **Security Operations** in United States.

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
| Advanced Executive Program — Cybersecurity | IIIT Bangalore                              |  June 2026        |
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

### 🛡️ [Web Application VAPT — Simulated FinTech App](https://github.com/SAIKIRAN-TAMMALI/fintech-webapp-vapt) — *Jun 2026 · IIIT Bangalore*

> Black-box vulnerability assessment & penetration test of a deliberately vulnerable FinTech web app. Captured **6 hidden flags** and mapped each weakness to **OWASP Top 10 / CWE** with **CVSS** scoring and remediation guidance — covering anonymous FTP exposure (incl. a leaked PGP key), `robots.txt` data leakage, secrets in source comments, an exposed admin panel, a `phpinfo()` config dump on EOL PHP, and cleartext-HTTP transmission. Delivered a full VA report in professional format. **Tools:** Nmap · Gobuster · dirb · Burp Suite · Kali Linux · VirtualBox.

### 🕵️ Digital Forensics & Steganography — Hidden-Data Recovery from a JPG

> End-to-end forensics exercise modelled on a **financial-institution data-breach** investigation. Concealed text inside an ordinary JPG with **SilentEye**, stored it on a **two-disk 2 GB NTFS** environment, simulated deletion to mimic an attacker covering their tracks, then acquired a forensic disk image and **recovered + validated** the file with **FTK Imager** — proving evidence integrity via **MD5 + SHA1** hash verification before reconstructing the full-resolution image. **Tools:** SilentEye · FTK Imager · NTFS · MD5/SHA1 hashing.

**1. Embedding the secret message** — carrier `01.jpg` encoded in SilentEye (JPEG format, luminance interval k=5, 75% quality, bottom header). The payload *"This is a secret message.."* fits within the 7350 / 7376 octets available and outputs a JPG visually identical to the original.

![SilentEye encode dialog configuring JPEG options and hiding the message inside 01.jpg](assets/Encoded_message.png)

**2. Verifying disk-image integrity** — FTK Imager recomputes cryptographic hashes and compares them to the values recorded at acquisition. Both **MD5** and **SHA1** report **Match**, with **no bad blocks found** — confirming the evidence is authentic and unaltered (a prerequisite for forensic soundness and admissibility).

![FTK Imager verify results showing MD5 and SHA1 both Match with no bad blocks](assets/Hash_file.png)

**3. Recovering the deleted JPG** — FTK Imager parses the NTFS file system, locates the deleted carrier image (modified 01-07-2026), and exports it. The preview pane shows the tell-tale **JFIF** header bytes, and the recovered file opens intact at full **2592 × 1458 px** — an ordinary-looking photo that silently carries the Step 1 payload, ready to be decoded to close the investigative loop.

![Recovered JPG opened from the FTK image, valid full-resolution photograph with JFIF header visible](assets/recovered_img.png)

---

### 🎯 Full-Chain Cyber Intrusion Simulation — Metasploit · Ngrok · Malware Analysis

> Recreated a complete **authorised** attack chain in a fully isolated lab (**Kali Linux** attacker + **Windows Server 2022** victim, VirtualBox) — then switched to the **defender's** point of view to analyse and monitor the same payload. Built a Windows reverse-shell with **msfvenom**, exposed the listener to the internet through an **ngrok** TCP tunnel, caught the session in a Metasploit **multi/handler**, disguised the executable as a media file, and validated detection with **VirusTotal** and live monitoring with **TCPView**. *No real or third-party systems were ever involved.* **Tools:** Metasploit Framework · msfvenom · ngrok · VirusTotal · TCPView · VirtualBox.

<details>
<summary><b>📖 View the 10-step walkthrough (with screenshots)</b></summary>

<br>

**Step 1 — Reconnaissance of the attacker machine.** Ran `ip a` on Kali to map its interfaces: `lo` (127.0.0.1), the lab-facing `eth0` at `10.0.2.5/24`, and the unused `docker0` bridge — establishing which host is which before building anything.

![Running ip a on Kali to check the attacker machine's network interfaces](assets/ipaddr.png)

**Step 2 — Installing the Metasploit Framework.** Installed from the Kali repos with `apt-get install metasploit-framework` after refreshing package lists (1318 packages upgradable). A first-attempt typo (`metaasploit-framework`) triggered *Unable to locate package* — an early lesson that commands must be exact.

![Installing the Metasploit Framework with apt-get after correcting the spelling](assets/metasploit-framework.png)

**Step 3 — Adding the ngrok authtoken.** Linked ngrok to a personal free account. The initial `ngrok config add-authtoken …` returned *ngrok: not found* (not on PATH); running `./ngrok …` from the working folder succeeded with *Authtoken saved to configuration file*.

![Saving the personal ngrok authtoken so the tunnel can be authenticated](assets/ngrok_authtoken.png)

**Step 4 — Starting the ngrok TCP tunnel.** Brought the tunnel **online**, producing a public forwarding address (e.g. `0.tcp.in.ngrok.io:20673 → localhost:9999`). Anything sent to the public ngrok address now lands on port `9999` of the Kali box — right where the listener will wait. The terminal was kept open for the duration, since closing it drops the tunnel.

![The live ngrok tunnel forwarding a public internet address to local port 9999](assets/ngrok_tcp.png)

**Step 5 — Generating the payload with msfvenom.** Built a `windows/meterpreter/reverse_tcp` executable pointed at the ngrok address (LHOST) and port (LPORT) so it calls home through the tunnel. Early runs failed with *options failed to validate: LHOST*; once corrected it produced `payload.exe` — **payload size 355 bytes, final exe 7168 bytes**.

![Building the Windows reverse-shell payload with msfvenom, pointed at the ngrok tunnel](assets/payload-generated.png)

**Step 6 — Disguising the payload.** On the victim desktop the executable was renamed to appear as an ordinary `payload.mp4` media file sitting among legitimate tools — illustrating how social engineering gets a user to double-click a "video" that is actually a program.

![The payload disguised as an ordinary media file on the Windows victim's desktop](assets/payloadspoof.png)

**Step 7 — Loading the listener module.** On **Metasploit v6.4.135**, loaded `use exploit/multi/handler` and set the matching `PAYLOAD windows/meterpreter/reverse_tcp` — the handler now knows exactly what kind of connection to expect.

![Loading the multi/handler module and setting the matching reverse_tcp payload](assets/multi-handler.png)

**Step 8 — Configuring & starting the reverse TCP listener.** Set `LHOST 0.0.0.0` (accept on all interfaces) and `LPORT 9999` (the port ngrok forwards to), then `exploit` — printing *Started reverse TCP handler on 0.0.0.0:9999*. The full chain is now armed: if the victim runs the file, it tunnels through ngrok and lands here.

![Setting LHOST/LPORT and launching the handler; reverse TCP listener running on port 9999](assets/metasploit-lstn.png)

**Step 9 — Analysing the payload on VirusTotal (defender view).** Uploading the executable, **29 of 70 vendors** flagged it as malicious — tagged `peexe` / `corrupt` / `spreader` with the popular threat label *trojan.msfshell/meterpreter*. Even a freshly built payload is widely caught, underlining why signatures must stay current.

![VirusTotal flagging the payload as a Meterpreter trojan, detected by 29 of 70 engines](assets/virustotal.png)

**Step 10 — Monitoring connections with TCPView.** On the victim, TCPView lists every process with its protocol, state and remote address, cleanly separating **Listening** ports from **Established** sessions. An unexpected *Established* connection from an odd process to an unknown remote is the tell-tale sign of a reverse shell — tying the attacker and defender halves together.

![Monitoring live network connections on the Windows victim with TCPView](assets/tcpview.png)

</details>

> **Key takeaways:** reverse shells call *outbound*, so egress monitoring is critical · tunnelling tools like ngrok expand the threat surface even without a public IP · standard payloads are widely detected, so updated AV genuinely helps · defensive tooling (VirusTotal, TCPView) turns an invisible intrusion into something observable and actionable.

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
| **CC – Certified in Cybersecurity** | **ISC2** | **2026** | [![ISC2 CC](https://img.shields.io/badge/ISC2-Certified_in_Cybersecurity_(CC)-00A0B0?style=flat-square&logoColor=white)](https://github.com/SAIKIRAN-TAMMALI/SAIKIRAN-TAMMALI/blob/main/3010f389-0db6-4052-bfe3-206e7aaa9773.pdf) |
| **ISC2 Candidate Member** | **ISC2** | **2026** | [![ISC2 Candidate](https://img.shields.io/badge/ISC2-Candidate_Member-1F3A6E?style=flat-square&logoColor=white)](https://www.isc2.org/candidate) |
| Bits & Bytes of Computer Networking | Google | 2024 | — |
| Ethical Hacking with AI | Internshala | 2022 | — |
| *(In Progress)* CompTIA Security+ | CompTIA | 2026 | — |

### 🏅 ISC2 Badge

<a href="https://www.isc2.org/candidate" target="_blank">
  <img src="https://raw.githubusercontent.com/SAIKIRAN-TAMMALI/SAIKIRAN-TAMMALI/main/isc2-candidate.png" alt="ISC2 Candidate Badge" width="120"/>
</a>

> **CC – Certified in Cybersecurity** issued by ISC2 on May 18, 2026. Valid for 3 years. Learner ID: `f02cd1ab-5c1f-4f7b-ae25-e2dc9bc8316c`

---

## 📊 GitHub Stats

[![](https://github-readme-stats.vercel.app/api?username=SAIKIRAN-TAMMALI&show_icons=true&theme=dark&hide_border=true&count_private=true)](https://github.com/SAIKIRAN-TAMMALI) [![](https://github-readme-stats.vercel.app/api/top-langs/?username=SAIKIRAN-TAMMALI&layout=compact&theme=dark&hide_border=true)](https://github.com/SAIKIRAN-TAMMALI)

---

## 📚 Currently Learning

```
🔴  MITRE ATT&CK detection engineering & threat hunting
🔵  Splunk SPL — advanced query writing and detection rule development  
☁️  Cloud security — AWS Security Hub, GuardDuty, CloudTrail analysis
📋  CompTIA Security+ certification prep
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
