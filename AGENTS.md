# Swallowsafe AI Brings Evidence Based — agent rules

Imperative rules for any AI coding agent (Cursor, Claude Code, Cline, Aider, v0, Replit Agent) implementing this product.

## Operating principles

- Read **PRD.md** for product scope before writing any code.
- Read **DESIGN.md** for the visual contract before generating UI.
- Treat every **MUST** as a hard requirement.
- Treat every **MUST NOT** as a tripwire, stop and surface for re-scoping if you find yourself about to violate one.
- Treat **SHOULD** as a default that may be overridden if the user explicitly says so.

## Working discipline

Apply these on every task, in every mode. They keep an AI tool from inventing scope, sprawling, or rewriting code that was not in the request.

- **Think before coding.** State your assumptions. If two readings of the spec exist, present both; do not pick silently. If a simpler approach exists, say so. If something is unclear, stop and ask.
- **Simplicity first.** Minimum code that solves the problem. No speculative features, no abstractions for single-use code, no configurability nobody asked for, no error handling for impossible states. If it is 200 lines and could be 50, rewrite it.
- **Surgical changes.** Touch only what the task requires. Match the surrounding style even if you would do it differently. Do not refactor working code or reformat adjacent lines. Remove only the imports and variables your own change orphaned; leave pre-existing dead code alone and mention it instead.
- **Reuse first.** Search for an existing helper, component, or pattern before writing a new one.
- **Goal-driven execution.** Define what "done" looks like before you start, then verify against it. To fix a bug, write a test that reproduces it, then make it pass.
- **Finish the whole thing.** Cover the edge cases and error paths, not just the happy path. If the task is genuinely a rewrite or multi-step migration, flag it and scope it instead of half-doing it.
- **Take a position.** When you recommend something, say what you would do and what would change your mind. Recommending is not acting: surface the recommendation, then confirm before you build.

## Project-specific rules

These rules are derived from the user's answers for THIS specific product. They override generic defaults below.

- MUST NOT regress on this failure mode: The output looks plausible but is subtly wrong. Even if every test passes, this counts as a broken build.
- MUST flag uncertainty to the user before changing the load-bearing decision: The data model — schema changes get expensive fast. Don't refactor this layer without explicit sign-off.
- MUST NOT build: Version 1 will not support physician-facing workflows.
- MUST NOT build: Hospital electronic medical record (EMR) integration.
- MUST NOT build: Appointment scheduling.
- MUST deliver the v1 capability: Conversational symptom assessment, adaptive follow-up questions, evidence-based clinical recommendations, image upload for swallowed objects or medical documents, structured clinical summaries, pre-arrival instructions, and hospital guidance.
- MUST implement using Next.js + TypeScript, Tailwind CSS, Supabase (Postgres + Auth + Storage + Edge Functions), Vercel hosting. Don't substitute frameworks without checking with the user first. If your runtime can't produce Next.js + TypeScript, Tailwind CSS, Supabase (Postgres + Auth + Storage + Edge Functions), Vercel hosting as written (e.g. Lovable substituting TanStack Start), STOP and tell the user before swapping — let them choose between switching tools or switching stacks.
- MUST respect the cost/usage frame: Free tier with a small allowance.

## Input handling

- MUST autosave on field blur with a 500ms debounce, never lose user input.
- MUST validate inline; MUST NOT block on a modal for validation errors.
- MUST mark optional fields with the literal word "(optional)" in the label.
- MUST keep total required-field count at the minimum needed to deliver value.
- SHOULD restore the last-typed value on reload of the same session.

## UI & interaction

- MUST NOT use free-text inputs where a choice of ≤5 options would suffice.
- MUST NOT use modal dialogs that interrupt mid-task, inline messages only.
- MUST NOT expose implementation jargon in the UI (database names, error codes, status enums).
- MUST NOT require sign-in before showing initial value.
- MUST keep tap/click targets ≥ 44 × 44 pt on touch surfaces.
- MUST keep every action reachable by keyboard.

## Accessibility

- MUST meet WCAG AA contrast minimum on text and interactive elements.
- MUST support light and dark themes, both production-ready, neither a stretch goal.

## Out-of-scope tripwires

If you find yourself about to build any of the below, **stop** and ask the user before proceeding:

- MUST NOT build: Version 1 will not support physician-facing workflows
- MUST NOT build: Hospital electronic medical record (EMR) integration
- MUST NOT build: Appointment scheduling
- MUST NOT build: Telemedicine consultations
- MUST NOT build: Or AI-generated clinical decisions beyond published evidence-based guidelines
