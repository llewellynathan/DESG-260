---
description: Generate a lesson plan for a specified day number
allowed-tools: Read, Write, Edit, Glob
---

**Usage:** `/lesson-plan [day number]` (e.g., `/lesson-plan 5`)

Generate a simple, studio-focused lesson plan for Day $ARGUMENTS of DESG 260.

## Design Philosophy

Create **simple but information-rich** lesson plans. Provide high-value direct instruction in minimal time so students have abundant studio time.

**Activities should be:**
- **Warm-up** — Students start independently
- **Today's Learning Goals** — Review Desired Results, preview how activities address them
- **Direct Instruction** (required) — Information-rich, teacher-led explicit teaching: modeling techniques, explaining concepts, demonstrating processes ("I do, We do, You do")
- **Additional learning activities** (optional) — Critique, discussion, peer feedback
- **Work session** — The main event; gets remaining time

**Aim for 4-6 activities total** (not 8-10). Consolidate related content into fewer, high-value activities.

## Context Files to Read
1. @course_schedule.md — Find Day $ARGUMENTS and extract Desired Results, Assignments, and Resources
2. @CLAUDE.md — Follow course framework (forming/rendering intent)
3. **Read the relevant unit files based on day number:**
   - Days 1-4: `unit_a/assignment.md`
   - Days 5-8: `unit_b/assignment.md`
   - Days 9-14: `unit_c/assignment.md`
   - Days 15-25: `unit_d/assignment.md`
   - Days 26-28: `unit_e/assignment.md`

## Requirements
1. Create the lesson plan at the appropriate unit folder: `unit_X/day_XX.md`
2. Pull all Desired Results from course_schedule.md for that day
3. **Write a Focus that becomes a "Big Idea"** — What's the one thing students should remember?
4. **Consolidate into 4-6 activities** (warm-up, learning goals, direct instruction, possibly critique/discussion, work session)
5. Ensure at least half the class is work/studio time
6. Use the tagging system: `**Activity Name** (X min) [EQ1, U2, S1]`
7. Pull exact requirements from assignment files when introducing milestones
8. Frame activities using forming/rendering intent

## Output Structure

```markdown
# Day X — [Weekday], [Date]
## Unit [Letter]: [Name]

**Focus:** [One-line Big Idea — what should students remember from this class?]

**Why This Matters:** [1-2 sentences connecting today's topic to students' real design work. Answer: "Why should I care about this?" Frame it in terms of what students will be able to DO better as designers, or what problems they'll avoid. Be specific and practical, not abstract.]

**Targeted Learning Outcomes:** [From course_schedule.md]

---

### Desired Results

**Essential Questions:**
- EQ1: [From course_schedule.md]
- EQ2: [From course_schedule.md]

**Understandings:**
- U1: [From course_schedule.md]
- U2: [From course_schedule.md]

**Students Will Know:**
- K1: [From course_schedule.md]
- K2: [From course_schedule.md]

**Students Will Be Able To:**
- S1: [From course_schedule.md]
- S2: [From course_schedule.md]

---

### Assignments Due
- 📚 [Readings]
- ⛳ [Checkpoints]
- 🚩 [Major assignments]

---

### Activities

1. **Warm-Up: [Activity Name]** (10 min) `[relevant tags]`
   - Students can begin independently without instructor
   - Prepares for the day's content
   - Late arrivals aren't disadvantaged

2. **Today's Learning Goals** (5 min) `[all tags]`
   - **Why this matters:** [Connect to real design work — what will students do better?]
   - Preview what activities will address each learning goal
   - Frame the day's learning in terms of forming/rendering intent

3. **[Direct Instruction Activity]** (~15-25 min) `[relevant tags]`
   - **I do:** Teacher models/demonstrates/explains
   - **We do:** Class practices together
   - **You do:** Students try independently
   - Information-rich: substantial content, not stretched thin
   - Examples: Vector tools demo, design principles lecture, technique demonstration

4. **[Additional Activity if needed]** (~15-20 min) `[relevant tags]`
   - Critique, discussion, peer feedback, etc.
   - Only include if the day requires it

5. **[Assignment Introduction]** (~10 min) `[relevant tags]`
   - Only if introducing a new milestone
   - Requirements (pull from assignment.md)
   - Due date

6. **Work Session + 1:1 Feedback** (remaining time) `[relevant tags]`
   - What students are working on
   - Instructor focus during circulation
   - What's due by end of class (if anything)

---

### Homework
- [Specific items with due dates]

---

### Resources
- [Links and references from course_schedule.md]
```

## Special Cases

- **Day 1** — Allow extended instruction for course intro, defining design, and foundational concepts. Day 1 establishes the forming/rendering framework.
- **Final unit days** (e.g., Day 4, Day 8) — Minimal instruction; mostly work time and 1:1 feedback.

## Guiding Principles

1. **Start with why** — Every lesson needs a clear "Why This Matters" that connects to real design work
2. **Desired Results drive activities** — Activities should directly address EQs, Understandings, and Skills
3. **Review Desired Results each class** — Activity 2 previews learning goals with the "why" framing
4. **Include Direct Instruction** — Each lesson needs information-rich, teacher-led teaching
5. **Consolidate related content** — Combine items into fewer, high-value activities
6. **Work session is the main event** — Instruction prepares students for productive work time
7. **Pull exact requirements from assignment files** — Dimensions, formats, due dates
