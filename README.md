# exp33
Completionist tracker for Exp33 fans

Track your 100% run through Clair Obscur: Expedition 33.

## 🎨 Expedition 33 Completionist Checklist

A single self-contained HTML tracker for a **full 100% run** of *Clair Obscur: Expedition 33* — every boss, collectible, and missable, organized the way you actually play. Four synced views: an in-order **Walkthrough** (every location Prologue → endgame, each item sequenced as you'll pass it), a **Dashboard** of category cards, a sortable **Spreadsheet**, and a printable **Missables Cheat Sheet**. Tick something in one view and it updates everywhere, including the overall progress bar. Built for a game with **no in-game map**, so every boss comes with turn-by-turn directions from in-world landmarks.

Built in an afternoon with Cowork in the Claude desktop app — and you can build your own in a few minutes with the prompt below.

## Try it

Download `expedition33_completionist_checklist.html` and double-click it — it opens in any browser, no install, no internet needed. Your progress saves automatically in that browser.

The shared file ships **empty** — it's a tracker, not a snapshot. Each person fills in their own run, and progress is stored locally per browser (it won't sync between devices or people). Nothing ever resets or "repopulates," so revisiting a location keeps your counts.

## Build your own (copy-paste into Cowork)

Open the Claude desktop app and start a Cowork session. Edit the **CUSTOMIZE ME** block (the game and how you want spoilers handled). Paste the prompt below and send it. Answer the clarifying questions, then let it research and build (a few minutes). Ask it for the standalone `.html` to share.

Requires the Claude desktop app with Cowork enabled (it needs web search + the ability to create files). It won't fully work from the plain web chat.

### The prompt

Build me a completionist checklist for a video game as a single self-contained HTML tracker — a tool I can use to track my 100% run and share with others.

```
=== CUSTOMIZE ME ===
Game: Clair Obscur: Expedition 33
Scope: full 100% — every boss, all collectibles, all missables
Spoilers: full spoilers OK (I've finished a run)
Difficulty tags: tag each boss with BOTH combat difficulty AND missability
====================
```

CLARIFY FIRST: before building, ask me (multiple-choice where possible) about format, scope, spoiler handling, and what "difficulty" should mean — unless I've already answered in CUSTOMIZE ME.

RESEARCH FIRST (don't trust memory — verify everything):
- Cross-check every count across at least two of: PowerPyx, Game8, Fextralife, game-checklists.com, IGN, GameRant, PSNProfiles/PushSquare. Note the game's latest patch.
- Bosses: every fightable boss (main story, optional/world, chromatic/field, postgame superbosses, and any DLC/patch additions). For each: location, act/phase, combat difficulty (Easy/Medium/Hard/Very Hard/Extreme), and whether it's missable.
- Collectible totals: journals, records, pictos, weapons, monoco skills, gestrals, gestral games, nevron quests, relationship interactions — record the trophy totals and any DLC deltas.
- Missables: every item permanently lost after a point of no return, with the exact trigger.
- In-visit-order manifest: for each region in the order you reach it, the ordered list of collectibles. Where a guide documents item-level order, keep it; where it only gives a count, record the count — do NOT invent an order or names you can't source.
- Navigation (this game has no map): turn-by-turn "how to reach it" directions per boss using campfires/landmarks, plus a one-line orientation note per region and an overworld traversal model.
Flag every place sources conflict or data is thin — those flags go into the tool.

BUILD — one self-contained HTML file, no dependencies, works offline, progress saved in localStorage. Four toggle views over one shared saved state:
1. Walkthrough (in order) — the primary view. Every location Prologue → endgame in visit order; within each, every item sequenced as encountered. Named items are checkboxes; groups a guide gives only as a count (e.g. "region Pictos ×12") are +/- counters. Counters persist across revisits and never reset. Each location header shows its Act, the traversal gate to reach it (Swim/Fly/Dive/Optional), and a live x/y count. Expand-all / collapse-all.
2. Dashboard — category cards (bosses with difficulty + find-it directions, missables, collectible totals). The collectible totals here AUTO-FILL from the Walkthrough (read-only, with a jump button).
3. Spreadsheet — the same data as a sortable table (click headers to sort) with a "how to find it" column; checkboxes and counters editable inline.
4. Missables Cheat Sheet — printable, grouped by Act, with a Print/Save-as-PDF button and point-of-no-return reminders. Include an @media print stylesheet.

CROSS-VIEW SYNC (important): bosses and missables are the same record shown in multiple views — ticking one updates all. Collectibles roll up: map each collectible type to a game-total counter and sum every Walkthrough item into the Dashboard totals + overall bar, live. Because the Walkthrough can't itemize all ~500 pickups, add a final "Uncatalogued — cleanup" location holding the remainder per type, sized so itemized + remainder = the true game total. Verify the sums hit each real total at 100%.

LOOK & FEEL: dark, game-appropriate palette; difficulty and missability as colored badges; directions in a callout style; honest inline flags for contested/thin data. Works on desktop and phone. Single self-contained HTML file (inline all CSS/JS) so it opens by double-clicking.

HONESTY RULES (carry into the artifact): never fabricate a boss, count, or location. Mark DLC/patch content explicitly. Where a boss roster or item order is uncertain, label it in the row ("verify in-game", "sources disagree") rather than faking precision. If a location's directions can't be verified, say "no verified path — see video guide" instead of inventing steps.

AFTER BUILDING: hand me the standalone .html file to share. Verify before finishing — via a scratch script, confirm the data parses, no duplicate IDs, every boss reference resolves, the engine JS parses, and at simulated 100% every rolled-up collectible type equals its real game total.

## Customizing further (just ask Cowork after it builds)

- "Split the single 'Remaining Pictos' bucket into per-region Picto counters."
- "Add a per-character weapon breakdown."
- "Add a 'hide completed locations' toggle to the Walkthrough."
- "Walk me through Act-by-Act reconciling what I've already done."
- "Adapt this whole thing for [another game]." (swap the source list + rollup map; the rest is game-agnostic)

## Honest caveats

- **Progress is per-browser and local.** The shared `.html` ships empty; your ticks don't sync between devices or people. Re-share the blank file for someone else to start their own.
- **A few data points are genuinely contested** and are flagged inside the tool: the full Chromatic field-boss roster varies by source, the total weapon count blends base + patch content (~104 base / ~117 with the 1.5.0 "Thank You" update), and a couple of interior paths (Ancient Sanctuary's maze, Grosse Tête's exact overworld spot) couldn't be verified — those say so rather than guess.
- **Full spoilers.** Postgame regions and superbosses are named directly.
- Data current as of Patch 1.5.0 — re-run the research step to refresh after a major update.

Made with Cowork in the Claude desktop app. Swap in your own game and run it for your own 100% run.
