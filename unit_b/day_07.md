# Day 7 — Monday, Feb 2
## Unit B: Make It Better App

**Focus:** AI tools can accelerate rendering, but only if you've done the hard work of forming intent first.

**Targeted Learning Outcomes:** Problem Discovery & Research, Better Interactions & Experiences

---

### Desired Results

**Essential Questions:**
- EQ1: How do we identify opportunities in an existing product—and how do we know our new feature genuinely improves the experience?
- EQ2: How do AI prototyping tools change the rendering process—and what do they require from us as designers?

**Understandings:**
- U1: Usability testing is a design activity, not a validation step—it reveals problems designers cannot see on their own.
- U2: AI tools can accelerate rendering intent, but they cannot form intent. The quality of AI output depends on the clarity of your design thinking.
- U3: Moving from paper to digital is not just translating—it's an opportunity to refine, add fidelity, and test whether your decisions hold at higher resolution.

**Students Will Know:**
- K1: Current AI prototyping tools and what each is best suited for (Figma Make, v0, Lovable, Play)
- K2: The limitations and risks of AI-generated prototypes (generic design, hallucinated interactions, platform convention violations)
- K3: Basic Figma prototyping techniques and shortcuts

**Students Will Be Able To:**
- S1: Synthesize usability testing feedback into design improvements
- S2: Use AI tools to generate UI elements and evaluate/refine the output against platform conventions and their design intent
- S3: Build interactive prototypes in Figma

---

### Assignments Due
- ⛳ B2 Paper Prototype + User Task Diagram (should be complete from Day 6)
- Tested paper prototype with at least 1 person outside class

---

### Activities

1. **Warm-Up: Testing Debrief** (10 min) `[EQ1, U1, S1]`
   - Write: What surprised you most from testing your paper prototype?
   - What did users struggle with that you didn't anticipate?
   - Be ready to share one insight that changed your design

2. **Today's Learning Goals** (5 min) `[EQ1, EQ2, U1, U2, U3, K1, K3, S1, S2, S3]`
   - You've done the hard work of *forming intent*: research, user flows, paper prototypes, usability testing
   - Now we shift to *rendering intent*: translating your tested paper designs into high-fidelity digital prototypes
   - Today: We'll learn how AI tools can accelerate this process—and where they fall short
   - Preview: AI prototyping landscape, Figma prototyping demo, then work time to iterate on B3 and start going digital

3. **Direct Instruction: AI Tools for Prototyping** (25 min) `[EQ2, U2, K1, K2, S2]`

   **Part A: The Rendering Problem** (3 min)
   - **I do:** Frame the challenge you face right now:
     - You have tested paper prototypes with clear design intent
     - B4 requires a high-fidelity prototype "indistinguishable from native iOS/Android"
     - That's a big jump. How do we get there efficiently?
   - Key concept: AI is a *rendering* tool, not a *forming* tool. It can't decide what problem to solve or what users need. It can accelerate execution of decisions you've already made.

   **Part B: AI Prototyping Tool Landscape** (15 min)
   - **I do:** Walk through the current tool landscape with examples:
     - **Figma Make** — AI built into Figma; generates UI from text prompts within your existing Figma file. Best for students already in the Figma workflow.
     - **v0 by Vercel** — Generates React-based UIs from text or image input; free tier available. Produces actual running code you can preview in a browser.
     - **Lovable** — Chat-based full-stack prototype builder. Describe your app and iterate in real time with a live running prototype.
     - **Play** (createwithplay.com) — iOS-specific prototyping tool that uses real native elements and Core Animation. Prototypes feel like real iOS apps. Exports directly to SwiftUI/Xcode. Share prototypes via App Clips—no app download needed. **Free education program:** 6 months of Starter plan for students with school email verification.
   - For each: show a quick example of input → output (have screenshots or short recordings prepared)
   - **Using AI to write your prompts:**
     - The quality of what these tools produce depends entirely on the quality of your prompt
     - Use Claude (or another LLM) to help you write detailed, specific prompts for prototyping tools
     - Workflow: Describe your feature and target app to Claude → ask it to write a prompt for v0/Lovable/Figma Make → refine the prompt → paste into the tool
     - **Demo:** Show a before/after—a vague prompt vs. a Claude-refined prompt and the difference in output quality
     - This is a transferable skill: learning to describe design intent clearly in text makes you a better designer and a better collaborator

   **Part C: Limitations & Critical Evaluation** (7 min)
   - **We do:** Look at an AI-generated prototype together and critique it:
     - Does it follow iOS/Android platform conventions? (Connect to Day 6 learning)
     - Does it use real content or generic placeholder text?
     - Are the interactions standard or hallucinated?
     - Does it match the design intent you would have specified?
   - Key risks to watch for:
     - Generic "template" aesthetic that doesn't match your target app's design language
     - Interactions that look plausible but don't follow platform norms
     - Over-reliance: accepting AI output without evaluating against your tested design
   - Rule of thumb: AI output is a *starting point for refinement*, not a finished deliverable
   - **Important policy:** You may use AI tools freely for your B3 digital prototype, but your final B4 high-fidelity prototype must be designed in Figma without AI. B3 is where you learn what AI can do; B4 is where you prove what *you* can do.
   - Ask: What can you learn from AI-generated output that will help you build better screens yourself?

