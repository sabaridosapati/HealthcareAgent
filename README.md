# 🏥 Healthcare Agentic AI Advisor — n8n

## Overview
A production-ready multi-agent AI system built with n8n 
that intelligently routes healthcare queries to specialist 
agents using Google Gemini LLM, real-time web search via 
SerpAPI, and conversation memory.

## 🏗️ Architecture
```
User Query (Chat)
      ↓
Orchestrator Agent (Google Gemini)
      ↓
Switch Router
      ↓
┌─────────────────────────────────────┐
│  Emergency  │ Symptoms │ Medication │ Appointment │
│  Agent      │ Agent    │ Agent      │ Agent       │
└─────────────────────────────────────┘
      ↓
SerpAPI (Real-time Web Search)
      ↓
Response with Disclaimer
```

## 🛠️ Tech Stack
- **n8n** — workflow orchestration
- **Google Gemini** — LLM for all agents
- **SerpAPI** — real-time web search
- **Simple Memory** — conversation context
- **Chat Trigger** — user interface

## 🤖 Agents
| Agent | Responsibility |
|-------|---------------|
| Orchestrator | Routes query to correct specialist |
| Emergency | Life threatening situations, 911 guidance |
| Symptoms | General health questions, possible conditions |
| Medication | Drug information, interactions, dosages |
| Appointment | Specialist recommendations, scheduling |

## ✨ Features
- Multi-agent orchestration with intelligent routing
- Real-time medical information via SerpAPI
- Conversation memory across sessions
- Medical disclaimer on every response
- Emergency detection and 911 guidance
- HIPAA-aware response formatting

## 🚀 How to Run
1. Install n8n desktop from https://n8n.io
2. Import `workflow/healthcare-agent-workflow.json`
3. Add credentials:
   - Google Gemini API key
   - SerpAPI API key
4. Click Activate
5. Open Chat and start asking!

## 💬 Sample Queries
| Query | Routed To |
|-------|-----------|
| "I have chest pain" | 🚨 Emergency Agent |
| "I have fever and sore throat" | 🏥 Symptoms Agent |
| "Can I take ibuprofen with aspirin?" | 💊 Medication Agent |
| "I need to see a cardiologist" | 📅 Appointment Agent |

## 📸 Workflow Screenshot
![Workflow](screenshots/workflow.png)

## ⚠️ Disclaimer
This AI system provides general health information only.
It is not a substitute for professional medical advice,
diagnosis, or treatment.

## 👨‍💻 Author
Sabari Dosapati
- GitHub: github.com/SabariDosapati
- Role: Generative AI Architect & Agentic AI Engineer
```

---

### Folder Structure:
```
healthcare-agentic-ai-n8n/
├── README.md
├── workflow/
│   └── healthcare-agent-workflow.json
├── docs/
│   └── architecture.md
├── screenshots/
│   └── workflow.png
└── .gitignore
```

---

### .gitignore file:
```
.env
*.env
node_modules/
.n8n/
config/
