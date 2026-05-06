# Data

## Files Tracked in This Repository

| File | Size | Description |
|------|------|-------------|
| `LeagueSchedule25_26.csv` | 183 KB | Official NBA 2025-26 regular season schedule with game dates, home/away teams, arena info |

**Source:** [Kaggle — Historical NBA Data and Player Box Scores](https://www.kaggle.com/datasets/eoinamoore/historical-nba-data-and-player-box-scores?select=LeagueSchedule25_26.csv)

---

## Files NOT Tracked (Too Large for Git)

| File | Size | Description |
|------|------|-------------|
| `pbp2026.csv` | ~76 MB | Play-by-play event data for all 1,230 regular season games (622K rows) |

**Source:** [Kaggle — NBA Play-by-Play Data 1997–2026](https://www.kaggle.com/datasets/szymonjwiak/nba-play-by-play-data-1997-2023)
*(Despite the title, this dataset includes through the 2025-26 season.)*

To reproduce the analysis, download `pbp2026.csv` from the link above and place it in this `data/` directory.

---

## Schema

### `LeagueSchedule25_26.csv`
| Column | Description |
|--------|-------------|
| `gameId` | Unique game identifier (matches `gameid` in pbp2026.csv) |
| `gameDateTimeEst` | Game date and tip-off time (EST) |
| `gameDay` | Day of week |
| `homeTeamId` / `awayTeamId` | NBA team IDs |
| `homeTeamName` / `awayTeamName` | Team names |
| `arenaName`, `arenaCity`, `arenaState` | Venue info |

### `pbp2026.csv`
| Column | Description |
|--------|-------------|
| `gameid` | Unique game identifier |
| `period` | Quarter (1–4, plus OT) |
| `clock` | Time remaining in period (ISO 8601 duration) |
| `h_pts` / `a_pts` | Running score (home / away) |
| `team` | Team abbreviation of the player involved |
| `playerid` | NBA player ID |
| `player` | Player name (abbreviated) |
| `type` | Event type (Made Shot, Missed Shot, Rebound, Turnover, Foul, etc.) |
| `subtype` | Event subtype (Jump Shot, Driving Layup, etc.) |
| `result` | Made / Missed (for shot events) |
| `x`, `y` | Shot coordinates on court |
| `dist` | Shot distance (feet) |
| `desc` | Full play description |
| `season` | Season year (2026) |
