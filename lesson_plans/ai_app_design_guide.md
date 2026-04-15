# AI App Design Guide (Bonus)
## How to design and ship a real app using Claude, Claude Code, and a design tool

*A bonus resource for DESG 260. This is optional — not required for any unit or assignment.*

*Last verified: [update this date when you re-test the workflow]*

---

## Who this guide is for

You've done some work in Unit D. You know how to research a problem, interview users, and design screens in Figma. Now you want to **actually ship a working app** — something a friend can open on their phone or in a browser.

You are not a programmer. You probably won't become one through this guide. That's fine. The goal here isn't to teach you to code — it's to teach you how to **form intent clearly enough that AI can render it**. The thinking is still yours. The typing is mostly the AI's.

**One honest tension to name upfront:** Unit D's assignment treats AI prototypes as *disposable*. You research, validate, prototype with AI, throw the prototype away, and hand-build the final screens in Figma. That protects craft skills. This bonus guide does the opposite: **AI builds the shipped product, and you refine it with a design tool.** Both are legitimate workflows. They teach different muscles. Use Unit D's approach for your capstone portfolio piece. Use this guide when you want to see something real in the world.

---

## The workflow at a glance

1. **Research** — talk to 3 potential users before touching AI
2. **Product brief** — write a one-page brief with Claude
3. **DESIGN.md** — write a design spec with Claude
4. **Build** — hand brief + DESIGN.md to Claude Code, save to GitHub
5. **Refine the UI** — explore in Figma (default) or Paper (alternative)
6. **Deploy** — web via Vercel (default) or TestFlight (optional stretch)

**Accounts you'll create along the way:** a Claude account (Step 1), a GitHub account (Step 3, *free*), and a Vercel account (Step 5, *free*). You don't need any of them up front — create each one when the guide tells you to, and your brain won't be cluttered with signup forms while you're trying to design.

The forming-intent work lives in Steps 1–3. Steps 4–6 are rendering. The guide won't stop you from skipping Steps 1–3, but if you do, you'll just get the same generic AI app everyone else is getting.

---

## Before you start: do the research

Don't skip this. Really.

**Talk to 3 potential users.** Ask them about the problem you think your app solves — without pitching your app. Use the Mom Test principles from Unit D: ask about specific past behavior, not hypothetical future use.

Take notes. The quotes, frustrations, and workarounds you hear are the raw material for your brief. **Claude cannot make up user research for you.** If you hand Claude a vague problem, you get a vague app.

---

## Step 1 — Write a product brief (with Claude)

**Why:** A one-page brief is the most valuable document in this workflow. It captures *what you're building and for whom* in a form Claude Code can actually use. Without it, the AI guesses.

### What to do

