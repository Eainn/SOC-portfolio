# 🛡️ Wazuh Alert Investigation: Privilege Escalation & SSH Brute Force

## 📌 Lab Setup
- Wazuh Manager (Ubuntu Server)
- Wazuh Agent (Ubuntu Server)
- VMware Workstation Lab

---
## 🔍  **Scenario 1: Privilege Escalation Detection**

**Alert:** Successful sudo to ROOT executed  

**Description:**  
A user executed a sudo command to gain root privileges and accessed a sensitive file.

**Analysis:**  
The command used:
`/usr/bin/cat wazuh-install-files/wazuh-passwords.txt`

This indicates access to sensitive credential data. The alert was triggered due to privilege escalation.

**Conclusion:**  
This activity was expected during lab setup but could indicate suspicious behavior in a production environment.

---

## 🔍 Scenario 2: SSH Brute Force Attack Simulation

**Attack Method:**
Simulated multiple failed SSH login attempts using a non-existent user.

**Command used:**
ssh scriptkiddo@localhost

**Detection:**
Wazuh generated alerts including:
- Failed login attempts  
- Invalid user access  
- Multiple authentication failures  

**Analysis:**  
Repeated login failures within a short time frame indicate brute force behavior (MITRE ATT&CK T1110).

**Conclusion:**  
This behavior is consistent with brute force attacks attempting unauthorized access.

---

## 🚨 Severity
- Medium to High (Level 5–10)
  
**Why this is suspicious:**
- Multiple failed login attempts in a short time
- Invalid username used
- Repeated authentication failures

**Potential Risk:**
If successful, attacker could gain unauthorized access to the system.

---

## 🛠️ Skills Demonstrated
- SIEM monitoring (Wazuh)  
- Log analysis  
- Threat detection  
- Incident investigation  
- Attack simulation

## 🧑‍💻 SOC Analyst Response

If this occurred in a real environment:

- Investigate source IP address
- Block IP after multiple failed attempts
- Check for successful login attempts after failures
- Enforce stronger authentication (e.g., disable password login, use SSH keys)
- Monitor system for further suspicious activity

---

## 📸 Screenshots
![Alerts](alert_overview.png)
![Alert Detail](alert-detail.png)
![Bruteforce](FailedLogin_Bruteforce.png)
![Bruteforce Detail](LoginFailed_Detail.png)
