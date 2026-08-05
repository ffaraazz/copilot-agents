---
name: quality-gate
description: Run a pre-review quality gate that checks simplicity, reuse, duplication, and comment hygiene before adversarial review.
argument-hint: "scope and files to quality-check"
---

# Quality Gate

## Purpose

Catch maintainability and design-quality regressions before formal code review.

## Inputs

- Requirements and accepted scope
- Architecture and contract constraints
- Changed code and tests

## Outputs

- Quality gate report with pass or fail decision
- Severity-ranked findings for overengineering, duplication, and hygiene
- Recommended remediation actions

## Procedure

1. Check scope discipline: reject features outside requirements.
2. Check simplicity: flag unnecessary abstractions and speculative generalization.
3. Check reuse: detect where existing utilities/components should be reused.
4. Check duplication: identify repeated logic and near-duplicate implementations.
5. Check comments: flag excessive, redundant, or low-value comments.
6. Verify test impact and maintainability risk of accepted code shape.
7. Emit a gate decision with clear evidence and follow-up actions.
