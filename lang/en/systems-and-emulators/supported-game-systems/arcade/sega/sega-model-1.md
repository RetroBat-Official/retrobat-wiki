---
description: Sega
---

# Sega Model 1

<div align="left"><figure><img src="../../../../.gitbook/assets/image (565).png" alt="" width="525"><figcaption></figcaption></figure></div>

## Overview

The **Sega Model 1** is Sega's first 3D arcade board, released in 1992. Designed by Yu Suzuki's AM2 team, it displays flat-shaded, untextured polygons thanks to a NEC V60 CPU and a coprocessor dedicated to geometry calculations.

Only six games were released on Model 1, but they made history: **Virtua Racing** (1992), which popularized 3D in arcades, and **Virtua Fighter** (1993), the first 3D fighting game. They were followed by Star Wars Arcade, Wing War, Virtua Formula (a giant cabinet version of Virtua Racing) and NetMerc, a virtual reality game with a headset. The board was replaced by the Model 2 as early as 1994.

RetroBat offers four emulators: **Keisho** (formerly sm2-emu, an emulator dedicated to Model 1, 2 and 3), **Supermodel**, and **MAME** as a standalone emulator or as a libretro core.

{% embed url="https://en.wikipedia.org/wiki/List_of_Sega_arcade_system_boards#Model_1" %}

## At a glance

<table><thead><tr><th width="239"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\model1</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>Keisho</td></tr><tr><td><strong>BIOS</strong></td><td>None (<code>model1io.zip</code> / <code>model1io2.zip</code> depending on the romset, see BIOS)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, Keisho; Supermodel and MAME with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores (mame)</td></tr><tr><td><strong>Wheels</strong></td><td>Keisho, Supermodel</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="189.5">Emulator</th><th width="307.75">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>Keisho</strong> (default)</td><td>Emulator dedicated to Model 1, 2 and 3, fast, upscaling, CRT filter, force feedback and rumble, save states.</td><td>NetMerc still preliminary (almost no sound).</td></tr><tr><td><strong>supermodel</strong></td><td>Also runs Virtua Fighter and NetMerc, which MAME does not emulate properly yet. Widescreen mode.</td><td>No Virtua Formula. Save states with the keyboard only.</td></tr><tr><td><strong>libretro: mame</strong> / <strong>mame64</strong></td><td>All games, including Virtua Formula.</td><td>Virtua Fighter and NetMerc do not work. Slower.</td></tr></tbody></table>

| Game             | Set                                                | Keisho         | Supermodel    | MAME |
| ---------------- | -------------------------------------------------- | -------------- | ------------- | ---- |
| Virtua Racing    | `vr`                                               | ✅              | ✅             | ✅    |
| Virtua Formula   | `vformula`                                         | ✅              | ❌             | ✅    |
| Virtua Fighter   | `vf`                                               | ✅              | ✅             | ❌    |
| Star Wars Arcade | `swa`, `swaj`                                      | ✅              | ✅             | ✅    |
| Wing War         | `wingwar` (+ `wingwaru`, `wingwarj`, `wingwar360`) | ✅              | ✅ (`wingwar`) | ✅    |
| NetMerc          | `netmerc`                                          | ⚠️ preliminary | ✅             | ❌    |

## BIOS

The Model 1 has no BIOS. The games do use the ROM of their I/O board, stored in a separate archive:

| File            | Games                                                           | Used by                                |
| --------------- | --------------------------------------------------------------- | -------------------------------------- |
| `model1io.zip`  | Virtua Racing, Virtua Formula, Virtua Fighter, Star Wars Arcade | MAME (split or merged romsets), Keisho |
| `model1io2.zip` | Wing War, NetMerc                                               | MAME (split or merged romsets)         |

