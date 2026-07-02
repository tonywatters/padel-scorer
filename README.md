# Padel Scorer — Watch PWA

A lightweight padel/tennis score tracker built for a WearOS smartwatch. Full tennis scoring (0/15/30/40/Deuce/Advantage), games, sets, tiebreak at 6-6, serve indicator, undo, and a setup screen for team names.

## Files
- `index.html` — the entire app (HTML + CSS + JS in one file)
- `manifest.json` — PWA manifest so it installs on the watch
- `sw.js` — service worker for offline use
- `icon-192.png`, `icon-512.png` — app icons

## Deploy on Replit
1. Create a new Repl → import these files (or drag the folder in)
2. Serve the folder as a static site. Easiest way: add a `Static` deployment, or run a simple server:
   ```
   python3 -m http.server 8080
   ```
3. Publish the Repl — you'll get a public URL like `padel-scorer.yourname.repl.co`

## Get it on your watch
1. On the WearOS watch, open **Chrome**
2. Go to your published URL (tip: message the link to yourself and open it on the watch, easier than typing)
3. Tap the menu → **Add to Home screen**
4. It installs as a standalone app on your watch face

The service worker caches everything on first load, so it works offline after that.

## How to use
1. Enter both team names (or leave blank for "Us" / "Them")
2. Tap **Start Match**
3. Tap the **top half** to score for your team, **bottom half** for opponents
4. Scoring runs automatically: 0 → 15 → 30 → 40 → Deuce → Advantage → Game
5. Games and sets track on the left; serve dot shows who serves
6. **Undo** reverses the last point; **New** starts a fresh match
7. Best of 3 sets — winner banner appears when the match is done
