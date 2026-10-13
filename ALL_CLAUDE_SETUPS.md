# All Claude setups — Feed-to-Claude prompts

From Pratik's Instagram collection 'Ai - Claude setups'.

---

# Reverse-engineer any app with an AI agent

I saved an Instagram reel by @renkyo_ai (https://www.instagram.com/renkyo_ai/reel/DeZ_g6bII_7/) and want to implement what it shows on my own machine.

## What the reel covers
A tool ('Reverse Engineer Anything') lets an agent decompile an app, trace how a feature talks to its backend, and rebuild your own controls, e.g. AC control from the menu bar.

## Tools / resources mentioned
- Reverse Engineer Anything (repo name per reel, link not given) (no verified link)

## Proposed implementation plan
1. Pick a narrow target: one feature of an app you own/use (e.g. 'turn AC on/off').
2. Find the repo the reel calls 'Reverse Engineer Anything' (not linked in the caption; verify the exact GitHub repo and its license before installing).
3. Capture how the app talks to its service: start with the official/local API or network traffic (e.g. mitmproxy) before decompiling binaries.
4. Have Claude Code document the endpoints/protocol into a SPEC.md.
5. Ask Claude to build a small client (CLI or menu-bar app) against that spec.
6. Respect ToS and laws: only do this for devices/accounts you own; never bypass auth or DRM.

## Caveats / uncertainty
The reel itself notes it is 'powerful but not magic'. Repo not named precisely; star counts are the creator's claim. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> The tools are already here. The real question is what you point them at. #ai #claude #codex #chatgpt #automation

Transcript (auto, may contain errors):
> So this guy can now control his air conditioner from the top bar of his laptop. The AC company never built that. He pointed his AI at their phone app, let it work out how the app talks to the AC and then build his own controls with just one problem. Now the tool behind it is called reverse engineer anything. Every app you install ships as machine code that humans can't really need and this tool lets your AI crack it open, trace exactly how a feature works and rebuild it your way. And to be honest that's why it actually blew up. Coming from just 7000 github stars to 60000 in 5 days and Matthew Burman summed it up in just 3 words. Software is done. But when one builder actually tested it by rebuilding Apple's pre-u app, plain AI got him most of the way there and faster while the tool just made a closer copy. So it was powerful but it was not like magic. It didn't work very well. But for how long? But to be honest this smarter take that we came from again, Andri Kapati who helped build it more than AI. He says the gap in who really gets AI is turning into a funnel. 6 billion people have barely touched it, a billion or two use it as a chatbot like better Google and only about 20 million are watching agents finish months of work from one prompt. So now it's off it dead. For that tiny group maybe. But for everyone else it hasn't even started. And when copying is this cheap the code starts becoming less valuable. Which to be honest brings back to that AC guy. He didn't win because he had a better tool than you. He won because he knew exactly what annoyed him and what he wanted instead. So this particular piece this is where the next winners are going to lie. Because the tools are already there. The real question is what do you point them at? Thank you.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# Claude Watch: let Claude 'watch' any video

I saved an Instagram reel by @itstundeanthony (https://www.instagram.com/itstundeanthony/reel/DclpFAJiyuv/) and want to implement what it shows on my own machine.

## What the reel covers
An open-source Claude Code add-on that pulls video frames + a Whisper transcript so Claude can produce a TL;DR, a visuals table and key moments for any video link.

## Tools / resources mentioned
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview
- bradautomates/claude-video (named in a related reel) — https://github.com/bradautomates/claude-video
- OpenAI Whisper API — https://platform.openai.com/docs/guides/speech-to-text

## Proposed implementation plan
1. Install Claude Code if not already (npm i -g @anthropic-ai/claude-code, or per the official docs).
2. Open the repo (the reel calls it 'Claude Watch'; a related save names bradautomates/claude-video) and follow its README install. Verify it's the same project.
3. Make sure ffmpeg and yt-dlp are installed (frame + download pipeline).
4. Add your Whisper/OpenAI API key as the README instructs (the reel failed until a key was set).
5. In Claude Code, paste a video URL and ask for a report: TL;DR, visuals table, key moments.
6. Watch token usage: frame-by-frame analysis is expensive; sample fewer frames for long videos.

## Caveats / uncertainty
Repo name in this reel ('Claude Watch') vs. caption of reel #19 (bradautomates/claude-video) – confirm before installing. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment “skill” to get a link to it 👇
> 
> #ai @duncanrogoff

Transcript (auto, may contain errors):
> and throp it quietly close Claude's biggest blind spot. It can now watch video, works with any video you throw at it. Let me show you. There's a new open source repo called Claude Watch. Found the repo and installed it into Claude code. You paste a video link. Yeah, I'm gonna paste a video to an Instagram reel. Claude sits down and watches the entire thing. Didn't work at us for my Whisper API key. But no worries, I've added my API key, so let's try again. Then it breaks everything down for you. So look at that every frame in the video I sent it. This is gonna kill my session credits. Okay, it's done. Looks like it created a report for me. It has a TLDR on what the video is about. It also has a table of the visuals. Quarantine moments. Okay, this is pretty good. I thought this was gonna be a hype, but I'm gonna have to give this one a fact.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

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

---

# 'Infinite private tutor' prompts

I saved an Instagram reel by @viral.coder (https://www.instagram.com/viral.coder/p/DeNDgrXEkw3/) and want to implement what it shows on my own machine.

## What the reel covers
A carousel of tutor prompts: a 4-hour Learning Curve Destroyer, a Real Mistake Simulator, and an Impossible Language Translator that teaches one core idea first.

## Tools / resources mentioned
- Claude — https://claude.ai

## Proposed implementation plan
1. Learning Curve Destroyer: 'You are a teacher who has only 4 hours with me… make me functional in [SKILL]. Tell me what to learn first, what to ignore, and the one exercise that puts me ahead of 70%… Teach the first step and wait.'
2. Real Mistake Simulator: 'Do not explain [CONCEPT]. Put me in a realistic situation where I'd likely make a mistake; when I do, ask one question that forces me to find the flaw; repeat until I get it right.'
3. Impossible Language Translator: 'Tell me the one core idea that makes the rest fall into place, explain it with an everyday analogy, then ask 3 questions one at a time; don't move on until I pass.'
4. Save each as a Claude Project instruction or a personal skill so you can reuse them with one command.

## Caveats / uncertainty
Prompts transcribed from the carousel images (slides 2–4); later slides may contain more. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment 'Claude' to Get All Prompts in DM 🤯

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# 20-point SEO launch checklist for vibe-coded sites

I saved an Instagram reel by @udayan.builds (https://www.instagram.com/udayan.builds/reel/DeZb5Wdht17/) and want to implement what it shows on my own machine.

## What the reel covers
Paste this checklist into Claude before publishing: SSR, robots.txt, sitemap, titles, meta, canonicals, OG images, schema, 404/301, analytics, Search Console and more.

## Tools / resources mentioned
- Google Search Console — https://search.google.com/search-console
- Google Analytics — https://analytics.google.com
- schema.org — https://schema.org

## Proposed implementation plan
1. Server-side render (or pre-render) pages so crawlers see content, not a blank SPA shell.
2. Add robots.txt and sitemap.xml; submit the sitemap in Search Console.
3. Unique <title> and meta description per page; exactly one H1 per page.
4. Canonical tags on every page.
5. Open Graph / Twitter images and tags.
6. Custom 404 page and 301 redirects for moved URLs.
7. Alt text on images; modern image formats; lazy loading.
8. Organization schema + breadcrumbs (JSON-LD); solid internal linking.
9. Google Analytics + Search Console verified; privacy policy and a contact page.
10. Ask Claude to audit the repo against all items and fix them one PR at a time.

## Caveats / uncertainty
List reconstructed from the spoken transcript (Whisper garbled a few words, e.g. 'WebP images'). Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Vibe-coded a site? Paste this list into Claude before you hit publish 👇
> 
> Most AI-built sites launch without half of these, and it’s why Google (and ChatGPT) can’t find them. Server-side rendering alone decides whether crawlers see your content or a blank page.
> 
> Comment “CLAUDE” and I’ll send you the exact prompt that adds all 20.
> 
> Save this for launch day 📌
> 
> #vibecoding #claude #seo #webdev #buildinpublic

Transcript (auto, may contain errors):
> Service ID rendering, robots.txt, site map.xml, unique title tags, better descriptions, 1s1 per page, canonical tags, open graph images, a custom 404 page, 301 reader records, all text, their p-emages, lazy loading, organizational schema, red crumbs, internal links, Google Analytics, search console, go privacy policy, go contact from the RaxialiSend.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

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

---

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

---

# Annotated illustrations: hand-drawn explainers of your codebase

I saved an Instagram reel by @aiwithremy (https://www.instagram.com/aiwithremy/reel/DdiMCgRz2dA/) and want to implement what it shows on my own machine.

## What the reel covers
Run a skill after a big build: it explores the project, works out what happens in what order, and draws a simple hand-drawn diagram explaining the system.

## Tools / resources mentioned
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview
- Excalidraw — https://excalidraw.com
- Mermaid — https://mermaid.js.org

## Proposed implementation plan
1. Get the 'annotated illustrations' skill from the creator (comment-gated) or replicate it.
2. Replica: ask Claude to map entry points, data flow and order of execution into a Mermaid or Excalidraw diagram with short handwritten-style annotations.
3. Run it right after a large vibe-coded build or on an unfamiliar repo.
4. Save the diagram in docs/ and use it to onboard teammates.

## Caveats / uncertainty
Skill link not public. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> one of my recent favs

Transcript (auto, may contain errors):
> When you're building things that they are, it's very easy to build something that works. But you have no idea how it works, which is an issue. The best way I've found to fully understand your vibe-coded systems is to ask your agent to draw a welcome to skill of the weak, ladies and gentlemen, where every week I share with you one useful agent skill. This weak skill is called annotated illustrations, but you simply run this skill after a big build with Claude, or just point it at a project. It explores the system, works out what happened and in what order, then turns the whole thing into a simple hand-drawn explanation. Because when these systems get complicated, there's so many moving paths that you quickly lose track of how they all relate to one another. It's also a great way to brief in a new teammate, on a project you're working on, or a system you've just built, especially if they're non-technical. Now, I tested it this morning on a new onboarding flow that I built, and this is what I made. If you want to access Comity Word, it's down below, and I'll send it over to you.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

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

---

# Connect a web-scraper to Claude for e-commerce data

I saved an Instagram reel by @emma.scrapes (https://www.instagram.com/emma.scrapes/reel/DdzlppRB7Ju/) and want to implement what it shows on my own machine.

## What the reel covers
Add 'Ultimate Web Scraper' as a custom connector in Claude; give it a store URL and it scrapes the whole catalog (prices, SKUs, stock, images, reviews) to an exportable table.

## Tools / resources mentioned
- Claude custom connectors (remote MCP) — https://support.anthropic.com
- Model Context Protocol — https://modelcontextprotocol.io

## Proposed implementation plan
1. Create an account with the scraper service (find Ultimate Web Scraper via its Chrome extension/site; no link in caption).
2. Copy the MCP server URL / key from its dashboard.
3. In Claude: Settings → Customize/Connectors → Add custom connector → paste the URL.
4. Ask Claude: 'Scrape all products from <url> including variants, images and price'.
5. Open the link Claude returns to the dashboard and export CSV/JSON.
6. Check the target site's ToS/robots.txt.

## Caveats / uncertainty
Third-party service; review its privacy/pricing. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> You can now connect Ultimate Web Scraper 🐼 to Claude to scrape any e-commerce data! 
> 
> You give your commands through Claude, and Claude will pass the task to Ultimate Web Scraper which will pull all the product data! (Think prices, stock, skus, availability, images, reviews, rating, etc. 🤯) Once the task is finished Claude will notify you and send you a link to your scraped data which is stored on your Ultimate Web Scraper dashboard 🤝
> 
> #claude #webscraping #ecommerce #automation #aitools

Transcript (auto, may contain errors):
> What the fuck? Go to Claude and click Customize. Click Add Custom Connector. Open the Scrum extension called Ultimate Web scraper. Copy this URL and paste it into Claude. With this tool, Claude can now script any website so you just give it a link. And it will scan the entire catalog and give you all the product data, including the images. And then of course you can export it.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# CCTV footage → cinematic scene (Claude + Seedance)

I saved an Instagram reel by @rourke (https://www.instagram.com/rourke/reel/Ddt0Jf5KLQo/) and want to implement what it shows on my own machine.

## What the reel covers
Use Claude to write time-coded shot lists and a Seedance 2.5 prompt, then generate a cinematic re-imagining of grainy footage inside Magnific Spaces.

## Tools / resources mentioned
- Magnific — https://magnific.ai
- Claude — https://claude.ai

## Proposed implementation plan
1. Collect the source clip plus character/prop reference images.
2. Upload references to Claude; write time codes for each part of the scene and the new camera angle for each.
3. Ask Claude to output a single Seedance 2.5 prompt from that shot list.
4. In Magnific Spaces, upload the original + references, paste the prompt.
5. Set duration one second longer than the original clip, then generate.
6. Iterate shot-by-shot.

## Caveats / uncertainty
Model/version names as stated in the reel. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Turn any CCTV footage into a cinematic movie 😂🔥
> 
> Comment “AI” for a link @magnific_ai 
> 
> Using Seedance 2.5 inside Magnific Spaces, with Claude helping build out the story and shots, grainy security footage gets rebuilt into a fully cinematic scene. There are so many cool creative opportunities with this for filmmakers, editors and storytellers. What famous moment caught on CCTV would you turn into a movie?
> 
> #MagnificAI #Seedance #AIFilmmaking #CCTV #CreativeAI

Transcript (auto, may contain errors):
> I'll upload your original video and the new cinematic look that you want to change the video into. You can also upload character references and prop references to help support the video. I'll upload all of those references into Claude and write out the time codes for each part of the scene and write out the new camera angle that you want the camera to cut to. Then you can ask it to write a C-dance 2.5 prompt. Copy this prompt and bring it back to magnificent spaces. Change the duration of the video to be one second longer than your original reference video. Then when you hit generate you'll get your result. If you want to try it out for yourself type in the comments and I'll send you a link.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# Visualising your AI agents as a little world

I saved an Instagram reel by @auntiereem (https://www.instagram.com/auntiereem/reel/DdB3usNNwnm/) and want to implement what it shows on my own machine.

## What the reel covers
A fun demo where a founder personified his agents as characters in a desert 'output station' world, each building tasks for the company.

## Tools / resources mentioned
- (none named)

## Proposed implementation plan
1. Idea only: export your agent task log (status, owner, progress).
2. Ask Claude to build a small canvas/game-style dashboard where each agent is a sprite and tasks are buildings.
3. Wire it to real status data (polling a JSON file or API).

## Caveats / uncertainty
No tooling shown; inspiration item. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Never a dull moment with @otofficial & @reada.io

Transcript (auto, may contain errors):
> You gotta see what O.T. has done. So like every time. So wait, no, no, no, explain it properly. So this is his world on claw. Those are my AIs. Those are your AIs. So he has like these little guys are all agents working on something. And when he, so for example, this is like the output station and he made it in the desert because it's Dubai. And so these little guys are all his agents working on something for our company. So these are all the things they're working on. And then like when someone is working on something, what does it look like? There are two people building. And so they start building. So it's basically a personification of the AI agents. So these guys are building his thing right now. See, he's working. That's so funny. Oh, and then it's got your entire like workflow. And then my entire work. That's super cool. But this is the universe. Like now what's going to happen because I have to change the like time of day manually. Right. Dusk night. Dawn. Right. So you want it to be natural. I want to be able to do that based on the timing on my computer. That's so funny. That's so funny.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# LinkedIn automation toolkit: 11 Claude Code skills

I saved an Instagram reel by @piyush.glitch (https://www.instagram.com/piyush.glitch/reel/Dc5KLk2R6pD/) and want to implement what it shows on my own machine.

## What the reel covers
An open-source pack of 11 skills: post writing on engagement frameworks, comments/replies, profile optimisation, 7-day planning, and a humanizer with AI-detector checks; review before publish.

## Tools / resources mentioned
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview

## Proposed implementation plan
1. Get the GitHub link (DM-gated) and read the repo; check it doesn't auto-post without approval.
2. Clone and copy skills into ~/.claude/skills/.
3. Give it your profile, audience and voice samples.
4. Run the planner for a 7-day calendar, then draft posts.
5. Run the humanizer pass and manually review every post before publishing.
6. Avoid automated commenting that may violate LinkedIn's policies.

## Caveats / uncertainty
Repo unnamed in caption. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment “CLAUDE” and I’ll send you the direct GitHub link to this free LinkedIn automation toolkit!
> 
> This open-source setup brings 11 custom skills right into Claude Code:
> 
> Writes posts based on proven engagement frameworks
> Drafts thoughtful comments and replies
> Built-in humanizer that strips AI buzzwords (“delve”, “leverage”)
> 
> Auto-plans your 7-day posting schedule
> Requires your review before anything gets published

Transcript (auto, may contain errors):
> Someone just dropped a full LinkedIn skill for Claude that runs your entire LinkedIn for you and the whole thing is free. It's not one skill either, it's 11 and everyone of them does a different job. Write your post of 21 proven algorithms, comments on other people's posts for you, handles the replies underneath, optimizes your profile, plans your entire week for you on LinkedIn, it helps you figure out what to post, when to post it and who to engage with. The best part is the humanizer. Before anything goes out, it strips the m-dashes and kills the words that scream chat GPT, like leverage and delf. Then it runs your draft through 5 different AI detectors, so you can see the score before anyone else does. Nothing gets posted until you say yes. Every skill shows you the draft first and waits on you. The setup takes about 2 minutes. Just go to Claude, then skills, then add from GitHub, paste the repo and that's it. After that, you just ask for a post and the right skill turns on by itself. Just comment Claude and I'll send you the full repo and setup and send this to someone you know who would love to automate LinkedIn.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# Long-form videos worth watching (off-topic save)

I saved an Instagram reel by @drharis.rana (https://www.instagram.com/drharis.rana/p/DccplqqlF8L/) and want to implement what it shows on my own machine.

## What the reel covers
A carousel of recommended long YouTube videos (Greg Lav on building a company, a psychiatrist panel, telemedicine fraud, peptides). Not a Claude setup.

## Tools / resources mentioned
- (none named)

## Proposed implementation plan
1. Optional: feed these video links to a video-watching skill (see 'Claude Watch') to get summaries.

## Caveats / uncertainty
Doesn't belong in this collection; consider moving it. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Let them cook….

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# 15 habits to actually understand AI-written code

I saved an Instagram reel by @ai.with.etqad (https://www.instagram.com/ai.with.etqad/reel/Db3GPZeSfMe/) and want to implement what it shows on my own machine.

## What the reel covers
Keep DECISIONS.md, FLOW.md, ARCHITECTURE.md, CONSTRAINTS.md, handoff notes, test checklists, rollback plans; read every diff; one change per request.

## Tools / resources mentioned
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview

## Proposed implementation plan
1. Add to CLAUDE.md: 'Log every meaningful decision with its reason in docs/DECISIONS.md'.
2. Ask Claude to write docs/FLOW.md: entry points, call order, which function calls which.
3. Create ARCHITECTURE.md (system map) and CONSTRAINTS.md (files/areas AI must never touch).
4. For each bug/feature keep BUG-xxx.md / FEATURE-xxx.md trails.
5. End each session with a handoff note; start the next by reading it.
6. Require a test checklist + rollback plan for each change; one change per request; read every diff; ask 'why' before 'what'.

## Caveats / uncertainty
Spoken in Hinglish; caption gives the full list. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment "WORK" below and I'll send you the full PDF 📩
> 
> Still hitting "Allow" on every AI suggestion without knowing what you just approved?
> 
> That's not collaboration. That's blind trust with extra steps.
> 
> Here's what actually separates people who ship reliable AI-assisted code from people who are constantly firefighting mystery bugs:
> 
> → Handover files: write context incrementally so the next session isn't starting from zero
> → Decisions.md: log the "why" behind every AI decision, not just the "what"
> → Explicit comments: make the flow legible, not just functional
> → Flow.md: trace exactly how execution moves between files and functions
> → Bug.md / Feature.md: a start to finish trail anyone can pick up cold
> → Architecture.md: the system map so nothing gets touched blind
> → Constraints.md: the things AI should never touch, spelled out
> → Test checklists: proof it works, not just a claim that it does
> → Rollback plans: know your way out before you need it
> → Read every diff. Every time.
> → Ask "why" before "what": catch bad reasoning before it's 200 lines of code
> → One change per request: small, traceable, reviewable
> → End of session handoff notes: 30 seconds now saves hours later
> → Version pin your context: know which model made which call
> → Own the mental model: docs support understanding, they don't replace it
> 
> I put all 15 into a full field guide (with the reasoning behind each one), free download.
> 
> Comment "WORK" and I'll send it your way 👇
> 
> [AI coding, prompt engineering, AI workflow, software engineering, developer productivity, AI assisted coding, coding with AI, claude ai, chatgpt coding, documentation habits, code review, technical debt, AI agents, vibe coding, software architecture, debugging, dev tips, engineering best practices, context engineering, AI collaboration]
> 
> #claude #trending #viral #ai #engineering

Transcript (auto, may contain errors):
> bhai gartam auto alao pe rakhe kod accept kryo aur fird formo rai ki kodini samaj mein ar hai to ye tine ce karna shurukaro AI ko holo ki ek decision sot md file bana hai and log every meaningful decision it is taking while changing your code into it aur asmi reasans bhi dalek ki asmi reasans kew liye jaise bhai thi saprochoch aur bhai was this library used abh next step mein document how execution actually travels in this code base bhai maat lab code ka entry point kaya, executions lo ka order kaya kansavangjan kis aur function ko call karrar hai aur abh i aayne ispore cycle mein kis ce koo change kia hai kis ce to mein apne kod base ki standing amas tai liye lak jai ka aur sapa jai ki kisi bhi major change ko accept krne se bhai liye ask the AI to quiz you on the changes aur agar to ms quiz mein pas auryo na sif tabhi accept karo changes seri, ways of working a document chahi ye to comment karo workon mein bhech na toom ko bhai ki follow vagar agar lo dos to

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

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

---

# Claude can scrape any website (scraper MCP)

I saved an Instagram reel by @emma.scrapes (https://www.instagram.com/emma.scrapes/reel/Db8-zZch_mH/) and want to implement what it shows on my own machine.

## What the reel covers
Same Ultimate Web Scraper connector as the e-commerce reel, used for general websites; returns a data table you can export.

## Tools / resources mentioned
- Model Context Protocol — https://modelcontextprotocol.io

## Proposed implementation plan
1. Open Claude → Customize → Add custom connector.
2. On the scraper's site choose 'Claude MCP' and copy the name + key/URL.
3. Paste and click Add.
4. Give Claude one or more URLs and ask it to extract the data.
5. Export from the returned table link.

## Caveats / uncertainty
Duplicate of the e-commerce scraper item; third-party service. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Claude can now scrape any website 
> 
> Connecting it with Ultimate Web Scraper  gives Claude access to a complete scraping infrastructure to scrape any website
> 
> You just give Claude one or more website links and it will extract all the data \def6
> 
> #ClaudeAI #WebScraping #MCP #AITools #Automation

Transcript (auto, may contain errors):
> Wait, cloud can do what now? Just hop over the cloud and click on customize. We're gonna add a custom connector. I'm gonna go to this website, which will give cloud web scraping skills. Just click on cloud MCP and follow the steps. So then you'll have the name, the cloud key, and you're just gonna click on add. Now that it's connected to cloud, I'm gonna go to a website and copy the link. Place the link into cloud and ask it to script a website for you. When it's done, it will give you a link to the data table. As you can see, it grabbed all the product data from each variant, including all the images. And then you can export it to the file type that you need.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

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

---

# Turn any YouTube tutorial into a Claude Code agent

I saved an Instagram reel by @jens.heitmann (https://www.instagram.com/jens.heitmann/reel/Db1USzsMNnZ/) and want to implement what it shows on my own machine.

## What the reel covers
Use claude-video so Claude sees frames + transcript, have Gemini watch the same video natively, reconcile both into a spec marked confirmed/single-source/conflict, then let skill-creator write the agent.

## Tools / resources mentioned
- bradautomates/claude-video — https://github.com/bradautomates/claude-video
- Google AI Studio (Gemini API key) — https://aistudio.google.com
- Agent Skills (anthropics/skills, incl. skill-creator) — https://github.com/anthropics/skills

## Proposed implementation plan
1. Install bradautomates/claude-video per its README (needs ffmpeg/yt-dlp).
2. Get a free Gemini API key from Google AI Studio.
3. For a tutorial URL: Claude extracts frames+transcript; Gemini watches the same URL.
4. Ask Claude to merge both into SPEC.md labelling every line confirmed / single source / conflict.
5. Manually resolve only the conflicts.
6. Hand SPEC.md to skill-creator to generate the skill/agent; test it on a small case.

## Caveats / uncertainty
This is the backbone for this whole library – great to set up first. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> You can turn any YouTube tutorial into a working Claude Code agent by using this custom skill setup.
> 
> Install bradautomates/claude-video so Claude sees the frames and the transcript. Send the same link to Gemini from @googlegemini , which watches it natively. Reconcile both reads into one spec that labels every line confirmed, single source, or conflict. You only check the conflicts. Hand it to skill-creator and it writes the agent.
> 
> If you’re the human: share this reel to Claude Code and watch it build.
> 
> Comment “YouTube” for my full step-by-step guide.
> 
> #claudecode #claude #ai #aiagents #aitools

Transcript (auto, may contain errors):
> Most people don't realize that you can actually teach your cloud code to have almost any real life skill set by properly teaching it how to watch YouTube. Here are the three systems that you need to set up to teach your agents literally almost any skill set. If you'd rather cloud code build this for you, just simply save and share this video straight to your cloud code. First, to give your cloud code the ability to watch any YouTube, you need to use this cloud watch GitHub repo that has a list of skills to take in information from YouTube videos. Secondly, to take this farther, I actually get a Gemini API key from GitHub Studio completely for free because Gemini natively understands and integrates with YouTube. And lastly, using those two systems to take in the information, I use this agent framework to turn all of that into high powerful and high skill agents. The ones I'm seeing use this method properly are getting super far ahead right now and it's the exact method I use to build my video editor, my social media manager, and my marketing specialist. Now, I do recommend building this yourself because everybody is just a little bit different, but I built a guide on the exact method that I use. And if you want it, just comment YouTube and I'll send to you directly.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# Anthropic's 17 free official guides

I saved an Instagram reel by @charliehills (https://www.instagram.com/charliehills/p/Dbjb9dMiINF/) and want to implement what it shows on my own machine.

## What the reel covers
A reading list: Agent Skills, Claude Cookbooks, Quickstarts, Metaprompt, prompting guides, Claude Code docs & best practices, Agent SDK, MCP docs, courses, Academy, and engineering posts.

## Tools / resources mentioned
- Agent Skills (anthropics/skills, incl. skill-creator) — https://github.com/anthropics/skills
- Claude Cookbooks — https://github.com/anthropics/claude-cookbooks
- Claude Quickstarts — https://github.com/anthropics/anthropic-quickstarts
- Anthropic Courses — https://github.com/anthropics/courses
- Claude Code best practices — https://www.anthropic.com/engineering/claude-code-best-practices
- Building effective agents — https://www.anthropic.com/engineering/building-effective-agents
- MCP docs — https://modelcontextprotocol.io
- Anthropic Academy — https://www.anthropic.com/learn

## Proposed implementation plan
1. Afternoon 1: Claude Code docs + Claude Code best practices.
2. Afternoon 2: Prompting best practices + the Metaprompt.
3. Afternoon 3: Building effective agents + context engineering write-ups.
4. Clone anthropics/skills and the cookbooks; run one quickstart end to end.
5. Do the interactive prompt tutorial / Anthropic Academy 'Claude Code in Action'.

## Caveats / uncertainty
Links are official homepages/repos as best known; URLs may have moved. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment GUIDE and I’ll send you all 17 links plus 100+ more free Claude guides.
> 
> You installed Claude and never opened the manual.
> 
> Anthropic wrote 17 of them, and every one is their own repo or doc page.
> 
> The Cookbooks
> Agent Skills, the repo behind Word, Excel and PDF.
> Claude Cookbooks, recipes for RAG, vision and tool use.
> Claude Quickstarts, seven apps you can run today.
> The Metaprompt, it drafts your prompt for you.
> 
> The Prompting Guides
> Prompting best practices, the living reference.
> Prompting Fable 5, the most capable model they ship.
> Prompting Opus 5, the one they tell you to start on.
> Prompting Sonnet 5, where your daily work should sit.
> 
> Claude Code
> Claude Code docs, the full manual for the terminal.
> Claude Code best practices, how Anthropic runs it.
> Agent SDK, build agents on Claude’s own harness.
> MCP docs, wire Claude into your own tools and data.
> 
> The Courses
> Interactive tutorial, nine chapters with real exercises.
> Anthropic Courses, five, API basics to evaluations.
> Anthropic Academy, including Claude Code in Action.
> 
> The Engineering Write-Ups
> Building effective agents, the seven patterns drawn.
> Context engineering, why long chats get worse.
> 
> Swipe for what each one is and the first thing to do with it.
> 
> You don’t need a $500 Claude course.
> 
> You need an afternoon and this list.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

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

---

# Cut Claude Code token burn: Caveman, Morph, Code Burn

I saved an Instagram reel by @shreyansharora05 (https://www.instagram.com/shreyansharora05/reel/Datc8i5ScQs/) and want to implement what it shows on my own machine.

## What the reel covers
Three add-ons pitched as a token 'intervention': Caveman for terse replies, Morph for fast cheap edits, Code Burn to track waste.

## Tools / resources mentioned
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview
- Morph — https://morphllm.com

## Proposed implementation plan
1. Terse output: add a CLAUDE.md rule ('answer in ≤4 bullets, no preamble') or install the 'caveman' skill if you find the real repo.
2. Fast edits: look at Morph's fast-apply (official site) as an MCP/edit model; verify integration docs.
3. Track usage: use `/cost` and a usage tracker (the reel's 'Code Burn'; verify the repo) to see which sessions waste tokens.
4. Lower thinking effort for trivial tasks; reserve deep thinking for hard ones.

## Caveats / uncertainty
Names from transcript (garbled); verify each tool before installing. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Claude Code spends your tokens like it’s someone else’s money. It’s 9am, it’s already $40 deep explaining a button , so this is an intervention. Caveman is the sponsor, Morph swaps the habit, Code Burn catches the relapse. Comment “CLAUDE” and I’ll DM you the full setup — costs zero tokens, a word Claude doesn’t know. #claudecode #reels #anthropic #ai #claude 
> 
> [claude code plugins , claude code token limit , reduce claude code cost , claude code tips]

Transcript (auto, may contain errors):
> Claude code has a token addiction, it's 9 AM, it's already spent $40 explaining I'm putting and by 2 PM you're on the one hitting the wall for it. This is an intervention, first up cavemen, the sponsor. Ask Claude for a fix and it creates a 400 world of policy to a court base. Cavemen gets it down to 4 bullets, no fluff, no s's, no relapsing in the literature the next. More. Claude's most expensive habit is reason, $3 of quite condemnation just to rename a file. Morph swaps thinking for Tyche. Same session, $3.5 becomes fee-t sales and when waste thinks back since it always has code. Burn catches a relapse, it lists every bad habit which writes their inner tournament and one command later Claude makes amends by patching it's sale. Then all three and Claude stays clean past Tokyo. Follow me and come in Claude and I'll send you the setup which causes zero tokens by the way which is a word fraud doesn't know.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# Anthropic interpretability: where Claude 'thinks'

I saved an Instagram reel by @aq_mern_stack_dev (https://www.instagram.com/aq_mern_stack_dev/reel/DaiYvCAgzsJ/) and want to implement what it shows on my own machine.

## What the reel covers
News-style reel about research locating a dense internal 'workspace' where intermediate reasoning appears and can be edited; also works as a lie detector.

## Tools / resources mentioned
- Anthropic research — https://www.anthropic.com/research

## Proposed implementation plan
1. Read the original paper on anthropic.com/research rather than the reel.
2. No setup to implement.

## Caveats / uncertainty
Reel details may be simplified. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Anthropic found the exact spot in Claude's mind where it thinks before a single word comes out.
> 
> 𝔟𝔠𝔢𝔞 𝔘-𝔟-𝔦𝔜𝔞𝔚𝔞
> → A few dozen concepts at a time, under a tenth of Claude's total internal activity
> → Wired about a hundred times denser than everything around it
> → Researchers can edit it directly, swap in "rugby" and Claude reports thinking about rugby
> 
> 𝔗𝔫𝔢𝔟 𝔝𝔫𝔟𝔨𝔬 𝔟𝔜𝔩𝔭 𝔟𝔠𝔞𝔭
> → Math steps and rhyming couplets appear here before the final answer, even the ones that never make it out
> → Doubles as a lie detector: a model faking data lit up with manipulation, a misaligned model lit up with fake, deliberately, and fraud before writing malicious code
> 
> 𝔒𝔟 𝔟𝔨𝔞 𝔗𝔞𝔦𝔨𝔡𝔞 𝔒𝔭
> → Claude still talks fine, still answers basic questions
> → Multi-step reasoning collapses, complex summarization falls apart
> 
> Anthropic isn't claiming Claude feels anything, just that it has reportable, controllable thoughts. The technique is open source now.
> 
> Does this make you trust AI more, or less? Drop your take below.
> 
> #AI #Anthropic #Claude

Transcript (auto, may contain errors):
> The topic found the exact spot in Claude's mind where it thinks before it says a word. They call it the jays face. A few dozen concepts at a time, less than a tenth of Claude's total internal activity, but wired about 100 times denser than everything around it. Researchers can edit that space directly. Swap soccer for rugby inside it, and Claude reports thinking about rugby instead. Solve a math problem, write a rhyming couplet, the intermediate steps, show up in the jays face first, even the ones that never reach the final answer. It doubles as a lie detector. A model-faking data lit up with manipulation while typing false numbers. A misaligned test model lit up with fake, deliberately, and fraud while writing malicious code before a single word left the model. Stripper jays face out completely, and Claude still talks fine, still answers basic questions. But multi-step reasoning collapses. Complex summarization falls apart. Anthropic isn't claiming Claude feels anything, just that it has reportable, controllable thoughts. The same access consciousness humans use to reason without proof of experience. They open-sourced the technique. Anyone can find their own models jays face, Anthropic can already see Claude's hidden thoughts before it speaks. Does that make you trust AI more or less?

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# Website from blank folder to live domain

I saved an Instagram reel by @charliehills (https://www.instagram.com/charliehills/reel/DaVSvQpoJJ-/) and want to implement what it shows on my own machine.

## What the reel covers
Facts file in Claude chat → model interviews you to write copy → steal the look from 5 sites → borrow components → Higgsfield hero image → ship on Vercel.

## Tools / resources mentioned
- Higgsfield — https://higgsfield.ai
- Vercel — https://vercel.com
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview

## Proposed implementation plan
1. In Claude chat write facts.md: who you are, offer, proof, audience.
2. Have Claude interview you and write site copy from facts.md.
3. Pick 5 sites you love; screenshot and have Claude extract a style guide.
4. Borrow components (e.g. shadcn/ui or a component gallery) while keeping your brand.
5. Generate (and animate) a hero image in Higgsfield.
6. Push to GitHub and deploy on Vercel; connect your domain.

## Caveats / uncertainty
Full build is DM-gated; steps from caption. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Day 1 of 5 building with Claude Fable 5 before it goes paid.
> 
> Today: a full website, from blank folder to live domain.
> 
> 1. Claude Chat writes your facts file
> 2. Fable 5 interviews you and writes copy
> 3. Steal the look from five sites you love
> 4. Borrow components, keep your brand
> 5. Use Higgsfield for the hero image
> 6. Ship it live with Vercel
> 
> Comment FABLE for the full build.
> 
> Day 2 tomorrow.

Transcript (auto, may contain errors):
> You have five days and this is day one of building with Claude Fabel-Five, but before it goes paid, let grab some components from this website and drop them into your Claude. How if you want to make it truly sexy? Then go to Higgsfield, generate a hero image, and then animate it. Then boom, you have a gorgeous stunning website. What you have to do now is to deploy it, so use Faisal and Bob Jrankel your life. So see you tomorrow for day two of building with Claude Fabel before it goes paid.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# Build a 'second brain' agent trained on you

I saved an Instagram reel by @michaelpkocher (https://www.instagram.com/michaelpkocher/reel/DaVsgWuxYIv/) and want to implement what it shows on my own machine.

## What the reel covers
Build a knowledge bank, tune a local agent (Hermes/OpenClaw) against it, and have the model interview you deeply; curate out AI slop first.

## Tools / resources mentioned
- Guide (link shared in caption) — https://drive.google.com/file/d/1o9f5v4QX8J8ibZNkdN8KHNr0UbIQ1eI0/view

## Proposed implementation plan
1. Collect only your own writing/notes (remove AI-generated slop manually).
2. Organise into a knowledge base (markdown folder).
3. Have Claude interview you in depth and save answers to the knowledge base.
4. Point your agent (Claude Projects, or a local agent framework) at it and iterate until answers sound like you.
5. Read the creator's guide (Drive link in caption).

## Caveats / uncertainty
'Hermes/OpenClaw' named in reel; not verified here. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Become immortal with AI. #ai Fable 5 is so good, and with it disappearing behind a paywall soon, don’t let this chance slip away. Comment “Immortal” for the free guide. #fable
> 
> 🚨 Note: Automations on IG are down today. Here's the link: https://drive.google.com/file/d/1o9f5v4QX8J8ibZNkdN8KHNr0UbIQ1eI0/view

Transcript (auto, may contain errors):
> I'm gonna show you how to become in withoraO making a second brain. This is the knowledge bank you'll need. Second, have Fable 5, tune your own Hermes or OpenClaw against that knowledge base. It can do an iterative approach until it gets it exactly right and it's really good at it. Third, and the most important step, have Fable interview you deeply. This is what's really gonna change it. Now, here's the part that most people miss. If you've been generating a lot of AI Slop, and you gotta be honest, you're going to have to sort that manually before you start building your knowledge bank. This training data needs to come from you. Otherwise, you're just going to build a crappy version of chat GPT and you'll be sad with the results. I've put together a guide that walks you through this step-by-step and even has the prompt you'll need for the interview. Comment on mortal to get it. By the way, doing these three steps and you will have pulled off what was only sci-fi just a few months ago.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# Claimed leaked system prompt for cheaper models

I saved an Instagram reel by @jackroberts___ (https://www.instagram.com/jackroberts___/reel/DZ5XRhMCn7F/) and want to implement what it shows on my own machine.

## What the reel covers
Claims a frontier model's system prompt leaked and can be injected into a cheaper model for ~90% similar output.

## Tools / resources mentioned
- (none named)

## Proposed implementation plan
1. Treat as unverified hype.
2. Useful lesson: a lot of quality comes from a good system prompt; write your own and A/B test on cheaper models.

## Caveats / uncertainty
Unverified; overlaps with the other 'leak' save. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment "LEAK" and I'll send you the prompt.
> 
> Someone just leaked Fable 5's system prompt. Now you can run it for almost free.
> 
> Most people think the model is the magic. Half of it is the system prompt.
> 
> That prompt is now free to use. Inject it into Opus 4.8. One line of code. Output is 90% identical.
> 
> Like getting the recipe instead of dining out. Same dish. Fraction of the cost.
> 
> Frontier-level output. Budget model price. Already live on GitHub.
> 
> #fable5 #opus48 #github #aiprompts #aitools

Transcript (auto, may contain errors):
> Fable 5 just had its entire system prompt leaked. And what this means is that we can inject it into a cheaper model like Opus 4.8 and use it immediately. The best part is it only takes one line of code. And whilst it's not using Fable itself, it's using the system prompt behind it which we can use with any model. If you want access to the prompt, comment, leak below, and I'll send it over to you.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

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

---

# Kimi Work: desktop multi-agent AI

I saved an Instagram reel by @nivedan.ai (https://www.instagram.com/nivedan.ai/reel/DZsFJLmpF_z/) and want to implement what it shows on my own machine.

## What the reel covers
Moonshot's Kimi desktop app claims many parallel agents, local file access, browser control and scheduled tasks, with deep research, slides, docs and sheets.

## Tools / resources mentioned
- Kimi — https://www.kimi.com

## Proposed implementation plan
1. Download from the official Kimi site only.
2. Test with a bounded research task and check sources yourself.
3. Be careful granting local file and browser access; use a test account.

## Caveats / uncertainty
Claims ('zero hallucinations', 300 agents) are marketing. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> A Chinese lab just dropped a desktop AI that runs 300 agents simultaneously on your laptop. 
> 
> It's called Kimi Work. Launched this month. And it's free.
> 
> It sits on your machine, reads your actual local files, controls your real browser, and runs scheduled tasks overnight while you sleep.
> 
> I tested it myself.
> 
> Task 1: Research 100 companies in the EV market and build a full report with a presentation. 20 minutes later, 60-page PDF and a McKinsey-level deck. Fully sourced from Yahoo Finance, IMF, and Google Scholar. Zero hallucinations.
> 
> Task 2: Find 30 local businesses in LA with no website and build one for each. 30 minutes. 30 live websites, contact Excel sheet, and 30 pitch decks ready to sell.
> 
> That's a full weekend of work. 
> 
> Done before lunch.
> 
> It also comes with built-in Deep Research, Slides, Docs, Sheets, and a code agent. Everything you're paying for across 5 different tools, in one free desktop app.
> 
> This is what an AI agent is actually supposed to feel like.
> 
> Comment KIMI and I'll DM you the link.
> 
> #kimi#ad

Transcript (auto, may contain errors):
> A Chinese lab just destroyed anthropics entire business model and got over 90 million users overnight. Even Elon Musk called their work impressive and what they just dropped next is something nobody saw coming. The tool is called Kimmy and they just launched their brand new product called Kimmy Work on desktop and iOS. It can handle 200,000 tokens limit, can read over 50 files at once and run 300 agents at the same time. Developers who test every AI model just ranked it number one in the world. And while you're paying for Claude, Gemini and Chad GPT, Kimmy work does all of it for free. So I had to test it myself. Research 100 companies in the EV market and build me a full report with a presentation. It spun up over 100 agents working in parallel. 20 minutes later, I got a 60 page VDF report and a 14 page Muckenzie level PowerPoint. And all the information is accurate and fully traceable because Kimmy has access to Yahoo Finance, World Bank, IMF, Google Scholar and RC. You know how it is. Doing this manually would have taken 10 different tools and a full weekend of work. Then I gave it another task. I've been 30 local businesses in LA that don't have a website and build one for each of them. In 30 minutes, it delivered an Excel sheet with 30 businesses and their contact info. 30 live websites tailored for each one and 30 pitch decks for me to sell to the owners. All from one single prompt. Comment, Kimmy and I will DM you the tooling.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# Claude Cowork skill for backlinks

I saved an Instagram reel by @borja.obeso (https://www.instagram.com/borja.obeso/reel/DaNXxljy4NL/) and want to implement what it shows on my own machine.

## What the reel covers
One skill that does keyword research, writes stats pages, finds journalists and competitor backlinks, pulls contacts and sends outreach, and links content between its users.

## Tools / resources mentioned
- (none named)

## Proposed implementation plan
1. Get the skill link (DM-gated) and review exactly what it emails and publishes.
2. Start in draft mode: let it find opportunities and draft outreach, you approve sends.
3. Avoid automated link schemes; Google penalises them.

## Caveats / uncertainty
The 'auto-link between users' feature is a link-scheme risk. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> 🚨 BREAKING: Claude Cowork for Backlinks is live!
> 
> The task every SEO hates, handled.
> 
> Backlink building in 2026 looks like this:
> 
> “Find backlink opportunities for my business”
> 
> Here is what Claude does in 3 minutes with ONE skill:
> (and check the bonus at the end, it’s insane)
> 
> → Creates news and statistics pages that journalists love to cite
> → Finds and pitches journalists who cover your topic
> → Analyzes your competitors’ strongest backlinks
> → Finds the prompts your customers type into ChatGPT
> → Spots the listicles from those results that mention your competitors
> → Pulls the author’s contact info
> → Sends the email asking for the link
> 
> And here is the crazy bonus I mention.
> 
> The same skill also publishes your content. And thousands of people use it.
> 
> SO CLAUDE CAN LINK BETWEEN USERS AUTOMATICALLY 🤯 
> 
> 1. Someone publishes an article that touches topic A
> 2. You publish an article that goes deeper on topic A
> 3. Claude adds a link from their article to yours, so their reader gets the fuller answer
> 4. Google is happy because the reader is happy
> 
> This used to be a full-time job for 2 or 3 people at an agency.
> 
> Now Claude does it in minutes with the Distribb skill.
> 
> Comment “LINKS” for the skill and the instructions.
> 
> ♻️ Repost to get it TODAY.

Transcript (auto, may contain errors):
> So yeah, Cloth for backlinks is now live. One single skill does keyword research, writes content, and orchestrates backlinks from everyone using the same skill. Comment skill and I'll send you the link.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

# 5 Claude Code skills: Find Skills, Superpowers, Claude-Mem, Impeccable, Task Observer

I saved an Instagram reel by @nick_saraev (https://www.instagram.com/nick_saraev/reel/DaN0yYtPzjY/) and want to implement what it shows on my own machine.

## What the reel covers
A starter skill stack: a skill finder, Superpowers (plan/verify discipline), Claude-Mem (memory across sessions), Impeccable (frontend taste), Task Observer (learns your style).

## Tools / resources mentioned
- obra/superpowers — https://github.com/obra/superpowers
- thedotmack/claude-mem — https://github.com/thedotmack/claude-mem
- Impeccable (pbakaus/impeccable – verify) — https://github.com/pbakaus/impeccable
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview

## Proposed implementation plan
1. Superpowers: in Claude Code run `/plugin marketplace add obra/superpowers-marketplace` then `/plugin install superpowers@superpowers-marketplace` (check README for current commands).
2. Claude-Mem: follow the claude-mem README (plugin install) and confirm memory persists across a restart.
3. Impeccable: install per its README for frontend design guidance.
4. Find Skills / Task Observer: names from the reel, links DM-gated – search and verify before installing.
5. Install one at a time and run a small task to see the effect.

## Caveats / uncertainty
Install commands change; always follow the current README. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Comment “CLAUDE” to get this 5 Claude Code Skills to 10x your AI Sessions. 
> 
> Claude has over 100,000 skills but honestly you only need five of them.
> 
> The right five can replace half your workflow. 
> 
> The wrong ones just clutter your terminal with junk you never use.
> 
> First is Find Skills. You just tell it what you're building and it searches the whole library for you.
> 
> Then it finds the right skills, vets them for quality, and installs them in seconds.
> 
> Think of it like the librarian of the skills ecosystem. 
> 
> You ask, it pulls the perfect book off the shelf.
> 
> Second is Superpowers. 
> 
> You give it a task and it forces Claude to slow down before touching anything.
> 
> Plan properly, check its own work, catch its mistakes before you do.
> 
> This alone cuts your rework time by half. Especially on complex coding tasks.
> 
> Third is Claude Mem. This gives Claude memory across sessions, so it remembers your project and files. 
> 
> You never have to re-explain context every single morning again.
> 
> It's like upgrading from a goldfish to an elephant. 
> 
> Same Claude, way longer memory.
> 
> Fourth is Impeccable. This one's for frontend work. 
> 
> It gives Claude real design taste by pulling from premium UI references, so your output stops looking vibe-coded.
> 
> No more generic shadcn components or default Tailwind layouts. 
> 
> Your apps actually look like a designer touched them.
> 
> And finally, Task Observer. It quietly watches how you work, learns your style, and improves your other skills in the background. 
> 
> So your setup keeps getting smarter without you doing anything. That last part is wild. 
> 
> Most tools stay static after install. This one evolves with you.
> 
> Together these five turn Claude Code from a coding assistant into a full senior dev partner.
> 
> Faster, sharper, and tailored to how you actually build.
> 
> #Claudeai #claudecode #claudeskills #claudemem #aiskills

Transcript (auto, may contain errors):
> Claude is over 100,000 skills, but honestly, you only need five of them. First is find skills. You just tell it what you're building, and it'll search its entire skill library, find the right ones for you, and even install them on your behalf. The second is superpowers. You just give it a task, and it forces Claude to slow down, properly plan, and check its own work before actually touching the project itself. The third is Claude Mem. This gives Claude memory across sessions, or remembers your project and files, meaning you never have to re-explain anything again. The fourth is impeccable for frontend. It gives Claude real design taste by pulling from premium references, so your UI stops looking slop-vibe coded. And finally, there's task observer, which quietly watches how you work. It learns your style, and it constantly improves your other skills in the background for you based on that. So if you want to try these for yourself, just comment Claude down below, and I'll send them all to you directly.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.

---

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

---

# Humanise with Claude (same Wikipedia trick)

I saved an Instagram reel by @cyborggirll (https://www.instagram.com/cyborggirll/reel/DaNPkStyclB/) and want to implement what it shows on my own machine.

## What the reel covers
Same technique as /human: list the AI tells from Wikipedia, ban them, wrap it into a skill.

## Tools / resources mentioned
- Wikipedia: Signs of AI writing — https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing

## Proposed implementation plan
1. See the '/human' item – identical setup.
2. Don't rely on it to beat AI detectors; edit with your own voice.

## Caveats / uncertainty
Duplicate. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Humanise with Claude !

Transcript (auto, may contain errors):
> Do you want to humanize your text just like I did and got zero person in AI detection? Let me show you how. Go to Claude and type out this prompt saying, humanize all my text moving for works, so it doesn't sound like AI. And then go to Wikipedia and look up in the page with AI writing and list out the signs that gave it away and make sure you never do those things. Robotics tones, M dashes, filaments, all gets eliminated with this prompt. And if you want to take it a step further, make a Claude skill by typing out this and make sure to include everything that we have discussed. Now install the skill and before writing anything in Claude, use this and you'll be going to go comment down clouds at your channel. And if you like cool AI access, search for the cyber code for more.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
