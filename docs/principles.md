# UI Design Principles
*Working reference for Sy — actionable rules only. If it doesn't help make a better design decision, it's not here.*
*Last audited: March 20 2026*

---

## SPACING (Rule of 4 / 8pt Grid)
```
4px   — micro gaps (icon-to-label)
8px   — tight (inline, button padding-y)
12px  — small (input padding-y)
16px  — base (card padding, button padding-x, page margins)
24px  — medium (section inner gap)
32px  — large (section outer gap)
48px  — xl (major breaks)
64px  — 2xl (section-to-section)
```
**Rule:** Inner padding < outer gap. If a card has 24px padding, gap between cards ≥ 24px.

---

## TYPOGRAPHY

**Body:** 16px / 1.5 line-height / 0 letter-spacing
**Dense UI:** 14px / 1.4 / 0
**Heading:** 24–32px / 1.2 / -0.02em
**Display:** 48px+ / 1.1 / -0.03em to -0.05em
**Uppercase labels:** +0.05em to +0.15em letter-spacing
**Max line length:** 60–75 characters

**Scale (mobile UI):** 11 · 12 · 13 · 14 · 15 · 16 · 18 · 20 · 24 · 28 · 32 · 36 · 40 · 48
If a size isn't in the scale, it shouldn't exist.

**Line height by context:**
```
Body text (long-form):     1.5–1.6
UI body text (labels):     1.3–1.5
Headings (single line):    1.0–1.2
Headings (2+ lines):       1.1–1.3
```

**Letter spacing:**
```
Large display (32px+):   -0.02em to -0.04em  ← tighten
Body (14–18px):          0 to +0.01em
All-caps labels:         +0.05em minimum
```

**Font weight:**
```
Below 400:  never — fails contrast, looks weak
400:        body text, secondary
500:        buttons, medium labels
600:        section headers, emphasized body
700:        display, key numbers, primary headings
```
**Never change weight on hover/active** — causes layout shift. Use color or opacity instead.

**Font smoothing (apply globally):**
```css
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
```

**Tabular numbers (any value that updates dynamically):**
```css
font-variant-numeric: tabular-nums;
```

**Headline text wrap:**
```css
h1, h2, h3 { text-wrap: balance; }
```
Prevents orphaned single words. Don't apply to body text.

---

## FONTS WITH CHARACTER (BEYOND INTER)

**The Il1 test:** Before using any font, check capital I / lowercase l / number 1. If indistinguishable → reject. Eliminates Gill Sans, Helvetica, many geometric sans-serifs.

**Open apertures required:** Closed apertures blur at 11–12px. Prefer fonts with open counters (PT Sans, Fira Sans, Source Sans Pro). This is why Helvetica failed in macOS Yosemite.

**Fonts that have personality and pass both tests:**
- **Albert Sans** — geometric, open forms, tactile quality (CutList)
- **DM Sans** — clean but slightly quirky, approachable
- **Plus Jakarta Sans** — warm, curved, human
- **Instrument Sans** — Figma's choice, confident, modern
- **Mona Sans** — GitHub variable font, excellent weight range
- **Figtree** — curved terminals on y/f/t, friendly without being weak
- **Atkinson Hyperlegible** — designed for legibility, genuinely distinctive letterforms

**Font pairing rule:** One does the work (readable at small sizes), one makes the statement (display/headings only). Two fonts with strong character compete. One should be calm.

**For most UI:** Single typeface, multiple weights. Better single font > two mediocre ones.

---

## COLOR CONTRAST (WCAG)
```
Normal text (<18px):     AA = 4.5:1   AAA = 7:1
Large text (≥18px):      AA = 3:1     AAA = 4.5:1
UI components/icons:     AA = 3:1
Focus indicator:         3:1 vs unfocused state
```
`#767676` on white = 4.54:1 → AA minimum.

