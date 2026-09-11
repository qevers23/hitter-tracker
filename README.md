# Mount Marty Hitter Tracker

Pitch-by-pitch tracking for college hitters. A coach taps a zone, a pitch type, and what
happened; the app builds zone heat maps, swing-decision reports, spray charts, and season
profiles from that one stream.

**Live app:** https://qevers23.github.io/hitter-tracker/

## What it does

- 13x13 plate grid with the classic nine-box zone overlaid; ball/strike is derived from the
  tap, so the count is never typed
- Games vs scrimmages tracked separately, with hitter pages defaulting to games only
- Substitutions mid plate appearance, scored the way a scorebook does: the pitches already
  thrown stay with the hitter who saw them, the outcome goes to whoever finished the at-bat
- Two lineups at once for intrasquads
- wOBA, xwOBA (with its measurement coverage always shown), plate discipline, and a
  decision-runs figure that credits the decision rather than the outcome
- Per-hitter game reports, ready to email
- CSV and JSON export, and an importer to move a season between copies

## Setup

This page needs a Supabase project to hold the data. It stores nothing itself.
See `SETUP.md` in the project folder for the walkthrough.

Nothing sensitive lives in this repository: the database URL and public key are entered on
first run and kept in the browser, and access is controlled by a coaches allowlist enforced
by Postgres row-level security.
