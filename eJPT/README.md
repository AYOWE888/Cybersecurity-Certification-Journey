# 🕵️ eJPT v2 Certification Prep Roadmap & Logs

This repository tracks my progress toward the **eLearnSecurity Junior Penetration Tester (eJPT)** certification. This roadmap aligns official INE domains with my active lab work on TryHackMe.

---

## 🧭 Learning Path & Milestones

### 🟢 Phase 1: Assessment Methodologies (25%)
*Focus: OSINT and Infrastructure Discovery*
- [x] **Passive Recon:** Gathering company info, emails, and technical data.
- [x] **Active Discovery:** Locating endpoints and identifying open ports via Nmap.
- [x] **Vulnerability Research:** Identifying service vulnerabilities (CVE research).
*Status: Completed (Methodology & Network Auditing logs updated)*

### 🟡 Phase 2: Host & Network Auditing (25%)
*Focus: Enumeration and Data Collection*
- [ ] **System Enumeration:** Gathering user accounts and system details.
- [ ] **Post-Enum Actions:** Extracting password hashes and config files.
- [ ] **Data Management:** Mastering file transfers (SCP/FTP/Netcat).
*Status: In Progress (Advanced Enumeration pending)*

### 🟠 Phase 3: Host & Network Penetration Testing (35%)
*Focus: Exploitation and Lateral Movement*
- [ ] **Metasploit Mastery:** Initializing `msfconsole` and selecting payloads.
- [ ] **Pivoting:** Adding routes to reach internal networks.
- [ ] **Credential Attacks:** Brute-force and hash cracking.
*Status: Started (Exploitation log initialized)*

### 🔴 Phase 4: Web Application Penetration Testing (15%)
*Focus: Web Recon and Vulnerabilities*
- [ ] **Web Recon:** Locating hidden directories (Gobuster/Nikto).
- [ ] **Web Attacks:** Brute-force login attacks.
*Status: Not Started*

---

## 🧪 Active Lab Logs (THM)

| Module | Status | Lab Write-ups |
| :--- | :---: | :--- |
| Pentesting Fundamentals | 🟢 | [View Methodology](./Methodology.md) |
| Network Security (Nmap) | 🟢 | [View Network Auditing](./labs/Networkauditing.md) |
| Vulnerability Research | 🟢 | [View Research Notes](./labs/VulnerabilityResearch.md) |
| Metasploit | 🟡 | [View Exploitation](./Exploitation.md) |
| Introduction to Web Pentesting | 🔴 | Not Started |
| Privilege Escalation | 🔴 | Not Started |

---

## 🛠️ Pentesting Toolbelt (Current)

| Tool | Category | Command Cheat Sheet |
| :--- | :--- | :--- |
| **Nmap** | Scanning | `nmap -sV -sC -p- <IP>` |
| **Hping3** | Packet Crafting | `sudo hping3 -S --flood <IP>` |
| **Metasploit** | Exploitation | `msfconsole -q` |
| **Gobuster** | Directory Brute | `gobuster dir -u <URL> -w <Wordlist>` |

---

## 📚 Recommended Resources
- **INE Training:** Official eJPT PrepStart course.
- **TryHackMe:** "Jr Penetration Tester" Pathway.
- **HackTheBox:** "Active Directory 101" and "Easy" Linux/Windows boxes.

---
*Last Updated: 2026-02-27*
