# 🛡️ Cybersecurity Incident Report 

## 📡 Network Traffic Analysis

This report documents a simulated investigation conducted during **Course 3: Connect and Protect – Networks and Network Security** (Google Cybersecurity Certificate). The activity involved analyzing suspicious DNS and ICMP traffic between two hosts to determine the root cause of a network communication issue.

---

### 🧩 Part 1: Summary of the Problem (DNS and ICMP Traffic)

| Description | Analysis |
| :---- | ----- |
| DNS/ICMP Issue | The UDP protocol reveals that multiple DNS queries were sent from `192.51.100.15` to the DNS server at `203.0.113.2`, requesting an A record for `yummyrecipesforme.com`. However, the ICMP echo reply returned the error: `"udp port 53 unreachable."` This indicates that DNS requests could not be processed. UDP port 53 is used for DNS lookups. The server may be down, misconfigured, or blocking queries from the source IP. |

---

### 🔍 Part 2: Analysis of the Incident

| Detail | Findings |
| :---- | -------- |
| **Time of Incident** | 13:24:32 |
| **How Incident Was Detected** | Network monitoring alerts and/or user reports of failed DNS lookups |
| **Actions Taken** | Connectivity between `192.51.100.15` and `203.0.113.2` was tested multiple times using ICMP. Responses confirmed that UDP port 53 was unreachable. |
| **Key Findings** | DNS server at `203.0.113.2` is either rejecting or not responding to requests. ICMP error supports DNS resolution failure. |
| **Likely Cause** | DNS server issue due to one or more of the following: <br> - DDoS attack <br> - Misconfiguration <br> - Firewall blocking requests |
| **Next Steps** |  - Review DNS server logs <br> - Check firewall rule sets <br>  - Restart DNS services if necessary |

---
