# Turn a Wi-Fi smart light into your own Mac app

I saved an Instagram reel by @sneha_sidequest (https://www.instagram.com/sneha_sidequest/reel/Debj3F3uxYE/) and want to implement what it shows on my own machine.

## What the reel covers
Following the 'Reverse Engineer Anything' trend, the creator had Claude work out how her Philips WiZ tubelight is controlled over home Wi-Fi and build a small Mac app for it in about five minutes, without needing the repo. She notes the light has no password, so anyone on the network can control it.

## Tools / resources mentioned
- Reverse Engineer Anything / REA (named in the reel, link not given) (no verified link)
- pywizlight (open-source WiZ light library; my suggestion, not from the reel) — https://github.com/sbidy/pywizlight
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview

## Proposed implementation plan
1. Pick a device you own on your home Wi-Fi (the reel uses a Philips WiZ light) and note its IP address from your router or the vendor app.
2. In Claude Code, ask Claude to research how that device is controlled locally before touching any binaries; for WiZ lights an open-source Python library, pywizlight, documents the local protocol.
3. Have Claude write a tiny script that turns the light on/off and changes brightness, and test it from the terminal.
4. Once that works, ask Claude to wrap it in a small Mac menu-bar app (e.g. SwiftUI, or a Python menu-bar library) with on/off and brightness controls.
5. Optional: only reach for the 'Reverse Engineer Anything' tooling if there's no documented local API; the reel says Claude didn't need it for this light.
6. Security check: since the light accepts commands from anyone on the network, consider putting smart-home devices on a separate guest/IoT network.

## Caveats / uncertainty
The 'Reverse Engineer Anything' (REA) repo isn't linked in the post, and the 180k-star count is the creator's claim; verify the exact repo before installing. pywizlight is my suggestion for WiZ lights, not something the reel mentions. Only do this on devices you own. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> i reverse engineered my room light with AI 💡
> 
> → REA (reverse engineer anything) just crossed 180k stars on github
> → someone turned their AC into a mac app, and PS5 jailbreaks are blowing up (allegedly with AI 👀)
> → i tried it on my philips tubelight… claude didn't even need the repo. 5 mins later i had a mac app for my light
> 
> the light has zero password btw. anyone on your wifi can control it 💀
> 
> send this to the friend who still gets up to switch off the light
> what would you reverse engineer first?
> 
> #reverseengineering #claudeai #smarthome #philipswiz #sidequestexplains

Transcript (auto, may contain errors):
> I engineered my room light in five minutes and I didn't write a single line of code. Everyone's doing this right now. There's a repo called Rhea, reverse engineer anything. 180,000 stars on GitHub. It plugs, clod or codex into real reverse engineering tools. So your AI can pull up a part. One guy did his AC and built a Mac app for it. 1.7 million views. And this week, PS5 jailbreak's blew up. The funny part, the light has zero password. Anyone on my wifi can control it. Until now, you use stuff exactly how the company built it. Now you can just make it yours. Possibilities are endless. What would you reverse engineer first?

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
