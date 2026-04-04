# SWEEPER | Minesweeper with teeth

Arcade-pressure minesweeper. Five depths, countdown timers, artifacts, procedural audio. Dark terminal aesthetic inspired by Inscryption.

## Quick Start

Open `index.html` in any browser. No install, no server, no dependencies.

Or host it anywhere that serves static files (GitHub Pages, Netlify, etc).

## What It Does

You descend through 5 depths where the grid grows, mines multiply, and time shrinks. Hit a skull or run out of time and you're back to Depth 1.

| Depth | Grid | Mines | Time |
|-------|------|-------|------|
| 1 | 8x8 | 10 | 2:30 |
| 2 | 10x10 | 15 | 2:20 |
| 3 | 12x12 | 25 | 2:10 |
| 4 | 14x14 | 35 | 2:00 |
| 5 | 16x16 | 50 | 1:50 |

Half of your remaining time carries into the next depth.

### Shop

Earn shards by revealing tiles (1 per tile) and clearing depths (bonus). Between depths, spend shards in the shop:

- **The Eye** -- reveals one safe tile
- **Hourglass** -- reclaims 20 seconds
- **The Ward** -- absorbs one mine hit
- **The Compass** -- auto-stakes 3 buried mines
- **The Oracle** -- reveals a 3x3 safe region
- **Rewind** -- restart current depth with a fresh board, keep your remaining time
- **The Crown** -- claims 500 points

Cursed artifacts appear rarely (~30% chance). Cheap, but at a cost:

- **The Leech** -- reveals 5 safe tiles but devours 25 seconds
- **Blood Tithe** -- auto-stakes 5 mines but your next hit ignores the Ward
- **The Bargain** -- +45 seconds but sacrifices half your score

Artifacts carry between levels. Click their badge during gameplay to activate.

### Controls

- **Left-click** -- reveal a tile
- **Right-click** (or long-press on mobile) -- place a stake (flag)
- **Artifact badges** -- click to activate during gameplay

### Shards

Shards are the only currency. Earn them, spend them in the shop.

- 1 shard per revealed tile
- Combo bonus for rapid reveals (2+ in a row)
- Depth bonus on clear (10 x depth)
- Time bonus on clear (1 per 5 seconds remaining)

## Tech Stack

| Layer | Tools |
|-------|-------|
| Game | Single-file HTML/CSS/JS |
| Fonts | Space Grotesk, JetBrains Mono (Google Fonts) |
| Audio | Web Audio API (procedural, no files) |
| Save | localStorage |
| Visual | CRT scanlines, particle dust, drifting orbs, SVG icons |

## Project Structure

```
index.html          # the entire game (HTML + CSS + JS)
DESIGN.md           # full design system (colors, fonts, spacing, motion)
src/                # original Java 17 / Swing desktop version
  main/java/        #   game model, board, cell, save/load
  test/java/        #   tests
pom.xml             # Maven config (Java version only)
```

## Design

See `DESIGN.md` for the full design system. Inscryption-inspired dark terminal aesthetic with CRT scanlines, runic level indicators, diegetic UI, and atmospheric procedural sound.

## Java Version

The original desktop version lives in `src/` (Java 17, Swing). Run with `mvn exec:java` if Maven is installed.

---

Built by Thomas Ou
