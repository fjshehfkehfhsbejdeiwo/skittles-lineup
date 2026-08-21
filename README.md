# Skittles Lineup Manager

A one-file web app for running fielding and batting lineups for your 2nd grade softball team, on your phone, during the game. No install, no internet required once it's on your phone — everything is saved locally in the browser.

## Getting it onto your phone

The whole app is the single file `index.html`. Easiest ways to open it on your phone:

1. **Email it to yourself** (or AirDrop / Google Drive / OneDrive), open the attachment on your phone, and choose "Open in Chrome/Safari."
2. Or, if you'd like a stable bookmark-able link instead of a file, this can be hosted for free (e.g. GitHub Pages) — just ask and it can be set up.

Once it's open in your phone's browser, use the browser's **"Add to Home Screen"** option (Share button → Add to Home Screen on iPhone; ⋮ menu → Add to Home screen on Android). That gives you an app-like icon that opens straight to the tool.

**Important:** all data (roster, games, stats) is saved in that one browser on that one device. It won't sync to another phone or computer. Don't clear your browser data/history for this to keep your season stats.

## How to use it

**Roster tab** — Enter your full season roster once. Tap "Set P" on any girl eligible to pitch.

**Game tab** — Before each game: pick the date/opponent/# of innings, check off who's available today, then set who pitches each inning (only eligible pitchers show up as options). Tap **Generate Fielding Lineup** — this randomizes everyone else into the remaining positions and bench, weighted by each girl's own season history so it balances out over time.

**Field tab** — Shows every inning. Tap any position to swap who's playing it (works for swapping with the bench too). If someone gets hurt or has to leave, mark her "Out" and it'll offer to reshuffle the *remaining* innings only — everything already played stays as-is. A late arrival can be added the same way. "Next ▶" advances the current-inning marker as the real game progresses.

**Batting tab** — Generate a random batting order for today. During the game, tap whichever batter made the last out of the inning — the app highlights who leads off the next inning.

**Stats tab** — Season totals per player: games played, bench innings, and innings at each position (with % of her own playing time), so you can see the balancing at a glance.

## How the balancing works

- **Positions:** each girl is scored per position by *her own* historical percentage of time spent there — lower percentage = more likely to get that spot next, with some randomness mixed in so it's not robotic. A brand-new player with no history is equally likely at anything.
- **Bench:** whoever has been benched the *fewest* times this season is benched first when someone has to sit. The app hard-blocks benching the same girl twice in one game unless it's truly unavoidable (too many bodies, not enough spots) — in that case it warns you on screen.
- **Pitchers** are always set by you, manually, per inning — never randomized. A pitcher who isn't pitching a given inning is treated exactly like everyone else for that inning's fielding/bench assignment.

## Notes

- Default is 6 innings; change it per game as needed.
- "Reset All Data" in the Roster tab wipes everything on this device — only use it to start fresh for a new season.
