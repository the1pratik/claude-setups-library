# 'What if' 3D scale explainer: stacking every human on Earth

I saved an Instagram reel by @realityrendered__ (https://www.instagram.com/realityrendered__/reel/Deov5ZTp5ae/) and want to implement what it shows on my own machine.

## What the reel covers
A one-minute 3D data-visualization reel that stacks every person on Earth (about 5 ft 3 in each) into one tower, with a running people counter and height readout passing landmarks from a basketball hoop to the Moon. No Claude or other tool is named in the caption, audio or on screen; it's an inspiration save for the format.

## Tools / resources mentioned
- Three.js (3D library for the browser; my suggestion, not from the reel) — https://threejs.org
- Claude Code — https://docs.anthropic.com/en/docs/claude-code/overview

## Proposed implementation plan
1. Idea only: the reel doesn't name the tool it was made with, so treat it as a format to recreate rather than a setup to copy.
2. Pick your own 'what if' scale question and have Claude do the math first: unit size, total count, and a list of milestones the stack passes (the reel uses about 5 ft 3 in per person, from 2 people for a basketball hoop to 241 million for the Moon and 8.2 billion for 34 times the Earth-Moon distance). Ask it to show its working and cite a source for each landmark height or distance.
3. Have Claude turn those numbers into a timed script: one milestone label per beat, a big counter ('PEOPLE' plus the number), the height in feet or miles underneath, and a short caption line every few beats.
4. Ask Claude to build the animation as a single web page with a 3D library such as Three.js (my suggestion): a low-poly scene and a camera that pulls back as the tower grows, moving from city to clouds to space to Earth as a ball.
5. Use a logarithmic camera pull-back so the jump from 2 people to 8.2 billion fits in about a minute, and add a closing twist (the reel ends with everyone standing side by side, one square meter each, covering about the land area of Puerto Rico).
6. Record the page at a vertical 1080x1920, add a voiceover, and re-check every on-screen number against Claude's working before posting.

## Caveats / uncertainty
The caption, audio and on-screen text never say how this was made or mention Claude, so the steps above rebuild the format from scratch rather than the creator's workflow. Three.js and Claude Code are my suggestions, not from the reel. The figures are the creator's; spot checks line up (8.2 billion x 5 ft 3 in is about 8.15 million miles, roughly 34 Moon distances), but verify any number you reuse. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> What if you stacked every human on Earth? #pov #whatif #simulation

Transcript (auto, may contain errors):
> What if you stacked every human on earth? It starts with you then everyone climbs on. Each person adds about 5'3. Your whole city. Passed the clouds. Passed. 62,500 people. That space. Passed.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
