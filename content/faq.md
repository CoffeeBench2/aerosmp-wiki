---
title: FAQ
---

# FAQ

## Can I play without buying Minecraft?

Yes. The server is **hybrid** — premium and offline (cracked) accounts both join
at the same address, and offline players get the same features, including custom
skins via `/skin`.

Offline players set a password on first join and use `/login` afterwards.

## The server list shows 0 players — is it dead?

Usually it means **maintenance or an update**, not that nobody plays. We restart
often to keep the pack current.

**Check [Discord](https://discord.gg/AnFUh5vTz6) for live status** — that's where
restart and downtime notices go.

## How much RAM should I give it?

**5–8 GB.** Do not go higher.

Over-allocating is a real failure mode, not a preference: the game dies during
loading with **no crash report**, the log just stops. That's the graphics driver
and Distant Horizons being starved of memory outside the Java heap. If that
happens to you, lower your allocation to 8 GB.

Everything else about frame rate — Potato mode, shaders, Distant Horizons — is
on **[[performance]]**.

## Why does the game take so long to load?

It's a 200+ mod pack with heavy worldgen and Distant Horizons. First launch is
the slowest; later ones are quicker.

## Why can't I break my own blocks?

Almost always a claim. Land claims are **full-height columns**, so you can be
inside someone else's claim while flying well above their build. See [[claims]]
for how to work through it.

## Where's the End?

**Currently closed.** Portals, waystones and teleports into it are all blocked.
Ask in Discord if you want to know when it opens.

## Why do I have to stand still during `/rtp`?

The server is preparing your destination before it moves you — that's what stops
new terrain hitching for everyone else. Moving cancels it, but a cancelled
teleport **doesn't** use up your cooldown.

## My teleport said the world took too long

The destination wasn't ready in time. Nothing was charged — just run it again.

## Can I use my own mods?

Client-side visual mods are usually fine. Anything giving an unfair advantage —
x-ray, radar, cheat clients — gets you removed.

Note the in-game updater manages the `mods` folder and removes older duplicate
versions of pack mods, so keep any additions to things the pack doesn't already ship.

## Do I lose my stuff if I log out in combat?

Yes. Disconnecting while combat-tagged kills you and drops your items where the
fight was. Don't combat log.

## I'm stuck / fell somewhere I can't get out of

Ask in **[Discord](https://discord.gg/AnFUh5vTz6)** with your coordinates. Staff
can move you.

## Can I play in VR?

Yes, and it's already in the pack — nothing extra to install. VR and desktop
players share the same world. See [[vr]].

## Is there anything to actually do?

There's a quest book with **43 chapters**, from your first log to your first
airship. It's optional and nothing is withheld if you ignore it, but it's the
quickest way to find out what this pack contains. See [[quests]].

## Why did my level drop?

Levels used to count advancements, and 86% of this pack's ~9,000 advancements
complete on their own the moment you touch an ingredient — so playtime was
worth about 2.5% of your level. Levels are now **pure playtime**. See
[[progression]].

## How do I link my Discord?

Run `/link <code>` in Discord — the code comes from in-game. Linking makes your
messages show your server identity in chat, and gets you on `/leaderboard`.
