# Luau Trainer — User Guide

## What This Is

Luau Trainer is an app that teaches you the Roblox coding language (Luau) through quick interactive lessons. It works like Duolingo: answer questions, earn XP, keep your streak alive, and unlock new levels.

Every lesson starts with a Roblox game scenario, teaches the code pattern through that scenario, and connects to a real build project you can do in Roblox Studio.

50 lessons. 10 units. 6 build labs. 10 coding challenges. No account needed.

---

## Getting Started

1. Save the HTML file somewhere you can find it (Desktop, Downloads, Files app, Google Drive, wherever).
2. Open it in any browser (Chrome, Safari, Edge, Firefox).
3. That's it. The app loads and you're on the path map.

It works on your phone, tablet, or computer. No internet needed after you save the file (Spotify needs a connection, but everything else works offline). The app has no external dependencies and runs entirely from the single HTML file.

---

## The Path Map

When you open the app, you see a vertical path with colored circles. Each circle is one lesson.

- **Colored circle with a number** — ready to play. Tap it.
- **Gold star with a checkmark** — you already completed this one. You can replay it.
- **Gray circle with a lock** — not unlocked yet. Complete the lesson above it first.

Lessons unlock top to bottom. No skipping.

Between units you will see two other types of nodes:

- **💡 Challenge nodes** — open-ended coding prompts (gold border). Always accessible. Tap to try.
- **Lab nodes** — real Roblox Studio build projects (colored border with emoji). Always accessible. Tap to explore.

The top bar shows three items:

- 🔥 **Streak** — how many days in a row you've completed at least one lesson
- ⚡ **XP** — total experience points earned
- 🎵 **Music** — tap to open the Spotify player
- ⚙️ **Settings** — tap to open the sync panel

---

## Playing a Lesson

Each lesson starts with **teaching slides** that explain the concept, then follows with quiz questions. The app teaches first, then tests.

### Unit Colors

Each unit has its own color. When you enter a lesson, the progress bar, option borders, code accents, check button, and selection glow all change to match the current unit's color. Basics is green, Logic is blue, Loops is purple, Functions is orange, and so on. This makes each unit feel different as you progress.

### Teaching Slides

These show up with a colored "LEARN" badge. Every lesson opens with a Roblox game scenario that shows what the code concept makes happen in a real game. The slides then show the code pattern with an example. The last slide in each lesson tells you which lab project uses the skill you just learned.

Read the slide, then tap **Got it →** to continue. Teaching slides don't cost hearts and don't affect accuracy. They're just for learning.

### Quiz Questions

After the teaching slides, the quiz begins. You get **3 hearts** (❤️❤️❤️) per lesson.

### Question Types

**Multiple Choice** — Tap the right answer from 2 to 4 options. Each option has a colored left border matching the unit. Questions test real skills: predict what code outputs, find the bug, or pick the safer pattern.

**Fill in the Blank** — A code snippet has a blank. Type the missing piece. Most answers are case-insensitive (typing "local" or "LOCAL" both work). However, Roblox service names, class names, and API method names are case-sensitive because Roblox requires exact capitalization. For example, `"Players"` must be typed with a capital P, and `FindFirstChild` must match exactly. If the answer needs quotes (like `"Players"` for GetService), you must include them.

**Arrange the Blocks** — Tap code blocks in the correct order to build working code. Tap a block in your answer to remove it.

### How It Works

1. Answer the question.
2. Tap **Check**.
3. You'll see green (correct) or red (wrong) with an explanation.
4. Tap **Continue** to move on.

### Sound Effects

The app plays short sounds at key moments:

- **Correct answer** — ascending two-note chime
- **Wrong answer** — low descending tone
- **Lesson complete** — four-note fanfare
- **MC option tap** — quick tap sound
- **XP earned** — bright ascending triple ping

Sounds are synthesized in the browser. No audio files needed. If your device is muted, no sounds play.

