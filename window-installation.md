# Wazuh Agent Installation on Windows

## 📌 Overview
This document explains how to install the **Wazuh Agent** on a Windows 8.1 PC.  
The agent allows your Windows machine to send logs and security events to the **Wazuh Manager** on Ubuntu Server.

---

## 🖥 System Requirements
- Windows 8.1 (64-bit)
- Minimum 8 GB RAM
- Minimum 1 CPU core
- Administrator privileges
- Internet connectivity

---

## 🔄 Step 1: Download Wazuh Agent
1. Open your browser and visit:  
   [Wazuh Downloads](https://wazuh.com/downloads/)
2. Download the **Windows Agent Installer (MSI)** for your system.

---

## 📦 Step 2: Install the Agent
1. Double-click the downloaded `.msi` file.
2. Follow the installation wizard:
   - Accept the license agreement
   - Select installation directory (default is fine)
   - Click **Next** until installation completes

---

## 🔐 Step 3: Configure the Agent
During installation, configure the following:

- **Wazuh Manager IP:** Enter your Ubuntu Server IP  
- **Authentication key** Enter your Authentication key generated from Ubuntu server terminal 
- Finish installation and click **save**
---

## ▶️ Step 4: Generate Authentication key 

Generate authentication key from Wazuh Manager (Ubuntu Server)
Register the agent using the auth key
Confirm the agent appears on the Wazuh dashboard
