# Connect a web-scraper to Claude for e-commerce data

I saved an Instagram reel by @emma.scrapes (https://www.instagram.com/emma.scrapes/reel/DdzlppRB7Ju/) and want to implement what it shows on my own machine.

## What the reel covers
Add 'Ultimate Web Scraper' as a custom connector in Claude; give it a store URL and it scrapes the whole catalog (prices, SKUs, stock, images, reviews) to an exportable table.

## Tools / resources mentioned
- Claude custom connectors (remote MCP) — https://support.anthropic.com
- Model Context Protocol — https://modelcontextprotocol.io

## Proposed implementation plan
1. Create an account with the scraper service (find Ultimate Web Scraper via its Chrome extension/site; no link in caption).
2. Copy the MCP server URL / key from its dashboard.
3. In Claude: Settings → Customize/Connectors → Add custom connector → paste the URL.
4. Ask Claude: 'Scrape all products from <url> including variants, images and price'.
5. Open the link Claude returns to the dashboard and export CSV/JSON.
6. Check the target site's ToS/robots.txt.

## Caveats / uncertainty
Third-party service; review its privacy/pricing. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> You can now connect Ultimate Web Scraper 🐼 to Claude to scrape any e-commerce data! 
> 
> You give your commands through Claude, and Claude will pass the task to Ultimate Web Scraper which will pull all the product data! (Think prices, stock, skus, availability, images, reviews, rating, etc. 🤯) Once the task is finished Claude will notify you and send you a link to your scraped data which is stored on your Ultimate Web Scraper dashboard 🤝
> 
> #claude #webscraping #ecommerce #automation #aitools

Transcript (auto, may contain errors):
> What the fuck? Go to Claude and click Customize. Click Add Custom Connector. Open the Scrum extension called Ultimate Web scraper. Copy this URL and paste it into Claude. With this tool, Claude can now script any website so you just give it a link. And it will scan the entire catalog and give you all the product data, including the images. And then of course you can export it.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
