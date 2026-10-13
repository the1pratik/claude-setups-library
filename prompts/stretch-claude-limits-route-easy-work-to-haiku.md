# Stretch Claude limits: route easy work to Haiku

I saved an Instagram reel by @chenbuildsai (https://www.instagram.com/chenbuildsai/reel/DebKw4BDNgI/) and want to implement what it shows on my own machine.

## What the reel covers
A skill + CLAUDE.md note that triages tasks: file search/log reading go to a cheap Haiku model, Opus is kept for hard reasoning.

## Tools / resources mentioned
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview
- Claude Code subagents docs — https://docs.anthropic.com/en/docs/claude-code/sub-agents

## Proposed implementation plan
1. Create a subagent in .claude/agents/ (e.g. 'scout.md') whose frontmatter sets `model: haiku` and whose job is search, grep, log reading, file listing.
2. Add a CLAUDE.md rule: 'Delegate file search, log reading and bulk renames to the scout subagent; keep design/debugging in the main model.'
3. Optionally run `/model` to pick your main model and confirm the subagent uses Haiku.
4. Test with a task like 'find every place we call X and summarise' and check /cost or usage.
5. Tune: the savings depend on how much of your work is actually easy.

## Caveats / uncertainty
Model names/prices ('Haiku 5.5, 90% cheaper') are the creator's claims. The creator's exact skill is DM-gated; this recreates the idea with official subagents. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment "LIMIT" and I'll DM you the link to the skill: a Haiku 5.5 helper and the CLAUDE.md note, ready to paste. Follow so the DM lands 📩

Transcript (auto, may contain errors):
> Everyone hitting their clawed limit is wasting it on work a model 90% cheaper could do. Because Opus handles every naming a file and every renamed file takes a bite out of your limit. So my skills sorts each task first. File searches and log reading go to Hiku 5.5 and Opus keeps the hard thinking. And get this, Hiku 5.5 costs 90% less per token than the last Hiku. While Opus uses meaningfully more of your usage, but the catch. How far your limit stretches depends on how much of your work is easy. I will DM you the link to the skill, just comment limit.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
