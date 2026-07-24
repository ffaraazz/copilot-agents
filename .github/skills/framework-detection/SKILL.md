---
name: framework-detection
description: Detect languages, frameworks, runtimes, package managers, build systems, and test stacks from repository evidence. Use during onboarding.
argument-hint: "repository root or scope"
---

# Framework Detection

## Purpose

Detect repository technologies from evidence, not assumptions.

## Inputs

- Repository root path
- File system and search tool outputs

## Outputs

- Structured stack summary
- Confidence level (high/medium/low)
- Missing evidence or ambiguities
- Follow-up questions for developer when needed

## Procedure

1. Collect evidence from manifest and lock files.
2. Detect language, framework, runtime, package manager, build system, test framework.
3. Detect project topology: monorepo or single package.
4. Detect domains: frontend/backend/mobile/desktop/infra/CI.
5. Emit confidence score.
6. If confidence is below high, ask explicit confirmation questions.

## Evidence Matrix

- JavaScript/TypeScript: `package.json`, `pnpm-lock.yaml`, `yarn.lock`, `bun.lockb`
- Python: `pyproject.toml`, `requirements.txt`, `poetry.lock`
- .NET: `*.csproj`, `global.json`
- Go: `go.mod`
- Rust: `Cargo.toml`
- Java: `pom.xml`, `build.gradle`
- Ruby: `Gemfile`
- CI: `.github/workflows/*`
