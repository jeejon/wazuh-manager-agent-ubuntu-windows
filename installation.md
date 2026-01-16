# Wazuh Manager Installation on Ubuntu Server

## 📌 Overview
This document provides step-by-step instructions for installing **Wazuh Manager** on an Ubuntu Server system.  
The Wazuh Manager acts as the central component for log analysis, alerting, and endpoint monitoring.

---

## 🖥 System Requirements
- Ubuntu Server 20.04 / 22.04 (64-bit)
- Minimum 8 GB RAM (16 GB recommended)
- Minimum 2 CPU cores
- Minimum 40 GB ROM
- Root or sudo privileges
- Internet connectivity

---

##  Step 1: Update the System
Ensure the server packages are up to date.

sudo apt update && sudo apt upgrade -y

## Step 2: Install basic packages required for installation.

sudo apt install curl apt-transport-https lsb-release gnupg2 -y

## Step 3: Download and Run Wazuh Installation Script

Wazuh provides an all-in-one installation script that installs:
Wazuh Manager
Filebeat
Wazuh Dashboard

curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
sudo bash wazuh-install.sh -a

The -a flag installs all required components automatically.

## Step 4: Wait for Installation to Complete

The installation may take several minutes.
Once completed, you will see credentials for the Wazuh Dashboard.

⚠️ Save the username and password displayed on the screen.

## Step 5: Verify Wazuh Services

sudo systemctl enable wazuh-manager
sudo systemctl enable filebeat

sudo systemctl start wazuh-manager
sudo systemctl start filebeat

sudo systemctl status wazuh-manager
sudo systemctl status filebeat

## Step 6 Access Wazuh Dashboard
Open a browser and visit

https:// SERVER-IP

Log in using the credentials generated during installation.

## Step 7: Confirm Manager Is Ready
From the dashboard:
Ensure the Wazuh Manager is running
Confirm no critical errors are shown
Verify the server is ready to accept agents

🧪 Common Issues & Fixes
Issue: Dashboard not loading

sudo systemctl restart wazuh-dashboard

Issue: Manager service not running

sudo systemctl restart wazuh-manager
