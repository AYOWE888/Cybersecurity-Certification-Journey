# Lab Report: NMAP Host Discovery

- **Certification Track:** eJPT
- **Domain:** Network Attacks
- **Platform:** TryHackMe
- **Date Completed:** 2026-10-03
- **Time Invested:** 1.0 Hours
- **Core Skills & Tools:** 
map, ARP, ICMP

---

## 1. Executive Summary
The target environment involved isolated subnets requiring host discovery techniques. The objective was to identify live hosts using various Layer 2 and Layer 3/4 probing methods, bypassing standard ICMP blocks.

## 2. Key Objectives & Methodologies
* Execute ARP ping sweeps for fast local subnet discovery.
* Utilize ICMP timestamp and TCP SYN/ACK pings to bypass firewalls on remote networks.
* Enumerate live targets for subsequent deep scanning.

## 3. Commands Executed & Payloads Used
`ash
nmap -sn -PR 192.168.1.0/24
nmap -sn -PE -PP -PM 10.10.10.0/24
nmap -sn -PS22,80,443 -PA80 10.10.10.0/24
nmap -sn -PU53,161 10.10.10.0/24
`

## 4. Artifact Embedding
| PROOF-01 | Host discovery ping sweep results | *Terminal Log Verification - Output Recorded in Section 3* |

## 5. Defensive Takeaways
* **Root Cause:** Permissive ICMP and unconventional TCP/UDP traffic allowed through perimeter firewalls enabling hostile network mapping.
* **Remediation:** Configure firewalls to strictly rate-limit or drop non-essential ICMP requests (like Timestamp/Address Mask) and drop unsolicited TCP ACK packets.
