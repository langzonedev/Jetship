# Jetship

**[Play Jetship](https://langzonedev.github.io/Jetship/)**

A futuristic, nostalgic endless flyer by **Lang Systems**. Thread a neon skyline, dodge pillars, chase boost rings, and beat your personal best. Built for a quick run on a phone or desktop.

## Controls

| Action | Phone / tablet / mouse | Keyboard |
| --- | --- | --- |
| Steer left | Hold the left half of the screen | Left arrow / A |
| Steer right | Hold the right half of the screen | Right arrow / D |
| Fly straight | Release | Release |
| Pause / resume | Pause button / Keep flying | P / Escape |

Forward flight is automatic. Fly through a lime ring to gain a short speed boost; chain rings for streak feedback. Pillars end the run with an explosion and tumbling ship debris; results appear after three seconds. Distance and rings are shown separately. Your best distance is stored on this device. Switching tabs automatically pauses the game.

## Features

- Original low-poly jet with banking, engine glow, perspective skyline and sunset grid.
- Continuous analog steering with gentle inertia; full-screen touch targets.
- Procedural obstacle rows with clear routes, a gentle opening, and increasing pace.
- Boost trails, particles, close-call feedback, ring streaks and quick retries.
- Optional synthesized audio (muted by default), fullscreen where supported, and reduced-motion effects.
- Installable web app with native-size icons and offline play after an initial online load.
- No accounts, analytics, external assets, runtime libraries or paid services.

## Run locally

Requires Python 3 for a local server and Node.js 22+ for validation. No dependency installation or build is needed.

```sh
python3 -m http.server 8080
# Open http://localhost:8080
npm run check
npm test
```

Serve over HTTP locally or HTTPS when hosted; service workers cannot run from a file URL.

## Deployment

`.github/workflows/pages.yml` validates the game and deploys only its static assets to GitHub Pages when `main` changes. Pages uses **GitHub Actions** as its source. If the repository's workflow token cannot enable Pages automatically, select that source once under Settings → Pages. The expected public URL is https://langzonedev.github.io/Jetship/.

The service worker uses network-first updates and an offline cache. After an update, finish the current run and reopen the app. Increment the cache version in `sw.js` when changing its precached file list.

## Scope

Standalone first release. Arcade-directory integration is intentionally deferred until Greg has tried the game. Scores are local, not a shared leaderboard. Real-device feel and audio still benefit from player feedback.

See [acceptance and verification](docs/ACCEPTANCE_CRITERIA.md) and [architecture](docs/ARCHITECTURE.md).
