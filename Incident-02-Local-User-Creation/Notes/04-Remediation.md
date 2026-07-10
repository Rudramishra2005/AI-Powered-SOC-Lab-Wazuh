# Remediation Recommendations

## Objective

The local user account creation observed during this incident was intentionally performed for testing purposes. Although no malicious activity was identified, unauthorized account creation is a common persistence technique used by attackers. The following recommendations help reduce the risk of unauthorized local account creation.

---

## Recommended Actions

### 1. Monitor User Account Creation
Continuously monitor Windows Security Event ID 4720 using Wazuh to detect newly created local user accounts.

### 2. Review Administrative Activity
Verify that the account creation was performed by an authorized administrator and was part of an approved administrative task.

### 3. Apply Least Privilege
Limit administrative privileges to only authorized users to reduce the risk of unauthorized account creation.

### 4. Audit Local User Accounts
Regularly review local user accounts and remove accounts that are no longer required or appear suspicious.

### 5. Correlate Related Events
Investigate associated logon events, privilege changes, group membership modifications, and other account management activities to determine whether the account creation is part of a larger attack.

---

## Conclusion

In this lab, the account creation was legitimate and generated for testing purposes. However, unauthorized local account creation is frequently used by attackers to establish persistence. Continuous monitoring and regular auditing of user account management events are essential for detecting suspicious activity.