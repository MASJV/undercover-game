# Undercover — Offline Word Party Game

A beautiful, fully offline single-phone party game inspired by the popular social deduction game **Undercover**.

Play with **3–12 players** on a single phone. No accounts, no setup, no internet, no ads.

Built as both:

* a native Android application
* and a single self-contained HTML file (~90 KB) that runs offline in modern browsers

---

# Why This Project Exists

Most existing Undercover-style apps suffer from the same problems:

* repetitive word decks
* aggressive ads and subscriptions
* weak offline support
* poor replayability
* unnecessary friction for casual play

This project was built to solve those problems directly.

The goal was not to build an unnecessarily complex application.

The focus was:

* identifying real friction in an existing product category
* simplifying the experience
* maximizing replayability
* creating something portable, fast, and permanently usable offline

This project is intentionally product-driven rather than technology-driven.

---

# Product Thinking & AI-Assisted Development

This repository is also an experiment in modern AI-assisted product development.

A large portion of the implementation was AI-assisted using modern LLM tooling and rapid prototyping workflows. The goal of the project was never to prove low-level manual coding difficulty.

The goal was to demonstrate:

* product thinking
* problem solving
* gameplay system design
* UX prioritization
* feature scoping
* rapid iteration
* shipping ability
* practical AI-assisted development workflows

The important part was not:

> “Can every line be handwritten manually?”

The important part was:

> “Can a frustrating user experience be identified and transformed into a polished, usable product?”

This project represents that philosophy.

While implementation was AI-assisted, the product architecture, gameplay systems, UX decisions, feature design, replayability logic, and overall direction were human-designed and iteratively refined.

---

# Core Features

## 🎮 Fully Offline

* No internet required
* No backend
* No analytics
* No ads
* No tracking
* Works completely offline after download

---

## 🔁 Massive Replayability

* Hundreds of curated word pairs across six categories
* Smart no-repeat deck cycling system
* Word pairs do not repeat until the entire deck is exhausted

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
* ~90 KB total size
* self-contained gameplay logic and embedded assets

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
| Impostors Win  | Impostors outlast civilians                          |
| Mr. White Wins | Survives until the end or correctly guesses the word |
| Bad Guys Win   | Impostors + Mr. White equal or outnumber civilians   |

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

---

# Technical Highlights

* Offline-first architecture
* Single-file deployment design
* Persistent local player storage
* Responsive mobile-first UI
* Material 3 inspired dark theme
* Embedded Web Audio API tone system
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

## 🌐 Live Demo

https://undercover-party-game.netlify.app

Instantly playable in browser.

---

## 📲 Android APK

[Download Latest APK](https://github.com/MASJV/undercover-game/releases/latest)

Fully offline after installation.

---

## 💾 Standalone HTML Version

The project also includes a self-contained offline HTML build for portability and archival purposes.

---

# Development Notes

Built during 2nd year summer break as a product-focused side project.

This repository intentionally emphasizes:

* solving a real usability problem
* creating a polished user experience
* fast iteration and experimentation
* practical AI-assisted workflows
* shipping usable software quickly

over:

* framework complexity
* resume-driven engineering
* artificial technical overengineering

The project was developed using a modern AI-assisted workflow where implementation speed was prioritized, while architecture decisions, gameplay systems, UX flow, replayability mechanics, and product direction were continuously refined manually.

---

# Changelog

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