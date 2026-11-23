# Release 1.0.0

23 November 2026. Owner-authorised direct release to main and public GitHub Pages; arcade-directory addition awaits player feedback.

Validation: JavaScript syntax checks and six gameplay/cache tests pass. Desktop browser smoke verified launch, autonomous flight, collision result, persisted best, and pause/resume screen. Browser render inspection at 390 × 844 and 844 × 390 confirms the menu and primary controls fit portrait and landscape. These are browser-sized frames, not physical-device tests. Touch steering and cancellation are covered by the simulated-DOM test; actual phone feel remains an operator acceptance check. No audio listening test or independent reviewer is claimed.

Deployment: the Pages workflow checks source, assembles eight static assets, and deploys to the github-pages environment. The workflow attempts Pages enablement; repository administration may require a one-time Settings → Pages → GitHub Actions selection if the workflow token lacks permission.

Original procedural polygon graphics and generated Web Audio only. No third-party asset licences or external runtime dependencies. Optional sound defaults off; no analytics or server state.
