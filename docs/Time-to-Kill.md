# Duke Nukem PSX: Time to Kill modern controls

A Dual Shock controls patch for **Duke Nukem: Time to Kill (USA), SLUS-00583**
on PlayStation.

## Download

[Duke Nukem Time to Kill Dual Shock.ppf](../patches/Duke%20Nukem%20Time%20to%20Kill%20Dual%20Shock.ppf)

## Important controller settings

**Custom controls can still override the patched controls. Do not touch the
controller mapping; leave the patched default layout unchanged.** A saved custom
layout can replace these assignments when loaded. Restore the default layout
in the controller screen if an older custom layout is active.

**Press the Analog button on your joypad to enable analog mode.** In DuckStation,
select Analog Controller and enable its analog mode. The patch does not add
automatic analog-mode activation.

## Controls

| Input | Action |
| --- | --- |
| D-pad / left stick up and down | Move forward and backward |
| D-pad / left stick left and right | Strafe left and right |
| Right stick left and right | Turn left and right |
| R1 | Shoot / action |
| R2 | Jump / swim / jetpack |
| L2 | Hold to walk |
| L1 | Look around |
| Cross (X) | Turn around |
| Square | Draw weapon |

Circle and Triangle are unassigned in gameplay. Right-stick vertical movement
and stick clicks are unused. Start and Select retain their existing assignments.
Menu navigation retains the original button mappings, and the left stick also
navigates menus.

Stick directions use the game's original digital movement and turning speeds,
with a central dead zone. This patch does not add proportional analog movement.

## Applying the patch

1. Back up your supported game image.
2. Apply the PPF to the **BIN**, using a PPF3-compatible patcher.
3. Keep the matching CUE with the patched BIN. Boot the game fresh.

Old savestates can restore the unpatched executable and controls. For CHD use,
patch the BIN before rebuilding the CHD. The PPF contains undo data; use your
patcher's undo operation or restore your backup to remove it.

Supported source BIN SHA-256:

```text
708c040436c4a8bfe0ef43379e934172d0b94131ee3db47e406767c9d306a8c1
```

Patched BIN SHA-256:

```text
f5804ec2bc678960f3b25d49fd84e4da6931456f6fa560c7deae4ae6f3d02017
```

Patch SHA-256:

```text
ee748f576ca1b35c9bb0ed060ad5578c8a95c52fb4ef4ae22584c108f58f3693
```

Other revisions and patch combinations have not been verified. Game images
are not included in this repository.

## Validation

- 5,466 simulated MIPS execution cases passed, covering controller ports,
  button combinations, stick thresholds, input histories, default-layout
  loading, and controller-icon rendering.
- PPF application and undo, sector EDC/ECC, and preservation of all bytes
  outside the five changed executable sectors were verified.
- The patch was applied to a running DuckStation session. Complete gameplay
  validation and a fresh boot of the generated disc remain to be confirmed.
- Physical hardware, multiplayer gameplay, and memory-card layout persistence
  have not been tested.
