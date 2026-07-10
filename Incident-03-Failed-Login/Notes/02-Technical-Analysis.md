# Technical Analysis

## Attack Overview

A failed Windows login attempt was intentionally performed by entering an incorrect password for a valid local user account. Windows generated Security Event ID 4625 (An account failed to log on). The Wazuh Agent successfully collected the event from the Windows Security log and forwarded it to the Wazuh Server, where it became available for investigation through the Wazuh Dashboard.

## Evidence Collected

- Failed login attempt performed successfully.
- Windows Security Event ID 4625 generated.
- Wazuh successfully collected Event ID 4625.
- Failed authentication details identified during investigation.

## Important Fields Observed

| Field | Description |
|-------|-------------|
| Event ID | Windows Security Event ID 4625 |
| Target User Name | Account that failed to authenticate |
| Logon Type | Type of logon attempt |
| Failure Reason | Reason authentication failed |
| Agent Name | Windows endpoint that generated the event |
| Provider Name | Microsoft-Windows-Security-Auditing |
| Timestamp | Time the failed login occurred |

## Investigation Summary

The failed login activity was intentionally generated during the SOC laboratory exercise to simulate a password guessing attempt. Windows generated Security Event ID 4625, and Wazuh successfully collected and displayed the event for investigation.