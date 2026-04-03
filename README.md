# undercover-game

**Undercover — Offline Word Party Game (Impostor + Mr. White)**

A beautiful, 100% offline pass-the-phone party game inspired by the popular **Undercover** word game.

Play with 3–12 friends on a single phone. No internet required after loading.

---

### Why This Version Exists

The official Undercover app on the Play Store has two major limitations in its free version:
- Frequent word repeats
- Limited number of word pairs
- Ads and in-app purchases

This project was built to solve those problems while keeping the original spirit of the game intact.

**What’s better here:**
- **350 carefully chosen hidden word pairs** (India-flavoured but universally known)
- Smart no-repeat deck system — you will never see the same pair again until all 350 have been used
- Completely free and 100% offline — no ads, no purchases, no internet needed
- Single self-contained HTML file (~69 KB) that works on any phone

The result is significantly higher replayability and a cleaner, more enjoyable experience.

---

### How to Play
- Most players are **Civilians** — all get the **same** secret word.
- One or more players are the **Impostor(s)** — each gets a **similar but different** word.
- Optionally, one player is **Mr. White** — gets **no word at all** and must bluff blindly.
- Describe your word cleverly (without saying it), discuss, then vote to eliminate suspects.
- If Mr. White is eliminated, they get one final chance to guess the civilians' word.

---

### Win Conditions
| Outcome                  | Condition |
|--------------------------|-----------|
| **Civilians Win**        | All Impostors eliminated, and Mr. White eliminated (if enabled) |
| **Impostor(s) Win**      | Impostor(s) outlast the civilians |
| **Mr. White Wins**       | Mr. White outlasts everyone or correctly guesses the word when caught |
| **Bad Guys Win**         | Impostors + Mr. White together outnumber remaining civilians |

---

### Key Features
- 350 hidden word pairs with smart no-repeat deck
- Premium dark UI with smooth animations
- Built-in discussion timer with 3-beep sound alert
- Mr. White final guess mechanic
- Single self-contained HTML file — works offline forever

---

### New in v2 (Major Improvements)

#### 1. Roles Hidden During Reveal
Players no longer see their exact role label.  
- Everyone sees only their word (or “— No Word —” for Mr. White).  
- Mr. White naturally figures out their identity.  
- Impostors and Civilians cannot tell who is who — pure bluffing.

#### 2. Flexible Setup Options
- **Mr. White Toggle** (default: ON) — can be turned off at any player count
- **Configurable Number of Impostors** (1 or more)
- Live role breakdown that updates instantly
- Smart ratio enforcement so bad guys never start with majority

#### 3. Improved Voting System
Three-phase voting (Individual → Review → Optional Change Vote) with mandatory tie resolution. No more random tiebreak — every elimination is a deliberate group decision.

#### 4. Better Replay Experience
- Player names persist across games (no need to re-type)
- Complete game state reset between rounds
- Stale callback protection so old game results never interfere with a new game

---

### Recommended Setup (for best experience)

| Total Players | Mr. White ON                  | Mr. White OFF              |
|---------------|-------------------------------|----------------------------|
| 3–6           | 1 Impostor                    | 1 Impostor                 |
| 7             | 1 Impostor                    | 1–2 Impostors              |
| 8–12          | 1–2 Impostors                 | 2 Impostors                |

---

### Play Now
▶️ **Live Demo:** [https://undercover-party-game.netlify.app](https://undercover-party-game.netlify.app)

You can also download the `undercover.html` file and play completely offline.

---

### Changelog

**v2.0**  
- Roles hidden during reveal  
- Mr. White toggle + configurable impostor count  
- Smart ratio enforcement + live role breakdown  
- Three-phase voting with mandatory tie resolution  
- Player names now persist across games  
- Full game state reset on new game  

**v1.0 (April 2026)**  
- Initial release with 350 hidden word pairs and classic Undercover rules

---

**Made with ❤️ by Jaiveer** (2nd Year)