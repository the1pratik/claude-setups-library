# Annotated illustrations: hand-drawn explainers of your codebase

I saved an Instagram reel by @aiwithremy (https://www.instagram.com/aiwithremy/reel/DdiMCgRz2dA/) and want to implement what it shows on my own machine.

## What the reel covers
Run a skill after a big build: it explores the project, works out what happens in what order, and draws a simple hand-drawn diagram explaining the system.

## Tools / resources mentioned
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview
- Excalidraw — https://excalidraw.com
- Mermaid — https://mermaid.js.org

## Proposed implementation plan
1. Get the 'annotated illustrations' skill from the creator (comment-gated) or replicate it.
2. Replica: ask Claude to map entry points, data flow and order of execution into a Mermaid or Excalidraw diagram with short handwritten-style annotations.
3. Run it right after a large vibe-coded build or on an unfamiliar repo.
4. Save the diagram in docs/ and use it to onboard teammates.

## Caveats / uncertainty
Skill link not public. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> one of my recent favs

Transcript (auto, may contain errors):
> When you're building things that they are, it's very easy to build something that works. But you have no idea how it works, which is an issue. The best way I've found to fully understand your vibe-coded systems is to ask your agent to draw a welcome to skill of the weak, ladies and gentlemen, where every week I share with you one useful agent skill. This weak skill is called annotated illustrations, but you simply run this skill after a big build with Claude, or just point it at a project. It explores the system, works out what happened and in what order, then turns the whole thing into a simple hand-drawn explanation. Because when these systems get complicated, there's so many moving paths that you quickly lose track of how they all relate to one another. It's also a great way to brief in a new teammate, on a project you're working on, or a system you've just built, especially if they're non-technical. Now, I tested it this morning on a new onboarding flow that I built, and this is what I made. If you want to access Comity Word, it's down below, and I'll send it over to you.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
