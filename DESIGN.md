---
design_tokens:
 # Auto-derived from the DESIGN.md tables below. Edit the tables, not
 # this block (it is regenerated on every change).
 colors:
 light:
 bg: "#FBF7F1"
 surface: "#FFFFFF"
 border: "#E8E0D3"
 text-primary: "#2A2520"
 text-secondary: "#6B5F52"
 text-muted: "#7C7166"
 primary: "#C2410C"
 secondary: "#15803D"
 tertiary: "#B45309"
 cta: "#EAB308"
 success: "#16A34A"
 warning: "#D97706"
 danger: "#B91C1C"
 info: "#0369A1"
 dark:
 bg: "#1B1612"
 surface: "#26201B"
 border: "#3A332C"
 text-primary: "#F5EFE6"
 text-secondary: "#C5B8A8"
 text-muted: "#8B7E6E"
 primary: "#FB923C"
 secondary: "#4ADE80"
 tertiary: "#FBBF24"
 cta: "#FACC15"
 success: "#4ADE80"
 warning: "#FBBF24"
 danger: "#F87171"
 info: "#38BDF8"
 typography:
 display: "Fraunces"
 body: "Inter"
 mono: "IBM Plex Mono"
---

# Swallowsafe AI Brings Evidence Based — design

Visual contract for this product. Treat this as the authoritative source for any UI you generate, colors, typography, spacing, motion, and component primitives. Do not invent new tokens; if something isn't covered here, ask before adding it.

## Design philosophy

Inviting, human, late-afternoon-light. Cream surfaces, terracotta and forest accents. Fraunces gives headlines a literary, considered feel, a hint of optical-size variation per heading level reads as craft. Inter keeps body type modern and neutral.

**This brand is:** _inviting_ · _human_ · _honest_ · _tactile_ · _unhurried_

**This brand is NOT:** _cold_ · _clinical_ · _sterile_ · _machined_. When a visual choice would push the product toward one of these, flag it instead of shipping it.

## Color palette · Warm & cozy

> Inviting, human, late-afternoon-light. Cream surfaces, terracotta and forest accents.

### Light theme

| Token | Hex | Use |
|---|---|---|
| `--bg` | `#FBF7F1` | Page background |
| `--surface` | `#FFFFFF` | Cards, modals, raised surfaces |
| `--border` | `#E8E0D3` | Subtle dividers and input borders |
| `--text-primary` | `#2A2520` | Body copy, headings |
| `--text-secondary` | `#6B5F52` | Helper text, captions |
| `--text-muted` | `#7C7166` | Disabled / least-emphasis copy |
| `--primary` | `#C2410C` | Primary action, brand emphasis |
| `--secondary` | `#15803D` | Secondary highlights, accents |
| `--tertiary` | `#B45309` | Decorative pops, tags |
| `--cta` | `#EAB308` | The single most-important CTA per page |
| `--success` | `#16A34A` | Confirmations, positive feedback |
| `--warning` | `#D97706` | Soft caution states |
| `--danger` | `#B91C1C` | Destructive actions, errors |
| `--info` | `#0369A1` | Neutral informational accents |

### Dark theme

| Token | Hex | Use |
|---|---|---|
| `--bg` | `#1B1612` | Page background |
| `--surface` | `#26201B` | Cards, modals, raised surfaces |
| `--border` | `#3A332C` | Subtle dividers and input borders |
| `--text-primary` | `#F5EFE6` | Body copy, headings |
| `--text-secondary` | `#C5B8A8` | Helper text, captions |
| `--text-muted` | `#8B7E6E` | Disabled / least-emphasis copy |
| `--primary` | `#FB923C` | Primary action, brand emphasis |
| `--secondary` | `#4ADE80` | Secondary highlights, accents |
| `--tertiary` | `#FBBF24` | Decorative pops, tags |
| `--cta` | `#FACC15` | The single most-important CTA per page |
| `--success` | `#4ADE80` | Confirmations, positive feedback |
| `--warning` | `#FBBF24` | Soft caution states |
| `--danger` | `#F87171` | Destructive actions, errors |
| `--info` | `#38BDF8` | Neutral informational accents |

**Contrast rules:** every text/background pairing MUST meet WCAG AA (4.5:1 for body text, 3:1 for large text). When in doubt, run a contrast check before shipping.

## Typography · Editorial serif

Fraunces gives headlines a literary, considered feel, a hint of optical-size variation per heading level reads as craft. Inter keeps body type modern and neutral.

### Font families

- **Display / Headings:** Fraunces (weights 500, 700, 900)
 - Google Fonts: https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,700;9..144,900&display=swap
 - Stack: `'Fraunces', Georgia, 'Times New Roman', serif`
