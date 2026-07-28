# AI-Lead-Intelligence-System
Automatically enriches incoming B2B leads with company data, qualifies them using AI, stores structured lead information, and instantly notifies the sales team.


---

# Business Problem

Sales teams often receive incomplete or unqualified leads from websites, landing pages, and contact forms.

Before contacting a customer, managers must manually:

- identify the company;
- verify that it exists;
- collect company information;
- evaluate customer intent;
- estimate lead quality;
- save the lead into CRM;
- notify the sales team.

These repetitive tasks slow down response time and reduce sales efficiency.

---

# 👥 Target Users

- Sales teams
- B2B companies
- CRM administrators
- Business owners


# Solution Overview

This workflow automatically processes every incoming lead.

It enriches company information using DaData, validates business data, checks the internal company repository, creates new company records when necessary, prepares structured context for AI analysis, qualifies the lead using an LLM, stores the analyzed lead in Google Sheets, and immediately notifies the sales team via Telegram.

---

# Workflow Architecture

*(Workflow architecture screenshot)*

---

# Workflow

```text
Receive Lead (Webhook)
        ↓
Normalize Input
        ↓
Validate Contact
        ↓
Enrich Company (DaData)
        ↓
Normalize Company Data
        ↓
Check Company Status
        ↓
Check Required Company Data
        ↓
Find Existing Company
        ↓
Company Exists?
      ↙             ↘
Yes               No
 │                  ↓
 │        Create Company Record
 └──────────────┬───────────────
                ↓
Prepare Lead Context
        ↓
LLM Lead Analysis
        ↓
Create Lead Record
        ↓
Notify Sales Manager
```

---

# Demo

## Incoming Lead

```text
Name:
Ivan Petrov

Company:
ООО СтройТех

Message:
"We want to implement a CRM system and automate lead processing."
```

↓

## AI Qualification

```text
Need:
CRM implementation and workflow automation

Priority:
High

Score:
9/10

Summary:
Potential customer interested in CRM implementation.

Reason:
The customer clearly described a business need and requested automation services.
```

↓

## Output

- Company enriched using DaData
- Company automatically added to repository (if not found)
- Lead qualified by AI
- Lead stored in Google Sheets
- Sales manager notified in Telegram

---

# Features

- Automatic lead intake via Webhook
- Company enrichment with DaData API
- Contact validation
- Company validation
- Automatic company repository
- AI-powered lead qualification
- Structured AI output (JSON Schema)
- Google Sheets integration
- Telegram notifications
- Fully automated workflow

---

# Tech Stack

- n8n
- OpenAI GPT-4.1 Mini
- DaData API
- Google Sheets
- Telegram Bot API
- Webhooks

---

# Key Skills Demonstrated

- AI Workflow Design
- Business Process Automation
- AI Lead Qualification
- API Integration
- Data Enrichment
- Structured AI Outputs
- JSON Schema
- Google Sheets Automation
- Repository Pattern
- Business Rule Validation
- Workflow Architecture
- Sales Process Automation

---

# Repository Structure

```text
README.md
architecture.png
workflow.png
telegram-demo.png
google-sheets-demo.png
```

---

# Future Improvements

- CRM integration (HubSpot, Bitrix24, Salesforce)
- Duplicate lead detection
- Automatic email follow-up
- AI-generated sales responses
- Lead scoring analytics
- Multi-channel lead intake (Email, Telegram, Website)
- Dashboard for sales managers
