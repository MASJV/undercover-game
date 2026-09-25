# Undercover — Offline Word Party Game

A beautiful, fully offline single-phone party game inspired by the popular social deduction game **Undercover**.

Play with **3–12 players** on a single phone. No accounts, no setup, no internet, no ads.

**[▶ Play now in your browser](https://undercover-party-game.netlify.app)** — the web version is the latest build.

Available as:

* a web version — a single self-contained HTML file (latest)
* a native Android application (v5.1)

---

# Why This Project Exists

Most existing Undercover-style apps suffer from the same problems:

* repetitive word decks
* aggressive ads and subscriptions
* weak offline support
* poor replayability
* unnecessary friction for casual play

This project solves each of them:

| Problem                  | Solution                                                    |
| ------------------------ | ----------------------------------------------------------- |
| Repetitive word decks    | 880+ curated pairs with no-repeat deck cycling              |
| Ads and subscriptions    | None, ever                                                  |
| Weak offline support     | Runs fully offline from a single file or the APK            |
| Poor replayability       | Seven categories, Mr. White role, deck progress that persists across sessions |
| Friction for casual play | No accounts or multiplayer setup — one phone, pass and play |

---

# How It Was Built

The product decisions are mine: the problem, the game rules, the UX flow, the replayability system, and what to cut. Implementation was AI-assisted using LLM tooling, which let me iterate fast — v2.0 onward was shaped directly by playtest feedback.

## What Playtesting Changed

Watching real groups play led to these changes in v2.0 and later:

* **Roles hidden during reveal** — the reveal card is neutral, so nobody learns their role from the screen; it's pure bluffing
* **Mr. White made optional** — a toggle (default on) that works at any player count
* **Configurable Impostor count** — with a live recommendation and role breakdown during setup
* **Balance guardrails** — a warning when the bad guys are set up too strong for the group size
* **No random tiebreaks** — three-phase voting with mandatory tie resolution, so eliminations are always decided by players
* **Faster rematches** — player names carry over between games, with a full state reset so nothing leaks from the last round
* **Edge-case fixes** — duplicate player names and empty Mr. White guesses are now blocked

---

# Core Features

## 🎮 Fully Offline

* No internet required for the APK after installation.
* No backend
* No analytics
* No ads
* No tracking
* The web version is a single HTML file with the word bank embedded — download it once and it works offline.

---

## 🔁 Massive Replayability

* 880+ curated word pairs across seven categories
* Smart no-repeat deck cycling system
* Word pairs do not repeat until the entire deck is exhausted
* Deck progress is saved, so reloading or coming back later doesn't reset it
* Short hints under each word so players can place unfamiliar terms

---

## 📱 Single-Phone Pass-and-Play

Designed specifically for:

* parties
* road trips
* classrooms
* casual hangouts
* offline social play

No accounts or multiplayer setup required.

---

## 🕵️ Mr. White System

Supports the classic:

* Civilian
* Impostor
* Mr. White

social deduction gameplay loop.

Mr. White receives no word and must dynamically infer the secret topic through player clues.

---

## 🗳️ Tie-Protected Voting

Includes:

* hidden voting flow
* enforced tie-break rounds
* elimination locking
* clean endgame handling

---

## ⚡ Lightweight Distribution

The entire web version exists as:

* one standalone HTML file
* self-contained gameplay logic and embedded word bank

Portable enough to:

* AirDrop
* share over WhatsApp
* keep permanently offline
* run on nearly any browser

---

# How to Play

## 1. Pass the Phone

Each player secretly reveals their role and word.

* 🟢 Civilians receive the same word
* 🟠 Impostors receive a very similar but different word
* ⚪ Mr. White receives no word

Example:

* Civilian: "Samosa"
* Impostor: "Kachori"

---

## 2. Describe Your Word

Players go around the circle giving:

* one-word
* or two-word

clues about their secret word.

Rules:

* you cannot say the word itself
* clues must remain subtle enough to avoid exposure

Mr. White must improvise and blend in using context clues alone.

---

## 3. Vote Secretly

Players pass the device and cast votes privately.

The game:

* tracks votes
* prevents unresolved ties
* forces tie-break discussion rounds when necessary

---

## 4. Final Guess Opportunity

If Mr. White is eliminated:

* they get one final chance
* to type the civilians' real word

If guessed correctly:

* Mr. White steals the victory.

---

# Win Conditions

| Outcome        | Condition                                            |
| -------------- | ---------------------------------------------------- |
| Civilians Win  | All Impostors and Mr. White are eliminated           |
| Bad Guys Win   | Impostors + Mr. White equal or outnumber civilians   |
| Mr. White Wins | Eliminated Mr. White correctly guesses the civilians' word |

---

# Categories

## 🇮🇳 Desi Blend

Indian food, Bollywood references, landmarks, sweets, cities, and pop culture.

## 🇺🇸 American Culture

Fast food, sports, brands, landmarks, and Americana.

## 🏛️ World Landmarks

Historical monuments and global tourist locations.

## 🌎 Nations

Countries, territories, and geopolitical contrasts.

## 🗺️ Places & Spaces

Everyday environments, destinations, and scenarios.

## 🎬 Movies & Tech

Films, operating systems, gadgets, and modern apps.

## 🎭 Actors & Characters

Marvel & DC heroes, Hollywood stars, and movie icons.

---

# Technical Highlights

* Offline-first architecture
* Single-file HTML build with an embedded word bank; `words.json` is the editable source and is loaded instead when placed alongside
* Deck progress and game history persist across reloads (localStorage)
* Back-button guard confirms before leaving a game in progress
* Responsive mobile-first UI
* Material 3 inspired dark theme
* Structured multi-phase gameplay flow
* Non-repeating deck cycling system

---

# Recommended Setup

| Players | Mr. White | Impostors |
| ------- | --------- | --------- |
| 3–6     | ON        | 1         |
| 7       | ON/OFF    | 1–2       |
| 8–12    | ON        | 2         |

---

# Play

## 🌐 Web Version (Recommended)

https://undercover-party-game.netlify.app

Instantly playable in any modern browser, including iOS and desktop. This is the latest build and has every feature listed above.

---

## 💾 Offline HTML

1. Download `undercover.html`.
2. Open it in any modern browser — no internet needed.

---

## 📲 Android APK

[Download APK (v5.1)](https://github.com/MASJV/undercover-game/releases/latest)

Fully offline after installation. The APK is behind the web version — it doesn't yet include the newest features (seventh category, word hints, saved deck progress).

---

# Development Notes

Built during 2nd year summer break as a product-focused side project.

---

# Changelog

## Web (latest)

* Added Actors & Characters category (seven categories total)
* Expanded to 880+ word pairs
* Added short hints under each word
* Deck progress now persists across reloads
* Word bank embedded in the HTML, so the web version runs as a single file

## v5.1

* Added session persistence to survive reloads and accidental exits
* Open-source word bank (JSON + contributions)
* Random starter selection in discussion phase
* Tie-break logic refinement

## v5.0

* Synced Android + HTML feature parity
* Added six-category deck system
* Expanded to hundreds of curated word pairs across six categories
* Added responsive category grid
* Improved player flow visibility during pass-and-play sessions

## v2.0 – v4.0

* Added multi-phase voting
* Added tie-lock enforcement
* Added Mr. White guessing system
* Expanded Indian-flavored deck library

---

Built with curiosity, iteration, product obsession, and modern AI-assisted development.