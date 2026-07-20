# Grupo Capo — Artist Booking Agency

A fast, self-contained landing page for **Grupo Capo**, a Marbella-based artist
booking agency. Editorial black-and-white design, real roster and services, and
a booking form that captures enquiries. One static file — no build, no framework.

## Files

- `index.html` — the entire site (HTML, CSS and JS inline)
- `netlify.toml` — Netlify deploy settings
- `assets/` — drop your real logo here (e.g. `assets/logo.png`)

## Deploy to Netlify

1. [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project**.
2. Connect this repo.
3. Leave the build command empty (it's static) and deploy.

You can also drag this folder onto Netlify to deploy instantly.

## The booking form (Netlify Forms)

The form uses **Netlify Forms**, so enquiries are captured automatically — no
backend needed.

- View entries: Netlify dashboard → your site → **Forms** → `booking`.
- Get emailed on every request: **Site settings → Forms → Form notifications →
  Add notification → Email** → send to `grupocapomarbella@gmail.com`.
- Fields captured: `name`, `email`, `country_code`, `phone`, `event_date`,
  `genre`, `details`.

> Netlify only starts capturing after the first deploy — submit one test booking
> once the site is live to confirm it lands in your dashboard.

## Using your real logo

The logo is currently recreated in type (the `gc` mark + GRUPO CAPO wordmark).
To use your actual logo file:

1. Save it as `assets/logo.png`. Because the site is dark, a **white or
   transparent** version looks best. (A plain black-on-white file also works —
   keep the `filter:invert(1)` shown below to flip it white.)
2. In `index.html`, replace the recreated mark in the nav **and** the footer:
   ```html
   <a href="#top" class="logo" aria-label="Grupo Capo — home">
     <img src="assets/logo.png" alt="Grupo Capo" style="height:52px;filter:invert(1)">
   </a>
   ```

## Editing content

Everything lives in `index.html`, in plain sections you can edit:

- **Stats** — `8+`, `6`, `Marbella`, `A–List`.
- **Services**, **Our Work** (the artist/venue roster), **Genres**, **Trusted
  Network**, **Why Grupo Capo** — each is a clearly labelled section.
- **Genres** — keep each card's `data-genre` matching a radio `value` in the
  form so clicking a card pre-selects it.
- **Contact** — email, phone/WhatsApp and Instagram.
