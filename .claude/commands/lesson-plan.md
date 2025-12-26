---
description: Generate a lesson plan for a specified day number
allowed-tools: Read, Write, Edit, Glob
---

Generate a complete lesson plan for Day $ARGUMENTS of DESG 260.

## Context Files to Read
1. @course_schedule.md — Find Day $ARGUMENTS and extract all Desired Results, Topics, Assignments, Activities, and Resources
2. @lesson_plans/_template.md — Use this structure
3. @CLAUDE.md — Follow all conventions in "Lesson Plan Format" and "Style Preferences"
4. @lesson_plans/day_01.md and @lesson_plans/day_02.md — Match the established patterns
5. **Read the relevant assignment file based on the day's unit:**
   - Days 1-4: @assignment_1_wayfinding.md
   - Days 5-8: @assignment_2_make_it_better_app.md
   - Days 9-13: @assignment_3_hierarchy_responsive_website.md
   - Days 14-24: @assignment_4_neue_application.md

## Requirements
1. Create the lesson plan at `lesson_plans/day_XX.md` (use two-digit format: day_03.md)
2. Pull all content from course_schedule.md for that day
3. Transform Topics into concrete Activities with time estimates
4. Calculate total time (Monday ~120 min, Wednesday ~180 min)
5. Ensure at least half the class is work/studio time
6. Frame activities using forming/rendering intent
7. **Verify ALL Desired Results align to activities** (per CLAUDE.md "Alignment Check"):
   - Each Essential Question → explicitly asked or discussed in an activity
   - Each Understanding → activity helps students arrive at this understanding
   - Each "Students Will Know" → knowledge introduced or reinforced in an activity
   - Each "Students Will Be Able To" → skill practiced during class
8. Introduce assignments BEFORE related work sessions
9. **When introducing or referencing assignments, pull exact requirements from the assignment file** (dimensions, format, quantity, grading criteria, due dates)
10. After creating the lesson plan, update course_schedule.md to simplify that day's entry to match Day 1's format

## Output Format
Follow the exact structure in _template.md with all sections filled in.
