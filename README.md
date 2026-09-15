# Duke Nukem PSX: Time to Kill and Land of the Babes modern controls

Dual Shock controls patches for **Duke Nukem: Time to Kill (USA), SLUS-00583**
and **Duke Nukem: Land of the Babes (USA), SLUS-01002** on PlayStation.

## Downloads

- [Time to Kill Dual Shock patch](patches/Duke%20Nukem%20Time%20to%20Kill%20Dual%20Shock.ppf)
  — [instructions, supported image hashes and validation](docs/Time-to-Kill.md).
- [Land of the Babes Dual Shock patch](patches/Duke%20Nukem%20Land%20of%20the%20Babes%20Dual%20Shock.ppf)
  — [instructions, supported image hashes and validation](docs/Land-of-the-Babes.md).

Use the patch matching your game. These are separate patches for separate images.

## Important controller settings

**Custom controls can still override the patched controls. Do not touch the
controller mapping; leave the patched default layout unchanged.** A saved custom
layout can replace these assignments when loaded. Restore the default layout
in the controller screen if an older custom layout is active.

**Press the Analog button on your joypad to enable analog mode.** Analog mode
is not activated automatically by these patches. In DuckStation, select Analog
Controller and enable its analog mode.

## Controls

Both games use the same layout except for L2:

| Input | Action |
| --- | --- |
| D-pad / left stick up and down | Move forward and backward |
| D-pad / left stick left and right | Strafe left and right |
| Right stick left and right | Turn left and right |
| R1 | Shoot / action |
| R2 | Jump / swim / jetpack |
| L2 — Time to Kill | Hold to walk |
| L2 — Land of the Babes | Auto target |
| L1 | Look around |
| Cross (X) | Turn around |
| Square | Draw weapon |

Circle and Triangle are unassigned in gameplay. Right-stick vertical movement
and stick clicks are unused. Start and Select retain their existing assignments.
Menu navigation retains the original button mappings, and the left stick also
navigates menus.

Stick directions use the games' original digital movement and turning speeds,
with a central dead zone. These patches do not add proportional analog movement.

## Applying a patch

1. Check the supported source-image hash in the instructions for your game.
2. Back up the BIN and apply the matching PPF with a PPF3-compatible patcher.
3. Keep the matching CUE with the patched BIN and boot the game fresh.

Old savestates can restore the unpatched executable and controls. For CHD use,
patch the BIN before rebuilding the CHD. Both PPFs contain undo data; use your
patcher's undo operation or restore your backup to remove a patch.

Other revisions and patch combinations have not been verified. Game images
are not included in this repository.

## Validation

Each patch passed 5,466 simulated MIPS execution cases, plus PPF application,
undo and sector EDC/ECC checks. Both were applied in DuckStation, and the user
confirmed that the Land of the Babes gameplay controls work. See each game's
instructions for its detailed validation status and remaining testing limits.
