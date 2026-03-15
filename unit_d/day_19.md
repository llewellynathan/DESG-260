# Day 19 — Monday, Mar 16
## Unit D: Neue App (Capstone)

**Focus:** One concept, two platforms — your app has to live somewhere else, and that changes everything.

**Why This Matters:** Your assignment requires designing for two platforms. Every platform has different strengths, constraints, and user expectations — a watch rewards glanceable information, a tablet rewards rich layouts, a desktop rewards density and keyboard shortcuts. The best designers think about *what the platform is good at* and redesign around that — keeping the core value while rethinking the interface. Today you'll learn to make those translation decisions intentionally, so your second platform feels native instead of ported.

**Targeted Learning Outcomes:**
- Better Interactions & Experiences
- Critical Analysis of Form and Format
- Design Strategy
- Familiarity and Distinctiveness

---

### Desired Results

**Essential Questions:**
- EQ1: What changes and what stays the same when a concept moves to a different platform?
- EQ2: How do platform constraints (screen size, input method, context of use) reshape an interface?
- EQ3: What did usability testing reveal about your primary platform design?

**Understandings:**
- U1: Adapting to a new platform isn't resizing — it's redesigning around different constraints and opportunities
- U2: Each platform has conventions users expect; violating them costs trust
- U3: The core value proposition stays the same across platforms, but the interface must change to serve it

**Students Will Know:**
- K1: How screen real estate, input modality, and context of use differ across platforms (phone, watch, tablet, desktop, etc.)
- K2: Key platform conventions for their chosen second platform (Apple HIG for watch, tablet layouts, desktop patterns, etc.)
- K3: Which screens and flows from their primary platform survive translation and which need to be simplified, expanded, or removed

**Students Will Be Able To:**
- S1: Analyze usability testing results and identify priority changes
- S2: Create a user flow diagram adapted for a different platform's constraints
- S3: Sketch platform-appropriate screens that feel native, not ported

---

### Assignments Due
- ⛳ D5: Usability Testing Rd. 1 (submitted before class)
  - Tested 5+ people outside class
  - Documented observations, quotes, usability issues, validation signals
  - Synthesized: patterns, top issues, what you'll change

---

### Activities

1. **Warm-Up: Testing Debrief Pairs** (10 min) `[EQ3, S1]`
   - Pair up with someone you haven't worked with recently
   - Share your single most surprising finding from D5 usability testing
   - For each finding, discuss: Is this a usability issue (they couldn't do it) or a validation issue (they wouldn't want to)?
   - Write down the top 3 changes you'll make to your primary platform based on testing

2. **Today's Learning Goals** (5 min) `[EQ1, EQ2, U1, U2, U3]`
   - **Why this matters:** Your assignment requires two platforms. Today you'll learn to design for the second one so it feels like it belongs there — not like a resized afterthought.
   - Preview:
     - What changes when your concept moves to a watch, tablet, desktop, or other platform
     - Platform conventions: what users expect and what happens when you break expectations
     - How to decide which screens survive and which get redesigned
   - Connection to forming/rendering: The intent (what your app does and why) stays the same across platforms. The rendering (how users interact with it) must change to match the platform. Same forming, different rendering.

3. **Direct Instruction: Designing Across Platforms** (30 min) `[EQ1, EQ2, U1, U2, U3, K1, K2, K3]`

   **Part A: What Changes Across Platforms** (12 min)
   - **I do:** The three dimensions that change
     - **Screen real estate:** Phone (moderate) → Watch (tiny) → Tablet (expansive) → Desktop (wide)
     - **Input modality:** Touch (phone/tablet) → Crown + small touch (watch) → Keyboard + mouse/trackpad (desktop) → Voice + gaze (Vision Pro)
     - **Context of use:** Where and when people use each platform
       - Phone: everywhere, short bursts or extended sessions
       - Watch: glanceable, mid-activity (running, cooking, commuting)
       - Tablet: lean-back, longer sessions, often at home
       - Desktop: focused work, complex tasks, multitasking
   - **I do:** What stays the same
     - Core value proposition — why the app exists
     - Brand identity — colors, typography family, personality
     - Mental model — the user's understanding of what the app does
   - **We do:** Quick exercise — for a fitness tracking app, what's the #1 screen on each platform?
     - Phone: dashboard with today's activity + history
     - Watch: current workout in progress (heart rate, timer, pace)
     - Tablet: weekly/monthly trends and detailed analytics
     - Desktop: long-term progress, data export, goal planning

   **Part B: Platform Conventions That Matter** (10 min)
   - **I do:** Breaking conventions costs trust
     - Users bring expectations from every other app on that platform
     - Navigation patterns differ: tab bar (phone), side menu (tablet), menu bar (desktop), complications (watch)
     - Information density differs: watch shows 1-2 data points per screen; desktop can show tables, sidebars, and dashboards simultaneously
   - **I do:** Quick reference for common second platforms
     - **Watch:** Glanceable. 1 action per screen. Short sessions (< 15 sec). Complications for at-a-glance data. Digital Crown for scrolling.
     - **Tablet:** More room ≠ bigger phone. Use split views, sidebars, popovers. Multi-column layouts. Apple Pencil interactions.
     - **Desktop:** Keyboard shortcuts, hover states, right-click menus. Multiple windows. Dense information display. Persistent navigation.
     - **Car dashboard:** Minimal interaction. Voice-first. Large touch targets. No reading.
   - **We do:** Name one convention you've noticed on your chosen platform that your phone app doesn't have

   **Part C: Deciding What Survives** (8 min)
   - **I do:** The translation decision framework
     - **Carry:** Core value screens that work on both platforms (maybe with layout changes)
     - **Simplify:** Screens that exist but need to be stripped down (watch gets the essential data, not the full dashboard)
     - **Expand:** Screens that benefit from more space (tablet gets richer analytics, desktop gets side-by-side comparison)
     - **Remove:** Screens that don't make sense on the new platform (onboarding wizard on a watch? Probably not.)
     - **Add:** New screens that leverage the platform's unique strengths (watch complications, desktop keyboard shortcuts panel)
   - **I do:** Example — a budgeting app
     - Phone: full app (transactions, budgets, goals, reports)
     - Watch: today's spending total, quick expense logging (amount + category), budget alerts
     - Removed from watch: detailed reports, category management, goal setting
     - Added for watch: complication showing remaining daily budget
   - **You do:** Mentally run through your app's screens — which category does each fall into for your chosen platform?

