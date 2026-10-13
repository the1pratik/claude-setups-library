# Ask Claude for interactive HTML instead of text walls

I saved an Instagram reel by @ultra.skills (https://www.instagram.com/ultra.skills/reel/DaQgvXzMCd9/) and want to implement what it shows on my own machine.

## What the reel covers
Instead of 2,000-word answers, ask Claude to deliver comparisons and reports as a single browser-ready interactive HTML page/dashboard.

## Tools / resources mentioned
- Claude artifacts — https://claude.ai

## Proposed implementation plan
1. Add to your prompt: 'Deliver this as one self-contained HTML file with an interactive dashboard (filters, charts, tabs). No external build.'
2. In Claude.ai this renders as an artifact; in Claude Code, ask it to write report.html and open it.
3. Share the HTML with clients instead of long text.

## Caveats / uncertainty
Video download failed; built from caption. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> 🤯 Stop drowning in long Claude outputs when you already have an unfair advantage sitting inside your prompt bar.
> 
> ❌ Not a new third-party software.
> 💻 Real browser-ready pages built using a single prompt instruction.
> 
> • Old Way: Sifting through unreadable, 2,000-word plain-text walls that your partners or clients completely ignore.
> • New Way: Anthropic’s secret default that turns data comparisons into interactive dashboards instantly.
> 
> Valuable work left unread is just a vanity metric.
> 
> Comment HTML below to auto-grab the exact upgrade prompt library instantly in your DMs.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
