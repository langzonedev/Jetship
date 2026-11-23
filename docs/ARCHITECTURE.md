# Architecture

Buildless HTML/CSS/JavaScript. Canvas 2D projects world coordinates into perspective; painter sorting renders original polygonal pillars, ring strokes and ship geometry. No GPU dependencies or external requests are required for play. Device pixel ratio is capped at 2 to limit fill cost.

requestAnimationFrame with delta time drives flight. Frame gaps are capped at 40 ms; hidden pages and window blur pause the run. State transitions are menu → play → result, with play ↔ paused. Pointer capture and cancellation clear touch state; key state clears on pause/retry. Both directions together cancel.

Procedural rows place a ring in one of five lanes and omit the obstacle in that lane. Difficulty increases base speed and row density, with caps. Ring boosts are temporary and capped at five seconds. Collision checks occur at the ship crossing plane; frame movement remains below obstacle thickness at the maximum speed. Near misses are feedback only, not score inflation. Displayed distance is world travel multiplied by two.

Only best distance and sound preference persist in localStorage; failures are tolerated. No secrets, private strategy or personal data are present. Web Audio starts after a user gesture and is silent by default. An HTTPS service worker precaches local game assets and falls back to cache when offline. It never intercepts cross-origin requests. PWA scope and all URLs are relative for GitHub Pages project subpaths.

Deployment is GitHub Actions to Pages. Roll back by reverting the game commit on main; the next successful workflow redeploys it. No backend or database.
