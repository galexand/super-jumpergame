# 📚 References & design rules

This file records **where the characters and scenes came from** and the **rules that must be
followed** when adding new content. Gameplay, controls and setup live in [README.md](README.md) —
they are not repeated here.

---

## ⚖️ The one rule that matters

Every character, background and object in these games is **drawn from scratch in code** (Canvas 2D)
as an original "inspired-by" design. The links below were used **only as visual inspiration** —
no artwork, sprite or photo from them is copied, embedded or redistributed.

**When adding a new character or scene, keep it that way**: look at a reference, then draw an
original interpretation in code. Never embed or link a copyrighted image file.

---

## 🧑‍🎤 Character references

Full cast lists used to pick characters and their traits:

- Lilo & Stitch Wiki — character category: <https://liloandstitch.fandom.com/wiki/Category:Characters>
- Wikipedia — list of characters: <https://en.wikipedia.org/wiki/List_of_Lilo_%26_Stitch_characters>

Specific references that were given for individual characters:

| Character | In the games | Reference |
|---|---|---|
| **Stitch** | Hero of Super Jumper; playable in Ohana Karts | <https://en.wikipedia.org/wiki/Stitch_(Lilo_%26_Stitch)#/media/File:Stitch_(Lilo_&_Stitch).svg> |
| **Gantu** | Bruiser villain (turns good from World 10); kart racer villain | <https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSrHEvkKvj95L_QYb7lLBD3XVU_OD47YgefYnuj5MtxnAFt9xwm2v7hLFjVOy3PDvnKhyE0FN7Xa3q8S7HKlnA8BGUfEBZPkLHExDsgky1COw&s=10> |
| **Hämsterviel** | Hamster villain; the star of Whack Hämsterviel | <https://static.wikia.nocookie.net/disney/images/7/7e/H%C3%A4msterviel.png/revision/latest?cb=20130813090948&path-prefix=es> |
| **Reuben (X-625)** | Sandwich thrower (turns good from World 10) | <https://en.wikipedia.org/wiki/List_of_Lilo_%26_Stitch_characters#Reuben_(X-625)> |
| **Mertle Edmonds** | Screamer — touching her means a 10-second nap | <https://liloandstitch.fandom.com/wiki/Mertle_Edmonds> |
| **Grand Councilwoman** | Lands her ship and awards the golden medal after World 12 | <https://liloandstitch.fandom.com/wiki/Grand_Councilwoman> |

Characters taken from the cast lists above without a specific link: **Lilo, Nani, David, Pleakley,
Jumba, Angel, Leroy**, and the experiments **Babyfier (151), Amnesio (303), Sample (258),
Fibber (032)**.

---

## 🏝 Scene references

| Scene | In the games | Reference |
|---|---|---|
| **Lilo & Stitch's house** — the goal at the end of every world (replaced the flag) | Super Jumper | User-attached painting of the blue house on stilts with the red roof and dome turret (no URL) |
| **Inside the house** — World 11 backdrop | Super Jumper | [Google Images: "stitch and lilo house pictures on the inside"](https://www.google.com/search?udm=2&q=stitch+and+lilo+house+pictures+on+the+inside) |

---

## 🔧 Technical notes not covered in the README

- **Saved data** (browser `localStorage`, per device):
  - `superJumperScores` — top-10 list of `{name, score, coins, world}`
  - `superJumperName` — last name typed, pre-filled next time
  - `whackHamBest` — best whack-a-mole score
  - Ohana Karts stores a best lap time per character
- **Adding a game**: drop a new single-file `<game>.html` in this folder and add one entry to the
  `GAMES` array in `index.html`; the home page sorts the list alphabetically by itself.
- **Every game must work with both touch and keyboard**, and be safe for a young player:
  forgiving physics, no dead ends, and nothing that can permanently break a run.
