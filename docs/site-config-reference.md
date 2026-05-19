# SITE_CONFIG Field Reference

All fields live in the `SITE_CONFIG` block at the top of `<script>` in `index.html`.

| Field | Type | Description |
|---|---|---|
| `customer` | string | Customer short name (shown in UI) |
| `version` | string | Version label e.g. `"V.1.0 PCG"` |
| `gasProxyUrl` | string | Google Apps Script proxy exec URL |
| `csvUrl` | string | Published Google Sheet CSV URL |
| `drones.active` | string[] | Active drone names |
| `batteries.active` | string[] | Active battery IDs |
| `batteries.dead` | string[] | Decommissioned battery IDs |
| `aisleMap` | object | Aisle number → display name mapping |
| `aislePrefixN` | string | Prefix letter for N-type aisles |
| `aislePrefixE` | string | Prefix letter for E-type aisles |
| `battRemapRules` | array | Battery ID correction rules (fixes historical typos) |
| `shifts.day.start` | number | Day shift start hour (24h) |
| `shifts.day.end` | number | Day shift end hour (24h) |
| `shifts.night.start` | number | Night shift start hour (24h) |
| `shifts.night.end` | number | Night shift end hour (24h) |
| `columns.timestamp` | number | Column index for timestamp |
| `columns.person` | number | Column index for operator name |
| `columns.type` | number | Column index for flight type |
| `columns.completed` | number | Column index for completed flag |
| `columns.reason` | number | Column index for reason/note |
| `columns.armTime` | number | Column index for arm time |
| `columns.disarmTime` | number | Column index for disarm time |
| `columns.battName` | number | Column index for battery name |
| `columns.battLanding` | number | Column index for battery at landing |
| `columns.drone` | number | Column index for drone name |
| `columns.rcOp` | number | Column index for RC operator |
| `columns.logId` | number | Column index for log ID |
| `columns.inPlant` | number | Column index for in-plant flag |
| `columns.battCharge` | number | Column index for battery charge % |
| `pin` | string | 4-digit PIN for dashboard access |
