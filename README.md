# Telegram Task-Splitter Bot

Ein kleines **No-Code/Low-Code-Projekt** mit n8n, das Telegram-Nachrichten entgegennimmt, in Teilaufgaben zerlegt und direkt zurück in den Chat sendet.

---

## 🚀 Features

- **Telegram-Integration** über Webhook  
- **AI-unterstützte Aufgabenteilung** (via OpenRouter)  
- **No-Code-Workflow** in n8n konfiguriert  
- Leicht importierbarer Workflow (JSON)

---

## 🛠 Tech-Stack

- [n8n](https://n8n.io/) (Workflow-Orchestrator)  
- [Docker Compose](https://docs.docker.com/compose/) (Containerisierung)  
- [ngrok](https://ngrok.com/) (HTTPS-Tunnel für Webhooks)  
- OpenRouter Chat Model (gemäß n8n LangChain-Node)  
- Telegram Bot API

---

## ⏱ Setup & Quickstart

1. **Voraussetzungen**  
   - Docker & Docker Compose  
   - ngrok (frei verfügbar)  
   - Telegram-Bot-Token (von [@BotFather](https://t.me/BotFather))

2. **ngrok-Tunnel starten**  
   ```bash
   ngrok http 5678
Merke dir die HTTPS-URL (z.B. https://abc123.ngrok-free.app).

3. **ngrok-URL in docker-compose.yml eintragen**
environment:
  - N8N_PROTOCOL=https
  - WEBHOOK_URL=https://abc123.ngrok-free.app
  - N8N_EDITOR_BASE_URL=https://abc123.ngrok-free.app

4. Container starten
   ```bash
  docker compose up -d
  Workflow importieren

Öffne http://localhost:5678

„+“ → Import → Datei splitBot_n8n_workflow.json auswählen

Workflow speichern und Active schalten

Bot im Chat aktivieren

/start an deinen Bot senden

Beliebige Nachricht, z.B. Split: Projektplan erstellen
