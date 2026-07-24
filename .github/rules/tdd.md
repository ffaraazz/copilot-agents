# TDD Rule

Use Red-Green-Refactor for implementation tasks unless explicitly exempted.

## Red

- Ensure tests exist and fail for the intended behavior.

## Green

- Implement the minimal change needed to pass failing tests.

## Refactor

- Improve structure without changing behavior.
- Re-run tests to confirm no regressions.

## Guardrails

- Do not weaken or skip tests to force green status.
- Do not implement features outside validated requirements and contract.
