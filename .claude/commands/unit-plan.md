---
description: Plan a complete unit with overview and assignment files
allowed-tools: Read, Write, Glob
---

**Usage:** `/unit-plan [unit letter]` (e.g., `/unit-plan B`)

Generate the foundational files for Unit $ARGUMENTS of DESG 260.

## Context Files to Read
1. @course_schedule.md — Find all days in Unit $ARGUMENTS and extract Desired Results, Topics, and Assignments
2. @CLAUDE.md — Follow course framework and style preferences
3. @unit_a/overview.md — Use as a template for tone and structure
4. @unit_a/assignment.md — Use as a template for assignment format

## Unit Boundaries
- Unit A: Days 1-4
- Unit B: Days 5-8
- Unit C: Days 9-13
- Unit D: Days 14-24
- Unit E: Days 25-27

## What to Generate

### 1. overview.md
Create `unit_[letter]/overview.md` with these sections:

**Title:** `# Unit [Letter]: [Name]`
**Subtitle:** `## [Subtitle from course_schedule]`

**Sections:**
- **The Big Idea** — Connect to forming/rendering intent framework; what's the central design concept?
- **What You'll Learn** — 4-5 bullet points synthesized from the Desired Results across all days
- **What You'll Make** — Describe the final deliverable(s)
- **Why This Matters** — Professional relevance; how this skill translates to real design work

**Tone:** Welcoming but direct. Second person ("you'll"). No fluff.

### 2. assignment.md
Create `unit_[letter]/assignment.md` with these sections:

**Title:** `# Assignment [Number]: [Name]`

**Sections:**
- **Introduction** — Frame the assignment; why does this matter?
- **The Assignment** — Clear description of what students will create
- **Requirements** — Bulleted constraints and specifications (use 💚 for required, ❌ for prohibited)
- **Rubric** — 5 criteria × 4 levels (Beginning/Developing/Proficient/Exemplary) in table format
- **Process** — Milestones leading to final (A1, A2, A3... or B1, B2, B3... etc.)
- **Final Deliverable** — Exact specifications for the final submission

**Rubric Criteria to Include:**
1. Conceptual Depth & Novelty
2. Testing & Iteration
3. [Project-specific craft criterion]
4. Overall Visual Design
5. Process Documentation

## Output
After generating both files, summarize what was created and suggest running `/lesson-plan` for each day in the unit.
