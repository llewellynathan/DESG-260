---
description: Generate a presentation outline from a lesson plan
allowed-tools: Read, Glob, Write
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

**Key principle:** The Warm-Up is the first thing students see when entering class. Title and preview come after, then remaining activities follow.

Generate slides in this order:

### 1. Warm-Up Slide
- Pull from Activity 1 (Warm-Up) in the lesson plan
- This is what students see immediately when they enter — they can start working right away
- Include the activity name and instructions

### 2. Title Slide
- Day number, weekday, and date
- Unit letter and name
- **Big Idea:** A single memorable statement distilled from the Focus section — what students should take away

### 3. Today's Activities Slide
- **Today:** List the main activities in order, separated by arrows (→)
- This previews what the class will cover

### 4. Activity Slides
For each activity in the lesson plan (starting from Activity 2, since Warm-Up is Slide 1), create slides based on its content:

**Simple activity** (1 slide): Activity has ≤3 bullet points, no sub-lists, no discussion prompts
- Single slide with activity name, time, and brief description

**Complex activity** (multiple slides): Activity has setup instructions, multi-step processes, OR discussion/debrief prompts
- **Activity Title slide**: Name and time only
- **Content slides**: Break down the activity's bullet points into logical slides
- **Discussion slide** (if has discussion prompts): Questions for class discussion
- **Reveal slide** (if instructor shares a definition or answer after discussion): The instructor's key point

**Pulling in Desired Results:** If an activity references learning goals, EQs, or objectives (e.g., "Display Essential Questions", "Today's Learning Goals"), include ALL Desired Results at that point — each category on a separate slide:
- Essential Questions slide
- Understandings slide
- Students Will Know slide
- Students Will Be Able To slide

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

### Slide 1: Warm-Up
**Warm-Up: [Specific Activity]** (10 min)
- [Instruction 1]
- [Instruction 2]
- [Instruction 3]

---

### Slide 2: Title
**Day X — [Weekday], [Date]**
Unit [Letter]: [Name]

**Big Idea:** [Single memorable takeaway from Focus section]

---

### Slide 3: Today's Activities
**Today:** [Activity 2] → [Activity 3] → [Activity 4] → ...

---

### Slide 4: [Activity 2 Name]
**[Activity Name]** ([X] min)
[Activity content...]

---

[Continue with slides following the Activities sequence...]

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

## Save Output

After generating the slides, save the output to a file:

1. **File location:** Same unit folder as the lesson plan
2. **File name:** `day_XX_slides.md` (use two-digit format matching the lesson plan)

Examples:
- Day 1 slides → `unit_a/day_01_slides.md`
- Day 7 slides → `unit_b/day_07_slides.md`
- Day 14 slides → `unit_d/day_14_slides.md`

## Important Notes

- Number slides sequentially (Slide 1, Slide 2, etc.)
- Remove alignment codes like `[EQ1, U2]` from activity names
- Keep bullet points concise — these are slide prompts, not full scripts
- Discussion prompts should be framed as questions students will discuss
- Include instructor definitions/answers on separate "reveal" slides after discussion prompts
- Total slide count will vary based on activity complexity
