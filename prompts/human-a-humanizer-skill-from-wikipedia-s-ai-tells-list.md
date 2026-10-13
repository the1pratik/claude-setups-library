# /human: a humanizer skill from Wikipedia's AI-tells list

I saved an Instagram reel by @buildwithai.club (https://www.instagram.com/buildwithai.club/reel/DaNefufqIfC/) and want to implement what it shows on my own machine.

## What the reel covers
Feed Claude Wikipedia's 'Signs of AI writing', ban every tell, then use skill-creator to save it as a personal skill called 'human'.

## Tools / resources mentioned
- Wikipedia: Signs of AI writing — https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing
- Agent Skills (anthropics/skills, incl. skill-creator) — https://github.com/anthropics/skills

## Proposed implementation plan
1. Tell Claude: 'Humanize everything; stop writing like AI.'
2. Paste/attach the Wikipedia 'Signs of AI writing' page; ask it to list every tell (em dashes, puffery, rule-of-three, etc.).
3. Tell it to never use any of them.
4. In the same chat: 'Use skill-creator to turn this into a personal skill named human' and install it.
5. Type /human before anything you write.

## Caveats / uncertainty
None noted. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Wikipedia accidentally built the best guide to making AI writing sound human. You can turn it into a one-word Claude command.
> 
> Here’s the 60-second setup:
> 
> 1.Tell Claude to humanize everything and stop writing like AI.
> 2.Feed it Wikipedia’s “Signs of AI writing” page and have it list every tell: the em dashes, the robotic tone, all of it.
> 3.Tell it to never use any of them.
> 4.In the same chat, open Skill Creator and turn it all into a personal skill named “human.”
> 5.Type /human before anything you write. It comes out clean.
> 
> Step 4 is the whole trick. Most people stop at one chat and re-explain it forever. Build the skill once and you never type “make it sound human” again.
> Comment HUMAN and I’ll DM you the free Notion guide with the exact prompts.
> 
> #claudeai #aiwriting #aitools #chatgpt #aitools

Transcript (auto, may contain errors):
> Wikipedia built a public list of every word that exposes AI writing. I turned it into one cloud command and now nothing it writes sounds like AI again. Here's the setup. Open Cloud and tell it to humanize everything and stop writing like AI. Then drop in the Wikipedia page, signs of AI writing and have it list every tell. The M dash is the robotic tone all of it. Band them all. But here's the part most people miss. In that same chat, open skill creator and say, turn this into a personal humanizer skill named human, install it. Now you just type slash human before anything and it writes like a human every time. Everyone else retives make it sound human in every new chat. You taught Cloud to do it once. Want my exact prompts? Comment human for the free notion guide.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
