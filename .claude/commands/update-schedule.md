---
description: Update course_schedule.md after creating a lesson plan
allowed-tools: Read, Edit
---

Update the Day $ARGUMENTS entry in course_schedule.md to the simplified format.

## Context Files to Read
1. @course_schedule.md — Find Day $ARGUMENTS current entry
2. @lesson_plans/day_XX.md — Get the focus and activities from the lesson plan (use two-digit format)

## Format Template

Replace the day's entry with this structure:

```markdown
### Day X — [Weekday], [Date]
**Unit [Letter]: [Name]**
Today's Focus: [One-line focus from the lesson plan]

**Come to class having done:**
- 📚 [Reading assignments]
- ⛳ [Checkpoints due]
- 🚩 [Major assignments due]

**In class:**
- [Activity 1 summary]
- [Activity 2 summary]
- [Continue for main activities...]

→ [Lesson Plan](unit_X/day_XX.md)
```

## Formatting Rules

1. **Legend symbols:**
   - 📚 = Reading due before class
   - ⛳ = Checkpoint (minor, in-class or sharing)
   - 🚩 = Major assignment due

2. **"Come to class having done:" section:**
   - Include only if there are pre-class assignments (readings, checkpoints, or major assignments due)
   - Omit the entire section if nothing is due before class

3. **"In class:" section:**
   - Brief summaries, not full activity descriptions
   - Include 4-6 main activities
   - Use verbs: "Introduce...", "Discuss...", "Workshop...", "Work session..."

4. **Remove from original entry:**
   - All Desired Results (Essential Questions, Understandings, Know, Do)
   - Topics section
   - Assignments section (move relevant items to "Come to class having done")
   - Resources section
   - Targeted Learning Outcomes

5. **Keep:**
   - Day number, weekday, date
   - Unit and name
   - Lesson plan link (update path if needed)

## Example (Day 1)

```markdown
### Day 1 — Wed, Jan 7
**Unit A: Wayfinding Map & Icons**
Today's Focus: What is design? Forming vs. rendering intent.

**Come to class having done:**
- 📚 Read syllabus before class

**In class:**
- Introduce the forming/rendering framework as the course's central concept
- 7 principles of great design & learning (feedback, externalization, failure, incubation, iteration, teaching, reflection)
- Wayfinding & experience mapping concepts + gallery walk
- Introduce Assignment 1: Wayfinding Map & Icons
- Brainstorming: identify journeys worth mapping

→ [Lesson Plan](unit_a/day_01.md)
```
