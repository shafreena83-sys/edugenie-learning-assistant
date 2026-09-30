# 📘 EduGenie – Project Documentation

Complete technical and user documentation for **EduGenie**, an AI-powered learning assistant that explains concepts, answers doubts, generates quizzes, and summarizes notes.

---

## 📑 Table of Contents

1. [Introduction](#1-introduction)
2. [System Architecture](#2-system-architecture)
3. [Modules](#3-modules)
4. [Installation & Setup](#4-installation--setup)
5. [Configuration](#5-configuration)
6. [User Guide](#6-user-guide)
7. [API Reference](#7-api-reference)
8. [Database Design](#8-database-design)
9. [Testing](#9-testing)
10. [Troubleshooting](#10-troubleshooting)
11. [Glossary](#11-glossary)

---

## 1. Introduction

### 1.1 Purpose
EduGenie helps students learn faster by giving instant, simple explanations and interactive practice.

### 1.2 Intended Audience
- Students and self-learners (users)
- Developers maintaining or extending the project
- Reviewers / evaluators

### 1.3 Key Features
- Doubt clearing through chat
- Step-by-step concept explanations
- Quiz generation
- Notes summarization
- Progress tracking

---

## 2. System Architecture

```
┌──────────┐     ┌──────────────┐     ┌────────────┐
│ Frontend │ ──▶ │   Backend    │ ──▶ │  AI Model  │
│  (UI)    │ ◀── │  (API layer) │ ◀── │  (API)     │
└──────────┘     └──────┬───────┘     └────────────┘
                        │
                  ┌─────▼─────┐
                  │ Database  │
                  └───────────┘
```

**Flow:** The user sends a request from the UI → the backend validates it and builds a prompt → the AI model returns a response → the backend formats and stores it → the UI displays the result.

---

## 3. Modules

| Module              | Description                                         |
|---------------------|-----------------------------------------------------|
| Chat Module         | Handles user questions and returns explanations     |
| Quiz Module         | Generates multiple-choice questions for a topic     |
| Summarizer Module   | Converts long notes into short summaries            |
| Progress Module     | Stores and displays learning history                |
| Utility / Config    | Input validation, error handling, environment setup |

---

## 4. Installation & Setup

### Prerequisites
- Python 3.9+ *(or Node.js 18+, based on your stack)*
- Git
- AI service API key

### Steps

```bash
git clone https://github.com/<your-username>/edugenie.git
cd edugenie
pip install -r requirements.txt
cp .env.example .env
python src/main.py
```

---

## 5. Configuration

Set these values in the `.env` file:

| Variable        | Description                        | Example              |
|-----------------|------------------------------------|----------------------|
| `API_KEY`       | Key for the AI service             | `sk-xxxx`            |
| `MODEL_NAME`    | Model used for responses           | `your-model-name`    |
| `MAX_TOKENS`    | Maximum length of a response       | `1000`               |
| `DB_PATH`       | Location of the database           | `./data/edugenie.db` |

> ⚠️ Never commit the `.env` file to GitHub.

---

## 6. User Guide

### Asking a Question
1. Open EduGenie.
2. Type your doubt in the chat box (e.g., *"What is photosynthesis?"*).
3. Read the explanation and ask follow-up questions if needed.

### Taking a Quiz
1. Choose **Quiz** from the menu.
2. Enter a topic and select difficulty.
3. Answer the questions and view your score.

### Summarizing Notes
1. Choose **Summarizer**.
2. Paste your notes.
3. Click **Summarize** to get a short version.

### Viewing Progress
Open the **Progress** page to see topics studied and quiz scores.

---

## 7. API Reference

*(Update endpoints to match your implementation.)*

| Method | Endpoint       | Description                  |
|--------|----------------|------------------------------|
| POST   | `/api/ask`     | Ask a question               |
| POST   | `/api/quiz`    | Generate a quiz              |
| POST   | `/api/summary` | Summarize given notes        |
| GET    | `/api/progress`| Get user progress            |

**Example request**

```json
POST /api/ask
{
  "question": "Explain Newton's second law"
}
```

**Example response**

```json
{
  "answer": "Newton's second law states that force equals mass times acceleration...",
  "status": "success"
}
```

---

## 8. Database Design

| Table      | Fields                                              |
|------------|-----------------------------------------------------|
| `users`    | id, name, email, created_at                         |
| `sessions` | id, user_id, question, answer, created_at           |
| `quizzes`  | id, user_id, topic, score, taken_at                 |
| `notes`    | id, user_id, original_text, summary, created_at     |

---

## 9. Testing

Test cases are available in the [`Project_Testing`](../Project_Testing/README.md) folder.

```bash
pytest tests/
```

Areas covered: answer accuracy, quiz generation, input validation, error handling.

---

## 10. Troubleshooting

| Problem                          | Possible Cause                | Solution                                  |
|----------------------------------|-------------------------------|-------------------------------------------|
| No response from assistant       | Invalid or missing API key    | Check `API_KEY` in `.env`                 |
| Slow responses                   | Network or rate limits        | Retry later, reduce `MAX_TOKENS`          |
| Quiz not generated               | Topic too vague               | Use a more specific topic                 |
| App fails to start               | Missing dependencies          | Run `pip install -r requirements.txt`     |

---

## 11. Glossary

| Term      | Meaning                                                     |
|-----------|-------------------------------------------------------------|
| **API**   | Interface that lets two software systems communicate        |
| **Prompt**| The instruction/question sent to the AI model               |
| **MVP**   | Minimum Viable Product – the first usable version           |
| **Token** | A small unit of text processed by the AI model              |

---

## 🔗 Related Documents

- [Main README](../README.md)
- [Project Planning](../_Project_Planning/README.md)
- [Project Testing](../Project_Testing/README.md)

*Last updated: 30 Sep 2026*
