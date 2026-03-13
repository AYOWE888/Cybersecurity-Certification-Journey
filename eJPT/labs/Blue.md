#,Question,Key Analysis Point
1,Which Nmap script verified the flaw?,smb-vuln-ms17-010—Verification is vital before exploitation.
2,What is the highest Windows privilege?,NT AUTHORITY\SYSTEM—Achieved in this lab.
3,Why is SMBv1 dangerous?,Legacy protocol with poor memory handling/no encryption.
4,"What does a ""Staged"" payload do?","Uses a ""stager"" to pull the main payload, saving memory space."
5,What is the primary risk of EternalBlue?,"Can cause BSOD, impacting the Availability pillar."
6,"What is a ""Message Digest"" (Hash)?",One-way mathematical password representation (from hashdump).
7,How do we find the exploit in MSF?,Using the search command with ms17-010.
8,How does this link to CCNA?,SMB is Layer 7; operates over TCP Port 445.
