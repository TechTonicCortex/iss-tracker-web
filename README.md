# ISS Live Tracker

**Shows where the International Space Station is right now, and who is on board.**
Open `index.html` in a browser. It needs internet.

## What it does
- Plots the ISS position on a live map and updates it about every 5 seconds
- Lists the astronauts currently in space

## How it works
- **Where it is:** `api.wheretheiss.at` returns the ISS latitude and longitude.
- **Who is aboard:** `api.open-notify.org` returns the people in space.
- **Map:** Leaflet.js.
- The page asks the APIs again on a timer using `fetch` and `setInterval`.
- Both APIs are free and need no key.

## Known issue (honest)
The astronaut list uses an `http://` link. When the page is hosted on GitHub Pages (`https://`), browsers block that request, so the crew list may not load there. It works when you open the file from your computer. Fix: use an HTTPS source, or show a friendly "crew list unavailable" message.

## What I learned
How to get live data from an API, and why live data can fail (rate limits, blocked requests, no internet).

## Next steps
- Draw the ISS's recent path
- Show a message when an API fails instead of leaving the page blank

---
Part of [Aadit's projects](https://github.com/TechTonicCortex/techtoniccortex).
