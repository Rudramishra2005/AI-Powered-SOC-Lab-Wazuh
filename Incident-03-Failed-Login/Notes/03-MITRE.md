# MITRE ATT&CK Mapping

## Tactic

**Credential Access (TA0006)**

The Credential Access tactic represents techniques used by adversaries to obtain account credentials or gain unauthorized access through authentication attempts.

---

## Technique

**Brute Force (T1110)**

Attackers may attempt to guess passwords by repeatedly trying different password combinations until authentication succeeds.

---

## Why this Incident Maps to T1110

During this incident, an incorrect password was intentionally entered for a valid local user account, generating Windows Security Event ID 4625 (An account failed to log on). Wazuh successfully collected the event for investigation.

Although the activity was performed in a controlled laboratory environment, repeated failed authentication attempts are commonly associated with brute-force attacks and password guessing.