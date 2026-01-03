# n8n Lead Automation Workflow

This project is an **n8n automation workflow** that captures leads from a form, stores them in Google Sheets, filters them based on budget, sends email notifications, and automatically replies to customers based on the selected service.

---

## 🚀 Features

- 📋 Contact / Quote form submission
- 📊 Automatically saves leads to Google Sheets
- 💰 Filters leads based on minimum budget
- 📧 Sends internal notification email for qualified leads
- 🤖 Sends automated reply emails based on selected service
- ✅ Updates lead status in Google Sheets (Contacted / Rejected)

---

## 🧩 Workflow Overview

### 1. Form Submission
The workflow starts when a user submits the form with the following fields:
- Full Name
- Email
- Budget
- Service (AI Agent, Gen AI, etc.)

---

### 2. Save Lead to Google Sheets
All form submissions are appended as a new row in Google Sheets with:
- Full Name
- Email
- Service
- Budget
- Date

---


are processed further.  
Low-budget leads are ignored automatically.

---

### 4. Internal Email Notification
For qualified leads, an email is sent to the admin containing:
- Name
- Email
- Service
- Budget

---

### 5. Conditional Auto-Reply to Client

Based on the selected service:

- **Gen AI**
  - Sends a Gen AI specific email
- **AI Agent**
  - Sends an AI Agent specific email

Each email includes:
- Personalized greeting
- Short service message
- Calendly booking link

---

### 6. Update Lead Status in Google Sheets
After email is sent:
- `Contacted = TRUE`
- `Rejected = FALSE` (if budget ≥ 1000)

---

## 🛠️ Tech Stack

- **n8n**
- **Google Sheets**
- **Gmail (OAuth2)**
- **Calendly**

---

## 🔐 Required Credentials

Make sure the following credentials are set in n8n:

- Google Sheets OAuth2
- Gmail OAuth2

---

## 📁 Files

- `work.json` → n8n workflow export
- `README.md` → Documentation

---

## ⚙️ Setup Instructions

1. Import `work.json` into n8n
2. Connect Google Sheets & Gmail credentials
3. Update:
   - Email addresses
   - Google Sheet ID
   - Calendly link
4. Activate the workflow

---

## ✅ Result

A fully automated lead management system:
- No manual follow-ups
- Clean lead tracking
- Faster response time

---

## 📌 Notes

- Budget comparison is numeric — ensure dropdown values are handled correctly
- You can easily add more services and email branches

---

## 📞 Support

If you need help customizing or extending this workflow, feel free to reach out.

Happy Automating 🚀


