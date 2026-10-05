# Lab Report: NMAP Basic Port Scans

- **Certification Track:** eJPT
- **Domain:** Network Attacks
- **Platform:** TryHackMe
- **Date Completed:** 2026-10-03
- **Time Invested:** 1.0 Hours
- **Core Skills & Tools:** 
map, TCP SYN Scan, UDP Scan

---

## 1. Executive Summary
The target environment featured firewalled servers. The objective was to analyze the 6 distinct port states and fine-tune scan performance while performing TCP Connect, TCP SYN, and UDP scans.

## 2. Key Objectives & Methodologies
* Perform TCP Connect and Half-Open SYN scans to identify open ports.
* Execute UDP connectionless scanning to find exposed stateless services.
* Optimize scan timing and parallelism for efficiency.

## 3. Commands Executed & Payloads Used
`ash
nmap -sT -p- 10.10.10.10
nmap -sS -p 22,80,443 -T3 10.10.10.10
nmap -sU --top-ports 10 --min-parallelism 10 10.10.10.10
`

## 4. Artifact Embedding
| PROOF-01 | Port scan state evaluation | *Terminal Log Verification - Output Recorded in Section 3* |

## 5. Defensive Takeaways
* **Root Cause:** Unnecessary services listening on public interfaces and predictable firewall response patterns to UDP probes.
* **Remediation:** Disable unused services. Configure firewalls to uniformly drop unauthorized traffic rather than returning ICMP Port Unreachable errors to thwart UDP scanning.