4. **D6 Assignment Introduction** (5 min) `[S2, S3]`
   - **D6: Second Platform Flow + Sketches** (due Wed, Mar 18 @ 5:15pm)
   - Choose your second platform (watch, tablet, desktop, Vision Pro, car dashboard, etc.)
   - **Deliverables:**
     - User flow diagram for your second platform — showing which screens carry, simplify, expand, or get removed
     - Annotated sketches of key screens at the platform's actual scale
     - Brief written rationale (1 paragraph): what changed from your primary platform and why
   - Reminder: you'll build high-fidelity screens for this platform later (Day 23), so invest in thinking through the flow now

5. **Work Session: Second Platform Design** (70 min) `[EQ1, EQ2, U1, U2, U3, K2, K3, S2, S3]`
   - **First 10 min:** Decide your second platform. Consider:
     - Which platform would your target user actually use alongside the phone?
     - Which platform creates the most interesting design challenge?
     - Which platform would strengthen your portfolio?
   - **Next 20 min:** Create your second platform user flow
     - Start from your primary platform flow (D4)
     - Apply the carry/simplify/expand/remove/add framework
     - Annotate: note what changed and why
   - **Next 30 min:** Sketch key screens
     - Draw at the platform's actual scale (trace a real device or use a template)
     - Focus on the 3-4 most important screens
     - Include real content (not lorem ipsum)
     - Mark tap targets, navigation patterns, and key interactions
   - **Final 10 min:** Write your rationale paragraph — what changed and why
   - Instructor circulates for 1:1 feedback on platform choices and flow decisions

**Total: 120 min**

---

### Alignment Check

| Code | Desired Result | Activities |
|------|----------------|------------|
| EQ1 | What changes vs. stays the same across platforms | 2, 3A, 5 |
| EQ2 | How platform constraints reshape an interface | 2, 3B, 5 |
| EQ3 | What usability testing revealed | 1 |
| U1 | Adapting ≠ resizing — it's redesigning | 2, 3A, 5 |
| U2 | Platform conventions cost trust when violated | 3B, 5 |
| U3 | Core value stays; interface changes | 2, 3A, 3C |
| K1 | Screen real estate, input, context differences | 3A |
| K2 | Platform conventions for chosen platform | 3B, 5 |
| K3 | Which screens survive translation | 3C, 5 |
| S1 | Analyze usability testing results | 1 |
| S2 | Create adapted user flow | 4, 5 |
| S3 | Sketch platform-appropriate screens | 4, 5 |

---

### Homework
- ⛳ D6: Second Platform Flow + Sketches (due Wed, Mar 18 @ 5:15pm)
  - User flow diagram for second platform
  - Annotated sketches showing key screens at platform scale
  - Brief written rationale: what changed from primary platform and why
  - Submit: PDF to Learning Suite

---

### Resources
- Apple Human Interface Guidelines — Platform considerations: https://developer.apple.com/design/human-interface-guidelines/
- Material Design — Adaptive layouts: https://m3.material.io/foundations/layout/understanding-layout
- watchOS design guidelines: https://developer.apple.com/design/human-interface-guidelines/designing-for-watchos
- visionOS design guidelines: https://developer.apple.com/design/human-interface-guidelines/designing-for-visionos
