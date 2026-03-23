# Spec: UI Design Checklist — Static HTML Page

## Purpose
A single-page static HTML file students can open in a browser or be linked to. They use it to audit one screen of their high-fidelity design before submitting. No frameworks, no build step, no backend — one `.html` file that works offline.

---

## Functional Requirements

- **Checkboxes are interactive** — clicking a checkbox marks it checked
- **Checked state persists via `localStorage`** — if the student closes and reopens the tab, their progress is saved
- **"Reset" button** clears all checkboxes and localStorage (one button, subtle placement)
- **Progress indicator** — shows "X of Y complete" that updates live as boxes are checked
- **Print-friendly** — `@media print` styles that render cleanly (checkboxes visible, no UI chrome)
- No login, no server, no dependencies (no CDN imports either — fully self-contained)

---

## Layout

Two-column layout on desktop (≥768px), single column on mobile. All content fits on one page on desktop without scrolling (use compact spacing).

**Page structure:**
```
[Title]
[Subtitle]            [Progress: X of Y complete]
─────────────────────────────────────────────────
[Left column]   [Right column]
─────────────────────────────────────────────────
[Footer note]         [Reset button]
```

---

## Visual Design

**Aesthetic:** Clean, minimal, editorial. Feels like something from a design book, not a generic web form. White background, dark ink, subtle rules. No decorative elements.

**Typography:**
- Font: `system-ui, -apple-system, 'Helvetica Neue', sans-serif`
- Page title: 28–32px, weight 600, tight letter-spacing (-0.02em)
- Section headers: 10–11px, weight 700, ALL CAPS, letter-spacing +0.08em, muted color (#666)
- Checklist items: 13–14px, weight 400, color #1a1a1a, line-height 1.45
- Sub-notes (indented italic hints under some items): 11–12px, italic, color #999

**Colors:**
- Background: #ffffff
- Body text: #1a1a1a
- Section label: #666666
- Sub-notes: #999999
- Rules/borders: #e8e8e8
- Row separator: #f4f4f4
- Checkbox border: #c0c0c0
- Checkbox checked fill: #1a1a1a (or dark brand-neutral)
- Progress text: #666

**Spacing:**
- Page padding: 40px (desktop), 20px (mobile)
- Column gap: 40px
- Section header margin-top: 24px
- Between checklist items: 1px rule, 6px padding top/bottom
- Checkbox size: 14×14px, border-radius 3px, border 1.5px

**Checkbox behavior:**
- Default: white fill, #c0c0c0 border
- Checked: dark fill (#1a1a1a), white checkmark (✓ via `::after` pseudo-element or SVG)
- Checked item text: slightly reduced opacity (0.5) with a subtle strikethrough — makes progress feel satisfying
- Smooth transition on check/uncheck (150ms ease)

**Section headers:**
- Small rule line above each section header
- Emoji + label, e.g. "🎯  VISUAL HIERARCHY"

---

## Content

### Left Column

**🎯 Visual Hierarchy**
- I can identify my **Level 1 element** (the most important thing) in under 3 seconds
- I have **no more than 3 hierarchy levels** visible at once
- I used **bold, regular, and light** weights intentionally — not everything the same
- I used **color contrast** alongside size to build hierarchy
- Competing elements are **de-emphasized** — lighter, smaller, or lower contrast

**📏 Spacing**
- All spacing is a **multiple of 8** — 8, 16, 24, 32, 48, 64px
- Space **between groups** is noticeably larger than space **within groups**
- I started with generous whitespace and only removed what felt excessive
- Related elements are **close**; unrelated elements have breathing room

**🔤 Typography**
- I'm using **4 or fewer font sizes** — no arbitrary in-between values
- Large headlines have **tighter letter spacing** (~−0.02em)
- All-caps labels have **looser letter spacing** (at least +0.05em)
- Body text is **15–16px** with 1.4–1.5 line height
- Mixed-size text on the same line is **baseline-aligned**, not center-aligned

**📐 Alignment**
- I can draw an invisible line through the **left edges** of my main content
- Elements that look like they should align actually **do** align — not approximately
- Icons beside text align to the **optical center of the text**, not the bounding box

### Right Column

**🎨 Color**
- I have **one primary accent color** — used only for actions and interactive elements
- My accent color is **rare** — not on more than ~10% of the screen
- All text/background pairs pass **4.5:1 contrast minimum**
- I'm not using **pure grey** for neutrals — my greys have a warm or cool tint
- Color is **not the only** indicator of state — errors also have icons, borders, or text
- I'm not using color on **non-interactive headings** — it makes them look like links

**🏷 Labels & Data**
- I'm not showing data as **"Label: Value"** everywhere — labels are embedded into values where possible
  - *Sub-note: "In stock: 12" → "12 left in stock"*
- Where labels are necessary, they are **de-emphasized** — smaller, lighter, lower contrast
- Form fields have **visible labels above the input** — not just placeholder text

**✂️ Restraint**
- **Cover test:** I covered each element — if removing it loses nothing, I considered cutting it
- I haven't added elements because something "felt empty" — I fixed the hierarchy instead
- Cards and borders only exist because **spacing alone** doesn't create the grouping

**♿ Accessibility**
- All text passes **4.5:1 contrast** against its background
- Errors and status states use **icons or text**, not color alone
- Touch targets are at least **44×44px**

**🚨 Quick Gut-Check**
- No "Label: Value" dumps — data has hierarchy
- No equidistant spacing — tighter within groups, wider between them
- No color as the only error indicator — icon or message added
- No light text on medium-saturation color — contrast checked
- No random font sizes — every size is from my defined scale
- No same-size, same-weight everything — clear hierarchy exists

---

## Footer

Left-aligned italic note:
> *Your first instinct is usually "add something." The fix is usually "adjust hierarchy, spacing, or contrast." · Principles from Refactoring UI & Practical UI*

Right-aligned: `[Reset checklist]` button — small, plain text style (no filled background), color #999, hover color #333.

---

## Print Styles (`@media print`)

- Hide the Reset button and progress indicator
- Remove transitions
- Ensure checkboxes render visibly (solid border, filled if checked)
- No page break inside a section
- Margins: 0.75in

---

## File Output

Single file: `ui-design-checklist.html`
No external dependencies. Inline all CSS and JS.
