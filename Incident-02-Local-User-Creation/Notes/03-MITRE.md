# MITRE ATT&CK Mapping

## Tactic

**Persistence (TA0003)**

The Persistence tactic consists of techniques that adversaries use to maintain access to a compromised system across reboots, logouts, or password changes.

---

## Technique

**Create Account: Local Account (T1136.001)**

Adversaries may create a local user account to maintain persistent access to a compromised Windows system. These accounts can be used later to log in, escalate privileges, or avoid losing access if the original compromised account is disabled.

---

## Why this Incident Maps to T1136.001

During this incident, a new local Windows user account (`SOC_TestUser`) was created using the `net user` command. Windows generated Security Event ID 4720 (A user account was created), which was successfully collected by the Wazuh Agent and forwarded to the Wazuh Server.

Although the activity was intentionally performed as part of this SOC laboratory exercise, the same technique is commonly used by attackers to establish persistence after compromising a system. Monitoring account creation events enables security analysts to identify unauthorized user creation and investigate potential persistence mechanisms.