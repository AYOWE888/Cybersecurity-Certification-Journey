# TryHackMe Room Completion: SOC Workbooks and Lookups

## Executive Summary
* **Date:** June 9, 2026
* **Platform:** [TryHackMe | SOC Workbooks and Lookups](https://tryhackme.com/room/socworkbookslookups)
* **Milestones Achieved:** 100% Room Completion | 72-Day Continuous Learning Streak | Advanced to #2 Platinum League (MAGE Tier, 232 Points)

---

## 1. Operational Analysis (The "Why")
In a Tier 1 Security Operations Center (SOC) environment, consistency eliminates human error. When security alerts trigger, analysts cannot rely on a hunch or unverified intuition. 

Modular Workbooks (Playbooks) serve as repeatable, step-by-step technical blueprints that guide an analyst through structured **Enrichment** and **Investigation** phases. This process ensures true threats are instantly escalated while false positives are tuned out efficiently, saving critical operational time.

---

## 2. Technical Triage Workflows (The Process)

### Phase A: External Email Analysis (Workbook 01)
* **Objective:** Triage a high-severity alert indicating a suspicious phishing email delivery containing a potentially malicious script/binary attachment.
* **Execution Pathway:**
  1. **Header Parsing:** Utilized an EML Analyzer to break down the raw message file, evaluating routing servers via Mail Transfer Agents (MTAs).
  2. **Identity Authentication:** Checked public DNS indicators to verify **SPF (Sender Policy Framework)** host alignments and **DKIM (DomainKeys Identified Mail)** cryptographic signatures to determine if the origin was faked.
  3. **Payload Isolation:** Extracted hidden URLs and isolated attachment files to safely compute unique cryptographic hashes ($\text{MD5}$ / $\text{SHA-256}$) for Sandbox execution and Threat Intelligence (TI) reputation lookups.
* **Result:** Successfully isolated malicious artifacts and submitted the first flag: `THM{the_most_common_soc_workbook}`.

### Phase B: PowerShell Script Analysis (Workbook 02)
* **Objective:** Triage a critical alert involving an unauthorized executable download spawned by a background PowerShell session.
* **Execution Pathway:**
  1. **Asset Contextualization:** Assigned the alert and queried asset inventories to determine the machine's functional baseline.
  2. **Data Preservation:** Preserved volatile SIEM logs covering the `[WIN] Process Tree` and `[WIN] Login Timeline`.
  3. **Process Tree Reconstruction:** Traced parent-child process relationships to identify how PowerShell was spawned (e.g., checking if it originated from a compromised browser or macro-enabled document).
  4. **Verification:** Audited the download URL via reputation feeds and initiated out-of-band communication with the end-user to confirm authorization status.
* **Result:** Confirmed execution anomalies and submitted the second flag: `THM{be_vigilant_with_powershell}`.

---

## 3. Key Defensive Takeaways (The Results)
* **The 5 W's Rule:** Mastered structured escalation reporting to Tier 2 (L2) teams by summarizing **Who** (Identity context), **What** (Malicious actions observed), **Where** (Source IP/ASN infrastructure), **When** (Precise UTC timeline), and **Why** (Analytical verdict).
* **Infrastructure Auditing:** Learned to leverage Autonomous System Numbers (ASNs) to evaluate network boundaries and identify malicious or bulletproof Internet Service Providers (ISPs).

---

## Reference Material
* **Interactive Training:** [TryHackMe | SOC Workbooks and Lookups](https://tryhackme.com/room/socworkbookslookups)
* **Core Concepts:** Process Tree Auditing, EML Parsing, Infrastructure Enrichment, and SIEM Timeline Reviews.

## Proof of Completion
* **Status:** Complete (6/6 Tasks)
* **Evidence:** Screenshots of completed interactive workbook logic models captured locally to accompany this log.
