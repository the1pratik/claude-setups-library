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
