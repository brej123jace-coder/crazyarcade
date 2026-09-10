# Crazy Arcade

A single-page site for a retro arcade lounge: cabinet showcase, tab-switchable house leaderboards, and an upcoming-tournaments list with a live countdown. Orange-and-black neon theme.

## Files

- `index.html` — page structure and content
- `styles.css` — all styling (no build step, no framework)
- `script.js` — leaderboard tabs, tournament rendering, countdown timer, mobile nav

No dependencies to install and no build step — it's plain HTML/CSS/JS, so it runs as-is.

## Publish it on GitHub Pages

1. Create a new GitHub repository (or use an existing one).
2. Add these three files to the **root** of the repo.
3. Commit and push:
   ```bash
   git init
   git add .
   git commit -m "Add Crazy Arcade site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```
4. On GitHub: go to **Settings → Pages**. Under "Build and deployment," set **Source** to "Deploy from a branch," pick the `main` branch and the `/ (root)` folder, then save.
5. GitHub will give you a URL like `https://YOUR-USERNAME.github.io/YOUR-REPO/`. It can take a minute or two to go live after the first deploy.

## Customizing

- **Games/cabinets:** each cabinet is an `<article class="cabinet">` block in `index.html`. Swap the name, description, and tags to reskin one. The little SVG icon inside `.cabinet-screen` is plain inline SVG — edit the shapes or swap in your own.
- **Leaderboards:** edit the `boards` object at the top of `script.js` — one entry per cabinet, keyed to match the `data-game` attribute on each tab button.
- **Tournaments:** edit the `tournaments` array in `script.js`. Dates use JS `Date` objects (`'YYYY-MM-DDTHH:MM:SS'`); the countdown automatically tracks whichever one is soonest.
- **Colors:** the orange/black palette lives as CSS custom properties at the top of `styles.css` (`:root`) — `--orange`, `--orange-deep`, `--amber`, plus `--bg`/`--panel` for the black tones.

## Notes

- Palette contrast was checked against WCAG AA (4.5:1 minimum for body text) for every text/background pairing before shipping — all pass, several comfortably above AAA (7:1).
- The neon "marquee" bars and section headings have a subtle flicker animation (like an aging neon sign) that's automatically disabled if the visitor's OS has "reduce motion" turned on.
- This is a display-only version — the leaderboard and tournament data are static placeholders in `script.js`, not connected to live gameplay. Ask if you'd like playable mini-games added to the cabinets, like in the previous build.
