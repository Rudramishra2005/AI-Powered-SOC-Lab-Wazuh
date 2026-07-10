# AI SOC Analyst Report

## Alert Summary

A failed Windows login attempt was detected on the endpoint **Windows-11-SOC**. Windows generated Security Event ID **4625 (An account failed to log on)**, which was successfully collected by the Wazuh Agent and forwarded to the Wazuh Server for centralized analysis.

---

## Risk Assessment

**Risk Level:** Medium

A single failed login attempt is not necessarily malicious. However, repeated authentication failures may indicate password guessing or brute-force attacks targeting user accounts.

---

## MITRE ATT&CK

**Credential Access (TA0006)**

**T1110 – Brute Force**

---

## Investigation Checklist

The analyst should verify:

- Which account was targeted.
- The logon type.
- The failure reason.
- The source workstation or IP address (if available).
- Whether multiple failed attempts occurred within a short period.
- Whether a successful login followed the failed attempts.

---

## Recommended Response

- Monitor for repeated failed authentication attempts.
- Review account lockout events.
- Verify whether the login attempts were authorized.
- Continue monitoring for suspicious authentication activity.

---

## AI Conclusion

The detected activity involved a failed authentication attempt against a local Windows user account. During this SOC laboratory exercise, the activity was intentionally performed to validate Windows Security Event ID 4625 collection through Wazuh.

In a production environment, multiple failed login attempts should be investigated as potential indicators of brute-force or password guessing attacks.