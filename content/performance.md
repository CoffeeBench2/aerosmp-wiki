---
title: Performance
---

# Performance

This is a 200+ mod pack with Distant Horizons and real airship physics. It asks
a lot of a computer. Most of the fixes are one setting, and the most common one
is counter-intuitive.

---

## RAM: 5–8 GB, and no more

> [!warning] More RAM is not better. It is the single most common crash here.
> Over-allocating starves the graphics driver and Distant Horizons of memory
> **outside** the Java heap. The game dies during loading with **no crash
> report** — the log simply stops mid-line.
>
> If your game vanishes while loading and leaves nothing behind, this is almost
> certainly why. Come back down to 8 GB.

| Allocation | Result |
|---|---|
| Under 5 GB | Runs out of memory, stutters badly |
| **5–8 GB** | **What you want** |
| Over 10 GB | Native crashes, no crash report |

Having 32 GB in your machine does not mean giving 22 GB to Minecraft. The heap
shares the box with everything the heap doesn't cover.

## Potato mode

There's a **Mode** button in **Aero Settings**, reachable from the main menu.

**Potato** strips the pack back to what a weaker machine can actually run.
**Normal** puts it back. You can flip between them whenever you like — it isn't
a one-way door, and it doesn't touch your world or your keybinds.

If the pack is unplayable on your hardware, try this **before** you start
disabling mods by hand. Removing pack mods yourself will fight the updater,
which manages the `mods` folder and will put them back.

<!-- IMAGE SLOT: screenshot of Aero Settings with the Mode button -->

## Shaders

Shaders are optional and they are the most expensive thing you can turn on.

> [!warning] Don't run the Ultra shader preset on 8 GB
> Compiling a heavy shader pack needs a large block of memory *outside* the
> heap, at exactly the moment Distant Horizons wants the same. That combination
> is a native crash with no crash report — the same failure as over-allocating.
>
> If you want shaders, start from a lower preset and work up.

## Distant Horizons

DH is what lets you see terrain far past your render distance, which is most of
the point of flying. It is also doing real work in the background.

If you're struggling, **lower your render distance before you turn DH off** —
vanilla chunks cost far more per chunk than DH's simplified terrain does. Many
people run a modest render distance with DH reaching much further and get both
the view and the frame rate.

## Getting your FPS back, in order

Work down this list. Stop when it's good enough.

1. **Check your RAM allocation is 5–8 GB.** Yes, again. It's usually this
2. **Turn shaders off**, or drop to a lower preset
3. **Lower render distance** to 8–12 and let DH handle the horizon
4. **Switch to Potato mode** in Aero Settings
5. **Close the other things.** A browser with forty tabs is competing for the
   same memory that just crashed your game

Still bad? Ask in **[Discord](https://discord.gg/AnFUh5vTz6)** with your specs
and your allocation — that's usually enough to spot it.

---

## Related

- [[getting-started]] — setting the allocation in the first place
- [[faq]] — load times and other common questions
- [[vr]] — VR has its own requirements
