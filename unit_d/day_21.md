# Day 21 — Monday, Mar 23
## Unit D: Neue App (Capstone)

**Focus:** Ugly isn't a taste problem — it's a hierarchy problem.

**Why This Matters:** Almost every "this doesn't look good" from a beginner designer is actually one of three things: no visual hierarchy, inconsistent spacing, or too much going on. Today you learn 6 principles that fix 80% of high-fidelity design problems before you even touch color or branding. These are the same things a senior designer would flag in a design review — learn them now and your screens will look professional by the end of the work session.

**Targeted Learning Outcomes:**
- Better Interactions & Experiences
- Critical Analysis of Form and Format
- Familiarity and Distinctiveness
- Design Strategy

---

### Desired Results

**Essential Questions:**
- EQ1: What separates a professional-quality interface from a beginner one?
- EQ2: How do you create visual hierarchy when everything on screen feels equally important?
- EQ3: How do spacing, typography, and color work together to communicate structure?

**Understandings:**
- U1: Most "ugly" designs are actually hierarchy problems — fix the reading order and the design improves dramatically
- U2: Constraint is a design tool — fewer sizes, fewer colors, and more whitespace produce stronger results than adding more
- U3: Spacing communicates relationships (proximity = grouping) — it's not decoration, it's information

**Students Will Know:**
- K1: The 6 high-fidelity craft principles: hierarchy (3 levels), spacing (8pt grid), typography (4 sizes + letter spacing rules), color (60-30-10), alignment (grid discipline), and restraint (subtraction)
- K2: How to self-audit a screen using each principle as a diagnostic question
- K3: The specific values that separate amateur from professional work (8pt increments, -0.02em headline tracking, 4.5:1 contrast ratio, max 3 hierarchy levels)

**Students Will Be Able To:**
- S1: Identify the 3 hierarchy levels (hero, supporting, meta) on any screen — or diagnose their absence
- S2: Audit and fix spacing, type scale, color distribution, and alignment on their own high-fidelity screens
- S3: Apply the "cover test" and restraint principle to remove elements that don't earn their place

---

### Assignments Due
- ⛳ D7: Design System + 5 Iterations (submitted before class)

---

### Activities

1. **Warm-Up: 5 Iterations Gallery Walk** (10 min) `[EQ1, K1]`
   - Lay out your 5 stylistic explorations on your desk or screen
   - Walk around and look at 3–4 classmates' iterations
   - For each person: Which iteration feels most "finished"? What makes it work?
   - Which direction surprised you — something you wouldn't have tried?

2. **Today's Learning Goals** (5 min) `[EQ1, EQ2, EQ3, U1, U2, U3]`
   - **Why this matters:** Today you start building high-fidelity screens from scratch. The difference between student work and professional work isn't talent — it's knowing what to check. Today you learn 6 principles that work as a diagnostic checklist.
   - Preview:
     - 6 principles that fix 80% of high-fidelity design problems
     - Before/after examples showing each principle in action
     - Self-audit: you'll apply every principle to your own screens today
   - Connection to forming/rendering: You've formed the intent — validated the problem, mapped the flow, built the system. Now it's pure rendering. These principles are the craft skills that make rendering excellent.

