# Copilot Agent Architecture (Modernized)

This repository now implements a modular, deterministic, MCP-first architecture for GitHub Copilot Agents.

## Design Goals

- Orchestrator-first execution
- Reusable skills and universal rules
- Shared memory for long sessions
- Contract-first full-stack development
- Reduced hallucination risk through inspect-first and MCP-first behavior
- Minimal duplication across agent files

## Current Structure

```text
.github/
   copilot-instructions.md
   agents/
      ProjectOrchestrator.agent.md
      BusinessAnalyst.agent.md
      ProductArchitect.agent.md
      UI-Designer.agent.md
      TestEngineer.agent.md
      BackendDeveloper.agent.md
      UI-Developer.agent.md
      CodeReviewer.agent.md
   rules/
      development-cycle.md
      hallucination-prevention.md
      coding-standards.md
      context-management.md
      tdd.md
      contract-first.md
   skills/
      framework-detection/SKILL.md
      mcp/SKILL.md
      planning/SKILL.md
      memory/SKILL.md
      architecture/SKILL.md
      code-analysis/SKILL.md
      documentation/SKILL.md
      testing/SKILL.md
      debugging/SKILL.md
      review/SKILL.md
      figma/SKILL.md
      agent-selection/SKILL.md
   context/
      session-memory.md
      repo-profile.md
      contract.md
      decision-log.md
      progress.md
   docs/
      modernization-report.md
      mcp-setup.md
```

## How It Works

1. Start with `ProjectOrchestrator`.
2. The orchestrator performs onboarding before any implementation delegation.
3. Onboarding runs repository analysis, framework detection, framework confirmation, and MCP validation.
4. If frontend and backend are both affected, a contract is created and frozen before implementation.
5. Specialist agents are selected adaptively, not by default.
6. Shared memory files are updated after every major milestone.

## Skill Format (Official)

Skills follow the VS Code Agent Skills format:

- Path: `.github/skills/<skill-name>/SKILL.md`
- `SKILL.md` must include YAML frontmatter.
- Required frontmatter fields: `name`, `description`.
- `name` must be lowercase letters, numbers, and hyphens only.
- `name` must match the parent directory name exactly.

## Lifecycle (Enforced)

The enforced lifecycle is defined in `.github/rules/development-cycle.md`:

Prompt -> Requirements Analysis -> Repository Analysis -> Framework Detection -> MCP Validation -> Architecture Analysis -> Contract Design -> Developer Approval -> Planning -> TDD/Test Plan -> Implementation -> Integration Testing -> Code Review -> Refactoring -> Documentation -> Validation -> Completion

## Shared Memory

Use `.github/context/*.md` as the source of truth for:

- detected repository profile
- current lifecycle stage
- frozen contract status
- decisions and rationale
- progress, blockers, and quality status

## MCP-First Behavior

- Orchestrator checks for `.vscode/mcp.json` during onboarding.
- If missing, the developer must choose create or skip.
- Official MCP docs and code samples are preferred over model memory.

## Why This Is Better

- Less duplication and lower maintenance burden
- Stronger determinism and less assumption drift
- Better coordination for parallel frontend/backend work
- Better resilience for long-running sessions

## Next Setup Step

Add `.vscode/mcp.json` for your stack and keep it aligned with `.github/docs/mcp-setup.md`.
