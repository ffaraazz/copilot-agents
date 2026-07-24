---
name: code-analysis
description: Analyze repository code changes against requirements, architecture boundaries, and contracts. Use before implementation and during review.
argument-hint: "changed modules and expected behavior"
---

# Code Analysis

## Purpose

Ground implementation and review in current repository behavior.

## Inputs

- Changed files
- Requirements and contract
- Existing tests and docs

## Outputs

- Compatibility notes
- Risk hotspots
- Required code and test updates

## Procedure

1. Map changed behavior to touched modules.
2. Check for architecture boundary violations.
3. Identify integration points and likely regressions.
4. Verify consistency with contract and standards.
