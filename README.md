# Drone Dashboard Creator

Template and checklist for spinning up a new Avilon Photon drone mission dashboard per customer site.

Each customer gets their own repo + GitHub Pages URL. This repo is the starting point.

## How to Create a New Site

```bash
git clone https://github.com/Cart-kart/Drone-Dashboard-Creator.git [CustomerName]-Drone-Dashboard
cd [CustomerName]-Drone-Dashboard
cp template/index.html index.html
git remote set-url origin https://github.com/Cart-kart/[CustomerName]-Drone-Dashboard.git
gh repo create Cart-kart/[CustomerName]-Drone-Dashboard --public
git push -u origin master
gh api repos/Cart-kart/[CustomerName]-Drone-Dashboard/pages --method POST --field "source[branch]=master" --field "source[path]=/"
```

Then fill in `SITE_CONFIG` at the top of `index.html`. See [NEW-SITE-CHECKLIST.md](NEW-SITE-CHECKLIST.md) for the full checklist.

## Live Sites

| Customer | Repo | Live URL | Status |
|---|---|---|---|
| Harley Davidson / DHL | [HD-DHL-Drone-Dashboard](https://github.com/Cart-kart/HD-DHL-Drone-Dashboard) | https://cart-kart.github.io/HD-DHL-Drone-Dashboard/ | Live V.0.7.5 |
| PCG (Perfect Companion Group) | [PCG-Drone-Dashboard](https://github.com/Cart-kart/PCG-Drone-Dashboard) | https://cart-kart.github.io/PCG-Drone-Dashboard/ | Live |
| Yusen Logistics | [Yusen-Drone-Dashboard](https://github.com/Cart-kart/Yusen-Drone-Dashboard) | https://cart-kart.github.io/Yusen-Drone-Dashboard/ | Live V.1.0 |
| DKSH Bangna | [DKSH-Drone-Dashboard](https://github.com/Cart-kart/DKSH-Drone-Dashboard) | https://cart-kart.github.io/DKSH-Drone-Dashboard/ | Blank — SITE_CONFIG pending |

## Files

| File | Purpose |
|---|---|
| `template/index.html` | Base dashboard — copy to root, fill SITE_CONFIG |
| `NEW-SITE-CHECKLIST.md` | Step-by-step checklist + info to gather from customer |
| `docs/site-config-reference.md` | Full SITE_CONFIG field reference |
| `CLAUDE.md` | Claude Code guidance for this repo |
