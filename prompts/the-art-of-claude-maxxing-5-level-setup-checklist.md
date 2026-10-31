# The art of Claude maxxing (5-level setup checklist)

I saved an Instagram reel by @artem.novitckii (https://www.instagram.com/p/De4AwvFlFga/) and want to implement what it shows on my own machine.

## What the reel covers
A 7-slide carousel checklist for setting Claude up properly, in five levels: context (CLAUDE.md about you, memory on, a 'how I write' doc, project knowledge, screenshots and examples), skills (one SKILL.md per repeated task with reference files, install from anthropics/skills, plugins, slash commands), agents (plan mode first, Claude Code over chat, subagents, hooks, scheduled tasks, parallel sessions, overnight runs), tools (MCP connectors for Gmail/Notion/Drive/Calendar, Claude in Chrome, Canva and Figma, computer use) and taste (ask for 3 options, specific feedback, self-review, custom style, ban AI-slop words, human final edit, inspo folder).

## Tools / resources mentioned
- Anthropic Agent Skills repo — https://github.com/anthropics/skills
- Superpowers plugin (obra) — https://github.com/obra/superpowers
- Claude Code hooks docs — https://docs.claude.com/en/docs/claude-code/hooks
- Claude Code subagents docs — https://docs.claude.com/en/docs/claude-code/sub-agents

## Proposed implementation plan
1. Context: write a CLAUDE.md about you (who you are, voice, rules like 'never use em dashes', 'ask before big edits'), turn on Memory, add a 'how I write' doc and your brand files to Project knowledge, and give screenshots and examples instead of descriptions.
2. Skills: for each repeated task (weekly report, invoices, email replies) make a folder with a SKILL.md (name, description, numbered steps) plus a references/ folder of templates and past examples; edit the description so it says 'in my voice'.
3. Install ready-made skills from github.com/anthropics/skills (e.g. skill-creator, frontend-design, docx, brand-guidelines) and plugins such as obra/superpowers; trigger them as slash commands like /weekly-report.
4. Agents: start bigger jobs in plan mode (Shift+Tab to cycle) in Claude Code, let it spin up subagents, add hooks for automatic checks, set scheduled tasks, and run several sessions in parallel (inbox, website, research, invoices).
5. Tools: connect Gmail, Google Drive, Notion and Calendar as connectors/MCP servers, plus Canva and Figma; use the Claude Desktop app, Claude in Chrome and computer use for browser and app work.
6. Taste: ask for 3 very different options, give specific feedback ('cut the intro, open with the number, max 3 lines'), have Claude review its own draft, train a custom style, ban AI-slop words (delve, tapestry, em dashes), keep an inspo folder, and always do a human final edit.

## Caveats / uncertainty
This is a high-level checklist, not a step-by-step guide; the full 'Claude maxxing setup' (CLAUDE.md template, skills pack, agent workflows) is gated behind commenting MAXX, so it isn't included. 'Claude Duet, always on' is named on the slides but I couldn't confirm it as an official Anthropic product, so check before relying on it. Verified: github.com/anthropics/skills (with skill-creator, frontend-design, docx, brand-guidelines) and github.com/obra/superpowers exist. Hooks, plan mode and subagents are real Claude Code features.

## Source material
Caption:
> Comment “MAXX” and I’ll send you my full Claude maxxing setup ⬇️
>
> The people getting the most out of Claude all have one thing in common: they set it up properly.
>
> These are the 5 levels, from a CLAUDE.md file that makes Claude actually know you, to agents that keep working while you sleep (including the new Claude Duet).
>
> Save this so you can set it up this weekend. 
>
> Comment MAXX for the full guide
>  
> #ai #claude #anthropic

Slide text:
> Slide 1: The art of Claude maxxing (CLAUDE.md, plan mode, SKILL.md, subagents, scheduled task, Claude Code).
> Slide 2, Context maxxing: a CLAUDE.md file about you; voice-dump your brief; memory turned on; examples over descriptions; screenshots over words; a 'how I write' doc; project knowledge.
> Slide 3, Skills maxxing: a SKILL.md file; one skill per repeated task; install skills from GitHub (anthropics/skills); reference files; install plugins (superpowers, frontend-design, small-business); edit it for your workflow; slash commands.
> Slide 4, Agent maxxing: plan mode first; Claude Code, not chat; scheduled tasks; subagents; hooks for auto-checks; let it run overnight; Claude Duet, always on; run 4 sessions at once.
> Slide 5, Tool maxxing: Gmail, Notion, Drive linked; MCP connectors; Claude in Chrome; Claude Desktop app; Canva + Figma connected; connect all your tools; computer use.
> Slide 6, Taste maxxing: ask for 3 options; have Claude review its draft; specific feedback; train a custom style; remove AI slop writing; human final edit; keep an inspo folder.
> Slide 7: Comment MAXX to get the free Claude maxxing setup (CLAUDE.md template, skills pack, agent workflows, connector stack, taste checklist).

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