**Four combos that always fail:**
- Light grey text on white (#999 on #FFF = 2.85:1)
- Red on green (colorblindness)
- Blue link on blue-tinted card background
- White text on medium-saturation color (must darken the bg significantly)

**Never use color as the sole indicator of meaning.** Always pair with icon, label, or pattern.

---

## COLOR SYSTEM

**The 60-30-10 rule:**
```
60% — Neutral (backgrounds, surfaces)
30% — Secondary (cards, sidebars)
10% — Accent (CTAs, active states, alerts — nothing else)
```
The accent's power comes from scarcity. 10% is a hard limit.

**Three-layer token architecture:**
```
Primitive tokens  → raw values (blue-100 through blue-900)
Semantic tokens   → purpose-assigned (text/primary → blue-800)
Component tokens  → component-specific (button/primary → interactive/brand)
```
Never apply primitives directly to components.

**Eight semantic roles every UI must define:**
```
surface/default      — primary background
surface/elevated     — modals, popovers, floating panels
text/primary         — body + headings (target 7:1 AAA)
text/secondary       — labels, captions, metadata (min 4.5:1 AA)
interactive/default  — buttons, links, active states
interactive/hover    — 10–15% darker than default
status/success       — never the sole indicator (pair with icon)
status/error         — never the sole indicator (pair with icon)
```

**Building neutrals — always use a hue temperature, never pure grey:**
```
Warm (30–40°H):  human, editorial, craft — CutList, Notion-adjacent
Cool (220–240°H): technical, precise, developer — Linear, Vercel
Pure grey (#808080): dead, institutional — never use
```

**Building an accent scale (HSB method):**
```
Tints (lighter): ↑ Brightness, ↓ Saturation slightly
Shades (darker): ↓ Brightness, ↑ Saturation slightly
```
Adjusting only Brightness → washed out tints + muddy darks.

**Palette personality table:**

| Palette | Communicates | Examples |
|---|---|---|
| White + blue/purple accent | SaaS default, generic | Half of Dribbble |
| Dark navy + indigo | Technical, precise | Linear, Vercel |
| Warm white + forest green | Craft, care, nature | CutList |
| Warm white + deep brown | Editorial, human | Notion-adjacent |
| Off-black + amber | Premium, tactile | Luxury, tools |

**Dark mode — don't invert, design it:**
- Text: use #F1F5F9 or #FAFAFA, not pure white (too harsh)
- Accent: desaturate and lighten for dark backgrounds
- Elevation: lighter-than-surface fill (not shadows) indicates elevation
- Semantic tokens make this switchable without touching component code

---

## iOS / iPadOS NATIVE DESIGN

**Touch targets:** min 44×44pt
**Horizontal margins:** 16pt minimum
**Tab bar:** bottom (iPhone) / max 5 tabs / navigation only, never actions
**Back button:** system tint by default — override if it conflicts with your color system

**iOS Text Styles (always use these in SwiftUI — never hardcode sizes):**
```
.largeTitle    → 34pt   Screen titles
.title         → 28pt   Section headings
.headline      → 17pt semibold   Row labels, card heads
.body          → 17pt   Default content
.subheadline   → 15pt   Secondary labels
.caption       → 12pt   Section headers, meta
.caption2      → 11pt   Metadata only — minimum
```

**SF Symbols:** Filled = active/selected. Outline = inactive. Don't use in icons/logos (license).

**Grouped list surfaces:**
```
systemGroupedBackground           → Page
secondarySystemGroupedBackground  → Card
tertiarySystemGroupedBackground   → Row within card
```

**Disclosure (›) vs Info (ⓘ):** Disclosure navigates. Info shows detail. Never both on same row.

---

## COMPONENT SIZES
```
Input height:   32px (compact) / 40px (standard) / 48px (large)
Button height:  32px (sm) / 36px (md) / 40px (lg) / 52px (prominent)
Row height:     32–40px (dense) / 48px (standard) / 56px (comfortable)
Icon size:      16px (inline) / 20px (button) / 24px (standalone)
Avatar:         24 / 32 / 40 / 48px
```

---

## CONCENTRIC BORDER RADIUS
When nesting elements, outer radius must equal inner radius + padding.
```
outer_radius = inner_radius + padding

Example:
  inner button: border-radius 12px
  card padding: 8px
  → card: border-radius 20px
```
Applies to: buttons in cards, badges in rows, icons in containers, inputs in form cards. Mismatched radii look cheap immediately.

---

## SHADOWS
Layered box-shadow reads better than a solid 1px border — adapts to any background via transparency.
```css
/* Card resting */
box-shadow:
  0px 0px 0px 1px rgba(0, 0, 0, 0.06),
  0px 1px 2px -1px rgba(0, 0, 0, 0.06),
  0px 2px 4px 0px rgba(0, 0, 0, 0.04);

/* Card hover */
box-shadow:
  0px 0px 0px 1px rgba(0, 0, 0, 0.08),
  0px 1px 2px -1px rgba(0, 0, 0, 0.08),
  0px 2px 4px 0px rgba(0, 0, 0, 0.06);
```
Images: `outline: 1px solid rgba(0,0,0,0.1); outline-offset: -1px` gives consistent edges.

---

## ANIMATION

**Timing:**
```
Micro (hover, toggle):  50–150ms
Short (dropdown):       150–300ms
Medium (modal, page):   300–500ms
Max for interactions:   200ms — anything longer feels slow
```

**Easing:**
```
ease-out:    cubic-bezier(0, 0, 0.2, 1)      → elements entering
ease-in:     cubic-bezier(0.4, 0, 1, 1)      → elements leaving
ease-in-out: cubic-bezier(0.4, 0, 0.2, 1)   → elements repositioning
```

**Enter/exit:**
- Scale up from ~0.8 (not 0) for dialogs and menus
- Scale down on press: ~0.96–0.97 (not 0.8 — too dramatic)
- Enter: `translateY(8px) + blur(5px) + opacity 0→1`
- Exit: `translateY(-12px) + blur(4px) + opacity 1→0` ← smaller offset, subtler

**Staggered enter (heading → body → buttons):**
```css
animation-delay: calc(var(--index) * 80ms);
```

**CSS transitions = interruptible. CSS keyframes = not interruptible.**
Rule: transitions for all user interactions. Keyframes only for one-shot sequences (onboarding, celebrations).

**Frequency × Novelty decision:**
```
High frequency + low novelty → NO animation
  (right-click menus, list item add/delete, common button presses)

Low frequency + high novelty → full animation appropriate
  (onboarding, celebrations, special transitions)
```
Novelty is spent by repetition. The 500th time, a delight animation is cognitive tax.

**Spatial consistency:** If something slides in from the right, it lives to the right. Every directional animation is a spatial claim. Be consistent or it breaks the mental model.

**When overlays appear:** Dim or blur the backdrop. This communicates that the backdrop is NOT interactive. A context menu over an undimmed screen implies everything behind it is still tappable.

---

## GESTURE TIMING RULES

- **Lightweight, reversible actions** (overlays, peeks) → trigger DURING gesture, past a distance threshold
- **Destructive / high-commitment actions** (delete, dismiss app) → trigger ON GESTURE END only
- **Peeking** → never trigger on distance; only on gesture end

**Immediate physical feedback + delayed commitment = correct feel.**
A gesture with zero feedback until the threshold feels broken.

---

## RESPONSE TIMES
```
< 100ms   Instant — no feedback needed
100–400ms Acceptable — user stays in flow
> 400ms   Show loading indicator
> 2000ms  Flow is broken — user disengages
```

---

## FEEDBACK RULES
- Feedback should be **relative to its trigger**: inline checkmark on successful copy, NOT a toast
- Highlight the specific input on validation error, not just a top-level error message
- **The quietest feedback that communicates the state** is the right feedback
- Errors that call attention to themselves are bad design — not bad engineering

---

## FORM RULES
- Labels above inputs always (never placeholder-only)
- Validate on blur, not on keystroke
- Error message below the field, specific ("8+ characters required" not "Invalid")
- Wrap inputs in `<form>` — enables Enter to submit
- Single-column for conversational flows

---

## VISUAL HIERARCHY
```
Display / hero:    48–64px / 700 / -0.03em
Page title:        28–36px / 700 / -0.02em
Section heading:   20–24px / 600 / -0.01em
Body:              15–16px / 400 / 0
Label / meta:      11–13px / 400 / +0.05em
```
**Max 3 hierarchy levels visible at once.** If everything is semibold, nothing is.

---

## PROXIMITY RULES (GESTALT)
- Things close together = related. Use 4–8px within a group, 24–48px between groups.
- Tighter spacing between label + input than between separate fields.
- Proximity does grouping work — you often don't need a border or card wrapper if spacing is right.
- Same visual treatment = same semantic role (all disabled states same opacity, all CTAs same style).
- A card clipped at the bottom = "scroll for more" — use intentionally, not accidentally.

---

## ACCESSIBILITY
```
Touch targets:    min 44×44px
Focus ring:       box-shadow (not outline — ignores border-radius in older Safari)
                  box-shadow: 0 0 0 2px accent-color
Screen reader:    aria-label on all icon-only buttons
Color alone:      never the sole indicator of state
Reduced motion:   @media (prefers-reduced-motion: reduce) { * { transition: none } }
Hover on mobile:  @media (hover: hover) — never show hover on touch press
Input font size:  min 16px on mobile (below this = iOS auto-zoom on focus)
```

---

## INTERACTIVITY CHECKLIST
- Input label tap → focuses the input (always)
- Toggles → take effect immediately, no confirmation
- Buttons → disable after submission to prevent duplicates
- Decorative elements → `pointer-events: none` (glows, gradients, overlays)
- No dead areas between interactive elements in lists — use padding to fill gaps
- Dropdown menus → open on `mousedown`, not `click` (feels more responsive)
- Disabled buttons → no tooltip (disabled elements aren't in tab order)
- `user-select: none` on interactive element inner content

---

## WHAT MAKES AN INTERFACE BEAUTIFUL (VS. MERELY CORRECT)

**The soulless AI design signature** — any of these alone is forgivable; several together = AI slop:
- Inter or Roboto everywhere, no variation
- Purple or blue gradient hero on white, green for success, grey for everything else
- White cards on grey background with colored left accent border
- `box-shadow: 0 2px 8px rgba(0,0,0,0.1)` copied everywhere unchanged
- Pill-shaped buttons, brand purple fill, nothing distinctive
- Lucide icons, default stroke weight, unadapted to context
- Three-column feature grid. Two-column hero (headline left, mockup right). Footer with four columns.
- Abstract blob illustrations, floating UI mockups, three-person teams with laptops
- Empty state: light grey icon centered on white, brief paragraph, one button

**The antidote: specificity.** Generic is the first idea. Specific is the right one.

**Ask: what real-world reference solved this same information problem already?**
- Flighty → airport departure boards (50 years of solving stressed-traveler information design)
- Mela → kitchen context (hands wet, phone 3 feet away, eyes on the pan)
- Financial interfaces → ticker tape, trading floor conventions
- Medical interfaces → clinical readability standards

The physical world has already solved most information design problems for high-stakes contexts. Borrow from it — your design gains authority without users knowing why.

**The 20 ideas rule:** Generate 20 design directions before committing to one. At 3–5 you're still answering the obvious question. At 12–15 you start getting somewhere interesting. The discipline prevents defaulting to the first thing that works.

**Restraint test:** Cover up each element. Does the design lose information or hierarchy without it? If no: remove it. Beautiful design is mostly subtraction.

**Commit to one constraint.** Personality requires commitment. A half-committed personality is worse than none. If the app is going to feel like something, it has to feel like it throughout — not just in the hero.

---

## TOKEN NAMING
```
--color-bg-base         → Page background
--color-bg-surface      → Card / container
--color-bg-elevated     → Modal / popover
--color-text-primary    → Main body text
--color-text-secondary  → Supporting text
--color-text-muted      → Placeholder, meta
--color-brand-primary   → Primary action color
--color-border-default  → Normal borders
--color-destructive     → Error / delete
--color-success         → Success states
```

---

## DESIGN SYSTEMS WORTH STUDYING
1. **Radix Colors** — 12-step scales, dark mode ready, perceptually even
2. **Linear** — industrial dark UI, highest craft bar in the industry
3. **Primer (GitHub)** — developer-focused, dense, accessible
4. **shadcn/ui** — token architecture, React components
5. **Material 3** — role-based color system, a11y first

---

## SHADOWS — BEAUTIFUL, NOT GENERIC

**Light comes from above and slightly left.** Every shadow on the screen should behave as though cast from the same light source. When shadows are inconsistent, the UI looks like disconnected parts, not a unified object.

**As elevation increases:**
```
↑ Vertical offset (shadow moves further away)
↑ Blur radius (shadow softens)
↓ Opacity (shadow fades)
```
Press your hand on a desk and slowly lift it — watch what happens to the shadow. That's the mental model.

**Layered shadows > single shadow:**
One `box-shadow` produces a flat, blurry box. Layering 2–3 shadows with slightly different offsets and blurs produces something that looks like it has real depth.
```css
/* Subtle elevation — card */
box-shadow:
  0px 1px 2px rgba(0,0,0,0.07),
  0px 2px 4px rgba(0,0,0,0.05),
  0px 4px 8px rgba(0,0,0,0.03);

/* Medium elevation — dropdown */
box-shadow:
  0px 2px 4px rgba(0,0,0,0.08),
  0px 4px 8px rgba(0,0,0,0.06),
  0px 8px 16px rgba(0,0,0,0.04);

/* High elevation — modal */
box-shadow:
  0px 4px 8px rgba(0,0,0,0.10),
  0px 8px 16px rgba(0,0,0,0.08),
  0px 16px 32px rgba(0,0,0,0.06);
```

**Color-match your shadows.** A grey shadow on a colored background looks wrong — it desaturates the surface. Instead, use the surface's hue at lower saturation and brightness.
```
Surface: hsl(220, 60%, 50%)
Shadow:  hsl(220, 40%, 20%) at low opacity  ← same hue, darker and less saturated
NOT:     rgba(0, 0, 0, 0.2)  ← this produces a dead grey cast
```

**Which elements are inset (pressed in) vs. outset (raised):**
```
Inset (concave, recessed):     text inputs, pressed buttons, slider tracks, checkboxes, radio buttons
Outset (convex, elevated):     cards, unpressed buttons, popovers, slider thumbs, FABs
```

---

## GRADIENTS — AVOIDING THE GREY DEAD ZONE

CSS gradients interpolate in RGB by default. When two saturated colors mix through RGB, they produce a grey midpoint. Yellow → Blue goes grey in the middle. That's the grey dead zone.

**Fix 1: Add a mid-color stop** that routes the gradient around grey. For yellow→blue, add green or teal at 50%.

**Fix 2: Use HSL interpolation** (modern browsers):
```css
background: linear-gradient(in hsl, hsl(60,100%,50%), hsl(240,100%,50%));
```
This routes through hue angles rather than RGB channels — keeps saturation high throughout.

**Fix 3: Generate intermediate stops programmatically** using chroma.js with HCL color mode for perceptually even gradients.

**Scrim technique** (for text over images — subtle, few people use it):
An elliptical radial gradient from `rgba(0,0,0,0.4)` center to `transparent` edges, placed behind text. More natural-looking than a flat overlay.

**Floor fade** (for hero images with text at bottom):
Subtle gradient from `transparent` at 50% to `rgba(0,0,0,0.3)` at 100%, applied over the bottom of an image. Mirrors natural lighting (darker at bottom). Almost invisible but makes text reliably legible.

---

## TEXT HIERARCHY — POP AND UN-POP

Making text stand out is not just about making it bigger or bolder. Use **contrasting attributes** to create hierarchy without visual noise.

**To make text pop (draw attention):** increase one or more of — size, weight, contrast, color saturation, capitalization (sparingly).

**To un-pop text (de-emphasize):** decrease contrast (lighter color, not grey — use a lower-opacity version of the text color), smaller size, lighter weight. Do not use italics for de-emphasis — italic implies quotation or emphasis, not hierarchy.

**The key insight:** big + light = pop. Small + dark = pop. Big + dark = VERY pop (use sparingly — for key numbers, hero stats). Avoid big + heavy + dark for body text — it reads as shouting.

**Contrasting attributes for hierarchy (pick 2–3 per level):**
```
Size: 32px vs 16px vs 13px
Weight: 700 vs 400
Color: #1c1814 vs #786b5e vs #b0a898
Capitalization: Title Case vs CAPS (labels only)
Letter spacing: 0 vs +0.05em
```

**Black and white first rule:** Design in greyscale before adding color. If the hierarchy isn't clear in greyscale, color won't save it — it'll just add noise. Color should *reinforce* hierarchy that already works structurally.

---

## WHITESPACE — START WITH MORE THAN YOU THINK

Default instinct: tight. The correct approach: loose, then tighten only where density earns its place.

**Double your whitespace** as a starting point. Most developers and first-draft designers cut whitespace by default. Designers with trained eyes start with generous space and reduce only when content demands proximity.

**Where whitespace does structural work:**
- Between unrelated sections: 40–64px
- Between related items within a group: 8–16px
- The *difference* between these two values is what creates perceived hierarchy
- If adjacent spacing values are too similar, the grouping is invisible

**Whitespace doesn't mean empty.** Intentional whitespace is structural — it creates groups, guides the eye, and communicates which elements belong together. Whitespace removed from the wrong place collapses meaning.

---

## EMPTY STATES — THREE TYPES, THREE JOBS

Empty states are not error states. They are design opportunities. Most are ignored; the great ones are remembered.

**Type 1: First-use (blank slate)**
User just created an account or project. Nothing exists yet. The job: reduce anxiety, explain the value, give a clear first action.
- Copy pattern: "Start by [specific action]" — NOT "You don't have any X yet"
- Include a primary CTA that does the first thing
- Illustration should show the *outcome* of using the feature, not the emptiness itself
- Optional: provide templates or examples to lower the activation energy

**Type 2: No results (search/filter came up empty)**
The job: redirect, not apologize.
- "No results for 'walnut boards'" → suggest clearing the filter, broadening the search, or checking spelling
- Never just show an empty container with no guidance — that looks broken
- Consider: show nearby or related results anyway

**Type 3: Completion (everything done)**
The job: celebrate and reset.
- GitHub's "all issues cleared" screen with Octocat taking a walk in the forest
- This is the most under-designed state. It's where the app's personality can shine.
- Don't just go blank — acknowledge the accomplishment, suggest what's next

**Copy rules for empty states:**
- Positive framing: "Add your first project" beats "No projects found"
- Specific action: "Add a piece" beats "Get started"
- Explain the benefit: one sentence on why this feature exists
- Never use system/technical language ("No entities in this collection")

---

## MICROCOPY — WORDS ARE PART OF THE UI

Every label, placeholder, tooltip, error, and button copy is a design decision. Bad copy makes a polished UI feel broken. Good copy makes a plain UI feel considered.

**Error messages: describe the solution, not the problem**
```
❌ "Authentication token invalid"
✅ "There's an issue with your login — try again or reset your password"

❌ "Required field"
✅ "Email is required"

❌ "Invalid input"
✅ "Password needs at least 8 characters"
```

**Button labels: describe the outcome, not the action**
```
❌ "Submit"
✅ "Create project" / "Save changes" / "Add piece"

❌ "OK" (on a destructive confirmation)
✅ "Delete project" (makes the consequence explicit)

❌ "Yes" / "No" (on a modal)
✅ "Delete" / "Keep project"
```

**Placeholder text: supplementary, not substitute for labels**
- Placeholder disappears on input — it cannot replace a visible label
- Use for format hints: "e.g. 36" or "Oak, maple, plywood…"
- Never use placeholder as the field label — it creates memory load

**Clear > clever.** Cleverness in copy is a seasoning, not a base. One clever line in an otherwise clear UI lands well. A clever UI throughout is exhausting.

**Tonal consistency:** The copy should sound like one person. If one screen says "Oops, something went wrong!" and another says "Error code 5003 — contact support," the product has no voice.

---

## OPTICAL ALIGNMENT — OVERRIDE THE MATH

Mathematical centering ≠ visual centering. The human eye perceives weight, not coordinates.

**Icon optical centering:** Icons with visual weight concentrated at the top feel bottom-heavy when mathematically centered. Shift them up by 1–2px. Test by squinting — it should feel balanced, not measured.

**Text and icon alignment:** When placing an icon next to text, align to the **cap height** or **optical center of the text**, not the bounding box. Most icons have invisible padding — use the visual center of the icon shape, not the bounding box edge.

**Large numbers:** Very large numerals (32px+) can feel top-heavy due to stroke distribution. Optical tracking (-0.02 to -0.04em) helps by closing space between strokes, making them feel more cohesive.

**Cards:** Content that is purely geometrically centered in a card often looks like it's sitting in the bottom half. Shift it up by 5–10% of the container height. This compensates for the visual weight of the bottom edge.

**Rounded corners:** Perfect mathematical rounding (`border-radius: 50%`) on an icon can look slightly off due to the content inside. Adjust by 1–2px based on what looks right — the measurement is a starting point, not a rule.

---

## VISUAL WEIGHT — BALANCING WITHOUT SYMMETRY

Visual weight is the perceived heaviness of an element — determined by size, color, density, contrast, and position.

**Elements with high visual weight:**
- Dark, saturated colors
- Large size
- Complex shapes / high detail
- Unusual position (edges and corners attract attention)
- Isolation (a single element in whitespace has higher perceived weight)

**Elements with low visual weight:**
- Light colors, low contrast
- Small size
- Simple / regular shapes
- Predictable position (center, along grid)

**Asymmetric balance:** Two small dark elements can balance one large light element. A dense text block can balance a large illustration. Visual balance is not math — it's perception. Test by squinting and asking: where does my eye land first?

**The focal point:** Every screen should have one. The element with the most visual weight determines reading order. If everything competes equally, nothing is primary. If nothing competes, the screen has no energy.

---

## ELEVATION SYSTEM (CONSISTENT ACROSS THE APP)

Use 4–5 elevation levels maximum. More creates inconsistency; fewer creates flatness.

```
Level 0 — Page background: no shadow, base surface
Level 1 — Cards, inset sections: 0 2px 8px rgba(0,0,0,0.06)
Level 2 — Sticky headers, floating toolbars: 0 4px 12px rgba(0,0,0,0.08)
Level 3 — Dropdowns, popovers: 0 8px 24px rgba(0,0,0,0.12)
Level 4 — Modals, dialogs: 0 16px 40px rgba(0,0,0,0.16)
```

Establish this system once. Apply it consistently. Never create a one-off shadow.

