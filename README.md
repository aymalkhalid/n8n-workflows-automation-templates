# ⚙️ n8n Workflow Automation Templates

Welcome to my repository of **n8n workflow templates** — a curated collection of ready-to-use JSON workflows that automate tasks, connect APIs, and streamline operations.

Whether you're building a basic automation or a complex multi-step process, these templates give you a working starting point you can import and customize in minutes.

---

## ✅ Requirements

- A running **[n8n](https://n8n.io)** instance (self-hosted or cloud).
- Accounts / credentials for the services a workflow uses (e.g. OpenAI, WhatsApp Business Cloud API, Google Calendar, Slack). The needed credentials are listed per category below.

---

## 📂 Repository Structure

Workflows are organized into folders by category or platform so you can quickly find the right automation.

### 💬 WhatsApp Integration
AI-powered WhatsApp assistants built on the WhatsApp Business Cloud API.

| # | Workflow | Description |
|---|----------|-------------|
| 1 | **WhatsApp Incoming Message Setup** | Verifies the Meta webhook and replies to incoming text messages using an OpenAI AI Agent with conversation memory. |
| 2 | **Incoming WhatsApp Router — Text / Voice / Vision** | Routes incoming messages by type and handles **text**, **voice** (audio transcription), and **image** (vision) with OpenAI, then replies on WhatsApp. |
| 3 | **WhatsApp + Google Calendar Integration** | Extends the assistant with **Google Calendar** as an AI Agent tool to read and manage events. |

**Credentials needed:** OpenAI, WhatsApp Business Cloud API (plus Google Calendar for workflow #3).

### 💬 Slack Integration
Event-driven Slack bots built on the Slack Events API.

| # | Workflow | Description |
|---|----------|-------------|
| 1 | **Slack Events — Direct Message & Channel Mention** | Handles the Slack Events **URL verification** handshake and replies to **direct messages** and **channel mentions**. |

**Credentials needed:** Slack API (bot token).

*(More categories coming soon...)*

---

## 🚀 How to Use These Workflows

Importing a workflow into your own n8n instance is quick. Choose either method:

### Method 1 — Copy & Paste (fastest)
1. Open the category folder (e.g. `Whatsapp Integration`).
2. Open the specific `.json` workflow file.
3. Click **Copy raw contents** (the overlapping-squares icon at the top-right of the code box).
4. On your n8n canvas, paste (`Ctrl+V` / `Cmd+V`) — the nodes generate automatically.

### Method 2 — Import from File
1. Download the `.json` file from this repository.
2. Open n8n and click the workflow options menu (the `⋯` icon).
3. Select **Import from File…** and choose the downloaded file.

After importing, open any node that shows a credential warning and connect **your own** credentials.

---

## 🔒 Security & Credentials

All workflows here are **scrubbed of personal API keys, tokens, webhooks, and passwords** — they contain only credential *references*, which you re-point to your own accounts.

A few nodes authenticate with a plain HTTP header instead of a stored credential. In those cases the value is a placeholder you must replace, for example:

```
Authorization: Bearer Replace with Generated Access Token
```

Swap in your own WhatsApp Business Cloud API access token before running the workflow.

> ⚠️ Never commit real tokens back into a workflow file. If a secret is ever exposed, rotate it immediately in the provider's dashboard.

---

## 🤝 Contributing

Contributions are welcome! To add a workflow:

1. Export it from n8n as JSON.
2. Remove any personal data or credentials (keep only credential references).
3. Drop the `.json` into the relevant category folder (or create a new one).
4. Open a pull request describing what the workflow does.

---

## 📝 License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute these workflows for both personal and commercial projects.
