# AI Interview & Scoring System

> An end-to-end AI-powered platform that conducts structured interviews, evaluates candidate responses using machine learning, and generates actionable insights for decision-makers — built for HR screening and academic admissions.

---

## 🎥 Demo

📺 [Watch the full demo on LinkedIn](https://www.linkedin.com/posts/wardahkhan9)

---

## 📌 The Problem

Traditional interview screening is slow, inconsistent, and unscalable. Evaluating hundreds of candidates manually introduces bias, takes weeks, and produces decisions that are hard to justify with data.

This system brings **consistency, scalability, and data-backed decision-making** into interview-based evaluations — and reduces manual screening effort by **~70%**.

---

## ✨ Core Features

### 🎤 Interview System
- Candidate login with a guided, structured interview panel
- Questions across **4 competency areas**
- Supports both **MCQs and open-ended responses** (text or speech)
- **Text-to-Speech** for an interactive interview experience
- Automated AI scoring immediately after submission

### 📊 Analytics Dashboard
- Data-driven insights with visual charts and breakdowns
- Candidate filtering, sorting, and **CSV export**
- Deep-dive into individual responses and scores
- **Downloadable AI-generated reports** per candidate

### ❓ Question Management
- Dynamic add, edit, and delete of interview questions
- Activate or deactivate questions based on interview needs

### 👥 Bulk Candidate Handling
- CSV-based onboarding for mass intake scenarios
- Bulk and selective invite system for large cohorts

---

## ⚙️ System Architecture

```
Candidate → Interview Panel (React) → Django REST API → Scoring Engine → PostgreSQL → Admin Dashboard
                                                              ↓
                                              RoBERTa (1–5 response scoring)
                                              LangChain + Groq (interview flow & report generation)
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React + Tailwind CSS |
| Backend API | Django REST Framework |
| NLP Scoring | Hugging Face RoBERTa (hybrid model) |
| Interview Flow | LangChain + Groq |
| Speech | Text-to-Speech integration |
| Database | PostgreSQL |
| Authentication | JWT-based login |

---

## 📁 Repository Structure

This project is split across two repositories:

| Repo | Description | Link |
|---|---|---|
| `ai-interview-backend` | Django REST API, scoring engine, PostgreSQL models, LangChain integration | [Backend Repo →](https://github.com/Wardahk98/AI-Interview-Chatbot-and-Scoring-System-Backend.git) |
| `ai-interview-frontend` | React dashboard, candidate interview panel, admin analytics UI | [Frontend Repo →](https://github.com/Wardahk98/AI-Interview-Chatbot-and-Scoring-System-Frontend.git) |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- Node.js 16+
- PostgreSQL
- A Groq API key and Hugging Face access token

### Backend Setup

```bash
git clone https://github.com/Wardahk98/AI-Interview-Chatbot-and-Scoring-System-Backend
cd AI-Interview-Chatbot-and-Scoring-System-Backend
python -m venv env
source env/bin/activate        # Windows: .\env\Scripts\activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

### Frontend Setup

```bash
git clone YOUR_FRONTEND_REPO_LINK
cd ai-interview-frontend
npm install
npm start
```

---

## 💡 Key Engineering Challenges

**Bridging model output and usable system decisions** was the hardest part. Getting RoBERTa to score responses on a 1–5 scale is one thing — making those scores integrate cleanly into a backend pipeline, remain interpretable to non-technical reviewers, and surface meaningfully in an admin dashboard required careful system design end to end.

This project reinforced that building impactful AI systems is not just about models. It is about designing end-to-end systems that enable better decisions at scale.

---

## 📄 Documentation

- [Business Requirements Document (BRD)](https://github.com/Wardahk98/AI-Interview-Chatbot-and-Scoring-System-Backend/blob/main/docs/AI_Interview_Scoring_System_BRD.pdf)

---

## 🗺️ Roadmap

- [ ] Voice input via Web Speech API
- [ ] Camera integration with MediaRecorder
- [ ] Admin role-based access control
- [ ] Scoring explainability layer

---

## 👩‍💻 Developed By

**Wardah Khan** — AI Backend Engineer  
[LinkedIn](https://linkedin.com/in/wardahkhan9) · [GitHub](https://github.com/Wardahk98)
