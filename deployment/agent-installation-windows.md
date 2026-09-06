# Windows Agent Installation

## 1. Download Agent

From Wazuh dashboard:
- Agents → Deploy new agent → Windows

Download the MSI.

## 2. Install Agent

Run: 
wazuh-agent-<version>.msi

Enter:
- Manager IP
- Agent name (e.g., `WS01`)
- Group: `windows`

## 3. Start Agent

net start wazuh-agent

## 4. Validate Connection

In dashboard:
- Agents → Status → Should show "Active"

## 5. Enable Modules

### Sysmon
Install Sysmon: 
Sysmon64.exe -i sysmonconfig.xml

### PowerShell Logging
Enable via GPO:
- Script Block Logging
- Module Logging

### Windows Event Logs
Enabled by default.

Your Windows host is now fully monitored.

