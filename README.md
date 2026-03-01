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

🛠️ Installation & Setup
To get this bot running on your own n8n instance, follow these steps:

Prerequisites

Install n8n (Desktop, Docker, or Cloud).

Install Ollama and run ollama run llama3.

Create a bot via @BotFather on Telegram to get your API Token.

Import the Workflow

Download the hindi-relationship-bot.json file from this repository.

In n8n, create a new workflow and select Import from File (or simply press Ctrl+V on the canvas).

Configure Credentials

Open the Telegram node and create a new credential using your API Token.

Open the Ollama node and ensure the base URL is correct (usually http://localhost:11434).

Personalize Chat IDs

Open the Code Node (labeled "Set IDs" or "User List").

Replace the placeholder values (REPLACE_WITH_YOUR_ID) with your actual Telegram Chat ID.

Tip: Use @userinfobot on Telegram to find your ID.

Activate

Flip the toggle in the top right to Active. Your bot is now live!

💡 How the Logic Works
The workflow follows a linear path:

Trigger: A cron job fires every hour between 9 AM and 9 PM.

Data Prep: A JavaScript snippet creates a list of recipients.

AI Generation: Ollama receives the "Letter of the Day" and generates a unique Hindi sentence.

Delivery: The Telegram node loops through the recipient list and delivers the message.

