Smart Logistics Automation System

An automation system designed to replace manual Excel-based logistics workflows with an AI-powered, Telegram-controlled smart agent. Built using n8n, Telegram Bot API, Google Sheets, Gmail API, and optional dashboards. This system enables real-time revenue checks, dispatch updates, client management, and automated email notifications — all from a simple chat interface.

🚀 Overview

This automation replicates a lightweight CRM + operations assistant that works through Telegram. The workflow uses an AI agent to:

Understand natural-language messages

Read and update Google Sheets

Trigger Gmail notifications

Provide instant responses inside Telegram

Maintain context using memory buffering

The system functions like a conversational operations manager, eliminating repetitive Excel tasks and making business monitoring effortless.

🧠 Features

Chat-based Data Retrieval
Ask Telegram:
“Show today’s revenue”
“Give me dispatch details”
“What is the quantity for Client X?”

Google Sheets Automation

Read rows

Append rows

Update existing data

Match clients automatically

Prevent accidental overwrites

AI-Powered Understanding

Interprets user intent

Extracts fields from natural language

Decides which tool to run

Sends confirmations

Automated Gmail Messages

Trigger payment reminders

Send client follow-ups

Custom messages supported

Telegram Bot Interface

Full conversational flow

HTML-safe output

Fast responses

🏗 Architecture
Telegram Message
        ↓
Telegram Trigger (n8n)
        ↓
AI Agent (Google Gemini + Memory)
        ↓
┌───────────────┬────────────────┬────────────────────────────┐
│ Read Google Sheet │ Update Google Sheet │ Send Gmail Message │
└───────────────┴────────────────┴────────────────────────────┘
        ↓
Send Response Back to Telegram


The AI layer uses:

Google Gemini Model

Buffer Window Memory

Workflow tools:

read_google_sheet

update_google_sheet

gmailTool

📂 Project Structure
.
├── README.md
└── workflow/
    └── ai-telegram-google-sheets-agent.json


workflow/ai-telegram-google-sheets-agent.json
→ The exported n8n workflow file (with sensitive credentials removed).

🛠 Tech Stack

n8n – workflow automation engine

Telegram Bot API – bot interface

Google Sheets API – database operations

Google Gemini (PaLM) – AI agent

Gmail API – automated email sending

📸 Workflow Highlights

This workflow includes:

Telegram Trigger Node

AI Agent Node

Memory Buffer Node

Google Sheets Tools

Gmail Tool

Response Formatter

You can import the .json workflow into your own n8n instance to explore the full node map.

🔧 How to Use This Workflow
1. Import into n8n

Open n8n

Go to Workflows → Import from File

Upload:
workflow/ai-telegram-google-sheets-agent.json

2. Add Your Own Credentials

Set credentials for:

Telegram Bot API

Google Sheets OAuth

Gmail OAuth

Google Gemini API

3. Replace Placeholder Values

Inside the JSON:

Add your real Google Sheet ID

Update sheet names

Replace fake email placeholders

4. Start Using

Send commands to your Telegram bot like:

“Update client XYZ amount to 2000”

“Send payment reminder to client ABC”

“Show me all revenue entries for today”

⚠️ Security Notes

All credentials and tokens have been removed.

Always store secrets using environment variables or n8n credentials — never commit them to GitHub.

Avoid uploading real client Excel sheets publicly.

⭐ Why This Project Matters

This workflow demonstrates real-world automation skills:

AI + Automation Integration

Workflow Orchestration

Google Sheets as a lightweight database

Business use-case execution

Real operational impact

Perfect for showcasing automation engineering, no-code/low-code integration, and AI-assisted workflow design.

🤝 Contributions

Feel free to fork, improve, or extend the workflow.
PRs are welcome!
