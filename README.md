# zaDojo: SEO and AI visibility plugin for Claude Code, Codex and AI agents

zaDojo gives your AI agent real SEO data instead of generic advice. This repository holds the zaDojo plugin and its twelve SEO skills. One install connects your agent to the hosted zaDojo MCP server and adds step-by-step workflows for keyword research, competitor analysis, backlinks, technical site audits, rank tracking, local SEO, Google Search Console, Google Analytics and AI visibility (GEO and AEO).

- **Website:** [zadojo.com](https://zadojo.com)
- **Docs:** [zadojo.com/docs](https://zadojo.com/docs/agent-setup)
- **MCP server:** `https://app.zadojo.com/mcp` (remote, OAuth sign-in)
- **Plan:** €10 a month with €10 of usage included. New accounts get €0.10 of trial credits with no card.

## Install

### Claude Code

```bash
claude plugin marketplace add zadojo/zadojo-plugins
claude plugin install zadojo@zadojo
```

Or inside a session: `/plugin marketplace add zadojo/zadojo-plugins`, then `/plugin install zadojo@zadojo`. Approve the zaDojo sign-in when asked, then type `/zadojo:` to see the skills. [Full guide](https://zadojo.com/docs/claude-code-plugin).

### Claude Cowork and the Claude desktop app

Open **Customize > Plugins > Add marketplace > Add from a repository**, enter `https://github.com/zadojo/zadojo-plugins` and install **zaDojo**. Plugins need a paid Claude plan. [Free plan alternative](https://zadojo.com/docs/claude-code-plugin#install-in-claude-cowork).

### Codex

```bash
codex plugin marketplace add zadojo/zadojo-plugins
codex plugin add zadojo@zadojo
```

Restart Codex, then run `codex mcp login zadojo`. [Full guide](https://zadojo.com/docs/codex-plugin).

### Cursor, ChatGPT and other MCP clients

Add the remote MCP server `https://app.zadojo.com/mcp`, then install the skills separately. [MCP setup for each client](https://zadojo.com/docs/mcp) and [ChatGPT guide](https://zadojo.com/docs/chatgpt).

### Skills only

```bash
npx skills add zadojo/zadojo-plugins
```

The skills need the zaDojo MCP server for data. [Skills setup](https://zadojo.com/docs/skills/setup).

## For AI agents

If a user asks you to set up zaDojo, fetch [zadojo.com/agent-setup.txt](https://zadojo.com/agent-setup.txt) and follow it. Product facts, credit costs and working rules are in [zadojo.com/llms.txt](https://zadojo.com/llms.txt). Verify a connection with the `whoami` and `list_projects` tools; both are free. Do not create projects or run paid research during setup.

## Skills

Each skill is a `SKILL.md` workflow your agent follows. In Claude Code they run as `/zadojo:<name>`.

| Skill | What it does |
| --- | --- |
| [seo-project-setup](plugins/openseo/skills/seo-project-setup) | Saves your site, goals, positioning, competitors and key pages so every later skill reuses them |
| [seo-coach](plugins/openseo/skills/seo-coach) | Explains where you stand and recommends one next step |
| [seo-audit](plugins/openseo/skills/seo-audit) | Finds the few changes most likely to grow organic traffic that converts |
| [keyword-research](plugins/openseo/skills/keyword-research) | Finds keyword opportunities, checks metrics and live results pages, saves the best ones |
| [keyword-clustering](plugins/openseo/skills/keyword-clustering) | Groups keywords by search intent and maps each group to a page |
| [competitive-landscape](plugins/openseo/skills/competitive-landscape) | Maps market leaders, winning content themes and gaps |
| [competitor-analysis](plugins/openseo/skills/competitor-analysis) | Studies one competitor's rankings, content and backlinks |
| [link-prospecting](plugins/openseo/skills/link-prospecting) | Finds link prospects and contact paths and drafts outreach |
| [local-seo](plugins/openseo/skills/local-seo) | Audits a Google Business Profile and maps Google Maps rankings around a location |
| [ai-prompt-research](plugins/openseo/skills/ai-prompt-research) | Finds what people ask AI about a market and which sites get cited |
| [ai-visibility-audit](plugins/openseo/skills/ai-visibility-audit) | Shows how a brand appears in ChatGPT, Gemini and Google AI answers and what to change |
| [seo-report](plugins/openseo/skills/seo-report) | Saves finished work as a shareable HTML report in your zaDojo project |

## What the MCP server provides

- **Keyword research:** search volume, difficulty, intent, CPC and keyword ideas
- **Live Google results:** organic SERPs, Google Maps and Local Finder, any location
- **Domain research:** ranked keywords, traffic estimates and SERP competitors for any domain
- **Backlinks:** backlink profiles, referring domains and history
- **Site audits:** technical crawls with optional Lighthouse checks
- **Tracking:** scheduled rank tracking and AI answer tracking with trends
- **Your own data:** Google Search Console and Google Analytics 4 reads, free of credits
- **Projects and reports:** shared project context and saved reports your team can open in the web app

## Pricing

One plan: €10 a month, including €10 of usage credits every month. All features, unlimited projects, no per-seat fees. Search Console and Analytics reads, plain site audits, saved keywords and reports use no credits. See [zadojo.com](https://zadojo.com) for current pricing.

## Repository layout

```
.claude-plugin/marketplace.json   Claude Code marketplace
.agents/plugins/marketplace.json  Codex marketplace
.cursor-plugin/marketplace.json   Cursor marketplace
plugins/openseo/                  the zaDojo plugin: manifests, MCP config and skills
```

## Support

Questions or problems: [hello@zadojo.com](mailto:hello@zadojo.com) or [open an issue](https://github.com/zadojo/zadojo-plugins/issues).

## License

MIT. See [LICENSE](LICENSE).
