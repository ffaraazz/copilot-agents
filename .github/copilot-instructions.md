## Repository Copilot Instructions

This repository defines a modular, MCP-first multi-agent workflow.

### Global Priorities

1. Orchestrator-first execution: start with `ProjectOrchestrator` for every new session.
2. Deterministic behavior: inspect repository state first, verify assumptions, ask when uncertain.
3. MCP-first documentation: prefer official MCP documentation and code samples over model memory.
4. Contract-first delivery: when frontend and backend both change, freeze a shared contract before implementation.
5. Shared memory discipline: update shared session files after each major milestone.
6. Minimal duplication: keep agent-specific files small and delegate reusable behavior to `.github/skills` and `.github/rules`.

### Reusable Modules

- Rules: `.github/rules/*.md`
- Skills: `.github/skills/*.md`
- Shared context templates: `.github/context/*.md`

### Source Of Truth Order

1. Developer-confirmed requirements
2. Frozen shared contract (if cross-team)
3. Repository code and configuration
4. Shared session memory files
5. Official MCP documentation

### Hard Safety Rules

- Never invent files, APIs, frameworks, configs, or architecture.
- Never continue with low-confidence assumptions without explicit developer confirmation.
- Never bypass lifecycle stages defined in `.github/rules/development-cycle.md`.
- Never duplicate large policy blocks inside agent files; reference the reusable modules instead.

<!-- mermaid-ai-skills:start -->
## Mermaid Diagrams

When the user asks to create, edit, or visualize a diagram, follow the
instructions in `.github/instructions/mermaid.instructions.md`.
<!-- mermaid-ai-skills:end -->
