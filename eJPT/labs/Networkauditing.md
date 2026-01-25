# 🕵️ Lab Report: Advanced Network Reconnaissance
**Certification Path:** eJPT (Junior Penetration Tester)  
**Lab Platform:** TryHackMe  
**Room:** [Further Nmap](https://tryhackme.com/room/furthernmap)

---

## 🏛️ Executive Summary: Core Mechanics
This lab focused on the transition from basic scanning to advanced enumeration and firewall evasion. The primary takeaway is the ability to interpret how Nmap interacts with the TCP/IP stack to identify "hidden" services.

### 1. Scanning Methodologies
* **TCP Connect (`-sT`):** Performs a full 3-way handshake. Reliable but highly visible in application logs.
* **SYN Stealth (`-sS`):** The "Half-Open" scan. It sends a `SYN`, receives a `SYN/ACK`, and immediately sends a `RST`. This prevents the connection from being fully established, staying below the radar of basic logging.
* **UDP Scanning (`-sU`):** Connectionless and slower. It relies on the absence of an **ICMP Port Unreachable** message to assume a port is `Open|Filtered`.

### 2. Stealth & Evasion (RFC 793)
* **Null (`-sN`), FIN (`-sF`), and Xmas (`-sX`):** These "invisible" scans set specific flags (or none). According to RFC 793, if a port is closed, it should respond with a `RST`. If open, it should ignore the packet.
* **Firewall Bypass (`-Pn`):** Configures Nmap to skip host discovery. Essential for targets that drop ICMP (Ping) packets but leave services exposed.
* **Firewall Behavior:** Discovered that firewalls can be configured to **drop** TCP packets to blocked ports (specifically those with the `SYN` flag), forcing Nmap to report them as `Filtered`.

### 3. Nmap Scripting Engine (NSE)
Mastered the use of specialized scripts to automate vulnerability discovery and exploitation:
* **Categories:** `Safe`, `Intrusive`, `Vuln`, `Exploit`, `Auth`, and `Brute`.
* **Arguments:** Learned to pass parameters (e.g., `--script-args http-put.url='/uploads/'`) to customize script behavior for specific targets.
* **Service Specificity:** Noted that each script is tailored for a particular service (e.g., `ftp-anon` for FTP).

---

## 🛠️ Technical Verification (Task 14: Practical)

| Objective | Technical Result | Command Used |
| :--- | :--- | :--- |
| **Firewall Evasion** | Bypassed ICMP block | `nmap -Pn` |
| **Open Ports (5k)** | **5** | `sudo nmap -sS -Pn --top-ports 5000 <IP>` |
| **Xmas Scan (999)** | **999 (Open\|Filtered)** | `sudo nmap -sX -p 1-999 <IP>` |
| **Xmas Reason** | **no-response** | (Nmap Output Detail) |
| **FTP Vulnerability**| Anonymous Login: **YES** | `nmap --script ftp-anon -p 21 <IP>` |

### 🔍 Service Enumeration Findings
* **Port 21 (FTP):** Anonymous access permitted.
* **Port 80 (HTTP):** Web server detected; requires further web enumeration.

---

## 🧠 Lessons Learned
* **False Negatives:** If a host appears "down," it is likely a firewall dropping pings. Always re-test with `-Pn`.
* **NSE Efficiency:** Scripts can move a penetration test from "discovery" to "access" quickly (e.g., using `brute` scripts for credential testing).
* **Protocol Nuance:** Understanding that UDP scans assume "open" if no ICMP reply is received is vital for accurate network mapping.

_**Although my findings are interesting and really detailed, to master this skill and tool, I'll have to practice continuously.**_

_**I'll post my results after every lab here :)**_

---

## ✅ Proof of Completion
* **Status:** 🟢 100% Completed

* **Platform:** [My TryHackMe Profile](https://tryhackme.com/room/furthernmap?utm_campaign=social_share&utm_medium=social&utm_content=room&utm_source=reddit&sharerId=68be8259779eb658bbc19236)
![Room Completion Screenshot](./Nmap_Room.png)

