# undercover-game

**Undercover — Offline Word Party Game (Impostor + Mr. White)**

A beautiful, 100% offline pass-the-phone party game inspired by the popular **Undercover** word game.

Play with 3–12 friends on a single phone. No internet required after loading.

---

### How to Play
- Most players are **Civilians** — all get the **same** secret word.
- One or more players are the **Impostor(s)** — each gets a **similar but different** word.
- Optionally, one player is **Mr. White** — gets **no word at all** and must bluff blindly.
- Describe your word cleverly (without saying it), discuss, then vote to eliminate suspects.
- If Mr. White is eliminated, they get one final chance to guess the civilians' word.

---

### Win Conditions
| Outcome | Condition |
|---|---|
| **Civilians Win** | All Impostors eliminated, and Mr. White eliminated (if enabled) |
| **Impostor(s) Win** | Impostor(s) outlast civilians (bad guys ≥ civilians remaining) |
| **Mr. White Wins (survival)** | Mr. White outlasts all civilians with Impostors also gone |
| **Mr. White Wins (guess)** | Mr. White is caught but correctly guesses the civilians' word |
| **Bad Guys Win** | Mr. White + Impostor(s) together outlast civilians |

---

### Key Features
- **350 India-flavoured hidden word pairs** — smart, non-obvious, universally known
- Smart no-repeat deck system (all 350 used before any repeat)
- Premium dark UI with smooth animations
- Built-in discussion timer with 3-beep sound alert
- Three-phase voting with submit confirmation and change-vote support
- Mr. White final guess mechanic (case-insensitive, only when Mr. White is enabled)
- Single self-contained HTML file — no install, no internet

---

### New in v2

#### 1. Roles Hidden During Reveal
Players no longer see their role label (Civilian / Impostor / Mr. White) on the reveal card.
- **Civilians** see: *"Your word is: [WORD]"*
- **Impostors** see: *"Your word is: [WORD]"* — identical card, different word
- **Mr. White** sees: *"— No Word —"* — they naturally know without being told

All cards use the same neutral dark design. No card style or label gives away who is who.

Tip shown to everyone: *"Describe your word in 1–2 words without saying it directly. Be careful — not everyone at the table may have the same word!"*

---

#### 2. Mr. White Toggle (Default: ON)
A toggle on the Setup screen lets the host include or exclude Mr. White from the game.
- **ON** (default): 1 Mr. White + Impostors + Civilians
- **OFF**: Impostors + Civilians only (classic Undercover mode)
- Toggle is available at **all player counts** — even 3 players can include Mr. White

---

#### 3. Configurable Number of Impostors
A stepper (+/−) on the Setup screen lets the host choose how many Impostors to include.
- Minimum: **1 Impostor** (always)
- Maximum: enforced by ratio rule (see below)
- A **"Recommended: X"** hint updates live based on player count and Mr. White toggle

---

#### 4. Smart Ratio Enforcement
The game prevents Impostors + Mr. White from equalling or outnumbering Civilians at game start.

Max impostors formula: `floor((N − 2×MW − 1) / 2)`, minimum 1

Recommended impostor counts by player count:

| Total Players | Mr. White ON | Mr. White OFF |
|---|---|---|
| 3 | 1 Impostor (1 Civ) | 1 Impostor (2 Civ) |
| 4 | 1 Impostor (2 Civ) | 1 Impostor (3 Civ) |
| 5 | **1 Impostor (3 Civ)** | 1 Impostor (4 Civ) |
| 6 | **1 Impostor (4 Civ)** | 1 Impostor (5 Civ) |
| 7 | 1 Impostor (5 Civ) | 1–2 Impostors |
| 8 | 1–2 Impostors | **2 Impostors (6 Civ)** |
| 9 | **2 Impostors (6 Civ)** | 2 Impostors (7 Civ) |
| 10 | **2 Impostors (7 Civ)** | 2 Impostors (8 Civ) |
| 11 | 2 Impostors (8 Civ) | 2 Impostors (9 Civ) |
| 12 | **2 Impostors (9 Civ)** | 2 Impostors (10 Civ) |

When the host changes the player count, the impostor count auto-resets to the recommended value.

A **ratio warning** appears when the selected configuration puts bad guys at or above civilian count.

---

#### 5. Live Role Breakdown
The setup screen shows a live pill-badge breakdown of roles as settings are adjusted:
> 🟢 4 Civilians · 🟠 1 Impostor · ⚪ 1 Mr. White

---

#### 6. Redesigned Voting System
The old tie-prevention voting has been replaced with a three-phase system:

