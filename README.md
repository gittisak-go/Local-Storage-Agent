# Local-Storage-Agent (Security-Oriented AI System)

This repository defines an architecture-first Local Storage AI Agent
designed for secure QR / NFC verification workflows.

The system is optimized for:
- Offline-first operations
- Law-enforcement and security use cases
- Strong data governance and auditability
- Supabase as the backend source of truth

No mobile or frontend application code is included at this stage.

---

## 🎯 Project Goals

- Provide an AI agent that operates safely on local storage
- Support QR Code and NFC UID validation workflows
- Enforce blacklist and audit rules strictly
- Reduce backend load while preserving security
- Ensure all sensitive decisions remain server-side

---

## 🧠 AI Governance Model

This project controls AI behavior using explicit context files:

- `docs/SKILL.md`  
  Defines what the AI can and cannot do.

- `mcp/mcp.yaml`  
  Defines system context, domain boundaries, and mindset.

- `prompts/local-agent.system.prompt.md`  
  Defines how the Local-Storage-Agent reasons and responds.

The AI is intentionally constrained to act as an
**advisory intelligence layer only**.

---
```
## 📦 Repository Structure
/
├─ docs/
│ └─ SKILL.md
├─ mcp/
│ └─ mcp.yaml
├─ agent/
│ ├─ memory.schema.md
│ └─ agent.rules.md
├─ supabase/
│ └─ schema.plan.md
├─ prompts/
│ └─ local-agent.system.prompt.md
└─ README.md
```
---

## 🔐 Security Principles

- Supabase backend is always the source of truth
- Row Level Security (RLS) is mandatory on all tables
- Scan logs are append-only and immutable
- National ID data must never be stored in plaintext
- Local storage contains cache and advisory data only

---

## 📍 What This Repo Does NOT Do

- ❌ Does not contain Flutter, web, or mobile UI code
- ❌ Does not perform final authorization decisions
- ❌ Does not bypass backend validation
- ❌ Does not store sensitive personal data locally

---

## 🧭 Intended Usage Flow

1. Local agent provides offline hints and warnings
2. Scan data is submitted to Supabase backend
3. Backend validates against blacklist and policies
4. All scans are logged for audit
5. Alerts and analytics are handled server-side

---

## 🚀 Roadmap (High-Level)

- Phase 1: Architecture, AI context, and governance (current)
- Phase 2: Supabase Edge Functions and alert workflows
- Phase 3: Analytics and dashboards
- Phase 4: Mobile application integration (future)

---

## ⚠️ Disclaimer

This project is intended for controlled environments.
All deployments must comply with applicable laws,
privacy regulations, and organizational policies.

---

## ✅ Status

- Architecture defined
- AI behavior constrained and documented
- Ready for backend and agent implementation

