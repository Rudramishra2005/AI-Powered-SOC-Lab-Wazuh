# Incident Report 03

## Title

Failed Windows Login Detection using Windows Security Logs and Wazuh SIEM

---

## Incident Summary

A failed login attempt was intentionally generated on the monitored Windows 11 endpoint by entering an incorrect password for a valid local user account. The activity produced Windows Security Event ID 4625 (An account failed to log on), which was successfully collected by the Wazuh Agent and forwarded to the Wazuh Server for investigation.

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

To verify that failed Windows login attempts generate Security Event ID 4625 and that the event is successfully collected, forwarded, and displayed by Wazuh SIEM.

---

## Attack Performed

### Activity

An incorrect password was entered for the local user account `SOCadmin`, generating a failed authentication event.

---

## Detection

The failed authentication generated Windows Security Event ID 4625.

The Wazuh Agent collected the event from the Windows Security log and forwarded it to the Wazuh Server.

The event was successfully observed and investigated within the Wazuh Dashboard.

---

## Evidence

- Failed login attempt
- Windows Security Event ID 4625 screenshot
- Wazuh Event ID 4625 screenshot

---

## MITRE ATT&CK

| Category | Value |
|----------|-------|
| Tactic | Credential Access (TA0006) |
| Technique | T1110 – Brute Force |

---

## Analysis

Repeated failed login attempts are commonly associated with password guessing and brute-force attacks. Monitoring Windows Security Event ID 4625 enables analysts to identify authentication failures and investigate potential unauthorized access attempts.

In this laboratory exercise, the failed login was intentionally generated for testing purposes. The successful collection of Event ID 4625 demonstrates that Windows authentication events are being monitored and analyzed through Wazuh.

---

## Severity

Medium

---

## Recommendations

- Monitor repeated failed login attempts.
- Enable account lockout policies.
- Enforce strong password policies.
- Investigate multiple failures targeting the same account.
- Correlate failed and successful authentication events.

---

## Conclusion

The incident successfully demonstrated end-to-end visibility of Windows failed authentication events. Windows generated Security Event ID 4625, the Wazuh Agent collected the event, and the Wazuh Dashboard provided centralized visibility for investigation and analysis.