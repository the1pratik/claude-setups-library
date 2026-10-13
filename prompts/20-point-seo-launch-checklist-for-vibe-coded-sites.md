# 20-point SEO launch checklist for vibe-coded sites

I saved an Instagram reel by @udayan.builds (https://www.instagram.com/udayan.builds/reel/DeZb5Wdht17/) and want to implement what it shows on my own machine.

## What the reel covers
Paste this checklist into Claude before publishing: SSR, robots.txt, sitemap, titles, meta, canonicals, OG images, schema, 404/301, analytics, Search Console and more.

## Tools / resources mentioned
- Google Search Console — https://search.google.com/search-console
- Google Analytics — https://analytics.google.com
- schema.org — https://schema.org

## Proposed implementation plan
1. Server-side render (or pre-render) pages so crawlers see content, not a blank SPA shell.
2. Add robots.txt and sitemap.xml; submit the sitemap in Search Console.
3. Unique <title> and meta description per page; exactly one H1 per page.
4. Canonical tags on every page.
5. Open Graph / Twitter images and tags.
6. Custom 404 page and 301 redirects for moved URLs.
7. Alt text on images; modern image formats; lazy loading.
8. Organization schema + breadcrumbs (JSON-LD); solid internal linking.
9. Google Analytics + Search Console verified; privacy policy and a contact page.
10. Ask Claude to audit the repo against all items and fix them one PR at a time.

## Caveats / uncertainty
List reconstructed from the spoken transcript (Whisper garbled a few words, e.g. 'WebP images'). Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Vibe-coded a site? Paste this list into Claude before you hit publish 👇
> 
> Most AI-built sites launch without half of these, and it’s why Google (and ChatGPT) can’t find them. Server-side rendering alone decides whether crawlers see your content or a blank page.
> 
> Comment “CLAUDE” and I’ll send you the exact prompt that adds all 20.
> 
> Save this for launch day 📌
> 
> #vibecoding #claude #seo #webdev #buildinpublic

Transcript (auto, may contain errors):
> Service ID rendering, robots.txt, site map.xml, unique title tags, better descriptions, 1s1 per page, canonical tags, open graph images, a custom 404 page, 301 reader records, all text, their p-emages, lazy loading, organizational schema, red crumbs, internal links, Google Analytics, search console, go privacy policy, go contact from the RaxialiSend.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
