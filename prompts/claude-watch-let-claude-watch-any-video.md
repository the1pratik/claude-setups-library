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
