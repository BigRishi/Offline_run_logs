# Run Logger PWA

This package is ready for GitHub Pages. GitHub Pages serves the app over HTTPS, which allows Chrome to use its normal Geolocation permission prompt.

## Publish with GitHub Pages

1. On GitHub, create a new **public** repository, for example `run-logger`.
2. Extract this ZIP on your computer.
3. Upload **all files inside the `RunLogger_PWA` folder** to the repository root (not the containing folder).
   Required files: `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch `main`, folder `/(root)`, then Save.
7. Wait for GitHub Pages to publish. Open the HTTPS URL it provides, usually:
   `https://YOUR-USERNAME.github.io/run-logger/`

## On Android

1. Open that HTTPS URL in Chrome while online for the first visit.
2. Tap **Enable GPS / request permission** and choose **Allow while using the site**. Enable precise location.
3. Wait for a successful GPS fix.
4. Install using the in-page Install button, or Chrome menu → **Install app** / **Add to Home screen**.
5. Open the installed app once while online so its app shell is cached.
6. Test offline: turn on Airplane mode, turn Location back on if Airplane mode disabled it, and reopen the installed app.
7. Start and stop a short test run outdoors.

## Offline and permission notes

- The first visit and first cache installation require internet.
- After the app shell is cached, the interface and calculations work offline.
- GPS satellite positioning does not require mobile data or Wi-Fi.
- Location permission is tied to the HTTPS origin. Open the same GitHub Pages URL when granting permission and when testing.
- A PWA cannot force Android's Location switch on or bypass a denied permission.
- The browser may not grant a fresh permission prompt if you previously blocked it; reset the site's Location permission in Chrome site settings.
- The service worker caches the app shell, not GPS coordinates on a remote server. Run samples remain in page memory until exported as CSV.
- For reliable run tracking, keep the installed app in the foreground. A PWA cannot guarantee background GPS tracking after Android suspends the browser.

## Files

- `index.html` — Run Logger UI and GPS logic
- `manifest.webmanifest` — install metadata
- `sw.js` — offline app-shell cache
- `icon-192.png`, `icon-512.png` — app icons
