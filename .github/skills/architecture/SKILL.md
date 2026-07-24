---
name: architecture
description: Produce implementation-ready architecture and shared contracts. Use when system boundaries, interface contracts, or major technical decisions are needed.
argument-hint: "requirements summary and affected systems"
---

# Architecture And Contract Design

## Purpose

Produce implementation-ready architecture and shared contracts.

## Inputs

- Specs and constraints
- Repository patterns and existing architecture
- Detected stack profile

## Outputs

- Architecture decisions
- Contract artifact and version
- Tradeoff log

## Procedure

1. Analyze existing architecture style and conventions.
2. Detect whether cross-team contract is required.
3. Propose contract format and versioning strategy.
4. Define validation/auth/error semantics.
5. Obtain developer approval before freezing.
6. Record decisions in shared memory and architecture docs.
