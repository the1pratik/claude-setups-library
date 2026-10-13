# 5 design tools to make Claude Code UIs look premium

I saved an Instagram reel by @imaginetechz (https://www.instagram.com/imaginetechz/reel/DdshHpFpqdi/) and want to implement what it shows on my own machine.

## What the reel covers
Taste Skill, Web Design Guidelines, Awesome Design references, Image-to-Code, and Playwright CLI so Claude can see and test its own UI.

## Tools / resources mentioned
- Vercel web-interface guidelines / agent-skills — https://github.com/vercel-labs/agent-skills
- Playwright — https://playwright.dev
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview

## Proposed implementation plan
1. Taste skill: install a design-taste skill (creator's link is DM-gated) to push away from purple-gradient defaults.
2. Web design guidelines: install a guidelines/audit skill (Vercel publishes 'web-design-guidelines' in vercel-labs/agent-skills – verify) and run it on your UI.
3. Awesome design: give Claude real design systems (typography, color, spacing) as references in the repo.
4. Image-to-code: screenshot designs you like and paste them into Claude Code to recreate layouts.
5. Playwright: `npm init playwright@latest` (or the Playwright MCP) so Claude can open, screenshot and test pages itself.

## Caveats / uncertainty
Exact repos for 'Taste Skill' and 'Awesome Design' not given; the Vercel link is my best match. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment “DESIGN” and I’ll send you the 5 Claude Code tools. 👇
> 
> Your Claude Code app doesn’t need more code — it needs a better design workflow.
> 
> In this Reel, Alex breaks down 5 tools that can take your vibe-coded UI from generic to much more polished:
> 
> 🎨 Taste Skill — better design direction
> 📐 Web Design Guidelines — audit your UI
> 🧩 Awesome Design — real design systems & references
> 🖼️ Image-to-Code — turn design references into code
> 🌐 Playwright CLI — let Claude inspect and test the UI
> 
> If you're using Claude Code, Vibe Coding, AI Coding, or AI App Builders, save this one.
> 
> Comment “DESIGN” 👇
> 
> Trending Keywords:
> Claude Code, Claude Code Skills, Claude Code Plugins, Vibe Coding, Vibe Coded Apps, AI Coding, AI App Development, AI Website Builder, AI UI Design, AI Developer Tools, Claude AI, Frontend AI, AI Coding Tools
> 
> #VibeCoding #ClaudeCode #AICoding #ClaudeAI #AITools

Transcript (auto, may contain errors):
> Alex, why does everyone's Claude code app look like it costs 10K? And mine looks like it was built in 2006! Because you're using Claude code wrong. Excuse me? You're missing five tools. Five? Five. First one, taste skill. Okay, what does that do? It basically helps Claude develop better design taste. So Claude finally learns what premium means? Exactly. Because it's one more purple gradient with three rounded cards? I know, we need to call the authorities. Okay, what's next? Web design guidelines. Another design thing? Yeah, but this one checks what Claude already built. So instead of me staring at the screen thinking, something feels wrong. Claude can actually audit the interface against design guidelines. I would have saved me so many embarrassing launches. Number three? Awesome design. Sounds suspiciously awesome. It gives your coding agent actual design references and systems to work from. Like what? Typography, colors, spacing, components, layouts. So I don't have to sit there for 45 minutes choosing between two shades of blue? No. Finally, a technology that solves the real problem. Okay, number four. What's the trick? Image to code. Wait, image to code? Find a design you like, screenshot it, give it to Claude. And Claude repreates it? That's the idea. So Pinterest just became a development tool? Basically, that's Pinterest. Very. Alright, last one. What's number five? Playwright CLI. Okay, what does that have to do with design? Everything. Everything? Claude can actually open the browser, interact with your website, take screenshots, and check what it built. Wait. Yeah. So Claude can build the UI. Yep, open it. Yep. And actually look at it. Now you're getting it. Okay, that's slightly terrifying. And extremely useful. Alright. Where do I get all five? I've put them all together. Where? Comment, design, and I'll send you the complete list.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
