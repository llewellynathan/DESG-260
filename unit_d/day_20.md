# Day 20 — Wednesday, Mar 18
## Unit D: Neue App (Capstone)

**Focus:** A design system is the toolkit you build before you build the product.

**Why This Matters:** Starting Day 21, you'll hand-build every screen in Figma from scratch. Without a design system, you'll make hundreds of one-off decisions — picking colors by eye, guessing font sizes, rebuilding the same button five different ways. A simple design system (logo, wordmark, type scale, color tokens, basic components) eliminates those decisions upfront. Every professional UI team builds one before touching a single screen. Today you build yours.

**Targeted Learning Outcomes:**
- Critical Analysis of Form and Format
- Design Strategy
- Familiarity and Distinctiveness
- Better Interactions & Experiences

---

### Desired Results

**Essential Questions:**
- EQ1: What is a design system and why do UI designers build one before designing screens?
- EQ2: How do you set up typography, color, and components in Figma so they work as a connected system?
- EQ3: How simple can a logo and wordmark be while still being effective?

**Understandings:**
- U1: A design system is not a style guide — it's a set of reusable decisions that make every subsequent design faster and more consistent
- U2: Typography hierarchy in UI is about function (scannability, readability, interaction) more than expression
- U3: Color in UI serves meaning (primary actions, surfaces, errors, success) — not just brand personality

**Students Will Know:**
- K1: The components of a simple UI design system (logo, wordmark, type scale, color tokens, basic UI elements)
- K2: How to set up Figma text styles and color styles as reusable tokens
- K3: How to create a simple logo and wordmark that's functional at small sizes

**Students Will Be Able To:**
- S1: Create a simple logo and wordmark appropriate for an app icon and navigation bar
- S2: Build a type scale in Figma with named text styles (Display, H1, H2, Body, Caption, Label, Button)
- S3: Define a color token system (primary, surface, text, border, semantic colors) with accessible contrast
- S4: Produce 5 design iterations showing different visual directions for their app

---

### Assignments Due
- ⛳ D6: Second Platform Flow + Sketches (submitted before class)

---

### Activities

1. **Warm-Up: D6 Second Platform Gallery** (10 min) `[EQ1]`
   - Lay out your D6 submissions on your desk or screen
   - Walk around and look at 3–4 classmates' second platform designs
   - For each: What platform did they choose? What's the most interesting adaptation?
   - Find someone who chose a different platform than you — compare notes

