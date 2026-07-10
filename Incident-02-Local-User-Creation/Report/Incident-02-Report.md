# Incident Report 02

## Title

Unauthorized Local User Account Creation Detection using Windows Security Logs and Wazuh SIEM

---

## Incident Summary

A new local Windows user account was intentionally created on the monitored Windows 11 endpoint using the `net user` command to simulate a common attacker persistence technique.

Windows generated Security Event ID 4720 (A user account was created), which was successfully collected by the Wazuh Agent and forwarded to the Wazuh Server. The event was then investigated using the Wazuh Dashboard.

---

## Environment

| Component | Details |
|-----------|---------|
| Hypervisor | Oracle VirtualBox |
| SIEM | Wazuh 4.14.5 |
| Endpoint | Windows 11 |
| Attacker Machine | Kali Linux |
| Monitoring Tool | Windows Security Log |
| Agent | Wazuh Agent |

---

## Objective

To verify that the creation of a local Windows user account generates Security Event ID 4720 and that the event is successfully collected, forwarded, and displayed by Wazuh.

---

## Attack Performed

### Command

```cmd
net user SOC_TestUser Password@123 /add
```

---

## Detection

The account creation generated Windows Security Event ID 4720.

The Wazuh Agent collected the event from the Windows Security log and forwarded it to the Wazuh Server.

The event was successfully observed and investigated within the Wazuh Dashboard.

---

## Evidence

- Local user creation command screenshot
- Windows Security Event ID 4720 screenshot
- Wazuh Event ID 4720 detection screenshot

---

## MITRE ATT&CK

| Category | Value |
|----------|-------|
| Tactic | Persistence (TA0003) |
| Technique | T1136.001 – Create Account: Local Account |

---

## Analysis

Creating a new local user account is a common persistence technique used by attackers after obtaining administrative privileges. The account can be used to regain access to the system even if the original compromised account is disabled.

In this laboratory exercise, the activity was intentionally performed for educational purposes. The successful detection of Event ID 4720 demonstrates that Windows account management events are being monitored and collected by Wazuh.

---

## Severity

High

---

## Recommendations

- Monitor all user account creation events.
- Review administrative account activity regularly.
- Apply the principle of least privilege.
- Audit local accounts periodically.
- Investigate unexpected account creation immediately.

---

## Conclusion

The incident successfully demonstrated end-to-end visibility of Windows account creation events. Windows generated Security Event ID 4720, the Wazuh Agent collected the event, and the Wazuh Dashboard provided centralized visibility for investigation and analysis.