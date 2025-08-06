# Autonomous Threat Hunting Agent (MVP)

This project is a prototype for an **Agentic AI** system designed to autonomously detect and respond to cybersecurity threats using log data and LLM-powered reasoning.

## 🚀 Features
- Ingest and analyze firewall, syslog, or cloud logs
- Detect suspicious patterns (e.g., data exfiltration)
- Enrich logs with threat intelligence
- Generate natural language summaries via GPT
- Simulate or recommend remediation actions
- Interactive Streamlit UI for demo or SOC use

## 🧱 Architecture
```
Logs → Parser → Analyzer → Enrichment → LLM Summary → Simulated Response
```

## 🛠️ Tech Stack
- Python
- Streamlit
- OpenAI GPT-4
- Elasticsearch/OpenSearch (optional)
- Ansible (for remediation simulation)

## 📂 Project Structure
- `agent/`: Detection and response logic
- `llm/`: LLM summary generation
- `ui/`: Streamlit dashboard
- `utils/`: IP detection & helpers
- `data/`: Sample logs
- `docs/`: Pitch deck and grant drafts

## ▶️ Run the Streamlit Demo
```bash
pip install -r requirements.txt
streamlit run ui/streamlit_app.py
```

## 📥 Sample Log Format
```json
[
  {
    "timestamp": "2025-08-05T08:00:00Z",
    "source_ip": "192.168.1.45",
    "destination_ip": "203.0.113.23",
    "port": 443,
    "bytes_sent": 2048000,
    "bytes_received": 500,
    "protocol": "HTTPS"
  }
]
```

## 📄 License
MIT License
