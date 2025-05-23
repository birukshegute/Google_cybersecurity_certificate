# 🛡️ Cybersecurity Incident Report

## 🔐 Brute Force Attack on Web Server

This report was completed as part of a simulated investigation in **Course 3: Connect and Protect – Networks and Network Security**. The objective was to analyze suspicious HTTP traffic patterns, identify the type of attack, and propose an appropriate remediation method. This scenario focuses on brute force password attacks that resulted in unauthorized access and web server compromise.

---

### 📡 Section 1: Network Protocols Involved

| Detail | Protocols Identified |
|--------|----------------------|
| Network protocols observed in the incident | **DNS**, **HTTP**, **TCP** |

---

### 🕵️ Section 2: Incident Summary

| Description |
|------------|
| One likely cause of the website's timeout error is a successful **brute force attack** on the web server. Logs indicate:<br><br>- DNS queries successfully resolved `yummyrecipesforme.com` and `greatrecipesforme.com`<br>- HTTP traffic spiked on port 80 shortly after the resolution<br>- A redirect occurred from `yummyrecipesforme.com` to `greatrecipesforme.com`<br><br>These signs suggest an attacker gained access to the server using a **default admin password**. No brute force protection (e.g., rate limiting or account lockout) was in place, allowing repeated login attempts. Once inside, the attacker modified website files and redirected traffic. |

---

### 🛠️ Section 3: Remediation Strategy

| Recommendation |
|----------------|
| A highly effective control against brute force attacks is the implementation of **account lockout policies**. This security measure locks accounts temporarily after a set number of failed login attempts, thereby limiting the attacker's ability to guess passwords.<br><br>Additional best practices include:<br>- Enforcing strong password policies<br>- Regular password rotation<br>- Using CAPTCHA or MFA (multi-factor authentication)<br>- Monitoring login attempts for anomalies |

---

📄 *This project emphasized hands-on analysis of real-world brute force tactics, the importance of log analysis, and the design of appropriate prevention strategies.*

📄 **[View Full Report on Google Docs](https://docs.google.com/document/d/1-QHW1BsEroDT6_PkMvIrWtTKUu38Rk4JbPxK9ker0FU/edit?usp=sharing)**
