# Auction War Room

Live draft board for Travis's Super Bowl Challenge (14 teams, half PPR, $200 auction).

Four tabs: Draft Board, Draft Plan, Sleepers, Depth Charts.

## Putting it online

1. Create a **public** repo on GitHub.
2. Upload `index.html`, `config.js` and this file to the root.
3. Repo **Settings > Pages**, set Source to `main` / root, save.
4. Wait a minute. The URL is `https://<your-username>.github.io/<repo-name>/`

Send that link to anyone. No login, works on phones.

## Turning on live sync

Without it, each browser tracks its own draft. With it, a pick logged on one
device appears on every other device in well under a second.

1. console.firebase.google.com, create a project.
2. Build > Realtime Database > Create Database. Choose **test mode**.
3. Project settings > Your apps > Web. Register an app.
4. Copy the config values into `config.js`, uncomment them, commit.

The badge beside the tabs reads "Shared — live" when it's working.

Test mode leaves the database open to anyone who has the URL. For a fantasy
draft that is fine. If you want it locked down, set the database rules to
require a shared secret or an auth token.

## Data behind it

- Prices from 2024 and 2025 auction results in this league, modelled by tier
- Expected points from nine seasons of nflverse play-by-play, scored under league rules
- Consistency labels from 2025 weekly positional finishes
- Strength of schedule from the real 2026 schedule against 2025 defensive EPA
- Team offence from Vegas implied points per game
- Pros, cons and sleepers researched across the fantasy press, Sept 2026
