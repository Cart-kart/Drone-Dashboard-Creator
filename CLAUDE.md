# CLAUDE.md

This file provides guidance to Claude Code when working in this repository.

## Project: Drone Dashboard Creator

Template and checklist for creating new Avilon Photon drone mission dashboards per customer.

- **Related repos:** Cart-kart/Indoor-Drone-Mission-Creator (mission files), individual dashboard repos per client
- **Template:** `template/index.html` — base dashboard, copy to root of new site repo and fill SITE_CONFIG

## Architecture

Each customer dashboard is a **separate GitHub repo** with GitHub Pages enabled.
This repo is only the template + docs — do not deploy this repo as a live site.

```
Drone-Dashboard-Creator/       ← this repo (template only)
[Customer]-Drone-Dashboard/    ← separate repo per customer (live site)
```

## Creating a New Site

1. Clone this repo → rename → re-point remote → create new GitHub repo → push
2. `cp template/index.html index.html`
3. Fill in `SITE_CONFIG` block at top of `<script>` in index.html
4. Swap logo/header image
5. Enable GitHub Pages (source: master, root)
6. Add customer to Sites Built table in NEW-SITE-CHECKLIST.md and README.md

Full instructions: [NEW-SITE-CHECKLIST.md](NEW-SITE-CHECKLIST.md)

## Key Rule

All customer settings are in `SITE_CONFIG` — one block at the top of `<script>`.
Never hardcode customer data anywhere else in the HTML.

## When Adding a New Dashboard Version

Update `template/index.html` so future sites get the latest features.
Existing site repos are independent — they do not auto-update.
