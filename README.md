# Roblox-Luau

A single-file offline coding trainer that teaches Luau (the Roblox scripting language) through interactive lessons, quizzes, and hands-on Studio projects. Built for a 13-year-old learner. Works like Duolingo but for game development.

## What It Does

50 lessons across 10 units take the learner from `local health = 100` to DataStores, client-server architecture, and OOP with metatables. Every lesson opens with a Roblox game scenario, teaches the code pattern through that scenario, and connects to a real Roblox Studio build project.

**10 Units:** Basics, Logic, Loops, Functions, Tables, Roblox Objects, Events, UI Scripting, Client-Server, Data & Systems

**6 Labs:** Kill Brick Obby, Coin Collector, Item Shop, Tycoon Dropper, Custom HUD, Full Mini-Game

**10 Challenges:** Open-ended "What Would You Build?" prompts with model answers after each unit

## Features

- Three question types: multiple choice, fill-in-the-blank, and arrange-the-blocks (Parsons Problems)
- Teaching slides before every quiz with code examples and Roblox Studio context
- Hearts system (3 per lesson), XP tracking, daily streaks, and confetti on completion
- Review tab that resurfaces missed questions for spaced repetition practice
- Searchable reference glossary of every Luau concept
- Per-unit accuracy stats with visual breakdown
- Progress sync between devices via export code, JSON file backup, or both
- Spotify integration with custom playlist support
- Sound effects for correct, wrong, completion, and XP events
- Unit-colored theming (each unit paints the quiz in its own accent color)
- Fully responsive (phone, tablet, desktop)
- Modern Luau syntax: string interpolation, compound assignment, generalized iteration

## How to Use

1. Download `luau-trainer.html`
2. Open it in Chrome, Safari, Edge, or Firefox
3. Start at Lesson 1

No internet required for lessons (Spotify needs a connection). No account, no install, no dependencies. One HTML file, everything included.

## Tech

- Single-file vanilla JavaScript, zero external libraries
- Web Audio API for synthesized sound effects (no audio files)
- localStorage for progress persistence
- Base64 export/import for cross-device sync
- CSS custom properties for dynamic unit theming
- Spotify embed iframe with custom playlist URL support

## Content Accuracy

All 50 lessons verified against the Roblox Creator Hub documentation and Luau language specification. Covers current best practices including `task.wait()` (not deprecated `wait()`), generalized iteration (not `ipairs`), `typeof()` for Roblox types, and the create-configure-parent pattern for `Instance.new()`.

## Files

| File | Description |
|------|-------------|
| `luau-trainer.html` | The trainer application (single file, everything included) |
| `luau-trainer-guide.md` | User guide explaining every feature |
| `README.md` | This file |

## Background

Built by [Basil Puglisi](https://basilpuglisi.com) to teach his son Roblox scripting. The project started as a basic quiz app and evolved through 15 iterative versions with content rewrites, code audits, and user testing.

## License

MIT License. See [LICENSE](LICENSE) for details.

#AIassisted
