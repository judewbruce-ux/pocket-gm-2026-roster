# Correction candidate — October 17, 2026

These are local candidates, not yet published or tested in Pocket GM 3.

- Player import: `PGMRoster_2026_Corrected.json` (2,731 players).
- Staff import: `PGMStaff_2026_Corrected.json` (443 staff; 58 ages corrected from explicit birth dates in the official 2025 NFL fact book).
- Keep player and staff imports separate. A player file in the staff import field produces the missing `role` error.

## Applied corrections

209 players changed across 587 fields: 417 Madden-based skill corrections, 31 fields restored after two incorrect namesake matches, 15 corroborated ages, 25 portrait skin-tone corrections based on NFL headshots, and 99 development fields across the 97 added players.

Ages use September 1, 2026 as a consistent provisional season-start anchor. Madden data is the downloaded Madden 27 launch dataset, not current weekly ratings. The roster transaction snapshot is October 7, not a verified October 17 roster.

Development curves for added players were regenerated after age edits. These are estimates derived from the official template's positional retirement profiles. Simulation outcomes and overall-rating recalculation need an in-game check. Staff uses different potential semantics; its skills, potential and growth curves have been preserved pending further verification. The official fact book verified 113 staff birth dates and supported 58 age corrections; 330 staff remain unmatched.

95 added-player headshots were reviewed; ambiguous differences were left alone. Appearance edits concern visible skin tone, not racial identity. The rest of the league has not received a complete individual photo audit. Exact portrait rendering needs an in-game check.

## Remaining work

- Resolve 121 held age proposals; conflicting sources are recorded in `work/audit_2026_10_16/held_age_changes.json`.
- Verify the remaining unmatched staff ages and investigate staff development behavior. Todd Monken was corrected from 51 to 60 using his February 5, 1966 birth date.
- Complete remaining identity/appearance verification. Two added players lack available headshots.
- Height and weight are not supported fields in the current player import schema. Player_Measurements_Reference.json preserves 2,355 source-listed measurements separately; these are not individually verified or imported.
- Finish validation, publish versioned import links, and test both imports in Pocket GM 3.
- Simulate seasons to check rookie growth, veteran decline, and unexpectedly inflated overalls.

Reproducible builder: `work/audit_2026_10_16/build_corrected.py`.
Field-level before/after evidence: `work/audit_2026_10_16/changes.json`.
