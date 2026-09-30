# 🗓️ EduGenie – Project Planning

This document outlines the plan for building **EduGenie**, a learning assistant that helps students understand concepts, clear doubts, and practice through quizzes.

---

## 1. Project Summary

| Item            | Details                                                        |
|-----------------|----------------------------------------------------------------|
| **Project**     | EduGenie – Learning Assistant                                  |
| **Goal**        | Give students a simple, interactive way to learn and revise    |
| **Target Users**| School / college students, self-learners                       |
| **Start Date**  | *(add date)*                                                   |
| **Target Release** | *(add date)*                                                |
| **Owner**       | *(your name)*                                                  |

## 2. Problem Statement

Students often struggle to get quick, clear explanations when they are stuck, and traditional resources are static and not personalized. EduGenie solves this by providing an on-demand assistant that explains topics in simple language, tests understanding, and tracks progress.

## 3. Objectives

- Provide accurate, easy-to-understand answers to student questions
- Generate quizzes to reinforce learning
- Summarize notes for quick revision
- Track learning progress over time
- Keep the interface simple and fast to use

## 4. Scope

### ✅ In Scope (MVP)

- Question & answer chat
- Concept explanations with examples
- Quiz generation (multiple choice)
- Notes summarizer

### ❌ Out of Scope (for now)

- Voice input/output
- Mobile app
- Teacher/classroom dashboard
- Payments / subscriptions

## 5. Requirements

### Functional

| ID   | Requirement                                     | Priority |
|------|-------------------------------------------------|----------|
| FR1  | User can ask a question and get an explanation  | High     |
| FR2  | User can generate a quiz on a chosen topic      | High     |
| FR3  | User can paste notes and get a summary          | Medium   |
| FR4  | User can view past sessions and progress        | Medium   |
| FR5  | User can choose difficulty level                | Low      |

### Non-Functional

- **Performance:** responses within a few seconds
- **Usability:** clean UI, usable without training
- **Reliability:** graceful error messages when the AI service is unavailable
- **Security:** API keys stored in environment variables, never committed

## 6. Milestones & Timeline

| Phase | Milestone                        | Duration | Status      |
|-------|----------------------------------|----------|-------------|
| 1     | Requirements & planning          | Week 1   | 🟡 In progress |
| 2     | UI design / wireframes           | Week 2   | ⬜ Not started |
| 3     | Backend + AI integration         | Weeks 3–4| ⬜ Not started |
| 4     | Frontend development             | Weeks 4–5| ⬜ Not started |
| 5     | Quiz & summarizer features       | Week 6   | ⬜ Not started |
| 6     | Testing & bug fixing             | Week 7   | ⬜ Not started |
| 7     | Documentation & release          | Week 8   | ⬜ Not started |

> ✏️ Adjust durations to match your actual schedule.

## 7. Task Breakdown

- [ ] Finalize features and tech stack
- [ ] Create wireframes for chat, quiz, and progress screens
- [ ] Set up repository and folder structure
- [ ] Integrate the AI API
- [ ] Build chat interface
- [ ] Implement quiz generator
- [ ] Implement notes summarizer
- [ ] Add progress tracking
- [ ] Write test cases (see `Project_Testing/`)
- [ ] Prepare final documentation and demo

## 8. Tech Stack (Planned)

| Layer    | Choice                          |
|----------|---------------------------------|
| Frontend | *(e.g., React / HTML-CSS-JS)*   |
| Backend  | *(e.g., Python / Node.js)*      |
| AI / NLP | *(e.g., Claude API)*            |
| Database | *(e.g., SQLite / MongoDB)*      |
| Tools    | Git, GitHub, VS Code            |

## 9. Risks & Mitigation

| Risk                                   | Impact | Mitigation                                       |
|----------------------------------------|--------|--------------------------------------------------|
| AI gives incorrect or unclear answers  | High   | Add prompt guidelines, show sources, allow feedback |
| API cost or rate limits                | Medium | Cache common responses, set usage limits         |
| Scope creep                            | Medium | Stick to MVP scope, move extras to roadmap       |
| Time constraints                       | Medium | Prioritize high-priority features first          |

## 10. Success Criteria

- Users can get a helpful answer to a question in a single step
- Quizzes are generated correctly for the chosen topic
- Test cases in `Project_Testing/` pass
- The project can be set up by following the main README

## 11. Team & Responsibilities

| Name          | Role                | Responsibilities            |
|---------------|---------------------|-----------------------------|
| *(your name)* | Developer / Owner   | Planning, development, testing |
| *(add more)*  |                     |                             |

## 12. Future Enhancements

- Voice-based Q&A
- Personalized study plans
- Mobile app
- Teacher / classroom dashboard
- Multi-language support

---

*Last updated: 30 Sep 2026*
