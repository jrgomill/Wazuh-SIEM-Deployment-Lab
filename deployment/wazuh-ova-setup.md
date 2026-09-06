# Wazuh OVA Deployment Guide

## 1. Download the OVA

Download the official Wazuh OVA:
https://wazuh.com/downloads/

OVA includes:
- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard

## 2. Import OVA

In VirtualBox / VMware:
- File → Import Appliance
- Select the OVA
- Assign:
  - CPU: 4 vCPU
  - RAM: 8 GB
  - Disk: 50–100 GB

## 3. Initial Configuration

After boot:
- Login: `admin`
- Default password: `admin`
- Change password immediately

Access dashboard:


## 4. Network Setup

Assign static IP:

Apply: sudo nano /etc/netplan/01-netcfg.yaml

Apply: sudo netplan apply


## 5. Validate Services
- systemctl status wazuh-manager
- systemctl status wazuh-indexer
- systemctl status wazuh-dashboard


All should be **active (running)**.

You are now ready to install agents.

