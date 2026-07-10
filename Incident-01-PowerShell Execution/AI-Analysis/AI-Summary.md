# AI SOC Analyst Report

## Alert Summary

A PowerShell process was detected on the endpoint **Windows-11-SOC**.

Sysmon generated a Process Creation event (Event ID 1), which was successfully collected by the Wazuh Agent and forwarded to the Wazuh Server.

---

## Risk Assessment

**Risk Level:** Medium

PowerShell is a legitimate administrative tool. However, it is frequently abused by attackers for malicious scripting, payload execution, persistence, and post-exploitation activities.

The execution observed in this incident was part of a controlled laboratory exercise.

---

## MITRE ATT&CK

**Execution (TA0002)**

**T1059.001 – PowerShell**

---

## Investigation Checklist

The analyst should verify:

- Which user executed PowerShell.
- The full command line.
- The parent process.
- Child processes created afterward.
- Network connections initiated by the process.
- File modifications related to the execution.

---

## Recommended Response

- Confirm whether the execution was authorized.
- Review additional endpoint activity around the same timestamp.
- Continue monitoring subsequent PowerShell executions.
- Escalate only if suspicious command lines or related malicious behavior are identified.

---

## AI Conclusion

Based on the available telemetry, the activity appears to be a legitimate administrative execution performed during a controlled SOC laboratory exercise.

No indicators of compromise were identified.

The event demonstrates successful endpoint monitoring using Sysmon and centralized log collection through Wazuh SIEM.