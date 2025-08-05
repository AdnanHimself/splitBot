# Telegram Task-Splitter Bot

A compact **No-Code/Low-Code project** with n8n that receives Telegram messages via webhook, splits them into subtasks, and sends the results back in chat.

---

## 🚀 Features

- Telegram integration via webhook  
- AI-powered task splitting (OpenRouter Chat Model)  
- No-Code workflow configured in n8n  
- Easy reuse via JSON export  

---

## 🛠 Tech-Stack

- n8n (workflow orchestrator)  
- Docker & Docker Compose  
- ngrok (free HTTPS tunnel)  
- OpenRouter Chat Model  
- Telegram Bot API  

---

## ⏱ Setup & Quickstart

```bash
# 1. Start ngrok tunnel and note the URL  
ngrok http 5678

# 2. Update docker-compose.yml  
#    environment:
#      - N8N_PROTOCOL=https
#      - WEBHOOK_URL=https://<your-ngrok-url>.ngrok-free.app
#      - N8N_EDITOR_BASE_URL=https://<your-ngrok-url>.ngrok-free.app

# 3. Start the container  
docker compose up -d

# 4. Import the workflow  
#    http://localhost:5678 → Import → splitBot_n8n_workflow.json → Active

# 5. Activate the bot in chat  
#    Send /start to your bot  
#    Split: Create project plan
```
---
## Screenshot of the Workflow
![Workflow Canvas](./splitBot_workflow_screenshot.png)
