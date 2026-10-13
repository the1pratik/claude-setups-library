# Claimed 'leaked' Claude system prompt

I saved an Instagram reel by @andrewshemett (https://www.instagram.com/andrewshemett/reel/Da1T8MuhX81/) and want to implement what it shows on my own machine.

## What the reel covers
Claims a 120k-character Claude system prompt is on GitHub and can be injected into open models like Kimi or GLM.

## Tools / resources mentioned
- Anthropic's published system prompts (official) — https://docs.anthropic.com/en/release-notes/system-prompts

## Proposed implementation plan
1. Prefer the official published system prompts Anthropic shares in its docs.
2. If studying a 'leak', treat it as unverified; don't run unknown code from such repos.
3. Takeaway worth keeping: write a strong, structured system prompt for your own agents (tools, search/citation rules, refusals).

## Caveats / uncertainty
Unverified leak claims; possible ToS/licensing issues. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment Fable and I’ll send you the full GitHub link so you can grab it yourself. Anthropic leaked the 120,000-character instruction manual for Claude, revealing over 1,500 lines of detailed rules guiding its reasoning, search, and safety protocols. This unprecedented insight allows developers to inject Claude’s system prompt into open-source models like Kimi or GLM, potentially elevating their performance and alignment. #AnthropicClaude #ClaudeFable #AIsystemPrompt #AIResearch #OpenSourceAI

Transcript (auto, may contain errors):
> Anthropics 120,000 character instruction manual for Claude leaked. Copy it into any AI model. This is the Claude Fable 5 System Prom, available on GitHub. Over 1,500 lines of rules, Anthropic uses for Claude's thinking, searching, refusing, and behavior. These instructions can inject into cheaper open source models like Kimme or GLM, making them follow Anthropics Playbook. A third of it is tool definitions. Another part is search and citation rules. Safety guidelines are 17% of the hall. Researchers call this the most detailed public look into a Frontier AI System. Comment Fable and I'll send you the full GitHub link so you can grab it yourself.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
