# MITRE ATT&CK Mapping

## Tactic

Execution (TA0002)

Command and Control (TA0011)

---

## Techniques

T1059.001 – PowerShell

PowerShell is frequently abused by attackers to execute commands, automate malicious activity, and download payloads.

---

T1105 – Ingress Tool Transfer

Attackers commonly download tools or payloads from remote servers after gaining access to a system.

---

## Why this Incident Maps Here

During this incident, Windows used PowerShell's Invoke-WebRequest command to download a file from a Kali Linux HTTP server.

This simulated a common attacker technique used during malware delivery and post-exploitation.