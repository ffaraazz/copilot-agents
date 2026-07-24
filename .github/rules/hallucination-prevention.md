# Hallucination Prevention Rule

## Non-Negotiable Behavior

- Inspect first. Never invent repository structure, packages, APIs, frameworks, or configs.
- Verify assumptions against files, tool output, or approved contract.
- Ask the developer when confidence is low.
- Prefer official documentation via MCP tools whenever available.

## Verification Checklist

1. Is this claim supported by repository evidence?
2. Is this API/schema confirmed by contract or source code?
3. Is this framework/library behavior validated in MCP docs?
4. Is there any unresolved ambiguity that requires developer input?

If any answer is no, stop and resolve before implementation.
