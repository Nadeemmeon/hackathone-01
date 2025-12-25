---
id: 1
title: Create Constitution
stage: constitution
date: 2025-12-21
surface: agent
model: claude-sonnet-4-5-20250929
feature: none
branch: main
user: user
command: /sp.constitution
labels: [constitution,spec-driven,project-setup]
links:
  spec: null
  ticket: null
  adr: null
  pr: null
files:
 - .specify/memory/constitution.md
tests:
---

## Prompt

```
/sp.constitution

Project: AI/Spec-Driven Book with Embedded RAG Chatbot

Core principles:
- Specification-first development (Spec-Kit Plus)
- Accuracy and retrieval-grounded responses
- Clarity for technical readers
- Reproducibility and modularity

Key standards:
- Book written in Docusaurus using `.md` files only
- Authored via Claude Code + Spec-Kit Plus
- Deployed to GitHub Pages
- Clear separation: book, backend, chatbot

Technology stack:
- FastAPI backend
- OpenAI Agents / ChatKit SDKs
- Qdrant Cloud (Free Tier)
- Neon Serverless Postgres

Chatbot rules:
- Answers strictly from retrieved content
- Supports full-book and selected-text-only Q&A
- No hallucination; respond "answer not available" if context missing

Constraints:
- No hardcoded secrets
- Free-tier limits respected
- Automated, repeatable deployment

Success criteria:
- Book live on GitHub Pages
- Embedded RAG chatbot functional
- Selected-text Q&A enforced
- Full project reproducible from clean repo
```

## Response snapshot

Updated the project constitution file with specific principles and standards for the AI/Spec-Driven Book with Embedded RAG Chatbot project. The constitution now includes six core principles: Specification-First Development, Accuracy and Retrieval-Grounded Responses, Clarity for Technical Readers, Reproducibility and Modularity, Technology Stack Compliance, and Security and Constraint Adherence. It also includes sections on additional constraints, development workflow, and governance.

## Outcome

- ✅ Impact: Created project constitution with 6 core principles and governance structure
- 🧪 Tests: N/A (documentation update)
- 📁 Files: Updated .specify/memory/constitution.md with project-specific principles
- 🔁 Next prompts: Proceed with project planning and specification
- 🧠 Reflection: Constitution provides clear guidelines for the entire project lifecycle

## Evaluation notes (flywheel)

- Failure modes observed: None
- Graders run and results (PASS/FAIL): N/A
- Prompt variant (if applicable): N/A
- Next experiment (smallest change to try): Begin project specification