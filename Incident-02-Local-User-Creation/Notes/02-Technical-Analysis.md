# Technical Analysis

## Attack Overview

A new local Windows user account was intentionally created using the Windows `net user` command to simulate a common persistence technique used by attackers after obtaining administrative privileges.

Windows generated Security Event ID 4720 (A user account was created). The Wazuh Agent successfully collected the event from the Windows Security log and forwarded it to the Wazuh Server, where it became available for investigation through the Wazuh Dashboard.

## Evidence Collected

- Local user creation command executed successfully.
- Windows Security Event ID 4720 generated.
- Wazuh successfully collected Event ID 4720.
- New user account identified during investigation.

## Important Fields Observed

| Field | Description |
|-------|-------------|
| Event ID | Windows Security Event ID 4720 |
| Subject User Name | User account that created the new account |
| Target User Name | Newly created user account |
| Agent Name | Windows endpoint that generated the event |
| Provider Name | Microsoft-Windows-Security-Auditing |
| Timestamp | Time the account was created |

## Investigation Summary

The account creation activity was intentionally performed during the SOC laboratory exercise to simulate attacker persistence. The Windows Security log generated Event ID 4720, and Wazuh successfully collected and displayed the event for analysis. This confirms that account management activities can be monitored and investigated through the SIEM platform.