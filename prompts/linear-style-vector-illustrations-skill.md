# Linear-style vector illustrations skill

I saved an Instagram reel by @shai.hq (https://www.instagram.com/shai.hq/reel/DeEhSRWBAi2/) and want to implement what it shows on my own machine.

## What the reel covers
A Claude skill encoding 10 rules for Linear-inspired hairline vector animations; run a create command, describe an idea, then add cursor interactivity and intensity controls.

## Tools / resources mentioned
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview
- Linear (style reference) — https://linear.app

## Proposed implementation plan
1. Get the skill from the creator (DM-gated; the reel shows a '/hairline create'-style command but no public link).
2. Install it into ~/.claude/skills/<name>/ (or a project .claude/skills/) so Claude Code can load SKILL.md.
3. Run the create command and describe the idea (e.g. 'an orbiting data pipeline').
4. Ask for cursor-reactive interactivity and an intensity slider.
5. Iterate: 'thinner strokes, slower easing, fewer nodes'.
6. Embed the resulting HTML/SVG/Canvas into your site.

## Caveats / uncertainty
Exact skill name/command unconfirmed; if you can't get it, ask Claude to write a SKILL.md capturing hairline-vector rules (thin strokes, monochrome, subtle glow, grid alignment, slow easing). Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> I just found this crazy way to get Claude to create those beautiful Linear inspired vector animations.
> 
> The creator basically made a Claude Skill that teaches coding agents 10 specific rules for creating this kind of illustration.
> 
> You just have to install the skill and give Claude an idea.
> 
> It then generates the entire interactive illustration for me.
> 
> You can move my cursor around and interact with it.
> Control the intensity.
> And even ask Claude to refine it until I’m happy with it.
> 
> It works with Claude Code, Cursor, Codex and other coding agents.
> 
> Honestly, this is one of the coolest ways I’ve seen AI being used for design.
> 
> Comment “linear” and I’ll send you the Skill.

Transcript (auto, may contain errors):
> Someone just figured out how to create this linear style vector animations using Claude code and built it into a single Claude skill. This skill teaches you coding agent's 10 specific rules to create these illustrations. You can simply go ahead to use this command to install the skill, then use slash hairline create and explain your idea. You can then go ahead to add interactiveness to your cursor, control the intensity and even ask Claude to refine it. It works with both Claude code and codex. Go ahead to comment linear and I'll send a skill in your DA.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
