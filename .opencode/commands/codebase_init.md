---
description: Run tests with coverage
agent: build
model: anthropic/claude-3-5-sonnet
---

Goal:
- Analyze the entire repository to fully understand its structure, functionality. 
- Do NOT modify any files.

Scope:
- Recursively review all directories and files.
- Prioritize GEMINI.md and README.md if present.
- Respect .gitignore and skip non-essential/generated artifacts.

Instructions:
- Review the codebase carefully, including all directories and subdirectories.
- Develop a complete understanding of the project.
- Map the folder & file structure (key paths only).
- Summarize architecture: modules/components and responsibilities.
- List routes/endpoints and their handlers.
- Infer data model/schema from ORM models/migrations/configs.
- Identify dependencies (runtime/dev) and external services.

Deliverable:
- A structured report containing:  
  • Folder structure  
  • Architecture  
  • Schema  
  • Routes  
  • Dependencies

