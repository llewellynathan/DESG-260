# Day 11 — Tuesday, Feb 17
## Unit C: Hierarchy & Responsive Web

**Focus:** Grids are invisible scaffolding — they create consistency and speed up every design decision.

**Targeted Learning Outcomes:**
- Better Interactions & Experiences
- Critical Analysis of Form and Format
- Design Strategy

---

### Desired Results

**Essential Questions:**
- EQ1: How do grids enable both consistency and flexibility?
- EQ2: What's the difference between designing for mobile-first vs. desktop-first?
- EQ3: How do constraints (like grid systems) actually speed up design decisions?

**Understandings:**
- U1: Grids create consistency and enable faster, more confident design decisions
- U2: Responsive design requires thinking in systems, not fixed layouts
- U3: The same content can be arranged differently across breakpoints while maintaining coherence

**Students Will Know:**
- K1: The box model (content, padding, border, margin) and how element size is calculated
- K2: How to set up and use layout grids in Figma (columns, margins, gutters)
- K3: The 4px increment system for consistent spacing (implicit grid)
- K4: Common grid patterns for mobile and desktop (4-column mobile, 12-column desktop)
- K5: How Figma auto-layout maps to the box model (padding yes, margin no, gap instead)
- K6: What makes an effective wireframe (clarity, hierarchy, no distracting details)

**Students Will Be Able To:**
- S1: Create responsive frames in Figma with proper grid setup
- S2: Design a layout that works across mobile and desktop breakpoints
- S3: Align elements consistently using grid and auto-layout

---

### Assignments Due
- ⛳ C2: Type Hierarchy (due before class)
- PDP rough wireframes (paper or digital sketches)

---

### Activities

1. **Warm-Up: Grid Detective** (10 min) `[EQ1, U1, K2]`
   - Prompt on screen: "Open a well-designed website. Can you find the grid? How many columns? Where are the margins?"
   - Students screenshot and annotate with grid overlay guesses
   - Quick share: 2-3 examples — what patterns emerge?

2. **Today's Learning Goals** (5 min) `[EQ1, EQ2, EQ3, U1, U2, U3]`
   - Today we're adding structure to your PDP: grids and responsive frames
   - Connection to forming/rendering: grids are how we *render* consistency — they're the invisible system that makes designs feel intentional
   - By end of class: your PDP will have proper grid setup for both mobile and desktop

3. **Direct Instruction: Grid Systems in Figma** (30 min) `[K1, K2, K3, K5, U1, U2, S1, S3]`
   - **I do:** The Box Model — see everything as a box
     - Every element is a box with: content, padding, border, margin (inside → outside)
     - Total element width = content + padding + border (margin is spacing, not size)
     - **Margin vs. padding rule:** When backgrounds differ, use both; when backgrounds match, consolidate into padding
     - Tip: Developers use debug borders to visualize boxes — you can think this way too
   - **I do:** Auto-Layout and the Box Model
     - Figma auto-layout is NOT the same as the CSS box model — it's closer to CSS Flexbox
     - **What auto-layout HAS:**
       - Padding (internal spacing inside a frame) — same as CSS
       - Gap (spacing between child elements) — like CSS Flexbox gap
     - **What auto-layout DOESN'T have:**
       - Margin (external spacing around a frame)
     - **Key difference:** Gap only creates space BETWEEN children, not on the outside edges
     - **Practical tip:** To add space around an auto-layout frame, wrap it in a parent frame and use that parent's padding
     - Demo: Show padding vs. gap in a simple auto-layout frame
   - **I do:** Explain grid fundamentals
     - **Explicit grid:** columns, gutters, margins — the visible structure
     - **Implicit grid:** the spacing rhythm between all elements (the "clean" feel)
     - **4px increment rule:** Use 4, 8, 12, 16, 20, 24... for all spacing decisions
       - Why 4px? Divides evenly, aligns with browser defaults
       - Even numbers divide cleanly; avoid 5px or 10px increments
     - Common patterns: 4-column mobile, 12-column desktop
     - Vignelli's perspective: "The grid is an attitude"
   - **I do:** Demo setting up grids in Figma
     - Create desktop frame (1440px) with 12-column grid
     - Create mobile frame (375px) with 4-column grid
     - Show how same content aligns to different grids
   - **We do:** Build and place a product card
     - First, create a simple product card together (image placeholder, title, price)
     - Then experiment with placing it on both grids:
       - Desktop: try spanning 3 or 4 columns
       - Mobile: try full width or 2 columns side-by-side
     - Discuss: what changed? What stayed the same?
   - **You do:** Students set up grids on their own PDP frames (5 min)

4. **Introduce C3: Mobile + Desktop Wireframes** (15 min) `[S2, U2, U3, K6]`
   - **I do:** What makes an effective wireframe
     - Clarity: Can someone understand the layout at a glance?
     - Hierarchy: Is it obvious what's most important?
     - No distracting details: Use boxes and text labels, not real content
     - Wireframes separate structure decisions from visual decisions
     - Show example: cluttered wireframe vs. clear wireframe
   - **Due: Wed, Feb 18 @ 11:59pm**
   - Requirements:
     - Simple wireframes for both mobile and desktop PDP
     - Show: product title + details, image placements, button placements, page layout
     - Focus on structure, not visual polish
   - These wireframes become the foundation for high-fidelity work
   - Reminder: same content, different arrangement — let the grid guide you

5. **Work Session: Grid Setup + Wireframes** (60 min) `[S1, S2, S3, EQ2, EQ3]`
   - **Priority 1:** Set up Figma frames with proper grids (mobile + desktop)
   - **Priority 2:** Complete C3 wireframes (due Wed @ 11:59pm)
   - **Priority 3:** Begin placing content from C1 into wireframe structure
   - Instructor circulates for 1:1 feedback:
     - Are grids set up correctly? (columns, margins, gutters)
     - Does content align to the grid?
     - Does the mobile layout make sense for thumb-zone navigation?
     - Is the hierarchy clear in the wireframe?

**Total: 120 min** (Monday schedule on Tuesday due to Presidents' Day)

---

### Homework
- Continue C3: Mobile + Desktop Wireframes (due Wed, Feb 18 @ 11:59pm)
- Begin high-fidelity PDP designs

---

### Resources
- [Box Model reference](resources/box-model.md) — see everything as a box
- [Implicit Grid reference](resources/implicit-grid.md) — the 4px increment system
- Vignelli Canon: Grids (p. 40 of PDF)
- Using grids in Figma: YouTube tutorial
- Figma: Layout Grids documentation

---

### Alignment Check

| Code | Desired Result | Activities |
|------|----------------|------------|
| EQ1 | How do grids enable consistency and flexibility? | 1, 2, 3 |
| EQ2 | Mobile-first vs. desktop-first? | 2, 5 |
| EQ3 | How do constraints speed up decisions? | 2, 3, 5 |
| U1 | Grids create consistency | 1, 3 |
| U2 | Responsive = thinking in systems | 3, 4 |
| U3 | Same content, different arrangement | 3, 4 |
| K1 | Box model and element size calculation | 3 |
| K2 | Layout grids in Figma | 3 |
| K3 | 4px increment system (implicit grid) | 3 |
| K4 | Common grid patterns | 1, 3 |
| K5 | Auto-layout maps to box model | 3 |
| K6 | What makes an effective wireframe | 4 |
| S1 | Create responsive frames with grids | 3, 5 |
| S2 | Design for mobile and desktop | 4, 5 |
| S3 | Align elements using grid | 3, 5 |
