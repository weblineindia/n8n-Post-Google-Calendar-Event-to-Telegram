# 📅 Post New Google Calendar Events to Telegram 

## 📝 Overview  

This **n8n workflow automatically sends a Telegram message** whenever a **new event** is added to **Google Calendar**. It extracts key event details, including:  

✅ **Event Name**  
✅ **Description**  
✅ **Event Creator**  
✅ **Start & End Date**  
✅ **Location**  

The event details are **forwarded to a specified Telegram chat**, ensuring you stay updated on newly scheduled events directly from Telegram.  

---

## ✅ Prerequisites  

Before setting up the workflow, ensure you have:  

1️⃣ **Google Account with Google Calendar Access**  
   - The **Google Calendar API** must be enabled.  
   - Use **OAuth2 authentication** for Google Calendar.  

2️⃣ **Telegram Bot**  
   - Create a bot using **BotFather** on Telegram.  
   - Retrieve the **Bot Token**.  

3️⃣ **Telegram Chat ID**  
   - Get the **Chat ID** (personal chat or group).  

---

## 🔄 Workflow Steps  

### **Step 1: Google Calendar Trigger Node (Event Created Event)**  
📌 **Action**: Detects new events in Google Calendar.  

- Click on **"Add Node"** and search for **"Google Calendar"**.  
- Select **"Google Calendar Trigger"** and add it.  
- Authenticate using your **Google OAuth2 credentials**.  
- Set **Trigger Type** to **"Event Created"**.  
- Choose the **specific calendar** to monitor.  
- Click **"Execute Node"** to test the connection.  
- Click **"Save"**.  

---

### **Step 2: Telegram Node (Send Message Action)**  
📌 **Action**: Sends the event details to Telegram.  

- Click on **"Add Node"** and search for **"Telegram"**.  
- Select **"Send Message"** as the action.  
- Authenticate using your **Telegram Bot Token**.  
- Set the **Chat ID** (personal or group chat).  
- Format the message using details from the **Google Calendar Trigger**:  
  ```plaintext
  📅 New Event Scheduled!  
  📝 **Event:** {{Event Name}}  
  📍 **Location:** {{Location}}  
  🕒 **Starts:** {{Start Date}}  
  ⏳ **Ends:** {{End Date}}  
  👤 **Organizer:** {{Event Creator}}  
  📝 **Details:** {{Description}}  
  ```  
- Click **"Execute Node"** to test.  
- Click **"Save"**.  

---

### **Step 3: Connect & Test the Workflow**  
✅ **Attach both nodes**:  
   - **Google Calendar Trigger** → **Telegram Send Message**  

✅ **Run the workflow manually**.  
✅ **Create a test event in Google Calendar**.  
✅ **Check Telegram for the notification**.  

---

## 📌 Outcome  

Once set up, this workflow will:  
✅ **Automatically notify you in Telegram** when a new event is created.  
✅ **Send structured event details**, ensuring you're always updated.  
✅ **Improve scheduling visibility and reduce manual follow-ups**.  

---

## 🚀 About WeblineIndia  

This workflow is built by the **AI development team at WeblineIndia**.  

📌 **Who are we?**  
✔ **25+ years** of software development experience.  
✔ **3,500+ successful projects** delivered across **25+ countries**.  
✔ Expertise in **no-code automation, AI systems, and enterprise solutions**.  

📩 **Need a custom workflow?** Hire our AI developers to build **tailored automation solutions** for your business!  
