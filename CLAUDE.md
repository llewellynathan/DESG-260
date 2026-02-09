# DESG 260 Project Context

## Course Overview
- **Course:** DESG 260: Interface & Usability (User Experience 1)
- **Institution:** BYU
- **Semester:** Winter 2026
- **Class sessions:** 28 (Mon & Wed)

## Class Timing

- **Mondays:** ~2 hours (120 min)
- **Wednesdays:** ~3 hours (180 min)
- **Work time:** At least half of each class should be studio/work time
  - Mondays: ~60 min instruction, ~60 min work
  - Wednesdays: ~90 min instruction, ~90 min work

## Core Framework: Forming vs. Rendering Intent

This is the central concept of the course. Reference it throughout:

- **Design is the forming and rendering of intent**
- **Forming intent:** Discovering the right problem and envisioning the right solution
- **Rendering intent:** Executing that vision with skill and craft
- **Good design = excellence in both**
- **Bad design = failure in either forming OR rendering**

Qualities that support each:
- Forming: empathy, curiosity, humility
- Rendering: craft skills (typography, prototyping, visual hierarchy)

## File Structure

```
DESG 260/
├── CLAUDE.md                   ← This file
├── course_overview.md          ← Course-level backward design
├── course_schedule.md          ← Simplified calendar
├── lesson_plans/
│   └── _template.md            ← Copy for new lessons
└── unit_a/                     ← Unit A: Wayfinding Map & Icons
    ├── overview.md             ← Student-facing unit introduction
    ├── assignment.md           ← Assignment brief
    ├── day_01.md
    ├── day_02.md
    ├── day_03.md
    └── day_04.md
```

*Future units (B, C, D, E) will follow the same structure: `unit_x/overview.md`, `unit_x/assignment.md`, and daily lesson plans.*

## Lesson Plan Format

Each lesson plan follows this structure:
1. Title: `# Day X — [Weekday], [Date]`
2. Unit: `## Unit [A-E]: [Name]`
3. Focus: One-line theme
4. Desired Results (EQs, Understandings, Know, Do, Learning Outcomes)
5. Assignments Due
6. Activities (numbered, with time in parentheses)
7. Homework
8. Resources

## Key Decisions

1. **Activities replace Topics** — Don't use a separate "Topics" section; integrate all topics into Activities
2. **Assignment intro before related work** — Introduce assignments before students start working on them (e.g., introduce A1 before brainstorming session)
3. **Feedback activities on feedback days** — Place feedback-related activities (like Telestrations) on days when students actually give/receive feedback
4. **Include time estimates** — Every activity gets (X min)
5. **Total time** — Include total at end of Activities section
6. **Homework is specific** — State exactly what's due and when
7. **Update schedule when creating lesson plans** — When a lesson plan is created, ensure that day's entry in `course_schedule.md` follows this format:
   ```
   ### Day X — [Weekday], [Date]
   **Unit [A-E]: [Name]**
   Today's Focus: [One-line theme]

   **In class:**
   - [Activities, topics, exercises]

   **Come to class having done:**
   - [Readings, assignments to complete before class]

   **Assignments due before next class:**
   - [Deliverables due after this class, before the next one]

   → [Lesson Plan](unit_X/day_XX.md)
   ```

## Slides Workflow

HTML slides are hosted via GitHub Pages in a separate repo: `DESG-260-slides`

When generating or editing slides:
1. Create/edit the HTML file in `unit_x/day_xx_slides.html` (this repo)
2. Copy the file to `../DESG-260-slides/unit_x/day_xx_slides.html`
3. Update `../DESG-260-slides/index.html` if adding a new day
4. **After slide work is complete** (creation or edits), ask the user if they want to commit and push to the slides repo

## Style Preferences

- Use bold for activity names: **Activity Name** (X min)
- Use bullet points for activity details
- Connect activities to Essential Questions where relevant
- Reference forming/rendering framework regularly
- Be specific about deliverable requirements (size, format, quantity)

## Projects & Units

| Unit | Project | Days | Focus |
|------|---------|------|-------|
| A | Wayfinding Map & Icons | 1-4 | Journeys, Destinations, Touchpoints |
| B | Make It Better App | 5-8 | Product Design, Conventions |
| C | Hierarchy/Responsive Web | 9-14 | Responsive, Online, Mobile |
| D | Neue App (Capstone) | 15-25 | Problem Seeking, Beautiful & Functional |
| E | Documentation | 26-28 | Storytelling, Case Studies |

## Seven Learning Outcomes

1. Better Interactions & Experiences
2. Critical Analysis of Form and Format
3. Problem Discovery & Research (Curiosity, Empathy, Humility)
4. Familiarity and Distinctiveness
5. Design Strategy
6. Communication and Feedback
7. Detailed Documentation

## Alignment Check: Desired Results ↔ Activities

Each lesson plan uses a tagging system to connect Desired Results to Activities.

### Tagging System

Number each desired result with a prefix:
- `EQ#` — Essential Questions (EQ1, EQ2, etc.)
- `U#` — Understandings
- `K#` — Students Will Know
- `S#` — Students Will Be Able To (Skills)

### How to Use

1. **In Desired Results** — Number each item explicitly:
   ```markdown
   **Essential Questions:**
   - EQ1: What is design?
   - EQ2: What is forming vs. rendering intent?
   ```

2. **In Activities** — Add inline tags after the time:
   ```markdown
   3. **"What is Design?" Discussion** (15 min) `[EQ1, EQ2, K1]`
   ```

3. **In Alignment Check table** — Verify every result is addressed:
   ```markdown
   | Code | Desired Result | Activities |
   |------|----------------|------------|
   | EQ1 | What is design? | 3, 6 |
   | EQ2 | Forming vs. rendering | 2, 3, 5 |
   ```

### Verification

After drafting a lesson plan, check the Alignment table:
- Every code should have at least one activity listed
- If a result shows `—` (no activities), add it to an existing activity or create a new one

### Common Gaps and Fixes

1. **EQ not addressed** → Add a discussion question or prompt to an existing activity
2. **Understanding not connected** → Frame an activity introduction with the understanding
3. **Knowledge not introduced** → Add vocabulary or concept explanation to a relevant activity
4. **Skill not practiced** → Rename activity to emphasize the skill; add prompts that require students to demonstrate it
