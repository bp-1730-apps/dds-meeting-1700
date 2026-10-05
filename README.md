# dds-meeting-1700 — Novus Ops Hub, Plant 1700

Its own copy of the Novus Ops Hub. No L2L sync lives here: this plant's Excel workbook
calls L2L itself, and its Power Automate flow writes everything (including OEE, Downtime,
Code Red, Code Yellow) into `dashboard-data.json` at the repo root.

Site:  https://<owner>.github.io/dds-meeting-1700/
Data:  https://<owner>.github.io/dds-meeting-1700/dashboard-data.json

Edit before going live:
- `plants.json` — `location` and `lines` (line codes must match the `Line` column your workbook sends)
- `supabase-config.js` — this plant's Supabase URL and anon key
- `index.html` — the `ALLOWED_USERS` list (each user's `plant` must be `1700`)

Setup: see 00_REBUILD_GUIDE.md and 3-PowerAutomate-Setup-Guide.md in the kit.
