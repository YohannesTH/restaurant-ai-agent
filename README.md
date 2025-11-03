# 🍽️ Restaurant AI Agent (n8n Automation)

<p align="center">
  <img src="https://img.shields.io/badge/n8n-Automation-blue?style=for-the-badge&logo=n8n&logoColor=white" />
  <img src="https://img.shields.io/badge/Google%20Gemini-AI%20Model-4285F4?style=for-the-badge&logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/Telegram%20Bot-Automation-229ED9?style=for-the-badge&logo=telegram&logoColor=white" />
  <img src="https://img.shields.io/badge/Google%20Sheets-Data%20Logging-34A853?style=for-the-badge&logo=googlesheets&logoColor=white" />
  <img src="https://img.shields.io/badge/Google%20Calendar-Booking-4285F4?style=for-the-badge&logo=googlecalendar&logoColor=white" />
</p>

---

## 🧠 Overview

**Restaurant AI Agent** is an end-to-end **AI-powered Telegram assistant** built using **n8n**, **Google Gemini**, and **Google Workspace APIs**.  
It automates restaurant workflows such as:
- Taking food orders (text or voice)
- Booking reservations automatically
- Fetching menu details
- Logging orders to Google Sheets
- Responding to customers through Telegram

This project demonstrates how **AI + automation tools** can streamline restaurant operations efficiently.

---

## ⚙️ Key Features

- 🤖 **AI Assistant (Gemini):** Understands and responds to text and voice inputs.
- 🎙️ **Voice Transcription:** Converts Telegram voice messages into text using Gemini’s audio transcription.
- 📋 **Menu Tool:** Retrieves real-time menu details from a connected document or database.
- 📅 **Calendar Integration:**
  - `Get Events` → Fetches existing bookings.
  - `Create Events` → Adds new reservations automatically.
- 📈 **Order Management:** Logs food orders into Google Sheets.
- 🧩 **Memory:** Keeps short-term memory for contextual responses.

---

## 🧰 Tech Stack

| Component | Purpose |
|------------|----------|
| **n8n** | Automation & workflow orchestration |
| **Google Gemini** | AI chat model and audio transcription |
| **Telegram Bot API** | Chat interface for customers |
| **Google Calendar API** | Reservation management |
| **Google Sheets API** | Order tracking and record-keeping |

---

## 🧱 Workflow Architecture

1. **Telegram Trigger** — Captures incoming user messages.  
2. **Switch Node** — Determines whether the input is text or audio.  
3. **Audio Path:**  
   - Download audio → Transcribe via Gemini → Send to AI Agent  
4. **Text Path:**  
   - Directly sends user text to the AI Agent  
5. **AI Agent Node:**  
   - Uses Google Gemini with connected tools and memory  
6. **Connected Tools:**
   - Menu Tool → Fetches menu  
   - Calendar Get/Create → Handles bookings  
   - Google Sheets → Logs orders  
7. **Telegram Output:** Sends the AI’s response back to the user.

---

## 🖼️ Workflow Diagram

![Workflow Diagram](./workflow.png)

> Example: Visual overview of the n8n setup showing Telegram input, audio transcription, AI processing, and connected Google tools.

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/restaurant-ai-agent-n8n.git
cd restaurant-ai-agent-n8n

### 2️⃣ Import Workflow to n8n

- Go to your **n8n dashboard**.  
- Import the provided `.json` workflow file (included in this repository).

---

### 3️⃣ Set Up Credentials

Configure the following credentials in **n8n**:

- **Telegram Bot Token**  
- **Google Sheets & Calendar** credentials  
- **Gemini API access**

---

### 4️⃣ Start Workflow

Deploy the workflow — your **Telegram bot** is now live and ready to handle messages.
