# Bonus Session — AI Fishing Demo
## Using AI to Figure Out Anything You Don't Yet Know

*A 60-minute standalone session. Not tied to a specific unit. Deliver anytime after Unit B, when students already have experience with AI prototyping tools and are asking "okay, but how do I use AI for X?"*

### Focus
The real skill isn't prompting — it's directing AI to extend your competence into domains you don't yet know.

### Why This Matters
AI tools will change faster than any syllabus can keep up with. What won't change is the meta-skill: how to ask AI to teach you something, push back when it's vague, demand clarity, and build your own mental model through conversation. Students who leave with this skill can apply it to Figma plugins, coding, writing, research, or anything else AI-adjacent — for the rest of their careers. The tools come and go. The fishing rod stays.

---

### Desired Results

**Essential Questions:**
- EQ1: What distinguishes "using AI" from "directing AI"?
- EQ2: How do you learn something unfamiliar *through* AI, rather than from it?
- EQ3: When should you accept AI's first answer, and when should you push back?

**Understandings:**
- U1: Working with AI is a skill of *asking better questions*, not of composing perfect prompts
- U2: The most valuable AI interaction is usually not "do this for me" but "teach me how this works"
- U3: AI's first answer is often a starting point, not an endpoint — the dialogue is the work
- U4: Demanding clarity is a discipline; AI will give you whatever level of rigor you ask for

**Students Will Know:**
- K1: Eight reusable "fishing moves" for directing AI conversations
- K2: The difference between cognitive offloading (bad) and cognitive delegation (good)
- K3: When to demand understanding vs. when to black-box a technical detail
- K4: How to capture conversational AI output into durable, reusable notes

**Students Will Be Able To:**
- S1: Deploy at least 3 of the 8 fishing moves in a real AI conversation
- S2: Push back productively when AI gives a vague or unhelpful answer
- S3: Translate a multi-turn AI conversation into a concise, self-authored summary
- S4: Identify what they still don't understand after an AI session (metacognitive calibration)

**Targeted Learning Outcomes:** Communication and Feedback, Problem Discovery & Research (Curiosity, Empathy, Humility)

---

### Assignments Due
None. This is a bonus session — no prerequisite deliverables.

---

### Pre-Class Prep (for the instructor)

- Pick a live demo topic you **genuinely don't know how to do**. The demo falls flat if it's scripted. Some options:
  - "How do I make my app send a reminder at a time the user picks?"
  - "What does `npm install` actually do, and how much do I need to understand it?"
  - "How do I embed a Figma prototype on a website?"
