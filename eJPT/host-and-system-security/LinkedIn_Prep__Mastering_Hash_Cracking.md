# Lab Report: TryHackMe - Mastering Hash Cracking

- **Certification Track:** eJPT
- **Domain:** Host Security
- **Platform:** TryHackMe
- **Date Completed:** 2026-10-03
- **Time Invested:** 1.0 Hours
- **Core Skills & Tools:** john, zip2john, ar2john, unzip, unrar

---

## 1. Executive Summary
The target environment was a compressed archive protected by a weak password. Demonstrated the extraction of cryptographic hashes and offline dictionary attacks. The objective was to recover the cleartext password and extract the sensitive hidden flag file.

## 2. Key Objectives & Methodologies
* Extract hash representations from ZIP and RAR archives using specialized tools.
* Target auditing by executing John the Ripper with the rockyou.txt wordlist.
* Exploit the vulnerable archive by unpacking it with the recovered credentials.

## 3. Commands Executed & Payloads Used
`ash
zip2john target.zip > hash.txt
rar2john target.rar > hash_rar.txt
john --wordlist=rockyou.txt hash.txt
unzip target.zip
unrar x target.rar
`

## 4. Artifact Embedding
| PROOF-01 | Successfully cracked hash output | *Terminal Log Verification - Output Recorded in Section 3* |

## 5. Defensive Takeaways
* **Root Cause:** Relying on basic archive passwords without implementing robust, high-entropy character strings leaves data open to offline dictionary attacks.
* **Remediation:** Enforce strong, complex passphrases for all encrypted archives. Utilize strong encryption algorithms (e.g. AES-256) and implement key management policies instead of static passwords where possible.
