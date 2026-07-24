---
name: testing
description: Author deterministic tests for new behavior and validate integrated quality outcomes in QA mode.
argument-hint: "requirements, contract, and target test scope"
---

# Testing

## Purpose

Drive implementation with deterministic tests and validate integrated behavior.

## Inputs

- Requirements and FR-IDs
- Contract artifact
- Existing test setup

## Outputs

- Failing tests for new behavior
- QA validation report

## Procedure

1. Author tests tied to requirements and contract behavior.
2. Ensure tests fail for missing behavior before implementation.
3. Validate positive, negative, and edge behavior.
4. In QA mode, execute full relevant suite and summarize risk.
