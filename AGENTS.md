# AGENTS.md — thatcraftygibbon-links

Public **link tree** for That Crafty Gibbon. Tiny repo: one static page plus Wrangler. Do not overbuild docs or turn this into an app.

## How we work

- Nick **describes**. Agents **execute**. Nick **reviews** before a change is treated as committed.
- **PR-only** for this public static site. Open a PR; do **not** merge unless Nick asks.
- **Never Unraid APPLY from here.** Cerebro host mutations belong in [`unraid-server`](https://github.com/penguinpal77/unraid-server). Merge here is not host apply.
- Review is **iPhone-first**. Prefer short approval cards over long shell blocks.

## What this repo is

Cloudflare Workers **static assets**. No framework, no `package.json`, no checkout, no API.

| File | Role |
|------|------|
| [`index.html`](index.html) | The whole site: logo, “Handmade crafts and creations”, Folksy / Instagram / Facebook / [thatcraftygibbon.com](https://thatcraftygibbon.com) / email buttons. Narrow card column (`max-width: 480px`). |
| [`wrangler.jsonc`](wrangler.jsonc) | Worker `thatcraftygibbon-links`; `assets.directory` is `.`. |
| [`.gitignore`](.gitignore) | Ignores `.wrangler`, `.dev.vars*`, `.env*`. |

Preview locally with `npx wrangler dev`. Deploy only when Nick asks (`npx wrangler deploy`). There is no CI and no auto-deploy.

Keep the page a single column of tappable cards. Do not add pages, a bundler, or Next.js here.

## Secrets

None expected. Never commit tokens, Wrangler login, Cloudflare API keys, or `.env` / `.dev.vars` values. This public repo stays secret-free.

## Siblings

| Repo | Role |
|------|------|
| [`thatcraftygibbon-web`](https://github.com/penguinpal77/thatcraftygibbon-web) | Main marketing site (Next.js on Workers). |
| [`unraid-server`](https://github.com/penguinpal77/unraid-server) | Cerebro knowledge base. |

Do not edit siblings from a links PR.

## Priority

That Crafty Gibbon work comes **after** AI/Docker foundation and Home Assistant.
