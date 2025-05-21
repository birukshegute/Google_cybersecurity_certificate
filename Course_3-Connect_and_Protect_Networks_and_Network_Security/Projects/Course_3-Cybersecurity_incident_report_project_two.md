# 🛡️ Cybersecurity Incident Report  
## 🌐 SYN Flood Attack Investigation

This report documents a simulated cybersecurity scenario presented in **Course 3: Connect and Protect – Networks and Network Security**. The task involved analyzing abnormal TCP traffic patterns resulting in a network outage and identifying the likely cause. The project focuses on understanding how a SYN flood attack disrupts the TCP handshake process and impacts server performance.

---

### 🔍 Section 1: Identify the Type of Attack

| Description | Analysis |
|------------|----------|
| **Issue** | The website is receiving an excessive number of SYN requests and is unable to complete TCP handshakes, leading to timeouts for legitimate users. |
| **Evidence from Logs** | - Spike in incoming SYN packets<br>- Few or no corresponding ACK responses<br>- Large number of incomplete handshakes<br>- Server resource exhaustion and connection failures |
| **Type of Attack** | **Denial-of-Service (DoS)** – more specifically, a **SYN Flood Attack**, which overwhelms the server with half-open TCP connections. |

---

### 📉 Section 2: How the Attack Causes Website Failure

| Detail | Explanation |
|-------|-------------|
| **TCP Handshake Process** | 1. **SYN** – Client initiates a connection with a SYN request<br>2. **SYN-ACK** – Server responds to acknowledge<br>3. **ACK** – Client finalizes the handshake |
| **Attack Behavior** | The attacker sends many SYN requests without completing the handshake (never sends the final ACK). The server allocates resources and waits, keeping connections half-open. |
| **Impact** | - Server reaches connection limit<br>- Cannot respond to legitimate traffic<br>- Website becomes unavailable |
| **What the Logs Show** | - Unusual surge in SYN packets<br>- Absence of corresponding ACKs<br>- High backlog of half-open connections<br>- Repeated timeout errors for real users |

---

### ✅ Recommended Next Steps

- 🔒 Implement **rate limiting** to restrict excessive SYN requests per source IP  
- 🧠 Enable **SYN cookies** to protect against resource exhaustion  
- 🌐 Deploy a **Web Application Firewall (WAF)** or **DDoS mitigation service**  
- 🔍 Monitor traffic patterns and **block suspicious IP addresses**

---

📄 **[View Full Report on Google Docs](https://docs.google.com/document/d/14tc2pEy0CsoBpWABmDlveVUEOJjGsqHHV6nZt666GsQ/edit?usp=drive_link)**