# 🧠 ITSM Agentic AI Support System for Banking

An experimental **Agentic AI-based ITSM (IT Service Management)** support system built for the **banking industry**, using **Dify**, **Supabase**, and **Notion**. Designed to streamline support for common issues like login failures, OTP delays, and account lockouts—powered by LLM reasoning, log parsing, and structured ticketing workflows.

* Full Site in [Notion](https://honeysuckle-thrill-f65.notion.site/ITSM-22c925a5329c80138216e671936d4cfa?source=copy_link) 

---

## ✨ Features

* 🤖 **Agentic AI Workflow** powered by [Dify](https://github.com/langgenius/dify)
* 📚 **Knowledge Base Ingestion** from Notion (error codes, escalation paths, etc.)
* 🧾 **Log Analysis** via Supabase log tracker with JSON log ingestion
* 🌻 **Auto Ticket Creation** via Supabase `ticket_tracker`
* 🧠 **Prompt-chain reasoning** for multi-step logic & human-like decision making
* 🛠️ Open-source and customizable for other ITSM environments

---

## 🧱 Architecture Overview

<img width="1920" height="1080" alt="ITSMWorkflow2 (1)" src="https://github.com/user-attachments/assets/3bf3db39-10a0-4395-9bee-3e99f4fd5204" />


* **Dify**: LLM-based agent framework with memory, tools, and prompt chaining
* **Supabase**: Stores structured ticket and log data
* **Notion**: Source of truth for Knowledge Base content

---

## Actual Architecture in Dify

![ITSM Support](https://github.com/user-attachments/assets/02b809e7-7771-44ac-aab0-7032ccba5f37)

---

## 📚 Knowledge Base (KB)

The KB is built using **Notion tables**, categorized into:

* **Error Code KB** (e.g. A403 = User locked out)
* **Policy KB** (support SLAs, escalation steps)
* **Ticket KB** (how to create and manage tickets)

KB content is chunked and imported into Dify with overlap for optimal LLM access.

---

## 🧠 AI Agent Workflow (Dify)

1. **Classify** the issue (based on user input)
2. **Query Notion KB**
3. **Check Supabase Logs** via customer ID
4. **Interpret Logs** via prompt chaining
5. **Create Ticket** in `ticket_tracker`
6. \*\*Respond with Solution or Ticket ID\`

---

## ⚙️ Setup Instructions

1. Clone the repo & set up Supabase tables
2. Import Notion KB into Dify via web UI
3. Configure Dify tools (Supabase API, prompts)
4. Run your agent via the Dify chatbot
5. Optional: set up Make or n8n for advanced webhook flows

---

## 📊 Use Cases

* Auto-triage login or OTP errors
* Human-like diagnosis based on logs
* 24/7 automated agent for simple ITSM queries
* Escalation routing when issues persist

---

## 🔍 Why Dify?

Dify is purpose-built for **Agentic AI**, with:

* Native support for LLM tools & prompt chaining
* Built-in KB ingestion (Notion, PDFs, websites)
* Visual workflow interface for agents
* Memory management & tool-calling abilities

> Compared to automation tools like `n8n`, Dify is optimized for **reasoning**, not just rule-based flows.

---

## 🚀 Future Enhancements

* Escalation agent after 48 hours
* Customer-facing UI with integrated chat
* Slack/email alert integration
* Scheduled agent to review unresolved logs

---

## 📄 License

MIT License

---

## 🤝 Contributing

Pull requests welcome! If you’ve worked on a similar Agentic AI use case, feel free to fork and share your own flow.

---

## 📬 Contact

Created by \Wong Man ee
Questions? Reach out via GitHub Issues or connect on LinkedIn.
https://www.linkedin.com/in/wmanee/

