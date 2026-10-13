# The Council: five disagreeing advisors skill

I saved an Instagram reel by @charliehills (https://www.instagram.com/charliehills/p/DbJsAW7DbiD/) and want to implement what it shows on my own machine.

## What the reel covers
A /council skill that runs a decision past five personas (Contrarian, First Principles, Expansionist, Outsider, Executor), lets them debate, then a chairman gives one verdict.

## Tools / resources mentioned
- Agent Skills (anthropics/skills, incl. skill-creator) — https://github.com/anthropics/skills

## Proposed implementation plan
1. Build it yourself with skill-creator: ask Claude 'Create a skill named council'.
2. Define the five advisors exactly as in the caption and make each argue against the others in one thread.
3. Add a Chairman step that reads the debate and returns one verdict + next Monday actions.
4. Install, then run `/council <decision>` for real trade-offs (pricing, pivot, hire vs automate), not factual lookups.

## Caveats / uncertainty
Creator's version is DM-gated; this rebuild follows the caption exactly. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment GUIDE and I’ll send you the Council skill plus my 100+ free Claude guides.
> 
> Ask Claude if your plan is good and it argues for it. Ask if it’s bad and it argues against it.
> 
> It just tells you what you already want to hear. A yes-man.
> 
> So I stopped asking one Claude. I convene a council.
> 
> One skill runs your decision past five advisors, each trained to disagree, then to argue with each other:
> 
> 1. The Contrarian, only hunts for what will fail
> 2. First Principles, rebuilds your question from scratch
> 3. The Expansionist, finds the upside you missed
> 4. The Outsider, strips your context and sees it raw
> 5. The Executor, only cares what to do Monday
> 
> They clash in one thread. A chairman reads the whole debate and hands you one verdict.
> 
> You stop getting an echo. You start getting a decision.
> 
> Use it for the calls with real trade-offs: pricing, pivot or stay, hire or automate. Skip the factual lookups.
> 
> Type /council this after any messy call and let them fight it out.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
