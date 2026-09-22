# 🔐 AI-Powered SOAR Pipeline

### Wazuh × n8n × Gemini AI

> **AI-driven Security Orchestration, Automation and Response (SOAR) pipeline for intelligent alert analysis and automated SOC notifications.**

<p align="center">

**Wazuh** → **Python** → **n8n** → **Gemini AI** → **Severity Routing** → **Gmail**

</p>

---

## 📌 Overview

This project integrates **Wazuh, n8n, Python, and Google Gemini AI** to automatically analyze security alerts and assist with SOC triage.

Instead of sending raw alerts to an analyst, the pipeline:

* 🛡️ Detects security events with **Wazuh**
* 🐍 Forwards alerts using **Python**
* 🔄 Automates processing with **n8n**
* 🤖 Analyzes alerts using **Gemini AI**
* 🚨 Classifies severity as **High / Medium / Low**
* 📧 Sends automated Gmail notifications

---

## 🏗️ Architecture

```text
┌─────────────┐
│ Kali Linux  │
│   Testing   │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│    Wazuh    │
│     SIEM    │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│   Python    │
│ Integration │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│     n8n     │
│  Automation │
└──────┬──────┘
       │
       ▼
┌─────────────┐
│  Gemini AI  │
│   Analysis  │
└──────┬──────┘
       │
       ▼
 ┌─────┴─────┐
 │ Severity  │
 └─────┬─────┘
       │
 ┌─────┼─────┐
 ▼     ▼     ▼
HIGH MEDIUM  LOW
 │     │     │
 ▼     ▼     ▼
📧    📧    📧
Gmail Gmail Gmail
```

---

## ⚙️ Workflow

```text
Security Event
      ↓
Wazuh Detection
      ↓
Python Integration
      ↓
n8n Webhook
      ↓
Gemini AI Analysis
      ↓
Severity + Explanation
      ↓
Recommended Action
      ↓
n8n Branching
      ↓
Gmail Notification
```

Gemini provides:

* 🔎 Attack type
* 🚨 Severity
* 📝 Plain-English explanation
* 💡 Recommended response

---

## ✨ Key Features

| Feature             | Description                              |
| ------------------- | ---------------------------------------- |
| 🛡️ Wazuh           | Security event detection                 |
| 🤖 Gemini AI        | Intelligent alert analysis               |
| 🔄 n8n              | Workflow automation                      |
| 🐍 Python           | Alert integration                        |
| 🚨 Severity Routing | High / Medium / Low                      |
| 📧 Gmail            | Automated notifications                  |
| 🧪 Testing          | `curl` + live SSH brute-force validation |

---

## 🧰 Tech Stack

**Security:** Wazuh, Kali Linux
**Automation:** n8n
**AI:** Google Gemini
**Integration:** Python
**Notifications:** Gmail
**Virtualization:** VMware
**Server:** Ubuntu Server

---

## 🧪 Testing

The pipeline was validated using:

### Manual Testing

Custom `curl` payloads were used to test:

```text
🔴 HIGH    → High Severity Email
🟡 MEDIUM  → Medium Severity Email
🟢 LOW     → Low Severity Email
```

### Live Security Testing

An authorized SSH brute-force simulation from Kali Linux generated authentication failures that were detected by Wazuh and processed through the complete AI-powered pipeline.



## 🚀 Future Improvements

* 🎫 Automated incident ticket creation
* 🧠 MITRE ATT&CK mapping
* 🌐 Threat intelligence enrichment
* 🛡️ Automated endpoint response
* 💬 Slack / Teams notifications
* 📊 SOC dashboard integration
* 🔗 Multi-source alert correlation
* 📄 AI-generated incident reports

---

## 🔐 Security

Never commit:

```text
❌ API Keys
❌ Gmail Credentials
❌ Passwords
❌ Private Wazuh Logs
❌ Environment Files
```

Use environment variables or a secure secrets manager for sensitive credentials.

---

## 👨‍💻 Author

**Muhammad Shayan Younas**

**AI-Powered SOAR Pipeline**
*Wazuh + n8n + Gemini AI*

> **Better Detection • Smarter Analysis • Faster Response**

---

### ⚠️ Disclaimer

This project was developed for **educational and authorized cybersecurity lab purposes only**. Security testing should only be performed on systems you own or have explicit permission to test.
