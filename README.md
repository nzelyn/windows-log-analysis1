# windows-log-analysis1# 🪟 Windows Log Analysis - Home Lab

This project demonstrates a comprehensive **Windows Log Analysis** setup for detecting and responding to potential security incidents in a Windows environment. The setup is ideal for learning SIEM, SOC operations, and hands-on threat detection using real Windows log data.

---

## 📌 Project Objectives

- Collect, parse, and analyze Windows event logs
- Identify security-related events (logins, failures, privilege escalations)
- Detect Indicators of Compromise (IOCs) using open-source tools
- Build your own mini SOC (Security Operations Center) environment

---

## 🛠️ Tools & Technologies Used

- 🖥️ **Windows 10/11 (Lab Machine)**
- 📥 **Event Viewer** for manual log review
- 🔎 **Wazuh** / **Winlogbeat + ELK Stack** for log collection & visualization
- 💾 **Sysmon** for detailed logging
- 📊 **Kibana / Splunk (Free)** for dashboards and threat hunting

---

## 🧪 Use Cases Demonstrated

- Failed/successful login attempts tracking
- Admin privilege escalation detection
- Execution of suspicious binaries (via Sysmon)
- Registry modifications
- PowerShell abuse detection
- Lateral movement and persistence attempts

---

## 🧰 Setup Instructions

> ⚠️ Note: Admin rights may be required for some installations.

### 1. Enable Windows Event Logging
- Audit policies enabled via `secpol.msc` or Group Policy
- Logging categories: Logon, Account Lockout, System, PowerShell

### 2. Install Sysmon
```powershell
Sysmon.exe -accepteula -i sysmonconfig.xml
3. Configure Winlogbeat
Download from Elastic

Set up winlogbeat.yml to forward logs to ELK

4. Deploy Wazuh (Optional)
Use Wazuh agent to monitor Windows and send to Wazuh manager

📊 Sample Dashboards
Top Failed Logins

Logon Type Heatmap

PowerShell Script Execution Events

User Account Lockout Trends

Screenshots of dashboards can be found in the /screenshots folder (if available).

📁 Folder Structure
pgsql
Copy
Edit
windows-log-analysis/
├── configs/
│   ├── sysmonconfig.xml
│   └── winlogbeat.yml
├── scripts/
│   ├── eventlog_export.ps1
├── screenshots/
├── README.md
📚 Learning Outcomes
Hands-on Windows log analysis

Familiarity with Sysmon, Winlogbeat, Wazuh

Threat detection skills in Windows environments

Log correlation and alerting fundamentals

👨‍💻 Author
Naveen A D
Cybersecurity Analyst & Forensics Consultant
🌐 [TryHackMe Top 10% | CEH | CompTIA Security+ | SOC Certified]

📫 Connect with me:

🔗 LinkedIn

📝 Blog

📺 YouTube

📷 Instagram

📜 License
This project is for educational purposes only. Use responsibly.
