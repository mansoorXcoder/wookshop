# 🤖 AI Build 2026 — Hackathon Playbook

> **Project:** Domain-Specific RAG Chatbot — Offline AI with Ollama  
> **Author:** Pathan Mansoor Alikhan  
> **Goal:** Build a local AI chatbot that answers questions from uploaded documents using **Llama 3.1, RAG, FAISS, LangChain, FastAPI, and Streamlit**.

---

## 📌 Table of Contents

- [🎯 Project Goal](#-project-goal)
- [🧰 Tech Stack](#-tech-stack)
- [🏗️ System Architecture](#️-system-architecture)
- [⏱️ Day 1 — Build Plan](#️-day-1--build-plan)
- [🚀 Day 2 — Finalization & Judging](#-day-2--finalization--judging)
- [🎤 Presentation Plan](#-presentation-plan)
- [❓ Questions Judges May Ask](#-questions-judges-may-ask)
- [🔌 API Flow](#-api-flow)
- [🗂️ Storage Design](#️-storage-design)
- [📁 Folder Structure](#-folder-structure)
- [🧠 Prompt Templates](#-prompt-templates)
- [🔀 GitHub Milestones](#-github-milestones)
- [✨ Future Enhancements](#-future-enhancements)
- [⚠️ Risk Management](#️-risk-management)
- [🧪 Testing Checklist](#-testing-checklist)
- [📝 README Checklist](#-readme-checklist)
- [🎬 Demo Script](#-demo-script)
- [🚢 Deployment Plan](#-deployment-plan)
- [📊 Success Metrics](#-success-metrics)
- [👥 Team Communication](#-team-communication)
- [✅ Final Checklist](#-final-checklist)
- [🏆 Golden Rule](#-golden-rule)
- [🥇 Winning Formula](#-winning-formula)

---

## 🎯 Project Goal

Build a **Domain-Specific RAG Chatbot** that can:

- 📄 Accept uploaded PDF documents
- 🔎 Retrieve relevant information from those documents
- 🧠 Generate answers using a local **Llama 3.1** model
- 🔒 Run locally without depending on a cloud LLM API
- ⚡ Provide fast document search through **FAISS**
- 💬 Offer a simple chat experience through **Streamlit**

### Core idea

```text
User
  │
  ▼
Upload Documents
  │
  ▼
Document Processing
  │
  ▼
Chunking + Embeddings
  │
  ▼
FAISS Vector Search
  │
  ▼
Relevant Context
  │
  ▼
Ollama + Llama 3.1
  │
  ▼
Grounded Answer
```

---

## 🧰 Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| 🎨 Frontend | Streamlit | Chat and document-upload interface |
| ⚡ Backend | FastAPI | API layer and application services |
| 🧠 LLM | Ollama + Llama 3.1 | Local answer generation |
| 🔗 AI Framework | LangChain | RAG orchestration |
| 🗃️ Vector Database | FAISS | Similarity search over embeddings |
| 🐍 Language | Python | Application development |
| 🌱 Version Control | Git + GitHub | Collaboration and source control |
| 💻 IDE | VS Code | Development environment |

---

## 🏗️ System Architecture

```text
                         ┌─────────────────┐
                         │      User       │
                         └────────┬────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │ Streamlit UI    │
                         └────────┬────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │ FastAPI Backend │
                         └────────┬────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │ LangChain RAG   │
                         │    Pipeline     │
                         └───────┬─┬───────┘
                                 │ │
                    ┌────────────┘ └────────────┐
                    ▼                           ▼
             ┌─────────────┐             ┌─────────────┐
             │    FAISS    │             │   Ollama    │
             │ Vector DB   │             │  Llama 3.1  │
             └──────┬──────┘             └──────┬──────┘
                    │                           │
                    └───────────┬───────────────┘
                                ▼
                       ┌─────────────────┐
                       │  Final Answer   │
                       └─────────────────┘
```

---

# ⏱️ Day 1 — Build Plan

## 🕒 3:00 PM – 4:00 PM — Registration & Setup

### Checklist

- [ ] Registration
- [ ] Meet teammates
- [ ] Set up laptops
- [ ] Check internet
- [ ] Create WhatsApp group
- [ ] Decide team leader

**Output:** Team is ready to start.

---

## 🕓 4:00 PM – 4:45 PM — Problem Statement Briefing

### What to capture

- What is the problem?
- Who are the target users?
- What needs to be submitted?
- What are the judging criteria?
- What is the time limit?

### Checklist

- [ ] Listen carefully
- [ ] Write important keywords
- [ ] Capture constraints
- [ ] Create one-page notes

**Output:** Clear problem understanding and one-page notes.

---

## 🕔 4:45 PM – 5:15 PM — Brainstorming

### Decision Framework

```text
Problem
   ↓
Possible Solution
   ↓
Is AI Needed?
   ↓
Can We Build It in 18 Hours?
   ↓
       YES
        ↓
   Select Idea
```

### Selected Project

**Domain-Specific RAG Chatbot**

### MVP Features

- 📄 PDF upload
- 💬 Question answering
- 🤖 AI-generated answers
- 🏠 Local LLM execution
- 🔎 Fast semantic search

**Output:** Project finalized.

---

## 🕠 5:15 PM – 6:00 PM — Architecture

Finalize:

- Frontend flow
- Backend APIs
- Document ingestion
- Chunking
- Embeddings
- FAISS retrieval
- Ollama integration
- Answer generation

**Output:** Architecture ready.

---

## 🕕 6:00 PM – 7:00 PM — Task Distribution

| Member | Responsibility |
|---|---|
| Member 1 | Backend |
| Member 2 | Frontend |
| Member 3 | RAG Pipeline |
| Member 4 | Testing |
| Member 5 | Presentation |

**Output:** Everyone starts coding with a clear owner.

---

## 🌙 7:00 PM – Midnight — Development Sprint

### Build Priority

```text
1. Backend
   ↓
2. PDF Upload
   ↓
3. Embeddings
   ↓
4. FAISS
   ↓
5. Ollama
   ↓
6. Chat Interface
   ↓
7. Testing
   ↓
8. GitHub Push
```

### Git Workflow

```bash
git init
# Create GitHub repository
git add .
git commit -m "Initial setup"
git push
# Repeat after meaningful milestones
```

**Target:** Working MVP before the end of the first day.

---

# 🚀 Day 2 — Finalization & Judging

## 🌅 Morning — Complete Remaining Features

### Checklist

- [ ] Fix bugs
- [ ] Improve UI
- [ ] Improve prompt
- [ ] Improve answer quality
- [ ] Run full tests

---

## 🕚 11:00 AM — Submission

### Submission Checklist

- [ ] GitHub repository updated
- [ ] README completed
- [ ] Screenshots added
- [ ] Demo tested
- [ ] Final submission completed

---

## 🕛 12:00 PM – 3:00 PM — Judging

### Explain the project in this order

```text
Problem
   ↓
Existing Solutions / Limitations
   ↓
Our Solution
   ↓
Architecture
   ↓
AI Technologies
   ↓
Live Demo
   ↓
Future Scope
```

---

## 🕒 3:00 PM – 5:00 PM — Final Presentation

| Slide | Content |
|---|---|
| 1 | Problem |
| 2 | Solution |
| 3 | Architecture |
| 4 | Live Demo |
| 5 | Impact |
| 6 | Future Scope |

---

# 🎤 Presentation Plan

Keep the presentation **simple, visual, and demo-focused**.

### Recommended flow

1. Introduce the team
2. Explain the problem
3. Show why existing approaches are insufficient
4. Introduce the solution
5. Explain the architecture
6. Run the live demo
7. Explain the AI technologies
8. Show impact / value
9. Explain future scope
10. Thank the judges

> **Tip:** Spend less time reading slides and more time demonstrating the working product.

---

# ❓ Questions Judges May Ask

Prepare concise answers for:

### Product & Problem

- Why this idea?
- Why does this problem matter?
- Who are the users?
- What makes the solution unique?
- Why is AI useful here?

### Technical

- Why Ollama?
- Why local AI?
- Why RAG?
- How does FAISS work?
- What is LangChain?
- How does document retrieval work?
- What datasets or documents are used?
- How scalable is the architecture?

### Engineering

- What happens if the PDF cannot be parsed?
- How do you handle hallucinations?
- What are the security considerations?
- What is the expected response time?
- What is the cost?
- What are the main technical limitations?

### Roadmap

- What would you improve next?
- Can it support multiple users?
- Can it support other LLMs?
- Can it be deployed to the cloud?
- What is the future roadmap?

---

# 🔌 API Flow

```text
User
 │
 ▼
Frontend
(Streamlit / React)
 │
 │ HTTP Request
 ▼
FastAPI Backend
 │
 ├── POST /upload
 ├── POST /chat
 ├── GET  /history
 └── GET  /health
 │
 ▼
LangChain
 │
 ▼
FAISS Vector DB
 │
 │ Relevant Chunks
 ▼
Ollama + Llama 3.1
 │
 │ Generated Answer
 ▼
FastAPI Backend
 │
 ▼
Frontend
```

## API Endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| `POST` | `/upload` | Upload and process documents |
| `POST` | `/chat` | Ask a question |
| `GET` | `/history` | Retrieve chat history |
| `GET` | `/health` | Check service health |

---

# 🗂️ Storage Design

```text
project/
├── documents/       # Uploaded PDF files
├── embeddings/      # FAISS index / vector data
├── history/         # Chat history
├── logs/            # Application logs
├── config/          # Configuration
└── temp/            # Temporary uploads
```

### Optional Database

- SQLite
- MongoDB

### Suggested Collections / Tables

| Entity | Purpose |
|---|---|
| Users | User accounts / identity |
| Documents | Uploaded document metadata |
| Chats | Conversation history |
| Logs | Application and error logs |

---

# 📁 Folder Structure

```text
project/
│
├── backend/
│   ├── app.py
│   ├── routes/
│   ├── services/
│   └── models/
│
├── frontend/
│   └── streamlit_app.py
│
├── rag/
│   ├── loader.py
│   ├── splitter.py
│   ├── embeddings.py
│   └── retriever.py
│
├── llm/
│   └── ollama.py
│
├── database/
│   └── faiss/
│
├── documents/
├── static/
├── templates/
├── tests/
│
├── README.md
├── requirements.txt
├── Dockerfile
└── .gitignore
```

---

# 🧠 Prompt Templates

## System Prompt

```text
You are an AI assistant.

Answer only using the uploaded documents.
If the information is unavailable in the documents, say:
"I don't know."

Keep answers concise, accurate, and grounded in the provided context.
```

## User Prompt

```text
Answer the following question using the uploaded documents.

Question:
{user_question}
```

## RAG Prompt

```text
Context:
{retrieved_chunks}

Question:
{question}

Answer:
```

### RAG Principle

> **Retrieve first → provide context → generate a grounded answer.**

---

# 🔀 GitHub Milestones

| Milestone | Deliverable |
|---|---|
| 1 | Repository created |
| 2 | Backend ready |
| 3 | Frontend ready |
| 4 | RAG working |
| 5 | Testing complete |
| 6 | Final submission ready |

### Commit Strategy

```text
Initial Setup
     ↓
Backend
     ↓
Frontend
     ↓
RAG
     ↓
Testing
     ↓
README
     ↓
Final Submission
```

> Push frequently. Do not wait until the final hour to upload everything.

---

# ✨ Future Enhancements

### AI & UX

- Voice input
- Voice output
- OCR support
- Image understanding
- Multiple LLM support
- Multi-language support
- AI agent workflows

### Platform

- Authentication
- Multi-user support
- Cloud deployment
- Mobile app
- Analytics dashboard
- Admin panel
- Feedback system

### Integrations

- Email integration
- Slack integration
- Microsoft Teams integration

---

# ⚠️ Risk Management

| Risk | Backup / Mitigation |
|---|---|
| Ollama not running | Verify local model before demo |
| Model loads slowly | Pre-load model before presentation |
| FAISS index failure | Keep a backup index |
| PDF parsing issues | Test multiple PDFs |
| Internet unavailable | Keep the entire stack local |
| Git merge conflicts | Commit and merge frequently |
| Laptop battery issues | Keep chargers / power backup ready |

### Backup Plan

- [ ] Keep one local project backup
- [ ] Push to GitHub regularly
- [ ] Save FAISS index frequently
- [ ] Keep offline documentation
- [ ] Run a final demo test before submission

---

# 🧪 Testing Checklist

## Backend

- [ ] Upload API
- [ ] Chat API
- [ ] Error handling
- [ ] Response time
- [ ] Health check

## Frontend

- [ ] Upload button
- [ ] Chat window
- [ ] Loading state / animation
- [ ] Error messages
- [ ] Empty-state handling

## AI / RAG

- [ ] Correct answers
- [ ] Hallucination checks
- [ ] Empty query handling
- [ ] Invalid PDF handling
- [ ] Irrelevant-question handling

## Performance

- [ ] Large PDF
- [ ] Multiple questions
- [ ] Memory usage
- [ ] Retrieval speed
- [ ] Model response time

---

# 📝 README Checklist

The final project README should contain:

- [ ] Project name
- [ ] Overview
- [ ] Problem statement
- [ ] Solution
- [ ] Features
- [ ] Architecture
- [ ] Tech stack
- [ ] Installation instructions
- [ ] Usage instructions
- [ ] Screenshots
- [ ] Future scope
- [ ] Team members
- [ ] License

---

# 🎬 Demo Script

### 1. Introduce the Team
Briefly introduce each member and their role.

### 2. Explain the Problem
Describe the real-world problem in one or two sentences.

### 3. Explain Existing Challenges
Show why traditional search or existing solutions are insufficient.

### 4. Present Our Solution
Introduce the Domain-Specific RAG Chatbot.

### 5. Explain the Architecture
Show the data flow from document upload to generated answer.

### 6. Run the Live Demo
Demonstrate:

```text
Upload PDF
   ↓
Ask Question
   ↓
Retrieve Relevant Content
   ↓
Generate Answer
   ↓
Show Response
```

### 7. Explain AI Technologies
Briefly explain RAG, FAISS, LangChain, Ollama, and Llama 3.1.

### 8. Show Impact
Explain how the solution saves time and makes document knowledge easier to access.

### 9. Explain Future Scope
Mention the strongest 2–4 next improvements.

### 10. Thank the Judges

---

# 🚢 Deployment Plan

```text
Development
    ↓
Local Testing
    ↓
Bug Fixes
    ↓
Final Testing
    ↓
GitHub Push
    ↓
Submission
    ↓
Presentation
```

---

# 📊 Success Metrics

Track the metrics that matter most to the judges and users:

| Metric | What to Measure |
|---|---|
| ⚡ Response Time | Time to retrieve and generate an answer |
| 🎯 Accuracy | Correctness of answers |
| 😊 User Experience | Ease and clarity of the interface |
| 🧠 AI Quality | Relevance and groundedness |
| 💡 Innovation | Uniqueness of the approach |
| 📈 Scalability | Ability to handle more documents/users |
| 🛡️ Reliability | Stability during repeated use |

---

# 👥 Team Communication

## Before Coding

- [ ] Finalize idea
- [ ] Assign tasks
- [ ] Define MVP
- [ ] Agree on Git workflow

## During Coding

- [ ] Share progress regularly
- [ ] Push code frequently
- [ ] Report blockers immediately
- [ ] Avoid duplicating work
- [ ] Keep interfaces between modules clear

## Before Submission

- [ ] Merge all branches
- [ ] Test the complete application
- [ ] Verify README
- [ ] Prepare presentation
- [ ] Verify GitHub repository
- [ ] Run the final demo end-to-end

---

# ✅ Final Checklist

## Product

- [ ] Problem clearly defined
- [ ] Unique solution
- [ ] Working MVP
- [ ] Clean UI
- [ ] Stable backend
- [ ] AI working
- [ ] RAG working

## Submission

- [ ] GitHub repository
- [ ] README
- [ ] Working demo
- [ ] Architecture diagram
- [ ] Screenshots
- [ ] Test cases
- [ ] Submission completed before deadline
- [ ] Backup copy available

## Team

- [ ] Team roles assigned
- [ ] Everyone knows their speaking role
- [ ] Everyone understands the architecture
- [ ] Everyone can explain the project

## Confidence

- [ ] Can explain the problem clearly
- [ ] Can explain why AI is needed
- [ ] Can explain why RAG is used
- [ ] Can explain the architecture
- [ ] Can demonstrate the product confidently

---

# 🏆 Golden Rule

```text
Think Less
    ↓
Plan Fast
    ↓
Build MVP
    ↓
Test
    ↓
Improve
    ↓
Present Clearly
```

# 🥇 Winning Formula

```text
Problem
   +
Working Demo
   +
Simple UI
   +
Clear Story
   +
Confidence
   =
Higher Chance of Winning 🚀
```

---

## 💡 Final Hackathon Mindset

> **Do not try to build everything. Build the smallest version that clearly solves the problem, make it reliable, and demonstrate it confidently.**

### Priority order

**Working product > fancy features**

**Reliable demo > complex architecture**

**Clear explanation > too many slides**

**Tested MVP > unfinished perfection**

---

**Good luck with AI Build 2026! 🚀🤖**

> **Build fast. Test hard. Demo confidently.**
