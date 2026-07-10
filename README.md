# 🛡️ AI-Powered SOC Lab using Wazuh, Sysmon, Windows & Kali Linux

## 📌 Project Overview

This project demonstrates the design and implementation of a Security Operations Center (SOC) laboratory using **Wazuh SIEM**, **Sysmon**, **Windows 11**, and **Kali Linux**.

The lab simulates real-world cyber attack scenarios, collects endpoint telemetry, investigates security events using Wazuh, maps each incident to the **MITRE ATT&CK Framework**, and documents the investigation using professional SOC reporting practices.

This project also serves as the foundation for an **AI SOC Analyst**, which will automate alert analysis, MITRE ATT&CK mapping, and incident reporting.

---

# 🏗️ Lab Architecture

```text
                     Kali Linux
                (Attacker Machine)
                        │
                        │
      PowerShell File Download
                        │
                        ▼
              Windows 11 Endpoint
                 Sysmon Installed
                Wazuh Agent Installed
                        │
                        ▼
                 Wazuh Manager
                        │
                        ▼
                Wazuh Dashboard
                        │
                        ▼
              Incident Investigation
                        │
                        ▼
                 AI SOC Analyst
```

---

# 🛠️ Technologies Used

- Wazuh SIEM
- Sysmon
- Windows 11
- Kali Linux
- Oracle VirtualBox
- PowerShell
- Python HTTP Server
- MITRE ATT&CK Framework
- Git & GitHub
- Markdown

---

# 🚨 Simulated Incidents

## 🟢 Incident 01 – PowerShell Execution

**Objective**

Detect PowerShell execution using Sysmon and investigate the activity through Wazuh.

**MITRE ATT&CK**

- T1059.001 – PowerShell

---

## 🟢 Incident 02 – Local User Creation

**Objective**

Detect unauthorized local user account creation.

**Windows Event**

- Event ID 4720

**MITRE ATT&CK**

- T1136.001 – Create Account: Local Account

---

## 🟢 Incident 03 – Failed Login Detection

**Objective**

Investigate failed Windows authentication attempts.

**Windows Event**

- Event ID 4625

**MITRE ATT&CK**

- T1110 – Brute Force

---

## 🟢 Incident 04 – PowerShell File Download

**Objective**

Simulate a PowerShell-based file download from an attacker-controlled Kali Linux HTTP server.

**MITRE ATT&CK**

- T1059.001 – PowerShell
- T1105 – Ingress Tool Transfer

---
# 🚨 Simulated Incidents

- [Incident 01 – PowerShell Execution](./Incident-01-PowerShell-Execution)
- [Incident 02 – Local User Creation](./Incident-02-Local-User-Creation)
- [Incident 03 – Failed Login Detection](./Incident-03-Failed-Login)
- [Incident 04 – PowerShell File Download](./Incident-04-PowerShell-File-Download)

---
  
# 📂 Project Structure

```text
AI-Powered-SOC-Lab-Wazuh
│
├── Incident-01-PowerShell-Execution
├── Incident-02-Local-User-Creation
├── Incident-03-Failed-Login
├── Incident-04-PowerShell-File-Download
│
├── Screenshots
│   ├── Incident-01
│   ├── Incident-02
│   ├── Incident-03
│   └── Incident-04
│
└── README.md
```

Each incident contains:

- 📁 Evidence
- 📝 Notes
- 📄 Technical Report
- 🤖 AI Analysis

---

# 🔍 SOC Investigation Workflow

For every simulated incident:

1. Simulate attacker activity.
2. Generate endpoint telemetry.
3. Collect logs using Sysmon.
4. Forward logs to Wazuh.
5. Investigate alerts in Wazuh.
6. Map findings to MITRE ATT&CK.
7. Document the incident.
8. Produce AI-assisted analysis.

---

# 🎯 Skills Demonstrated

- SIEM Investigation
- Wazuh Administration
- Windows Event Analysis
- Sysmon Log Analysis
- PowerShell Investigation
- Threat Hunting
- Incident Response
- MITRE ATT&CK Mapping
- Endpoint Monitoring
- Technical Documentation

---

# 📸 Evidence

Each incident includes:

- Attack execution screenshots
- Windows Event Viewer evidence
- Sysmon logs
- Wazuh investigation screenshots
- Technical analysis
- AI-generated incident summary

---

# 🚀 Future Improvements

- AI SOC Analyst Web Application
- Wazuh API Integration
- Automated Incident Report Generation
- VirusTotal Integration
- Threat Intelligence Integration
- Sigma Rule Support
- YARA Rule Support

---

# 👨‍💻 Author

**Rudra Mishra**

Final Year B.Tech Student (Electronics & Computer Science)

Interested in **Cybersecurity**, **SOC Operations**, **Threat Detection**, and **Blue Teaming**.

---

# 🙏 Acknowledgements

- Wazuh
- Microsoft Sysinternals (Sysmon)
- MITRE ATT&CK
- Oracle VirtualBox
