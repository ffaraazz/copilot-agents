---
name: debugging
description: Diagnose failures deterministically and route remediation to the correct lifecycle stage. Use for failing tests, runtime errors, and regression triage.
argument-hint: "error details and reproduction steps"
---

# Debugging

## Purpose

Diagnose failures deterministically and route to the right lifecycle stage.

## Inputs

- Failing tests or runtime errors
- Logs and stack traces
- Recent changes

## Outputs

- Root cause hypothesis ranked by evidence
- Minimal fix plan
- Stage rollback recommendation if needed

## Procedure

1. Reproduce failure.
2. Isolate impacted module and contract surface.
3. Validate hypotheses with tests/logs.
4. Propose smallest safe fix.
5. Re-run tests and update memory with outcome.
