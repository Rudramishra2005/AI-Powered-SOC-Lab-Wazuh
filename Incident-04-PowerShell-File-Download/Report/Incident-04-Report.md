# Incident Report 04

## Title

PowerShell File Download Detection using Kali Linux, Sysmon and Wazuh SIEM

---

## Incident Summary

A harmless file was hosted on a Kali Linux HTTP server and downloaded by the monitored Windows 11 endpoint using PowerShell's Invoke-WebRequest command. The activity simulated a common attacker technique for downloading payloads from a remote server.

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

To simulate a PowerShell-based file download from an attacker-controlled system and investigate the activity using Windows endpoint telemetry and Wazuh SIEM.

---

## Attack Performed

### Kali Linux

Hosted a file using:

python3 -m http.server 8000

### Windows

Downloaded the file using:

Invoke-WebRequest

---

## Detection

The HTTP request was successfully received by the Kali server.

The file was successfully downloaded to the Windows endpoint.

Sysmon recorded related endpoint activity, allowing the incident to be investigated.

---

## Evidence

- Kali HTTP server
- HTTP GET request
- Successful file download
- Windows Sysmon event
- Wazuh investigation

---

## MITRE ATT&CK

| Category | Value |
|----------|-------|
| Tactic | Execution (TA0002) |
| Technique | T1059.001 – PowerShell |
| Technique | T1105 – Ingress Tool Transfer |

---

## Severity

High

---

## Recommendations

- Monitor PowerShell execution.
- Restrict unauthorized PowerShell usage.
- Investigate unexpected file downloads.
- Correlate PowerShell activity with network connections.

---

## Conclusion

The incident demonstrated an attacker-controlled file transfer from Kali Linux to a monitored Windows endpoint using PowerShell. The activity was validated through endpoint telemetry and network evidence, illustrating a common malware delivery technique.