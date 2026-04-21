
# AI Email Orchestrator (n8n)

## Overview

This workflow is an AI-powered email automation system built using n8n. It processes incoming Gmail messages, understands their intent using an LLM (Grok / LLaMA 3.3 70B), and decides whether to respond, summarize, or request human approval.

The system reduces manual email handling by combining intelligent classification, automated drafting, and human-in-the-loop validation.

---

## 🚀 Features

* 📩 Automatic Gmail trigger for incoming emails
* 🧠 AI-based email understanding and intent detection
* 📅 Smart scheduling detection with Google Calendar integration
* ✍️ AI-generated email replies
* ✅ Human approval workflow via Slack
* 🔔 Slack notifications for summaries and approvals
* 🔄 End-to-end automation with decision branching

---

## ⚙️ How It Works

1. **Email Trigger**

   * A new email is received via Gmail trigger

2. **AI Processing**

   * The email content is analyzed using an LLM (Grok / LLaMA 3.3 70B)
   * The system determines intent:

     * Requires reply
     * Informational only
     * Scheduling-related

3. **Decision Logic**

   * If scheduling is detected:

     * Checks availability in Google Calendar
   * If no reply is needed:

     * Sends a summarized message to Slack
   * If a reply is required:

     * Generates a draft response using AI

4. **Human Approval Loop**

   * Draft is sent to Slack for approval
   * Upon approval:

     * Email is sent automatically
     * Status is updated in Slack

---

## 🧩 Tech Stack

* n8n (workflow automation)
* Gmail API
* Slack API (webhooks)
* Google Calendar API
* LLM (Grok / LLaMA 3.3 70B)

---

## 📸 Workflow Preview

*Add screenshot here (workflow canvas)*

---

## 🛠️ Setup Instructions

1. Import the `workflow.json` into n8n
2. Configure the following credentials:

   * Gmail account
   * Slack webhook / API
   * Google Calendar
3. Replace placeholders:

   * Webhook URLs
   * API keys
4. Activate the workflow

---

## 🔐 Security Notes

* Credentials are not included in this repository
* Replace all API keys and tokens with your own
* Avoid hardcoding sensitive data inside nodes

---

## 💡 Use Cases

* Founder / solo operator inbox automation
* Customer support triage
* Lead qualification and response
* Meeting scheduling automation

---

## 📌 Future Improvements

* Multi-language support
* Priority scoring for emails
* CRM integration (HubSpot, Salesforce)
* Auto-follow-ups

---

## 📄 License

MIT License