- **Body / UI:** Inter (weights 400, 500, 600)
 - Google Fonts: https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap
 - Stack: `'Inter', system-ui, -apple-system, sans-serif`
- **Code / Mono:** IBM Plex Mono (weights 400, 600)
 - Google Fonts: https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;600&display=swap
 - Stack: `'IBM Plex Mono', ui-monospace, SFMono-Regular, monospace`

### HTML setup

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,700;9..144,900&display=swap">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&display=swap">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;600&display=swap">
```

### Type scale (1.250 major-third ratio)

| Token | Size | Line height | Weight | Use |
|---|---|---|---|---|
| `display` | 3.815rem / 61px | 1.05 | 800 | Marketing hero |
| `h1` | 3.052rem / 49px | 1.1 | 800 | Page title |
| `h2` | 2.441rem / 39px | 1.15 | 700 | Section heading |
| `h3` | 1.953rem / 31px | 1.2 | 700 | Sub-section |
| `h4` | 1.563rem / 25px | 1.25 | 600 | Card title |
| `body-lg` | 1.25rem / 20px | 1.55 | 400 | Lead paragraph |
| `body` | 1rem / 16px | 1.6 | 400 | Default body |
| `body-sm` | 0.875rem / 14px | 1.5 | 400 | Helper text |
| `caption` | 0.75rem / 12px | 1.4 | 500 | Captions, labels |
| `mono` | 0.875rem / 14px | 1.55 | 400 | Code, technical detail |

## Spacing scale (4px base)

| Token | Value | Use |
|---|---|---|
| `space-1` | 4px / 0.25rem | Hairline gap between adjacent icons/text |
| `space-2` | 8px / 0.5rem | Tight inline gap |
| `space-3` | 12px / 0.75rem | Default control padding |
| `space-4` | 16px / 1rem | Default block padding |
| `space-5` | 24px / 1.5rem | Section padding |
| `space-6` | 32px / 2rem | Generous separation |
| `space-8` | 48px / 3rem | Block-to-block divider |
| `space-10` | 64px / 4rem | Hero / large layout breathing room |

**Rule:** stick to multiples of 4. Never ship a 13px or 17px value, they break vertical rhythm.

## Border radius

| Token | Value | Use |
|---|---|---|
| `radius-sm` | 6px | Small inputs, chips |
| `radius-md` | 10px | Buttons, default inputs |
| `radius-lg` | 16px | Cards, dialogs |
| `radius-xl` | 24px | Hero blocks, large media |
| `radius-full` | 9999px | Pills, avatar circles |

## Elevation (shadows)

```css
--shadow-sm: 0 1px 2px rgba(0,0,0,0.06), 0 1px 1px rgba(0,0,0,0.04);
--shadow-md: 0 4px 8px rgba(0,0,0,0.08), 0 2px 4px rgba(0,0,0,0.05);
--shadow-lg: 0 12px 24px rgba(0,0,0,0.10), 0 6px 12px rgba(0,0,0,0.06);
--shadow-xl: 0 24px 48px rgba(0,0,0,0.14), 0 12px 24px rgba(0,0,0,0.08);
```

Use shadow sparingly, borders + background contrast usually carry depth better in dark mode. Never combine `shadow-xl` with `border-2` on the same element.

## Motion

| Token | Duration | Easing | Use |
|---|---|---|---|
| `motion-fast` | 120ms | `cubic-bezier(0.4, 0, 0.2, 1)` | Hover, focus, micro-state |
| `motion-normal` | 220ms | `cubic-bezier(0.4, 0, 0.2, 1)` | Default UI transition |
| `motion-slow` | 360ms | `cubic-bezier(0.16, 1, 0.3, 1)` | Modals, page transitions |
| `motion-spring` | 480ms | `cubic-bezier(0.34, 1.56, 0.64, 1)` | Playful confirmations |

**Respect `prefers-reduced-motion`**, fall back to opacity-only transitions when the user has it on.

## Component primitives

Apply these baseline styles to every UI primitive you generate.

### Buttons

- **Primary**, `--cta` background, `--text-primary` foreground (or white on dark CTA), `radius-md`, `space-3` vertical / `space-4` horizontal padding, min-height 44px.
- **Secondary**, transparent background, `--primary` text, 2px `--primary` border.
- **Ghost**, transparent background, `--text-secondary` text, no border, `--surface` hover.
- **Destructive**, `--danger` background, white text. Confirm before firing.
- **States**, hover (8% darken), focus (2px ring `--primary` at 40% opacity, 2px offset), active (12% darken), disabled (50% opacity, `cursor: not-allowed`).

### Inputs

- 2px `--border` border, `radius-md`, `space-3` padding.
- Focus: border swaps to `--primary` (no glow). Maintain WCAG AA contrast.
- Error: border `--danger`, helper text `--danger`. Never rely on color alone, include an icon or label.

### Cards

- `--surface` background, 1px `--border`, `radius-lg`, `space-5` padding.
- Avoid `shadow-lg` on cards in dark mode, it muddies contrast. Lean on the border.

### Toasts / notifications

- Bottom-right anchored, slide-in over 220ms.
- Success → `--success` left border. Warning → `--warning`. Danger → `--danger`. Info → `--info`.
- Auto-dismiss after 5s except for `danger` (sticky until dismissed).

### Modals / dialogs

- 16px backdrop blur over a 50%-opacity black scrim.
- Centered, `max-width: 32rem`, `radius-xl`, `space-6` padding.
- Esc closes. Click-outside closes. First focusable element receives focus on open.

## Component do / don't

Use these as hard tripwires. If the implementation lands in the right column, stop and re-do it.

| Component | DO | DON'T |
| ----------- | ----------------------------------------------------- | -------------------------------------------------------- |
| Button | Outcome-named labels ("Save changes", "Delete jar") | Generic verbs ("Submit", "OK", "Cancel" alone) |
| Button | Solid `--danger` background on destructive | Gradient on destructive; red text on red bg |
| Input | Pick ONE error signal: red border OR red helper text | Combine red border + red icon + red helper (overkill) |
| Input | Visible label OR programmatic label + `aria-label` | Placeholder as the only label (vanishes on focus) |
| Toast | Auto-dismiss non-destructive after 5s | Persist any toast > 6s except `danger` (which is sticky) |
| Toast | Anchor bottom-right, slide in 220ms | Block the user's primary action with a centered banner |
| Modal | One primary action + one secondary (cancel/dismiss) | Three or more buttons of equal weight |
| Modal | Esc closes; first focusable gets focus on open | Trap the user with no Esc and no visible Close button |
| Card | Lean on `--border` in dark mode | Use `shadow-lg` on cards in dark mode (muddies contrast) |
| Icon | Pair with a visible label OR `aria-label` | Ship icon-only buttons with no accessible name |

## Iconography

- **Library:** Lucide (https://lucide.dev), modern, MIT-licensed, consistent stroke. Alternative: Phosphor or Heroicons. Pick one and stay there.
- **Stroke width:** 1.75 for outline icons, 2 for ones that need more weight at small sizes.
- **Size scale:** 14 / 16 / 20 / 24 / 32, never ship a 13 or 17.
- **Color:** inherits `currentColor`. Don't hard-code icon fills.

## Imagery

- **Aspect ratios:** 16:9 (hero / video), 4:3 (card thumbnail), 1:1 (avatar / badge), 3:4 (mobile-first portrait).
- **Treatment:** apply consistent `radius-lg` (or `radius-full` for avatars). Avoid hard 0-radius photos in cards.
- **Empty / placeholder images:** use a subtle `--surface` block with a Lucide outline icon, not stock-photo silhouettes.

## Accessibility

- **Contrast:** every text/background pairing MUST meet WCAG AA. Use the tokens above, they're already vetted.
- **Focus:** every interactive element MUST show a visible focus ring (default: 2px `--primary` at 40% opacity, 2px offset). Never `outline: none` without a replacement.
- **Tap targets:** 44 × 44 px minimum on any touch surface.
- **Motion:** honour `prefers-reduced-motion: reduce`.
- **Color alone:** never use color as the only signal, pair with icon, label, or position.
- **Form labels:** every input MUST have a visible label or a programmatically associated one. Placeholder ≠ label.

## Tone & voice (UI copy)

- Plain language. No engineering jargon.
- Active voice. Short sentences.
- Buttons name the outcome ("Save changes", not "Submit").
- Errors say what happened AND how to fix it ("We couldn't load your PRDs. Try refreshing.").
- Confirmations are specific ("PRD saved · 2 sec ago", not just "Saved").

### Tone in practice (before → after)

Rewrite anything that lands in the left column. Match the right column's specificity.

| Before (don't ship) | After (ship) |
| ---------------------------------------------- | ----------------------------------------------------------- |
| Submit | Save changes |
| Are you sure? | Delete this saved item? Click Delete again to confirm. |
| Error: invalid email. | That email is already in use. Try signing in instead. |
| Something went wrong. | We could not reach the server. Check your connection, then retry. |
| Loading... | Loading your saved work. |
| Settings updated. | Changes saved. |

---

**Implementation note:** Don't reinvent. If you need a token not listed here (a new shadow, a new size, a new color), surface the gap and ask before adding it. The whole point of this file is that there's ONE source of visual truth.
