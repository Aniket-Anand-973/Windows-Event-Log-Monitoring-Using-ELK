# Windows Event Log Monitoring using ELK Stack

## 📌 Project Overview

This project demonstrates how to build a Security Operations Center (SOC) monitoring lab using the Elastic Stack (ELK), Winlogbeat, and Sysmon. The lab collects Windows Security and Sysmon logs, stores them in Elasticsearch, and visualizes them in Kibana for security monitoring and incident investigation.

The objective of this project is to simulate real-world SOC monitoring, log analysis, threat detection, and incident investigation.

---

# Project Architecture

Windows 11
↓
Winlogbeat
↓
Elasticsearch
↓
Kibana
↓
SOC Analyst

---

# Technologies Used

- Elasticsearch 8.19.18
- Kibana 8.19.18
- Winlogbeat 8.19.17
- Sysmon
- Ubuntu Server
- Windows 11
- PowerShell
- Git & GitHub

---

# Features

- Windows Security Log Collection
- Winlogbeat Configuration
- Sysmon Integration
- Authentication Monitoring
- Failed Login Detection
- Successful Login Detection
- Process Creation Monitoring
- Kibana Dashboard
- Log Analysis
- Threat Hunting
- Incident Investigation
- MITRE ATT&CK Mapping

---

# Windows Event IDs Monitored

| Event ID | Description |
|----------|-------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 1 | Sysmon Process Creation |

---

# Detection Queries (KQL)

## Failed Login

```kql
event.code:"4625"
```

## Successful Login

```kql
event.code:"4624"
```

## Process Creation

```kql
event.code:"1"
```

## PowerShell Execution

```kql
process.name:"powershell.exe"
```

## Command Prompt

```kql
process.name:"cmd.exe"
```

---

# MITRE ATT&CK Mapping

| Activity | Technique |
|----------|-----------|
| Failed Login | T1110 - Brute Force |
| PowerShell | T1059.001 |
| Process Creation | T1059 |

---

# Screenshots

## Kibana Dashboard

(Add Screenshot)

## Event Viewer

(Add Screenshot)

## Sysmon Events

(Add Screenshot)

## Winlogbeat Configuration

(Add Screenshot)

## Discover View

(Add Screenshot)

---

# Skills Demonstrated

- SIEM Monitoring
- Log Analysis
- Windows Event Monitoring
- Sysmon
- Threat Hunting
- Incident Investigation
- KQL
- Elasticsearch
- Kibana
- Winlogbeat

---

# Project Outcome

Successfully built an end-to-end Windows Event Monitoring Lab using ELK Stack. Configured Winlogbeat and Sysmon to collect Windows Security logs, analyzed authentication and process creation events in Kibana, created KQL-based detections, and performed SOC-style investigations.

---

# Future Improvements

- Add Sigma Rules
- Integrate Wazuh
- Email Alerting
- Slack Alert Integration
- Detection Rules
- Automated Incident Response

---

# Author

**Aniket Anand**

Cyber Security Analyst

LinkedIn:
https://www.linkedin.com/in/aniket-anand973

GitHub:
(Add Your GitHub URL)
