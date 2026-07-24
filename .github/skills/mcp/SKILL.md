---
name: mcp
description: Validate MCP configuration and enforce official MCP-first documentation usage for the detected technology stack.
argument-hint: "detected stack summary"
---

# MCP Validation And Usage

## Purpose

Ensure official MCP servers are validated early and used consistently.

## Inputs

- Detected stack summary
- Optional `.vscode/mcp.json`

## Outputs

- MCP status report (configured/missing/incomplete)
- Recommended official servers per stack
- Developer decision (create/skip) when missing

## Procedure

1. Check whether `.vscode/mcp.json` exists.
2. If present, parse configured servers and map to detected stack.
3. If missing or incomplete, recommend official servers.
4. Ask developer to create or skip when not present.
5. Record decision and implications in shared memory.
6. Prefer MCP docs and code samples throughout execution.

## Guardrails

- Never silently skip MCP detection.
- Never present unverified framework guidance when MCP is available.
