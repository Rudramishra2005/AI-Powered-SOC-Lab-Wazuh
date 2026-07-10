# Objective

## Purpose

The objective of this incident is to simulate a failed Windows login attempt and verify that the activity is detected and logged by the Windows Security Log and Wazuh SIEM.

This exercise demonstrates how failed authentication attempts can be monitored, investigated, and documented within a Security Operations Center (SOC) environment.

---

## Learning Objectives

- Simulate a failed Windows login attempt.
- Observe Windows Security Event ID 4625 (An account failed to log on).
- Verify that the Wazuh Agent collects the event and forwards it to the Wazuh Server.
- Investigate the event using the Wazuh Dashboard.
- Map the activity to the MITRE ATT&CK framework.
- Document the incident using standard SOC investigation procedures.