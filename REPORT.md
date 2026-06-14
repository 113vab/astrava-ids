# ASTRAVA

## Cyber Threat Detection & Monitoring Platform

### Project Report

**Developed By:** Vaibhav Vishal
**Organization:** Elevate Labs
**Project Type:** Cybersecurity Monitoring & Threat Detection System
**Technology Stack:** Python, Flask, Scapy, SQLAlchemy, SQLite, HTML, CSS, JavaScript

---

# Executive Summary

ASTRAVA is a real-time Cyber Threat Detection & Monitoring Platform designed to monitor network traffic, identify suspicious activities, and provide actionable security insights through an interactive dashboard.

The platform combines packet capture, threat analysis, database logging, and visualization technologies to simulate the core functionality of a lightweight Security Operations Center (SOC). By continuously monitoring network traffic, ASTRAVA detects abnormal behavior such as port scanning, excessive connection attempts, DNS tunneling patterns, suspicious port activity, and unusually large packet transmissions.

The project was developed to strengthen practical cybersecurity skills while providing hands-on experience with network analysis, intrusion detection, threat monitoring, and dashboard development.

---

# 1. Introduction

Modern networks generate thousands of packets every second. Security analysts rely on monitoring tools to identify malicious activities hidden within this traffic.

Traditional packet capture tools provide visibility but often require manual investigation. ASTRAVA addresses this challenge by automatically analyzing network traffic and generating alerts whenever suspicious behavior is detected.

The system provides both detection and visualization capabilities, allowing users to understand network activity through real-time dashboards and threat intelligence views.

---

# 2. Problem Statement

Network administrators and cybersecurity professionals often struggle to identify suspicious activities in large volumes of network traffic.

Common challenges include:

* Identifying unauthorized scanning attempts.
* Detecting abnormal connection behavior.
* Monitoring traffic in real time.
* Maintaining visibility into network security events.
* Correlating packet activity with potential threats.

ASTRAVA was developed to provide a centralized platform capable of capturing, analyzing, and visualizing network activity in real time.

---

# 3. Project Objectives

The primary objectives of this project were:

### Network Monitoring

Capture and inspect live network traffic.

### Threat Detection

Identify suspicious behavior using predefined security rules.

### Security Analytics

Visualize network events through interactive dashboards.

### Alert Management

Generate and store alerts based on detected anomalies.

### Data Persistence

Maintain packet and alert logs for future investigation.

### Cybersecurity Learning

Develop practical skills in packet analysis and intrusion detection.

---

# 4. System Architecture

The platform follows a modular architecture.

Network Interface
↓
Scapy Packet Sniffer
↓
Packet Processing Engine
↓
Threat Detection Engine
↓
SQLite Database
↓
Flask Backend API
↓
Security Dashboard

### Packet Sniffer Layer

The Packet Sniffer captures live packets using Scapy and extracts:

* Source IP Address
* Destination IP Address
* Protocol Information
* Packet Length
* Packet Summary

The captured information is forwarded to the Threat Detection Engine for further analysis.

### Threat Detection Layer

The Threat Detection Engine evaluates packets against multiple detection rules and generates alerts whenever abnormal behavior is identified.

### Database Layer

SQLite is used to store:

* Packet Logs
* Security Alerts
* Threat Metadata

SQLAlchemy ORM simplifies database interactions and relationships.

### Visualization Layer

The Flask-based dashboard provides:

* Protocol Analysis
* Threat Severity Distribution
* Live Packet Feeds
* Live Threat Feeds
* Threat Source Intelligence
* Security Trend Analysis

---

# 5. Threat Detection Rules

## 5.1 Port Scan Detection

ASTRAVA tracks unique destination ports accessed by each source IP address.

When the number of unique ports exceeds the configured threshold, the system generates a High Severity alert.

Purpose:
Detect reconnaissance activity commonly performed before an attack.

---

## 5.2 Excessive Connection Attempts

The platform monitors TCP connection frequencies.

A host generating excessive connection attempts within a short time window is flagged as suspicious.

Purpose:
Identify brute force attempts and connection flooding activities.

---

## 5.3 ICMP Flood Detection

The system monitors ICMP traffic patterns and identifies excessive packet rates.

Purpose:
Detect potential denial-of-service activity.

---

## 5.4 DNS Tunneling Detection

ASTRAVA evaluates DNS query lengths.

Unusually long DNS requests may indicate covert communication channels used for data exfiltration.

Purpose:
Detect hidden communication attempts.

---

## 5.5 Suspicious Port Detection

The system monitors ports commonly associated with malware, backdoors, and unauthorized remote access.

Examples:

* 1337
* 4444
* 5555
* 6667
* 31337

Purpose:
Identify potentially malicious communication channels.

---

## 5.6 Large Packet Detection

The platform identifies packets with unusually large payloads.

Purpose:
Detect possible bulk transfers or abnormal traffic behavior.

---

## 5.7 Insecure Protocol Detection

Telnet traffic is flagged because it transmits information without encryption.

Purpose:
Identify insecure communication channels.

---

# 6. Dashboard Features

### Threat Level Indicator

Displays the overall security posture of the monitored environment.

Possible states:

* Stable
* Guarded
* Elevated
* Severe
* Critical

### Protocol Distribution

Visualizes network traffic based on protocol usage.

### Severity Distribution

Displays the breakdown of security alerts by severity level.

### Threat Timeline

Tracks alert activity over time.

### Live Activity Feed

Displays recently captured network packets.

### Live Threat Feed

Displays newly generated security alerts.

### Top Threat Sources

Highlights IP addresses generating the highest number of alerts.

---

# 7. Testing & Validation

The platform was tested using normal browsing activity, local network traffic, and simulated suspicious behavior.

The following events were successfully detected:

* Port Scanning
* Excessive Connections
* Large Packet Transfers
* Suspicious Port Usage
* ICMP Activity

Generated alerts were correctly logged and displayed on the dashboard.

---

# 8. Results

The project successfully achieved all primary objectives.

Achievements include:

* Real-time packet monitoring.
* Automated threat detection.
* Security event logging.
* Dashboard-based visualization.
* Historical alert tracking.
* Threat intelligence summarization.

The system processed thousands of packets while maintaining responsive dashboard updates.

---

# 9. Challenges Faced

During development several technical challenges were encountered:

### Dependency Compatibility

SQLAlchemy compatibility issues were encountered with newer Python versions.

### Packet Capture Permissions

Windows packet capture required administrative privileges and Npcap installation.

### Real-Time Synchronization

Maintaining synchronization between packet capture, database updates, and dashboard refresh cycles required additional optimization.

### Dashboard Integration

Backend API structures had to be aligned with frontend visualization requirements.

---

# 10. Future Enhancements

Potential improvements include:

* Machine Learning Based Threat Detection
* Geo-IP Threat Intelligence
* Automated Email Notifications
* PDF Security Reporting
* Multi-User Authentication
* Threat Intelligence Feed Integration
* Advanced SOC Analytics
* Cloud Deployment Support

---

# Conclusion

ASTRAVA successfully demonstrates the implementation of a real-time Cyber Threat Detection & Monitoring Platform capable of capturing network traffic, identifying suspicious behavior, and presenting actionable security insights through an interactive dashboard.

The project provided practical experience in network analysis, intrusion detection, backend development, database management, and cybersecurity operations while establishing a strong foundation for future security-focused enhancements.

---

## Developed By

**Vaibhav Vishal**

**Elevate Labs Cybersecurity Project Program**
