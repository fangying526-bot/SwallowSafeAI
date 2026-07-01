# Swallowsafe AI Brings Evidence Based

## Pitch

- **Product:** SwallowSafe AI brings evidence-based pediatric foreign body management to parents before they reach the hospital.

By combining published clinical guidelines, deterministic clinical reasoning, and conversational AI, the product helps families recognize emergencies earlier, reduce delays in care, and make safer decisions while preserving the physician’s role in diagnosis and treatment.
- **Audience:** Parents and caregivers of children(0-18 years old).
- **Need:** Immediate, trustworthy guidance to determine whether this is an emergency, what to do before arriving at the hospital, and where to seek care.
- **Why now:** Different swallowed objects carry different risks, and parents often cannot determine the urgency or the appropriate next step

## 1. Primary Users

### Description

Parents and caregivers of children aged 0–18 years who suspect their child has swallowed a foreign body. They are non-medical users making urgent decisions under stress and need immediate, evidence-based guidance before arriving at the hospital. Success means quickly understanding whether the situation is an emergency, what to do next, and where to seek appropriate medical care.

### Segment

**Consumers**, daily or near-daily active usage expected.

### Required of this product

- MUST deliver useful output within 5 minutes of first launch
- MUST use plain language; SHOULD NOT use product-engineering jargon
- MUST fit inside the user's existing daily workflow (no context-switching for setup)
- SHOULD preserve any partial work across sessions

## 2. Problems to Solve

### Core problem

Users experience the following friction: Users do not know what to do next; Too many steps or decisions; Information is scattered and hard to find; Parents cannot accurately judge the urgency because different swallowed objects carry very different risks, even when the child has no symptoms..

### Worst-case failure mode

If everything technically works but users still abandon this, the most likely reason is: **The output looks plausible but is subtly wrong.** The team treats this as a regression even when tests are green.

### Success criterion

Target: ≥60% of started sessions reach the user's stated outcome within 2 weeks of activation.

Users experience the following friction: Users do not know what to do next; Too many steps or decisions; Information is scattered and hard to find; Parents cannot accurately judge the urgency because different swallowed objects carry very different risks, even when the child has no symptoms..

If everything technically works but users still abandon this, the most likely reason is: **The output looks plausible but is subtly wrong.** The team treats this as a regression even when tests are green.

Target: ≥60% of started sessions reach the user's stated outcome within 2 weeks of activation.

## 3. Capabilities

### Must have for v1

- Conversational symptom assessment, adaptive follow-up questions, evidence-based clinical recommendations, image upload for swallowed objects or medical documents, structured clinical summaries, pre-arrival instructions, and hospital guidance.

### Out of scope for v1 (tripwires)

If the implementation drifts toward any of the below, STOP and surface for re-scoping:

- **MUST NOT build:** Version 1 will not support physician-facing workflows
- **MUST NOT build:** Hospital electronic medical record (EMR) integration
- **MUST NOT build:** Appointment scheduling
- **MUST NOT build:** Telemedicine consultations
- **MUST NOT build:** Or AI-generated clinical decisions beyond published evidence-based guidelines

- Conversational symptom assessment, adaptive follow-up questions, evidence-based clinical recommendations, image upload for swallowed objects or medical documents, structured clinical summaries, pre-arrival instructions, and hospital guidance.

If the implementation drifts toward any of the below, STOP and surface for re-scoping:

- **MUST NOT build:** Version 1 will not support physician-facing workflows
- **MUST NOT build:** Hospital electronic medical record (EMR) integration
- **MUST NOT build:** Appointment scheduling
- **MUST NOT build:** Telemedicine consultations
- **MUST NOT build:** Or AI-generated clinical decisions beyond published evidence-based guidelines

## 4. Required Inputs

### Primary input method

Users interact through **Mix of choices and short text**.

### Required fields

- **The child's age, the suspected swallowed object, and whether the child has any symptoms. Additional information can be collected through guided follow-up questions.**

### Input rules

- MUST autosave on field blur with a 500ms debounce, never lose user input
- MUST validate inline; MUST NOT block on a modal for validation errors
- MUST mark optional fields with the literal word "(optional)" in the label
- MUST keep total required-field count at the minimum needed to deliver value
- SHOULD restore the last-typed value on reload of the same session

Users interact through **Mix of choices and short text**.

- **The child's age, the suspected swallowed object, and whether the child has any symptoms. Additional information can be collected through guided follow-up questions.**

- MUST autosave on field blur with a 500ms debounce, never lose user input
- MUST validate inline; MUST NOT block on a modal for validation errors
- MUST mark optional fields with the literal word "(optional)" in the label
- MUST keep total required-field count at the minimum needed to deliver value
- SHOULD restore the last-typed value on reload of the same session

## 5. User Flows

### First-time users

Try before sign-up, account only when saving.

**Goals for this flow:**

- Reach a first useful outcome in under 2 minutes
- Require no sign-up before initial value is shown
- Surface one clear primary action per step

