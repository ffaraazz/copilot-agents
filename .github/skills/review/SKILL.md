---
name: review
description: Perform severity-ranked governance review for correctness, security, performance, maintainability, and requirement traceability.
argument-hint: "scope and files to review"
---

# Review

## Purpose

Provide deterministic, severity-ranked quality governance.

## Inputs

- Requirements and contract
- Code and test changes
- Architecture constraints

## Outputs

- Findings ordered by severity
- Residual risks and test gaps
- Clear release recommendation

## Procedure

1. Validate requirement and contract traceability.
2. Validate model independence using `.github/rules/model-separation.md` and record implementation/reviewer model families.
3. Check correctness, security, performance, maintainability using adversarial, disconfirming analysis.
4. Verify tests cover changed behavior and challenge gaps with failure scenarios.
5. Report findings with evidence and actionable guidance, then include residual risks.
6. Include model-evidence sources used to verify implementation and reviewer model claims.
