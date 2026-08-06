---
title: "Setup notes (do not publish)"
---

# Setup notes — delete or exclude before publishing

This file is for you, not for players. Everything else in this folder is
player-facing.

## What's here

| File | Status |
|---|---|
| `index.md` | Home page |
| `getting-started.md` | Install (both paths), RAM, first login |
| `claims.md` | FTB Chunks vs AeroClaims — the big confusion source |
| `commands.md` | Every command with real cooldowns from the live config |
| `airships.md` | Building, claiming, naming, the capture trap |
| `faq.md` | Premium/offline, 0 players, RAM, End closed |

## ⚠️ Never publish the Obaa vault

This is a **separate** vault on purpose. `D:\aerosmp-obaa` holds server IPs, the
backend address, secret filenames, deployment steps and the DB host. Publishing
it would undo the git history purge that scrubbed IPs in the first place.

Only ever point a publisher at `D:\aerosmp-wiki`.

Nothing in these pages names the backend, the gate's raw IP, the panel, the
database, or how auth works. Keep it that way — the gate hostname
`coffeeaerosmp.duckdns.org` is the only address that belongs on a public page.

## Publishing with Quartz (free)

1. Create a **new public GitHub repo**, e.g. `aerosmp-wiki`. Do **not** use the
   modpack repo — that one stays unadvertised with no Source/Issues links.
2. Scaffold Quartz into it (`npx quartz create`).
3. Copy these `.md` files into Quartz's `content/` folder.
4. Push. The bundled GitHub Action builds and deploys to GitHub Pages.
5. Point a subdomain at it — `wiki.coffeeaerosmp.duckdns.org`, or a real domain.
6. Link it from the Modrinth description and Discord.

Alternative if you'd rather not touch a build config: **Obsidian Publish**
($8/mo) publishes this vault directly with no setup.

## Before it goes live — fill in

- [ ] Discord invite link — referenced on `index`, `getting-started`, `faq`,
      `claims`, `airships`. Search for "Discord" and add the real link
- [ ] A **rules** page — I didn't invent one; write your actual rules
- [ ] Confirm `/register` and `/link` flows match what players really see. I
      documented these from config and code, not from playing through them
- [ ] Confirm the **starter 300 spurs** and **daily reward** wording matches what
      players get
- [ ] Decide whether to say "200+ mods" (counted 218 jars in `overrides/mods`,
      some of which are libraries)

## Facts these pages are built on

Taken from the live server config, so they're accurate as of 2026-08-06 — but
**they'll drift when you change settings**:

- `/rtp` 15 min · `/spawn` 3 h · `/home` 5 min · `/back` 5 min window, 10 min lock
- `/tpa` request expires 60 s · `/daily` every 20 h
- Login timeout 3 min · starter bonus 300 spurs
- FTB Chunks 500 chunks per player, party limits now **SUM** (each member brings
  their own allowance)
- AeroClaims 250 blocks per claim
- The End is **locked** (`lockEndDimension = true`)
- Combat logging kills you · PvP allowed in claims

If you change any of those, update `commands.md` and `claims.md` to match.
