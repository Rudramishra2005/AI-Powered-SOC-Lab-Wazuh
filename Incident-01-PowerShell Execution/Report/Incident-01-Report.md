# Incident Report 01

## Title

PowerShell Process Execution Detection using Sysmon and Wazuh SIEM

---

## Incident Summary

A PowerShell process was intentionally executed on the monitored Windows 11 endpoint to validate the detection capabilities of Sysmon and the Wazuh Security Information and Event Management (SIEM) platform.

The process creation event was successfully captured by Sysmon (Event ID 1), forwarded by the Wazuh Agent, and displayed in the Wazuh Dashboard for investigation.

---

## Environment

| Component | Details |
|-----------|---------|
| Hypervisor | Oracle VirtualBox |
| SIEM | Wazuh 4.14.5 |
| Endpoint | Windows 11 |
| Attacker Machine | Kali Linux |
| Monitoring Tool | Sysmon |
| Agent | Wazuh Agent |

---

## Objective

To verify that PowerShell process execution generates Sysmon telemetry and that the event is successfully collected, forwarded, and displayed by Wazuh.

---

## Attack Performed

### Command

```powershell
powershell.exe
```

---

## Detection

The execution generated a Sysmon Process Creation event (Event ID 1).

The Wazuh Agent collected the event from the Microsoft-Windows-Sysmon/Operational event channel and forwarded it to the Wazuh Server.

The event was successfully observed within the Wazuh Discover interface.

---

## Evidence

- PowerShell execution screenshot
- Wazuh event screenshot
- Sysmon Event ID 1 screenshot

---

## MITRE ATT&CK

| Category | Value |
|----------|-------|
| Tactic | Execution (TA0002) |
| Technique | T1059.001 – PowerShell |

---

## Analysis

The detected activity was intentionally generated for laboratory testing.

Although the execution was legitimate, PowerShell is one of the most frequently abused Windows utilities by attackers because it can execute scripts, download payloads, and automate post-exploitation tasks.

Monitoring PowerShell execution allows analysts to identify suspicious behavior and investigate potentially malicious activity.

---

## Severity

Medium

---

## Recommendations

- Monitor all PowerShell executions.
- Enable PowerShell Script Block Logging.
- Investigate unusual parent-child process relationships.
- Correlate PowerShell activity with network connections and file modifications.

---

## Conclusion

The incident successfully demonstrated end-to-end visibility from endpoint telemetry generation to SIEM detection.

The experiment confirmed that Sysmon, the Wazuh Agent, and the Wazuh Server were correctly configured to capture and analyze PowerShell execution events.