### Hearts

- Wrong answer = lose a heart.
- Lose all 3 = lesson over. You'll see "Out of hearts!" and can try again.
- Complete the lesson with hearts left = success.

### XP

- **10 XP** per correct answer.
- **15 bonus XP** for a perfect lesson (no wrong answers).
- XP only counts the first time you complete a lesson. Replays earn 0 XP.

### Streak

Your streak goes up by 1 for every day you complete at least one lesson. Miss a day and it resets to 0. The streak tracks calendar days, so completing a lesson at 11 PM and another at 1 AM counts as two separate days.

---

## The 10 Units

| Unit | What You Learn |
|------|---------------|
| 1. Basics | Variables, print, compound assignment (+=), strings, string interpolation (backticks), comments, types |
| 2. Logic | If/else, elseif, and/or/not, comparisons, ~= operator |
| 3. Loops | For, while with task.wait(), break, continue, nested loops, compound operators (-=) |
| 4. Functions | Define, call, parameters, return, scope, anonymous functions |
| 5. Tables | Arrays (1-indexed), dictionaries, generalized iteration, insert/remove, nesting |
| 6. Roblox Objects | Services, GetService, Instance.new, FindFirstChild, properties, Destroy |
| 7. Events | Touched, PlayerAdded, Changed, GetPropertyChangedSignal, disconnect, kill brick pattern |
| 8. UI Scripting | ScreenGui, TextButtons, UDim2, AnchorPoint, health bars, TweenService |
| 9. Client-Server | RemoteEvents, FireServer, FireClient, FireAllClients, typeof validation, architecture |
| 10. Data & Systems | DataStores, ModuleScripts, pcall, OOP with metatables, task.wait, game loops |

---

## Modern Luau Features

The trainer teaches modern Luau syntax that matches what you'll see in current Roblox documentation and community code.

**String interpolation** — Instead of joining strings with `..`, you can use backtick strings with curly braces. Both work everywhere, but backticks are cleaner for longer messages. Taught in Unit 1.

```
-- Concatenation (still works)
local msg = playerName .. " found a " .. itemName

-- Interpolation (modern Luau)
local msg = `{playerName} found a {itemName}!`
```

**Compound assignment** — Instead of writing `coins = coins + 10`, you can write `coins += 10`. Works with all math operators: `+=`, `-=`, `*=`, `/=`. Taught in Unit 1, used throughout.

**Generalized iteration** — Instead of writing `for i, v in ipairs(table) do`, modern Luau lets you write `for i, v in table do` with no function call. Taught in Unit 5. Older code uses `ipairs` and `pairs`, which still work.

---

## Challenges (💡)

Challenges are "What Would You Build?" coding prompts. One appears after each unit on the path map, marked with a gold 💡 node.

### How They Work

1. Tap any challenge node on the path map.
2. Read the scenario (for example: "A treasure chest costs 50 coins to open. Write the code to check if the player can afford it.").
3. Write your code in the text area.
4. Tap **Show Answer** to reveal a model solution.
5. Compare your code to the model answer. No grading, just self-check.

Challenges are always open. You don't have to wait until you complete the unit. They're there whenever you want to practice writing real code.

---

## Labs (Studio Projects)

Labs are real build projects you do in Roblox Studio. They show up on the path map as rectangular buttons with an icon.

Labs appear on the path after the last unit they require skills from:

- 🧱 **Kill Brick Obby** and 🪙 **Coin Collector** — after Unit 7
- 🖥️ **Custom HUD** — after Unit 8
- 🏪 **Item Shop** and 🏭 **Tycoon Dropper** — after Unit 9
- 🎮 **Full Mini-Game** — after Unit 10

Labs are **always open**. You can tap into any lab from day one, even before you've done a single lesson. They're there as a preview of what you'll be able to build.

