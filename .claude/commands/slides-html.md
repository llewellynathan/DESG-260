---
description: Generate an HTML slide deck from a slide outline
allowed-tools: Read, Glob, Write, Bash(mkdir:*), Bash(open:*)
---

**Usage:** `/slides-html [day number]` (e.g., `/slides-html 7`)

Generate a self-contained HTML + CSS + JS slide deck for Day $ARGUMENTS of DESG 260.

## Context Files to Read

1. **Determine the unit folder based on day number:**
   - Days 1-4 → `unit_a/`
   - Days 5-8 → `unit_b/`
   - Days 9-13 → `unit_c/`
   - Days 14-24 → `unit_d/`
   - Days 25-27 → `unit_e/`

2. **Read the slide outline** at `unit_X/day_XX_slides.md` — this is your primary content source
3. **Read the lesson plan** at `unit_X/day_XX.md` — use this for section/activity context and to enrich thin slides
4. **Read the reference HTML** at `unit_b/day_07_slides.html` — this is the canonical design system. Copy its `<style>` block and `<script>` block exactly as the foundation. Then generate new `<section>` elements for each slide.

## Design System

### Core Principle
The HTML file must be **completely self-contained** — all CSS and JS inline, no external dependencies. Copy the full `<style>` and `<script>` blocks from the reference file (`unit_b/day_07_slides.html`), then replace only the slide `<section>` elements with new content.

### Section Color Assignment
Each major class activity maps to a section color. Assign colors based on activity type:

| Activity Type | Color Variable | Background Variable |
|---|---|---|
| Warm-up / Opening | `--amber` | `--amber-bg` |
| Direct Instruction / Lecture | `--blue` | `--blue-bg` |
| Demo / Hands-on | `--violet` | `--violet-bg` |
| Work Session / Closing | `--green` | `--green-bg` |

Read the lesson plan's Activities section to determine which activities exist and assign colors. Use `--section-color` on each slide's inline style to set the left-edge bar color, and use the background variable on section divider slides.

### Layout Selection Rules

Choose the layout class for each slide based on its content:

**`billboard`** — Use for slides with a single big statement or 1-2 short lines. Centered, large text.
- Title slides
- Key concept reveals ("AI is a rendering tool, not a forming tool.")
- Provocations / questions to the class
- Prayer
- Any slide where the content is ≤2 sentences and deserves emphasis

**`divider`** — Use for section transition slides. Full tinted background, no left-edge bar.
- Activity section headers ("AI Tools for Prototyping")
- Always pair with a subtitle synthesized from the activity's theme

**`content`** — Use for slides with a heading + body content, vertically centered.
- Concept explanations with bullet points
- Exercises with numbered steps
- Limitation lists, policy comparisons
- Most "teaching" slides

**`top`** — Use for slides with grids/cards that need vertical space.
- "By the end of today..." with card grid
- Tool landscape cards
- Resource lists
- Any slide with 3+ card-like items

**`split`** — Use when there's a clear label/title on the left and supporting content on the right.
- Use sparingly — only when the heading is very short and the content is a distinct block

### Content Element Mapping

Map markdown content patterns to HTML elements:

| Markdown Pattern | HTML Element | Notes |
|---|---|---|
| `### Slide N: Warm-Up` | Warm-up slide (content layout) | Use amber section color, amber-bg background |
| `### Slide N: Prayer` | Billboard layout | Amber section color |
| `### Slide N: Title` | Billboard layout | Large font-size on h1 (4.8rem), no section color |
| `### Slide N: Today` | Content layout with `.timeline` | Use timeline dots + lines with section colors |
| `### Slide N: By the end of today...` | Top layout with `.card-row.c3` | Cards with colored top-borders |
| Section headers (activity names) | Divider layout | Tinted background |
| Bullet lists (≤4 items) | `<ul>` or `<ol class="numbered">` | Use numbered for ordered points |
| Numbered steps (exercises) | `<ol class="steps">` | Circled numbers, section-colored |
| `> blockquote` (instructor cues) | `<p class="callout accent">` | Gold/amber colored callout |
| Tool/concept cards | `.card-row` grid with `.card` items | Match column count to item count |
| Key takeaway text | `<p class="big-text accent">` | Large, amber-colored |
| Side-by-side comparison | `.policy-pair` grid | Two columns |
| Resource links | `<ul class="resource-list">` | Label + link format |
| Keyboard shortcuts | `<kbd>` inside `.shortcut-row` | Styled key badges |
| `### Slide N: Next Up` | Top layout | Green section, green-bg background |

