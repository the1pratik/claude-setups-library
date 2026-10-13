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
