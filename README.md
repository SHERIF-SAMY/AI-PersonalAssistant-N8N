#  AI Personal Booking & Automation Assistant

An AI-powered personal assistant built with **n8n**, combining **LLM agents**, **Retrieval-Augmented Generation (RAG)**, and workflow automation to manage client conversations, schedule meetings, and automate business operations.

The assistant acts as a professional representative, answering client questions using a knowledge base, collecting meeting details, checking calendar availability, scheduling appointments, and sending confirmation emails—all through Telegram.

---
<img width="1191" height="964" alt="Sherif_Agent_Assest" src="https://github.com/user-attachments/assets/daa59fda-0f52-452e-bcd9-cfe239fa8f19" />


## Features

-  AI-powered conversational assistant
-  Retrieval-Augmented Generation (RAG) using Supabase Vector Store
-  Hugging Face Embeddings for semantic search
-  Telegram Bot interface
-  Google Calendar availability checking
-  Automatic client information extraction
-  Google Sheets CRM logging
-  Gmail confirmation emails
-  Conversation memory for multi-turn interactions
-  Fully automated workflow using n8n

---

##  Architecture

```
Telegram User
      │
      ▼
Telegram Trigger
      │
      ▼
AI Agent (OpenRouter LLM)
      │
      ├──────────────► Memory Buffer
      │
      ├──────────────► Supabase Vector Store (RAG)
      │                     │
      │                     ▼
      │          Hugging Face Embeddings
      │
      ├──────────────► Google Calendar
      │
      ├──────────────► Google Sheets
      │
      ├──────────────► Gmail
      │
      ▼
Telegram Response
```

---

##  Tech Stack

| Category | Technology |
|----------|------------|
| Workflow Automation | n8n |
| LLM | OpenRouter |
| Vector Database | Supabase Vector |
| Embeddings | Hugging Face (`all-MiniLM-L6-v2`) |
| RAG | LangChain + Supabase |
| Messaging | Telegram Bot |
| Calendar | Google Calendar API |
| Database | Google Sheets |
| Email | Gmail API |

---

##  Workflow Overview

The assistant follows this pipeline:

1. Receive client messages from Telegram.
2. Process the request using an AI Agent.
3. Retrieve relevant information from a RAG knowledge base containing:
   - CV
   - Skills
   - Experience
   - Projects
4. Answer client questions accurately using vector search.
5. Detect hiring intent.
6. Collect required meeting information:
   - Client Name
   - Email
   - Phone Number
   - Meeting Subject
   - Preferred Date
   - Start Time
   - End Time
   - Additional Notes
7. Store client information in Google Sheets.
8. Check availability in Google Calendar.
9. Schedule the meeting.
10. Send a professional confirmation email.
11. Reply to the client through Telegram.

---

##  AI Capabilities

The assistant can:

- Answer questions about professional experience
- Explain technical projects
- Handle client inquiries
- Collect structured business information
- Book appointments automatically
- Send confirmation emails
- Maintain conversational context using memory
- Reduce hallucinations through Retrieval-Augmented Generation (RAG)

---

##  Knowledge Base

The assistant uses a **Supabase Vector Store** containing documents such as:

- Resume / CV
- Skills
- Previous projects
- Technical experience
- Professional background

Instead of relying only on the LLM, responses are grounded using semantic retrieval to improve accuracy.

---

##  Automation Flow

- Telegram → AI Agent
- AI Agent → RAG Retrieval
- AI Agent → Calendar Availability
- AI Agent → Google Sheets Logging
- AI Agent → Gmail Confirmation
- AI Agent → Telegram Reply

Everything is orchestrated automatically inside **n8n**.

---

##  Key Highlights

- AI Agent with tool calling
- End-to-end business workflow automation
- RAG-powered knowledge retrieval
- Automatic meeting scheduling
- CRM logging using Google Sheets
- Email automation
- Multi-turn conversational memory
- Modular and scalable architecture

---

##  Future Improvements

- Voice assistant support
- WhatsApp integration
- Multi-language conversations
- OAuth authentication
- Stripe payment integration
- CRM integrations (HubSpot, Salesforce)
- Dashboard for analytics
- Multi-user support

---

##  Workflow Preview

> Add screenshots of your n8n workflow here.

```
images/workflow.png
```

---

##  Author

**Sherif Samy**

AI Engineer | Machine Learning | NLP | LLMs | Workflow Automation

- GitHub: https://github.com/SHERIF-SAMY
- LinkedIn: https://www.linkedin.com/in/sherif-samy