### "Today" Timeline Construction
For the "Today" slide, build a vertical timeline from the activity list:
```html
<div class="timeline">
  <div class="timeline-item"><div class="timeline-dot" style="background: var(--amber);"></div><span class="timeline-label">Activity Name</span></div>
  <div class="timeline-line"></div>
  <!-- repeat for each activity -->
</div>
```
Assign dot colors matching each activity's section color.

### Slide Structure Template
Every slide follows this pattern:
```html
<section class="slide [layout]" style="--section-color: var(--[color]);">
  <!-- content elements -->
</section>
```
The first slide gets the additional class `active`. All others start hidden.

## Content Enrichment Rules

The slide outline markdown is your primary source, but it may be sparse. When generating HTML:

1. **Don't copy markdown verbatim** — Rethink how each point is best presented visually. A bullet list in markdown might become cards, a timeline, or a single billboard statement.
2. **Reduce text** — If a slide has 5+ bullet points, consider splitting into two slides or consolidating into fewer, punchier statements. The instructor speaks; the slide anchors.
3. **Add instructor cues** — If the lesson plan mentions discussion prompts or "we do" activities that aren't in the slide outline, add them as `callout` paragraphs.
4. **Use the Question → Reveal pattern** — When a key concept can be framed as a question first, split it into two slides: a billboard question, then a billboard answer.
5. **Synthesize subtitles** — Section divider slides should have a subtitle that captures the angle/energy of the section, not just repeat the title.

## Animation System

The CSS and JS from the reference file handle all animations automatically. You do NOT need to add animation code. Just use the correct class names and element structures:

- Direct children of `.slide.active` get staggered `fadeUp` entrance
- `.billboard.active h1` and `.divider.active h1` get `scaleUp` entrance
- `.card` elements get staggered `fadeUp` with border `widen` effect
- `.timeline-item` elements cascade with `.timeline-dot` `popIn`
- `.steps li` elements stagger in sequence
- `.numbered li` elements stagger in sequence
- `.policy` children stagger left then right
- `.shortcut-row span` and `.resource-list li` stagger in
- `::before` section bars get `growDown` from top
- Slide transitions are directional (slide left/right) via JS

**All of this happens automatically** when you use the correct CSS classes. Just build the HTML structure.

## Output

Save the generated file to **two locations**:

1. **This repo (working copy):** `unit_X/day_XX_slides.html` in the same unit folder
2. **Slides repo (public):** `../DESG-260-slides/unit_X/day_XX_slides.html` — create the unit subfolder if it doesn't exist

The slides repo at `../DESG-260-slides/` is a separate public GitHub repo served via GitHub Pages. After writing the file there, also update `../DESG-260-slides/index.html` to include a link to the new slide deck under the appropriate unit heading. If the unit heading doesn't exist yet, add it.

After writing both files, run `open [path]` to open the local copy in the browser for verification.

## Checklist Before Saving

- [ ] Full `<style>` block copied from reference (including animations)
- [ ] Full `<script>` block copied from reference (including directional navigation)
- [ ] First slide has class `active`
- [ ] Every slide has a layout class (`billboard`, `divider`, `content`, `top`, or `split`)
- [ ] Section colors assigned via `--section-color` inline styles
- [ ] Section dividers use tinted `background` and `--section-bg`
- [ ] "Today" uses timeline component with colored dots
- [ ] "By the end of today" uses card grid
- [ ] Exercises use `<ol class="steps">`
- [ ] Instructor cues use `<p class="callout accent">`
- [ ] No external dependencies — everything inline
- [ ] Slide counter `<div>` present after the deck
