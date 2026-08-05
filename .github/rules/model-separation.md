# Model Separation Rule

## Purpose

Increase review reliability by separating implementation and review model families whenever possible.

## Required Inputs

- user-selected orchestrator model family (if explicitly chosen)
- implementation model family used for code changes
- currently available model families for the session
- review scope and risk level

## Availability-Gated Model Selection

1. Only assign models that are currently visible in the Copilot model picker or session model catalog.
2. Use exact model display strings when setting `model` in agent metadata or handoff metadata.
3. If Gemini-family models are unavailable, do not hardcode speculative Gemini model names.
4. When Gemini-family models become available, they may be added to agent `model` arrays with safe fallback ordering.

## Source Of Truth For Implementation Family

Determine implementation family in this priority order:

1. user-selected model family for ProjectOrchestrator session, when explicitly provided
2. explicit model argument used in implementation-agent dispatch
3. implementation report metadata
4. best-effort inference from chat context (last resort)

## Core Policy

1. Reviewer model family must differ from implementation model family by default.
2. If the user explicitly selected Claude-family for orchestration or implementation, reviewer must use a different family and should be pinned to the most capable available GPT-family review model. Prioritize GPT-5.3-Codex when available.
3. If implementation was performed with GPT-family models, prefer Claude-family review.
4. If implementation was performed with Gemini-family models, prefer GPT-family review (prioritize GPT-5.3-Codex), then Claude-family review.
5. If implementation model is unknown, choose the strongest available reviewer model family that is different from the likely implementation family.
6. Reviewer selection should prefer powerful-tier models over lightweight-tier models when both are available.

## Availability Fallback

Use this order when preferred reviewer family is unavailable:

1. alternate non-matching family with highest capability
2. any remaining non-matching family
3. same-family review only as last resort

For Gemini-family enablement:

1. verify exact Gemini model names from the active model picker/catalog
2. add Gemini entries to selected agent `model` arrays without removing existing non-Gemini fallbacks
3. validate review routing still preserves family separation

Capability ranking guidance for reviewer choice:

1. powerful-tier model in a non-matching family
2. balanced-tier model in a non-matching family
3. lightweight-tier model in a non-matching family
4. same-family model only with degraded independence declaration

If fallback step 3 is used, the review report must explicitly include:

- reason independence could not be achieved
- elevated residual-risk statement
- enhanced adversarial checklist evidence

If model identity evidence is missing, review cannot be marked complete.

## Adversarial Review Requirements

When reviewing, act with a disconfirming mindset:

1. Assume the change is unsafe until proven safe.
2. Try to break behavior through edge cases, threat cases, and contract violations.
3. Demand evidence for correctness claims from tests, contracts, and code paths.
4. Escalate uncertain behavior as findings, not assumptions.
5. Include exploit or failure scenarios for high-severity issues.

## Required Traceability

Before review completion, update shared memory and review artifacts with:

- implementation model family
- reviewer model family
- orchestrator user-selected model family (if any)
- fallback path used (if any)
- independence status: achieved or degraded
- evidence source for each model claim (for example: dispatch model argument, model picker confirmation, or platform audit log)