1. Open [claude.ai](https://claude.ai) in a new conversation.
2. Open the [product brief template](templates/product_brief_template.md) in another tab.
3. Paste this prompt into Claude, then paste your interview notes below it:

> ```
> I'm designing an app. I want you to help me write a one-page product
> brief using the template below. Use my interview notes — don't invent
> users or problems. Ask me clarifying questions one at a time before
> writing anything. Push back if I'm being vague.
>
> TEMPLATE:
> [paste the contents of product_brief_template.md here]
>
> INTERVIEW NOTES:
> [paste your raw notes from your 3 user conversations here]
> ```

4. Answer Claude's questions. Don't rush. The conversation is the work.
5. When Claude drafts your brief, save it as `product_brief.md` in a new folder for your project.

### Review & edit

Before moving on, reread your brief and ask yourself:
- [ ] **Did Claude invent anything?** Especially in the "Target User" and "Problem" sections — make sure every claim traces back to your interviews.
- [ ] **Is the core flow one thing, or a feature list in disguise?** One flow. One user. One goal.
- [ ] **Is "Out of Scope" doing real work?** If it's empty or obvious, you haven't cut anything yet.
- [ ] **Edit at least one section by hand** before moving on. Your judgment needs to be on the page.

---

## Step 2 — Create your DESIGN.md (with Claude)

**Why:** DESIGN.md is a persistent design spec. Unlike references in a chat window, this file lives in your project folder, and Claude Code rereads it every session. It's the single best way to keep your app's visual intent consistent across weeks of work.

### What to do

1. Gather 3–5 reference screenshots first. Apps, websites, artifacts — anything you want your product to feel like. Save them to a `references/` folder inside your project folder.
2. Open the [DESIGN.md template](templates/DESIGN_template.md).
3. In Claude (same or new conversation), paste:

> ```
> I'm creating a DESIGN.md for my app. Help me fill out the template
> below. Here's my product brief and my reference screenshots — I'll
> describe each reference in my own words.
>
> TEMPLATE:
> [paste DESIGN_template.md]
>
> PRODUCT BRIEF:
> [paste your product_brief.md]
>
> REFERENCES:
> [for each one: a short description + why you like it]
>
> Go one section at a time. Don't move on until I've signed off.
> Challenge me if my color/type/tone choices contradict each other.
> ```

4. Work through each section with Claude. Pick fonts from [Google Fonts](https://fonts.google.com). Use [Coolors](https://coolors.co) if you need help generating a palette.
5. Save the final file as `DESIGN.md` in your project folder.

### Review & edit

- [ ] **Every color is a hex code**, not "blue."
- [ ] **Every reference has a "why it matters"**, not just a screenshot.
- [ ] **The microcopy section has real words you'd actually ship** — not "Success!" but the specific sentence your app will say.
- [ ] **You'd be embarrassed if a designer you admire read this and it was vague.**

---

## Step 3 — Build with Claude Code

**Why:** Claude Code is a terminal tool that reads files in a folder and writes code there. Because it reads your `product_brief.md` and `DESIGN.md`, it can scaffold an app that actually reflects your intent — not a generic template.

### One-time setup

You only do this once, the first time you ever use Claude Code.

1. **Install Node.js.** Go to [nodejs.org](https://nodejs.org) and install the LTS version. This adds two terminal commands you'll need: `node` and `npm`.
2. **Install Claude Code.** Open Terminal (Mac) or PowerShell (Windows) and run:
   ```
   npm install -g @anthropic-ai/claude-code
   ```
3. **Sign in.** Run `claude` in your terminal and follow the prompts to sign in with your Claude account.
4. **Install git.** Git is how you save versions of your project — think of it as "Time Machine for your code." Mac: run `git --version` in your terminal; if it's not installed, it'll prompt you to install the developer tools. Windows: download from [git-scm.com](https://git-scm.com).
5. **Create a free GitHub account** at [github.com](https://github.com). GitHub is where your project snapshots live online. You'll need this later for deploying, but creating the account now means Claude Code can push to it whenever you're ready.

If any of the above fails, jump to [Appendix B: Common Claude Code errors](#appendix-b-common-claude-code-errors).

**Mental model for git and GitHub:** You are not learning to be a software engineer. Treat git like saving a document — you'll make a "save point" (a *commit*) whenever the app is in a state you'd be sad to lose. GitHub is where those save points sync online. Claude Code handles the mechanics; you just decide when to save.

### Scaffold the app

1. Make a new folder on your Desktop, named after your project. Move your `product_brief.md`, `DESIGN.md`, and `references/` folder into it.
2. In your terminal, navigate into that folder:
   ```
   cd ~/Desktop/your-project-name
   ```
3. Start Claude Code:
   ```
   claude
   ```
4. Paste this starter prompt:

> ```
> Read product_brief.md and DESIGN.md. Then scaffold a Next.js web app
> with Tailwind CSS that implements the core flow described in the brief.
>
> Rules:
> - Follow DESIGN.md exactly — colors, fonts, type scale, components.
> - Build only the core flow. No extra features.
> - Use Lucide icons.
> - Stop and ask me a question whenever the brief or DESIGN.md is
>   ambiguous. Do not guess.
>
> When scaffolding is done, tell me how to run the app locally.
> ```

5. Claude Code will ask you questions, create files, and eventually tell you to run `npm run dev`. Do that. Open the URL it prints (usually `http://localhost:3000`) in your browser.

### Save your first working version (GitHub)

**Do this the moment the app first runs.** This is your "nothing else has broken yet" baseline. Future you will thank you.

Back in Claude Code, paste:

> ```
> Set up git for this project and push it to a new private repository on
> my GitHub account. Name the repo after this folder. Walk me through
> anything I need to click or paste. When it's done, make an initial
> commit called "First working scaffold" and push it.
> ```

Claude Code will guide you through authenticating with GitHub (usually a one-time browser login), creating the repo, and pushing your code. When you refresh your GitHub page, you should see your project.

**Why this matters:** From now on, every time Claude Code makes a change you like, you'll save a new commit. If a later change breaks something, you can ask Claude Code to "revert to the last working commit" and get your app back. Without git, a single bad edit can cost you a weekend.

### Iterate

From here on, working with Claude Code is a conversation. Try:
- "The primary button should have more vertical padding — use 12px top/bottom instead of 8px."
- "The empty state on the home screen is too plain. Add the microcopy from DESIGN.md."
- "This screen doesn't match Reference 2. Look at the spacing and try again."

**End each working session with a commit.** When you're happy with a round of changes, say:

> ```
> Commit the current changes with a short message describing what changed,
> and push to GitHub.
> ```

You don't need to understand the git commands — Claude Code runs them. Just make it a habit: *change → check → commit*. If something breaks later, you can always come back to the last committed version.

### Review & edit

- [ ] **Does the app actually follow your DESIGN.md, or did Claude Code fall back to defaults?** Check colors, fonts, spacing.
- [ ] **Is the core flow from your brief the *only* thing implemented?** If Claude Code added features, remove them now. Scope creep is fatal.
- [ ] **Can you explain every screen to another student?** If not, you handed too much judgment to the AI.

---

## Step 4 — Refine the UI

**Why:** Claude Code will produce a functional app, but "functional" and "refined" are different. This step is where you push the visual craft from acceptable to good. You'll use a design tool to *explore visual directions* — not to reverse-engineer working code.

Pick one option. Don't try both on your first project.

### Option A: Figma (default, recommended)

You already know Figma from Units A–C. This option keeps you in familiar territory.

1. **Screenshot each key screen** from your running app (Cmd+Shift+4 on Mac, Win+Shift+S on Windows).
2. **Import into Figma.** Create one frame per screen.
3. **Redesign one screen at a time.** Change type, spacing, hierarchy, color usage. Try 2–3 visual directions for the same screen. Pick the one that best serves your product brief.
4. **Describe the change to Claude Code.** Open your project in Claude Code again and paste something like:

> ```
> I redesigned the home screen in Figma. Here's what I changed:
> - Increased the headline from 24px to 32px
> - Moved the streak counter from top-right to below the prompt
> - Added 24px of vertical breathing room between the prompt and input
> - Changed the primary button from full-width to auto-width, centered
>
> Here's a screenshot of the Figma version: [drag the PNG into Claude Code]
>
> Update the code to match. Preserve everything else.
> ```

5. Claude Code will update the code. Refresh your browser. Iterate.
6. **When a refinement round is done and you like the result, commit it.** Ask Claude Code to commit and push. Each refined screen becomes a save point you can roll back to if a later change goes sideways.

**Why this works:** You're not asking Claude Code to "make it look better" (too vague). You're describing specific, bounded changes that you decided in Figma. That's forming intent — then rendering it.

### Option B: Paper.design (alternative, experimental)

Paper is newer and less familiar, but has a tighter integration with Claude Code via its [MCP](https://modelcontextprotocol.io) server. It's worth trying if you like the idea of exploring many visual variants quickly.

1. Sign up at [paper.design](https://www.paper.design).
2. Install the Paper MCP per their docs. (Check their current setup guide — this changes.)
3. In Paper, design a few variants of one screen.
4. In Claude Code, with the Paper MCP running, say:

> ```
> Pull the [screen name] design from my Paper workspace and apply
> it to the equivalent screen in this project. Preserve the data
> flow — only change visuals.
> ```

**Caveat:** Paper MCP is evolving. If you hit rough edges, don't fight it — switch to Option A.

### Review & edit

- [ ] **Did you actually change things, or did you just approve what Claude Code produced?** Refinement without edits isn't refinement.
- [ ] **Each change you made should trace back to your DESIGN.md or your brief.** If it doesn't, update DESIGN.md so future changes stay consistent.

---

## Step 5 — Deploy

### Option A: Web via Vercel (default)

This is the easiest way to share your app. You'll get a URL anyone can open.

*Your project is already on GitHub from Step 3. That makes this step short.*

1. **Create a free account** at [vercel.com](https://vercel.com). **Sign in with the same GitHub account you used in Step 3** — this is what lets Vercel see your repo.
2. **In Claude Code, paste:**

> ```
> My project is already on GitHub and I just signed up for Vercel with
> the same GitHub account. Walk me through connecting this repo to
> Vercel and deploying it. Tell me what to click.
> ```

3. Claude Code will guide you through importing the repo into Vercel and triggering the first build. It's usually a 5-minute process the first time.
4. When done, you'll have a URL like `your-app-name.vercel.app`. That's your app. Share it.

**Bonus:** Because your app is linked to GitHub, every future commit you push automatically redeploys on Vercel. You don't have to think about deploy again after today — just commit, and the live site updates.

### Option B: TestFlight (optional, iOS only)

If you specifically want your app on an iPhone home screen via TestFlight, see [Appendix A: TestFlight walkthrough](#appendix-a-testflight-walkthrough). Warning: this requires an Apple Developer account ($99/year), a Mac, and patience for Apple's review queue. Budget a full week.

---

## Appendix A: TestFlight walkthrough

**Do not start here. Only attempt TestFlight if:**
- You specifically want a native iOS experience (not just web on mobile)
- You have access to a Mac with Xcode installed
- You have an Apple Developer account ($99/year)
- You have at least a week of buffer time

### The rough path

1. In Claude Code, ask it to convert your web app into an iOS app using [Expo](https://expo.dev) (React Native) or [Capacitor](https://capacitorjs.com) (wraps your web app in a native shell). Capacitor is the faster, less-disruptive path if your app is already web-based.
2. Install [Xcode](https://apps.apple.com/us/app/xcode/id497799835) from the Mac App Store. This is large — several GB.
3. Create an App Store Connect listing at [appstoreconnect.apple.com](https://appstoreconnect.apple.com).
4. Configure signing in Xcode with your Apple Developer account.
5. Archive and upload a build to App Store Connect.
6. Add testers in TestFlight. They'll get an email with a link to the TestFlight app.

Claude Code can help with steps 1 and 5. Steps 2–4 involve Apple's interfaces, which change frequently — check [Apple's TestFlight docs](https://developer.apple.com/testflight/) for current specifics.

**When you get stuck** (and you will), paste the exact error text into Claude Code. Xcode errors are notoriously opaque; AI is genuinely helpful for translating them.

---

## Appendix B: Common Claude Code errors

When something goes wrong, don't panic. Copy the full error text and paste it into Claude Code with "What does this mean, and how do I fix it?" The AI is very good at this. Below are the errors you're most likely to hit.

### 1. `command not found: claude`
Claude Code isn't installed or your terminal doesn't know about it. Reinstall:
```
npm install -g @anthropic-ai/claude-code
```
On Windows, you may need to close and reopen PowerShell after installing Node.js.

### 2. `command not found: npm`
Node.js isn't installed. Install the LTS version from [nodejs.org](https://nodejs.org).

### 3. `EACCES: permission denied` (Mac)
You tried to install something that needs admin privileges. Prefix with `sudo`:
```
sudo npm install -g @anthropic-ai/claude-code
```
You'll be asked for your Mac password.

### 4. `Port 3000 is already in use`
Something else is using that port. Either close the other app or, in Claude Code, ask: "Run the dev server on port 3001 instead."

### 5. `Module not found`
A dependency is missing. In your project folder, run:
```
npm install
```
Then try again.

### 6. `Unexpected token` or a big red error in the browser
Something in the code broke. Screenshot the error, paste it into Claude Code, and say: "I'm seeing this error. Fix it."

### 7. The app looks nothing like DESIGN.md
Claude Code drifted. Say: "Reread DESIGN.md and audit the current code against it. List every place the code doesn't match the spec. Fix them."

### 8. You don't know what folder you're in
Run:
```
pwd
```
It prints your current folder. If you're not in your project folder, `cd` into it:
```
cd ~/Desktop/your-project-name
```

### 9. GitHub asks for a password and nothing works
GitHub no longer accepts your account password in the terminal — you need a **personal access token** (PAT) or the GitHub CLI. Easiest path: ask Claude Code to install and set up the GitHub CLI (`gh`) for you. It handles authentication through a browser login and you never have to manage tokens.

> ```
> Install the GitHub CLI and sign me in. Walk me through the browser
> login. After I'm signed in, try pushing this repo again.
> ```

### 10. "Permission denied" when pushing to GitHub
You're probably pushing to someone else's repo, or the repo name is wrong. Ask Claude Code: "What's the remote URL of this repo, and does it match my GitHub username?" It'll diagnose and fix.

---

## A closing note

This workflow compresses into a few weekends what used to take a semester. That's a gift, but it's also a trap. **The AI is better at rendering than it is at forming.** If you skip the research, skip the brief, or let Claude Code decide your design choices, you'll ship something technically working and creatively hollow — and you'll know it.

The students who get the most out of this guide are the ones who treat Claude Code as a very fast, very literal junior collaborator. You're still the designer. The app should look like *your* work, not the AI's.

Good luck. Ship something real.

---

*Questions, errors, or improvements to this guide? Talk to your instructor or make a note for the next revision.*
