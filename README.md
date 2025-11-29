# Live Honeypot Deployment & Threat Intelligence Analysis

A cloud-hosted honeypot environment built using the **T-Pot multi-honeypot framework** to capture real-world attack traffic.  
This project focuses on collecting malicious telemetry, analyzing attacker behavior, separating botnet activity from manual reconnaissance, and mapping findings to MITRE ATT&CK techniques.

---

## 🔍 Project Overview

I deployed a fully functional **T-Pot honeypot** in a cloud environment and monitored live attacks from the internet.  
The honeypot automatically captured SSH, HTTP, SMB, and ICS traffic through multiple honeypots (Cowrie, Dionaea, etc.) and correlated logs using Suricata + Kibana dashboards.

In the first 48 hours, the system logged **20,000+ intrusion attempts**.

This project demonstrates:
- Threat intelligence fundamentals  
- Suricata alert analysis  
- Botnet fingerprinting (Mirai)  
- IOC extraction  
- ELK-based visualization  
- Cloud honeypot deployment and monitoring  

---

## 🧱 Architecture

- **Cloud VM (Ubuntu Server)**  
- **T-Pot 23.x** (Cowrie, Dionaea, Suricata, Elastic Stack, Attack Map)  
- **Suricata IDS**  
- **Elasticsearch + Kibana dashboards**  
- **SSH forwarder for remote analysis**  

Traffic Flow:
Internet → Honeypots → Suricata → Logstash → Elasticsearch → Kibana → Analysis

---

## 📊 Traffic Captured (First 48 Hours)

- **20,000+ total attacks**
- **Top attack types**
  - SSH brute force
  - Mirai botnet scanning
  - HTTP exploit attempts
  - Masscan-like port sweeps

- **Top origins**
  - US, Russia, China, India  
  (typical for IoT botnets)

---

## 🔥 Key Analyses Performed

### 1. **Mirai Botnet Identification**
Observed patterns:
- Repeated SSH credential attempts  
- Identical payload sequences  
- Predictable timing intervals (botnet waves)  
- Mirai fingerprinted User-Agents and telnet probes  

### 2. **Manual Reconnaissance Detection**
Indicators of a human attacker:
- Irregular probing  
- Unique commands  
- Targeted enumeration  

### 3. **Suricata Alert Analysis**
Common signatures:
- SSH brute force  
- Mirai exploitation  
- HTTP directory traversal  
- Suspicious User-Agent strings  

---

## 🧪 MITRE ATT&CK Mapping

| Behavior | Technique |
|---------|-----------|
| SSH brute force | T1110 |
| Automated botnet scanning | T1046 |
| HTTP exploit attempts | T1190 |
| Reconnaissance sweeps | T1595 |

---

## 📈 Sample Findings

- Multiple Mirai botnet clusters consistently targeting ports 22/23  
- High-volume scanning from compromised IoT devices  
- Suricata signatures triggered by inbound exploitation payloads  
- Attack patterns repeating every 5–10 minutes  

---

## 📁 Repository Structure

/Screenshots  
   kibana-dashboard.png  
   suricata-alerts.png  
   mirai-pattern.png  

/IOCs  
   ioc-ips.txt  
   ioc-useragents.txt  
   ioc-suricata-sids.txt  

/Reports  
   Threat_Intel_Report.pdf  

README.md

---

## 🧠 Key Learnings

- How real attackers behave on the internet  
- How botnets cycle through global targets  
- How Suricata logs + Kibana dashboards help identify TTPs  
- Operational use of multi-honeypot platforms  
- How to extract IOCs and map activity to MITRE ATT&CK  
- Fundamentals of threat intelligence reporting  

---

## 📬 Contact

LinkedIn: linkedin.com/in/Anirudh-Mehandru
