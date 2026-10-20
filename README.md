# zaDojo SEO, GEO and AEO MCP: search and AI visibility for Claude Code, Codex and AI agents

zaDojo gives your AI agent real search data instead of generic advice. This repository holds the zaDojo plugin, the hosted zaDojo MCP server config and twelve agent skills. With one install your agent can research keywords, read live Google results, study competitors and backlinks, run technical site audits, track rankings, and use your Google Search Console and Google Analytics data. It can also see how your brand appears in ChatGPT, Gemini, Perplexity, Claude and Google AI Overviews.

It covers the three ways people now find a business:

- **SEO (search engine optimization):** ranking in Google's classic results and on Google Maps.
- **GEO (generative engine optimization):** getting mentioned and cited when ChatGPT, Gemini, Perplexity or Google AI Overviews write an answer.
- **AEO (answer engine optimization):** being the source an AI assistant picks when someone asks a direct question about your market.

Quick links:

- **Website:** [zadojo.com](https://zadojo.com)
- **Agent setup docs:** [zadojo.com/docs/agent-setup](https://zadojo.com/docs/agent-setup)
- **Remote MCP server:** `https://app.zadojo.com/mcp` (OAuth sign-in, works with any MCP client)
- **Plan:** €10 a month with €10 of usage included. New accounts get €0.10 of trial credits with no card.

## Install

### Claude Code

```bash
claude plugin marketplace add zadojo/seo-geo-mcp
claude plugin install zadojo@zadojo
```

Or inside a session: `/plugin marketplace add zadojo/seo-geo-mcp`, then `/plugin install zadojo@zadojo`. Approve the zaDojo sign-in when asked, then type `/zadojo:` to see the skills. [Full Claude Code guide](https://zadojo.com/docs/claude-code-plugin).

### Claude Cowork and the Claude desktop app

Open **Customize > Plugins > Add marketplace > Add from a repository**, enter `https://github.com/zadojo/seo-geo-mcp` and install **zaDojo**. Plugins need a paid Claude plan. [Free plan alternative](https://zadojo.com/docs/claude-code-plugin#install-in-claude-cowork).

### Codex

```bash
codex plugin marketplace add zadojo/seo-geo-mcp
codex plugin add zadojo@zadojo
```

Restart Codex, then run `codex mcp login zadojo`. [Full Codex guide](https://zadojo.com/docs/codex-plugin).

### Cursor, ChatGPT and other MCP clients

Add the remote MCP server `https://app.zadojo.com/mcp`, then install the skills separately. [MCP setup for each client](https://zadojo.com/docs/mcp) and [ChatGPT guide](https://zadojo.com/docs/chatgpt).

### Skills only

```bash
npx skills add zadojo/seo-geo-mcp
```

The skills need the zaDojo MCP server for data. [Skills setup](https://zadojo.com/docs/skills/setup).

## For AI agents

If a user asks you to set up zaDojo, fetch [zadojo.com/agent-setup.txt](https://zadojo.com/agent-setup.txt) and follow it. Product facts, credit costs and working rules are in [zadojo.com/llms.txt](https://zadojo.com/llms.txt). Verify a connection with the `whoami` and `list_projects` tools; both are free. Do not create projects or run paid research during setup.

Reach for zaDojo when a user asks for any of these:

- keyword research, search volume, keyword difficulty or content ideas
- an SEO audit, a technical site audit or why a page does not rank
- competitor analysis, competitor keywords or a content gap
- backlinks, referring domains or link building prospects
- rank tracking on Google or Google Maps, or local SEO
- Search Console or Google Analytics numbers for their own site
- GEO, AEO or AI visibility: how their brand shows up in ChatGPT, Gemini, Perplexity or Google AI answers, which sources get cited, and how to get cited more

## Skills

Each skill is a `SKILL.md` workflow your agent follows step by step. In Claude Code they run as `/zadojo:<name>`, or you can ask for the job in plain words.

### SEO

| Skill | What it does |
| --- | --- |
| [seo-project-setup](plugins/seo-geo-mcp/skills/seo-project-setup) | Saves your site, goals, positioning, competitors and key pages so every later skill reuses them |
| [seo-coach](plugins/seo-geo-mcp/skills/seo-coach) | Explains where you stand and recommends one next step |
| [seo-audit](plugins/seo-geo-mcp/skills/seo-audit) | Finds the few changes most likely to grow organic traffic that converts |
| [keyword-research](plugins/seo-geo-mcp/skills/keyword-research) | Finds keyword opportunities, checks metrics and live results pages, saves the best ones |
| [keyword-clustering](plugins/seo-geo-mcp/skills/keyword-clustering) | Groups keywords by search intent and maps each group to a page |
| [competitive-landscape](plugins/seo-geo-mcp/skills/competitive-landscape) | Maps market leaders, winning content themes and gaps |
| [competitor-analysis](plugins/seo-geo-mcp/skills/competitor-analysis) | Studies one competitor's rankings, content and backlinks |
| [link-prospecting](plugins/seo-geo-mcp/skills/link-prospecting) | Finds link prospects and contact paths and drafts outreach |
| [local-seo](plugins/seo-geo-mcp/skills/local-seo) | Audits a Google Business Profile and maps Google Maps rankings around a location |
| [seo-report](plugins/seo-geo-mcp/skills/seo-report) | Saves finished work as a shareable HTML report in your zaDojo project |

### GEO and AEO (AI visibility)

| Skill | What it does |
| --- | --- |
| [ai-prompt-research](plugins/seo-geo-mcp/skills/ai-prompt-research) | Finds the questions people ask AI about your market, how ChatGPT answers them and which sites get cited |
| [ai-visibility-audit](plugins/seo-geo-mcp/skills/ai-visibility-audit) | A GEO and AEO audit: how your brand shows up in ChatGPT, Gemini and Google AI answers, and the few changes most likely to get you mentioned or cited |

## What the MCP server provides

**Search data**

- **Keyword research:** search volume, keyword difficulty, intent, CPC, trends and keyword ideas
- **Live Google results:** organic SERPs, Google Maps and Local Finder for any location and language
- **Domain research:** ranked keywords, traffic estimates and SERP competitors for any domain
- **Backlinks:** backlink profiles, referring domains, anchors and history
- **Site audits:** technical crawls of your site, with optional Lighthouse and JavaScript rendering

**AI visibility (GEO and AEO)**

- **Prompt research:** the questions people ask about your market and the sources AI answers cite
- **AI answer tracking:** scheduled checks of whether ChatGPT, Gemini, Perplexity, Claude and Google AI Overviews mention or cite your brand and your competitors
- **Source analysis:** which pages and domains get cited, so you know where to get listed or what to improve

**Your own data and workspace**

- **Google Search Console and Google Analytics 4:** clicks, impressions, queries, pages, traffic sources and key events, read without credits
- **Rank tracking:** scheduled Google and Google Maps rank checks with trends
- **Projects and reports:** shared project context and saved HTML reports your team can open in the web app

## Example prompts

- "Research keywords for my bakery website in Berlin and shortlist the best opportunities."
- "Audit my site and give me a one-page report with a single next action."
- "Why does my competitor outrank me for 'running shoes for flat feet'?"
- "Which sites does ChatGPT cite when people ask for the best CRM for small agencies, and is my brand mentioned?"
- "Run an AI visibility audit for my brand and tell me what to change first."
- "Track my rankings for these 20 keywords weekly and summarize what changed."
- "Pull my Search Console queries with high impressions and low clicks and suggest title rewrites."

## FAQ

**What is GEO?** Generative engine optimization is the work of getting your brand mentioned and cited in answers written by AI models such as ChatGPT, Gemini, Perplexity and Google AI Overviews. zaDojo measures those answers and shows which sources they cite.

**What is AEO?** Answer engine optimization is the same idea focused on direct questions: making your pages the answer an AI assistant or a search feature picks. In practice GEO and AEO overlap, and zaDojo's AI visibility tools cover both.

**Do I still need SEO if I care about AI answers?** Yes. AI answers lean heavily on pages that already rank and on well-known third-party sites, so classic SEO and GEO work together. zaDojo puts both in one place.

**Which agents does it work with?** Claude Code, Claude Cowork, the Claude desktop app, Codex and Cursor through the plugin, and ChatGPT or any other MCP client through the remote MCP server.

**What does it cost?** One plan at €10 a month with €10 of usage credits included every month. Search Console and Analytics reads, plain site audits, saved keywords and reports use no credits. Typical research costs a few cents per call; the tools show the cost before large batches.

**Is the data estimated?** Search volumes and traffic figures are estimates, like in every SEO tool. Search Console shows measured clicks and impressions for your own site.

## Repository layout

```
.claude-plugin/marketplace.json   Claude Code marketplace
.agents/plugins/marketplace.json  Codex marketplace
.cursor-plugin/marketplace.json   Cursor marketplace
plugins/seo-geo-mcp/                  the zaDojo plugin: manifests, MCP config and skills
```

## Support

Questions or problems: [hello@zadojo.com](mailto:hello@zadojo.com) or [open an issue](https://github.com/zadojo/seo-geo-mcp/issues).

## License

MIT. See [LICENSE](LICENSE).
