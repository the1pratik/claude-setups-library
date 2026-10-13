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
