DailyNews – n8n Workflow

This repository contains an n8n automation that creates and delivers a daily briefing.  
The briefing includes:
- Latest news headlines
- Current weather for Mangalore
- A motivational quote of the day

The update is summarized by AI and sent automatically via email and WhatsApp.

Features
- Scheduled Trigger –>Runs at custom times.
- News Fetching –> Retrieves headlines using the GNews API.
- Weather Update –> Fetches real-time weather from Open-Meteo API.
- Motivational Quote –> Pulls a random quote from ZenQuotes.
- AI Summarization –> Uses Google Gemini (PaLM) API for a concise, friendly briefing.
- Multi-Channel Delivery –> Sends updates via Gmail and WhatsApp (Twilio).

## Workflow Overview
1. Schedule Trigger – Starts the workflow at specified times.
2. Data Fetching – Gets news, weather, and a motivational quote.
3. Merge Node – Combines all fetched data.
4. Code Node – Formats the data into an AI-ready prompt.
5. AI Agent – Generates a clean daily briefing using Google Gemini.
6. Send Email – Delivers the briefing to your inbox.
7. Send WhatsApp Message – Sends the same briefing via Twilio.

 Setup Instructions
1. Clone this repository and import the file into your n8n instance.
2. Configure credentials for:
   - Gmail OAuth2
   - Twilio API
   - Google Gemini (PaLM) API
   - News API (GNews or NewsAPI)
3. Update recipient details in the Gmail and Twilio nodes.
4. Activate the workflow in n8n.

Example Output
Email Subject: 🌤 Your Daily Briefing  
Email/WhatsApp Body: A friendly AI-generated summary with news, weather, and the quote of the day.


License
This project is for educational and internal automation purposes only.  
⚠ Do not commit sensitive credentials or API keys.
