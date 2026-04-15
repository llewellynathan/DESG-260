# DESIGN.md — `[Your App Name]`

*This file is your design spec. Claude Code reads it every time you start a session, so it stays anchored to your visual intent. Keep it short, specific, and updated as you learn.*

*Think of this as a **portable studio** — everything Claude Code needs to render your intent consistently.*

---

## 1. Voice & Tone

**Three adjectives that describe how your app should *feel*:**

> 1. ________
> 2. ________
> 3. ________

**One "not this" — a tone to explicitly avoid:**

> *Example: "Not cheerful-corporate. No exclamation points. No 'Great job!' microcopy."*

**Sample microcopy.** Write the actual words for these five moments (keep them short):

| Moment | Your microcopy |
|---|---|
| Empty state (nothing to show yet) | |
| Success confirmation | |
| Error (something went wrong) | |
| Destructive action warning | |
| First-time welcome (one sentence) | |

---

## 2. Typography

**Headings font:** ___________________
**Body font:** ___________________
*(If only one, use the same for both. Pick from Google Fonts — they're free and easy for Claude Code to install.)*

**Type scale** (use these exact values in the code):

| Role | Size | Weight | Line height |
|---|---|---|---|
| Display (hero) | | | |
| H1 | | | |
| H2 | | | |
| Body | 16px | 400 | 1.5 |
| Small / caption | | | |

*If you're not sure, start with this scale: 48 / 32 / 24 / 16 / 14 px. Adjust later.*

---

## 3. Color Palette

**Write exact hex codes.** Don't write "blue" — write `#2563EB`. Claude Code needs tokens, not descriptions.

| Token | Hex | Used for |
|---|---|---|
| `--color-primary` | | Main action buttons, links |
| `--color-primary-hover` | | Primary hover/pressed state |
| `--color-bg` | | App background |
| `--color-surface` | | Cards, elevated surfaces |
| `--color-text` | | Primary text |
| `--color-text-muted` | | Secondary text, captions |
| `--color-border` | | Dividers, input borders |
| `--color-success` | | Success states |
| `--color-warning` | | Warnings, destructive hover |
| `--color-danger` | | Errors, destructive actions |

**Dark mode?** (circle one): Yes / No / Later

---

## 4. References

**3–5 screenshots of apps, websites, or artifacts you're drawing inspiration from. For each one, answer: *what specifically do you like, and why?***

The "why" is what matters. "I like Linear" is useless. "I like how Linear's empty states use a single illustration and one sentence instead of a feature tour — it respects the user's time" is a design brief.

### Reference 1
![Reference 1](references/ref-01.png)
- **Source:** *(app/site name)*
- **What I like:** *(specific: a component, a pattern, a piece of microcopy, a use of space)*
- **Why it matters for my app:** *(how this principle applies to your product, not just visual mimicry)*

### Reference 2
![Reference 2](references/ref-02.png)
- **Source:**
- **What I like:**
- **Why it matters for my app:**

### Reference 3
![Reference 3](references/ref-03.png)
- **Source:**
- **What I like:**
- **Why it matters for my app:**

*(Add 4 and 5 if useful. Stop at 5 — more references means less clarity, not more.)*

---

## 5. Component Inventory

**The parts your app is built from.** List what you need. Claude Code will use this to keep components consistent.

- **Buttons:** primary, secondary, destructive, ghost (text-only)
- **Inputs:** text, textarea, (add: checkbox, radio, select, toggle as needed)
- **Cards:** ___________________
- **Navigation pattern:** (tab bar? side nav? stack? ___________________)
- **Modals / dialogs:** when? ___________________
- **Empty states:** what should they look like? ___________________
- **Loading states:** what pattern? (skeletons? spinner? progressive reveal?)
- **Icons:** which library? *(Lucide is a safe default — free, clean, Claude Code knows it well)*

---

## 6. Layout & Spacing

**Spacing scale** (use these, don't invent custom values):
- `4px, 8px, 12px, 16px, 24px, 32px, 48px, 64px`

**Corner radius:**
- Buttons: `___` px
- Cards / surfaces: `___` px
- Inputs: `___` px

**Max content width** (for desktop): `___` px *(e.g., 720 for reading apps, 1200 for dashboards)*

---

## 7. Motion (optional)

Keep it minimal. Over-animating is the most common "AI app tells" that makes your product feel generic.

- **Default transition:** `150ms ease-out` *(safe baseline)*
- **When do you use motion?** *(e.g., "on state changes only — no decorative animation")*

---

## Review Checklist (before handing this to Claude Code)

- [ ] Every color is a hex code, not a word.
- [ ] Every type size has a pixel value.
- [ ] Every reference has a "why it matters," not just a screenshot.
- [ ] The voice/tone section could be used to write real microcopy — not just "friendly and modern."
- [ ] You'd be embarrassed if a designer you admire read this and it was vague.

---

*This template is part of the AI App Design Guide. See [`ai_app_design_guide.md`](../ai_app_design_guide.md) for the full workflow.*
