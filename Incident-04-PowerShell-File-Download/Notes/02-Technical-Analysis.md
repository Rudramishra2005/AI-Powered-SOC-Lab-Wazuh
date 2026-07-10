# Technical Analysis

## Attack Overview

A harmless text file was hosted on a Kali Linux machine using Python's built-in HTTP server. The monitored Windows 11 endpoint downloaded the file using PowerShell's Invoke-WebRequest command.

The download was verified through the Kali HTTP server logs, Windows endpoint activity, and Sysmon process creation events.

## Attack Flow

Kali Linux hosted the file using Python HTTP Server on port 8000.

Windows executed:

Invoke-WebRequest

to download the file from the Kali machine.

The downloaded file was successfully saved in the Downloads folder.

## Evidence Collected

- Python HTTP server running on Kali.
- HTTP GET request received by Kali.
- File successfully downloaded on Windows.
- Sysmon process activity observed.
- Wazuh investigation completed.

## MITRE ATT&CK

Execution (TA0002)

T1059.001 – PowerShell

Command and Control (TA0011)

T1105 – Ingress Tool Transfer

## Investigation Summary

The activity simulated a common malware delivery technique where PowerShell downloads a payload from a remote server.

Although the downloaded file was harmless, the attack chain demonstrated attacker-to-victim communication between Kali Linux and the monitored Windows endpoint.