- Open [claude.ai](https://claude.ai) in a clean window. No prior context.
- Print or share the [AI Fishing Moves handout](handouts/ai_fishing_moves.md) — students need it in front of them during Activity 2.
- Prepare one finished artifact (a deployed app, a published case study, a working prototype) to show in Activity 1 that was produced *with* AI — so students see the destination before the journey.

---

### Activities

1. **Frame the Skill** (8 min) `[EQ1, EQ2, U1, U2]`
   - Open with the reframe: "You won't leave here knowing how to build an app. You'll leave here knowing how to use AI to figure out how to build anything."
   - Show the finished artifact you prepared. Say: "This was made by someone with no more technical background than you. What they had was a way of talking to AI. That's what we're learning today."
   - Distribute the **AI Fishing Moves handout** (8 moves). Don't explain them yet — tell students they'll watch you use them, and should try to spot each one during the next activity.
   - Connect to forming/rendering: "Forming intent means knowing what you want. AI can help render it — but only if you can direct the rendering. Directing is the skill we're practicing."

2. **Live Demo: "Stuck and Narrating"** (17 min) `[EQ1, EQ2, EQ3, U1, U3, U4, K1, K3]`
   - Open Claude in front of the class. Use the topic you prepared — something you genuinely don't know.
   - **Narrate your strategy out loud.** Every move you make on the handout, say it: *"Notice I'm not asking 'how do I do this' — I'm asking 'what are the trade-offs.' That's move #2."*
   - Key moments to deliberately model:
     - Push back on a vague answer ("that's not specific enough — give me the minimum viable version")
     - Reject the first answer ("is there a simpler way?")
     - Demand audience-appropriate explanation ("explain this like I'm a design student who's never seen code")
     - Ask AI to predict your confusion ("where am I going to get stuck next?")
     - Capture the result ("summarize what we just figured out so I can paste it into my notes")
   - Resist the urge to perform expertise. The demo works *because* you're struggling in real time. That's the curriculum.

3. **Paired Practice: "Fish for Something You Don't Know"** (15 min) `[K1, K4, S1, S2, S3, S4]`
   - Students pair up. Each pair picks **one** thing they don't currently know how to do. Examples to offer:
     - "How would users save their progress in an app?"
     - "How do I make a case study site that's embeddable in my portfolio?"
     - "What's actually happening when I deploy a site?"
     - "How would I add user accounts?"
   - They use [claude.ai](https://claude.ai) (browser only — **no installs**) to *understand* the answer. Not build. Not execute. Just understand.
   - **Deliverable:** a 3-sentence "here's how I'd approach this," written by the student in their own words — not pasted from Claude. The 3-sentence constraint is intentional: it forces synthesis and blocks cognitive offloading.
   - Instructor floats and listens, but does not rescue. Struggle is the point.

4. **Trade and Critique** (12 min) `[S3, S4, K4]`
   - Each pair swaps their 3-sentence answer with another pair.
   - Partner pair reads it and asks two questions:
     1. *Could you actually do this now? Why or why not?*
     2. *What's still unclear — what would you need to learn next?*
   - This is metacognitive calibration in disguise. Students practice identifying what they still don't know — the most valuable self-regulated learning move.

5. **Debrief: Naming the Meta-Pattern** (8 min) `[EQ1, EQ2, EQ3, U1, U2, U3, U4]`
   - Ask 2–3 pairs to share what moves they used and which worked.
   - Surface patterns you heard while floating: "Pair A refused Claude's first answer — that's move #6." "Pair B asked Claude to predict their confusion — that's move #3."
   - Close with the durability line: *"Every AI tool in your career will come and go. The 8 moves on your handout will not. Keep that paper. Use it."*
   - Point students to the [AI App Design Guide](ai_app_design_guide.md) as the "next step if you want to actually ship something."

**Total time:** 60 minutes

---

### Alignment Check

| Code | Desired Result | Activities |
|------|----------------|------------|
| EQ1 | Using AI vs. directing AI | 1, 2, 5 |
| EQ2 | Learning through AI, not from it | 1, 2, 5 |
| EQ3 | When to accept vs. push back | 2, 5 |
| U1 | Asking better questions, not perfect prompts | 1, 2, 5 |
| U2 | "Teach me" vs. "do this" | 1, 2, 5 |
| U3 | First answer is a starting point | 2, 5 |
| U4 | Clarity is a discipline | 2, 5 |
| K1 | Eight fishing moves | 1, 2, 3 |
| K2 | Offloading vs. delegation | 1 |
| K3 | When to demand understanding vs. black-box | 2 |
| K4 | Capture conversation into notes | 3, 4 |
| S1 | Deploy at least 3 moves | 3 |
| S2 | Push back productively | 3 |
| S3 | Translate conversation to self-authored summary | 3, 4 |
| S4 | Identify what you still don't understand | 4 |

---

### Homework
None required. Optional extensions for motivated students:
- Pick another thing you don't know how to do. Practice the 8 moves on it. Write a 3-sentence summary and keep it.
- Read the [AI App Design Guide](ai_app_design_guide.md) if you want to go from "understanding how" to "actually shipping something."

---

### Facilitator Notes

- **Expect real silence during Activity 2.** Watching someone work with AI in real time is less viscerally engaging than doing it yourself — until the dividend arrives in Activity 3. Trust the slow opening.
- **Resist rescuing struggling pairs** in Activity 3. The experience of being stuck and asking AI better questions *is* the lesson. If you intervene, you replace AI as their Socratic partner and teach the wrong lesson ("when I'm stuck, I ask the teacher").
- **If a pair finishes early**, give them a second topic — don't let them polish the first. Rehearsing the moves on multiple topics is how the skill generalizes.
- **The 3-sentence constraint is load-bearing.** Do not let students write a longer summary. The whole point is forced synthesis.
- **If Claude produces something visibly impressive during the demo**, name it: "That's what happens when I direct it well. When I'm vague, I get vague back. The rigor comes from me, not from Claude."

---

### Resources
- [AI Fishing Moves — student handout](handouts/ai_fishing_moves.md)
- [AI App Design Guide](ai_app_design_guide.md) — the full workflow for students who want to continue
- [AI Self-Directed Learning](AI-self-directed-learning.md) — research-grounded principles this session operationalizes (especially Principles 1, 3, 6, 7, 10)
- [claude.ai](https://claude.ai) — the only tool needed for this session
