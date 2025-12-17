---
id: 1
title: Initial Constitution
stage: constitution
date: 2025-12-17
surface: agent
model: claude-sonnet-4-5-20250929
feature: none
branch: book/module-1-ros2
user: Claude
command: /sp.constitution
labels: [constitution, setup, ai-book]
links:
  spec: null
  ticket: null
  adr: null
  pr: null
files:
 - .specify/memory/constitution.md
tests:
 - none
---

## Prompt

/sp.constitution

Project: AI-Native Book with Embedded RAG Chatbot

Overview:
Create a technical book using Docusaurus, authored via Spec-Kit Plus and Claude Code, deployed to GitHub Pages, with an embedded RAG chatbot answering questions strictly from book content.

Core principles:
- Technical accuracy from official documentation
- Spec-driven, reproducible authoring
- Clarity for developers and AI engineers
- No hallucinated or unverifiable content

Standards:
- All claims traceable to authoritative sources
- Runnable, version-pinned code examples
- Clear mapping between architecture and implementation
- MDX-based Docusaurus structure

RAG chatbot constraints:
- Embedded in the book UI
- OpenAI Agents/ChatKit SDKs for orchestration
- FastAPI backend
- Neon Serverless Postgres + Qdrant Cloud (Free Tier)
- Retrieval limited to book content with source citations

Security and deployment:
- No hardcoded secrets
- Environment-variable configuration
- GitHub Pages for frontend
- Reproducible local and production deployment steps

Success criteria:
- Book builds and deploys successfully
- Chatbot answers accurately from indexed content
- End-to-end project reproducible by developers

## Response snapshot

Created the initial project constitution for the AI-Native Book with Embedded RAG Chatbot project. The constitution establishes six core principles:

1. Technical Accuracy and Source Verification - ensuring all content is from official documentation
2. Spec-Driven and Reproducible Authoring - using Spec-Kit Plus and Claude Code
3. Developer Clarity and Accessibility - with runnable, version-pinned examples
4. Secure Development and Deployment Practices - no hardcoded secrets
5. Docusaurus-Based Architecture - following MDX-based structure
6. RAG Chatbot Integration Standards - with OpenAI Agents/ChatKit SDKs

Additional sections cover technology stack requirements, content integrity standards, performance and scalability, development workflow, and governance procedures.

## Outcome

- ✅ Impact: Created initial constitution file with all project principles and guidelines
- 🧪 Tests: none
- 📁 Files: Updated .specify/memory/constitution.md with project-specific constitution
- 🔁 Next prompts: Continue with feature specification and planning
- 🧠 Reflection: Constitution provides clear governance framework for the AI book project

## Evaluation notes (flywheel)

- Failure modes observed: none
- Graders run and results (PASS/FAIL): N/A
- Prompt variant (if applicable): N/A
- Next experiment (smallest change to try): Begin feature specification based on constitution