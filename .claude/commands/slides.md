---
description: Generate a presentation outline from a lesson plan
allowed-tools: Read, Glob
---

**Usage:** `/slides [day number]` (e.g., `/slides 1`, `/slides 14`)

Generate a slide-by-slide presentation outline for Day $ARGUMENTS of DESG 260.

## Context Files to Read

1. **Determine the unit folder based on day number:**
   - Days 1-4 → `unit_a/`
   - Days 5-8 → `unit_b/`
   - Days 9-13 → `unit_c/`
   - Days 14-24 → `unit_d/`
   - Days 25-27 → `unit_e/`

2. **Read the lesson plan file** at `unit_X/day_XX.md` (use two-digit format)

## Slide Structure Rules

Generate slides in this order:

### 1. Title Slide
- Day number, weekday, and date
- Unit letter and name

### 2. Focus Slide
- The one-line focus statement from the lesson plan

### 3. Desired Results Slides (one slide per category)

**Essential Questions slide**
- All EQs listed together (without EQ# codes)

**Understandings slide**
- All understandings listed (without U# codes)

**Students Will Know slide**
- All knowledge items listed (without K# codes)

**Students Will Be Able To slide**
- All skills listed (without S# codes)

### 4. Activity Slides
For each activity in the lesson plan, determine complexity:

**Simple activity** (1 slide): Activity has ≤3 bullet points, no sub-lists, no discussion prompts
- Single slide with activity name, time, and brief description

**Complex activity** (multiple slides): Activity has setup instructions, multi-step processes, OR discussion/debrief prompts
- **Activity Title slide**: Name and time only
- **Setup slide** (if has materials or setup): Materials needed, how to arrange
- **Instructions slide** (if has numbered steps): Step-by-step process
- **Discussion/Debrief slide** (if has discussion prompts): Questions for class discussion

### 5. Homework Slide
- All homework items with their symbols (📚, ⛳, 🚩)

### 6. Resources Slide (if resources exist)
- Links and references from the Resources section

## Output Format

Use this exact markdown format with `---` as slide separators:

```markdown
# Day X Presentation Outline
## Unit [Letter]: [Name]

---

### Slide 1: Title
**Day X — [Weekday], [Date]**
Unit [Letter]: [Name]

---

### Slide 2: Today's Focus
[Focus statement]

---

### Slide 3: Essential Questions
- [EQ1 text without code]
- [EQ2 text without code]

---

### Slide 4: Understandings
- [U1 text without code]
- [U2 text without code]

---

### Slide 5: Students Will Know
- [K1 text without code]
- [K2 text without code]

---

### Slide 6: Students Will Be Able To
- [S1 text without code]
- [S2 text without code]

---

### Slide 7: Activity — [Name]
**[Activity Name]** ([X] min)

---

[Continue with appropriate slides for each activity...]

---

### Slide N: Homework
- 📚 [Reading]
- ⛳ [Checkpoint]
- 🚩 [Major assignment]

---

### Slide N+1: Resources
- [Resource 1]
- [Resource 2]
```

## Important Notes

- Number slides sequentially (Slide 1, Slide 2, etc.)
- Remove alignment codes like `[EQ1, U2]` from activity names
- Keep bullet points concise — these are slide prompts, not full scripts
- Discussion prompts should be framed as questions students will discuss
- Total slide count will vary based on activity complexity