2. **Today's Learning Goals** (5 min) `[EQ1, EQ2, EQ3, U1, U2, U3]`
   - **Why this matters:** Day 21, you build screens from scratch. Today you build the system that makes that work 10x faster. Without it, you'll spend hours making inconsistent decisions.
   - Preview:
     - What a UI design system is (and isn't)
     - Logo + wordmark: simple, functional, done
     - Type scale: setting up Figma text styles
     - Color tokens: defining your palette as a system
     - D6 peer feedback
   - Connection to forming/rendering: Your research formed the intent. Now you're building the rendering toolkit — the set of reusable decisions that will shape every screen.

3. **Direct Instruction: Building a UI Design System** (50 min) `[EQ1, EQ2, EQ3, U1, U2, U3, K1, K2, K3, S1, S2, S3]`

   **Part A: What Is a Design System?** (8 min)
   - **I do:** A design system is a set of reusable decisions
     - It's not a pretty PDF — it's a working Figma file with styles, tokens, and components
     - It answers: "What font size is a heading? What color is a primary button? What's the border radius?"
     - Without one, you answer those questions differently every time you design a new screen
   - **I do:** What goes in a simple UI design system
     - **Logo + Wordmark** — App icon, nav bar logo (simple and functional)
     - **Type scale** — Named text styles with sizes, weights, line heights
     - **Color tokens** — Named colors with roles (primary, surface, text, semantic)
     - **Basic UI elements** — Buttons, inputs, cards built from your tokens
   - **I do:** Show a real design system in Figma (Apple HIG Figma kit or Material Design kit)
     - Point out: text styles panel, color styles panel, component library
     - "You're building a small version of this today"

   **Part B: Logo + Wordmark** (10 min)
   - **I do:** Your logo needs to work at 29×29 pixels (app icon smallest size)
     - Simple beats clever — at small sizes, detail disappears
     - A strong wordmark can be your entire logo (think: Figma, Notion, Linear)
     - You need: app icon version + horizontal wordmark for nav bars
   - **I do:** Quick approaches that work
     - Lettermark: stylized first letter or initials
     - Simple symbol: one recognizable shape
     - Wordmark only: distinctive font treatment of your app name
     - Avoid: gradients that flatten at small size, thin lines that disappear, excessive detail
   - **We do:** Look at 5 well-known app icons. What makes them work at small sizes? What's the simplest element?
   - **You do:** Sketch 3 quick logo concepts in your notebook (2 min). Pick your strongest one — you'll refine it in the work session.

   **Part C: Type Scale for UI** (15 min)
   - **I do:** UI typography is about function, not expression
     - **Display** (28–34px) — Feature titles, hero text, onboarding
     - **H1** (22–24px) — Screen titles
     - **H2** (18–20px) — Section headings
     - **Body** (16–17px) — Primary content, descriptions
     - **Caption** (13–14px) — Metadata, timestamps, secondary info
     - **Label** (12–13px) — Form labels, tag text
     - **Button** (15–16px) — Interactive elements, medium weight
   - **I do:** Setting up text styles in Figma (live demo)
     - Create a text style for each role
     - Name them systematically: Display, H1, H2, Body, Caption, Label, Button
     - Set size, weight, line height, and letter spacing for each
     - Show how changing a text style updates every instance
   - **I do:** Choosing typefaces for UI
     - Readability at small sizes is non-negotiable — test at Caption size first
     - One typeface family is often enough for UI (use weight variations instead of pairing)
     - If you pair: one for headings (personality), one for body (readability)
     - Google Fonts and the BYU Type Library are your resources
   - **You do:** Open Figma. Create 7 text styles using the roles above. Pick a typeface and set your sizes. (5 min)

   **Part D: Color Tokens for UI** (17 min)
   - **I do:** Color in UI has a job — it's not just decoration
     - **Primary** — Your main brand color. Used for primary buttons, active states, links.
     - **On Primary** — Text/icons that sit on top of your primary color (usually white or dark)
     - **Surface** — Background of cards, sheets, modals (light or dark)
     - **Background** — App background (usually slightly different from surface)
     - **Text Primary** — Main body text color
     - **Text Secondary** — Captions, placeholders, less important text
     - **Border** — Dividers, input outlines
     - **Success / Error / Warning** — Semantic colors (green, red, amber)
   - **I do:** Setting up color styles in Figma (live demo)
     - Create a color style for each token
     - Name them by role, not by color: "Primary" not "Blue," "Error" not "Red"
     - Show how changing a color style propagates everywhere
   - **I do:** Accessibility in 30 seconds
     - Text on backgrounds must hit 4.5:1 contrast ratio (WCAG AA)
     - Use WebAIM contrast checker — test every text/background combination
     - If it fails, adjust the shade — don't skip the check
   - **We do:** Check contrast — instructor picks a student's primary color, tests it against white and dark text live. Does it pass?
   - **You do:** Pick your primary color. Test it against white text and against your intended background color using the WebAIM contrast checker. Adjust if needed. (3 min)

4. **D6 Peer Feedback** (15 min) `[EQ1]`
   - Groups of 3 (mix platforms if possible)
   - Each person presents D6 (2 min): What platform? What changed? Why?
   - Group feedback (3 min per person):
     - Does the second platform feel native or ported?
     - One specific suggestion for improvement

5. **D7 Assignment Introduction** (10 min) `[K1, S2, S3, S4]`
   - **D7: Design System + 5 Iterations** (due Mon, Mar 23 @ 5:15pm)
   - **Logo + Wordmark:**
     - App icon version (square, works at small sizes)
     - Horizontal wordmark for nav bars
   - **Type scale:**
     - Figma text styles for all 7 roles (Display, H1, H2, Body, Caption, Label, Button)
     - Show each level in context on a sample screen
   - **Color tokens:**
     - Primary, On Primary, Surface, Background, Text Primary, Text Secondary, Border
     - Semantic: Success, Error, Warning
     - Contrast ratios documented for text on backgrounds
   - **5 design iterations:**
     - Apply your design system to one key screen from your app
     - Each iteration should explore a meaningfully different direction — different typeface, different primary color, different layout density
     - Not 5 minor tweaks — 5 genuinely different visual approaches
   - Submit: PDF to Learning Suite

6. **Work Session: Build Your Design System** (90 min) `[EQ1, EQ2, EQ3, U1, U2, U3, K1, K2, K3, S1, S2, S3, S4]`
   - **First 15 min:** Logo + wordmark
     - Refine your strongest sketch concept in Figma or Illustrator
     - Test at app icon size (60×60 and 29×29) — does it still read?
     - Create a horizontal wordmark version
   - **Next 20 min:** Type scale setup
     - Choose your typeface(s) from Google Fonts or BYU Type Library
     - Create all 7 text styles in Figma with proper naming
     - Test readability: does your Caption size work? Is your Display size impactful?
   - **Next 20 min:** Color token setup
     - Define all color tokens as Figma color styles
     - Test contrast ratios for every text/background combination
     - Set up semantic colors (success, error, warning)
   - **Final 35 min:** Begin design iterations
     - Apply your system to one key screen
     - Build at least 2 different directions — push for variety
     - Try changing your primary color, your typeface, or your layout density between iterations
   - Instructor circulates for 1:1 feedback on type choices, color tokens, and logo refinement

**Total: 180 min**

---

### Alignment Check

| Code | Desired Result | Activities |
|------|----------------|------------|
| EQ1 | What is a design system and why build one | 2, 3A, 4 |
| EQ2 | Setting up type, color, components in Figma | 2, 3C, 3D, 6 |
| EQ3 | How simple can a logo be and still work | 3B, 6 |
| U1 | Design system = reusable decisions | 2, 3A |
| U2 | UI type is about function over expression | 3C, 6 |
| U3 | UI color serves meaning, not just personality | 3D, 6 |
| K1 | Components of a simple design system | 3A, 5 |
| K2 | Figma text styles and color styles | 3C, 3D, 6 |
| K3 | Creating a functional logo at small sizes | 3B, 6 |
| S1 | Create logo + wordmark for app icon and nav | 3B, 6 |
| S2 | Build type scale with named Figma text styles | 3C, 5, 6 |
| S3 | Define color tokens with accessible contrast | 3D, 5, 6 |
| S4 | Produce genuinely different design iterations | 5, 6 |

---

### Homework
- ⛳ D7: Design System + 5 Iterations (due Mon, Mar 23 @ 5:15pm)
  - Logo + wordmark (app icon + horizontal version)
  - Type scale (7 Figma text styles shown in context)
  - Color tokens (all roles defined, contrast ratios documented)
  - 5 design iterations of one key screen showing genuine visual exploration
  - Submit: PDF to Learning Suite

---

### Resources
- Google Fonts: https://fonts.google.com/
- BYU Graphic Design Type Library
- WebAIM Contrast Checker: https://webaim.org/resources/contrastchecker/
- Type Scale Calculator: https://typescale.com/
- Apple HIG — Foundations (Typography, Color): https://developer.apple.com/design/human-interface-guidelines/foundations
- Material Design — Design tokens: https://m3.material.io/foundations
