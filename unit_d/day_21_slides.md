# Day 21 Presentation Outline
## Unit D: Neue App (Capstone)

---

### Slide 1: Warm-Up
**Warm-Up: 5 Iterations Gallery Walk** (10 min)
- Lay out your 5 stylistic explorations on your desk or screen
- Walk around and look at 3–4 classmates' iterations
- For each person: Which iteration feels most "finished"? What makes it work?
- Which direction surprised you — something you wouldn't have tried?

---

### Slide 2: Prayer
**Prayer**
Mira, will you pray for us today?

---

### Slide 3: Title
**Unit D: Neue App**
Ugly isn't a taste problem — it's a hierarchy problem.

---

### Slide 4: Today
**Today**
- D7 gallery walk
- 6 principles of high-fidelity craft
- Self-audit your screens
- Hand-build high-fidelity screens in Figma

---

### Slide 5: By the end of today...
**Visual hierarchy** — You'll be able to identify (or diagnose the absence of) 3 clear reading levels on any screen

**The craft checklist** — You'll know 6 specific principles that fix the most common high-fidelity design mistakes — spacing, type, color, alignment, and restraint

**Self-audit skill** — You'll be able to look at your own screen and know exactly what's wrong and how to fix it, using diagnostic questions instead of guessing

---

### Slide 6: Why This Matters
**Why this matters**
Almost every "this doesn't look good" is actually one of three things: no visual hierarchy, inconsistent spacing, or too much going on.

Fix those and the design gets 80% better — before you even touch color or branding.

Today you learn the same things a senior designer would flag in a design review. These aren't opinions — they're craft skills with specific, checkable values.

---

### Slide 7: The Big Idea
**"Ugly isn't a taste problem. It's a hierarchy problem."**

The difference between student work and professional work isn't talent — it's knowing what to check.

6 principles. Each one is a diagnostic question you can ask of any screen.

---

### Slide 8: Principle 1 — Visual Hierarchy
**Only 3 levels at a time**
- **Level 1 (Hero):** The most important thing on screen. Big, bold, high contrast.
- **Level 2 (Supporting):** Secondary info. Medium weight, slightly lower contrast.
- **Level 3 (Meta):** Labels, timestamps, helper text. Small, muted.

Rule: If everything is semibold, nothing is.

**Pop and un-pop:**
- To pop: increase size, weight, contrast, or saturation
- To un-pop: lighter color (not grey), smaller size, lighter weight
- Key insight: big + light = pop. Small + dark = pop. Big + dark = VERY pop (use sparingly).

> Show 2 real app screens. Class calls out: "Where's Level 1? Level 2? Level 3?"

---

### Slide 9: You do — Hierarchy
**Check your D7 iteration**
1. Open your best D7 iteration
2. Can you point to your Level 1, 2, and 3 in 3 seconds?
3. If not, mark what needs to change

---

### Slide 10: Principle 2 — Spacing
**Spacing is communication**
- Things close together = related. Things far apart = separate.
- **8pt grid:** All spacing in multiples of 8 (8, 16, 24, 32, 48, 64)
- Inner padding < outer gap. Card has 24px padding → gap between cards ≥ 24px.

**The beginner gut check:** Double whatever spacing feels right. Beginners almost always start too tight.

Whitespace isn't empty — it's structural. The *difference* between tight spacing (within a group) and loose spacing (between groups) is what creates perceived grouping. If adjacent values are too similar, the grouping is invisible.

> Show a screen with tight spacing. "Where would you add space to create groups?"

---

### Slide 11: Principle 3 — Typography
**Two rules that fix everything**

**Rule 1: Limit your scale.** 4 sizes max. Don't make up in-between sizes.
- Display/title: 28–36px
- Heading: 20–24px
- Body: 15–16px
- Label/meta: 11–13px

**Rule 2: Letter spacing is backwards from what you'd expect.**
- Large text (headlines): *tighten* it (−0.02em)
- Small all-caps labels: *loosen* it (+0.05em minimum)
- Body text: zero — don't touch it

Font weight: Below 400 = never. 400 = body. 500 = buttons. 600 = headers. 700 = display.

> Look at your D7 type scale. Count your sizes. More than 4? Any in-between sizes that don't belong?

---

### Slide 12: Principle 4 — Color
**Constraint is strength**

**60-30-10 rule:**
- 60% neutral (backgrounds, surfaces)
- 30% secondary (cards, sidebars)
- 10% accent — CTAs, key interactions, *nothing else*

Your accent color only works if it's rare. When everything is blue, nothing is blue.

**Contrast:** Light grey on white = 2.85:1 → fails. Body text needs 4.5:1 minimum (WCAG AA). Check every text/background combo.

**Neutrals:** Never pure grey. Warm (hue 30–40°) = human, editorial. Cool (hue 220–240°) = technical, precise. Pure grey = dead.

> Look at your D7 color tokens. What percentage of your screen is accent color? Is it close to 10%?

---

### Slide 13: Principle 5 — Alignment
**The grid is your friend**
- Every element should be *intentionally* placed, not "approximately" there
- Use Figma's auto layout + layout grids
- If two elements look like they should align, they must actually align
- Consistent horizontal margins (16px minimum on mobile)

**Concentric border radius** — a small rule with big impact:
- Outer radius = inner radius + padding
- Button has 12px radius + card has 8px padding → card needs 20px radius
- Mismatched radii look cheap immediately

> Could you draw an invisible vertical line through the left edges of your content? If not, fix it.

---

### Slide 14: Principle 6 — Restraint
**Beautiful design is mostly subtraction**

**The cover test:** Cover each element. Does the design lose information or hierarchy without it? If no — remove it.

When something feels off, beginners add. Experienced designers remove.

**The AI slop checklist** — signs your design looks generic:
- Inter or system fonts everywhere, no variation
- Purple/blue gradient hero on white
- White cards on grey background with colored accent border
- Same box-shadow copied everywhere
- Three-column feature grid

The antidote is *specificity*. What real-world reference already solved this information problem? (Flighty → departure boards. Mela → kitchen context.)

> Look at your best D7 iteration. Is there anything you could remove and lose nothing?

---

### Slide 15: The 6-Principle Checklist
**Your self-audit checklist**
1. **Hierarchy** — Can I identify Level 1, 2, 3 in 3 seconds?
2. **Spacing** — Am I on the 8pt grid? Are groups clearly separated?
3. **Typography** — 4 sizes or fewer? Letter spacing correct?
4. **Color** — Accent at ~10%? All text/background combos pass 4.5:1?
5. **Alignment** — Left edges align? Border radii concentric?
6. **Restraint** — Can I remove anything without losing information?

Every screen you build should pass all 6.

---

### Slide 16: Next Up
**Next up**
- **Work session (60 min):** First 15 min — self-audit your best D7 iteration using the checklist. Then hand-build high-fidelity screens starting with your most important screen. Goal: 2–3 polished screens by end of class.
- Use auto layout in Figma with 8pt spacing values
- Every color and text style should come from your design system
- D8: High Fidelity Round 1 (due Wed, Apr 1 — bring to Day 24 for critique)
  - App icon and logo
  - Style guide with typography and color
  - At least 5 key interaction screens — hand-built in Figma
