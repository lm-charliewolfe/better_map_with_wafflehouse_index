# Better Map Widget + Waffle House Index

LogicMonitor map widget (fork of Kevin Ford's Better Map) with an optional **Waffle House Index** events overlay.

## What to use

**Use the CDN loader as a LogicMonitor Text widget.** That is the supported way to run this on a dashboard.

| What | Where |
|------|--------|
| **Paste into LogicMonitor** | [`logicmonitor/Better_Map_Widget-CDN.html`](logicmonitor/Better_Map_Widget-CDN.html) |
| Widget code loaded from GitHub (automatic) | [`src/`](src/) |
| Old / experimental files (do not paste) | [`legacy/`](legacy/) |

---

## Setup (LogicMonitor Text widget)

### Step 1 — Open the loader file

In this repo, open:

`logicmonitor/Better_Map_Widget-CDN.html`

### Step 2 — Copy the whole file

Select all (Cmd+A on Mac, Ctrl+A on Windows) and copy (Cmd+C / Ctrl+C).

### Step 3 — Paste into LogicMonitor

1. Open your LogicMonitor dashboard.
2. Add or edit a **Text** widget.
3. Click **Source** (not the visual editor).
4. Paste the copied HTML.
5. **Save** the widget.

### Step 4 — Confirm it loaded

Open the map and check the version label (for example **v3.78 CDN + WHI**).  
Enable **Events** in the gear menu and select **Waffle House Index** to see store markers.

---

## After you update this repo on GitHub

LogicMonitor keeps whatever you last pasted. A browser refresh alone does **not** pull new code.

1. Copy **`logicmonitor/Better_Map_Widget-CDN.html`** again from GitHub.
2. Re-paste into the Text widget **Source** and save.
3. Hard-refresh the dashboard (Cmd+Shift+R or Ctrl+Shift+R).

---

## Waffle House Index

- About **2,100** locations from [`src/data/wafflehouse.json`](src/data/wafflehouse.json)
- **Green** = open, **red pin** = temporarily closed
- In the gear menu: **Events** → open the dropdown → check **Waffle House Index**
- **Hide open** (next to the dropdown) shows only closed locations

---

## Repo layout

```
logicmonitor/          <- START HERE: paste Better_Map_Widget-CDN.html into LM
src/                   <- JS, CSS, icons, data (loaded from GitHub by the widget)
  Better_Map_Widget.js
  Better_Map_Widget.css
  icons/
  data/wafflehouse.json
legacy/                <- Do not use on dashboards (too large or standalone demos)
```

---

## Do not use on dashboards

- **`legacy/Better_Map_Widget-Full.html`** — ~370 KB single file; LogicMonitor save can hang.
- **`legacy/Wafflehouse-Map-Widget.html`** — standalone demo only.

Always use **`logicmonitor/Better_Map_Widget-CDN.html`**.

---

## Credits

- Better Map Widget: Kevin Ford / [LogicMonitor custom_widgets](https://github.com/logicmonitor/custom_widgets)
- Waffle House overlay fork: Charlie Wolfe
