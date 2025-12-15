# 📰 DailyNews – n8n Workflow

An automated daily briefing powered by **n8n**, combining the latest news headlines, real-time weather for Mangalore, and an inspiring quote — all summarized by AI and delivered via Email and WhatsApp.

---

## ✨ Features

- 📅 **Scheduled Trigger** – Runs automatically at your preferred times.
- 🗞 **Latest News** – Retrieves top headlines via GNews API.
- 🌤 **Weather Update** – Real-time Mangalore weather from Open-Meteo API.
- 💬 **Motivational Quote** – Random daily quote from ZenQuotes.
- 🤖 **AI Summarization** – Generates a friendly, concise briefing using Google Gemini (PaLM API).
- 📩 **Multi-Channel Delivery** – Sends updates via Gmail and WhatsApp (Twilio).

---

## 🔄 Workflow Overview

1. **Schedule Trigger** → Starts the workflow at set times.
2. **Data Fetching** → Collects news, weather, and quote data.
3. **Merge Node** → Combines all fetched data into a single set.
4. **Code Node** → Formats the data into a prompt for the AI.
5. **AI Agent** → Google Gemini creates a clean, engaging briefing.
6. **Send Email** → Gmail sends the briefing to your inbox.
7. **Send WhatsApp Message** → Twilio sends the same briefing via WhatsApp.

---

## 📂 Included File

- `daily-news-automation.json` → The n8n workflow export (ready to import).

---

## 🛠 Setup Instructions

1. Clone this repository or download the `.json` workflow file.
2. Open your **n8n Editor**.
3. Import → Upload `daily-news-automation.json`.
4. Configure credentials for:
   - Gmail OAuth2
   - Twilio API (for WhatsApp)
   - Google Gemini (PaLM / Generative Language API)
   - GNews API (or NewsAPI alternative)
5. Update recipient details in the Gmail and Twilio nodes.
6. Activate the workflow.

---

## 📧 Example Output

Good morning! Here’s your AI-powered daily briefing:

🗞 News: [Top headlines here]  
🌤 Weather: 28°C, sunny with light winds.  
💬 Quote: "The only way to do great work is to love what you do." – Steve Jobs

Have a great day ahead!

---

## ⚠ Security Notes

- Never commit API keys or credentials to version.
- This workflow is intended for educational and internal automation purposes only.

