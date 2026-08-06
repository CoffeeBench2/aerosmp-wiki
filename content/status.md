---
title: Server Status
---

# Server Status

Live, straight from the server. This updates every 30 seconds while the page is open.

<div id="aero-status" style="border:1px solid var(--lightgray);border-radius:10px;padding:1.2rem 1.4rem;margin:1.5rem 0;">
  <div style="font-size:0.85rem;letter-spacing:0.08em;text-transform:uppercase;opacity:0.6;">Coffee's Aero SMP</div>
  <div id="aero-state" style="font-size:1.6rem;font-weight:700;margin:0.35rem 0;">Checking…</div>
  <div id="aero-players" style="font-size:1.05rem;opacity:0.85;"></div>
  <div style="margin-top:0.9rem;font-family:monospace;font-size:0.95rem;">coffeeaerosmp.duckdns.org</div>
</div>

<script>
(function () {
  var HOST = "coffeeaerosmp.duckdns.org";
  function paint(state, colour, players) {
    var s = document.getElementById("aero-state");
    var p = document.getElementById("aero-players");
    if (!s || !p) return;
    s.textContent = state;
    s.style.color = colour;
    p.textContent = players || "";
  }
  function check() {
    fetch("https://api.mcsrvstat.us/3/" + HOST, { cache: "no-store" })
      .then(function (r) { return r.json(); })
      .then(function (d) {
        if (d && d.online) {
          var on = (d.players && d.players.online) || 0;
          var max = (d.players && d.players.max) || 0;
          paint("Online", "#3fa34d", on + " / " + max + " players");
        } else {
          paint("Offline", "#c94f4f", "Probably maintenance — check Discord");
        }
      })
      .catch(function () {
        paint("Unknown", "#b8862b", "Couldn't reach the status service");
      });
  }
  check();
  setInterval(check, 30000);
})();
</script>

> [!warning] Showing 0 players, or offline?
> That usually means **maintenance or an update**, not a dead server. We restart
> often to keep the pack current.
> **[Discord](https://discord.gg/AnFUh5vTz6)** has live status and restart notices.

---

## What the numbers mean

**Players** is the real count from the game server, not from the login gateway —
so it's the number of people actually playing right now.

**Offline** almost always means a restart in progress. They're usually short.
If it lasts, there'll be a notice in Discord explaining why.

---

## Having trouble connecting?

1. Check the status above — if it says Offline, wait for the restart
2. Make sure you're on the current pack version. If you have the Aero Core
   installed you'll be prompted from the main menu; see [[getting-started]]
3. Check your RAM allocation is **5–8 GB**, not more — see [[faq]]
4. Still stuck? Ask in [Discord](https://discord.gg/AnFUh5vTz6)
