# SOC-portfolio
My journey to becoming a SOC Analyst – SIEM, log analysis, and threat detection
## 🔎 Investigation Process

1. Monitored Wazuh SIEM dashboard for security alerts  
2. Identified suspicious activity related to privilege escalation and failed SSH logins  
3. Analyzed alert details including rule level, description, and log data  
4. Correlated multiple failed login attempts to detect brute force behavior  
5. Determined whether activity was malicious or expected within the lab environment  

---

## 🧠 Key Learnings

- Learned how to detect brute force attacks using SIEM alerts  
- Understood how privilege escalation activities are logged and monitored  
- Gained hands-on experience analyzing real security events  
- Improved ability to distinguish between normal and suspicious behavior  

---

## 🧭 MITRE ATT&CK Mapping

- **T1110 – Brute Force**
- **T1068 – Privilege Escalation**

---

## 📄 Log Evidence

Example of failed SSH login attempts:
- **Failed password for invalid user scriptkiddo from 127.0.0.1 port 22 ssh2**

These logs indicate repeated authentication failures, which is a strong indicator of brute force activity.

## 🚀 Future Improvements

- Simulate real brute force attacks using tools like Hydra  
- Create custom alert rules in Wazuh  
- Perform deeper log analysis and filtering  
- Expand lab with additional endpoints  
