eJPT Methodology Report: ACKme IT Services

Phase: Enumeration & Vulnerability Assessment
Target: 240.228.189.136

1. Information Gathering & Enumeration

In accordance with the INE eJPT standard, the engagement began with active reconnaissance.

Tool: Nmap

Objective: Identify open ports, services, and version numbers.

Result: Discovered a web service running on port 80. Version detection indicated a specific software build known to have public vulnerabilities.

2. Vulnerability Analysis

Once the service was identified through Nmap, we moved from Enumeration to Vulnerability Research:

NVD/CVE Cross-Referencing: The service version was checked against the National Vulnerability Database.

Exploit Selection: Using the findings from the enumeration phase, we searched Exploit-DB for a matching Proof of Concept (PoC) that could target the specific service version found by Nmap.

3. Exploitation (The "Showcase")

With a verified exploit found during research, we executed the attack:

Attack Vector: Remote Code Execution (RCE).

Outcome: Established a reverse shell.

Post-Exploitation: Verified identity using whoami.

Flag Captured: THM{ACKME_ENGAGEMENT}

4. eJPT Skill Alignment

| eJPT Domain | Activity Performed |
| Assessment Methodologies | Used NVD to understand vulnerability impact. |
| Host & Networking Auditing | Enumerated services via Nmap. |
| Web Application Penetration Testing | Identified and exploited a web-based RCE. |
