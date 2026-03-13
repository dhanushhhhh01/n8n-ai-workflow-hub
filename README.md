# 🔁 n8n AI Workflow Hub

> 12 production-ready n8n automation workflows for AI agents, IoT data pipelines, business automation, and monitoring/alerting systems.
>
> [![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io)
> [![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://docker.com)
> [![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com)
> [![InfluxDB](https://img.shields.io/badge/InfluxDB-22ADF6?style=for-the-badge&logo=influxdb&logoColor=white)](https://influxdata.com)
>
> ---
>
> ## 📁 Workflow Categories
>
> ### 🤖 AI Agents (`workflows/ai-agents/`)
> | Workflow | Description |
> |----------|-------------|
> | `email_triage_agent.json` | Classifies emails with GPT-4, sends Slack alerts for urgent items |
> | `document_summarizer.json` | Summarizes PDFs/Docs using Claude API, stores results in Notion |
> | `lead_enrichment_agent.json` | Enriches CRM leads with AI-generated company insights |
>
> ### 📊 Data Pipelines (`workflows/data-pipelines/`)
> | Workflow | Description |
> |----------|-------------|
> | `iot_webhook_to_influxdb.json` | Receives IoT sensor data via webhook, stores in InfluxDB with anomaly detection |
> | `csv_etl_pipeline.json` | ETL pipeline: reads CSV, transforms, loads to PostgreSQL |
> | `api_data_aggregator.json` | Aggregates data from multiple REST APIs into unified dataset |
>
> ### 💼 Business Automation (`workflows/business-automation/`)
> | Workflow | Description |
> |----------|-------------|
> | `invoice_processor.json` | Extracts invoice data via OCR + AI, creates entries in accounting system |
> | `onboarding_automation.json` | Automates new employee onboarding: accounts, Slack, Notion setup |
> | `report_generator.json` | Weekly KPI report: fetches metrics, generates PDF, emails stakeholders |
>
> ### 🚨 Monitoring & Alerts (`workflows/monitoring-alerts/`)
> | Workflow | Description |
> |----------|-------------|
> | `uptime_monitor.json` | Checks service health every 5 min, alerts on Slack/email if down |
> | `github_pr_notifier.json` | Notifies team on new PRs, auto-assigns reviewers |
> | `influxdb_threshold_alert.json` | Monitors InfluxDB metrics, triggers PagerDuty/Slack on threshold breach |
>
> ---
>
> ## 🚀 Quick Start
>
> ```bash
> git clone https://github.com/dhanushhhhh01/n8n-ai-workflow-hub.git
> cd n8n-ai-workflow-hub
> cp .env.example .env
> # Edit .env with your API keys
> docker-compose up -d
> # Access n8n at http://localhost:5678
> ```
>
> Import any workflow: **n8n UI → Workflows → Import from File → select .json**
>
> ---
>
> ## 🏗️ Architecture
>
> ```
> n8n (port 5678)
>     ├── PostgreSQL (workflow metadata)
>     ├── Redis (queue for async workflows)
>     └── Volume mount: ./workflows/
> ```
>
> ---
>
> ## 📬 Author
>
> **Dhanush Ramesh Babu** | [LinkedIn](https://linkedin.com/in/dhanushrameshbabu16) | MSc. Industry 4.0 @ SRH Berlin | 🟢 Open to Werkstudent/Internship
