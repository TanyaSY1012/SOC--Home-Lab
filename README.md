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

<img src="(https://github.com/TanyaSY1012/SOC--Home-Lab/blob/main/screenshots/dashboard-overview.png?raw=true)](https://github.com/TanyaSY1012/SOC--Home-Lab/blob/f627269415f28400a5a74bf17a0aec2a0370c25e/screenshots/dashboard-overview.png" width="900">

![(https://github.com/TanyaSY1012/SOC--Home-Lab/blob/880eac67de84e224b42de28aed3d650c97034921/screenshots/dashboard-overview2.png](https://github.com/TanyaSY1012/SOC--Home-Lab/blob/main/screenshots/dashboard-overview2.png?raw=true)

### Failed Password Detection

![(https://github.com/TanyaSY1012/SOC--Home-Lab/blob/main/screenshots/failed-password-detection.png?raw=true](https://github.com/TanyaSY1012/SOC--Home-Lab/blob/main/screenshots/failed-password-detection.png?raw=true)

### Top Log Sources

![(https://github.com/TanyaSY1012/SOC--Home-Lab/blob/main/screenshots/top-log-sources.png?raw=true)](https://github.com/TanyaSY1012/SOC--Home-Lab/blob/main/screenshots/top-log-sources.png?raw=true)

### Sudo Activity Monitoring

![https://github.com/TanyaSY1012/SOC--Home-Lab/blob/main/screenshots/sudo-activity.png?raw=true](https://github.com/TanyaSY1012/SOC--Home-Lab/blob/main/screenshots/sudo-activity.png?raw=true)
