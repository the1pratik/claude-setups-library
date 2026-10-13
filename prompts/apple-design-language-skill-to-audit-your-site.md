# Apple design-language skill to audit your site

I saved an Instagram reel by @stefan.karsen (https://www.instagram.com/stefan.karsen/reel/Dd48gTiORGZ/) and want to implement what it shows on my own machine.

## What the reel covers
Turn Apple's design rules into a skill and use it mainly to audit and fix an existing website rather than copy Apple's look.

## Tools / resources mentioned
- Apple Human Interface Guidelines — https://developer.apple.com/design/human-interface-guidelines

## Proposed implementation plan
1. Get the creator's skill (DM-gated) or build your own: have Claude read Apple's HIG and distil rules on typography, spacing, hierarchy, color, motion into SKILL.md.
2. Install it in your skills folder.
3. Point Claude Code at your existing site and ask: 'Audit this against the Apple design skill; list issues by severity.'
4. Apply fixes in small batches, screenshot before/after (Playwright helps).

## Caveats / uncertainty
No public link in caption. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment “Apple” and I’ll send you the skills 👀

Transcript (auto, may contain errors):
> Someone just turned Apple's design language into a skill. So instead of telling Claude, hey, make this website more premium, you can give it actual design rules to follow. Now, most people will use this to build a new website, but I think the better use case is to fix an existing website. Just drop this skill into Claude and ask it to audit your own website, and it will notice so many minor details that are wrong with your website. So instead of copying how Apple looks, you're using the design rules behind why it looks so good. Comment Apple below, and I'll send you the skills today.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
