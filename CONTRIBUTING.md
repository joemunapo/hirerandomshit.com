# Contributing

This repo is managed jointly by **Joe (human)** and the **AI Project Manager**.  
To keep everything consistent, follow these rules:

---

## 📌 Workflow
1. **Tasks** → Always create via `/ops/ISSUE_TEMPLATE_TASK.md`.  
2. **RFCs** → Use `/ops/ISSUE_TEMPLATE_RFC.md` for design decisions.  
3. **PRs** → Must reference an issue and use `/ops/PR_TEMPLATE.md`.  
4. **Evidence** → Store proofs/screenshots in `/evidence/YYYY-MM/`.  
5. **Decisions** → Append to `/logs/decision-log.md` with context + next step.  

---

## 📦 Branching
- `main` = stable  
- `dev` = work in progress  
- Feature branches: `feat/<short-name>`  
- Hotfix branches: `fix/<short-name>`  

---

## ✅ Review
- The **AI Reviewer** (`docs/prompts/reviewer.md`) checks acceptance criteria.  
- Joe or partners may override only with a logged decision.  

---

## 🔐 Guardrails
- Never commit secrets (API keys, .env).  
- Respect token-saving rules from `README.md`.  
- All outputs must be **concise and actionable**.  
