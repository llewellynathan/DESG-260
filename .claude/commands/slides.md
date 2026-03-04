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
   - Days 9-14 → `unit_c/`
   - Days 15-25 → `unit_d/`
   - Days 26-28 → `unit_e/`

2. **Read the lesson plan file** at `unit_X/day_XX.md` (use two-digit format)

3. **Read the prayer roll** at `prayer_roll.md` (project root)

## Prayer Roll Selection

Before generating slides, select a student for the Prayer slide:

1. **Parse `prayer_roll.md`** — Read the table of students and their "Last Prayed" dates
2. **Find eligible students** — Students with an empty "Last Prayed" column
3. **Reset if needed** — If ALL students have dates (everyone has prayed), clear all dates to start a new cycle
4. **Randomly select one** — From the eligible students, pick one at random
5. **Use first name only** — Insert just the first name (e.g., "Annika" not "Annika B.") into the Prayer slide
6. **Update the prayer roll** — Write today's date (M/D format, e.g., "2/9") in the "Last Prayed" column for the selected student

**Important:** The Prayer slide should contain the actual student name, not `[Name]`. Example:
```
### Slide 2: Prayer
**Prayer**
Annika, will you pray for us today?
```

## Slide Structure Rules

**Key principle:** The Warm-Up is the first thing students see when entering class. Prayer follows, then title, preview, and remaining activities. Target **12–16 slides** for a typical class session — prefer fewer, denser slides over many sparse ones.

Generate slides in this order:

### 1. Warm-Up Slide
- Pull from Activity 1 (Warm-Up) in the lesson plan
- This is what students see immediately when they enter — they can start working right away
- Include the activity name and instructions

### 2. Prayer Slide
- Always include a Prayer slide after the warm-up
- Title: "Prayer"
- Content: Use the student name selected from the prayer roll (see "Prayer Roll Selection" above)

### 3. Title Slide
- Unit letter and name only (large, centered)
- **Big Idea** as subtitle: A single memorable statement that connects all of the day's activities into one theme. Synthesize from the full lesson — not just the Focus section. It should feel like the thread running through everything students do that day.
- Do NOT include the day number, weekday, or date on this slide

### 4. Today Slide
- Title: **Today**
- List the main activities as a **bullet list** (not arrows)
- This previews what the class will cover

### 5. "By the end of today..." Slide
- Generate this slide to establish what students will learn before explaining why it matters
- Use **named categories** — each learning goal gets a short bold label (2-3 words) and a plain-language description
- Draw from the lesson's Desired Results, but write as things students will *do* or *make* — not academic language
- Format each as: **Label** — Description
- Example:
  - **AI Tools** — You'll know the current landscape of AI prototyping tools and what each is good (and bad) at
  - **Digital prototyping** — You'll start translating your paper prototype into an interactive digital prototype in Figma
  - **AI Policy** — You'll understand the B3/B4 AI policy: AI is welcome for B3, but B4 must be your own Figma work

### 6. "Why This Matters" Slide
- Title: **Why this matters**
- This slide follows the outcomes slide so students know what "this" refers to
- Pull from the lesson plan's "Why This Matters" field
- Frame as a direct answer to "Why should I care about this?"
- Connect today's topic to real design work students will do
- Keep it to 1-3 punchy statements — this is motivation, not a lecture
- Use language like "Without this, you'll..." or "This lets you..." or "Professional designers use this to..."
- Can include a concrete example or scenario that makes it tangible

### 7. Activity Slides
For each activity in the lesson plan (starting from Activity 2, since Warm-Up is Slide 1), create slides based on its content.

**Consolidation rule:** Prefer merging related concepts into a single slide rather than splitting every sub-point. If two consecutive content points support the same idea, combine them. Aim for roughly 1 slide per major idea.

**I Do / We Do / You Do structure:** When a Direct Instruction activity in the lesson plan has explicit "I do," "We do," and "You do" phases, preserve this pedagogical structure in the slides:

1. **I do phases** — Generate standard content slides. The instructor is presenting, demonstrating, or explaining. Use appropriate layouts (content slides, billboard for key statements). These form the bulk of the lecture slides.

