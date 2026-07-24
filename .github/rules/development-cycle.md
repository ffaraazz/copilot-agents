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
13. Code Review
14. Refactoring
15. Documentation Update
16. Validation
17. Completion

## Stage Governance

- Never skip stages.
- Never advance with unresolved blocking assumptions.
- If a failure invalidates assumptions, return to the earliest impacted stage.
- Keep current stage and transition reasons in shared memory.

## Exit Criteria

- Developer approval obtained for requirements and contracts.
- Tests and review are complete for all changed behavior.
- Documentation and memory are updated before completion.
