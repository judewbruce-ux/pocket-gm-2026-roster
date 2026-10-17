# Corrected import candidate — October 17, 2026

Use these separate raw links in Pocket GM 3:

- Players: https://raw.githubusercontent.com/judewbruce-ux/pocket-gm-2026-roster/main/PGMRoster_2026_Corrected.json
- Staff: https://raw.githubusercontent.com/judewbruce-ux/pocket-gm-2026-roster/main/PGMStaff_2026_Corrected.json

209 player records and 58 staff ages corrected. Both files pass structural checks; import, save/reload and multi-season simulation are still untested. See Correction_Status.md for remaining verification, and Phone_Test_Checklist.md for testing steps. This remains the October 7 transaction snapshot, not a live roster. The original file remains available below.

---

# Pocket GM 3 — 2026 NFL import candidate

Target: Pocket GM 3: Football Sim 1.6.2. Built October 11, 2026 from an October 7, 2026 NFL roster snapshot and Madden 27 launch ratings.

## Import

1. Upload `PGMRoster_2026_Oct07.json` to a public GitHub repository.
2. Open the file and select **Raw**. Copy that URL (it should serve JSON without requiring sign-in).
3. In Pocket GM 3, start a **new save**, choose **Import Rosters**, and paste the raw URL.
4. Start at **Regular Season** to keep current players with their teams. Use the game's default staff.
5. Check a few teams, simulate a week, then save and reload. Report any import error or obviously incorrect rating.

This candidate passed local structural checks. It has NOT yet been imported or simulated in the game. Do not overwrite a save you want to keep.

## Included

- All 32 NFL teams; 2,731 total player records, including free agents and inherited future prospects.
- 130 team-assignment updates from the October 7 snapshot.
- 97 missing NFL players added; unsupported long snappers omitted.
- Madden 27 launch-based rating adjustments for 2,080 existing players. Physical attributes map directly; other existing PGM skills use approximate adjustments. Displayed overalls are recalculated by PGM and may differ.
- Potential converted to remaining rating growth, following the original PGM template.
- Simplified contracts for added players and reduced team payrolls where needed to provide cap room. These are gameplay approximations, not real NFL contract figures.

## Limitations

NFL transactions after October 7 are not included. Practice-squad players are treated as free agents. Injured/reserve players remain ordinary roster depth. Added-player appearances and development are template approximations. Unsourced players retain base ratings or documented conservative estimates. Future draft classes are inherited and only lightly normalized; they are not verified scouting projections. Some legacy draft-pick metadata exceeds the old template range and needs an in-game display check. SF has 71 players; the game may require cuts. Some teams have thin DE/OLB depth due to position conventions. Actual salary-cap accounting remains unverified until import.

## Sources and credit

- Base roster: https://github.com/trbletrble1/pocketgm-rosters — adapted, not created from scratch.
- NFL roster snapshot: https://github.com/nflverse/nflverse-data/releases/tag/rosters — roster_2026.csv, asset updated October 7, 2026.
- Madden data: https://github.com/zachxwalton/madden-ratings-breakdown — Madden 27 Launch Ratings, originally sourced from EA.
- PGM import/template reference: https://github.com/PGM21-json/PGM21

Unofficial community adaptation; not endorsed by EA, the NFL, or Pocket GM.
