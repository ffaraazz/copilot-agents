# Development Lifecycle Rule

This lifecycle is mandatory for implementation tasks:

1. Prompt
2. Requirements Analysis
3. Repository Analysis
4. Framework Detection
5. MCP Validation
6. Architecture Analysis
7. Contract Design (when multiple components/services are involved)
8. Developer Approval
9. Planning
10. TDD or Test Plan
11. Parallel Implementation (when safe)
12. Integration Testing
13. Quality Gate (Pre-Review)
14. Code Review
15. Refactoring
16. Documentation Update
17. Validation
18. Completion

## Code Review Gate

Before Stage 14 can be marked complete:

1. Confirm pre-review quality gate passed or approved exceptions are documented.
1. Apply `.github/rules/model-separation.md`.
2. Confirm reviewer model family differs from implementation model family, or document fallback and degraded independence risk.
3. Ensure review findings are severity-ranked with evidence and residual risks.

## Stage Governance

- Never skip stages.
- Never advance with unresolved blocking assumptions.
- If a failure invalidates assumptions, return to the earliest impacted stage.
- Keep current stage and transition reasons in shared memory.

## Exit Criteria

- Developer approval obtained for requirements and contracts.
- Tests and review are complete for all changed behavior.
- Documentation and memory are updated before completion.
