---
description: Coleco
---

# ColecoVision

<div align="left"><figure><img src="../../../.gitbook/assets/image (738).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **ColecoVision** is **Coleco**'s home console, released in 1982. It came with Donkey Kong and offered very faithful arcade conversions for the time. Its controller has a joystick, two side buttons and a 12-key keypad, on which game-specific overlays are slid. Expansion modules add a steering wheel, the Super Action Controller or Atari 2600 games. It was discontinued in 1985.

Its library has about 150 games: Donkey Kong, Zaxxon, Venture, Lady Bug, Mr. Do!, Burgertime, Pitfall II, Q\*bert, Frogger, Turbo, Smurf: Rescue in Gargamel's Castle…

The **Coleco ADAM** computer has its own system in RetroBat (see the [**Coleco Adam**](../home-computer/coleco-adam.md) page).

{% embed url="https://en.wikipedia.org/wiki/ColecoVision" %}

## At a glance

<table><thead><tr><th width="236.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\colecovision</code></td></tr><tr><td><strong>Extensions</strong></td><td>.col .rom .ri .mx1 .mx2 .dsk .ddp .cas .sg .sc .m3u .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: gearcoleco</td></tr><tr><td><strong>BIOS</strong></td><td><code>colecovision.rom</code> (required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk, standalone emulators (hotkeys)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores gearcoleco, jollycv and fbneo</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                           | For whom?     | Strengths                                                                                                                                                                   | Limits                                                            |
| ---------------------------------- | ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| **libretro: gearcoleco** (default) | Everyone      | Very compatible, MegaCart and Activision cartridges, SGM expansion, spinner (Super Action Controller, steering wheel, Roller Controller) with the mouse, RetroAchievements. | —                                                                 |
| **libretro: jollycv**              | JollyCV users | Accurate emulation, palette choice.                                                                                                                                         | —                                                                 |
| **libretro: bluemsx**              | blueMSX users | Emulated keyboard.                                                                                                                                                          | No netplay.                                                       |
| **libretro: fbneo**                | FBNeo users   | Same settings as FBNeo arcade games.                                                                                                                                        | Only `.zip` or `.7z` games named like FBNeo ColecoVision sets.    |
| **openmsx**                        | openMSX users | ColecoVision machine with Super Game Module.                                                                                                                                | BIOS in a separate folder (see [**BIOS**](colecovision.md#bios)). |
| **ares**                           | Purists       | Very accurate emulation.                                                                                                                                                    | Save states with hotkeys.                                         |
| **bizhawk: Coleco**                | BizHawk users | RetroAchievements, save states in the RetroBat menu.                                                                                                                        | —                                                                 |
| **mesen**                          | Mesen users   | Region choice.                                                                                                                                                              | Save states with hotkeys.                                         |

**If in doubt, keep libretro: gearcoleco.**

## BIOS

<table><thead><tr><th width="167.75">File</th><th width="188.5">Folder</th><th width="203.75">MD5</th><th>Used by</th></tr></thead><tbody><tr><td><code>colecovision.rom</code></td><td><code>bios</code></td><td>2c66f5911e5b42b8ebe113403548eee7</td><td>gearcoleco, ares, BizHawk, Mesen</td></tr><tr><td><code>coleco.rom</code></td><td><code>bios</code></td><td>2c66f5911e5b42b8ebe113403548eee7</td><td>jollycv (created by RetroBat from <code>colecovision.rom</code> when missing)</td></tr><tr><td><code>coleco.rom</code></td><td><code>bios\openMSX\share\systemroms</code></td><td>2c66f5911e5b42b8ebe113403548eee7</td><td>openMSX</td></tr><tr><td><code>coleco.zip</code></td><td><code>roms\colecovision</code></td><td>—</td><td>fbneo (BIOS in FBNeo format)</td></tr></tbody></table>

It is the same file under three names. blueMSX uses the BIOS of its machines (`bios\Machines`, provided with RetroBat).

## Which game format?

<table><thead><tr><th width="236.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.col</strong>, <strong>.rom</strong></td><td>Cartridge image. Read by all emulators, except FBNeo.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Compressed game (one game per archive). With fbneo: FBNeo ColecoVision sets only (see the FBNeo game list).</td></tr><tr><td><strong>.ri .mx1 .mx2 .dsk .ddp .cas .sg .sc .m3u</strong></td><td>MSX and SG-1000 formats, read by blueMSX and openMSX.</td></tr></tbody></table>

## Controls

RetroBat sets up controllers automatically for all emulators, for two players. The keypad keys are spread over the controller.

| RetroBat controller                 | gearcoleco           | jollycv                                       |
| ----------------------------------- | -------------------- | --------------------------------------------- |
| D-pad                               | Joystick             | Joystick                                      |
| SOUTH                               | Left button (yellow) | Left button (yellow); with L2: 1; with R2: 5  |
| EAST                                | Right button (red)   | Right button (orange); with L2: 2; with R2: 6 |
| WEST                                | 1                    | Purple; with L2: 3; with R2: 7                |
| NORTH                               | 2                    | Blue; with L2: 4; with R2: 8                  |
| L1                                  | 3                    | Spinner -                                     |
| R1                                  | 4                    | Spinner +                                     |
| L2                                  | 5                    | Shift key 1                                   |
| R2                                  | 6                    | Shift key 2                                   |
| L3                                  | 7                    | —                                             |
| R3                                  | 8                    | —                                             |
| Left stick (horizontal / vertical)  | 0 / 9                | —                                             |
| Right stick (horizontal / vertical) | Blue / Purple        | —                                             |
| START                               | \*                   | #                                             |
| SELECT                              | #                    | \*; with L2: 9; with R2: 0                    |

The purple and blue buttons are used by the Super Action Controller (Super Action Baseball, Football…).

With blueMSX, **CONTROLLER TYPE** chooses the emulated controller or keyboard.

### Hotkeys

libretro cores use the standard RetroArch hotkeys. openMSX, ares, BizHawk and Mesen use the common RetroBat hotkeys. See the [**Hotkeys**](../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="231.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\colecovision</code></td></tr><tr><td>BIOS</td><td><code>bios</code>, <code>bios\openMSX\share\systemroms</code> (openMSX)</td></tr><tr><td>libretro cores: save states</td><td><p><code>saves\colecovision\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\colecovision\libretro.gearcoleco</code>)</p></td></tr><tr><td>BizHawk: save states</td><td><code>saves\colecovision\bizhawk\sstates\Coleco</code></td></tr><tr><td>BizHawk: screenshots</td><td><code>screenshots\bizhawk\colecovision</code></td></tr></tbody></table>

## Guides

### Spinner and steering wheel

With **libretro: gearcoleco**, **CONTROLS > SPINNER SUPPORT** emulates the **SUPER ACTION CONTROLLER**, the **WHEEL CONTROLLER** (Turbo, Destructor) or the **ROLLER CONTROLLER** (Slither) with the mouse. Mouse buttons are the left and right buttons. **SPINNER SENSITIVITY** sets the speed.

### Other useful options

<table><thead><tr><th width="178.25">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>gearcoleco, jollycv</td><td><strong>VIDEO > NO SPRITE LIMIT</strong></td><td>Removes flickering when too many sprites are on a line.</td></tr><tr><td>gearcoleco</td><td><strong>EMULATION > MAPPER</strong></td><td>Forces the cartridge type if a game does not start.</td></tr><tr><td>gearcoleco</td><td><strong>EMULATION > REFRESH RATE</strong></td><td>NTSC (60 Hz) or PAL (50 Hz).</td></tr><tr><td>jollycv</td><td><strong>VISUAL RENDERING > PALETTE</strong></td><td>Colors of the video chip.</td></tr><tr><td>Mesen</td><td><strong>EMULATION > SYSTEM REGION</strong></td><td>NTSC or PAL.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="319">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>Black screen or missing BIOS message</td><td><code>colecovision.rom</code> is missing from <code>bios</code> (see <a href="colecovision.md#bios"><strong>BIOS</strong></a>). For openMSX, copy it as <code>coleco.rom</code> into <code>bios\openMSX\share\systemroms</code>.</td></tr><tr><td>A game does not start with fbneo</td><td>fbneo only reads FBNeo ColecoVision sets, with <code>coleco.zip</code>: use gearcoleco.</td></tr><tr><td>The game waits for a keypad choice (level, number of players)</td><td>Keys 1 to 8 on the controller (see <a href="colecovision.md#controls"><strong>Controls</strong></a>): usually 1 to 4 for one player, 5 to 8 for two.</td></tr></tbody></table>
