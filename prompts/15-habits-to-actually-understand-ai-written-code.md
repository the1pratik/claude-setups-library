# 15 habits to actually understand AI-written code

I saved an Instagram reel by @ai.with.etqad (https://www.instagram.com/ai.with.etqad/reel/Db3GPZeSfMe/) and want to implement what it shows on my own machine.

## What the reel covers
Keep DECISIONS.md, FLOW.md, ARCHITECTURE.md, CONSTRAINTS.md, handoff notes, test checklists, rollback plans; read every diff; one change per request.

## Tools / resources mentioned
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview

## Proposed implementation plan
1. Add to CLAUDE.md: 'Log every meaningful decision with its reason in docs/DECISIONS.md'.
2. Ask Claude to write docs/FLOW.md: entry points, call order, which function calls which.
3. Create ARCHITECTURE.md (system map) and CONSTRAINTS.md (files/areas AI must never touch).
4. For each bug/feature keep BUG-xxx.md / FEATURE-xxx.md trails.
5. End each session with a handoff note; start the next by reading it.
6. Require a test checklist + rollback plan for each change; one change per request; read every diff; ask 'why' before 'what'.

## Caveats / uncertainty
Spoken in Hinglish; caption gives the full list. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment "WORK" below and I'll send you the full PDF 📩
> 
> Still hitting "Allow" on every AI suggestion without knowing what you just approved?
> 
> That's not collaboration. That's blind trust with extra steps.
> 
> Here's what actually separates people who ship reliable AI-assisted code from people who are constantly firefighting mystery bugs:
> 
> → Handover files: write context incrementally so the next session isn't starting from zero
> → Decisions.md: log the "why" behind every AI decision, not just the "what"
> → Explicit comments: make the flow legible, not just functional
> → Flow.md: trace exactly how execution moves between files and functions
> → Bug.md / Feature.md: a start to finish trail anyone can pick up cold
> → Architecture.md: the system map so nothing gets touched blind
> → Constraints.md: the things AI should never touch, spelled out
> → Test checklists: proof it works, not just a claim that it does
> → Rollback plans: know your way out before you need it
> → Read every diff. Every time.
> → Ask "why" before "what": catch bad reasoning before it's 200 lines of code
> → One change per request: small, traceable, reviewable
> → End of session handoff notes: 30 seconds now saves hours later
> → Version pin your context: know which model made which call
> → Own the mental model: docs support understanding, they don't replace it
> 
> I put all 15 into a full field guide (with the reasoning behind each one), free download.
> 
> Comment "WORK" and I'll send it your way 👇
> 
> [AI coding, prompt engineering, AI workflow, software engineering, developer productivity, AI assisted coding, coding with AI, claude ai, chatgpt coding, documentation habits, code review, technical debt, AI agents, vibe coding, software architecture, debugging, dev tips, engineering best practices, context engineering, AI collaboration]
> 
> #claude #trending #viral #ai #engineering

Transcript (auto, may contain errors):
> bhai gartam auto alao pe rakhe kod accept kryo aur fird formo rai ki kodini samaj mein ar hai to ye tine ce karna shurukaro AI ko holo ki ek decision sot md file bana hai and log every meaningful decision it is taking while changing your code into it aur asmi reasans bhi dalek ki asmi reasans kew liye jaise bhai thi saprochoch aur bhai was this library used abh next step mein document how execution actually travels in this code base bhai maat lab code ka entry point kaya, executions lo ka order kaya kansavangjan kis aur function ko call karrar hai aur abh i aayne ispore cycle mein kis ce koo change kia hai kis ce to mein apne kod base ki standing amas tai liye lak jai ka aur sapa jai ki kisi bhi major change ko accept krne se bhai liye ask the AI to quiz you on the changes aur agar to ms quiz mein pas auryo na sif tabhi accept karo changes seri, ways of working a document chahi ye to comment karo workon mein bhech na toom ko bhai ki follow vagar agar lo dos to

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
