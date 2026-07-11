# 🌺 Super Jumper

A Mario-style platformer inspired by *Lilo & Stitch*, built as a single HTML file so it runs
beautifully in Safari on **iPhone and iPad** (with big on-screen touch buttons) as well as on any
desktop browser. All graphics are drawn in code (original, "inspired-by" characters — no copyrighted
assets), and all sounds are generated with WebAudio, so there is nothing to download or install.

---

## 🚀 How to start the game

### Play on this Mac

```bash
cd ~/galexand/super-mario
python3 serve.py
```

Then open <http://localhost:8642> in your browser.

`serve.py` is a tiny wrapper around Python's built-in web server that adds **no-cache headers**, so
after any change to the game a simple page reload is always enough (no stale versions).

### Play on iPhone / iPad (same Wi-Fi)

1. Start the server on the Mac (see above) and keep it running.
2. Find the Mac's IP address: **System Settings → Wi-Fi → Details** (e.g. `192.168.1.23`).
3. On the iPad/iPhone, open Safari and go to `http://YOUR-MAC-IP:8642`.
4. Tap **Share → Add to Home Screen** — the game launches full-screen like a real app.

### Play from anywhere (no Mac needed)

Drag `index.html` onto [Netlify Drop](https://app.netlify.com/drop) — you get a free permanent URL
that works on any device. Re-upload the file whenever the game is updated.

---

## 🎮 Controls

| Action | Touch (iPad/iPhone) | Keyboard |
|---|---|---|
| Run left / right | ◀ ▶ buttons | ← → or `A` / `D` |
| Jump (hold = higher) | ⬆ button | ↑, `Space`, or `W` |
| Fire the pistol | green ✦ button (appears once found) | `F` or `X` |
| Pause / resume | tap the screen | `P` |

Stitch fires in the direction he is facing. Jumps have hidden kid-friendly forgiveness
(coyote time + jump buffering).

---

## 🗺 The adventure — everything that was asked for

### The worlds (11 levels, four lands)

| Worlds | Scenery |
|---|---|
| 1 – 3 | **Hawaii** — volcanic mountains, green hills, palm trees with coconuts |
| 4 – 7 | **The beach** — ocean horizon with waves, sand dunes, beach umbrellas, sandy ground |
| 8 – 10 | **Alien planet** (Jumba's homeworld vibes) — purple night sky, stars, two moons, crystal spires |
| 11 | **Inside Lilo's house** — warm wooden walls, night windows with curtains, family photos, couch, lamp and bookshelf |

Difficulty ramps up steadily: wider gaps, more villains, and armed enemies in the final worlds.
World 10 is the no-friends final gauntlet.

### The hero

- **Stitch-inspired blue alien** — big floppy ears, four arms once Lilo joins the team.
- 3 hearts (up to 5 with Nani), score, coins, and a flag at the end of every world.

### Power-ups

- 🥪 **Panini blocks** — bump the sandwich block and a walking panini pops out. Eating it makes
  Stitch **grow bigger**; while big, a hit only shrinks him back (no heart lost).
- 🔫 **Plasma pistol** (Worlds 7–10) — a floating ray-gun pickup. One bolt defeats most villains;
  Gantu takes two (first knocks him into his shell). Bolts can shoot enemy bolts out of the air.
- 🛸 **Rideable spacecraft** (World 5) — walk into the parked saucer to board it and **fly**:
  hold jump to rise, release to sink. Enemy contact crashes the ship instead of hurting Stitch.

### Friends to discover (touch them for their gift — gifts survive lost hearts)

| World | Friend | Gift |
|---|---|---|
| 2 | **Pleakley** | Coin magnet — nearby coins fly to you |
| 3 | **David** | Surf jump — permanently higher jumps |
| 4 | **Lilo** | Speed boost + Stitch's second pair of arms |
| 5 & 8 | **Nani** | +1 max heart (up to 5) |
| 6 | **Jumba** | Shield bubble that absorbs one hit |
| 7 & 9 | **Angel** | Refills all hearts |

### Villains

- 🐹 **Hamster villain** (Hämsterviel-style) — quick, caped; **cries a fountain of tears** when stomped.
- 🦈 **Big gray bruiser** (Gantu-style) — first stomp tucks him into his **shell like a turtle**
  (harmless while hiding, pops back out after ~5 s); stomp the shell to defeat him.
  From World 7 he carries a **blaster and shoots back**.
- 🔴 **Leroy, the red clone** — fast and hops; from World 5 he **drops out of a flying saucer**
  when you approach. From World 9 he's armed too.
- 🥪 **Reuben (X-625)** (Worlds 3–8) — the lazy golden clone who stands around and **throws
  sandwiches** at you. His sandwiches never hurt: they only shrink a big Stitch.
- 🧪 **The experiments** (they shoot, except Babyfier):
  - **Babyfier (151)** in World 6 — pink fluffball, behaves like the hamster (and cries when stomped).
  - **Amnesio (303)** in World 7 — touch or bolt wipes Stitch's memory: **back to World 3!**
  - **Sample (258)** in World 8 — his beat curse **doubles your runs and jumps** for a while (🎵 in the HUD).
  - **Fibber (032)** in World 9 — the dangerous one: costs **two hearts** (Jumba's shield still saves you).
  - All four join the final showdown in World 11.

### High scores

- At the end of every run a dialog pops up to **type your name** (native keyboard on iPad)
  and save the score.
- The **top 10 scores with names** are kept in the browser's localStorage (they survive closing
  the app); the best 3 are shown on the title screen. Your name is remembered for next time.

---

## 📁 Project files

| File | Purpose |
|---|---|
| `index.html` | The entire game — engine, levels, art, sound, UI. Edit levels in the `LEVELS` array (legend in the comments above it). |
| `serve.py` | Dev server with no-cache headers on port 8642. |
| `.claude/launch.json` | Preview-server config for Claude Code. |

Built with ❤️ by Claude Code for a young platforming fan and his ohana.
*Ohana means family — family means nobody gets left behind.*
