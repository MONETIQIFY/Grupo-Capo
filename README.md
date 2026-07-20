# Grupo Capo — Artist Booking Agency landing page

A fast, self-contained landing page for **Grupo Capo**. Visitors read about what
you do, browse the genres you book, see your past work, and submit a booking
request (name, email, phone, genre + event details). It's a single static file —
no build, no framework, nothing to maintain.

## Files

- `index.html` — the entire site (HTML, CSS and JS inline)
- `netlify.toml` — Netlify deploy settings
- `assets/` — drop your real logo here (e.g. `assets/logo.png`)

## Deploy to Netlify

1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project**.
2. Connect this GitHub repo.
3. Leave the build command empty (it's a static site) and deploy.

You can also just drag this folder onto Netlify to deploy instantly.

## The booking form (Netlify Forms)

The form uses **Netlify Forms**, so submissions are captured automatically — no
backend needed.

- View entries: Netlify dashboard → your site → **Forms** → `booking`.
- Get emailed on every request: **Site settings → Forms → Form notifications →
  Add notification → Email**.
- Fields captured: `name`, `email`, `phone`, `event_date`, `genre`, `details`.

> Netlify only starts capturing after the first deploy — submit one test booking
> once the site is live to confirm it lands in your dashboard.

## Editing content (no coding needed)

Open `index.html` and look for the `EDIT ME` comments:

- **Stats strip** — swap `120+`, `50+`, `15+` for your real numbers (or delete the section).
- **Genres** — currently Afrobeats, UK Hip Hop, USA Rap, European Rap, House.
  Keep each card's `data-genre` matching a radio `value` in the form so clicking
  a card pre-selects it.
- **Our Work** — replace the four highlights with your real events, venues and artists.

## Using your real logo

The logo is currently a styled text version of your `gc` mark. To use your image:

1. Save your logo as `assets/logo.png` (a white/transparent version looks best on
   the dark background).
2. In `index.html`, replace the `<span class="mark">gc</span>` + `<span class="words">…</span>`
   block inside the nav (and footer) with:
   ```html
   <img src="assets/logo.png" alt="Grupo Capo" style="height:44px" />
   ```
