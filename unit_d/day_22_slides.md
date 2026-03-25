# Day 22 Presentation Outline
## Unit D: Neue App (Capstone)

---

### Slide 1: Warm-Up
**Prototype Show & Tell** (8 min)
- Quick poll: Who has a clickable prototype? Who has static frames only?
- Two examples side by side: static screens vs. the same file with connections, animations, and overlays
- "Which would you test with a user? Which would you put in a portfolio?"
- Today's goal: everyone leaves with a working clickable prototype + at least one animated transition

---

### Slide 2: Prayer
**Prayer**

---

### Slide 3: Title
**Unit D: Neue App**
A prototype that doesn't move is a wireframe with better fonts.

---

### Slide 4: Today
**Today — Three Workshops + Structured Work**
1. Prototype Mechanics — flows, hotspots, triggers, actions, navigation
2. Smart Animate + Microinteractions — layer matching, card expand, component variants
3. Overlays + Scroll — modals, bottom sheets, fixed headers
4. Structured work session — 3 timed rounds to build your prototype

---

### Slide 5: By the end of today...
**Clickable prototype** — Every screen connected with proper navigation and transitions

**Smart Animate** — At least one animated transition using layer-name matching

**Microinteraction** — At least one interactive element built with component variants

**Ready to test** — A shareable prototype link for D9 external testing this weekend

---

### Slide 6: Why This Matters
**Why this matters**

Your screens look great as static frames — but apps are not posters.

Users expect things to respond, transition, and flow. A prototype that just jumps between screens feels like a slideshow. One that moves and responds feels like a product.

D9 requires 2 custom microinteractions. D10 requires an animated walkthrough video. Today is where you build those skills.

---

### Slide 7: Workshop 1 — Prototype Mechanics
**Workshop 1: Prototype Mechanics** (25 min)
Open Figma and follow along.

---

### Slide 8: Setting Up a Flow
**Setting Up a Flow**
1. Open the **Prototype** tab in the right panel
2. Click **+** to add a flow — name it (e.g., "Core Task Flow")
3. Set the **starting frame** — this plays when you hit Present
4. Click a button/element → drag the connection noodle to the destination frame

**Follow along now:** Connect your first two screens with a tap interaction.

---

### Slide 9: Anatomy of an Interaction
**Every connection has 6 parts:**

| Field | Options |
|-------|---------|
| **Trigger** | On tap, On drag, While hovering, After delay, Mouse enter/leave |
| **Action** | Navigate to, Open overlay, Swap overlay, Scroll to, Back, Open link |
| **Destination** | Target frame |
| **Animation** | Instant, Dissolve, Smart Animate, Move in/out, Push, Slide in/out |
| **Easing** | Ease in, Ease out, Ease in and out, Linear, Spring, Custom bezier |
| **Duration** | In ms (typical: 200–500ms) |

---

