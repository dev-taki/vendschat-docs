# Vendschat docs (Mintlify)

Public product documentation: **https://docs.vendschat.com**

This is a **new docs site**, not the Co-Admin ingest tree. Copy started from `notifyer_orm_backend/co-admin-docs`, then updated for the live dashboard (Broadcast **New broadcast**, sidebar **Integrations** including Agent Skill / Lovable / MCP).

GitHub: `vendocker/vendschat-docs` (private). Production branch: **`main`**. Mintlify GitHub App + DNS CNAME are dashboard/DNS steps — not Coolify.

Until DNS propagates, Mintlify also serves a `*.mintlify.app` URL.

## Run locally

Requires Node.js 20.17+ and the Mintlify CLI (`mint`).

```bash
npm i -g mint
cd vendschat-docs
mint dev
```

Open [http://localhost:3000](http://localhost:3000).

```bash
mint broken-links
```

## Edit

- Pages are MDX with YAML `title` + `description`
- Sidebar, brand, canonical URL: `docs.json` (`https://docs.vendschat.com`)
- Writing rules: `AGENTS.md`

Do **not** put secrets, demo passwords, or customer PII in these pages.

## Go live (trusted: Sajjad + Ishraq)

1. Mintlify dashboard → connect GitHub App to `vendocker/vendschat-docs` → production branch `main`
2. Custom domain: `docs.vendschat.com`
3. DNS (after Mintlify shows records): verification TXT first, then `CNAME docs` → `cname.mintlify.builders`
4. If Cloudflare: SSL Full (strict); do not orange-cloud until TLS is ready

Landing footer / `vendschat.com/docs` redirect is a **later** `vendschat-landing` PR, after this hostname resolves.

## vs Co-Admin ingest

`co-admin-docs/` in the backend still feeds **AI Workspace Co-Admin** search. Keep that tree in sync when you change operator-facing facts here, or Co-Admin will teach stale paths.
