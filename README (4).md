# Crazy Arcade

A one-page site for Crazy Arcade, a retro gaming lounge. Built with plain HTML, CSS, and JavaScript — no build step, so it drops straight into GitHub Pages.

**Live sections:** cabinets on the floor, high scores, upcoming tournaments, and visit/hours info.

## Files

```
index.html   the page content and structure
style.css    theme, layout, and responsive styles
script.js    mobile nav toggle + footer year
```

## Deploying to GitHub Pages

1. Create a new repository (or use an existing one) and add these three files to the root.
2. Commit and push to GitHub.
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
5. Choose the `main` branch and `/ (root)` folder, then **Save**.
6. GitHub will give you a URL like `https://your-username.github.io/your-repo-name/` within a minute or two.

If you'd rather serve it from a `/docs` folder, move the three files into `docs/` and select that folder in step 5 instead.

## Editing content

Everything below is placeholder and should be swapped for the real thing:

- **Cabinets** (`#games` section in `index.html`) — the six sample games, genres, and years. Add or remove `<article class="cab-card">` blocks freely; the grid reflows automatically.
- **High scores** (`#scores`) — player names, cabinets, and scores in the `<table class="scoreboard">`. Add rows the same way for more entries.
- **Tournaments** (`#tournaments`) — each `<li class="ticket">` is one event: date, title, description, time, and entry fee.
- **Visit info** (`#visit`) — hours, address, and contact details.
- **Stats strip** — the four numbers just under the hero (cabinet count, years running, etc).

## Customizing the look

Colors, fonts, and spacing are all defined as CSS variables at the top of `style.css`:

```css
:root {
  --bg: #0b0908;         /* page background */
  --orange: #ff7a1a;     /* primary accent */
  --orange-bright: #ffb347;
  --orange-deep: #b8430a;
  --text: #f4ebe0;
  --muted: #a4948a;
}
```

Change these to retheme the whole site without touching layout code.

## Browser support

Uses standard CSS Grid, Flexbox, and `backdrop-filter`. Works in current versions of Chrome, Firefox, Safari, and Edge. No dependencies beyond two Google Fonts loaded via CDN in `index.html`.

## Local preview

No build tools needed. From the project folder, run any local server, for example:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.
