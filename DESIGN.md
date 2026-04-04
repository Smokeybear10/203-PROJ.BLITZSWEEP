# Design System — SWEEPER

## Product Context
- **What this is:** Arcade-pressure minesweeper with 5 escalating levels, countdown timers, and scoring
- **Who it's for:** People who want minesweeper with stakes, not a calm Sunday puzzle
- **Space/industry:** Browser puzzle games. Competitors: freeminesweeper.org, minesweeper.online, minesweeper-pro.com
- **Project type:** Web app (single-page game)

## Aesthetic Direction
- **Direction:** Arcade Pressure
- **Decoration level:** Intentional — subtle glow effects on interactions, screen-edge vignette, minimal but purposeful
- **Mood:** Dark, electric, urgent. The feeling of an arcade cabinet at 11pm where the timer is counting down and you're in the zone. Fun-tense, not war-room-tense. Not calm puzzle gray. Not military cold.
- **Reference sites:** Every competitor is gray/white Windows 95 nostalgia. SWEEPER is the opposite.

## Typography
- **Display/Hero:** Space Grotesk (700) — geometric, tense, punchy for "SWEEPER" and headings
- **Body:** DM Sans (400/500) — clean, readable for menus, rules, instructions
- **UI/Labels:** DM Sans (500/600)
- **Data/Tables:** JetBrains Mono (700, tabular-nums) — LED-counter feel for timer, score, mine count
- **Code:** JetBrains Mono
- **Loading:** Google Fonts CDN
- **Scale:** 11px (labels) / 13px (body small) / 15px (body) / 18px (h4) / 24px (h3) / 36px (h2) / 48px (h1)

## Color
- **Approach:** Expressive dark palette
- **Background:** #0A0A0F (near-black)
- **Surface (unrevealed cells):** #1A1A2E (dark indigo)
- **Surface (revealed cells):** #0F0F1A (deeper dark)
- **Accent:** #E8FF00 (acid yellow — timer, active states, score, level indicator)
- **Danger:** #FF2D55 (hot pink-red — mines, low time warning, game over)
- **Text:** #E2E2F0 (cool white)
- **Text muted:** #6B6B80
- **Cell border:** rgba(255,255,255,0.06) — hairline separators, not raised 3D borders
- **Cell hover:** rgba(232,255,0,0.08)
- **Number colors (neon-saturated):** 1=#4DA6FF, 2=#00E676, 3=#FF2D55, 4=#7C4DFF, 5=#FF6D00, 6=#00E5FF, 7=#E8FF00, 8=#B0B0C0
- **Semantic:** success #00E676, warning #E8FF00, error #FF2D55
- **Dark mode:** This IS dark mode. No light mode planned.

## Spacing
- **Base unit:** 4px
- **Density:** Comfortable — cells need breathing room for touch targets
- **Scale:** 2xs(2) xs(4) sm(8) md(12) lg(16) xl(24) 2xl(32) 3xl(48)

## Layout
- **Approach:** Game-centered, single viewport
- **Grid:** The board IS the page. Status bar wraps tightly above, controls below. No scrolling during gameplay.
- **Max content width:** 520px (game container)
- **Border radius:** sm:2px (cells), md:4px (buttons), lg:8px (containers), full:9999px (badges)

## Motion
- **Approach:** Intentional
- **Cell reveal:** Quick flash animation (background pulses from accent-tint to revealed, 300ms ease-out)
- **Flag place:** Scale pop (0.8 -> 1.1 -> 1.0, 200ms ease-out)
- **Timer danger:** At <15 seconds, timer bar and time value pulse (0.8s ease-in-out infinite). Container gains red glow.
- **Level transition:** Brief sweep animation between stages
- **Easing:** enter(ease-out) exit(ease-in) move(ease-in-out)
- **Duration:** micro(100ms) short(200ms) medium(300ms) long(500ms)

## Key Design Decisions

### Safe (category baseline)
- Grid-based cell layout — this IS minesweeper, users expect the grid
- Color-coded numbers (1=blue, 2=green, 3=red) — universal muscle memory
- Right-click/long-press to flag — standard interaction pattern

### Risks (where SWEEPER gets its own face)
- Full dark arcade aesthetic — every competitor is gray/white/light
- Timer as a depleting bar, not just a number — plus background pulses red at <15s
- Level progression shown as arcade "stages" with visual pip indicator
- Neon glow effects on cell interactions (reward feedback)

## Decisions Log
| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-04-04 | Initial design system created | Created by /design-consultation based on competitive research (5 sites) + Claude subagent input. Every competitor is Windows 95 gray. SWEEPER plays like an arcade game (countdown timer, escalating difficulty), so the design reflects urgency, not calm. |
| 2026-04-04 | Acid yellow #E8FF00 as accent | Subagent proposed this over electric cyan. Yellow reads as urgency/warning, not coolness. Better fit for countdown pressure. |
| 2026-04-04 | No light mode | Dark-first is the aesthetic thesis. Adding a light mode would dilute the arcade identity. |
