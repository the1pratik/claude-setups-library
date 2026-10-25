# Claude makes movies: 8 free repos for films made in code (Lemo-Opuscar is the one we could identify)

I saved an Instagram reel by @sebastianhardy_ (https://www.instagram.com/sebastianhardy_/p/De4XEoLjg_f/) and want to implement what it shows on my own machine.

## What the reel covers
A carousel of 8 free GitHub projects for making films entirely in code with Claude: 59 film styles, 15 motion-design styles, a cartoon starter kit, a 4K60 lyric video, launch-film prompts and two big libraries of viral Claude videos with their prompts. The slides never name the repos; only slide 1 (Lemo-Opuscar) could be matched and verified.

## Tools / resources mentioned
- lemomo-ai/lemo-opuscar (59 film styles, slide 1) — https://github.com/lemomo-ai/lemo-opuscar
- Lemo-Opuscar gallery — https://lemomo-ai.github.io/lemo-opuscar/

## Proposed implementation plan
1. Check what Lemo-Opuscar needs (from its README): Claude Code, Node 20+, ffmpeg and Python 3.11+ (or uv). The README says the styles are tuned for Claude Opus 5.5 and other models may not reproduce them well.
2. Install it as a skill (recommended): `claude plugin marketplace add lemomo-ai/lemo-opuscar` then `claude plugin install lemo-opuscar@lemolab`. On first use it downloads its guides, tools and style prompts to `~/lemo-opuscar`.
3. Or clone it instead: `git clone https://github.com/lemomo-ai/lemo-opuscar.git`, `cd lemo-opuscar`, then run `claude`. Films land in `films/<name>/` inside the repo.
4. Pick a style from the gallery (https://lemomo-ai.github.io/lemo-opuscar/) or the style index in `styles/README.md`.
5. Ask for a film in one line, e.g. "Make a 45-second film in the watercolor style about the coffee farm my family runs. Warm female narrator." Or type `/lemo-opuscar:lemo-opuscar` on its own and it walks you through the options.
6. When it asks, say yes to a storyboard first so you see the key shots before the full render, and ask for 1080×1920 if the film is for Reels (the default is 1920×1080 at 24 fps).
7. Budget for it: the README says one film takes the agent about 30 to 60 minutes and a fair amount of tokens.
8. For the other 7 projects (motion-design styles, cartoon kit, lyric video, launch film, viral-video and prompt libraries), the creator only shares links by DM (comment DIRECTOR). Get the names that way, then check each repo on GitHub before installing anything.
9. For overlapping tools you already have, see the "8 free Claude skills for animation" entry (Remotion, GSAP, Lottie, Three.js skills).

## Caveats / uncertainty
The slides show no repo names, links or GitHub screenshots, only titles and stats; the creator sends the 8 repos by DM. Slide 1 (Claude Code skill, 59 film styles, about 6.3K stars) matches lemomo-ai/lemo-opuscar, found by GitHub search and checked on Oct 25, 2026 (59 styles, MIT, about 7.2K stars). The other 7 could not be identified with confidence, so no repos or commands are given for them. Stats on the slides (424 videos, 703 prompts, 10.1K stars and so on) are the creator's claims. The 8 'slides' are silent screen recordings, so there was no audio to transcribe. It overlaps in spirit with the okaashish 8 free animation skills entry (DeOxisYD6ap), but none of that entry's repos are clearly shown here.

## Source material
Caption:
> Holy sh*t, Claude makes movies now. Just use these 8 free repos.
>
> Comment «DIRECTOR» and I'll send you all 8 repos plus the exact setup.
>
> Follow @sebastianhardy_ for the AI systems I use to run the business.
>
> #claudeai #aivideo #motiondesign #github #aitools

Slide text (carousel, 10 slides; slides 2 to 9 are silent screen recordings):
> 1. Holy sh*t, Claude makes movies now. Just use these 8 free repos
> 2. 01 Pick a style. Get a film. (Claude Code skill · 59 film styles) A free Claude Code skill with 59 film styles. Pick one, tell Claude the story, and it writes the picture, the music and every cut in code. [GitHub stars 6.3K · Film styles 59]
> 3. 02 Motion design from 1 prompt. (15 styles · one prompt each) 15 motion-design styles, each a finished 10-second film with the exact prompt and code. Swap in a client's words and it's their brand intro. [Styles 15 · Prompts ALL 15]
> 4. 03 Hand-painted cartoons. (Cartoon starter kit) A starter kit with a ready cartoon character and 31 acted emotions. Ask for a 15-second scene and Claude storyboards, paints and renders it. [Emotions 31 · License MIT]
> 5. 04 A music video in 4K60. (Lyric music video, all code) Claude timed every word of the song, designed 17 scenes and rendered a lyric video you can export in 4K at 60 frames a second. [Scenes 17 · Export 4K60]
> 6. 05 Nobody wrote the scenes. (Same song, cartoon cut) Same song, a whole new cartoon. The only brief was the character and one line: make every lyric look interesting. Claude directed the rest. [Scenes by humans 0 · AI drafts 2]
> 7. 06 A launch film for $2. (Startup launch film, one prompt) 18 full prompts and 54 real cases. The shortest prompt turned out a startup launch film like this in about a minute for two dollars. [Prompts 18 · Cases 54]
> 8. 07 What actually goes viral. (424 Claude videos, sorted) 424 videos people made with Claude 5.5, each linked to the original post and sorted by type. This ocean is pure code, no camera. [Videos 424 · Made with Opus 301]
> 9. 08 703 prompts behind hits. (The biggest prompt library) The biggest library of viral Claude videos, each with the prompt that made it. Copy one, paste it into Claude, and get a film like it. [GitHub stars 10.1K · Prompts 703]
> 10. Comment "DIRECTOR" for my guide. I'll send you all 8 links, the 10-minute setup, the 10 prompts I'd start with and 5 ways to get paid for these films.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
