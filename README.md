# Rugby Stat Tracker

A single-page, mobile-first rugby match tracker styled for the Georgia Bulldogs. It provides a live scoreboard, match clock, team statistics, and a shareable match summary without requiring a build step or backend.

## Features

- Live score calculated from tries (5), conversions (2), and drop/penalty goals (3)
- Start, pause, half-time, full-time, and extra-time match tracking
- Timed possession and territory percentages
- Tracking for scrums, lineouts, turnovers, penalties, and yellow/red cards
- Card log with the match period and timestamp for each incident
- Hold a `+` control to undo a won/lost scrum or lineout entry; use the matching minus controls for other stats
- Visitor/home team names, with an optional Georgia-side highlight selected before the match starts
- Copy or native-share a complete text match summary
- Automatic local persistence in the browser via `localStorage`
- Mobile-friendly controls, keyboard focus states, reduced-motion support, vibration feedback where available, and a screen wake lock while the clock runs

## Run it

Save the pasted HTML as `index.html`, then open it in a modern browser:

```text
index.html
```

No dependencies, server, build process, or installation are required. The page loads its display fonts from Google Fonts; all match data stays in the current browser's local storage.

## How to use

1. Enter both team names.
2. Choose whether Visitor or Home is the Georgia side, if applicable. This choice locks once the match begins.
3. Start the clock. Statistic controls unlock after both names are entered and the clock has started.
4. Tap the relevant controls as play unfolds. For possession and territory, tap the team currently in control; tap it again to mark neither side.
5. Mark half-time and full-time when appropriate. These pause the clock and capture the score at that moment.
6. Select **Share stats** to copy or share the generated match summary.
7. Select **New match**, then confirm with a second tap, to clear the saved match.

## Data behavior

Match state is stored under the browser key `rugby-stat-tracker-v1`. Reloading restores the saved match in a paused state so that no elapsed time is added while the page is closed.

## Browser support

Use a current evergreen browser. Native sharing, vibration, and screen wake lock are progressive enhancements: the tracker continues to work if a browser does not support them.

## Attribution

© 2026 Larry Doong. All Rights Reserved.
