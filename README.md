# Wazuh SIEM Deployment Lab

## Overview

This lab demonstrates a full Wazuh SIEM deployment using the official OVA image,
including agent installation, log ingestion, custom detection rules, and
dashboard creation.

The goal is to showcase practical skills in:

- SIEM deployment
- Log ingestion and parsing
- Detection engineering
- Windows + Linux monitoring
- Custom Wazuh rule development
- Dashboard creation and alert analysis

This project pairs with my Active Directory Attack Simulation Lab to provide
end-to-end detection engineering coverage.

---

## Lab Architecture

- **Wazuh Server (OVA)**
  - Wazuh Manager
  - Wazuh Indexer
  - Wazuh Dashboard

- **Windows Server 2022**
  - Wazuh agent
  - Sysmon logging
  - Security event logs

- **Windows 10/11 Workstation**
  - Wazuh agent
  - PowerShell logging

- **Linux Host (optional)**
  - Wazuh agent
  - Syslog monitoring

See `deployment/wazuh-ova-setup.md` for installation details.

---

## Features Implemented

### ✔ Agent Deployment
- Windows Server agent
- Windows workstation agent
- Linux agent (optional)

### ✔ Log Sources Ingested
- Windows Security logs
- Sysmon logs
- PowerShell logs
- Linux auth logs

### ✔ Custom Detection Rules
Located in `/rules/`:
- Excessive failed logons
- Event log clearing (Security log)
- Suspicious PowerShell activity

### ✔ Dashboards
Located in `/dashboards/`:
- Failed logons dashboard
- PowerShell activity dashboard

---

## How to Use This Repo

1. Deploy Wazuh using the OVA guide.
2. Install agents on Windows and Linux hosts.
3. Run attack simulations from my AD lab.
4. Observe alerts in Wazuh.
5. Import dashboards for visualization.
6. Review custom rules and detection logic.

This project is for educational and defensive purposes only.
