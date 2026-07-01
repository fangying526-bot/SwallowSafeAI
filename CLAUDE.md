# Swallowsafe AI Brings Evidence Based — router

Project context for AI coding agents.

## Files in this project

- **PRD.md**, product scope: pitch, primary users, problems, capabilities, flows, success criteria.
- **AGENTS.md**, imperative MUST / MUST NOT / SHOULD rules. Read before generating code.
- **DESIGN.md**, visual contract: typography, colors, layout, theme, accessibility, reference images.

## When implementing a feature

1. Check **PRD.md → Pitch** and **→ Capabilities** to confirm the feature is in v1 scope.
2. Check **AGENTS.md → Out-of-scope tripwires** to confirm it's not explicitly excluded.
3. Read **AGENTS.md → UI & interaction** and **→ Input handling** for the rules you MUST follow.
4. Read **DESIGN.md** before generating UI markup.
5. If anything is ambiguous, ask before writing code, do not invent.

## How to work

Before writing code: think first (surface assumptions, ask when unclear), keep it simple (minimum code, nothing speculative), make surgical changes (touch only what the task needs), reuse existing patterns before inventing new ones, define "done" and verify against it, cover the edge cases, and recommend before you act. Full rules in **AGENTS.md → Working discipline**.

## Tone

Match the product's stated tone (see PRD.md → Constraints). Default to plain language; never expose engineering jargon to end users.
