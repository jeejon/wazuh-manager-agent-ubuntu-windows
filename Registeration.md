# Wazuh Agent Registration

## 📌 Overview
After installing the Wazuh Agent on Windows, it must be **registered with the Wazuh Manager** (Ubuntu Server) to start sending logs and alerts.  
This document explains how to generate the authentication key, register the agent, and troubleshoot common issues.

---

## 🔑 Step 1: Generate Agent Authentication Key on Wazuh Manager

SSH into your **Ubuntu Server** running Wazuh Manager:

ssh username@SERVER-IP

##  Step 2 Generate an authentication key for your agent:

sudo /var/ossec/bin/manage_agents

From the interactive menu, choose:

(A) Add agent

Enter agent name (e.g Windows-PC)

Enter agent IP address

Copy the generated key shown (we will use this on Windows agent)

Exit manage_agents.

## Step 3 View logs generated

sudo tail -f /var/ossec/logs/ossec.log
