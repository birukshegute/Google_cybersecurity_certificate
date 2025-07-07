# 🛡️ Cybersecurity Incident Report  

## 🌐 DDoS Attack Analysis — NIST Framework Alignment

This report was completed as the final portfolio project for **Course 3: Connect and Protect – Networks and Network Security**. The scenario involved a simulated Distributed Denial of Service (DDoS) attack that disrupted a multimedia company’s internal services. The report applies the NIST Cybersecurity Framework to analyze the incident, and propose mitigation and recovery strategies.

---

### 📝 Summary of the Incident

The organization experienced a **Distributed Denial of Service (DDoS)** attack that disrupted internal network operations for approximately two hours.

- The attack leveraged **ICMP packet flooding**
- Exploited a **misconfigured firewall**, which allowed unfiltered ICMP traffic.
- Employees lost access to critical systems during the outage.

**Response actions included**:

- Blocking ICMP traffic
- Shutting down non-essential systems
- Implementing updated firewall rules and monitoring solutions

---

## 🔎 NIST Cybersecurity Framework Breakdown

### 🧩 Identify

- **Type of attack**: ICMP-based DDoS  
- **Cause**: Improperly configured firewall  
- **Targeted Systems**: Internal infrastructure and services  
- **Attack Vector**: Spoofed ICMP traffic from external sources  
- **Impact**: Two-hour outage, service disruption, productivity loss  
- **Security Gaps**:
  - No ICMP filtering  
  - Lack of proactive monitoring and alerts  

---

### 🛡️ Protect

- Configure firewall to **limit ICMP traffic**  
- **Close unused ports** and restrict unnecessary protocols  
- Implement **source IP verification**  
- Apply **network segmentation** to contain impact  
- Conduct **regular firewall audits** and access reviews  
- Provide **employee training** on response procedures  

---

### 🔍 Detect

- Deploy **IDS/IPS** to detect abnormal traffic  
- Use **network monitoring tools** with alert thresholds  
- Track **access logs, user behavior**, and system activity  
- Establish **baseline traffic patterns**  
- Implement **SIEM** for centralized threat detection  

---

### 🚨 Respond

- Block malicious traffic via firewall  
- **Isolate affected systems** as needed  
- Shut down **non-critical services** to preserve bandwidth  
- Analyze traffic and logs to understand scope and origin  
- Document incident timeline and team actions  
- Update **incident response protocols** and notify stakeholders  

---

### 🔧 Recover

- Restore critical systems and verify data integrity  
- Gradually resume non-essential operations  
- Update **disaster recovery and business continuity plans**  
- Back up updated configurations  
- Conduct **post-incident review** to identify improvements  
- Reinforce team training and playbook updates  

---

## 🧠 Reflections & Notes

- Firewalls must be **proactively configured** to prevent common attacks.  
- Layered defenses and **real-time detection** greatly reduce risk.  
- **Preparedness and fast response** significantly limit downtime.  
- **Continuous improvement** of detection, response, and recovery strategies is key.  
- Strong coordination between **security and IT operations** supports faster recovery.

---

📄 *This report demonstrates the application of real-world incident response strategies using the NIST framework, strengthening both technical knowledge and documentation practice.*

**[View Full Report on Google Docs](https://docs.google.com/document/d/1nxo3iBAMNsniyCoAEQBvQIvvd_1dIdjfdOQrRoPz0io/edit?usp=sharing)**
