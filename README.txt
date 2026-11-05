FATAL LABYRINTH: REBALANCED
v1.0 FINAL
Sega Genesis / Mega Drive
Modified by RetchERezzed

SUMMARY
Rebalanced edition of the original Fatal Labyrinth with targeted combat, loot, bow, navigation and enemy-status corrections
Preserves the original 31-floor campaign, core controls and classic gameplay
The Trunadai action-table correction now enables its native paralysis spell, including the existing recovery protection

FEATURES
- Inherited combat, equipment, loot, food and damage-display corrections
- Equipped bows fire automatically through the game's normal directional attack when a target is present
- No B+C attack combination and no infinite bow ammunition
- Visible, explored-context clues for secret doors, pits and alarm tiles
- Normal A-button hidden-door interaction retained
- Enemy sleep and paralysis recovery protection
- Confusion recovery and enemy-forced teleport cooldown
- Original map templates, core gameplay, inventory and regional modes preserved
- Native Trunadai paralysis casting restored by a guarded two-byte action-table correction

CHANGELOG
v1.0 Final | 2026-11-05
- Restored native Trunadai paralysis casting by correcting its existing action table at ROM offsets A103 and A105
- Verified natural Trunadai paralysis application, expiration and patched recovery grace
- Verified sequential native Trunadai paralysis, Green Bar sleep and Necromancer confusion recovery in a debug-staged session
- Retested Gogon teleport cooldown with simultaneous confusion and full recovery
- Retested floor-30 death and Continue to floor 25 with the native checkpoint properly established
- Passed 62 of 62 dungeon-generation cases, 60 of 60 directional bow and control cases, and 6 of 6 reset cases

Pre-release QA features included in v1.0
- Rebalanced combat, equipment, loot, food and damage display
- Added automatic directional bow attacks using the existing controls and finite ammunition
- Made secret doors, pits and alarms discoverable with visible explored-context clues
- Added status recovery protection and enemy-forced teleport cooldown
- Preserved the 31-floor campaign, regional modes and original core controls

Note: Earlier QA identifiers refer to development builds, not separate public versions

INSTALLATION
1  Obtain your own unmodified Fatal Labyrinth (USA, Europe) Genesis ROM matching the ORIGINAL ROM checksums below
2  Extract Fatal_Labyrinth_Rebalanced_v1_0.bps from this ZIP
3  Open a compatible BPS patching tool and select the BPS patch and the exact ORIGINAL ROM
4  Apply the patch directly to that original ROM and save the patched output
5  Open the resulting ROM in a Genesis / Mega Drive emulator
6  Check the PATCHED ROM hashes below if your patcher or checksum utility supports them

IMPORTANT
- Apply this BPS directly to the original ROM, not to QA20, QA37, QA41 or any other modified ROM
- The patch is not a complete game and does not contain a copyrighted ROM
- A different region or byte order is not guaranteed to work

CONTROLS
- Direction pad: move or choose attack direction
- Directional attack: automatically fires the equipped bow at a valid target, otherwise uses normal game behavior
- A: original search, pickup and contextual actions including hidden doors
- B + direction: face without moving as in the original game
- C: original menu
- No new mandatory button combination is required for bow use

ORIGINAL ROM REQUIRED
Title: Fatal Labyrinth (USA, Europe), linear .md or .bin format
Size: 131072 bytes
CRC32: 5F0BD984
SHA256: 671782a5b25d7abac07e084a7efe0d02a1248f5fb894713a34b3f8b05d637695

PATCHED ROM OUTPUT
Size: 262144 bytes
CRC32: 0ED4B48F
SHA256: 50de8c7e1cd6afa0ce8ccb70211904165f27802113ec4815170fb85d5bcbd016
Genesis checksum: 50BC

BPS PATCH
Filename: Fatal_Labyrinth_Rebalanced_v1_0.bps
Size: 3066 bytes
CRC32: 2144DF1C
SHA256: cbdf036da273bbd93b39d7ddb1a4176991ad1c26aaf5be23600367cc8eedd68c

VERIFICATION SUMMARY
- Independent QA37 rebuild reproduced its ROM and hash exactly before applying the final correction
- Final ROM differs from QA37 / QA41 at only offsets A103 and A105
- Genuine floor-30 fatal hit and Continue to floor 25 passed with the checkpoint correctly established
- Native Trunadai paralysis casting and complete recovery passed in deterministic Genesis Plus GX fixtures
- Sequential naturally cast paralysis, sleep and confusion effects expired in one staged test session
- Gogon native teleport and confusion overlap and recovery passed using two tested seeds
- Map and monster-generation regression 62 of 62 cases passed
- Bow and control regression 60 of 60 U and J cases passed, including fresh isolated 30-case runs per region
- Reset counter clearing 6 of 6 cases passed
- BlastEm 68000 watchpoints captured intended recovery counter writers; original-ROM watched actions had no foreign writes
- Original-ROM two-marker sentinel test passed 62 of 62 cases across 31 staged floor generations
- BPS reconstructed the expected ROM with correct CRC32 and SHA256
- Wrong-source and corrupted-BPS negative controls rejected

TEST COVERAGE LIMITS
- Deterministic tests used developer savestates, debug-staged floors, and safe player HP / food maintenance
- The status chain was sequential, not a simultaneous three-caster room encounter
- Direct 68000 operand inventory and bounded BlastEm bus watches were checked, but not every possible indirect or bulk write on every unvisited path
- These tests do not certify an uninterrupted full 31-floor campaign, a measured win rate, or physical Genesis hardware
- All testing statements describe actual recorded test cases, not inferred full-game behavior

CREDITS
Modified by RetchERezzed
