# AI SOC Analyst Report

## Alert Summary

A new local Windows user account (**SOC_TestUser**) was created on the endpoint **Windows-11-SOC**. Windows generated Security Event ID **4720 (A user account was created)**, which was successfully collected by the Wazuh Agent and forwarded to the Wazuh Server for centralized analysis.

---

## Risk Assessment

**Risk Level:** High

Creating a new local user account is a legitimate administrative task; however, it is also a common persistence technique used by attackers after obtaining administrative privileges. Unauthorized account creation may allow an attacker to maintain long-term access to the system.

---

## MITRE ATT&CK

**Persistence (TA0003)**

**T1136.001 – Create Account: Local Account**

---

## Investigation Checklist

The analyst should verify:

- Who created the account.
- Whether the account creation was authorized.
- If the account was added to privileged groups.
- Any successful or failed logons using the new account.
- Other account management events occurring around the same time.

---

## Recommended Response

- Confirm whether the account creation was approved.
- Disable or remove unauthorized accounts.
- Review administrative activity around the event.
- Continue monitoring for additional persistence techniques.

---

## AI Conclusion

The detected activity involved the creation of a local Windows user account. During this SOC laboratory exercise, the activity was intentionally performed for testing and validation purposes.

In a production environment, unexpected local account creation should be treated as a high-priority event because it may indicate an attacker attempting to establish persistence.