# 🤖 Personal Assistant — n8n AI Agent Workflow

An automated personal assistant built in **n8n**, powered by a **Google Gemini Chat Model** AI Agent with memory and a suite of connected tools for email, calendar, notes, tasks, and expense tracking.

![Personal Assistant Workflow](https://github.com/MuhammadMudassirRaza12345/personal_assistant/blob/main/w3.png)

---

## 🧩 How It Works

1. A **Webhook** receives an incoming `POST` request (1 item) as the trigger.
2. The request is passed to the **AI Agent**, which is powered by:
   - **Chat Model:** Google Gemini Chat Model
   - **Memory:** Simple Memory (keeps conversation context)
3. Based on the user's request, the AI Agent calls the appropriate **tool** from the categories below.
4. The result is sent back through the **Respond to Webhook** node.

---

## 🛠️ Tools & Capabilities

### 📧 Gmail Tools
- Get single message from a Gmail (`get: message`)
- Get all messages from a Gmail (`getAll: message`)
- Send Message to Gmail (`send: message`)

### 🔍 Google Search
- SerpAPI — general web search

### 📅 Calendar Events
- Create Calendar Event (`create: event`)
- Get Single Calendar Event (`get: event`)
- Get many events in Google Calendar (`getAll: event`)

### 📝 Notes Creation
- Create a Note in Google Docs (`create: document`)
- Update a Note in Google Docs (`update: document`)
- Retrieve a Note from Google Docs (`get: document`)

### ✅ Task Tools
- Create a task in Google Tasks (`create: task`)
- Get a single task in Google Tasks (`get: task`)
- Get all tasks in Google Tasks (`getAll: task`)
- Delete a task in Google Tasks (`delete: task`)
- Update a task in Google Tasks (`update: task`)

### 💰 Expense Tracing
- Calculator — for computing totals/values
- Add Expense in Google Sheets (`append: sheet`)
- Retrieve Expense from Google Sheet (`read: sheet`)

---

## 🚧 Capabilities to Add (Roadmap)

1. Web Search
2. Calendar Add
3. Gmail Access
4. Expenses Tracking
5. Notes Creation
6. Task Creation and Task Deletion

---

## 🏗️ Architecture Summary

| Component | Role |
|---|---|
| Webhook | Entry point that triggers the workflow via POST request |
| AI Agent | Core reasoning engine that decides which tool to call |
| Google Gemini Chat Model | LLM powering the AI Agent |
| Simple Memory | Maintains conversational context |
| Respond to Webhook | Sends the final response back to the caller |

---

*Built with n8n — connecting Gmail, Google Calendar, Google Docs, Google Tasks, Google Sheets, and SerpAPI into one AI-driven personal assistant.*
