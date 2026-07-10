# Objective

## Purpose

The objective of this incident is to simulate a PowerShell-based file download from an attacker-controlled Kali Linux machine and verify that the activity can be investigated using Windows Sysmon and Wazuh SIEM.

This exercise demonstrates how PowerShell is commonly used by attackers to download payloads and how endpoint telemetry can be used during a SOC investigation.

---

## Learning Objectives

- Host a file on Kali Linux using a Python HTTP server.
- Download the file from Windows using PowerShell.
- Observe Sysmon Process Creation events.
- Investigate the activity using Wazuh.
- Map the activity to the MITRE ATT&CK framework.
- Document the incident using SOC investigation procedures.