🦈 Wireshark Challenge – Network Packet Analysis

📂 Platform
TryHackMe – Wireshark Room  

---

 📝 Summary
Completed hands-on labs using **Wireshark** to capture and analyze network traffic.  
Practiced identifying suspicious activity in PCAP files, focusing on protocol analysis and attacker behavior.  

---

 🛠️ Tools / Skills Practiced
- Wireshark Filters (`http`, `tcp.stream`, `ip.addr ==`)  
- Following TCP streams  
- Identifying credentials in cleartext traffic  
- Detecting anomalies in network packets  

---

📌 Findings
- Extracted user credentials sent in unencrypted HTTP traffic.  
- Identified unusual DNS requests that could indicate data exfiltration.  
- Observed a complete **TCP 3-way handshake and teardown.  

---

🛡️ Mitigation
- Always use encryption (HTTPS/TLS) to protect credentials.  
- Monitor DNS logs for anomalies.  
- Implement IDS/IPS to detect unusual packet flows.  

---

🔑 Key Learning
- Developed practical skill in reading packets line-by-line.  
- Gained confidence in using filters to speed up investigations.  
- Learned how attackers hide in normal-looking traffic.  
