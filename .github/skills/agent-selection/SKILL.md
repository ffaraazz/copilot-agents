---
name: agent-selection
description: Select only the specialist agents required for the current task and lifecycle stage. Use when deciding which agents to dispatch and which to skip.
argument-hint: "task summary and impacted domains"
---

# Adaptive Agent Selection

## Purpose

Select only the specialists needed for the current task.

## Inputs

- User prompt
- Repository profile
- Lifecycle stage
- Contract scope

## Outputs

- Selected agent list
- Skipped agent list with reasons
- Clarification questions when uncertain

## Procedure

1. Classify request type: analysis, architecture, implementation, QA, review.
2. Detect impacted domains: frontend, backend, data, infra, docs.
3. Select only agents required for those domains and current stage.
4. If uncertain, ask the developer before adding extra specialists.
5. Record selection decision in shared memory.
