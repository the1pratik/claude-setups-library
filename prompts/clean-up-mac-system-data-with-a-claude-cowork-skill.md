# Clean up Mac 'System Data' with a Claude Cowork skill

I saved an Instagram reel by @arthsawale (https://www.instagram.com/arthsawale/reel/Deb74_2T2uc/) and want to implement what it shows on my own machine.

## What the reel covers
The creator taught Claude Cowork where macOS hides 'System Data' and what is safe to delete, saved that as a reusable skill, and now asks Cowork to clean the Mac on demand. He reports about an 80% drop in System Data.

## Tools / resources mentioned
- Claude Cowork — https://claude.com/product/cowork
- Get started with Claude Cowork (Claude Help Center) — https://support.claude.com/en/articles/13345190-get-started-with-cowork
- Back up your Mac with Time Machine (Apple Support) — https://support.apple.com/en-us/104984

## Proposed implementation plan
1. Make a full Time Machine backup first (the reel's own pro tip) so any deletion can be undone.
2. Open Claude Cowork in the Claude desktop app (see the official 'Get started with Cowork' guide) and give it access only to the folders you want it to inspect.
3. Ask Claude to audit storage first, read-only: list the biggest folders under ~/Library (caches, logs, app support, old iOS backups, Xcode data, etc.) with sizes, and explain what each one is.
4. Review that list together and agree on a 'safe to remove' rule set (e.g. caches and logs yes; Mail, Photos libraries, keychains and anything in /System no).
5. Have Claude write those rules into a skill (a SKILL.md with where to look, what's safe, and 'ask before deleting anything over X GB'), so the next clean is one request.
6. Run the skill, approve each deletion when Cowork asks, then check System Settings > General > Storage to see the before/after.
7. Re-run monthly, or schedule it as a Cowork task, keeping the ask-before-deleting rule in place.

## Caveats / uncertainty
The creator's actual skill is only offered via 'comment clean', so it isn't included here; these steps rebuild the idea from scratch. The 80% figure is the creator's claim. Deleting the wrong Library folder can lose data or break apps, so keep the backup and approve deletions one by one. The caption is cut off in the app. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> My Mac kept filling up with System Data. So I made Claude [text cut off here] . #Claude #ClaudeAI #ClaudeCowork #MacBook #macOS MacTips AIAutomation AITools Productivity TechTips MacBookPro AppleTips StorageFull SystemData CleanMyMac DigitalDeclutter WorkSmarter CreatorTools AIForCreators TechReels ArthSawale

Transcript (auto, may contain errors):
> I love my Mac but it keeps filling up which is computer. Even after watching countless tutorials and cleaning 20 odd folders, there is still no way of properly cleaning it all. So I made Claude be clean it for me and you'll be shocked by the results. If you haven't heard of Claude Gowork, it basically takes control of your entire computer and uses it like a really smart human being. It works on its own, you can schedule any task and it will ask you before doing anything important. If you ask it to clean your Mac, it will do an okay job but not a great one. So I spent our teaching Claude exactly where to look and what's safe to remove and turn it into a skill. So now I just open Gowork, ask it to clean my system and let it do it magic. Pro tip, take a time machine back up before any deep clean, better safe than sorry. And 80% drop in system data. I could never do that much by hand. Comment clean and I'll send you the skill for free.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
