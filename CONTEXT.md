# Pong Game — Project Context

> **Last updated:** 2026-02-26
> **Purpose:** Persistent context for Claude to read when resuming work on the Pong game.

---

## Live App

**URL:** https://adakin97.github.io/pong
**GitHub repo:** https://github.com/adakin97/pong
**Local repo:** `C:\Users\alexd\Claude_Projects\pong-game\`
**Main file:** `C:\Users\alexd\Claude_Projects\pong-game\index.html`

---

## What It Is

A mobile-first Pong game built as a single HTML file, hosted on GitHub Pages and playable in Safari on iPhone. Also works on desktop in any browser.

---

## Features

- **Tennis theme** — rackets drawn as proper tennis rackets (oval head, string grid, wooden handle), ball as a yellow-green tennis ball with seam curves
- **Tennis court background** — green grass hard court with white lines (baselines, sidelines, service lines, centre service line), net with mesh and posts
- **Touch controls** — drag finger on the left half of the screen to move the player paddle
- **Mouse/keyboard controls** — mouse or ↑↓ arrow keys on desktop
- **AI opponent** — red racket on the right, tracks ball with capped speed
- **Scoring** — first to 7 points wins
- **Ball physics** — angle of return depends on where the ball hits the racket head; ball speeds up slightly each rally
- **Responsive** — canvas scales to fill any screen size

---

## Controls

| Input | Action |
|-------|--------|
| Drag finger (left half) | Move player paddle (mobile) |
| Mouse move | Move player paddle (desktop) |
| ↑ ↓ Arrow keys | Move player paddle (desktop) |
| Tap / Space / Enter | Start or restart game |

---

## File Structure

```
pong-game/
├── index.html   — full game (single file)
└── README.md    — not yet created
```

Also exists:
- `C:\Users\alexd\Claude_Projects\pong.html` — original desktop-only version
- `C:\Users\alexd\Claude_Projects\App\pong_mobile.html` — mobile version before GitHub deployment
- `G:\My Drive\0. Active\Testing\pong_mobile.html` — copy in Google Drive (used during deployment testing)

---

## Deployment

- Hosted on **GitHub Pages** from the `main` branch, `/ (root)` folder
- To deploy changes: edit `index.html`, then run from `pong-game\`:
  ```
  git commit -am "description"
  git push
  ```
- Changes go live within 30-60 seconds

---

## Session Log

| Date | What Happened |
|------|---------------|
| 2026-02-26 | Built desktop Pong game (pong.html) with mouse/keyboard controls, basic white paddles and ball. |
| 2026-02-26 | Built mobile version (pong_mobile.html) with touch controls and responsive canvas. Attempted Google Drive → Safari route — failed (iPhone blocks local HTML). Deployed to GitHub Pages at https://adakin97.github.io/pong. |
| 2026-02-26 | Changed background colour: pink → blue → pink (user testing changes). |
| 2026-02-26 | Added tennis racket visuals (oval head, string grid, wooden handle/grip) for both paddles. Added tennis ball (yellow-green with white seam curves and radial gradient). |
| 2026-02-26 | Added full tennis court background: green grass surface (two shades), white court lines (baselines, sidelines, service lines, centre service line), net with mesh, top tape and posts. |

---

## Key Decisions

- Single HTML file — no build tools, no dependencies, works anywhere
- GitHub Pages for hosting — free, instant, permanent URL
- Canvas-based rendering — full control over visuals
- Touch on left half only — right half free for other gestures
- Physics: collision angle based on hit position on racket head; max speed capped to prevent unplayable speeds
