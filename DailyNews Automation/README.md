# 📧 Google Sheets → Email Automation (n8n + Google Gemini)

Automatically send professional, structured emails whenever a new row is added to a Google Sheet — powered by **n8n**, **Google Gemini (1.5 Flash)**, and **Gmail**.

---

## 🚀 Overview
This automation monitors a Google Sheet for new entries and instantly sends a polished, AI-generated email to a chosen recipient.

### **Workflow Summary**
1. **Trigger:** Google Sheets → Detect new row  
2. **AI Processing:** Google Gemini → Generate email subject & body  
3. **Email Delivery:** Gmail → Send professional, structured email  

**Perfect for:**
- Order notifications  
- Client updates  
- Internal alerts  
- Smart summaries of form submissions  

---

## ⚙ How It Works

### **1. Detect New Row**
The workflow is triggered whenever a new row is added to a specific Google Sheet.

### **2. Generate Email Content**
- Row data is sent to Google Gemini (1.5 Flash) via an HTTP request.  
- Gemini returns a JSON response containing:
  - **EmailSubject:** Short, relevant subject line  
  - **EmailBody:** Professional, well-formatted email text  

### **3. Send Email**
The Gemini output is parsed and sent via Gmail to the configured recipient.

---

## 📂 File Included
- **`google-sheet-automation.json`** → The n8n workflow export.  
  *Import this directly into your n8n instance.*

---

## 🛠 Setup Instructions
1. Open your **n8n Editor**.  
2. Go to **Import** → Upload `google-sheet-automation.json`.  
3. Configure credentials for:
   - **Google Sheets Trigger**
   - **Gmail**
   - **Google Gemini** (PaLM / Generative Language API)  
4. **Activate the workflow**.

---

## 📌 Requirements
- n8n (self-hosted or n8n Cloud)  
- Access to **Google Sheets** & **Gmail**  
- **Google Gemini API key** (PaLM / Generative Language API)  

---

## 💡 Example Use Cases
- Automated order acknowledgment emails  
- Instant team alerts from client forms  
- Smart summaries of spreadsheet inputs  

---

## 🔐 Security Notes
- Keep your Gemini API key secure — **never commit it to version control**.  
- The workflow currently polls every **1 minute** by default — adjust as needed.
