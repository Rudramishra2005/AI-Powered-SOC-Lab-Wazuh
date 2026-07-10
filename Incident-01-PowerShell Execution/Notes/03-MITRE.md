\# MITRE ATT\&CK Mapping



\## Tactic



\*\*Execution (TA0002)\*\*



The Execution tactic represents techniques that adversaries use to run malicious code on a target system.



\---



\## Technique



\*\*PowerShell (T1059.001)\*\*



PowerShell is a Windows command-line shell and scripting language. Attackers frequently abuse PowerShell to execute commands, automate tasks, download payloads, and perform post-exploitation activities while using legitimate Windows tools.



\---



\## Why this Incident Maps to T1059.001



During this incident, a new PowerShell process (`powershell.exe`) was launched on the Windows endpoint. Sysmon recorded the process creation event (Event ID 1), and the Wazuh Agent forwarded the event to the Wazuh Server.



Although the execution in this lab was intentional and benign, the same technique is commonly observed during real-world attacks. Monitoring PowerShell activity helps security analysts identify suspicious script execution and investigate potentially malicious behavior.