Each lab shows which units it uses skills from. As you complete units, the skill pills inside the lab turn green with a checkmark. When all the relevant units are done, the lab shows "READY," meaning you've covered everything you need. But you don't have to wait for that. Jump in whenever you're curious.

### The 6 Labs

| Lab | Skills From | What You Build |
|-----|------------|----------------|
| 🧱 Kill Brick Obby | Basics, Logic, Objects, Events | A short obstacle course with kill bricks |
| 🪙 Coin Collector | Basics, Logic, Loops, Objects, Events | Collectible coins with a scoring leaderboard |
| 🏪 Item Shop | Functions, Tables, Events, UI, Client-Server | A working shop GUI with server-validated purchases |
| 🏭 Tycoon Dropper | Loops, Functions, Objects, Events, Client-Server | A dropper that earns money with upgrades |
| 🖥️ Custom HUD | Functions, Objects, Events, UI | Health bar, coin counter, XP bar, notification popups |
| 🎮 Full Mini-Game | Everything | A complete round-based game with data saving |

### How Labs Work

1. Tap any lab button on the path map.
2. You'll see the project description and which units it draws skills from.
3. Tap a step to expand it and read the instructions.
4. Open Roblox Studio and do what the step says.
5. When you've done a step, tap the checkbox to mark it complete.
6. Progress saves just like lessons.

### The Skill Tracker

Inside each lab, you'll see a "Uses Skills From" section with unit pills. Each pill shows whether you've completed that unit:

- **○ Unit 3: Loops** — you haven't finished this unit yet
- **✓ Unit 3: Loops** — you've completed it, you know this material

If you open a lab and some skills are unchecked, the lab tells you which units to focus on. Every lesson's last teaching slide tells you exactly which lab uses the skill you just learned.

---

## Music (🎵)

Tap the 🎵 button in the top bar to open the music player.

### Default Playlist

A chill beats playlist loads automatically. Tap play inside the Spotify widget to start listening while you learn.

### Custom Playlist

1. Open Spotify (app or website).
2. Find a playlist you like.
3. Tap Share > Copy Link.
4. Paste the link into the URL field in the music panel.
5. Tap **Set**.

Your playlist saves automatically. Next time you open the music panel, your playlist loads instead of the default.

### Troubleshooting

The Spotify player needs internet and a real browser. If you see "Webpage not available," you're probably viewing the file inside an app preview (like the Claude app) instead of a browser. Save the file and open it in Chrome or Safari.

If the embedded player doesn't load, tap **"▶ Open in Spotify app"** below it to jump directly to the playlist in the Spotify app on your device.

---

## Saving Your Progress

Your progress saves automatically in the browser you're using. Close the tab, shut down your device, come back later — your progress is still there.

**But** the save is tied to that specific browser on that specific device. If you switch devices or browsers, your progress won't follow automatically. That's what the sync feature is for.

---

## Moving Progress Between Devices

Tap the **⚙️ gear icon** in the top right corner of the path map. The Sync Panel opens.

### Option 1: Progress Code (Easiest)

**To export from your current device:**

1. Tap ⚙️ to open the panel.
2. Your progress code appears in the Export box. It looks like a long string of random letters.
3. Tap **📋 Copy**.
4. Send it to yourself however you want: text message, email, notes app, paste it in a doc.

**To import on your other device:**

1. Open the Luau Trainer file in the browser on that device.
2. Tap ⚙️ to open the panel.
3. Paste the code into the Import box.
4. Tap **📥 Load**.
5. Confirm when asked. Done. The app merges the imported progress with whatever is already on this device. It keeps the higher XP, the longer streak, all completed lessons from both sides, and combines any lab progress (completed steps are never lost during merge). Nothing is overwritten.

### Option 2: File Backup

**To download a backup:**

1. Tap ⚙️.
2. Tap **⬇ Download**.
3. A file called **luau-trainer-progress.json** saves to your device.
4. Move it to your other device however you want (AirDrop, email, Google Drive, USB).

