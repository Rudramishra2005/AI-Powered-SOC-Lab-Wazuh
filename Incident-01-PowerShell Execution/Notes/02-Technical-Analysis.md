\# Technical Analysis



\## Attack Overview



A PowerShell process was intentionally executed on the Windows 11 endpoint to generate a Sysmon Process Creation event (Event ID 1). The Wazuh Agent collected the event from the Microsoft-Windows-Sysmon/Operational event channel and forwarded it to the Wazuh Server for analysis.



\## Evidence Collected



\- Process Name: powershell.exe

\- Event Source: Sysmon

\- Event ID: 1 (Process Creation)

\- Endpoint: Windows-11-SOC

\- Detection Platform: Wazuh SIEM



\## Important Fields Observed



| Field | Description |

|-------|-------------|

| Image | Full path of the executed process |

| OriginalFileName | Original executable name |

| ProcessId | Windows Process ID |

| ProcessGuid | Unique identifier for the process |

| ParentProcessGuid | Identifies the process that launched PowerShell |

| UtcTime | Time when the event occurred |

| Agent Name | Endpoint that generated the event |



\## Investigation Summary



The execution of PowerShell was successfully captured by Sysmon and forwarded to Wazuh. The event confirms that endpoint telemetry collection and SIEM ingestion are functioning correctly.

