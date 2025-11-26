---

# 💼 AI Voice Agent Challenge | Day 5: Simple FAQ SDR + Lead Capture Agent 

A fully voice-powered **Sales Development Representative (SDR)** built using **LiveKit Agents**, **Murf AI Falcon TTS**, **Deepgram STT**, and **Google Gemini 2.5 Flash**.
This agent answers company FAQs, handles conversations naturally, and captures high-quality sales leads in real time.

---

## 📅 Challenge Progress

| Day      | Status         |
| -------- | -------------- |
| Day 1    | ✅ Completed    |
| Day 2    | ✅ Completed    |
| Day 3    | ✅ Completed    |
| Day 4    | ✅ Completed    |
| Day 5    | ✅ Completed    |
| Day 6–10 | 🔜 Coming soon |

---

# 🎯 Features

## 🧠 SDR Capabilities

* **Automated Company FAQ** → Answers questions about products, pricing, and services
* **Natural Lead Capture** → Collects user information conversationally (no robotic questioning)
* **Smart Question Tracking** → Logs every question asked during the call
* **Professional Call Summary** → Generates a clean summary and stores structured lead data

## 📝 Lead Information Collected

* Full Name
* Company
* Email
* Role / Position
* Use Case
* Team Size
* Sales Timeline (now / soon / later)
* Questions Asked
* Full Conversation Summary

## 🔊 Voice + AI Stack

* **Murf AI Falcon TTS** — Natural human-like voice (Ryan, Conversational style)
* **Deepgram STT** — Real-time speech to text
* **Google Gemini 2.5 Flash** — Conversation logic + function calling
* **LiveKit Agents** — Real-time voice communication framework

---

# 🚀 Quick Start Guide

## ✅ Prerequisites

* Python **3.11+**
* Node.js **18+**
* Murf AI API Key
* Deepgram API Key
* Google Gemini API Key
* LiveKit Server installed

---

# ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/vikasyadav097/AI-Voice-Agent-Challenge-Day-5-Simple-FAQ-SDR-Lead-Capture-Agent-
cd fifth_day_Murf_api/ten-days-of-voice-agents-2025
```

---

# 🖥️ Backend Setup

### 2️⃣ Create Virtual Environment

```bash
cd backend
python -m venv .venv
.venv\Scripts\activate      # Windows
# OR
source .venv/bin/activate   # Mac/Linux
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Create Backend Environment File

Create: `backend/.env.local`

```env
LIVEKIT_URL=ws://localhost:7880
LIVEKIT_API_KEY=devkey
LIVEKIT_API_SECRET=secret
DEEPGRAM_API_KEY=your_deepgram_key
GOOGLE_API_KEY=your_gemini_key
MURF_API_KEY=your_murf_key
```

---

# 🎨 Frontend Setup

### 5️⃣ Install Frontend Dependencies

```bash
cd ../frontend
npm install
```

### 6️⃣ Create Frontend Environment File

Create: `frontend/.env.local`

```env
LIVEKIT_URL=ws://localhost:7880
LIVEKIT_API_KEY=devkey
LIVEKIT_API_SECRET=secret
NEXT_PUBLIC_LIVEKIT_URL=ws://localhost:7880
```

---

# ▶️ Running the Application

### Terminal 1 → Start LiveKit Server

```bash
cd ten-days-of-voice-agents-2025
./livekit-server.exe --dev      # Windows
# or
./livekit-server --dev          # Mac/Linux
```

### Terminal 2 → Start SDR Agent

```bash
cd backend
.venv\Scripts\activate
python src/agent.py dev
```

### Terminal 3 → Start Frontend

```bash
cd frontend
npm run dev
```

### 🌐 Open Browser

Visit → **[http://localhost:3000](http://localhost:3000)**

---

# 💬 Example Conversation

```
SDR: "Hi! Welcome to Razorpay. What brings you here today?"

You: "I'm looking for a payment gateway for my online store."

SDR: "That's great! May I know your name?"

You: "I'm John from TechStore."

SDR: "Nice to meet you, John! What kind of products do you sell?"

You: "Electronics. What are your pricing plans?"

SDR: "Domestic cards cost 2%, UPI is free, and there are no setup fees!"

You: "Sounds good. I'm ready to move forward."

SDR: "Perfect! I've saved all your details and our team will reach out shortly."
```

---

# 📁 Project Structure

```
.
├── backend/
│   ├── src/
│   │   ├── agent.py          # Main SDR agent logic
│   │   └── murf_tts.py       # Murf AI TTS integration
│   ├── .env.local            # Backend environment variables
│   └── pyproject.toml        # Python dependencies
├── frontend/
│   ├── app/                  # Next.js app directory
│   ├── components/           # UI components
│   ├── .env.local            # Frontend env variables
│   └── package.json
├── shared-data/
│   ├── day5_company_faq.json # FAQ data for SDR
│   └── leads.json            # Auto-generated lead storage
├── challenges/
│   └── Day 5 Task.md
└── livekit-server.exe
```

---

# 🔧 Customization

## 🏢 Change Company Info

Modify:

```
shared-data/day5_company_faq.json
```

Update:

* Company name
* Product descriptions
* Pricing
* FAQ

---

## 🎙️ Change Voice Settings

Edit in `backend/src/agent.py`:

```python
tts=murf_tts.TTS(
    voice="en-US-ryan",
    style="Conversational",
    tokenizer=tokenize.basic.SentenceTokenizer(
        min_sentence_len=5,
    ),
)
```

---

## ✏️ Add or Remove Lead Fields

Modify the `lead_data` object inside **agent.py**.

---

# 📊 Viewing Captured Leads

All captured leads are stored automatically in:

```
shared-data/leads.json
```

Each entry includes:

* Timestamp
* All lead fields
* Questions asked
* Conversation summary

---

# 🛠️ Tech Stack

### Backend

* Python 3.11
* LiveKit Agents

### Frontend

* Next.js 15
* React + TypeScript

### Voice

* Murf AI Falcon TTS
* Deepgram STT

### LLM

* Google Gemini 2.5 Flash

---

# 🔑 Required API Keys

1. Murf AI — [https://murf.ai](https://murf.ai)
2. Deepgram — [https://deepgram.com](https://deepgram.com)
3. Google Gemini — [https://ai.google.dev](https://ai.google.dev)

---

# 📚 Learning Resources

* LiveKit Agents → [https://docs.livekit.io/agents](https://docs.livekit.io/agents)
* Murf AI API → [https://murf.ai/api-docs](https://murf.ai/api-docs)
* Deepgram API → [https://developers.deepgram.com](https://developers.deepgram.com)
* Gemini API → [https://ai.google.dev/docs](https://ai.google.dev/docs)

---

# 🤝 Contributing

This is part of a challenge project, but feel free to fork and extend it for your own use cases.

---

# 📄 License

MIT License — see LICENSE file.

---

# 🙏 Acknowledgments

Built for **Murf AI Voice Agent Challenge — Day 5**

* Murf AI
* LiveKit
* Razorpay (example dataset)

---




