---
description: Sega
---

# Game Gear

<div align="left"><figure><img src="../../../../.gitbook/assets/image (747).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Game Gear** is Sega's 8-bit handheld console, released in Japan in October 1990, then in North America and Europe in 1991. It reuses the Master System hardware with a backlit color screen, a richer palette and a landscape controller layout. The **Gear-to-Gear** cable links two consoles.

Its library includes Sonic the Hedgehog, Sonic Triple Trouble, Columns, The G.G. Shinobi, Shining Force: The Sword of Hajya, Defenders of Oasis, Ristar… The Master Gear Converter also let it play Master System cartridges: these games go in `roms\mastersystem`.

{% embed url="https://en.wikipedia.org/wiki/Game_Gear" %}

## At a glance

<table><thead><tr><th width="244"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\gamegear</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gg .bin .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: genesis_plus_gx</td></tr><tr><td><strong>BIOS</strong></td><td>None (<code>bios.gg</code> optional)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk, jgenesis, BlastEm; Mednafen and ares with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                                  | For whom?       | Strengths                                                     | Limits                                          |
| ----------------------------------------- | --------------- | ------------------------------------------------------------- | ----------------------------------------------- |
| **libretro: genesis\_plus\_gx** (default) | Everyone        | Very accurate, LCD screen filter, RetroAchievements, netplay. | —                                               |
| **libretro: picodrive**                   | Low-end PCs     | Fast.                                                         | Few options.                                    |
| **libretro: gearsystem**                  | Everyone        | Accurate, two-player games over the Gear-to-Gear cable.       | —                                               |
| **libretro: fbneo**                       | FBNeo users     | Games in the FBNeo format.                                    | Games must follow the FBNeo romset names.       |
| **jgenesis**                              | Curious players | Recent and accurate multi-system emulator.                    | No RetroAchievements.                           |
| **blastem**                               | BlastEm users   | Accurate Mega Drive emulator, with a Game Gear mode.          | No RetroAchievements.                           |
| **mednafen**                              | Mednafen users  | Solid emulation.                                              | No RetroAchievements. Save states with hotkeys. |
| **ares**                                  | Purists         | Very accurate emulation, faithful LCD screen rendering.       | No RetroAchievements. Save states with hotkeys. |
| **bizhawk: SMSHawk**                      | BizHawk users   | RetroAchievements, save states in the RetroBat menu.          | —                                               |

**If in doubt, keep libretro: genesis\_plus\_gx.**

## BIOS

The Game Gear does not need a BIOS: all emulators start games without it. The original BIOS shows the Sega license screen at startup.

<table><thead><tr><th width="93">File</th><th width="261.75">Description</th><th width="87.75">Folder</th><th>md5</th></tr></thead><tbody><tr><td><code>bios.gg</code></td><td>Game Gear BIOS (genesis_plus_gx, gearsystem)</td><td><code>bios</code></td><td>672e104c3be3a238301aceffc3b23fd6</td></tr></tbody></table>

This file is optional and checked by RetroBat. To boot on the BIOS, choose **EMULATION > START ORIGINAL BIOS** (genesis\_plus\_gx) or **EMULATION > ENABLE BIOS** (gearsystem).

## Which game format?

<table><thead><tr><th width="134">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gg</strong></td><td>Game Gear cartridge image.</td></tr><tr><td><strong>.bin</strong></td><td>Same content as a <code>.gg</code>, with another extension.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive). With fbneo: romset in the FBNeo format.</td></tr></tbody></table>

## Controls

RetroBat sets up the controllers automatically for all emulators. The Game Gear has two buttons, **1** and **2**, and a **START** button:

<table><thead><tr><th width="210.25">RetroBat controller</th><th>Game Gear</th></tr></thead><tbody><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>SOUTH</td><td>1</td></tr><tr><td>EAST</td><td>2</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (749).png" alt="" width="338"><figcaption></figcaption></figure></div>

To put buttons 1 and 2 on WEST and SOUTH, enable **CONTROLS > ROTATE BUTTONS** (genesis\_plus\_gx, picodrive and gearsystem cores, BlastEm, ares):

<table><thead><tr><th width="270.25">RetroBat controller</th><th>Game Gear</th></tr></thead><tbody><tr><td>WEST</td><td>1</td></tr><tr><td>SOUTH</td><td>2</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (748).png" alt="" width="338"><figcaption></figcaption></figure></div>

### Hotkeys

libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

Mednafen, ares, jgenesis and BizHawk use the RetroBat hotkeys:

| Action               | Controller         | Keyboard    |
| -------------------- | ------------------ | ----------- |
| Exit                 | HOTKEY + START     | `Esc`       |
| Pause                | HOTKEY + SOUTH     | `P`         |
| Save state           | HOTKEY + WEST      | `F2`        |
| Load state           | HOTKEY + NORTH     | `F4`        |
| Previous / next slot | HOTKEY + Down / Up | `F6` / `F7` |
| Rewind (if enabled)  | HOTKEY + Left      | `Backspace` |
| Fast forward (hold)  | HOTKEY + Right     | `L`         |
| Screenshot           | HOTKEY + R3        | `F8`        |
| Fullscreen           | HOTKEY + L3        | `F`         |

