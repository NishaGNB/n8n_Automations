# n8n-google-sheet-automation
Automatically sends a structured email whenever a new row is added to a Google Sheet using Google Gemini to generate professional messages.

**Google Sheet to Email Automation (n8n)**
This automation watches a Google Sheet for new entries and sends a professional, structured email using AI (Google Gemini) and Gmail.

Workflow Summary:

->\*\*Trigger:\*\* Google Sheets (row added)
->\*\*AI Processing:\*\* Google Gemini (Gemini 1.5 Flash model)
->\*\*Email Delivery:\*\* Gmail
->\*\*Use Case:\*\* Order notifications, internal alerts, client updates


How It Works:

1\. \*\*Detect New Row:\*\* The workflow triggers every time a new row is added to a specific Google Sheet.
2\. \*\*Generate Email Content:\*\* The row data is sent to Google Gemini via an HTTP request. Gemini responds with a JSON containing:
&nbsp;  - `EmailSubject`: Short, relevant subject line
&nbsp;  - `EmailBody`: A professional message formatted for email
3\. \*\*Send Email:\*\* The content is parsed and emailed to a predefined recipient using Gmail.


-> "Google sheet automation.json": The exported n8n workflow. Import this into your n8n instance.

Getting Started:
1\. Open your \[n8n editor](https://n8n.io).
2\. Go to `Import` → upload `Google sheet automation.json`.
3\. Set up credentials for:
&nbsp;  - Google Sheets Trigger
&nbsp;  - Gmail
&nbsp;  - Google Gemini (Palm API key)
4\. Turn on the workflow and you're good to go!


Requirements:
->n8n installed (local or cloud)
->Access to Google Sheets and Gmail
->Google Gemini API key (PaLM / Generative Language API)


Example Use Cases:
->Automated order acknowledgment emails
->Instant team alerts from client forms
->Smart summaries of spreadsheet inputs

Notes:
->Your Gemini API key should be kept secure; don’t commit it to version control.
->The workflow is currently set to poll every minute.






