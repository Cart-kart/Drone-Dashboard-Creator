# New Customer Site — Build Checklist

Clone this repo as the template → fill SITE_CONFIG → swap logo/colors → new GitHub repo.
~30 min per site once all info below is provided.

## How to Start

```bash
git clone https://github.com/Cart-kart/Drone-Dashboard-Creator.git [CustomerName]-Drone-Dashboard
cd [CustomerName]-Drone-Dashboard
cp template/index.html index.html
git remote set-url origin https://github.com/Cart-kart/[CustomerName]-Drone-Dashboard.git
gh repo create Cart-kart/[CustomerName]-Drone-Dashboard --public
git push -u origin master
gh api repos/Cart-kart/[CustomerName]-Drone-Dashboard/pages --method POST --field "source[branch]=master" --field "source[path]=/"
```

Then fill in `SITE_CONFIG` at the top of `index.html` and add a CLAUDE.md.

---

## Info Needed from Customer

### Branding
| # | Item | Example |
|---|---|---|
| 1 | Customer short name | PCG |
| 2 | Customer full name | Perfect Companion Group |
| 3 | Logo / header image file | PCGHEADER.png |
| 4 | CI colors (or just send header image) | light blue bg, dark navy text |

### Operations
| # | Item | Example |
|---|---|---|
| 5 | Drone name(s) | Photon 005 |
| 6 | Battery IDs — active | 01, 02, 03 |
| 7 | Battery IDs — dead/decommissioned | 04 |
| 8 | Aisle map (number → name) | 1: A01_ROW1, 2: A02_ROW2 |
| 9 | Shift hours | Day 07:00–20:59 / Night 21:00–06:59 |
| 10 | Operator name format (suffix to strip?) | " PCG" suffix, or none |

### Data Source
| # | Item | Example |
|---|---|---|
| 11 | Google Form set up yet? | Yes / No |
| 12 | GAS proxy URL or Sheet CSV URL | https://script.google.com/... |
| 13 | Battery ID correction rules | #01 was written as #11 during Jan 2026 |

### Access
| # | Item | Example |
|---|---|---|
| 14 | Dashboard PIN (4 digits) | 1234 |
| 15 | GitHub repo name | CustomerName-Drone-Dashboard |

---

## SITE_CONFIG Reference

All customer settings live in one block at the top of `<script>` in `index.html`:

```js
const SITE_CONFIG = {
  customer:    "PCG",
  version:     "V.1.0 PCG",
  gasProxyUrl: "",          // item 12
  csvUrl:      "",          // item 12
  drones:      { active: ["Photon 005"] },          // item 5
  batteries:   { active: [], dead: [] },            // items 6, 7
  aisleMap:    {},                                   // item 8
  aislePrefixN: "A",
  aislePrefixE: "B",
  battRemapRules: [],                               // item 13
  shifts:      { day: { start:7, end:20 }, night: { start:21, end:6 } }, // item 9
  columns:     { timestamp:0, person:1, type:2, completed:3, reason:4,
                 armTime:5, disarmTime:6, battName:7, battLanding:8,
                 drone:9, rcOp:10, logId:22, inPlant:29, battCharge:31 },
  pin:         "0000",                              // item 14
};
```

See [docs/site-config-reference.md](docs/site-config-reference.md) for full field descriptions.

---

## Sites Built

| Customer | Repo | Live URL | Status |
|---|---|---|---|
| Harley Davidson / DHL | [HD-DHL-Drone-Dashboard](https://github.com/Cart-kart/HD-DHL-Drone-Dashboard) | https://cart-kart.github.io/HD-DHL-Drone-Dashboard/ | Live V.0.7.5 |
| PCG (Perfect Companion Group) | [PCG-Drone-Dashboard](https://github.com/Cart-kart/PCG-Drone-Dashboard) | https://cart-kart.github.io/PCG-Drone-Dashboard/ | Live |
| Yusen Logistics | [Yusen-Drone-Dashboard](https://github.com/Cart-kart/Yusen-Drone-Dashboard) | https://cart-kart.github.io/Yusen-Drone-Dashboard/ | Live V.1.0 |
