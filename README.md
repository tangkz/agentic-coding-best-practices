# Agentic Coding Best Practices (Antigravity & Codex)

This repository contains 6 standardized agentic practice templates built on the **Antigravity 3-Layer Architecture** (Directive, Orchestration, Execution).

## 🚀 The 3-Layer Architecture
1. **Layer 1: Directive (`directives/`)** - SOPs, specifications, and project roadmaps in Markdown.
2. **Layer 2: Orchestration (`AGENTS.md`)** - The intelligence/routing layer that interprets directives and manages execution.
3. **Layer 3: Execution (`execution/`)** - Deterministic Python/PowerShell scripts for automated implementation and verification.

---

## 🤖 Platform Compatibility: Antigravity vs. Codex

While these templates are optimized for **Antigravity**, they are fully compatible with **Codex** through a simple mirroring strategy.

### ❓ Will it work for Codex?
**Yes.** Both platforms rely on Markdown-based system instructions, but they look for different filenames in the root or `.agent/` directories.

### 🔧 How to handle cross-platform support?

To ensure your agent personas and instructions work across both tools, we use **Tri-Mirroring**:

1.  **Antigravity:** Primary instructions live in `AGENTS.md`.
2.  **Codex:** Secondary instructions live in `CLAUDE.md`.
3.  **Universal:** We mirror the content across both files (and optionally `GEMINI.md`).

#### Codex Activation Workflow:
If you are using **Codex**, follow these steps:
1.  Initialize your project using one of the templates.
2.  In your terminal, run the execution script:
    ```powershell
    .\execution\mirror_instructions.ps1
    ```
3.  Codex will now pick up the `CLAUDE.md` file and adopt the specific Persona (e.g., SRE, UX Engineer).
4.  As you "Self-Anneal" and update `AGENTS.md`, re-run the script to keep Codex in sync.

---

## 📁 Included Templates
*   **Atomic-Instruction Loop:** High-precision, verified execution.
*   **Vibe Coding:** Creative, design-first UI/UX prototyping.
*   **Spec-Driven Development:** Architectural integrity and API-first logic.
*   **Multi-Agent Orchestration:** Parallel task distribution and coordination.
*   **MCP-Integrated Knowledge:** Data-grounded research and RAG.
*   **DevOps-Deployment:** Infrastructure stability and zero-downtime automation.

---

## 🛠️ Getting Started
1. Pick a template from the `Templates/` directory.
2. Copy its structure (`directives/`, `execution/`, `AGENTS.md`) into your project root.
3. (Codex User) Copy `AGENTS.md` to `CLAUDE.md`.
4. Follow the tailored persona instructions in the agent file.

Be pragmatic. Be reliable. Self-anneal.
