# SOC Home Lab – Splunk Enterprise

## Overview

This project demonstrates a self-built SOC (Security Operations Center) home lab using Splunk Enterprise running on Ubuntu Linux inside Microsoft Hyper-V.

The lab was designed to simulate real-world SIEM operations by ingesting Linux telemetry, monitoring authentication activity, visualizing security events, and developing SPL-based detections.

---

## Technologies Used

- Splunk Enterprise
- Ubuntu Linux
- Microsoft Hyper-V
- SPL (Search Processing Language)
- Linux System Logs
- Authentication Log Monitoring

---

## Skills Demonstrated

- SIEM administration
- Linux log analysis
- Security telemetry ingestion
- SPL query development
- Security dashboard creation
- Authentication monitoring
- Threat detection engineering
- Privilege escalation monitoring
- Virtualization using Hyper-V

---

## Dashboard Panels

- Authentication Events Over Time
- Failed Password Attempts
- Top Log Sources
- Event Volume Monitoring
- Sudo Activity Monitoring

---

## Example SPL Queries

### Failed Password Detection

```spl
index=main "password check failed"
| stats count by host
```

### Authentication Events Over Time

```spl
index=main auth
| timechart span=1h count
```

### Sudo Activity Monitoring

```spl
index=main sudo
| timechart span=1h count
```

---

## Project Architecture

Ubuntu Linux VM running in Microsoft Hyper-V generated authentication and system telemetry which was ingested into Splunk Enterprise for monitoring, visualization, and threat detection analysis.

---

## Screenshots

### SOC Dashboard Overview

PLACEHOLDER

### Failed Password Detection

PLACEHOLDER

### Top Log Sources

PLACEHOLDER

### Sudo Activity Monitoring

PLACEHOLDER
