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

## 📦 Repository Structure

