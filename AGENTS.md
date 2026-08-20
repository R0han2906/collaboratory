# Collaboratory — Agent Instructions

## For All AI Agents Working on This Project

### First action on every session
1. Read CLAUDE.md completely
2. Run `git status` to see current state
3. Run `git log --oneline -5` to see recent changes
4. Ask what the current task is before doing anything

### How to approach any task
1. INSPECT — Read relevant files first
2. PLAN — Propose what you will change and why
3. CONFIRM — Wait for human approval on the plan
4. IMPLEMENT — Make the smallest safe change
5. VERIFY — Run tests and typecheck
6. REPORT — Show exactly what changed

### Never do these without explicit instruction
- Install packages
- Modify database schema
- Change authentication logic
- Edit environment variable files
- Run destructive commands
- Push to GitHub

### When you are unsure
Stop and ask.
Do not guess and implement.
A wrong implementation is worse than a question.

## Provider Routing
This project uses OmniRoute for AI features.
All LLM calls go through: http://localhost:4000
Default model alias: "fast" → Groq Llama 3.3 70B
Fallback model alias: "local" → Ollama llama3.2

## Running the Project
Frontend: cd frontend && npm run dev
Backend: cd backend && uvicorn main:app --reload
All services: docker-compose up