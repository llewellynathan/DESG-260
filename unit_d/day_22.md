# Day 22 — Wednesday, Mar 25
## Unit D: Neue App (Capstone)

**Focus:** A prototype that doesn't move is a wireframe with better fonts.

**Why This Matters:** Your high-fidelity screens look great as static frames — but apps are not posters. Users expect things to respond, transition, and flow. Today you learn the mechanics of Figma prototyping: hotspots, flows, interaction details, Smart Animate, overlays, and scroll behaviors. By the end of class, your screens will feel like a real product. D9 requires 2 custom microinteractions. D10 requires an animated walkthrough video. Today is where you build those skills.

**Targeted Learning Outcomes:**
- Better Interactions & Experiences
- Critical Analysis of Form and Format
- Familiarity and Distinctiveness
- Design Strategy

---

### Desired Results

**Essential Questions:**
- EQ1: What makes a prototype feel like a real app instead of a slideshow?
- EQ2: When does motion help the user, and when does it get in the way?
- EQ3: How do interaction details (trigger, action, easing, duration) change the user's perception of quality?

**Understandings:**
- U1: Prototyping is interaction design, not just screen linking — every transition communicates something about the relationship between screens
- U2: Smart Animate is layer-name matching, not magic — understanding the mechanism gives you control over the result
- U3: Easing and duration are the difference between "feels right" and "feels cheap" — these are craft decisions, not arbitrary choices

**Students Will Know:**
- K1: How to build a complete Figma prototype flow (starting frame, hotspots, connections, flow naming)
- K2: The anatomy of an interaction: trigger (tap, drag, hover, delay), action (navigate, overlay, swap, scroll to), destination, animation type (instant, dissolve, move in/out, push, slide in/out, Smart Animate), easing curve, and duration
- K3: How Smart Animate works mechanically: matching layer names between frames, Figma interpolating position/size/opacity/rotation/fill
- K4: Component variants as state machines — using variant swaps for toggle states, button presses, input focus, and other microinteractions
- K5: Overlay transitions for modals, bottom sheets, dropdown menus, and toasts
- K6: Scroll behavior setup — vertical/horizontal scroll, fixed headers, sticky elements

**Students Will Be Able To:**
- S1: Set up a clickable Figma prototype with correct flow, starting frame, and hotspot connections
- S2: Build a Smart Animate transition by duplicating a frame and modifying matched layers
- S3: Create a microinteraction using component variants (e.g., button press, toggle switch, card expand)
- S4: Configure an overlay transition (modal or bottom sheet) with proper dismiss behavior
- S5: Set appropriate easing and duration values for different interaction types

---

### Assignments Due
- ⛳ D8: High Fidelity Round 1 (in progress — bring current screens to class)
- Watch: Smart Animate tutorial (before class)

---

### Activities

1. **Warm-Up: Prototype Show & Tell** (8 min) `[EQ1, K1]`
   - Quick poll: Who has a clickable prototype right now? Who has just static frames?
   - Show 2 examples side by side: a static Figma file vs. the same file with prototype connections, animations, and overlays
   - Ask: "Which one would you want to test with a user? Which one would you put in a portfolio?"
   - Today's goal: by end of class, everyone leaves with a working clickable prototype that includes at least one animated transition

2. **Today's Learning Goals** (4 min) `[EQ1, EQ2, EQ3, U1, U2, U3]`
   - Connection to forming/rendering: You formed the intent through research and testing. You started rendering with high-fidelity screens. Today you render the *behavior* — how your app moves, responds, and flows.
   - Preview the three workshop blocks: (1) Prototype Mechanics, (2) Smart Animate + Microinteractions, (3) Overlays + Scroll + Polish
   - By end of class you will have: a clickable prototype with connected screens, at least one Smart Animate transition, and at least one microinteraction using variants

