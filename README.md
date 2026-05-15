# AI Support Ticket System

AI-powered customer support ticketing workflow built with n8n, Telegram, Groq AI, and Google Sheets.

## Features

- Receive customer support requests via Telegram
- AI-powered ticket analysis using Groq LLM
- Automatic:
  - Ticket summarization
  - Priority detection
  - Category classification
- Store tickets in Google Sheets
- Detect urgent issues automatically
- Send instant alerts for urgent tickets
- Automatic customer confirmation replies

---
flowchart TD
    A[Telegram Message] --> B[Groq AI Analysis]
    B --> C[Code Parser]
    C --> D[Google Sheets Ticket Storage]
    D --> E{Priority == urgent?}

    E -->|Yes| F[Urgent Alert]
    E -->|No| G[Customer Confirmation]
    
---

## Tech Stack

- n8n
- Telegram Bot API
- Groq API
- Google Sheets API
- JavaScript

---

## AI Capabilities

The AI agent can:

- Summarize customer issues
- Detect urgency level
- Categorize tickets
- Flag tickets that require human review

Example output:

json {   "summary": "Customer cannot log in and needs urgent assistance",   "priority": "urgent",   "category": "login",   "needs_human": true } 

---

## Setup

### 1. Clone Repository

bash git clone https://github.com/YOUR_USERNAME/ai-support-ticket-system.git 

---

### 2. Import Workflow into n8n

Import:

text ai-customer-support-ticketing-clean.json 

---

### 3. Configure Credentials

Add your own credentials:

- Telegram Bot API
- Groq API Key
- Google Sheets OAuth2

---

### 4. Create Google Sheet

Create columns:

text date customer_message summary priority category needs_human 

---

## Security Notes

- Credentials are removed from the shared workflow
- API keys are NOT included
- Sensitive customer information should not be stored
- Human approval is recommended for:
  - Billing
  - Security
  - Legal
  - Account recovery

---

## Future Improvements

- Notion integration
- Email support
- Human approval dashboard
- SLA tracking
- CRM integration
- Sentiment analysis
- Multi-agent workflows

---

## License

MIT License

---

## Author
Amirali Barmar

Built by Amirali Barmar