2. **We do phases** — Generate slides with discussion prompts/callouts. Frame the content as participatory:
   - Use blockquote callouts for discussion questions
   - Include prompts like "Let's try this together..." or "As a class..."
   - Example: A slide titled "Apply Type Thinking" with content + blockquote asking "What's the H1 on your product page?"

3. **You do phases** — Generate hands-on exercise slides with numbered instructions. Students work independently:
   - Use numbered step format (not bullets)
   - Include time allocation if specified in the lesson plan
   - Frame as "do this" instructions, not descriptions
   - Example: "1. Open your PDP content  2. Identify what should be H1, H2, H3  3. Note any hierarchy decisions you're unsure about (5 min)"

**Important:** Don't skip "You do" phases even if they're brief. These are critical practice moments that let students apply what they just learned before moving on. Always generate a slide with clear instructions for student work.

**Activity section header** (for major activities like lectures or demos):
- Activity name as title
- Optional subtitle synthesized from the activity's theme (e.g., "The good, the bad, and the ugly")
- Use subtitles when the activity has a clear angle or framing beyond its name

**Content slides:**
- Break down the activity into logical slides based on distinct ideas
- Keep bullet points concise — these are slide prompts, not full scripts

**Hands-on exercise slides:** When an activity involves students doing something (not just listening), generate a slide with **numbered step-by-step instructions** rather than summary bullets. Structure as "do this" instructions.
- Example: "1. Go to Figma Make  2. Describe an app you want to make, keep it simple  3. Submit your prompt"

**Instructor cues and discussion prompts:** Do NOT create separate discussion slides. Instead, include discussion questions and instructor prompts as **blockquotes** within content slides:
```
> What are you noticing in the prototype it made for you?
```
These serve as prompts for the instructor to facilitate discussion — they are not standalone slides.

**Reveal/key takeaway:** If the instructor shares a definition or answer after discussion, include it on the same content slide (or as a follow-up content slide if the reveal is substantial). Use bold for emphasis.

### 8. "Next Up" Slide
- Replaces separate work session, homework, and due date slides
- Title: **Next up**
- Combine into a single slide:
  - What students are working on during the work session
  - Key reminders and tips
  - Homework items (plain text, no emoji prefixes)
  - Due dates
- Only split into multiple slides if the combined content is genuinely too dense for one slide (4+ distinct homework items AND work session instructions)

### 9. Resources Slide (only if needed)
- Only include a Resources slide if there are specific tools or links students need to access during class
- If resources are just reference material, skip this slide — students can find them in the lesson plan

## Output Format

Use this exact markdown format with `---` as slide separators:

```markdown
# Day X Presentation Outline
## Unit [Letter]: [Name]

---

### Slide 1: Warm-Up
**Warm-Up: [Specific Activity]** (X min)
- [Instruction 1]
- [Instruction 2]
- [Instruction 3]

---

### Slide 2: Prayer
**Prayer**
[Student name from prayer roll], will you pray for us today?

---

### Slide 3: Title
**Unit [Letter]: [Name]**
[Big Idea as subtitle]

---

### Slide 4: Today
**Today**
- [Activity name]
- [Activity name]
- [Activity name]
- [Activity name]

---

### Slide 5: By the end of today...
**[Label 1]** — [Plain-language description]

**[Label 2]** — [Plain-language description]

**[Label 3]** — [Plain-language description]

---

### Slide 6: Why This Matters
**Why this matters**
[1-3 punchy statements connecting today's topic to real design work]
[Now that students know what they'll learn, explain why it matters]

---

### Slide 7: [Activity Section Header]
**[Activity Name]**
[Optional subtitle]

---

### Slide 8: [Content]
**[Concept or topic]**
- [Point 1]
- [Point 2]

> [Instructor cue or discussion prompt]

---

[Continue with slides following the Activities sequence...]

---

### Slide N: Next Up
**Next up**
- [Work session task and details]
- [Key reminders]
- [Homework item 1] (due [when])
- [Homework item 2]

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
- Target 12–16 slides total — consolidate aggressively
- Discussion prompts use blockquote format (`>`) within content slides, not separate slides
- No emoji prefixes on slides (emojis stay in lesson plans only)
- Hands-on activities use numbered instructions, not summary bullets
