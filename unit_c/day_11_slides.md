# Day 11 Presentation Outline
## Unit C: Hierarchy & Responsive Web

---

### Slide 1: Warm-Up
**Warm-Up: Learn About Visual Rhythm** (10 min)
1. Open Claude or ChatGPT
2. Send this prompt: "I want to learn about visual rhythm and spacing in design. Can you break this topic down into the main sub-topics I should understand?"
3. Then follow up with: "Let's start with just one of those. What's the first thing I should learn? Please explain it to me, including why it is important, and provide me with trusted resources for digging deeper."
4. Be ready to share what you learned

---

### Slide 2: Prayer
**Prayer**
Mira, will you pray for us today?

---

### Slide 3: Title
**Unit C: Hierarchy & Responsive Web**
Grids are invisible scaffolding — the system that makes designs feel intentional.

---

### Slide 4: Today
**Today**
- Visual rhythm share-out
- Grid systems in Figma
- Introduce C3: Mobile + Desktop Wireframes
- Work session: Grid setup + wireframes

---

### Slide 5: Why This Matters
**Why this matters**
Without grids, you're guessing. Every spacing decision becomes a debate with yourself.

Grids reduce the amount of decision-making you have to do about layout. That's how professionals work fast without sacrificing quality.

---

### Slide 6: By the end of today...
**Grid fundamentals** — You'll understand the box model, how auto-layout relates to it, and the 4px spacing system

**Figma grids** — You'll set up proper layout grids for both mobile (4-column) and desktop (12-column) frames

**Responsive thinking** — You'll see how the same content adapts across breakpoints while staying consistent

---

### Slide 7: Grid Systems in Figma
**Grid Systems**
The invisible structure behind every good design

---

### Slide 8: The Box Model
**Every element is a box**
- Content → Padding → Border → Margin (inside to outside)
- Total width = content + padding + border
- Margin is spacing *between* boxes, not part of the box itself

> Developers use debug borders to visualize boxes — you can think this way too.

---

### Slide 9: Margin vs. Padding
**When to use which?**
- **Different backgrounds** → Use both (margin creates gap, padding creates internal space)
- **Same backgrounds** → Consolidate into padding

---

### Slide 10: Auto-Layout ≠ Box Model
**Figma auto-layout is NOT the CSS box model**
It's closer to CSS Flexbox.

- **Has padding** — internal spacing inside frames ✓
- **Has gap** — spacing between child elements ✓
- **No margin** — no external spacing property

---

### Slide 11: Gap vs. Margin
**Gap only creates space BETWEEN children**

- Margin: space on ALL sides of each element (including outer edges)
- Gap: space only BETWEEN siblings (not on outer edges)

> To add space around an auto-layout frame, wrap it in a parent and use padding.

---

### Slide 12: Explicit vs. Implicit Grid
**Two types of grid**
- **Explicit grid:** Columns, gutters, margins — the visible structure you set up
- **Implicit grid:** The spacing rhythm between *all* elements — what creates the "clean" feel

---

### Slide 13: The 4px Rule
**Use 4px increments for all spacing**
4, 8, 12, 16, 20, 24, 32, 40, 48...

- Why 4px? Divides evenly, aligns with browser defaults
- Even numbers divide cleanly
- Avoid 5px or 10px increments

> Vignelli: "The grid is an attitude."

---

### Slide 14: Common Grid Patterns
**Standard setups**
- **Mobile:** 4 columns (375px frame)
- **Desktop:** 12 columns (1440px frame)

Same content, different column spans.

---

### Slide 15: Demo — Setting Up Grids
**Watch: Figma grid setup**
1. Create desktop frame (1440px) with 12-column grid
2. Create mobile frame (375px) with 4-column grid
3. See how same content aligns to different grids

---

### Slide 16: Let's Try Together
**Place a product card on both grids**
- Desktop: card spans 4 columns
- Mobile: card spans full width

> What changed? What stayed the same?

---

### Slide 17: Your Turn
**Set up grids on your PDP frames** (5 min)
1. Create or select your desktop frame (1440px)
2. Add a 12-column layout grid
3. Create or select your mobile frame (375px)
4. Add a 4-column layout grid

---

### Slide 18: C3 — Mobile + Desktop Wireframes
**Due: Wednesday, Feb 18 @ 11:59pm**
- Simple wireframes for both mobile AND desktop PDP
- Show: product title + details, image placements, button placements, page layout
- Focus on structure, not visual polish

These wireframes become the foundation for your high-fidelity work.

> Same content, different arrangement — let the grid guide you.

---

### Slide 19: Next Up
**Next up**
- Work session: Set up grids, then start C3 wireframes
- Get feedback on grid setup and content alignment
- Think about thumb-zone navigation for mobile

**Homework:**
- C3: Mobile + Desktop Wireframes (due Wed @ 11:59pm)
- Begin high-fidelity PDP designs
