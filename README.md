# 🛡️ SSH Threat Hunting Dashboard using Splunk

### 🎯 Objective
To detect, analyze, and visualize SSH-based network threats using Splunk and Zeek SSH logs.

---

### 🧰 Tools & Technologies
- **Splunk Enterprise**
- **Zeek (Bro) SSH Logs**
- **SPL Queries**
- **Regex Field Extraction (rex)**

---

### 🧩 Field Extraction
```spl
| rex "^(?<ts>\d+\.\d+)\s+(?<uid>\S+)\s+(?<src_ip>\d{1,3}(?:\.\d{1,3}){3})\s+(?<src_port>\d+)\s+(?<dest_ip>\d{1,3}(?:\.\d{1,3}){3})\s+(?<dest_port>\d+)\s+(?<proto>\S+)\s+(?<direction>\S+)\s+(?<client>\S+)\s+(?<server>\S+)"
