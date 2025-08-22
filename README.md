# Stock News Dashboard

Single-file web app to browse stock news by ticker in horizontally scrolling lanes.

## Files
- **index.html** — the app (open directly in your browser)
- **(you provide)** FastAPI backend with:
  - `GET /tickers?q=...` → `[{symbol, name}]` for autocomplete
  - `GET /news?symbol=XYZ&limit=100` → `[{title, url, published_at, source, summary, sentiment}]`

## Quick Start
1. Start your backend on `http://localhost:8000` or another host.   See the earlier FastAPI scaffold in our chat.
2. Open `index.html` in a browser.
3. Click **Settings** and set **API Base URL** to your backend (e.g., `http://localhost:8000`).

## Features
- Multiple **lanes** (one per ticker), each with a horizontal, auto-scrolling news ticker
- **Backend-powered** ticker suggestions per lane
- Drag to **reorder lanes**
- **Auto-refresh** every N seconds
- Date range & sentiment filters (client-side)
- History of added tickers

## Notes
- The HTML currently includes an optional “Use demo data” toggle. Uncheck it in **Settings** to use your live backend only.
- Sentiment badges use: positive (green), negative (red), neutral (blue/yellow depending on style; adjust in code if needed).
- Respect publisher terms and copyright. Store metadata and short extracts only, link to originals.

---
Packaged on 2025-08-22T15:12:32.
