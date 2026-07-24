---
name: memory
description: Maintain shared session context so all agents stay synchronized on decisions, progress, assumptions, and blockers.
argument-hint: "milestone update details"
---

# Shared Memory Management

## Purpose

Maintain stable cross-agent context for long-running sessions.

## Inputs

- Current milestone state
- New decisions, assumptions, and outcomes

## Outputs

- Updated `.github/context/*.md` records

## Procedure

1. Read relevant context files before starting work.
2. Append concise updates after each milestone.
3. Keep entries factual, timestamped, and decision-oriented.
4. Link open questions to pending tasks.