### Slide 10: Navigation Patterns
**Navigation Patterns**
- **Back button:** Use the "Back" action — respects the navigation stack
- **Tab bar / bottom nav:** Connect each tab to its destination. Use "Instant" animation (tabs swap, they don't slide)
- **Multiple flows:** Onboarding flow → Main flow. Link them with a connection from the last onboarding frame.

**Follow along:** Connect your remaining screens. Add back actions. Set up tab navigation if applicable.

---

### Slide 11: Quick Check
**Quick Check**
Present your prototype (▶ button in top right).

Can you tap through your entire core flow?

> Raise your hand if you're stuck.

Common problems:
- Missing hotspots on tappable elements
- Wrong starting frame
- Connections pointing to the wrong frame

---

### Slide 12: Interaction Reference Card
**Reference Card — Keep This Handy**

**Duration guidelines:**
- 150–200ms → micro interactions (button press, toggle)
- 250–350ms → page transitions
- 400–600ms → complex choreography (multi-element)

**Easing guidelines:**
- **Ease out** → things entering the screen
- **Ease in** → things leaving the screen
- **Ease in and out** → things moving within the screen
- **Linear** → almost never (feels robotic)
- **Spring** → playful, organic micro interactions

**Animation types:**
- **Push** → forward navigation (iOS standard)
- **Slide in from right** → detail views
- **Dissolve** → tab switches, mood transitions
- **Instant** → tab bar taps, state changes
- **Smart Animate** → when elements morph between states

---

### Slide 13: Workshop 2 — Smart Animate
**Workshop 2: Smart Animate + Microinteractions** (30 min)

---

### Slide 14: How Smart Animate Works
**Smart Animate is layer-name matching**

Figma looks at Frame A and Frame B. For every layer with the **same name** in both frames:
- Different **position** → it moves
- Different **size** → it scales
- Different **opacity** → it fades
- Different **rotation** → it rotates
- Different **fill** → it color-shifts

**Layer only in A** → fades out
**Layer only in B** → fades in

Critical: layer names must match **exactly**. Rename your layers intentionally.

---

### Slide 15: The Workflow
**The Smart Animate Workflow**
1. **Duplicate** Frame A to create Frame B
2. **Modify** the layers you want to animate in Frame B (move, resize, hide, recolor)
3. **Connect** A → B with Smart Animate + your chosen easing + duration
4. **Present** and test

That's it. The "duplicate and modify" pattern is 90% of Smart Animate work.

---

### Slide 16: Guided Exercise — Card Expand
**Guided Exercise 1: Card Expand** (8 min)
Follow along step by step:

1. Find a screen with a card or list item
2. **Duplicate** the entire frame
3. In the duplicate: resize the card to fill the screen (detail view)
4. Move/resize text layers to their "expanded" positions
5. Connect the card in Frame A → Frame B: **Smart Animate, Ease out, 300ms**
6. Present and test

> No card in your design? Use a button that slides to a different position, or a nav bar that changes color.

---

### Slide 17: Component Variants as State Machines
**Component Variants = State Machines**

A component with variants is an interactive element:
- **Default** → Hover → **Pressed** → Disabled
- **Off** → **On** (toggle switch)
- **Collapsed** → **Expanded** (accordion)
- **Empty** → **Focused** → **Filled** (input field)

**How to wire it:**
1. Create a component with 2+ variants
2. In Prototype tab: On tap → **Change to** [other variant]
3. Animation: Smart Animate + Spring or Ease out, 200ms

The element responds to interaction without leaving the screen.

---

### Slide 18: Guided Exercise — Microinteraction
**Guided Exercise 2: Build a Microinteraction** (10 min)

1. Pick one element with two states (button, toggle, card, menu item)
2. Create it as a **component with 2 variants**
3. Add interaction: On tap → Change to [other variant], Smart Animate, Spring, 200ms
4. Test in Present mode

**Finished early?** Add a third state, or try different easing curves and compare how they feel.

---

### Slide 19: Workshop 3 — Overlays & Scroll
**Workshop 3: Overlays, Scroll, and Polish** (18 min)

---

### Slide 20: Overlays
**Overlays — Layers on Top of the Current Screen**

"Navigate to" replaces the screen. "Open overlay" adds on top.

**Building a bottom sheet:**
1. Create the sheet as its own frame (sized to the sheet, not the full screen)
2. On the trigger element: **Open overlay** → select the sheet frame
3. Animation: **Slide in from bottom**, Ease out, 300ms
4. Set overlay position (bottom-center or manual)
5. Enable **Close on outside click**
6. Set background dimming (50% black is standard)

**Use cases:** modals, bottom sheets, dropdown menus, snackbars, tooltips

**Follow along:** Pick one screen that should have a modal or bottom sheet. Build it.

---

### Slide 21: Scroll Behaviors
**Scroll Behaviors**

**Vertical scroll:**
- Frame height shorter than content
- Enable "Vertical scrolling" in Prototype settings
- Content scrolls inside the frame

**Horizontal scroll:**
- Same concept, horizontal direction
- Great for carousels, image galleries, category chips

**Fixed elements (sticky headers, bottom nav):**
- Select the element → Design panel → **Fix position when scrolling**
- Or: place it outside the scrollable group

---

### Slide 22: Quick Check 2
**Quick Check**
Present your prototype. Do you have:

☐ Connected screens (tap through your core flow)
☐ At least one Smart Animate transition
☐ At least one microinteraction (component variant)

**Missing something?** That's your #1 priority in the work session.

---

### Slide 23: Work Session
**Structured Work Session** (90 min)
Three timed rounds — not free work.

---

### Slide 24: Round 1
**Round 1: Complete Your Clickable Prototype** (30 min)

Goal: Every screen in your core flow is connected and navigable.

- Connect all screens with appropriate transitions
- Push for forward, slide back for backward
- Set up tab bar / navigation
- Test full-screen — can someone tap through without getting stuck?

---

### Slide 25: Round 2
**Round 2: Animation Challenge** (30 min)

Goal: Build **2 distinct animations** (this is the D9 requirement).

Pick 2:
- Onboarding transition (Smart Animate + staggered elements)
- Button press feedback (variant with scale/color change)
- Card expand to detail (Smart Animate)
- Toggle or checkbox (variant swap)
- Bottom sheet or modal (overlay + slide-in)
- Loading state / success confirmation (opacity + scale)
- Tab switch with content crossfade

**Common timing mistakes:** under 150ms feels broken, over 500ms feels sluggish, linear easing feels robotic.

---

### Slide 26: Round 3
**Round 3: Polish & Prepare for Testing** (30 min)

Goal: Your prototype is ready for a real user this weekend.

**Checklist:**
- ☐ Starts on the right screen?
- ☐ Can you complete the core task without getting stuck?
- ☐ No dead-end screens?
- ☐ Feels like the real thing full-screen with device frame?

**Set up sharing:** Prototype tab → Share → "Anyone with the link" → Copy link

**Day 21 craft checklist** for any new screens:
1. Hierarchy: 3 levels in 3 seconds?
2. Spacing: 8pt grid, groups separated?
3. Type: 4 sizes max, correct letter spacing?
4. Color: accent ~10%, text passes 4.5:1?
5. Alignment: edges align, concentric radii?
6. Restraint: can you remove anything?

---

### Slide 27: Closing
**Before you leave**

Show of hands: Who has a working clickable prototype? Who has 2+ animations?

**D9: Usability Testing Rd. 2** (due Mon, Mar 30 @ 5:15pm)
- Test with 3+ people outside class using your prototype link
- Document observations, quotes, usability issues
- Show before/after for changes you made

**Monday (Day 23):** Peer testing in class — bring your prototype ready to test.
