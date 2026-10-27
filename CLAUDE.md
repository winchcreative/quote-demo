# CLAUDE.md

## What this repo is

A standalone, read-only demo of a flip-book quote with e-signature, shown to prospects. It is a static site for GitHub Pages:

- `index.html` – the whole demo (HTML, CSS and JS inline).
- `404.html` – friendly not-found page.
- `vendor/` – StPageFlip, vendored so the page does not depend on a CDN for it (see `vendor/README.md`).

The demo is a made-up bathroom quote for "Mr & Mrs Taylor" (ref `DEMO-001`, dated the day it is opened) from "Your Company Here".
Everything is hard-coded in `index.html`. Signing and declining only change in-memory state, so a reload resets the demo.
There is no admin area, login, database or backend, and there must not be one.

A small banner at the top reads "Demo quote. Built by Winch Marketing" and links to `https://winchmarketing.co.uk/?r=demo-quote`.
Keep it.

## Rules

- **No client data or keys ever go in this repo.** That means no real business names, logos, staff names, addresses, phone numbers,
  email addresses, customer details, API keys, or any backend, database or auth URLs or keys, in code, comments, test data, seed data or
  commit messages. Use the "Your Company Here" placeholders.
- **No network requests** other than Google Fonts and CDN scripts. No analytics, no hotlinked images, no `fetch`/XHR. (A CSP
  `<meta>` in `index.html` enforces this; keep it in step if you add a CDN script.)
- **Customer-facing text is at least 18px.** This covers everything in the book, the signing dialog and the zoom view.
- **Buttons are at least 56px tall.**
- **No `CNAME` file**, so GitHub Pages stays on the default `github.io` address.
- **Always open a pull request. Never push to `main`.**

## Keeping the demo working

- Keep the zoom button and the single-finger page-turn swipe (a pinch must not turn a page).
- Photos are CSS placeholders labelled "Your photo here". Do not add image files or external images.
- Before opening a PR, load `index.html` in a browser (flip every page, zoom, sign, decline, reload) and search the repo for anything
  that looks like client data.
