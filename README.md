# ai-powered-email-crm-automation
<iframe src="https://player.vimeo.com/video/1061848061?h=88bbaa1617&amp;title=0&amp;byline=0&amp;portrait=0&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="1920" height="1080" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="AI Email CRM Automation Clipchamp"></iframe>
# 📧 AI-Powered Email Categorization & Automation   

This project automates email categorization, summarization, and response management using **n8n, Hugging Face API, and AI models**. It classifies emails into predefined categories, summarizes them, and allows users to **respond directly via Telegram**. The workflow also logs categorized emails into **Google Sheets** for tracking and management.

## 🔥 Features
 **AI-Powered Email Classification** → Categorizes emails into `Work`, `Personal`, `Spam`, `Promotions`, `Meetings`, and `Social` using `Google FLAN-T5-Large`.  
 **Summarization** → Extracts key points from emails for quick reading.  
 **Telegram Integration** → Notifies users in **Telegram** with inline buttons to `Mark as Read` or `Reply`.  
 **Smart Reply Handling** → Users can **reply directly from Telegram**, and the response is emailed back to the sender.  
 **Google Sheets Logging** → Categorized emails, summaries, and replies are saved for reference.  

---

## 🏗️ Workflow Architecture  
The workflow is built with **n8n**, an open-source workflow automation tool, and integrates the following:  

 **Gmail** → Fetches incoming emails.  
 **Hugging Face API** → Hosts the classification API.  
 **Google FLAN-T5** → Used for **Zero-Shot Classification & Summarization**.  
 **Telegram Bot** → Alerts users & manages responses.  
 **Google Sheets** → Logs categorized emails & replies.  

---

## 📜 Workflow Diagram
[🖼 Click here to view the detailed flowchart](./assets/Flowchart.jpg)  

---

## 🔧 Installation & Setup  
To run this project locally, follow these steps:

### **1️⃣ Clone the Repository**
```bash
    git clone https://github.com/your-username/ai-email-crm-automation.git
cd ai-email-crm-automation
```
### **2️⃣ Install and run n8n using Docker**
``` bash
    docker start n8n
```
### **3️⃣ Set Up Environment Variables**
```bash
    GMAIL_CLIENT_ID=your-client-id
    GMAIL_CLIENT_SECRET=your-secret
    TELEGRAM_BOT_TOKEN=your-bot-token
    GOOGLE_SHEETS_ID=your-google-sheets-id
```
### **4️⃣ Deploy Webhook**
Expose  your local n8n instance using ngrok/zrok:
```bash
    ngrok http 5678
```
Then set the Telegram Webhook:
```bash
    curl -X POST
    https://api.telegram.org/bot<YOUR_BOT_TOKEN>/setWebhook?url=<YOUR_NGROK_URL>/webhook/telegram-webhook&allowed_updates=%5B%22message%22,%22callback_query%22%5D
```

---

## 🖥️ Demo & Showcase
[🚀 Watch Demo Video](https://vimeo.com/1061848061/88bbaa1617?ts=0&share=copy)

---

## 📜 License
This project is licensed under the `MIT License`. See the [LICENSE](./LICENSE) file for details.

---

## 🤝 Contributing
Contributions are welcome! Feel free to fork this repo, create a new branch, and submit a Pull Request.

---

## 📬 Contact
📧 Email: [muhammad.hashim40@ee.ceme.edu.pk](muhammad.hashim40@ee.ceme.edu.pk)
