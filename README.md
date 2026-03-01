# 🤖 Hindi AI Relationship Bot (n8n + Ollama)

A fun automation project that uses local AI to generate and send cheesy Hindi relationship lines to Telegram users on an hourly schedule.

## 🚀 Features
- **Local AI:** Uses Ollama (Llama 3) to generate unique Hindi content.
- **Automated Scheduling:** Runs every hour during specific time windows.
- **Multi-User Support:** Sends messages to a list of authorized Telegram Chat IDs.
- **Zero Cost:** Built entirely using free, open-source tools.

## 🛠️ Tech Stack
- **n8n:** Workflow automation.
- **Ollama:** Local LLM hosting.
- **Telegram Bot API:** For message delivery.

## 📦 How to Use
1. **Import Workflow:** Import the `hindi-relationship-bot.json` file into your n8n instance.
2. **Setup Ollama:** Ensure Ollama is running locally with the `llama3` model.
3. **Configure Telegram:** Add your Bot Token and update the Chat IDs in the Code node.
4. **Activate:** Set the workflow to 'Active' and enjoy!

## 📸 Workflow Preview
![Workflow Screenshot]
<img width="1563" height="637" alt="image" src="https://github.com/user-attachments/assets/7e8ae51e-1515-4d4a-b929-bdcde025a7aa" />