3. **Workshop Block 1: Prototype Mechanics** (25 min) `[EQ1, U1, K1, K2, S1]`

   Live demo + follow-along. Students have Figma open and replicate each step.

   **I do / You do: Setting Up a Flow** (8 min)
   - Create a flow in the Prototype tab. Name it (e.g., "Onboarding Flow," "Core Task Flow").
   - Set the starting frame. This is what plays when you hit Present.
   - Add a hotspot on a button. Walk through each field:
     - **Trigger:** On tap (most common), On drag, While hovering, After delay, Mouse enter/leave
     - **Action:** Navigate to, Open overlay, Swap overlay, Scroll to, Back, Open link
     - **Destination:** Pick the target frame
     - **Animation:** Instant, Dissolve, Smart Animate, Move in, Move out, Push, Slide in, Slide out
     - **Easing:** Ease in, Ease out, Ease in and out, Linear, Spring, Custom bezier
     - **Duration:** in ms (typical range: 200–500ms)
   - Students follow along: connect their first two screens with a tap interaction

   **I do / You do: Navigation Patterns** (10 min)
   - Back navigation: use the "Back" action so prototype respects navigation stack
   - Tab bar / bottom nav: connect each tab to its destination screen. Tip: use "Instant" animation for tab switches (tabs don't animate — they swap)
   - Show how to link multiple flows (e.g., onboarding flow leads into main flow)
   - Demonstrate Present mode: full-screen, device frame, sharing link
   - Students follow along: connect their remaining screens, add a back action, set up tab navigation if applicable

   **Quick Check** (2 min)
   - Present your prototype. Can you tap through your entire core flow? Raise hand if stuck.
   - Common problems: missing hotspots, wrong starting frame, connections pointing to wrong frame

   **Reference Card** (5 min)
   - Review quick-reference slide with:
     - Trigger types and when to use each
     - Animation types and typical use cases (e.g., "Push" for forward navigation on iOS, "Slide in from right" for detail views)
     - Duration guidelines: 150–200ms for micro (button press), 250–350ms for page transitions, 400–600ms for complex choreography
     - Easing guidelines: "Ease out" for things entering, "Ease in" for things leaving, "Ease in and out" for things moving within view

4. **Workshop Block 2: Smart Animate + Microinteractions** (30 min) `[EQ2, EQ3, U2, U3, K3, K4, S2, S3, S5]`

   **I do: How Smart Animate Actually Works** (5 min)
   - The rule: Figma matches layers by **name** between source and destination frames. If a layer has the same name in both frames but different properties (position, size, opacity, rotation, fill), Figma animates between them.
   - If a layer exists in destination but not source → fades in. Source but not destination → fades out.
   - Critical: layer names must match **exactly**. Rename layers intentionally.
   - The workflow: duplicate Frame A to create Frame B, then change what you want to animate in Frame B. Connect A → B with Smart Animate.

   **Guided Exercise 1: Card Expand** (8 min) `[S2]`
   - Walk through together, step by step:
     1. Duplicate your screen that contains a card or list item
     2. In the duplicate, resize the card to fill the screen (simulating a detail view)
     3. Move/resize text layers to their "expanded" positions
     4. Connect the card in Frame A to Frame B with Smart Animate, Ease out, 300ms
     5. Present and test
   - If students don't have a card: use a button that slides to a different position, or a nav bar that changes color

   **I do: Component Variants as State Machines** (7 min) `[K4]`
   - Create a component with variants: Default, Hover, Pressed, Disabled
   - Show the Interaction Details panel with "Change to" action on the variant
   - The result: a button that visually responds to interaction without leaving the screen
   - This is how you build microinteractions: toggle switches (on/off variants), checkboxes, expandable sections, input field focus states
   - Demo: toggle switch with two variants (off/on), connected with Smart Animate + Spring easing

   **Guided Exercise 2: Build a Microinteraction** (10 min) `[S3, S5]`
   - Pick one element in your design that has two states (button, toggle, card, menu item)
   - Create it as a component with 2 variants
   - Add interaction: On tap → Change to [other variant], Smart Animate, Spring or Ease out, 200ms
   - Test in Present mode
   - Students who finish early: add a third state, or try a different easing curve and compare

5. **Workshop Block 3: Overlays, Scroll, and Polish** (18 min) `[EQ2, K5, K6, S4]`

   **I do / You do: Overlays** (8 min)
   - The difference between "Navigate to" and "Open overlay": overlays appear on top of the current screen, with optional background dimming
   - Build a bottom sheet: create the sheet as its own frame, then use "Open overlay" with "Slide in from bottom"
   - Set overlay position: manual or centered
   - Close on outside click: enable/disable
   - Background dimming: adjust opacity
   - Use cases: modals, bottom sheets, dropdown menus, snackbars/toasts, tooltips
   - Students follow along: pick one screen that should have a modal or bottom sheet, build the overlay frame, connect it

   **I do: Scroll Behaviors** (6 min)
   - Vertical scroll: set frame height shorter than content, enable "Vertical scrolling" in prototype settings
   - Horizontal scroll: same concept, horizontal direction (for carousels, image galleries)
   - Fixed elements: move header/nav bar outside the scrollable frame (or use "Fix position when scrolling" in the design panel)
   - Quick demo: a scrollable list with a fixed header and bottom nav

   **Quick Check** (4 min)
   - Present your prototype again. Do you have: (1) connected screens, (2) at least one Smart Animate transition, (3) at least one microinteraction? If not, note what's missing — that's your priority for the work session.

6. **Structured Work Session** (90 min) `[EQ1, EQ2, EQ3, U1, U2, U3, K1–K6, S1–S5]`

   Not free work — three timed rounds with specific goals.

   **Round 1: Complete Your Clickable Prototype** (30 min)
   - Goal: Every screen in your core flow is connected and navigable
   - Connect all screens with appropriate transitions (push for forward, slide back for backward)
   - Set up your tab bar / navigation if applicable
   - Test by presenting full-screen — can someone tap through your entire flow without getting stuck?
   - Instructor circulates, prioritizing students who had zero prototype connections at start of class

   **Round 2: Animation Challenge** (30 min)
   - Goal: Build 2 distinct animations/microinteractions (this is the D9 requirement)
   - Suggested targets (pick 2):
     - Onboarding screen transition (Smart Animate with staggered elements)
     - Button press feedback (component variant with scale/color change)
     - Card expand to detail (Smart Animate)
     - Toggle or checkbox (component variant swap)
     - Bottom sheet or modal (overlay with slide-in)
     - Loading state or success confirmation (Smart Animate with opacity + scale)
     - Tab switch with content crossfade
   - Instructor circulates with feedback on easing and timing — most common mistakes: too fast (under 150ms feels broken), too slow (over 500ms feels sluggish), wrong easing (linear feels robotic)

   **Round 3: Polish and Prepare for Testing** (30 min)
   - Goal: Your prototype is ready to put in front of a real user this weekend
   - Checklist:
     - Does your prototype start on the right screen?
     - Can you complete the core task without getting stuck?
     - Are there any dead-end screens (no way to navigate back)?
     - Does your prototype feel like the real thing when presented full-screen with a device frame?
   - Set up sharing: Prototype tab → Share → "Anyone with the link" → Copy link
   - Continue building screens if your core flow is complete
   - Apply Day 21 craft checklist to any new screens:
     1. Hierarchy: 3 levels visible in 3 seconds?
     2. Spacing: 8pt grid, groups clearly separated?
     3. Typography: 4 sizes max, correct letter spacing?
     4. Color: accent at ~10%, all text passes 4.5:1?
     5. Alignment: left edges align, concentric radii?
     6. Restraint: can you remove anything without losing info?

7. **Closing** (5 min) `[EQ1, EQ3]`
   - Show of hands: Who has a working clickable prototype? Who has 2+ animations?
   - Reminder: Test this weekend with 3+ people outside class (D9). Your prototype is now good enough to test — don't wait until it's "perfect."
   - Peer testing will happen Monday (Day 23) — bring your prototype ready to test

**Total: 180 min**

---

### Alignment Check

| Code | Desired Result | Activities |
|------|----------------|------------|
| EQ1 | What makes a prototype feel real vs. slideshow? | 1, 2, 3, 6, 7 |
| EQ2 | When does motion help vs. hinder? | 2, 4, 5, 6 |
| EQ3 | How do interaction details affect perceived quality? | 2, 4, 6, 7 |
| U1 | Prototyping is interaction design, not just screen linking | 2, 3, 6 |
| U2 | Smart Animate is layer-name matching, not magic | 4, 6 |
| U3 | Easing/duration are craft decisions, not arbitrary | 4, 6 |
| K1 | Build a complete Figma prototype flow | 3, 6 |
| K2 | Anatomy of an interaction (trigger, action, easing, duration) | 3 |
| K3 | Smart Animate mechanics (layer matching) | 4, 6 |
| K4 | Component variants as state machines | 4, 6 |
| K5 | Overlay transitions | 5, 6 |
| K6 | Scroll behaviors | 5, 6 |
| S1 | Set up clickable prototype with flow and hotspots | 3, 6 |
| S2 | Build Smart Animate transition | 4, 6 |
| S3 | Create microinteraction with component variants | 4, 6 |
| S4 | Configure overlay transition with dismiss behavior | 5, 6 |
| S5 | Set appropriate easing and duration values | 4, 6 |

---

### Homework
- ⛳ D9: Usability Testing Rd. 2 (due Mon, Mar 30 @ 5:15pm)
  - Test your clickable Figma prototype with 3+ people outside class
  - Document: observations, quotes, usability issues
  - For each issue: what specific change you made (or will make) in response
  - Include before/after screenshots where applicable

---

### Resources
- Figma Prototyping basics: https://help.figma.com/hc/en-us/articles/360040314193-Guide-to-prototyping-in-Figma
- Figma Smart Animate documentation: https://help.figma.com/hc/en-us/articles/360039818874-Create-advanced-animations-with-smart-animate
- Figma Interactive Components: https://help.figma.com/hc/en-us/articles/360061175334-Create-interactive-components-with-variants
- Figma Overflow Scrolling: https://help.figma.com/hc/en-us/articles/360039818734-Prototype-scrolling-with-overflow-behavior
- Day 21 craft principles checklist (apply to new screens during work session)
