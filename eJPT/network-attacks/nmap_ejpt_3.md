# Lab Report: Nmap Advanced Port Scans

- **Certification Track:** eJPT
- **Domain:** Network Attacks
- **Platform:** TryHackMe
- **Date Completed:** 2026-10-03
- **Time Invested:** 1.0 Hours
- **Core Skills & Tools:** 
map, TCP Flags, Packet Fragmentation

---

## 1. Executive Summary
The target environment deployed strict Intrusion Detection Systems (IDS) and deep packet inspection firewalls. The objective was to utilize advanced TCP flag combinations, spoofing, and fragmentation to silently map open ports.

## 2. Key Objectives & Methodologies
* Execute Null, FIN, Xmas, and ACK scans to bypass stateless firewalls and infer filtering rules.
* Implement packet fragmentation and source spoofing to evade IDS signatures.
* Perform Idle/Zombie scans to completely hide the scanner's true IP address.

## 3. Commands Executed & Payloads Used
`ash
nmap -sN -sF -sX 10.10.10.10
nmap -sA -sW 10.10.10.10
nmap -f -ff 10.10.10.10
nmap -sI 10.10.10.5 10.10.10.10
`

## 4. Artifact Embedding
| PROOF-01 | Advanced IDS evasion scan | *Terminal Log Verification - Output Recorded in Section 3* |

## 5. Defensive Takeaways
* **Root Cause:** Firewalls tracking only the SYN flag allow anomalous TCP packets (Null, FIN, Xmas) to slip through and solicit responses from internal hosts.
* **Remediation:** Deploy stateful packet inspection firewalls that drop invalid TCP flag combinations and implement strict IP spoofing protections (e.g. Reverse Path Forwarding).
