**eJPT Engagement Report: ACKme IT Services**

**📋 Engagement Overview**

This report outlines the methodology used during the security assessment of target 240.228.189.136, adhering strictly to the INE eJPT (eLearnSecurity Junior Penetration Tester) curriculum and the PTES (Penetration Testing Execution Standard).

🛠️ Phase 1: Enumeration (Nmap)

The engagement initiated with service discovery to identify the attack surface.


Findings:

Port 80/TCP: Open (HTTP)

Service: Apache/2.4.X (Specific vulnerable build identified)

Observation: Version headers revealed a legacy software stack susceptible to public exploits.

**🔍 Phase 2: Vulnerability Testing****

Following the eJPT walkthrough, we transitioned from scanning to analysis:

CVE Research: Cross-referenced service versions with the National Vulnerability Database (NVD).

Exploit Database: Utilized Exploit-DB to find a verified Proof of Concept (PoC).

Validation: Confirmed the vulnerability manually before attempting exploitation to ensure environment stability.

🚀 **Phase 3: Exploitation & Capture**

With the vulnerability verified, an exploit was deployed to gain initial access.

Exploit Type: Remote Code Execution (RCE)

Payload: Python-based reverse shell

Initial Access: www-data

Privilege Escalation: Exploited local misconfiguration to reach Administrator

Final Flag: THM{ACKME_ENGAGEMENT}

**🎓 eJPT Skill Mapping**

|Domain| |Action Taken|

|Networking & Auditing| |Advanced Nmap service/version detection|

|Vulnerability Research| |Manual CVE/Exploit-DB correlation|

|Exploitation| |Reverse shell management and flag capture|


This document was prepared as part of the eJPT certification preparation path.
