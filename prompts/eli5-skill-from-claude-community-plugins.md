# ELI5 skill from Claude community plugins

I saved an Instagram reel by @practicalyai (https://www.instagram.com/practicalyai/reel/DcXPGHSRjir/) and want to implement what it shows on my own machine.

## What the reel covers
Install an 'ELI5' skill from the Claude community plugins list; then /eli5 <topic> gives a big-picture, few-words explanation.

## Tools / resources mentioned
- Claude Code plugins docs — https://docs.anthropic.com/en/docs/claude-code/plugins

## Proposed implementation plan
1. Search for 'Claude Code community plugins' (marketplace list) and find the ELI5 skill.
2. In Claude Code: `/plugin` to add the marketplace and install, or ask Claude to install the skill from its URL.
3. Use `/eli5 <topic>`.
4. Combine with the 'tutor' prompts for deeper learning.

## Caveats / uncertainty
Exact marketplace URL not given. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Things you don’t know you can do with Claude (part 62) #claude #claudeskills #digitalsamaritan #practicalyai

Transcript (auto, may contain errors):
> So then Throbbing Team just dropped the skill they've been using a lot lately, which means this is things you don't really can do with Claude, Part 62. Research for Claude Community Plugins and click on the first link. Copy this link and ask your Claude to install this ELI 5 skill from this link. Now if I just type slash ELI 5 and just type the topic I'm trying to understand, it will basically explain the whole thing with big pictures and a few words so it's super easy to understand.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
