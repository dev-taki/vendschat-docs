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
- **Integrations** — sidebar **Integrations** (`/integrations`), not a buried Settings-only catalog
- **Workspace** — tenant container; **Member (Chat-only)** vs Admin vs Owner

## Style

- English artifacts only
- Active voice, second person
- Sentence case headings
- Bold UI labels: **Broadcast → New broadcast**
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
