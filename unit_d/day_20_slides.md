# Day 20 Presentation Outline
## Unit D: Neue App (Capstone)

---

### Slide 1: Warm-Up
**Warm-Up: D6 Second Platform Gallery** (10 min)
- Lay out your D6 submissions on your desk or screen
- Walk around and look at 3–4 classmates' second platform designs
- For each: What platform did they choose? What's the most interesting adaptation?
- Find someone who chose a different platform than you — compare notes

---

### Slide 2: Prayer
**Prayer**
Carol, will you pray for us today?

---

### Slide 3: Title
**Unit D: Neue App**
A design system is the toolkit you build before you build the product.

---

### Slide 4: Today
**Today**
- What is a design system?
- Logo + wordmark
- Type scale in Figma
- Color tokens
- D6 peer feedback
- Work session

---

### Slide 5: By the end of today...
**Design system** — You'll have a working Figma file with text styles, color styles, and a logo — the foundation for every screen you build

**Type scale** — You'll set up 7 named text styles in Figma (Display through Button) that update everywhere when you change them

**Color tokens** — You'll define colors by role (Primary, Surface, Error) not by name, with contrast ratios checked

**Logo** — You'll create a simple logo + wordmark that works at app icon size

---

### Slide 6: Why This Matters
**Why this matters**
- Day 21, you build screens from scratch in Figma. Without a design system, you'll make hundreds of one-off decisions — picking colors by eye, guessing font sizes, rebuilding the same button five times.
- A design system eliminates those decisions upfront. Every professional UI team builds one first.

---

### Slide 7: What Is a Design System?
**What Is a Design System?**
Reusable decisions, not a pretty PDF

---

### Slide 8: A set of reusable decisions
**A design system is a set of reusable decisions**
- It's a working Figma file with styles, tokens, and components
- It answers: What font size is a heading? What color is a primary button? What's the border radius?
- Without one, you answer those questions differently every time

**What goes in a simple one:**
- Logo + Wordmark
- Type scale (named text styles)
- Color tokens (named color styles)
- Basic UI elements (buttons, inputs, cards)

---

### Slide 9: Logo + Wordmark
**Logo + Wordmark**
Simple beats clever at small sizes

---

### Slide 10: Logo that works at 29px
**Your logo needs to work at 29×29 pixels**
- At small sizes, detail disappears — simple wins
- A wordmark can be your entire logo (Figma, Notion, Linear)
- You need two versions: app icon (square) + horizontal wordmark (nav bar)

**Quick approaches:**
- Lettermark: stylized first letter or initials
- Simple symbol: one recognizable shape
- Wordmark only: distinctive font treatment

> Look at 5 well-known app icons. What makes them work at small sizes?

---

### Slide 11: Sketch your logo
**Sketch 3 quick logo concepts**
1. Grab your notebook
2. Sketch 3 different directions (lettermark, symbol, wordmark)
3. Pick the strongest — you'll refine it in the work session
(2 min)

---

### Slide 12: Type Scale for UI
**Type Scale for UI**
Function over expression

---

### Slide 13: Seven type roles
**Seven roles in a UI type scale**
- **Display** (28–34px) — Feature titles, hero text, onboarding
- **H1** (22–24px) — Screen titles
- **H2** (18–20px) — Section headings
- **Body** (16–17px) — Primary content, descriptions
- **Caption** (13–14px) — Metadata, timestamps
- **Label** (12–13px) — Form labels, tag text
- **Button** (15–16px) — Interactive elements

---

### Slide 14: Setting up text styles (demo)
**Setting up Figma text styles**
1. Create a text style for each role
2. Name them systematically: Display, H1, H2, Body, Caption, Label, Button
3. Set size, weight, line height, letter spacing
4. Change the style once — it updates every instance

**Choosing typefaces:** Test at Caption size first. One family with weight variations is often enough.

> Open Figma. Create 7 text styles using these roles. Pick a typeface and set your sizes. (5 min)

---

### Slide 15: Color Tokens
**Color Tokens for UI**
Color has a job — name it by role, not by color

---

### Slide 16: Color token roles
**Name colors by role, not by hue**
- **Primary** — Main brand color (buttons, active states, links)
- **On Primary** — Text/icons on top of primary (usually white or dark)
- **Surface** — Card and modal backgrounds
- **Background** — App background
- **Text Primary / Text Secondary** — Main text and subdued text
- **Border** — Dividers, input outlines
- **Success / Error / Warning** — Semantic colors

Set these up as Figma color styles. "Primary" not "Blue."

---

### Slide 17: Contrast check
**Accessibility in 30 seconds**
- Text on backgrounds must hit **4.5:1 contrast** (WCAG AA)
- Use WebAIM contrast checker — test every text/background combo
- If it fails, adjust the shade — don't skip the check

> Let's check one live. Pick your primary color — does it pass against white text?

---

### Slide 18: Peer Feedback
**D6 Peer Feedback** (15 min)
1. Form groups of 3 (mix platforms if possible)
2. Each person presents D6 (2 min): What platform? What changed? Why?
3. Group feedback (3 min each): Does it feel native or ported? One specific suggestion.

---

### Slide 19: D7 Assignment
**D7: Design System + 5 Iterations**
Due Monday, Mar 23 @ 5:15pm

**Logo + Wordmark** — App icon version + horizontal wordmark

**Type scale** — 7 Figma text styles, each shown in context on a sample screen

**Color tokens** — All roles defined as Figma color styles, contrast ratios documented

**5 design iterations** — Apply your system to one key screen. Each must be a meaningfully different direction — different typeface, primary color, or layout density. Not 5 minor tweaks.

---

### Slide 20: Next Up
**Next up**
- **Work session (90 min):** Build your design system
  - First 15 min: Logo + wordmark (refine sketch in Figma, test at 29×29)
  - Next 20 min: Type scale (create 7 text styles, choose typeface, test readability)
  - Next 20 min: Color tokens (define all roles, check contrast ratios)
  - Final 35 min: Begin design iterations — apply your system to one key screen
- D7: Design System + 5 Iterations (due Mon, Mar 23 @ 5:15pm)

---

### Slide 21: Resources
**Resources**
- Google Fonts: fonts.google.com
- BYU Graphic Design Type Library
- WebAIM Contrast Checker: webaim.org/resources/contrastchecker
- Type Scale Calculator: typescale.com
- Apple HIG — Typography + Color: developer.apple.com/design/human-interface-guidelines/foundations
- Material Design — Design tokens: m3.material.io/foundations