jgenesis has no screenshot hotkey.

BlastEm has its own hotkeys:

| Action                | Controller            | Keyboard          |
| --------------------- | --------------------- | ----------------- |
| Exit                  | HOTKEY + START        | `Esc`             |
| BlastEm menu          | HOTKEY + SOUTH        | `F1`              |
| Pause                 | HOTKEY + L3           | `P`               |
| Save state            | HOTKEY + WEST         | `F2`              |
| Load state            | HOTKEY + NORTH        | `F4`              |
| Slower / faster speed | HOTKEY + Left / Right | `Backspace` / `L` |
| Screenshot            | HOTKEY + R3           | `F8`              |

## Folders

<table><thead><tr><th width="325.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores, Mednafen: game saves</td><td><code>saves\gamegear</code></td></tr><tr><td>libretro cores: save states</td><td><p><code>saves\gamegear\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\gamegear\libretro.genesis_plus_gx</code>)</p></td></tr><tr><td>Mednafen: save states</td><td><code>saves\gamegear\mednafen\sstates</code></td></tr><tr><td>ares: game saves and save states</td><td><code>saves\gamegear\ares</code></td></tr><tr><td>BlastEm: game saves and save states</td><td><code>saves\gamegear\blastem\&#x3C;game name></code></td></tr><tr><td>jgenesis: game saves</td><td><code>saves\gamegear\jgenesis</code></td></tr><tr><td>BizHawk: game saves</td><td><code>saves\gamegear\bizhawk</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>Cheats</td><td><p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\jgenesis</code> (jgenesis)</p><p><code>cheats\bizhawk\gamegear</code> (BizHawk)</p></td></tr><tr><td>Screenshots</td><td><p><code>screenshots\mednafen</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\gamegear</code></p><p><code>screenshots</code> (BlastEm)</p></td></tr></tbody></table>

## Guides

### LCD screen

The Game Gear screen left a trail behind moving objects. Some games use it to fake transparency by making objects flicker.

<table><thead><tr><th width="194.5">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>genesis_plus_gx core</td><td><strong>VIDEO > LCD GHOSTING FILTER</strong></td><td>Mimics the ghosting of the original screen.</td></tr><tr><td>ares</td><td><strong>VISUAL RENDERING > INTERFRAME BLENDING</strong></td><td>Mimics the screen transparency (with a slight motion blur).</td></tr><tr><td>ares</td><td><strong>VISUAL RENDERING > ACCURATE COLOR EMULATION</strong></td><td>Colors of the original screen.</td></tr><tr><td>jgenesis</td><td><strong>GAME ASPECT RATIO > GAMEGEAR LCD</strong></td><td>Proportions of the original screen (default).</td></tr></tbody></table>

### Two-player games (Gear-to-Gear cable)

The gearsystem core links two Game Gears side by side, with the same game on both consoles (Columns, Super Monaco GP, Sonic Drift 2…):

1. Choose the gearsystem core for the game.
2. Enable **EMULATION > 2 PLAYERS (LINK CABLE)**.
3. Choose the layout in **VIDEO > SCREEN LAYOUT POSITIONING**: **LEFT TO RIGHT** (default) or **TOP TO BOTTOM**.

Controller 1 controls the first screen, controller 2 the second one. Bezels are turned off in this mode: the picture is too wide.

### Other useful options

| Emulator                                      | Option                       | Effect                                                   |
| --------------------------------------------- | ---------------------------- | -------------------------------------------------------- |
| genesis\_plus\_gx, gearsystem cores, jgenesis | **NO SPRITE LIMIT**          | Removes flicker when many objects are on screen.         |
| gearsystem core                               | **EMULATION > FORCE REGION** | Japanese, export or international Game Gear.             |
| gearsystem core                               | **EMULATION > FORCE SYSTEM** | Runs the game as on a Game Gear, whatever its extension. |

## Known issues

<table><thead><tr><th width="337.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Objects leave a trail or the picture is blurry</td><td>Turn off <strong>LCD GHOSTING FILTER</strong> (genesis_plus_gx) or <strong>INTERFRAME BLENDING</strong> (ares).</td></tr><tr><td>The two-player game does not work</td><td>Use the gearsystem core and enable <strong>2 PLAYERS (LINK CABLE)</strong>.</td></tr><tr><td>A game does not start with fbneo</td><td>fbneo only reads romsets in the FBNeo format: use genesis_plus_gx.</td></tr><tr><td>A Master System game (<code>.sms</code>) does not show up</td><td>Master System games go in <code>roms\mastersystem</code>.</td></tr></tbody></table>
