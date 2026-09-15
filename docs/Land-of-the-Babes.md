# Duke Nukem PSX: Land of the Babes modern controls

A Dual Shock controls patch for **Duke Nukem: Land of the Babes (USA),
SLUS-01002** on PlayStation.

## Download

[Duke Nukem Land of the Babes Dual Shock.ppf](../patches/Duke%20Nukem%20Land%20of%20the%20Babes%20Dual%20Shock.ppf)

## Important controller settings

**Custom controls can still override the patched controls. Do not touch the
controller mapping; leave the patched default layout unchanged.** If loading
an older save restores a custom layout, restore the default layout in the
controller screen.

**Press the Analog button on your joypad to enable analog mode.** In DuckStation,
use Analog Controller and enable its analog mode. This patch does not add a
command to force analog mode or change the game's existing vibration behavior.

## Controls

| Input | Action |
| --- | --- |
| D-pad / left stick up and down | Move forward and backward |
| D-pad / left stick left and right | Strafe left and right |
| Right stick left and right | Turn left and right |
| R1 | Shoot / action |
| R2 | Jump / swim / jetpack |
| L2 | Auto target |
| L1 | Look around |
| Cross (X) | Turn around |
| Square | Draw weapon |

Circle and Triangle are unassigned in gameplay. Right-stick vertical movement
and stick clicks are unused. Start and Select retain their existing assignments.
Menu navigation retains the original button mappings; the left stick also
navigates menus. The controller screen shows the new action buttons and D-pad
left/right labels.

Stick directions use the original digital movement and turning speeds, with
a central dead zone (below 96 or above 160 on the 0–255 axis scale). This version
does not add proportional analog movement.

## Applying the PPF

Back up the supported source BIN, then apply
`Duke Nukem Land of the Babes Dual Shock.ppf` with a PPF3-compatible patcher.
Keep its matching CUE. For CHD use, patch the BIN before rebuilding the CHD.
Boot fresh: an old savestate can restore the previous executable and controls.

The PPF includes undo data. Use your patcher's undo operation or restore your
backup to remove it. Other revisions and patch combinations are unverified.

Supported source BIN SHA-256:

```text
4daee214458e02f33b3c2e1c1755fe299c4bc4c047f709ccb07e31fa22a1d332
```

Patched BIN SHA-256:

```text
c86af199233f504866da2646b1cb8181fdb100cf4de2dd876a3e3836426ba020
```

Patch SHA-256:

```text
3e4253f53c1f5037a6265430d50cf8184de4fe9418bd29a82667f606418b8562
```

## Validation

- 5,466 simulated MIPS execution cases passed, covering both ports, stick
  thresholds, button combinations, successive input histories, default-layout
  loading, legacy controller behavior, and safe controller-icon rendering.
- PPF application and undo and repaired sector EDC/ECC passed. Only four
  sectors changed, in the main executable and English text file. All bytes
  outside those sectors match the supported source.
- Applied and read back in DuckStation. The controller screen was visually
  checked with the new mappings, including L2 auto target.
- The user confirmed that the patched gameplay controls work in DuckStation.
- A fresh boot of the generated disc, physical hardware, multiplayer gameplay,
  and memory-card layout persistence have not been tested.

Game images are not included in this repository.
