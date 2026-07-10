# Objective

## Purpose

The objective of this incident is to simulate the creation of a new local Windows user account and verify that the activity is detected and logged by the Windows Security Log and Wazuh SIEM.

This exercise demonstrates how account creation events can be monitored, investigated, and documented within a Security Operations Center (SOC) environment.

---

## Learning Objectives

- Simulate local user account creation using the Windows `net user` command.
- Observe Windows Security Event ID 4720 (A user account was created).
- Verify that the Wazuh Agent collects the event and forwards it to the Wazuh Server.
- Investigate the event using the Wazuh Dashboard.
- Map the activity to the MITRE ATT&CK framework.
- Document the incident using standard SOC investigation procedures.