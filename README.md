# 🧠 Mindwave

**An AI-Powered Mental Health Sentiment Analyzer**
Built with HTML, Tailwind-style CSS & Chart.js — Premium Glassmorphism UI

`Status: Prototype` `UI: Glassmorphism` `Charts: Chart.js` `License: MIT`

---

## 🎬 App Preview

| 🏠 Home | 🧠 Analyzer | 📅 Mood Tracker | 💬 AI Chat |
|---|---|---|---|
| Hero + live check-in | Emotion, risk & confidence | Calendar + trend graphs | Supportive chatbot |

---

## ✨ Key Features

- 🎭 **AI Emotion Detection** — classifies free-text (or voice) check-ins into 9 emotional states: Happy, Sad, Anxious, Angry, Stressed, Depressed, Neutral, Excited, and Calm
- 📊 **Risk & Confidence Scoring** — animated doughnut gauge for mental-health risk score, plus live confidence and stress-level progress bars
- 🎙️ **Voice-to-Text Check-ins** — speak your mood using the Web Speech API, no typing required
- 🤖 **AI-Generated Reflection** — supportive, emotion-specific feedback generated for every check-in, journal entry, and chat message
- 📅 **Mood Tracker** — calendar-based daily mood logging with color-coded days
- 📈 **Trend Graphs** — weekly/monthly wellbeing trend line charts (Chart.js)
- 🌬️ **Breathing Exercise** — animated inhale/exhale guide circle
- 🧘 **Meditation Timer** — 2/5/10-minute guided sessions with countdown
- 📓 **Journal + AI Summary** — free-form journaling with an automatic sentiment summary
- 💬 **AI Chat Assistant** — conversational emotional support with built-in crisis-keyword detection that surfaces helpline resources instantly
- 🆘 **Emergency Help Section** — always-visible crisis support button with hotline numbers (988, Samaritans, Find A Helpline)
- 🕶️ **Anonymous Mode** — privacy toggle for check-ins
- 🏆 **Personal Dashboard** — check-in count, streaks, achievements, mood history
- 📄 **Export & Share** — one-click PDF mood report export (jsPDF)
- 🌗 **Dark / Light Mode** and 🌐 **English / Spanish / Hindi** UI
- 👤 Sign-In / Sign-Up modal, About, Contact, and FAQ sections

> No backend is wired up yet — authentication, mood history, and journal entries currently live in browser session state only. See [Roadmap](#️-roadmap).

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| Frontend | HTML5, Vanilla JavaScript, CSS (custom design tokens) |
| Data Visualization | Chart.js (line trend chart, doughnut risk gauge) |
| PDF Export | jsPDF |
| Voice Input | Web Speech API |
| Fonts | Fraunces (display), Plus Jakarta Sans (body) |
| UI/UX | Glassmorphism, animated gradients, breathing-orb motif, dark/light theming |

---

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/<your-username>/mindwave-ai.git
cd mindwave-ai
```

### 2. Run it ✅
No build step required — it's a single static file.
```bash
# Option A: just open it
open index.html

# Option B: serve it locally
npx serve .
```

### 3. Open Browser
```
http://localhost:3000
```

### 4. App Link
```
https://mindwave-ai-app.netlify.app
```

---

## 📁 Project Structure

```
mindwave-ai/
├── index.html          # entire app — markup, styles, and logic in one file
├── screenshots/         # README preview images
└── README.md
```

---

## 🧠 How the Sentiment Engine Works

- User input (typed or spoken) is lowercased and scanned against a weighted emotion lexicon covering all 9 supported states
- The highest-scoring emotion is selected as the primary label; word-hit count drives a **confidence score**
- **Stress level** and **risk score** are derived from the dominant emotion plus hit density, with a dedicated crisis-keyword check that immediately surfaces emergency resources
- Each result is paired with a hand-written, emotion-specific **AI reflection** message rather than a generic response
- The same engine powers the Analyzer, Journal summary, and Chat Assistant, so feedback stays consistent across the app

---

## 🏆 Why This Project Stands Out

- 🎨 **Premium, calming UI** — teal/lavender/mint gradients, glassmorphism cards, and a breathing-orb motif tying the hero and self-care sections together
- 🧩 **All-in-one wellness toolkit** — emotion analysis, mood tracking, breathing/meditation tools, journaling, and a support chatbot in a single interface
- 🩹 **Safety-conscious by design** — crisis-keyword detection, always-visible helpline access, and clear "not a diagnosis" messaging throughout
- 📱 **Fully responsive** — works cleanly across desktop, tablet, and mobile
- ⚡ **Zero external API keys required** to run the current prototype — everything runs client-side

---

## 🗺️ Roadmap

- [ ] Replace the lexicon-based engine with a fine-tuned transformer (BERT/RoBERTa/DistilBERT) served via a FastAPI backend
- [ ] Add a real backend (FastAPI + MongoDB or Firebase) for persistent auth, mood history, and journal storage
- [ ] Wire up JWT-based authentication and encrypted user data storage
- [ ] Swap the static quote/insight bank for real AI-generated, personalized feedback (OpenAI / Hugging Face Inference API)
- [ ] Add burnout prediction from historical mood data
- [ ] Email reminders for daily mood check-ins
- [ ] Admin analytics dashboard (aggregate-only, no private content access)

---

## ⚠️ Known Limitations

- Emotion detection is a **keyword-weighted heuristic**, not a trained ML model — it's a UX prototype of the intended AI feature, not a clinical or diagnostic tool
- Mood history, journal entries, streaks, and login state reset on page refresh (no backend persistence yet)
- Multilingual support currently covers UI labels only, not full sentiment analysis in other languages
- This app does not diagnose, treat, or replace professional mental health care — crisis resources are provided for genuine emergencies

---

*Made with 🧠 for anyone learning to check in with themselves.*
