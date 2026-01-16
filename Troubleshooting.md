# Wazuh Agent & Manager Troubleshooting

## 📌 Overview
This document covers **common issues and solutions** encountered during Wazuh Manager and Agent setup on Ubuntu Server and Windows PC.  
It is intended to help maintain a **stable SOC environment** and ensure agents are sending logs correctly.

---

## 🛠 Common Issues

### 1️⃣ Issue: Windows Agent Shows “No agent available”
**Symptoms:** Agent installed, but Wazuh Dashboard does not show it.  

**Possible Causes:**
- Firewall blocking port `1514` (TCP/UDP)
- Incorrect Manager IP configured on agent

Solution:
Check firewall rules and allow port 1514:

```cmd

netsh advfirewall firewall add rule name="Wazuh 1514" dir=in action=allow protocol=TCP localport=1514

netsh advfirewall firewall add rule name="Wazuh 1514" dir=in action=allow protocol=UDP localport=1514

Confirm the manager IP matches the Ubuntu server IP.

### 2️⃣ Issue: Agent Service Fails to Start

Symptoms: ossec-agent service does not run.

Possible Causes:

Agent installed without Administrator privileges

Windows security blocking service

Solution:

Run Command Prompt as Administrator

Restart agent:

Cmd

ossec-control.exe start

Reinstall agent if needed

### 3️⃣ Issue: Manager Not Receiving Logs

Symptoms: Agent appears online but no logs visible in dashboard.

Possible Causes:

Log collection not configured

Agent unable to communicate due to network issues

Solution:

Check agent status:

cmd

ossec-control.exe status

Confirm agent is connected in manager:

sudo /var/ossec/bin/agent_control -l

Check firewall/network connectivity between Windows and Ubuntu server

### 4️⃣ Issue: Authentication Key Invalid

Symptoms: Agent registration fails with key errors.

Solution:

Regenerate agent key on Ubuntu:

sudo /var/ossec/bin/manage_agents

Copy new key and re-import on Windows agent:


##@ 5️⃣ Issue: Dashboard Not Loading

Symptoms: Wazuh web interface inaccessible.

Solution:

sudo systemctl status wazuh-dashboard

sudo systemctl restart wazuh-dashboard

Ensure HTTPS port (default 5601) is open

Verify credentials