**Phase 1 — Individual Voting (pass-the-phone)**
- The phone is passed to each player in turn.
- Each player privately picks their target and taps **Confirm Vote**.
- No votes are revealed during this phase — nobody sees anyone else's choice.
- Any player can vote for any other alive player — no restrictions.

**Phase 2 — Review**
- Once every player has voted, a review screen appears: *"All players have voted!"*
- Two options are shown:
  - **Change a Vote** — opens the change-vote screen (see Phase 3).
  - **Submit & Reveal Results** — runs tie detection before finalising.
- Votes are not revealed until Submit is pressed.

**Tie Detection on Submit (Mandatory Resolution)**
- When Submit is tapped, the game checks for a tie at the top of the vote count.
- If a tie is found, **submission is locked** — the game cannot proceed until the tie is broken.
- A warning panel appears showing each tied player's name and exact vote count.
- The only option is **Change a Vote** — there is no random tiebreak escape hatch.
- Rationale: every elimination must be a deliberate group decision. A random tiebreak is unpredictable and can feel deeply unfair, especially late in the game when stakes are high.
- After changing a vote and returning to review, the Submit button is restored and a fresh tie check runs on the next tap.

**Phase 3 — Change a Vote (optional)**
- Tapping "Change a Vote" shows a list of all voters by name.
- Any player can tap their own name to re-cast their vote privately.
- After confirming the new vote, the review screen returns automatically.
- Multiple players can change votes in sequence before submitting.

---

#### 7. Play Again — Name Persistence & Clean State

**Player names persist across games.**
When the end screen appears and a player taps "Play Again", their names are saved internally. On the setup screen for the next game, all name fields are pre-filled exactly as they were — no re-typing needed. The player count is also restored to match the previous game.

**All game data is wiped between games.**
The following are completely cleared before each new game begins:

| Reset field | Why it matters |
|---|---|
| Roles (`isMW`, `isImpostor`) | Prevents old role assignments bleeding into the new game |
| Alive list | Starts fresh with all players alive |
| Votes & vote queue | No carry-over from previous round |
| Round counter | Always starts at Round 1 |
| Timer state | Discussion timer is reset and stopped |
| Pair (word set) | New word pair drawn for each game |

**Stale callback guard (game session ID).**
Every delayed end-game call (the 1.6 s reveal pause after an elimination) is tagged with the current game's ID. If a new game starts before a tagged callback fires — which can happen if players move quickly — the callback detects the mismatch and silently discards itself. This prevents a previous game's result screen from appearing mid-way through a new game.

---

#### 8. Updated Win Conditions (Multi-Impostor)
- If Mr. White is **OFF**: Civilians win when all Impostors are eliminated.
- If Mr. White is **ON**: Civilians win only when both all Impostors and Mr. White are eliminated.
- Mr. White final guess mechanic only appears when Mr. White is enabled.
- End-game banner correctly identifies which bad guys survived (solo Impostor, solo Mr. White, or both together).

---

### Changelog

**v3.0 (pending)**
- Mandatory tie resolution — submission locked until tie is broken; no random tiebreak option
- Every elimination is now guaranteed to be a deliberate group decision
- Player names now persist across games — pre-filled automatically when starting a new game
- Full game state reset on new game: all roles, alive list, votes, round counter, and timer wiped clean; only names are carried over
- Game session ID guard on all delayed end-game callbacks — stale timeouts from a previous game can no longer fire during a new game

**v2.0 (pending)**
- Roles hidden from players during reveal (neutral card for all)
- Mr. White toggle (default ON, available at all player counts)
- Configurable impostor count with live "Recommended: X" hint
- Smart ratio enforcement with max-impostors formula and ratio warning
- Auto-reset impostor count to recommended when player count changes
- Live role breakdown pill badges on setup screen
- Three-phase voting: individual → review → optional change-vote (no tie-prevention logic)
- Tie detection on submit with warning panel showing tied players and vote counts
- Updated win conditions for multi-impostor and optional Mr. White
- Unified reveal tip text so no player can infer their role from the message

**v1.0 (April 2026)**
- Initial release
- Full Undercover rules (Impostor + Mr. White)
- 350 India-flavoured hidden word pairs + private pass-the-phone reveals
- Discussion timer + smart voting + tie prevention

---

### Play Now
▶️ **Live Demo:** [https://undercover-party-game.netlify.app](https://undercover-party-game.netlify.app)

You can also download the `undercover.html` file and play completely offline.

---

**Made with ❤️ by Jaiveer** (2nd Year)
