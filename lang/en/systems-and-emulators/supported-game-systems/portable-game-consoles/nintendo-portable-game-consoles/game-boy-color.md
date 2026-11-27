---
description: Nintendo
---

# Game Boy Color

<div align="left"><figure><img src="../../../../.gitbook/assets/image (756).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Game Boy Color** is the successor of the Game Boy, released in Japan in October 1998, then in North America and Europe in November 1998. Its screen shows up to 56 colors at once, its processor can run twice as fast and an infrared port lets two consoles exchange data. It also plays all Game Boy games.

There are two kinds of cartridges: **black cartridges**, which also run on Game Boy (in black and white), and **clear cartridges**, for Game Boy Color only. Its games include Pokémon Gold, Silver and Crystal, The Legend of Zelda: Link's Awakening DX and Oracle of Seasons / Ages, Wario Land 3, Shantae, Kirby Tilt 'n' Tumble…

The games are played like Game Boy games: controls, hotkeys and most options are described on the [**Game Boy**](game-boy.md) page. Two-player games over the Game Link cable have their own system, [**Game Boy Color 2 Players**](game-boy-color-2-players.md).

{% embed url="https://en.wikipedia.org/wiki/Game_Boy_Color" %}

## At a glance

<table><thead><tr><th width="219"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\gbc</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gbc .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: gambatte</td></tr><tr><td><strong>BIOS</strong></td><td>None (<code>gbc_bios.bin</code> optional, for the boot screen)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk, jgenesis; Mesen, Mednafen and ares with hotkeys; mGBA from its menu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (except tgbdual and DoubleCherryGB), BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores (except DoubleCherryGB)</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                                       | For whom?       | Strengths                                                                                                 | Limits                                                     |
| ---------------------------------------------- | --------------- | --------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **libretro: gambatte** (default)               | Everyone        | Very accurate and light, color correction, RetroAchievements, netplay.                                    | —                                                          |
| **libretro: tgbdual**                          | Two players     | Made to link two Game Boy Colors: see [**Game Boy Color 2 Players**](game-boy-color-2-players.md).        | No RetroAchievements. No benefit for a single-player game. |
| **libretro: sameboy**                          | Purists         | Very accurate emulation, choice of Game Boy Color revision, several color corrections, RetroAchievements. | —                                                          |
| **libretro: DoubleCherryGB**                   | Multiplayer     | Links up to four consoles (see the [**Game Boy Color 2 Players**](game-boy-color-2-players.md) page).     | No RetroAchievements or netplay.                           |
| **libretro: gearboy**                          | Curious players | Recent emulator, **tilt sensor** (Kirby Tilt 'n' Tumble), RetroAchievements.                              | —                                                          |
| **mesen**                                      | Mesen users     | Mesen 2: accurate emulation, debugging tools, turbo buttons.                                              | No RetroAchievements. Save states with hotkeys.            |
| **jgenesis**                                   | Curious players | Recent multi-system emulator, 60 frames per second mode.                                                  | No RetroAchievements.                                      |
| **mgba** (standalone)                          | mGBA users      | mGBA for Windows: image filters.                                                                          | No RetroAchievements. Save states from the mGBA menu.      |
| **mednafen**                                   | Mednafen users  | Accurate emulation, turbo buttons.                                                                        | No RetroAchievements. Save states with hotkeys.            |
| **ares**                                       | Purists         | Very accurate emulation.                                                                                  | No RetroAchievements. Save states with hotkeys.            |
| **bizhawk: Gambatte**, **GBHawk**, **SameBoy** | BizHawk users   | Three emulations to choose from, RetroAchievements, save states in the RetroBat menu.                     | —                                                          |

**If in doubt, keep libretro: gambatte.**

## BIOS

No file is needed: all emulators start the games without a BIOS.

The Game Boy Color BIOS only shows the original boot screen (animated Game Boy logo). It is used by gambatte and gearboy when **EMULATION > START ORIGINAL BIOS** is enabled, by mGBA (unless **EMULATION > SKIP BIOS** is on) and by BizHawk.

<table><thead><tr><th width="132.75">File</th><th width="210.5">Description</th><th width="69.25">Folder</th><th>md5</th></tr></thead><tbody><tr><td><code>gbc_bios.bin</code></td><td>Game Boy Color BIOS</td><td><code>bios</code></td><td>dbfce9db9deaa2567f6a84fde55f9680</td></tr></tbody></table>

This file is optional and checked by RetroBat.

## Which game format?

<table><thead><tr><th width="177.75">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gbc</strong></td><td>Game Boy Color cartridge image (black or clear cartridge).</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive).</td></tr></tbody></table>

Game Boy games (`.gb`) go in `roms\gb`.

## Controls

