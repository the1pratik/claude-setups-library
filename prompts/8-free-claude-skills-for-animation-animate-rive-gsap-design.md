# 8 free Claude skills for animation: Animate, Rive, GSAP, Design Skills, Wiggle, Remotion, Lottie, Three.js

I saved an Instagram reel by @okaashish (https://www.instagram.com/okaashish/p/DeOxisYD6ap/) and want to implement what it shows on my own machine.

## What the reel covers
A carousel of 8 open-source animation skills for Claude: UI motion taste, Rive state machines, official GSAP, React micro-interactions, logo animation, Remotion motion graphics, text-to-Lottie and Three.js 3D.

## Tools / resources mentioned
- emilkowalski/skills (Animate) — https://github.com/emilkowalski/skills
- BowTiedSwan/rive-skills — https://github.com/BowTiedSwan/rive-skills
- greensock/gsap-skills — https://github.com/greensock/gsap-skills
- freshtechbro/claudedesignskills — https://github.com/freshtechbro/claudedesignskills
- talknerdytome-labs/wiggle-claude-skill — https://github.com/talknerdytome-labs/wiggle-claude-skill
- haidrrrry/claude-remotion-skill — https://github.com/haidrrrry/claude-remotion-skill
- diffusionstudio/lottie (text-to-lottie) — https://github.com/diffusionstudio/lottie
- CloudAI-X/threejs-skills — https://github.com/CloudAI-X/threejs-skills

## Proposed implementation plan
1. Animate (UI motion: when to animate, easing, duration, polish): `npx skills@latest add emilkowalski/skills` (the pack also includes improve-animations, review-animations and animation-performance).
2. GSAP (official, by GreenSock): `npx skills add https://github.com/greensock/gsap-skills`.
3. Rive (interactive, state-machine animations): `npx skills add bowtiedswan/rive-skills`.
4. Claude Design Skills (React animations, page transitions, hover effects, 3D): in Claude Code run `/plugin marketplace add freshtechbro/claudedesignskills`, then `/plugin install <plugin>` for the ones you want (e.g. `gsap-scrolltrigger`, `threejs-webgl`).
5. Remotion motion graphics (kinetic type, explainers, logo intros, captions): `git clone https://github.com/haidrrrry/claude-remotion-skill.git` then `cp -r claude-remotion-skill/remotion-motion-graphics ~/.claude/skills/`.
6. Text-to-Lottie (vector animations without After Effects): `npx skills add diffusionstudio/lottie`, then ask your agent to use `text-to-lottie`.
7. Three.js 3D animation: `npx skills add cloudai-x/threejs-skills` (or clone and copy `skills/*` into `~/.claude/skills/`).
8. Wiggle (logo animation from a PNG/SVG, outputs Lottie, GIF or MP4): download the repo ZIP and add it as a skill per Claude's skills guide; its README says Claude Code handles the Python dependencies.
9. Install only the 2 or 3 that match your work, restart Claude Code, and test each with one small prompt (e.g. "animate this card hover with GSAP").

## Caveats / uncertainty
Repo names were read from the GitHub screenshots in the slides and checked on GitHub on Oct 21, 2026; the creator's own links are DM-gated. Install commands come from each README and can change, so check the README before running. Some overlap: claudedesignskills also ships GSAP and Three.js plugins.

## Source material
Caption:
> Comment "animate" and I'll send all the links.
> -
> #ai #claudeskills #freeclaudecode #claude #artificialintelligence

Slide text (carousel, 10 slides):
> 1. Top 8 Free Claude Skills For Animations (don't miss out on these)
> 2. Animate: Makes Claude much better at UI motion. It knows when to animate, what easing to use, how long it should last, and how to make it actually feel polished.
> 3. Rive Skills: For animations that react to what users do. Great for interactive buttons, characters, state-machine animations and game-like interfaces.
> 4. GSAP Skills: These skills teach AI coding agents how to correctly use GSAP (GreenSock Animation Platform), including best practices, common animation patterns, and plugin usage.
> 5. Claude Design Skills: For React animations and micro-interactions. Animated cards, page transitions, hover effects, staggered elements, gestures and smooth layout changes.
> 6. Wiggle: This one is specifically for logo animation. Give it a PNG/SVG logo and create things like bounce, pulse, rotate or looping animations. It can output Lottie, GIF or MP4.
> 7. Claude Remotion Skill: Turns Claude into a code-based motion graphics editor. Use it for kinetic typography, explainers, logo intros, captions, transitions and social videos.
> 8. Text-to-Lottie: Create Lottie animations without opening After Effects. It can generate production-ready vector animations from prompts, SVGs, screenshots or motion specs.
> 9. Three.js Animation: Give Claude actual 3D animation knowledge. Character animations, camera movement, morphing, GLTF models, skeletal animation and blending between motions.
> 10. Comment "animate" and I'll send you all the links.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
