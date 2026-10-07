# Europe at War — PWA package

This package wraps the existing Stage58 HTML game as an installable PWA.

Files:
- `index.html` — Stage58 game with PWA manifest + Service Worker registration
- `manifest.json` — install/app metadata
- `service-worker.js` — network-first update strategy with offline fallback
- `icon-192.png`, `icon-512.png` — PWA icons

## GitHub Pages
Upload these files to the root of a GitHub repository, enable:
Settings → Pages → Deploy from a branch → main → / (root)

Then open the GitHub Pages URL on Android Chrome and use Install app / Add to Home screen.

## Updating the game
Change the PWA package files and push to GitHub. The Service Worker uses network-first behavior, so the newest `index.html` is preferred when online. If a new Service Worker version is needed, increment `CACHE_NAME` in `service-worker.js`.