3. **Direct Instruction: 6 Principles of High-Fidelity Craft** (40 min) `[EQ1, EQ2, EQ3, U1, U2, U3, K1, K2, K3, S1, S2, S3]`

   Open with the big idea: *"Ugly isn't a taste problem. It's a hierarchy problem."* Almost every "this doesn't look good" is actually: no visual hierarchy, inconsistent spacing, or too much going on. Fix those and the design gets 80% better before you touch color.

   **Principle 1: Visual Hierarchy — Only 3 Levels** (7 min)
   - **I do:** Show a before/after — same content, but the "after" has clear hierarchy
     - **Level 1 (Hero):** The most important thing on screen. Big, bold, high contrast.
     - **Level 2 (Supporting):** Secondary info. Medium weight, slightly lower contrast.
     - **Level 3 (Meta):** Labels, timestamps, helper text. Small, muted.
     - Rule: Max 3 levels visible at once. If everything is semibold, nothing is.
   - **I do:** The "pop and un-pop" technique
     - To make text pop (draw attention): increase size, weight, contrast, or color saturation
     - To un-pop (de-emphasize): decrease contrast (lighter color, not grey), smaller size, lighter weight
     - Key insight: big + light = pop. Small + dark = pop. Big + dark = VERY pop (use sparingly)
   - **We do:** Show 2 real app screens. Class calls out: "Where's level 1? Level 2? Level 3?"
   - **You do:** Look at your best D7 iteration. Can you point to your Level 1, 2, and 3 in 3 seconds? If not, mark what needs to change.

   **Principle 2: Spacing Is Communication** (7 min)
   - **I do:** Show the same card with random spacing vs. 8pt grid spacing
     - Things close together = related. Things far apart = separate.
     - The 8pt grid: all spacing in multiples of 8 (8, 16, 24, 32, 48, 64)
     - Inner padding < outer gap. If a card has 24px padding, gap between cards ≥ 24px.
   - **I do:** The beginner gut check — *double whatever spacing feels right*
     - Beginners almost always start too tight
     - Whitespace isn't empty — it's structural. It creates groups, guides the eye, communicates which elements belong together.
     - The *difference* between tight spacing (within a group) and loose spacing (between groups) is what creates perceived hierarchy. If adjacent spacing values are too similar, the grouping is invisible.
   - **We do:** Show a screen with tight spacing. Class suggests: "Where would you add space to create groups?"
   - **You do:** Check your D7 iteration — are you using consistent spacing values? Is there enough difference between inner gaps and outer gaps?

   **Principle 3: Typography — Two Rules That Fix Everything** (7 min)
   - **I do:** Limit your type scale. Pick 4 sizes max. Use them consistently. Don't make up in-between sizes.
     - Display/title: 28–36px
     - Heading: 20–24px
     - Body: 15–16px
     - Label/meta: 11–13px
     - If a size isn't in this scale, it shouldn't exist in your design
   - **I do:** Letter spacing is backwards from what you'd expect
     - Large text (headlines): *tighten* it (−0.02em) — large letters have too much natural space
     - Small all-caps labels: *loosen* it (+0.05em minimum) — letters need room to breathe
     - Body text: zero — don't touch it
   - **I do:** Font weight rules
     - Below 400: never — looks weak, fails contrast
     - 400: body text. 500: buttons. 600: section headers. 700: display headings.
     - Never change weight on hover — causes layout shift. Use color or opacity instead.
   - **We do:** Look at your D7 type scale. Count your sizes. Are there more than 4? Any in-between sizes that don't belong?

   **Principle 4: Color — Constraint Is Strength** (7 min)
   - **I do:** The fewer colors you use, the stronger each one gets
     - 60-30-10 rule:
       - 60% neutral (backgrounds, surfaces)
       - 30% secondary (cards, sidebars)
       - 10% accent — CTAs, key interactions, *nothing else*
     - The scarcity principle: your accent color only works if it's rare. When everything is blue, nothing is blue.
   - **I do:** Contrast matters more than you think
     - Light grey text on white = 2.85:1 contrast → fails accessibility
     - Minimum for body text: 4.5:1 (WCAG AA)
     - `#767676` on white = 4.54:1 → the bare minimum for AA
     - Never use color as the sole indicator of meaning — always pair with icon, label, or pattern
   - **I do:** Neutrals should never be pure grey
     - Warm neutrals (hue 30–40°): human, editorial, craft
     - Cool neutrals (hue 220–240°): technical, precise, developer
     - Pure grey (#808080): dead, institutional — never use
   - **We do:** Look at your D7 color tokens. Estimate: what percentage of your screen is accent color? Is it close to 10%?

   **Principle 5: Alignment — The Grid Is Your Friend** (6 min)
   - **I do:** Every element should be intentionally placed, not "approximately" there
     - Use Figma's auto layout + layout grids
     - If two elements look like they should align, they must *actually* align
     - Consistent horizontal margins (16px minimum on mobile)
   - **I do:** Concentric border radius — a small rule with big impact
     - When nesting elements, outer radius = inner radius + padding
     - Example: button has 12px radius, card has 8px padding → card needs 20px radius
     - Mismatched radii look cheap immediately — this is one of the easiest quality tells
   - **We do:** Audit question — could you draw an invisible vertical line through the left edges of your content? If not, something's misaligned.

   **Principle 6: Restraint Is a Skill** (6 min)
   - **I do:** Beautiful design is mostly subtraction
     - The cover test: cover each element. Does the design lose information or hierarchy without it? If no — remove it.
     - The instinct to add more usually means the core isn't working. When something feels off, beginners add. Experienced designers remove.
   - **I do:** The AI slop checklist — signs your design looks generic
     - Inter or default system fonts everywhere
     - Purple/blue gradient hero on white
     - White cards on grey background with colored accent border
     - Same box-shadow copied everywhere
     - Three-column feature grid
     - The antidote: *specificity*. Ask: what real-world reference already solved this information problem? (Flighty → departure boards. Mela → kitchen context.)
   - **We do:** Look at your best D7 iteration. Is there anything you could remove and lose nothing? Be honest.

4. **D8 Assignment Introduction** (5 min) `[K1, S2]`
   - **D8: High Fidelity Round 1** (due Wed, Apr 1 — bring to Day 24 for in-class critique)
   - What to bring:
     - App icon and logo
     - Style guide with typography and color
     - At least 5 key interaction screens — hand-built in Figma, not AI-generated
   - Use today's 6 principles as your quality checklist before submitting
   - Every screen should pass: hierarchy (3 levels), spacing (8pt grid), type (4 sizes), color (60-30-10), alignment (grid), restraint (cover test)
   - This is rendering intent at its highest — your research formed the intent, now craft the solution

5. **Work Session: Hand-Build High-Fidelity Screens** (60 min) `[EQ1, EQ2, EQ3, U1, U2, U3, K1, K2, K3, S1, S2, S3]`
   - **First 15 min:** Self-audit your best D7 iteration using the 6-principle checklist
     - Walk through each principle as a diagnostic question:
       1. Can I identify Level 1, 2, 3 in 3 seconds?
       2. Is my spacing consistent and on the 8pt grid? Are groups clearly separated?
       3. Am I using 4 type sizes or fewer? Is my letter spacing correct?
       4. Is my accent color at ~10%? Do all text/background combos pass 4.5:1?
       5. Do left edges align? Are my border radii concentric?
       6. Can I remove anything without losing information?
     - Mark everything that needs fixing
   - **Next 45 min:** Build high-fidelity screens
     - Start with your most important screen (the one that demonstrates your core feature)
     - Apply your design system tokens — every color, every text style should come from your system
     - Use auto layout in Figma with 8pt spacing values
     - Goal: 2–3 polished screens by end of class, with the rest in progress
   - Instructor circulates for 1:1 feedback — focusing on hierarchy, spacing, and restraint

**Total: 120 min**

---

### Alignment Check

| Code | Desired Result | Activities |
|------|----------------|------------|
| EQ1 | What separates professional from beginner UI | 1, 2, 3 (all principles), 5 |
| EQ2 | Creating hierarchy when everything feels equal | 2, 3 (P1: hierarchy, P3: type), 5 |
| EQ3 | How spacing, type, and color communicate structure | 2, 3 (P2, P3, P4), 5 |
| U1 | "Ugly" = hierarchy problem | 2, 3 (P1, P6) |
| U2 | Constraint produces stronger results | 3 (P3, P4, P6), 5 |
| U3 | Spacing communicates relationships | 3 (P2), 5 |
| K1 | The 6 craft principles | 3 (all parts) |
| K2 | How to self-audit using each principle | 3 (You do sections), 5 |
| K3 | Specific professional values (8pt, -0.02em, 4.5:1, 3 levels) | 3 (P1, P2, P3, P4) |
| S1 | Identify 3 hierarchy levels on any screen | 3 (P1), 5 |
| S2 | Audit and fix spacing, type, color, alignment | 3, 4, 5 |
| S3 | Apply cover test and restraint | 3 (P6), 5 |

---

### Homework
- ⛳ D8: High Fidelity Round 1 (due Wed, Apr 1 — bring to Day 24 for in-class critique)
  - App icon and logo
  - Style guide with typography and color
  - At least 5 key interaction screens — hand-built in Figma
  - Use the 6-principle checklist before submitting
  - Submit: Figma link to Learning Suite

---

### Resources
- UI Design Principles reference: `docs/principles.md`
- WebAIM Contrast Checker: https://webaim.org/resources/contrastchecker/
- Figma Auto Layout guide: https://help.figma.com/hc/en-us/articles/5731482952599-Using-auto-layout
- Type Scale Calculator: https://typescale.com/
