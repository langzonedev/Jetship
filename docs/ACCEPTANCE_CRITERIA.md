# Acceptance and verification

- One obvious launch/retry action. Screen halves steer continuously, release stops steering input, and keyboard provides an equivalent path.
- Automatic forward travel; pillars end a run; ring collection adds boost exactly once. Rows leave a clear ring lane.
- Pause freezes travel, clears inputs and resumes deliberately. Hidden/background pages pause.
- Fresh runs reset position, velocity, rings, obstacles and boosts. Best distance persists when storage is available; blocked storage cannot stop play.
- Phone portrait, phone landscape and desktop layouts avoid page scrolling and support large touch controls. Reduced motion removes shake, speed trails and hover bobbing.
- Static game assets, manifest and offline preload paths resolve under /Jetship/.
- No runtime third-party dependencies, accounts, tracking or secrets.

## Evidence

Automated: `npm run check`; six Node tests covering touch steering/cancellation, pause/retry, ring boost and acceleration, collision/best/storage failure, 500 generated clear-lane rows, and all offline preload paths. Tests run the actual game closure in a simulated DOM; they do not establish browser rendering or real-device performance.

Browser: desktop preview renders the original skyline and ship; launch progresses to a collision result and records a local best. Further browser checks and deployment disposition are recorded in RELEASE.md.
