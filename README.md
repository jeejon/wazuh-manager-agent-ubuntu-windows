# wazuh-manager-agent-ubuntu-windows
# Wazuh SIEM Deployment: Ubuntu Server & Windows Agent

## 📌 Project Overview
This project demonstrates the deployment and configuration of a **Security Information and Event Management (SIEM)** solution using **#0**.

The setup consists of:
- **Wazuh Manager** installed on **#1**
- **Wazuh Agent** installed on a **#2** endpoint

The goal of this project is to simulate a **real-world SOC environment** for endpoint monitoring, log analysis, and threat detection.

---

## 🏗 Architecture
- **Wazuh Manager:** Ubuntu Server  
- **Wazuh Agent:** Windows 8.1 PC  
- **Communication:** Secure agent-manager connection  
- **Monitoring Scope:** Logs, file integrity, system events  

(Architecture diagram available in the `architecture/` folder)

---

## 🛠 Tools & Technologies
- Wazuh Manager & Agent  
- Ubuntu Server (Linux)  
- Windows 8.1  
- File Integrity Monitoring (FIM)  
- Log Analysis & Alerting  
- SSH & Agent Authentication Keys
  

## ⚙️ Implementation Steps

### 1️⃣ Wazuh Manager Setup (Ubuntu Server)
- Installed Wazuh Manager and required components
- Verified services were running successfully
- Generated agent authentication keys

wazuh-manager/installation.md wazuh-manager/configuration.md
### 2️⃣ Wazuh Agent Setup (Windows)
- Installed Wazuh Agent on Windows PC
- Registered the agent using authentication keys
- Confirmed successful connection to the manager

wazuh-agent/windows-installation.md wazuh-agent/agent-registration.md

---

## 🔍 Features Enabled
- 📊 Log collection and analysis  
- 🛡 File Integrity Monitoring (FIM)  
- 🚨 Security alert generation  
- 👁 Endpoint visibility from the Wazuh dashboard  

---

## ✅ Results
- Wazuh Agent successfully connected and visible on the manager
- Logs and security events received from Windows endpoint
- Alerts generated for monitored activities
- Real-time endpoint monitoring achieved

Screenshots are available in the `logs-screenshots/` folder.

---

## 📚 Skills Demonstrated
- SIEM deployment and configuration  
- SOC Analyst fundamentals  
- Linux server administration  
- Windows endpoint security  
- Troubleshooting agent connectivity issues  

---

## 🚀 Future Improvements
- Add multiple agents (Linux & Windows)
- Configure email alert notifications
- Enable compliance checks (CIS, PCI DSS)
- Integrate threat intelligence feeds

---

## 📄 License
This project is licensed under the MIT License.
