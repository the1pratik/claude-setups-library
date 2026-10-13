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
