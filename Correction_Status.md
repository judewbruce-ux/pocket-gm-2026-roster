# Pocket GM 3 — corrected NFL roster

October 21, 2026 review candidate. NFL team assignments use the October 7 snapshot.

## Import links

- [Players](https://raw.githubusercontent.com/judewbruce-ux/pocket-gm-2026-roster/main/PGMRoster_2026_Corrected.json)
- [Staff](https://raw.githubusercontent.com/judewbruce-ux/pocket-gm-2026-roster/main/PGMStaff_2026_Corrected.json)

Use each link in its matching import field in a new save. These files contain 2,731 players and 443 staff. They pass local file checks; import, save/reload and multi-season gameplay are not confirmed.

## Changes

Compared with our original roster: 473 player records changed, including 266 draft prospects;58 staff ages corrected. The latest draft pass includes 253 EA-based skill profiles,71 portrait corrections and 74 development timing repairs. Counts overlap.

NFL skill data uses Madden 27 launch ratings. Draft skill data uses the downloaded official EA College Football Week 6 dataset. Physical attributes map directly; most technical attributes subtract 10 as an estimated college-to-pro adjustment. These are not official Pocket GM ratings. Stored overall ratings are retained; displayed overall and development need game testing.

## Remaining limits

-25 draft prospects lack an unambiguous EA match; their existing estimates remain.
-177 draft portraits were visually reviewed;101 were unavailable. Exact hairstyles are approximate.
-33 exact draft-player birthdays were found, but future-prospect age interpretation remains unverified. Placeholder ages have not been represented as correct.
-Height/weight are unsupported by the player import schema. Separate reference data is provided in Draft_Player_Biography_Reference.json; these measurements are not imported.
-Staff career dates and development semantics have unresolved issues. See Phone_Test_Checklist.md. Default staff remains an option while testing.
-The included draft classes are 2027(246 players) and 2028(32 players). No documented maximum number of future imported classes has been confirmed.
-Contracts are simplified gameplay estimates. Future development, prospect rankings and college-to-pro conversion are estimates. This is not a complete verification of every real-world detail.

## Test

Start a new save, check Bryce Underwood’s portrait and running/passing attributes, inspect several other prospects, then save/reload. Simulate an offseason and check young-player growth and veteran decline. Report the full error text if either import fails. Updating this link does not automatically modify an existing save.

## Sources and credit

- Base player/staff roster: https://github.com/trbletrble 1/pocketgm-rosters
- NFL roster snapshot: https://github.com/nflverse/nflverse-data/releases/tag/rosters
- Madden dataset: https://github.com/zachxwalton/madden-ratings-breakdown
- College skills: https://www.ea.com/games/ea-sports-college-football/ratings
- Player biographies/headshots: official college/team websites, with per-player source records saved in the audit.
- Staff birthdays: official 2025 NFL Record and Fact Book.

Original PGMRoster_2026_Oct07.json remains available. See corrected_validation_report.json and Full_Review_Progress.json for current file-check results and coverage.
