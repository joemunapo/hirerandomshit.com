# HireRandomShit – AI Manager Repo

This repo is the **single source of truth** for the AI Project Manager that guides the HireRandomShit.com build.

---

## 📌 TL;DR (for AI CLI)
- **Entry prompt**: `docs/prompts/manager.md`
- **Task schema**: `ai/task_schema.json`
- **Review checklist**: `ai/review_checklist.md`
- **Ground-truth config**: `ai/manager_config.json`
- **Diary for context**: `logs/progress-diary.md` (AI should read only the **last section** by date)
- **Decisions**: `logs/decision-log.md` (AI may read the **last 10 decisions** only)

---

## 🪙 Token-Saving Rules (the AI must obey)
1. Read **filenames first**, not file contents. Only open files specifically referenced in the current TaskSpec.  
2. When reading logs, read the **last dated section only** unless asked otherwise.  
3. Never load images. Assume their captions/filenames in `/evidence/**` are enough.  
4. Prefer existing summaries in `/docs/rfc/**` and `/research/**` before re-summarizing sources.  
5. Output must be **concise** and **actionable**: NMVT + TaskSpec JSON + acceptance criteria + max 3 questions if blocked.  

---

## 🔄 Operating Loop
1. Joe drops new info into `/evidence/YYYY-MM/` and appends a dated note to `logs/progress-diary.md`.  
2. Run AI CLI with `docs/prompts/manager.md` to get: NMVT + TaskSpec.  
3. Create/Update a GitHub Issue using `/ops/ISSUE_TEMPLATE_TASK.md`.  
4. Execute, save proof in `/evidence/**`.  
5. Ask AI to review using `ai/review_checklist.md`. Update `logs/decision-log.md`.  

---

## 📂 Files to Know
- `docs/charter/PROJECT_CHARTER.md` – mission, scope, and success metrics.  
- `docs/rfc/0001-mvp.md` – MVP definition.  
- `docs/prompts/manager.md` – the Manager agent’s system prompt.  
- `ai/task_schema.json` – JSON schema the Manager must emit for each task.  
- `ai/manager_config.json` – project constants/guardrails the Manager must respect.  
- `ai/weekly-cadence.md` – rhythm for planning, work, and review.  

---

## 🚀 Quick Start
1. Add today’s screenshot(s) to `/evidence/2025-08/`.  
2. Add a dated entry to `logs/progress-diary.md`.  
3. Run AI CLI with `docs/prompts/manager.md`.  

