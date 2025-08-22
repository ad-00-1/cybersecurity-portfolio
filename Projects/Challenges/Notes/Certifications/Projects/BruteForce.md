🔍 Brute Force Detection in Splunk

 🎯 Objective
Simulate a brute force attack and investigate it using Splunk queries.  
Goal: Detect repeated failed login attempts and understand attacker behavior.

---

🛠️ Tools Used
- **Splunk** → Log indexing & searching  
- **Sysmon** → Windows log collection  
- **Windows Event Viewer** → Source of raw logs  

---

📝 Steps Taken
1. Collected Windows Event Logs with **Sysmon** installed.  
2. Configured Splunk to index logs from the Windows machine.  
3. Ran the following query in Splunk:  


- `4625` = Failed login attempt  
- `4624` = Successful login  

4. Reviewed search results for multiple failed logins in a short time window.  

---

📌 Findings
- Multiple failed logins detected from IP `192.168.56.34`.  
- Targeted user account: **admin**.  
- Pattern indicates a brute force attack attempt.  

---

🛡️ Mitigation
- Implement **account lockout policy** (lock account after 5 failed attempts).  
- Block suspicious IP addresses on the firewall.  
- Enable monitoring alerts in Splunk for EventCode `4625`.  
- Use MFA (Multi-Factor Authentication) for admin accounts.  

---


---

🔑 Key Learning
- Learned how to identify brute force attempts from logs.  
- Understood how attackers try multiple passwords.  
- Practiced writing detection queries in Splunk.
