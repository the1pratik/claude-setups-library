# Claude can scrape any website (scraper MCP)

I saved an Instagram reel by @emma.scrapes (https://www.instagram.com/emma.scrapes/reel/Db8-zZch_mH/) and want to implement what it shows on my own machine.

## What the reel covers
Same Ultimate Web Scraper connector as the e-commerce reel, used for general websites; returns a data table you can export.

## Tools / resources mentioned
- Model Context Protocol — https://modelcontextprotocol.io

## Proposed implementation plan
1. Open Claude → Customize → Add custom connector.
2. On the scraper's site choose 'Claude MCP' and copy the name + key/URL.
3. Paste and click Add.
4. Give Claude one or more URLs and ask it to extract the data.
5. Export from the returned table link.

## Caveats / uncertainty
Duplicate of the e-commerce scraper item; third-party service. Some names come from an automatic transcript and may be misspelled; links that weren't in the post are flagged.

## Source material
Caption:
> Claude can now scrape any website 
> 
> Connecting it with Ultimate Web Scraper  gives Claude access to a complete scraping infrastructure to scrape any website
> 
> You just give Claude one or more website links and it will extract all the data \def6
> 
> #ClaudeAI #WebScraping #MCP #AITools #Automation

Transcript (auto, may contain errors):
> Wait, cloud can do what now? Just hop over the cloud and click on customize. We're gonna add a custom connector. I'm gonna go to this website, which will give cloud web scraping skills. Just click on cloud MCP and follow the steps. So then you'll have the name, the cloud key, and you're just gonna click on add. Now that it's connected to cloud, I'm gonna go to a website and copy the link. Place the link into cloud and ask it to script a website for you. When it's done, it will give you a link to the data table. As you can see, it grabbed all the product data from each variant, including all the images. And then you can export it to the file type that you need.

## What I want from you
1. First ask me about my OS, what I already have installed (Claude Code, Node, Python, git), and my goal for this setup.
2. Verify that any repo, package or command above actually exists before telling me to run it; if unsure, say so and suggest how to check (official docs/README).
3. Then walk me through the implementation one step at a time, waiting for me to confirm each step's output before moving on.
4. Explain briefly why each step matters, and finish with a quick test that proves the setup works.
