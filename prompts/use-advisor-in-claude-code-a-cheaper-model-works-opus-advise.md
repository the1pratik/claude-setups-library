# Use /advisor in Claude Code: a cheaper model works, Opus advises

I saved an Instagram reel by @sully.omarr (https://www.instagram.com/sully.omarr/reel/De3Gaq0TiUj/) and want to implement what it shows on my own machine.

## What the reel covers
Claude Code's built-in /advisor command: a cheaper main model such as Sonnet does the routine work (renaming files, reading docs, running tests) and consults Opus only at hard decisions, so your usage limit lasts longer.

## Tools / resources mentioned
- Claude Code advisor docs (official) - https://code.claude.com/docs/en/advisor
- Claude Code - https://docs.anthropic.com/en/docs/claude-code/overview

## Proposed implementation plan
1. Update Claude Code to the latest version (`claude update`), since /advisor is a recent, experimental feature.
2. Pick a cheaper main model with `/model`, for example Sonnet. The advisor has to rank at or above your main model, so Sonnet main + Opus advisor is the pairing the reel describes.
3. Type `/advisor` and choose Opus in the picker, or run `/advisor opus` directly. Claude Code replies `Advisor set to` plus the model name and saves it as `advisorModel` in your user settings.
4. Check for the notice `Advisor Tool (experimental) is on and may use more tokens · /advisor` at the start of the session. If it doesn't appear, your plan, provider or main model may not support it (see caveats).
5. Work as usual. Claude decides when to consult the advisor (before committing to an approach, when an error keeps coming back, before calling a task done). You'll see an `Advising` line, and `Ctrl+O` shows the guidance. You can also ask for it in your prompt: `consult the advisor before you continue`.
6. Optional: use `claude --advisor opus` to turn it on for one session only, or add `"advisorModel": "opus"` to your settings file as a default.
7. Watch `/usage` over a few days to see whether your limit actually lasts longer, and turn it off with `/advisor off` if it doesn't help.

## Caveats / uncertainty
Verified on Oct 24, 2026 against Anthropic's official Claude Code docs (code.claude.com/docs/en/advisor): /advisor is real, built in and marked experimental. It needs the Anthropic API directly (not Amazon Bedrock, Google Cloud or Microsoft Foundry) and stays off if flag fetching is disabled, for example with DISABLE_TELEMETRY set. Advisor calls still count toward your plan limits, so 'never hit your limit' is the creator's hype; the docs only say it usually costs less than running Opus the whole time. Opus doesn't literally manage other agents as the caption says: Claude sends it the full conversation at decision points and applies its advice. The creator says '/advisors' in the audio, but the command is `/advisor`. The transcript is automatic and hears 'Claude' as 'cloud'.

## Source material
Caption:
> If you keep hitting your Claude limit try using /advisor next time where it properly uses opus to manage other agents

Transcript (auto, may contain errors):
> This is the easiest way to never hit your cloud limit, and it's built directly into cloud code. It's called Advisor. Here's how it works. A cheaper model does all of the work, like renaming files, reading docs, writing tests. It only calls Opus when it hits a hard decision. So like how your database should work, or if it needs to send a very important email. So Opus then acts as a manager, not as an intern. That way you get the best answers from Opus on the parts that matter, and your limit lasts way longer because all of the other models are a lot cheaper to run. So just open Cloud Code and type slash advisors and pick Opus.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