Put these archives in `roms\model1`, next to the games. With a [**non-merged**](../../../arcade-guide.md#romset-types) MAME romset, they are already included in each game. RetroBat checks them as optional BIOS.

## Which game format should I use?

Games are MAME `.zip` (or `.7z`) archives, to keep compressed and unrenamed.

* Clones (`vformula`, `swaj`, `wingwaru`…) need their parent game (`vr`, `swa`, `wingwar`) in the same folder, except with a non-merged romset.
* Keisho identifies games by their content: a merged archive holding several versions runs the one named like the archive. It looks for the parent game and the `model1io` archives next to the game.

The `.decomp` extension is for PC ports, see the [**Recompilations**](../../others/recomp.md) page.

## Controls

### Automatic configuration

RetroBat automatically configures controllers for all emulators. The **AUTOCONFIGURE CONTROLLERS** option of Keisho and Supermodel keeps your own configuration.

<table><thead><tr><th width="295.25">Cabinet</th><th>Controller</th></tr></thead><tbody><tr><td>Joystick, steering wheel</td><td>Left stick (and D-pad for the joystick)</td></tr><tr><td>Accelerator, brake</td><td>R2, L2</td></tr><tr><td>Gear up / down</td><td>R1 / L1</td></tr><tr><td>View buttons (VR1 to VR4)</td><td>Face buttons (SOUTH, EAST, WEST, NORTH)</td></tr><tr><td>Start, Coin</td><td>START, SELECT</td></tr><tr><td>Service, Test</td><td>L3, R3</td></tr></tbody></table>

**Per game:**

* **Virtua Fighter**: Punch = WEST, Kick = NORTH, Guard = SOUTH.
* **Star Wars Arcade**: laser = WEST (or L2), torpedo = EAST (or R2); the left stick steers the ship. Player 2 is the gunner.
* **Wing War**: the left stick is the flight stick; pulling the right stick back or pressing L2 slows down; the D-pad changes the view. With Supermodel, R1 and L1 move the throttle up and down.
* **Virtua Racing**, **Virtua Formula**: view buttons on the four face buttons, gears on L1 / R1. With Supermodel, the **CONTROLS > USE SHOULDER BUTTONS FOR RACING GAMES** option puts the accelerator and brake on R1 / L1, and the gears on the D-pad.

**CONTROLLER LAYOUT** (Keisho, Supermodel) adapts the buttons to arcade sticks (modern8, 8alternative, 6alternative). For more details on arcade layouts, see the [**Arcade Guide**](../../../arcade-guide.md) page.

The buttons of each game are set in the `keisho.yml` and `supermodel.yml` files (`system\resources\inputmapping`), which you can copy to `user\inputmapping` to change them. For more details on `keisho.yml`, see the [**Keisho controller mapping**](../../../../controllers/specific_mapping/keisho-controller-mapping.md) page.

### Wheels

Keisho and Supermodel support wheels, with the **WHEELS > ENABLE WHEEL** option, for Virtua Racing and Virtua Formula.

* Keisho: **ENABLE FORCE FEEDBACK** and **FORCE FEEDBACK STRENGTH** for the drive board force feedback. Steering and pedals are detected by Keisho; the buttons are set per wheel type in `keisho_wheels.yml` (editable copy in `user\inputmapping`), and a wheel missing from the file keeps the buttons set in the Keisho menu.
* Supermodel: **ENABLE FORCE FEEDBACK**.

For more details on wheels, see the [**Wheels**](../../../../controllers/supported-controllers/wheels.md) page.

### Hotkeys

**Keisho**

| Hotkey             | Action                     | Keyboard  |
| ------------------ | -------------------------- | --------- |
| **HOTKEY + START** | Exit                       | ESC       |
| **HOTKEY + SOUTH** | Keisho menu                | F1        |
| **HOTKEY + WEST**  | Save state                 | F2        |
| **HOTKEY + NORTH** | Load state                 | F4        |
| **HOTKEY + LEFT**  | Rewind (**REWIND** option) | BACKSPACE |
| **HOTKEY + RIGHT** | Fast forward               | L         |
| **L3** / **R3**    | Service / Test             | 9 / 0     |
| —                  | Screenshot                 | F8        |
| —                  | Pause                      | P         |
| —                  | Fullscreen                 | F         |

In Virtua Racing and Virtua Formula, F1 to F5 shift gears on the keyboard: the menu moves to F10, save to F6 and load to F7. The controller hotkeys follow automatically. Keyboard keys can be customized, see the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

**Supermodel**

| Hotkey             | Action                                          | Keyboard     |
| ------------------ | ----------------------------------------------- | ------------ |
| **HOTKEY + START** | Exit                                            | ESC          |
| **L3** / **R3**    | Service / Test (**ENABLE SERVICE MENU** option) | 9 / 0        |
| —                  | Save state / change slot / load state           | F5 / F6 / F7 |
| —                  | Pause                                           | ALT + P      |
| —                  | Reset                                           | ALT + R      |
| —                  | Screenshot                                      | ALT + S      |
| —                  | Fullscreen                                      | ALT + ENTER  |
| —                  | Clear NVRAM                                     | ALT + N      |

**MAME and libretro mame core**: see the [**MAME**](../mame.md) page.

## Folders

| Content                                      | Folder                                                                                              |
| -------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| I/O board archives                           | `roms\model1`                                                                                       |
| Keisho: NVRAM (cabinet settings and records) | `saves\model1\keisho`                                                                               |
| Keisho: save states (managed by RetroBat)    | `saves\model1\keisho\sstates`                                                                       |
| Keisho: save states (emulator folder)        | `saves\model1\keisho\states`                                                                        |
| Keisho: screenshots                          | `screenshots\keisho`                                                                                |
| Keisho: configuration                        | `emulators\keisho\keisho.ini`                                                                       |
| Keisho: wheel buttons                        | `system\resources\inputmapping\wheels\keisho_wheels.yml` (editable copy in `user\inputmapping`)     |
| Supermodel: configuration                    | `emulators\supermodel\Config\Supermodel.ini`                                                        |
| Supermodel: NVRAM                            | `emulators\supermodel\NVRAM`                                                                        |
| Supermodel: save states                      | `emulators\supermodel\Saves`                                                                        |
| Per-game button mapping                      | `system\resources\inputmapping\keisho.yml`, `supermodel.yml` (editable copy in `user\inputmapping`) |

For the MAME folders, see the [**MAME**](../mame.md) page.

## Guides

### Other useful options

**Keisho**

<table><thead><tr><th width="330.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Increases the rendering resolution (Vulkan and OpenGL).</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>4/3 by default, like the arcade monitor (the bezel is only shown in 4/3). 16/9 widens the 3D view.</td></tr><tr><td><strong>VISUAL RENDERING > CRT FILTER</strong></td><td>Arcade monitor look: scanlines, shadow mask, glow.</td></tr><tr><td><strong>VISUAL RENDERING > TRANSLUCENCY</strong></td><td><strong>BLENDED</strong>: smooth transparency instead of the cabinet checkerboard (Vulkan and OpenGL).</td></tr><tr><td><strong>VISUAL RENDERING > ADJUST BRIGHTNESS</strong></td><td>Black level of the picture (50% by default, matched to an arcade capture).</td></tr><tr><td><strong>EMULATION > REWIND</strong></td><td>Enables rewind (<strong>HOTKEY + LEFT</strong>).</td></tr><tr><td><strong>CONTROLS > ENABLE RUMBLE</strong></td><td>Controller rumble in driving games.</td></tr></tbody></table>

**Supermodel**

<table><thead><tr><th width="335.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>VIDEO > WIDESCREEN HACK</strong></td><td>Displays games in 16/9.</td></tr><tr><td><strong>EMULATION > HIGH LEVEL GEOMETRIZER</strong></td><td>On by default (fast). Off, Supermodel runs the real geometry programs, more accurate but slower.</td></tr><tr><td><strong>VISUAL RENDERING > SUPERSAMPLING</strong></td><td>Smooths the picture (SSAA), at the cost of performance.</td></tr></tbody></table>

## Known issues

| Issue                                            | Solution                                                                                        |
| ------------------------------------------------ | ----------------------------------------------------------------------------------------------- |
| Virtua Fighter or NetMerc do not start with MAME | MAME does not emulate them yet: use Keisho or Supermodel (NetMerc: Supermodel).                 |
| Virtua Formula does not start with Supermodel    | Supermodel does not support this game: use Keisho or MAME.                                      |
| A game does not start with MAME (missing file)   | Add `model1io.zip` or `model1io2.zip` to `roms\model1`, and the parent game for a clone.        |
| Star Wars Arcade player 2 does nothing           | It is the gunner: a second controller is needed.                                                |
| Buttons do not match the cabinet                 | Select a **CONTROLLER LAYOUT**, or edit `keisho.yml` / `supermodel.yml` in `user\inputmapping`. |
