# AI SOC Analyst Report

## Alert Summary

A Windows endpoint downloaded a file from a Kali Linux HTTP server using PowerShell's Invoke-WebRequest command. The activity simulated a common attacker technique used to transfer payloads from an external system.

---

## Risk Assessment

Risk Level: High

PowerShell-based downloads are frequently observed during malware delivery and post-exploitation. Any unexpected PowerShell download should be investigated immediately.

---

## MITRE ATT&CK

Execution (TA0002)

T1059.001 – PowerShell

Command and Control (TA0011)

T1105 – Ingress Tool Transfer

---

## Investigation Checklist

- Verify who executed the PowerShell command.
- Review the destination IP address.
- Confirm whether the downloaded file is legitimate.
- Review subsequent process activity.
- Investigate persistence or additional downloads.

---

## Recommended Response

- Validate the downloaded file.
- Review PowerShell activity on the endpoint.
- Monitor for additional network communication.
- Isolate the endpoint if malicious activity is confirmed.

---

## AI Conclusion

The activity successfully demonstrated a PowerShell-based file download from an attacker-controlled Kali Linux server. Although the file was harmless and generated for laboratory purposes, the behavior closely resembles common malware delivery techniques observed in real-world attacks.