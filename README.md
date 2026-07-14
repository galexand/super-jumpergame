# 🌺 Ohana Arcade

A little collection of *Lilo & Stitch* inspired browser games, each built as a single HTML file so
they run beautifully in Safari on **iPhone and iPad** (with big on-screen touch buttons) as well as
on any desktop browser. All graphics are drawn in code (original, "inspired-by" characters — no
copyrighted assets), and all sounds are generated with WebAudio, so there is nothing to download.

**`index.html` is the home page** — it lists every game in alphabetical order. To add a new game,
drop a new `.html` file in the folder and add one entry to the `GAMES` array in `index.html`.

## 🕹 The games

| Game | File | What it is |
|---|---|---|
| **Ohana Karts** | `ohana-karts.html` | Beach kart race: play Lilo or Stitch, dodge the villains, beat your rival to the finish |
| **Super Jumper** | `super-jumper.html` | 12-world platform adventure with friends, experiments and a golden medal |
| **Whack Hämsterviel** | `whack-hamsterviel.html` | Whack-a-mole: bonk Hämsterviel with your finger, spare the friends, beat the clock |

---

# 🏎 Ohana Karts

Pick **Lilo or Stitch** — the other becomes your rival — and race along a two-lane beach road in
Hawaii. Auto-accelerate; your only job is **switching lanes** to dodge trouble:

- 🦈 **Gantu** guards a lane and **fires plasma bolts** down the road (bolt or crash = kart damage).
- 🐹 **Hämsterviel** putters along as a rolling roadblock — stuck behind him you crawl at his pace.
- 🥪 **Reuben (625)** lobs sandwiches onto the road from his beach mat — drive into one and it's a
  sticky slowdown.
- ⚡ **Boost pads** give a burst of speed; the kart has **3 hearts**, and losing them all means a
  costly pit-repair stop while the race runs on.

Best time per character is saved on the device. Controls: **⬆⬇ buttons** (or tap the top/bottom
half of the road), keyboard **↑ ↓** or `W`/`S`; on the picker `1` = Stitch, `2` = Lilo.

---

# 🔨 Whack Hämsterviel

A classic whack-a-mole. **Hämsterviel** keeps popping out of burrows on the beach — **tap him on
the head** to bonk him for points (chain hits for a combo bonus). But friends pop up too — hit
**Stitch, Lilo or Angel** by mistake and you lose points *and* time. The game speeds up as the
**45-second** clock runs down. Best score is saved on the device. Just tap — no other controls.

---

# 🌺 Super Jumper

---

## 🚀 How to start the arcade

### Online — the easiest way

The arcade is published with **GitHub Pages**, so it is already live: open the repository's Pages
URL (**Settings → Pages** shows it) on any phone, tablet or computer — no setup, nothing to install.
Every push updates the live site automatically.

On iPhone or iPad, open that URL in Safari and tap **Share → Add to Home Screen**: the arcade then
launches full-screen, exactly like a native app.

### Locally, from the repository

```bash
cd ohana-arcade-games
python3 serve.py
```

Then open <http://localhost:8642> — the home page lists all the games. Press `Ctrl+C` to stop.

`serve.py` is a tiny wrapper around Python's built-in web server that adds **no-cache headers**, so
after any change a plain page reload always gets the newest version (no stale copies).

### Locally, on an iPhone / iPad on the same Wi-Fi

1. Start the local server on your computer (see above) and leave it running.
2. Find the computer's IP address (macOS: **System Settings → Wi-Fi → Details**), e.g. `192.168.1.23`.
3. On the iPad or iPhone, open Safari and go to `http://YOUR-IP:8642`.
4. Tap **Share → Add to Home Screen** for the full-screen app experience.

---

## 🎮 Controls (Super Jumper)

| Action | Touch (iPad/iPhone) | Keyboard |
|---|---|---|
| Run left / right | ◀ ▶ buttons | ← → or `A` / `D` |
| Jump (hold = higher) | ⬆ button | ↑, `Space`, or `W` |
| Fire the pistol | green ✦ button (appears once found) | `F` or `X` |
| Switch to the next world | small 🌍 button next to ▶ | `N` |
| Pause / resume | tap the screen | `P` |

Stitch fires in the direction he is facing. Jumps have hidden kid-friendly forgiveness
(coyote time + jump buffering).

---

## 🗺 The adventure — everything that was asked for

### The worlds (12 levels, five lands)

| Worlds | Scenery |
|---|---|
| 1 – 3 | **Hawaii** — volcanic mountains, green hills, palm trees with coconuts |
| 4 – 7 | **The beach** — ocean horizon with waves, sand dunes, beach umbrellas, sandy ground |
| 8 – 10 | **Alien planet** (Jumba's homeworld vibes) — purple night sky, stars, two moons, crystal spires |
| 11 | **Inside Lilo's house** — warm wooden walls, night windows with curtains, family photos, couch, lamp and bookshelf |
| 12 | **Lilo's school** — ALOHA chalkboards, sunny windows, desks with books — and **you play as Lilo!** |

Difficulty ramps up steadily: wider gaps, more villains, and armed enemies in the later worlds.
Levels also grow **longer**: +10% per level from World 4, +20% per level from World 7
(World 12 is 2.5× its base length).

Finish World 12 and the **Grand Councilwoman's ship lands** for the grand finale: she steps out
and awards Lilo & Stitch a **golden medal**. (Tap to skip the ceremony.)

### The heroes

- **Stitch-inspired blue alien** — big floppy ears, four arms once Lilo joins the team.
- **Lilo herself is the playable character in World 12**, red leaf dress, flower and all.
- 3 hearts (up to 5 with Nani), score, coins, and **Lilo & Stitch's house** waiting at the end
  of every world — reach it to finish the level.

### Power-ups

- 🥪 **Panini blocks** — bump the sandwich block and a walking panini pops out — or, half the
  time, an **ice cream cone** (same power, more points). Eating one makes Stitch **grow bigger**;
  while big, a hit only shrinks him back (no heart lost).
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
- 😤 **Mertle Edmonds** (Worlds 2, 4, 11 and 12) — Lilo's rival: she plants her feet and
  **screams**, and touching her puts you **to sleep for 10 seconds** (💤). She's just a kid, so
  she can't be stomped or shot — go around her.
- 💗 **From World 10, Gantu and Reuben turn good** — hearts overhead, no more shooting, and
  friendly Reuben's sandwich throws become **snacks that make you grow** (+100).
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
| `index.html` | The arcade home page — lists all games alphabetically (`GAMES` array). |
| `super-jumper.html` | The platformer — engine, levels, art, sound, UI. Edit levels in the `LEVELS` array (legend in the comments above it). |
| `ohana-karts.html` | The beach kart racing game. |
| `whack-hamsterviel.html` | The whack-a-mole game. |
| `serve.py` | Dev server with no-cache headers on port 8642. |
| `.claude/launch.json` | Preview-server config for Claude Code. |

Built with ❤️ by Claude Code for a young platforming fan and his ohana.
*Ohana means family — family means nobody gets left behind.*
