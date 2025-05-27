# 🛡️ Security Risk Assessment Report  

## 🏢 Social Media Data Breach Response

This report was created as part of a hands-on activity in **Course 3: Connect and Protect – Networks and Network Security**. In this scenario, you are a security analyst responding to a data breach at a social media organization. The breach exposed sensitive customer information (names, addresses) due to poor internal security practices. The report outlines recommended network hardening methods to prevent similar incidents.

---

### 🔧 Part 1: Selected Network Hardening Methods

| Selected Methods |
|------------------|
| - Multifactor Authentication (MFA)<br>- Firewall Maintenance<br>- Password Policies |

---

### 🧠 Part 2: Justification & Recommendations

#### 🔐 1. Implement Multifactor Authentication (MFA)

The organization currently does not use MFA, which increases the risk of unauthorized account access—especially in environments where passwords are shared or compromised. MFA adds a critical second layer of verification, preventing attackers from accessing systems even if a password is leaked. This is essential for all users, especially those handling sensitive customer data or admin systems.

#### 🔥 2. Establish and Maintain Firewall Rules

It was discovered that no traffic filtering rules are in place for inbound or outbound network traffic. This leaves the network open to potential intrusions and data exfiltration. Implementing and maintaining proper firewall rules will restrict unauthorized IPs and protocols, reduce the overall attack surface, and enhance internal traffic monitoring.

#### 🔑 3. Enforce Strong Password Policies

Security inspection revealed two major concerns:

- Employees are sharing passwords.
- The database still uses a default admin password.

These practices make it easy for attackers to gain privileged access. Immediate action should include:

- Updating all default credentials
- Enforcing complex password requirements
- Educating employees on password hygiene
- Prohibiting credential sharing

Without these changes, the organization remains vulnerable to internal misuse and future breaches.

---

📄 *This report was part of a practical risk mitigation activity that emphasized network hardening through policy, authentication, and access control improvements.*

📄 **[View Full Report on Google Docs](https://docs.google.com/document/d/1G1X-Y0wF0XKPJnL8m4_vwFVZZ1HeeHVjkVrc6sCtsNs/edit?usp=sharing)**
