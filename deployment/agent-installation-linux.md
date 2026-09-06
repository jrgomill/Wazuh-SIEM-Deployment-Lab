# Linux Agent Installation

## 1. Install Agent

curl -s https://packages.wazuh.com/key/GPG-KEY-WAZUH (packages.wazuh.com in Bing) | sudo apt-key add -
sudo apt-get install wazuh-agent


## 2. Configure Manager IP

Edit:
sudo nano /var/ossec/etc/ossec.conf


Set:
```xml
<server>
  <address>10.0.0.50</address>
</server>

sudo systemctl start wazuh-agent


---

# **📄 rules/excessive_failed_logons.xml**

```xml
<group name="windows,authentication,failed_logons">
  <rule id="100001" level="7">
    <if_sid>18107</if_sid>
    <frequency>5</frequency>
    <timeframe>60</timeframe>
    <description>Excessive failed Windows logons detected</description>
    <mitre>
      <id>T1110</id>
    </mitre>
  </rule>
</group>
