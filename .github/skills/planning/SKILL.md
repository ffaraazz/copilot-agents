---
name: planning
description: Build stage-aware execution plans with clear acceptance criteria, dependencies, and agent dispatch boundaries.
argument-hint: "approved requirements and lifecycle stage"
---

# Planning

## Purpose

Create executable, stage-aware plans from approved requirements.

## Inputs

- Developer-approved requirements
- Lifecycle stage
- Repository profile
- Contract status

## Outputs

- Ordered task plan
- Agent dispatch map
- Risk list and blockers

## Procedure

1. Confirm lifecycle preconditions are met.
2. Break work into milestones with acceptance criteria.
3. Mark parallelizable items only when file boundaries and dependencies are independent.
4. Attach test and review gates per milestone.
5. Update progress memory with status transitions.
