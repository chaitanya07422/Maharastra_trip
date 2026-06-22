# Maharashtra Monsoon Trip Planner

A single-page trip planner for a 5-day Western Ghats road trip in July — Pune → Lonavala → Matheran → Lohagad → Mahabaleshwar → Panchgani → Pune.

No build step, no dependencies. Open `index.html` in a browser or deploy the folder as-is.

**🌐 Live site:** [https://chaitanya07422.github.io/Maharastra_trip/](https://chaitanya07422.github.io/Maharastra_trip/)

## Trip at a glance

| | |
|---|---|
| **Duration** | 5 days · 4 nights |
| **Travellers** | 6 people · 1 car |
| **Distance** | ~570 km |
| **Season** | Monsoon (July) |

**Route:** Pune → Lonavala → Matheran → Lohagad → Devkund → Tamhini Ghat → Mahabaleshwar → Panchgani → Pune

## Features

- **Overview** — full route, nightly budget ranges, summary table, Google Maps link
- **Day 1–5** — hour-by-hour schedule, stay details, booking links
- **All Bookings** — priority list (what to book first)
- **Packing & Tips** — gear, safety rules, car tips, local notes
- Mobile-friendly layout with sticky tab navigation

## View locally

```bash
# macOS
open index.html

# Or serve with Python (optional)
python3 -m http.server 8080
# Then open http://localhost:8080
```

## Deploy

This is a static site — only `index.html` needs to be hosted.

### GitHub Pages

```bash
cd maharashtra-monsoon-trip
git init
git add index.html README.md
git commit -m "Add Maharashtra monsoon trip planner"
gh repo create maharashtra-monsoon-trip --public --source=. --push
```

Then in the repo on GitHub: **Settings → Pages → Source: Deploy from branch `main` / folder `/ (root)`**.

Your site will be live at `https://<username>.github.io/maharashtra-monsoon-trip/`.

### Netlify

1. Go to [netlify.com](https://www.netlify.com) and sign in.
2. Drag the `maharashtra-monsoon-trip` folder onto the deploy area.
3. Netlify gives you a URL instantly (e.g. `random-name.netlify.app`).

Or with the CLI:

```bash
npx netlify-cli deploy --prod --dir=.
```

### Vercel

```bash
npx vercel --prod
```

Run from inside this folder; Vercel detects it as a static site.

### Cloudflare Pages

1. Push the repo to GitHub (see GitHub Pages steps above).
2. In Cloudflare Dashboard → **Pages → Create project → Connect to Git**.
3. Build command: leave empty. Output directory: `/`.

## Project structure

```
maharashtra-monsoon-trip/
├── index.html   # entire app (HTML + CSS + JS)
└── README.md
```

## Editing the plan

All content lives in `index.html`. Search for the day or place name you want to change — schedules, stays, and booking links are plain HTML.

Tab switching is handled by a small `show()` function at the bottom of the file.

## License

Personal trip planner — use and modify freely.
