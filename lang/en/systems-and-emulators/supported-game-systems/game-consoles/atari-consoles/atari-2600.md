---
description: Atari
---

# Atari 2600

<div align="left"><figure><img src="../../../../.gitbook/assets/image (633).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Atari 2600**, first called the **Atari VCS** (Video Computer System), came out in 1977. It was not the first cartridge console, but it made video games popular at home: it sold more than 30 million units and stayed in production until 1992.

Its library has more than 500 games: Adventure, Pitfall!, River Raid, Space Invaders, Pac-Man, Combat, Yars' Revenge, Kaboom!, Missile Command… The console has a one-button joystick, paddles (rotary controllers) and switches on the front: **Reset** (starts the game), **Select** (game mode), left and right **Difficulty** (A or B) and **Color / Black and white**.

{% embed url="https://en.wikipedia.org/wiki/Atari_2600" %}

## At a glance

<table><thead><tr><th width="217.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\atari2600</code></td></tr><tr><td><strong>Extensions</strong></td><td>.a26 .bin .rom .gz .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: stella</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk; Stella with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro stella and stella2014 cores</td></tr><tr><td><strong>Light guns</strong></td><td>stella core</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                       | For whom?     | Strengths                                                                                           | Limits                                          |
| ------------------------------ | ------------- | --------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| **libretro: stella** (default) | Everyone      | Recent Stella: excellent compatibility, paddles, light gun, TV filters, RetroAchievements, netplay. | —                                               |
| **libretro: stella2014**       | Low-end PCs   | Older Stella version, very light. RetroAchievements, netplay.                                       | Less compatible. No TV filters.                 |
| **stella** (standalone)        | Stella users  | Stella in its original version: TV filters, scanlines, autofire, debugger.                          | No RetroAchievements. Save states with hotkeys. |
| **bizhawk: Atari2600Hawk**     | BizHawk users | BizHawk's own emulation, RetroAchievements, save states in the RetroBat menu.                       | Less compatible than Stella.                    |

**If in doubt, keep libretro: stella.**

## BIOS

No BIOS is needed: the Atari 2600 has none.

## Which game format?

Games are cartridge images, `.a26` (or `.bin`, `.rom`), possibly compressed as `.zip` or `.7z` (one game per archive). Emulators recognize the cartridge type (size, bank switching) and the game's controller (joystick, paddles…) from their game database.

## Controls

RetroBat configures controllers automatically. The joystick has a single button. The console switches are on the controller.

<table><thead><tr><th width="159">RetroBat controller</th><th>libretro cores (stella, stella2014)</th><th>stella</th><th>bizhawk</th></tr></thead><tbody><tr><td>D-pad</td><td>Joystick</td><td>Joystick</td><td>Joystick</td></tr><tr><td>SOUTH</td><td>Fire</td><td>Fire</td><td>Fire</td></tr><tr><td>EAST</td><td>—</td><td>Select</td><td>Select</td></tr><tr><td>WEST</td><td>Paddle fire (stella2014)</td><td>Booster Grip button</td><td>—</td></tr><tr><td>NORTH</td><td>—</td><td>Booster Grip 2nd button</td><td>—</td></tr><tr><td>START</td><td>Reset (starts the game)</td><td>Reset (starts the game)</td><td>Reset (starts the game)</td></tr><tr><td>SELECT</td><td>Select</td><td>—</td><td>—</td></tr><tr><td>L1</td><td>Left difficulty A</td><td>Left difficulty (toggle)</td><td>—</td></tr><tr><td>R1</td><td>Right difficulty A</td><td>Right difficulty (toggle)</td><td>—</td></tr><tr><td>L2</td><td>Left difficulty B</td><td>—</td><td>—</td></tr><tr><td>R2</td><td>Right difficulty B</td><td>—</td><td>—</td></tr><tr><td>L3</td><td>Color</td><td>Color / Black and white (toggle)</td><td>—</td></tr><tr><td>R3</td><td>Black and white</td><td>—</td><td>—</td></tr></tbody></table>

With Stella and BizHawk, the controller's SELECT button is used for hotkeys: the console's Select switch is on EAST.

