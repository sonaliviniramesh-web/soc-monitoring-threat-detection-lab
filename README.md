# SOC Monitoring & Threat Detection Lab

This project demonstrates the development of a SOC monitoring and threat detection lab using Splunk Enterprise, Sysmon, Windows Event Logs, and Splunk Universal Forwarder telemetry.

The lab was designed to simulate practical blue-team monitoring workflows including:

- Endpoint telemetry collection
- Detection engineering
- PowerShell abuse monitoring
- LOLBin detection
- Alert creation
- Incident investigation
- Process lineage analysis
- MITRE ATT&CK mapping

The project also involved troubleshooting real telemetry ingestion and Sysmon forwarding issues during development.

---

# Technologies Used

- Splunk Enterprise
- Splunk Universal Forwarder
- Sysmon
- Windows Event Logs
- PowerShell
- SPL (Search Processing Language)

---

# Lab Architecture

Windows Endpoint → Sysmon → Universal Forwarder → Splunk Enterprise

---

# Key Detection Use Cases

## Brute Force Detection
Detection of repeated failed authentication attempts using Windows Security Event ID 4625.

## PowerShell Abuse Detection
Detection of suspicious PowerShell execution using execution policy bypass arguments.

## LOLBin Detection
Detection of suspicious `mshta.exe` execution using Sysmon process creation telemetry.

## Process Lineage Investigation
Analysis of parent-child process relationships using Sysmon Event ID 1 telemetry.

---

# MITRE ATT&CK Techniques Referenced

| Technique | Description |
|---|---|
| T1110 | Brute Force |
| T1218 | Signed Binary Proxy Execution |

---

# Repository Structure

```text
Screenshots/
├── Detections/
├── Investigations/
├── Dashboards/
└── Telemetry/

SPL-Queries/
Investigation-Reports/
Architecture/
```

---

# Notable Learning Areas

One of the most valuable parts of this project was troubleshooting telemetry ingestion problems involving Sysmon forwarding and Windows service permissions affecting the Splunk Universal Forwarder.

The project helped build practical understanding of:
- Windows telemetry collection
- Sysmon process monitoring
- Splunk ingestion troubleshooting
- Detection engineering fundamentals
- SOC investigation workflows

---

# Screenshots

The repository contains:
- Detection screenshots
- Alert evidence
- Sysmon telemetry visibility
- Parent-child process investigations
- DFIR-style investigation notes
- Dashboard visualizations

---

# Future Improvements

Possible future improvements for the lab include:
- Encoded PowerShell detection
- Persistence monitoring
- Registry change detection
- Multi-endpoint telemetry
- Additional Sysmon rules