### Returning users

View previous assessments, start a new assessment for another swallowing event, review prior recommendations, and update the child's symptoms if their condition changes.

**Goals for this flow:**

- Resume previous work without re-entering context
- Quick access to recent items and templates
- Fewer clicks than the first-time path

### Ideal journey

Try first → account only when saving or exporting

Try before sign-up, account only when saving.

**Goals for this flow:**

- Reach a first useful outcome in under 2 minutes
- Require no sign-up before initial value is shown
- Surface one clear primary action per step

View previous assessments, start a new assessment for another swallowing event, review prior recommendations, and update the child's symptoms if their condition changes.

**Goals for this flow:**

- Resume previous work without re-entering context
- Quick access to recent items and templates
- Fewer clicks than the first-time path

Try first → account only when saving or exporting

## 6. Constraints

### Hardest technical bet

The single decision most likely to break the product if wrong: **The data model — schema changes get expensive fast.** Flag uncertainty to the user before changing anything in this layer — don't refactor it silently.

### Experience constraints

- **Tone:** Balanced, guided but some flexibility
- **Reading level:** Plain language, no industry jargon by default
- **Forgiveness:** Easy undo, no destructive defaults
- **Onboarding:** Show, don't tell, inline demo over long copy

### Access & usage

- **Model:** Free tier with a small allowance, Future versions will offer subscription plans for healthcare professionals as well as enterprise plan for hospitals, medical schools, and endoscopy training programs.
- **Auth:** Optional for first run, required to save & export
- **Privacy:** Users own their data; export at any time

### What to avoid

- MUST NOT use free-text inputs where a choice of ≤5 options would suffice
- MUST NOT use modal dialogs that interrupt mid-task, inline messages only
- MUST NOT expose implementation jargon in the UI (database names, error codes, status enums).
- MUST NOT require sign-in before showing initial value

The single decision most likely to break the product if wrong: **The data model — schema changes get expensive fast.** Flag uncertainty to the user before changing anything in this layer — don't refactor it silently.

- **Tone:** Balanced, guided but some flexibility
- **Reading level:** Plain language, no industry jargon by default
- **Forgiveness:** Easy undo, no destructive defaults
- **Onboarding:** Show, don't tell, inline demo over long copy

- **Model:** Free tier with a small allowance, Future versions will offer subscription plans for healthcare professionals as well as enterprise plan for hospitals, medical schools, and endoscopy training programs.
- **Auth:** Optional for first run, required to save & export
- **Privacy:** Users own their data; export at any time

- MUST NOT use free-text inputs where a choice of ≤5 options would suffice
- MUST NOT use modal dialogs that interrupt mid-task, inline messages only
- MUST NOT expose implementation jargon in the UI (database names, error codes, status enums).
- MUST NOT require sign-in before showing initial value

## 7. Interface and Design Requirements

### Direction

- **Overall:** Calm and warm, soft neutrals with friendly type
- **Visual style:** Minimal and calm
- **Layout:** Single-column wizard

### Visual specifications

- **Theme support:** Light and dark modes, both production-ready
- **Iconography:** Consistent stroke weight across the set

### Accessibility

- **Contrast:** WCAG AA minimum on text and interactive elements
- **Keyboard:** Every action reachable without a mouse
- **Targets:** 44 × 44 pt minimum tap area on touch surfaces

- **Overall:** Calm and warm, soft neutrals with friendly type
- **Visual style:** Minimal and calm
- **Layout:** Single-column wizard

- **Theme support:** Light and dark modes, both production-ready
- **Iconography:** Consistent stroke weight across the set

- **Contrast:** WCAG AA minimum on text and interactive elements
- **Keyboard:** Every action reachable without a mouse
- **Targets:** 44 × 44 pt minimum tap area on touch surfaces

## 8. Platform and Implementation Requirements

### Build approach

- **Primary platform:** a vibe coding platform
- **Deploy target:** Web-first, mobile-responsive

### Recommended stack

- Next.js + TypeScript
- Tailwind CSS
- Supabase (Postgres + Auth + Storage + Edge Functions)
- Vercel hosting

### Export formats

- PDF summary
- Markdown bundle for Cursor / Claude Code
- Single PRD.md for Lovable / v0

### Implementation rules

- MUST deploy as a single web app at one origin; no separate admin app
- MUST treat the recommended stack above as the default; SHOULD ask before introducing a new dependency
- MUST persist user data through a clear, named storage layer (not in component state alone)
- SHOULD include a one-command local dev script (`npm run dev` or equivalent)

---

## Goals and Success Criteria

Track v1 success against the following measurable outcomes:

- **Activation:** ≥60% of new users reach their first useful result within 5 minutes of opening the product.
- **Retention:** ≥40% of activated users return within 7 days for a second session.
- **Quality:** Sessions complete without an error toast or a stuck loading state >2 seconds.
- **Out-of-scope tripwires hit:** 0. (Crossing one means re-scoping conversation.)