4. **Figma Prototyping Demo** (20 min) `[K3, S3, S2]`
   - **I do:** Essential Figma prototyping techniques
     - Connecting frames with prototype mode
     - Click/tap interactions
     - Smart Animate basics for transitions
     - Device preview on mobile
   - **I do:** Quick demonstration of Figma Make
     - Show how to prompt Figma Make with a description based on a paper prototype
     - Show how to refine the AI output manually in Figma
   - **Key shortcuts** for speed:
     - `R` for rectangle, `T` for text, `F` for frame
     - `Cmd/Ctrl + D` to duplicate
     - Hold `Opt/Alt` while dragging to duplicate
     - `Shift + A` for auto layout
   - **We do:** Build a simple 2-screen prototype together
   - Reminder: AI tools are great for getting your B3 digital prototype started quickly, but **your final B4 high-fidelity prototype must be designed in Figma without AI tools.** Use B3 to learn and explore with AI; use B4 to demonstrate your own craft. The result must be indistinguishable from the native app.

5. **Work Session: B3 Digital Prototype** (remaining ~60 min) `[EQ1, EQ2, U1, U2, U3, S1, S2, S3]`

   **What you're working on:**
   - **B3 Digital Prototype:** Translate your tested paper prototype into an interactive Figma prototype
     - Match the existing app's design language (typography, spacing, color, interaction patterns)
     - Try describing your screens to Figma Make, v0, or Lovable and iterate from the output
     - If designing for iOS, explore Play for native-feeling prototypes
     - Or build from scratch in Figma — whatever approach gets you to high fidelity fastest
   - **User Testing (Round 2):** Test your digital prototype with at least 2 people (not classmates)
   - **If you used an AI tool:** Check every screen against your paper prototype and platform conventions. What did it get right? What needs fixing? Remember: AI is allowed for B3, but your final B4 prototype must be built in Figma without AI.

   **Instructor circulating for 1:1s:**
   - Did your paper prototype testing reveal genuine usability issues?
   - How are you prioritizing what to fix in the digital version?
   - What approach are you taking — AI tools, pure Figma, or a combination?
   - If using AI tools: What did you keep from the AI output? What did you change and why?

   **B3 Due: Before Day 8 on Learning Suite**
   - PDF with link to Figma digital prototype
   - Testing notes from user testing (at least 2 people)
   - Format as a slide for your final documentation

**Total time:** ~120 minutes

---

### Alignment Check

| Code | Desired Result | Activities |
|------|----------------|------------|
| EQ1 | How do we know our new feature improves the experience? | 1, 2, 5 |
| EQ2 | How do AI tools change rendering—and what do they require? | 2, 3, 5 |
| U1 | Usability testing reveals unseen problems | 1, 2, 5 |
| U2 | AI accelerates rendering but cannot form intent | 2, 3, 5 |
| U3 | Paper-to-digital is a refinement opportunity | 2, 5 |
| K1 | AI prototyping tools and their strengths | 2, 3 |
| K2 | AI limitations and risks | 3 |
| K3 | Figma prototyping techniques | 2, 4 |
| S1 | Synthesize testing feedback | 1, 5 |
| S2 | Use and evaluate AI tool output | 3, 4, 5 |
| S3 | Build Figma prototypes | 4, 5 |

---

### Homework
- ⛳ B3 Digital Prototype + User Testing Round 2 (due on Learning Suite before Day 8)
- Test your digital prototype with at least 2 people (not classmates)
- Continue refining digital prototype in Figma
- Bring your laptop to Day 8 for extended work session

---

### Resources
- Figma Prototyping Basics: https://help.figma.com/hc/en-us/articles/360040314193-Guide-to-prototyping-in-Figma
- Smart Animate: https://help.figma.com/hc/en-us/articles/360039818874-Create-advanced-animations-with-smart-animate
- Figma Make (AI features): https://www.figma.com/ai/
- v0 by Vercel: https://v0.dev/
- Lovable: https://lovable.dev/
- Play (iOS prototyping): https://createwithplay.com/
- Play Education Program: https://learn.createwithplay.com/en/articles/10317719-play-for-education-program
