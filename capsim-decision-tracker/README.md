# CAPSIM Decision Tracker

A lightweight, browser-based tool for tracking CAPSIM simulation decisions across rounds. Calculates key metrics automatically and persists data locally.

## Quick Start

**Option 1: Open directly (no server needed)**
```bash
# Just open the file in your browser
open index.html
# or double-click index.html in your file explorer
```

**Option 2: Serve locally (recommended for full functionality)**
```bash
# Using Python
python3 -m http.server 8080
# Then open http://localhost:8080

# Using Node
npx serve .
# Then open the provided URL
```

## Features

- **Round-by-round tracking** — Switch between rounds 1–8+ with the tab selector
- **Auto-calculated metrics** — Revenue, operating spend, margin %, capacity utilization, automation cost estimate
- **Local persistence** — Data saves to `localStorage` automatically; survives browser restarts
- **Export to JSON** — Download all rounds as a timestamped JSON file for reports
- **Zero dependencies** — Single HTML file, runs anywhere

## Fields Tracked

| Category | Fields |
|----------|--------|
| R&D | Budget |
| Marketing | Budget, Promo Budget |
| Production | Capacity, Automation Level |
| Sales | Forecast (units), Price/unit |
| HR | Training Budget |
| TQM | Investment |
| Finance | Stock Buyback, Dividend/share |

## Metrics Calculated

- **Projected Revenue** = Sales Forecast × Price
- **Total Operating Spend** = R&D + Marketing + Promo + HR + TQM
- **Est. Margin %** = (Revenue - Spend) / Revenue × 100
- **Capacity Utilization %** = Forecast / Capacity × 100
- **Automation Cost Est.** = Capacity × Automation × $4,000

## Data Storage

All data lives in your browser's `localStorage` under key `capsim-decisions`. No server, no account, no tracking.

To clear: Open DevTools → Application → Local Storage → Delete `capsim-decisions`.

## Deployment

Deploy as a static site anywhere:
- **GitHub Pages**: Push to a repo, enable Pages in Settings
- **Netlify**: Drag the folder to netlify.com/drop
- **Vercel**: `npx vercel` in the folder
- **Render**: Static site, build command `echo 'static'`, publish directory `.`

## Rep Note

See [REP_NOTE.md](REP_NOTE.md) for the build reflection.