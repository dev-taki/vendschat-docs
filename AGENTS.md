# Vendschat documentation (Mintlify)

## About this project

- Public product docs: **https://docs.vendschat.com**
- GitHub: `vendocker/vendschat-docs` (private). Production branch: `main`
- Pages are MDX with YAML frontmatter (`title`, `description`)
- Site config: `docs.json` (canonical URL is `https://docs.vendschat.com`)
- Local preview: `mint dev` (CLI: `npm i -g mint`)
- Mintlify docs MCP: `https://www.mintlify.com/docs/mcp`

## Terminology

- **Vendschat** — product name (not Notifyer)
- **Chat** — shared inbox
- **AI Agent** — customer-facing bot on WhatsApp / Messenger / Instagram
- **AI Workspace Co-Admin** — internal helper; **never** sends customer messages
- **Agent Skill** — hosted skill + MCP so operators work from Cursor, Lovable, Claude Code, or any MCP client
- **Broadcast** — sidebar **Broadcast → New broadcast** (not “Chat composer only”)
- **Integrations** — **Settings → Workspace → Integrations** (`/settings/workspace/integrations`). Agent Skill, Lovable, MCP, Zapier, Make, n8n. `/integrations` is not the catalog.
- **Workspace** — tenant container; **Member (Chat-only)** vs Admin vs Owner

## Style

- English artifacts only
- Active voice, second person
- Sentence case headings
- Bold UI labels: **Broadcast → New broadcast**
- How-to pages: Mintlify `<Frame>` + `/images/*.png` from the live app. Never Chat PII, WABA/phone IDs, or team emails.
- Brand logo: SVG wordmark at Mintlify navbar size (`width="180"` `height="23"`). Icon + **Vendschat**. `/logo/light.svg` + `/logo/dark.svg`. Favicon `/favicon.png`. Partner marks in `/images/logos/`. Logo does not invert.
- Illustrative companies (Metro Clinics, BloomBox) — never claim real customers
- No testimonials, fake metrics, or medical advice in examples
- Paid plans start at **$20/mo**; first 100 customers **80% off**

## Content boundaries

Document what operators see in the dashboard. Do not document:

- Database tables, workers, encryption keys, Coolify, or production SSH
- Demo account credentials
- Unwired or planned UI as if it shipped

When the live app disagrees with `co-admin-docs/`, **the live app wins**. Update both trees.

## Must-update pages when the product changes

- `broadcasts/campaigns.mdx`
- `integrations/agent-skill.mdx`
- `integrations/integrations-and-automation-overview.mdx`
- `ai-agents/creating-and-training-agents.mdx`
- `use-cases/clinics-and-appointments.mdx`