RetroBat sets up the controllers automatically. The buttons, the **INVERT FACE BUTTONS** and **REMAP SELECT TO** options and the hotkeys are the same as on the [**Game Boy**](game-boy.md#controls) page.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (757).png" alt="" width="338"><figcaption></figcaption></figure></div>

## Folders

<table><thead><tr><th width="361.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores, Mesen, Mednafen, mGBA: game saves</td><td><code>saves\gbc</code></td></tr><tr><td>libretro cores: save states</td><td><p><code>saves\gbc\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\gbc\libretro.gambatte</code>)</p></td></tr><tr><td>Mesen: save states</td><td><code>saves\gbc\mesen\SaveStates</code></td></tr><tr><td>Mednafen: save states</td><td><code>saves\gbc\mednafen\sstates</code></td></tr><tr><td>mGBA: save states</td><td><code>saves\gbc\mgba\sstates</code></td></tr><tr><td>ares: game saves and save states</td><td><code>saves\gbc\ares</code></td></tr><tr><td>jgenesis: game saves</td><td><code>saves\gbc\jgenesis</code></td></tr><tr><td>BizHawk: game saves</td><td><code>saves\gbc\bizhawk</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>Cheats</td><td><p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\mgba</code> (mGBA)</p><p><code>cheats\jgenesis</code> (jgenesis)</p><p><code>cheats\bizhawk\gbc</code> (BizHawk)</p></td></tr><tr><td>Screenshots</td><td><p><code>screenshots\mesen</code></p><p><code>screenshots\mednafen</code></p><p><code>screenshots\mgba</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\gbc</code></p></td></tr></tbody></table>

## Guides

### Screen colors

The Game Boy Color screen was not backlit: games use very bright colors, which look garish on a modern screen. Several emulators correct them:

| Emulator      | Option                                       | Effect                                                                                                                                                   |
| ------------- | -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| gambatte core | **VISUAL RENDERING > COLOR CORRECTION**      | **GBC ONLY**, **ALWAYS** or **DISABLED**.                                                                                                                |
| sameboy core  | **VISUAL RENDERING > COLOR CORRECTION MODE** | **MODERN BALANCED**, **MODERN ACCURATE**, **MODERN BOOST CONTRAST**, **REDUCE BRIGHTNESS**, **COLOR CORRECT CURVES**, **HARSH REALITY** or **DISABLED**. |
| gearboy core  | **VISUAL RENDERING > COLOR CORRECTION**      | Turns the correction on or off.                                                                                                                          |
| jgenesis      | **VISUAL RENDERING > COLOR CORRECTION**      | **GAMEBOY COLOR LCD**, **GAMEBOY ADVANCE LCD** or **NONE**.                                                                                              |

### Kirby Tilt 'n' Tumble (tilt sensor)

Kirby Tilt 'n' Tumble is played by tilting the console. With the gearboy core, choose what replaces tilting in **CONTROLS > TILT CONTROL**: **ANALOG STICK** (default) or **MOUSE**.

### Game Boy Advance bonuses

A few Game Boy Color games unlock bonuses when run on a Game Boy Advance (like the secret shop of The Legend of Zelda: Oracle of Seasons / Ages). To get them:

<table><thead><tr><th width="201.5">Emulator</th><th>Option</th></tr></thead><tbody><tr><td>gambatte core</td><td><strong>EMULATION > FORCE HARDWARE > GBA</strong></td></tr><tr><td>gearboy core</td><td><strong>EMULATION > FORCE HARDWARE > GBA</strong></td></tr><tr><td>jgenesis</td><td><strong>EMULATION > PRETEND TO BE A GBA</strong></td></tr></tbody></table>

### Other useful options

<table><thead><tr><th width="159.5">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>sameboy core</td><td><strong>EMULATION > GAME BOY MODEL</strong></td><td>Game Boy Color CGB-E (default) or CGB-D, or another model.</td></tr><tr><td>gambatte core</td><td><strong>VISUAL RENDERING > INTERFRAME BLENDING</strong></td><td>Reproduces screen ghosting (transparency by flicker): <strong>ACCURATE</strong> by default.</td></tr><tr><td>jgenesis</td><td><strong>EMULATION > FORCE GB MODE</strong></td><td>Runs a black cartridge in Game Boy mode (black and white).</td></tr><tr><td>jgenesis</td><td><strong>EMULATION > TARGET 60 FPS</strong></td><td>Runs games at 60 frames per second.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="326.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>A <code>.gb</code> game does not show up</td><td>Game Boy games go in <code>roms\gb</code>.</td></tr><tr><td>Colors are too bright</td><td>See <a href="game-boy-color.md#screen-colors"><strong>Screen colors</strong></a>.</td></tr><tr><td>Kirby Tilt 'n' Tumble does not react</td><td>Use the gearboy core: see <a href="game-boy-color.md#kirby-tilt-n-tumble-tilt-sensor"><strong>Kirby Tilt 'n' Tumble</strong></a>.</td></tr><tr><td>The two-player game does not work</td><td>Put the game in <code>roms\gbc2players</code>.</td></tr></tbody></table>