**To upload on another device:**

1. Tap ⚙️.
2. Tap **⬆ Upload**.
3. Pick the JSON file.
4. Confirm when asked. Progress merged, same rules as the code import.

### When to Sync

Sync is manual. The app does not auto-sync between devices. If you play on your phone and then want to continue on your computer, export from the phone first, then import on the computer. The import merges progress, so you won't lose anything even if the other device has newer data.

Good habit: export your code after every session so you always have a current backup.

---

## Resetting Progress

If you want to start over:

1. Tap ⚙️.
2. Tap **Reset All Progress** at the bottom.
3. Confirm.

This clears everything: XP, streak, all completed lessons, and lab progress. It cannot be undone.

---

## Tips

- **Go in order.** Later lessons assume you know everything from earlier ones.
- **Read the explanations.** Even when you get the answer right, the explanation teaches you why.
- **Try the challenges.** After each unit, the 💡 challenge lets you write real code and compare it to a model answer.
- **Do the labs.** Lessons teach the language. Labs are where you prove you can use it. Don't skip them.
- **Try both string styles.** When you see `..` concatenation, try rewriting it with backtick interpolation. Knowing both makes you faster.
- **Put on music.** Tap 🎵 and pick a playlist. Coding with background music helps focus.
- **Check your stats.** If a unit shows low accuracy, redo those lessons before moving on.
- **Use the reference.** Don't guess at syntax. Look it up, then type it from memory next time.
- **Review your mistakes.** The red dot means you have questions to practice. Clear it.
- **Don't rush.** Getting a lesson wrong and retrying teaches more than guessing your way through.

---

## Bottom Navigation

The bottom of the screen has four tabs:

| Tab | What It Does |
|-----|-------------|
| 🏠 **Learn** | The path map with lessons, challenges, and labs |
| 🔄 **Review** | Practice questions you got wrong |
| 📖 **Reference** | Searchable Luau cheat sheet |
| 📊 **Stats** | Your accuracy breakdown by unit |

---

## Reference (📖)

A searchable glossary of every Luau concept organized by category: Variables, Operators, Control Flow, Loops, Functions, Tables, Roblox Services, Instances, Events, UI, Client-Server, Data Patterns.

Each entry shows the term, the exact syntax, and a one-line explanation.

**How to use it:** Type a keyword in the search bar. It filters instantly. If you're mid-lab and forget how table.insert works, this is where you look.

---

## Review (🔄)

Every question you answer wrong in a lesson gets saved. The Review tab pulls from that list and quizzes you on your weak spots.

**How it works:**

1. Tap the 🔄 Review tab.
2. You'll get up to 10 questions drawn randomly from your mistakes.
3. Answer them the same way as a lesson (multiple choice, fill-in, arrange).
4. Get one right in review and it's removed from your mistake list.
5. Get it wrong again and it stays for next time.

Mistakes also clear if you answer them correctly when replaying a lesson. You don't have to use Review to fix them.

A red dot appears on the Review tab when you have questions waiting. Clear the dot by getting them all right.

If the review tab shows "Nothing to review," that means you've cleared all your mistakes. Nice.

---

## Stats (📊)

Shows you where you're strong and where you're not.

**What you'll see:**

- **Overall accuracy percentage** — your right vs wrong across all lessons
- **Lessons completed, total XP, and streak** — the volume stats
- **Accuracy by unit** — a bar for each of the 10 units showing your percentage. Green (80%+) means solid. Yellow (50-79%) means shaky. Red (below 50%) means go back and redo those lessons.

Accuracy counts every attempt, including replays. If you replay a lesson and get more answers right, your accuracy goes up. This means accuracy reflects how well you know the material right now, not just how you did the first time.

- **Questions to review** — the specific questions you've missed, showing which unit and lesson they came from

Use this to decide what to work on next. If your Events accuracy is 45%, that's where your time should go before moving to Client-Server.
