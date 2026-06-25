# wazuh-ai
# 🛡️ AI-Powered SOC Assistant for Wazuh

> **Real-Time AI-Based Security Alert Analysis for Wazuh SIEM**

---

## 📌 Project Overview

Security Information and Event Management (SIEM) platforms generate thousands of security alerts every day. While Wazuh efficiently detects these events, security analysts still need to manually analyze alerts to understand their severity, identify potential threats, and determine appropriate remediation actions.

This project integrates an **AI-powered Security Operations Center (SOC) Assistant** with **Wazuh SIEM** to automate the initial investigation process.

The AI assistant continuously monitors Wazuh alerts, classifies threats, maps them to the **MITRE ATT&CK Framework**, assigns risk levels and priorities, generates executive summaries, and recommends remediation actions.

The objective is to reduce manual effort, improve alert triage, and accelerate incident response within Security Operations Centers (SOC).

---

# 🚀 Key Features

* ✅ Real-Time Wazuh Alert Monitoring
* ✅ Windows Endpoint Monitoring
* ✅ AI-Based Threat Classification
* ✅ MITRE ATT&CK Technique Mapping
* ✅ Incident Priority Assignment (P1–P4)
* ✅ Risk Assessment (Low, Medium, High, Critical)
* ✅ Executive Summary Generation
* ✅ Automated Security Recommendations
* ✅ AI Confidence Score
* ✅ Continuous Alert Monitoring
* ✅ Modular Python Architecture
* ✅ Docker-Based Wazuh Deployment

---

# 🏗️ System Architecture

```text
Windows Endpoint
        │
        ▼
+----------------------+
|   Wazuh Agent        |
+----------------------+
        │
        ▼
+----------------------+
|   Wazuh Manager      |
| (Docker Container)   |
+----------------------+
        │
        ▼
alerts.json
        │
        ▼
+----------------------+
|   AI Monitor         |
+----------------------+
        │
        ▼
+----------------------+
|   AI Analyzer        |
+----------------------+
        │
        ├── Threat Classification
        ├── Risk Assessment
        ├── MITRE ATT&CK Mapping
        ├── Executive Summary
        ├── Recommendations
        └── Confidence Score
        │
        ▼
SOC Analyst
```

---

# 🔄 Project Workflow

1. Windows generates a security event.
2. Wazuh Agent collects the event.
3. Wazuh Manager processes the event.
4. Alert is stored in `alerts.json`.
5. `ai_monitor.py` continuously watches for new alerts.
6. New alerts are passed to `ai_analyzer.py`.
7. AI analyzes the alert and generates:

   * Threat Category
   * Risk Level
   * MITRE ATT&CK Mapping
   * Priority
   * Executive Summary
   * Recommended Actions
8. Results are displayed to the SOC analyst.

---

# 💻 Technology Stack

| Category             | Technology      |
| -------------------- | --------------- |
| Operating System     | Kali Linux      |
| Endpoint             | Windows 11      |
| SIEM                 | Wazuh 4.12      |
| Containerization     | Docker          |
| Programming Language | Python 3.13     |
| Data Format          | JSON            |
| Dashboard            | Wazuh Dashboard |
| Framework            | MITRE ATT&CK    |

---

# 📂 Project Structure

```text
AI_Wazuh_Lab/
│
├── ai_monitor.py
├── ai_analyzer.py
├── config.py
├── requirements.txt
├── .env
│
├── reports/
│   ├── incident_report.txt
│   └── history.json
│
├── screenshots/
│
└── README.md
```

---

# ⚙️ Installation Summary

1. Install Docker on Kali Linux.
2. Deploy Wazuh 4.12 using Docker Compose.
3. Access the Wazuh Dashboard.
4. Install the Wazuh Agent on Windows.
5. Authenticate the Windows Agent with the Wazuh Manager.
6. Verify the agent connection in the Wazuh Dashboard.
7. Create the Python virtual environment.
8. Install required Python packages.
9. Configure the AI monitoring scripts.
10. Run the AI monitor.

---

# 🧪 Testing Performed

The following scenarios were tested successfully:

* Windows Successful Logon
* Failed Login Attempt
* Local Logon Events
* Continuous Real-Time Monitoring
* AI Threat Classification
* MITRE ATT&CK Mapping
* Recommendation Generation

---

# 📊 Sample AI Output

```
AI SECURITY ANALYSIS

Agent               : Balaganesh

Threat Category     : Authentication

Risk Level          : LOW

Priority            : P4

MITRE Technique     : T1078

Executive Summary

Successful Windows authentication detected.

Recommendations

1. Review logs
2. Verify activity
3. Continue monitoring

AI Confidence Score : 88%
```

---

# ⚠️ Challenges Faced

* Wazuh Docker version mismatch
* SSL certificate generation
* Windows Agent installation and authentication
* Docker container networking
* Accessing alerts inside Docker
* Python syntax and JSON parsing issues
* OpenAI API authentication and quota limitations
* Continuous monitoring stability

---

# 🔮 Future Enhancements

* GPT-5 / Local LLM Integration
* VirusTotal Integration
* AbuseIPDB Integration
* Email Notifications
* Slack / Microsoft Teams Integration
* AI Dashboard
* Historical Threat Analytics
* Automatic Incident Report Generation
* Machine Learning-Based Anomaly Detection

---

# 📈 Project Outcomes

* Successfully deployed Wazuh SIEM.
* Connected Windows endpoint to Wazuh.
* Built a real-time AI monitoring application.
* Automated threat classification and prioritization.
* Reduced manual effort in SOC alert analysis.
* Established a scalable architecture for future AI enhancements.

---

# 👨‍💻 Author

**Bala Ganesh Golla**

**Project:** AI-Powered SOC Assistant for Wazuh SIEM

**Year:** 2026
