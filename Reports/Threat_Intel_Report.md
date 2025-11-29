# Threat Intelligence Report: Honeypot Deployment & Analysis

## Overview
A T-Pot honeypot was deployed in a cloud environment, capturing over **20,000 intrusion attempts in 48 hours**.  
Using Suricata, Elasticsearch, and Kibana dashboards, attacker behavior, botnet waves, and reconnaissance attempts were analyzed.

---

## Key Findings
- Mirai botnet waves detected every **5–10 minutes**  
- Manual reconnaissance attempts identifiable via irregular probing  
- Suricata signatures triggered for SSH and HTTP exploit attempts  
- High-volume scanning originating from compromised IoT devices  
- Traffic exhibited consistent botnet fingerprints (payload reuse, timing patterns)

---

## MITRE ATT&CK Mapping
| Behavior | Technique |
|---------|-----------|
| SSH brute force | T1110 |
| Automated botnet scanning | T1046 |
| HTTP exploit attempts | T1190 |
| Active scanning | T1595 |

---

## IOC Summary
- Malicious IP addresses  
- Suspicious User-Agent strings  
- Suricata SID alerts  
(See IOC files included in this repository.)

---

## Conclusion
The honeypot effectively captured real-world attacker behavior and provided actionable insights into commodity botnet operations.  
Future improvement areas include:  
- ASN enrichment  
- GeoIP mapping  
- Payload clustering  
- Threat actor correlation  

---
