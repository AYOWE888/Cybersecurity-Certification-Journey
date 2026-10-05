# Lab Report: Windows NTLM Hashes - Remaining Set

- **Certification Track:** eJPT
- **Domain:** Host Security
- **Platform:** TryHackMe
- **Date Completed:** 2026-10-03
- **Time Invested:** 1.0 Hours
- **Core Skills & Tools:** hashcat, john, NTLM

---

## 1. Executive Summary
The target environment consisted of dumped Windows NTLM hashes. The vulnerability demonstrated was the usage of weak user passwords. The objective was to perform offline cracking to recover cleartext credentials.

## 2. Key Objectives & Methodologies
* Prepare and format the dumped NTLM hashes for offline cracking.
* Execute dictionary and rule-based attacks against the hashes.
* Recover and verify the cleartext passwords.

## 3. Commands Executed & Payloads Used
`ash
hashcat -m 1000 -a 0 hashes.txt rockyou.txt
john --format=NT hashes.txt --wordlist=rockyou.txt
`

## 4. Artifact Embedding
| PROOF-01 | NTLM crack results | *Terminal Log Verification - Output Recorded in Section 3* |

## 5. Defensive Takeaways
* **Root Cause:** Weak user passwords resulting in easily crackable NTLM hashes.
* **Remediation:** Enforce strict password complexity and length requirements (minimum 14 characters). Disable NTLM authentication across the domain and enforce Kerberos to prevent hash dumping and relay attacks.
