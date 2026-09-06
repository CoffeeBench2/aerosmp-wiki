---
title: Levels & Progression
---

# Levels & Progression

Your level is on the sidebar, next to your playtime. It measures **one thing:
hours actually played.** Not advancements, not kills, not wealth.

That's deliberate, and it used to be otherwise — see [[changelog]] if you
remember your level being much higher once.

---

## How the level is calculated

```
Level = 1 + 2 × √(hours played)
```

Rounded down. Which means:

| Hours played | Level |
|---|---|
| 1 | 3 |
| 20 | 10 |
| 50 | 15 |
| 144 | 25 |
| 600 | 50 |

The curve flattens on purpose. Early hours move you quickly, and a very high
level means somebody has genuinely lived here — it can't be rushed in a weekend
and it can't be bought.

> [!note] Your level is not power
> It unlocks nothing and grants no advantage. It is a record of time spent, and
> that's all it's meant to be.

## AFK time doesn't count

Idle for **5 minutes** and you're marked AFK; that time stops counting toward
playtime and your level. Come back and it resumes immediately.

This is why a level can look lower than a play session felt. Standing in a base
while a farm runs is not playing, and an AFK jiggler won't beat it either — the
tracker takes the idle stretch back out of your total rather than just pausing.

Boats, minecarts and horses are handled: you're not marked AFK while riding one.

## Playtime and the leaderboard

`/leaderboard` in **Discord** ranks the top 10 by playtime. Since levels are
playtime, the two now agree — which they historically didn't.

Link your account with `/link` to appear on it. Unlinked players are never
mentioned by the bot.

<!-- IMAGE SLOT: screenshot of the in-game sidebar showing level and playtime -->

## Seasons

The server runs in **seasons**. A new season resets the world so everyone starts
on fresh terrain together, rather than arriving to a map where the good spots
went years ago.

What carries across a season boundary:

- **Your account, password and skin** — you don't re-register
- **Your total playtime and veteran status.** Time served is never wiped
- **Season 1 veterans were paid out** at the Season 2 rollover, scaled by hours

What doesn't: your builds, your items and your claims. Those belong to the world
that ended.

We're currently in **Season 2**. Season endings are announced well ahead in
**[Discord](https://discord.gg/AnFUh5vTz6)** — nobody gets surprised by one.

---

## Related

- [[economy]] — daily and vote rewards
- [[commands]] — `/profile` and the Discord commands
- [[faq]] — linking Discord