Both Stella versions recognize paddles and driving controllers automatically: play with the left stick or the mouse. With standalone Stella, **CONTROLS > USE MOUSE AS CONTROLLER** sets mouse use.

### Hotkeys

libretro cores use the standard RetroArch hotkeys. BizHawk uses the common RetroBat hotkeys. Standalone Stella uses the common hotkeys too: HOTKEY + SOUTH opens the options menu, HOTKEY + WEST / NORTH saves / loads, HOTKEY + up / down changes the slot, HOTKEY + R3 takes a screenshot and HOTKEY + L3 toggles fullscreen. See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

### Light guns

The stella core supports the Atari light gun (XG-1) for the few games that use it (Sentinel, Shooting Arcade…). Turn on **GUNS > ENABLE GUN** (link to add to the **Gun controls** page). **GUNS > SHOW CROSSHAIR** shows the crosshair.

## Folders

<table><thead><tr><th width="259">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\atari2600</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\atari2600\libretro.&#x3C;core></code></td></tr><tr><td>Stella: save states</td><td><code>emulators\stella\state</code></td></tr><tr><td>Stella: configuration</td><td><code>emulators\stella\stella.sqlite3</code></td></tr><tr><td>Stella: screenshots</td><td><code>screenshots\stella</code></td></tr><tr><td>BizHawk: save states</td><td><code>saves\atari2600\bizhawk\sstates\Atari2600Hawk</code></td></tr><tr><td>BizHawk: screenshots</td><td><code>screenshots\bizhawk\atari2600</code></td></tr></tbody></table>

## Guides

### Starting a game

On the real console, the game starts with the **Reset** switch: press START. The **Select** switch chooses the game mode (number of players, variant) before starting. Most games have dozens of modes: the game manual describes them.

### Difficulty

The difficulty switches (A = hard, B = easy) change the game: paddle size, enemy speed… In a few games, the left switch (player 1) is essential.

* libretro cores: L1 / L2 (left A / B), R1 / R2 (right A / B).
* Stella: L1 and R1 toggle between A and B.
* BizHawk: **EMULATION > DIFFICULTY SWITCH** (**BEGINNER** or **ADVANCED**), for both switches.

### RetroAchievements

The stella and stella2014 cores and BizHawk are compatible. For more details, see the [**RetroAchievements**](../../../../advanced-features/retroachievements.md) page.

### Other useful options

<table><thead><tr><th width="153.25">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>stella core</td><td><strong>EMULATION > VIDEO FORMAT</strong></td><td>Forces NTSC, PAL, SECAM… (automatic by default).</td></tr><tr><td>stella core</td><td><strong>VISUAL RENDERING > TV EFFECTS</strong></td><td>Composite, S-Video, RGB rendering…</td></tr><tr><td>stella core</td><td><strong>VISUAL RENDERING > PHOSPHOR MODE</strong></td><td>Blends frames to remove the flicker of some games.</td></tr><tr><td>stella core</td><td><strong>VIDEO > CROP OVERSCAN</strong></td><td>Hides the black borders.</td></tr><tr><td>stella2014 core</td><td><strong>VISUAL RENDERING > INTERFRAME BLENDING</strong></td><td>Reduces flicker.</td></tr><tr><td>stella</td><td><strong>VISUAL RENDERING > VIDEO FILTER</strong>, <strong>SCANLINES INTENSITY</strong></td><td>TV filters and scanlines.</td></tr><tr><td>stella</td><td><strong>CONTROLS > AUTOFIRE</strong></td><td>Autofire, from 5 to 30 shots per second.</td></tr><tr><td>stella</td><td><strong>EMULATION > SAVE ON EXIT</strong></td><td>Saves the game when quitting and reloads it at the next launch.</td></tr></tbody></table>

## Known issues

| Issue                                      | Solution                                                                                                                                               |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| The game stays on the title screen         | Press START (Reset).                                                                                                                                   |
| The game flickers                          | **PHOSPHOR MODE** (stella core) or **INTERFRAME BLENDING** (stella2014 core). Some games draw their objects every other frame, as on the real console. |
| A paddle game is unplayable with the D-pad | Use the left stick or the mouse.                                                                                                                       |
| The game is too hard or too easy           | Change the difficulty switches (see [**Difficulty**](atari-2600.md#difficulty)).                                                                       |
