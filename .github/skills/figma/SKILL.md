---
name: figma
description: Integrate Figma design intent into frontend workflow, or infer design language when Figma is unavailable. Use for frontend onboarding and UI handoff.
argument-hint: "frontend scope and optional figma url"
---

# Figma Workflow

## Purpose

Integrate design intent into frontend delivery deterministically.

## Inputs

- Frontend scope flag
- Optional Figma URL
- Existing frontend codebase

## Outputs

- Design source decision (Figma-driven or inferred)
- Token/component mapping
- Handoff readiness notes

## Procedure

1. Ask if Figma exists whenever frontend work is in scope.
2. If yes, request URL and recommend Figma MCP server.
3. If no, infer tokens/components from existing UI and record assumptions.
4. Keep output aligned with existing design language and accessibility needs.
