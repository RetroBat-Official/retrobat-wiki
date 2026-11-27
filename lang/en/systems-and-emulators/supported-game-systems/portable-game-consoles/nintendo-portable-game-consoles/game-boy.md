---
description: Nintendo
---

# Game Boy

<div align="left"><figure><img src="../../../../.gitbook/assets/image (752).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Game Boy** is Nintendo's handheld console designed by Gunpei Yokoi's team, released in Japan in April 1989, in North America the same year and in Europe in 1990. Its screen shows four shades of green-grey and four AA batteries give it around thirty hours of play. Together with the Game Boy Color, it sold nearly 120 million units.

Bundled with Tetris, it received Super Mario Land, The Legend of Zelda: Link's Awakening, Kirby's Dream Land, Metroid II, Wario Land and above all Pokémon Red and Blue. The **Game Link cable** connects two consoles to play together or trade Pokémon: these games have their own system in RetroBat, [**Game Boy 2 Players**](game-boy-2-players.md). Game Boy Color games and games played on the Super Game Boy also have their own system.

{% embed url="https://en.wikipedia.org/wiki/Game_Boy" %}

## At a glance

<table><thead><tr><th width="229"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\gb</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gb .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: gambatte</td></tr><tr><td><strong>BIOS</strong></td><td>None (<code>gb_bios.bin</code> optional, for the boot screen)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk, jgenesis; Mesen, Mednafen and ares with hotkeys; mGBA from its menu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (except tgbdual and DoubleCherryGB), BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores (except DoubleCherryGB)</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                                       | For whom?       | Strengths                                                                                                                           | Limits                                                     |
| ---------------------------------------------- | --------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| **libretro: gambatte** (default)               | Everyone        | Very accurate and light, many palettes, colorization of games like on Game Boy Color or Super Game Boy, RetroAchievements, netplay. | —                                                          |
| **libretro: mesen-s**                          | Purists         | Accurate Mesen-S emulation.                                                                                                         | Few Game Boy options.                                      |
| **libretro: tgbdual**                          | Two players     | Made to link two Game Boys: see [**Game Boy 2 Players**](game-boy-2-players.md).                                                    | No RetroAchievements. No benefit for a single-player game. |
| **libretro: sameboy**                          | Purists         | Very accurate emulation, choice of model (Game Boy, Game Boy Pocket…), RetroAchievements.                                           | —                                                          |
| **libretro: DoubleCherryGB**                   | Multiplayer     | Links up to four Game Boys (see [**Multiplayer**](game-boy.md#multiplayer)).                                                        | No RetroAchievements or netplay.                           |
| **libretro: gearboy**                          | Curious players | Recent emulator, palettes, sprite limit removal, RetroAchievements.                                                                 | —                                                          |
| **mesen**                                      | Mesen users     | Mesen 2: accurate emulation, debugging tools, turbo buttons.                                                                        | No RetroAchievements. Save states with hotkeys.            |
| **jgenesis**                                   | Curious players | Recent multi-system emulator, 60 frames per second mode.                                                                            | No RetroAchievements.                                      |
| **mgba** (standalone)                          | mGBA users      | mGBA for Windows: image filters.                                                                                                    | No RetroAchievements. Save states from the mGBA menu.      |
| **mednafen**                                   | Mednafen users  | Accurate emulation, turbo buttons.                                                                                                  | No RetroAchievements. Save states with hotkeys.            |
| **ares**                                       | Purists         | Very accurate emulation.                                                                                                            | No RetroAchievements. Save states with hotkeys.            |
| **bizhawk: Gambatte**, **GBHawk**, **SameBoy** | BizHawk users   | Three emulations to choose from, RetroAchievements, save states in the RetroBat menu.                                               | —                                                          |

**If in doubt, keep libretro: gambatte.**

## BIOS

No file is needed: all emulators start the games without a BIOS.

The Game Boy BIOS only shows the original boot screen (the scrolling Nintendo logo). It is used by gambatte and gearboy when **EMULATION > START ORIGINAL BIOS** is enabled, by mGBA (unless **EMULATION > SKIP BIOS** is on) and by BizHawk.

<table><thead><tr><th width="124">File</th><th width="217.25">Description</th><th width="81">Folder</th><th>md5</th></tr></thead><tbody><tr><td><code>gb_bios.bin</code></td><td>Game Boy (DMG) BIOS</td><td><code>bios</code></td><td>32fbbd84168d3482956eb3c5051637f5</td></tr></tbody></table>

This file is optional and checked by RetroBat.

## Which game format?

<table><thead><tr><th width="144">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gb</strong></td><td>Game Boy cartridge image.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive).</td></tr></tbody></table>

Game Boy Color games (`.gbc`), including those that also run on Game Boy (black cartridges), go in `roms\gbc`. To play with the Super Game Boy borders and colors, put the games in `roms\sgb`.

## Controls

RetroBat sets up the controllers automatically for all emulators. The buttons keep their position on the Super Nintendo controller:

<table><thead><tr><th width="209">RetroBat controller</th><th>Game Boy</th></tr></thead><tbody><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>SOUTH</td><td>B</td></tr><tr><td>EAST</td><td>A</td></tr><tr><td>WEST</td><td>TURBO B (gambatte core, Mesen, Mednafen)</td></tr><tr><td>NORTH</td><td>TURBO A (gambatte core, Mesen, Mednafen)</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (755).png" alt="" width="338"><figcaption></figcaption></figure></div>

gambatte core:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (754).png" alt="" width="338"><figcaption></figcaption></figure></div>

Mesen and Mednafen:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (753).png" alt="" width="338"><figcaption></figcaption></figure></div>

Two **CONTROLS** options are available for all emulators (except **REMAP SELECT TO** with BizHawk):

<table><thead><tr><th width="236.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INVERT FACE BUTTONS</strong></td><td>Puts A on SOUTH and B on EAST (Xbox controller letters), turbos included.</td></tr><tr><td><strong>REMAP SELECT TO</strong></td><td>Puts SELECT on another button (L1, R1, L2, R2, L3 or R3), useful when SELECT is also the HOTKEY button.</td></tr></tbody></table>

### Hotkeys

libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

Mesen, Mednafen, ares, jgenesis and BizHawk use the RetroBat hotkeys:

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

jgenesis has no screenshot hotkey. With mGBA, only HOTKEY + START (exit) is set up: save states are made from its menu.

## Folders

| Content                                           | Folder                                                                                                                                                                                     |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| libretro cores, Mesen, Mednafen, mGBA: game saves | `saves\gb`                                                                                                                                                                                 |
| libretro cores: save states                       | <p><code>saves\gb\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\gb\libretro.gambatte</code>)</p>                                                                                     |
| Mesen: save states                                | `saves\gb\mesen\SaveStates`                                                                                                                                                                |
| Mednafen: save states                             | `saves\gb\mednafen\sstates`                                                                                                                                                                |
| mGBA: save states                                 | `saves\gb\mgba\sstates`                                                                                                                                                                    |
| ares: game saves and save states                  | `saves\gb\ares`                                                                                                                                                                            |
| jgenesis: game saves                              | `saves\gb\jgenesis`                                                                                                                                                                        |
| BizHawk: game saves                               | `saves\gb\bizhawk`                                                                                                                                                                         |
| BIOS                                              | `bios`                                                                                                                                                                                     |
| Cheats                                            | <p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\mgba</code> (mGBA)</p><p><code>cheats\jgenesis</code> (jgenesis)</p><p><code>cheats\bizhawk\gb</code> (BizHawk)</p>          |
| Screenshots                                       | <p><code>screenshots\mesen</code></p><p><code>screenshots\mednafen</code></p><p><code>screenshots\mgba</code></p><p><code>screenshots\ares</code>, <code>screenshots\bizhawk\gb</code></p> |

## Guides

### Colors and palettes

On a real Game Boy, the picture is in four shades of green. Several emulators offer other colors:

<table><thead><tr><th width="149.5">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>gambatte core</td><td><strong>VISUAL RENDERING > COLORIZATION</strong></td><td><strong>AUTOMATIC</strong>: the palette the Game Boy Color or the Super Game Boy gives the game; <strong>GAMEBOY COLOR</strong> or <strong>SUPER GAMEBOY</strong>: palettes of these consoles; <strong>INTERNAL</strong>: palette chosen in <strong>PALETTE</strong>.</td></tr><tr><td>gambatte core</td><td><strong>VISUAL RENDERING > PALETTE</strong></td><td>Game Boy (DMG, Pocket, Light) and Game Boy Color palettes, and many fan palettes (TWB64, PixelShift).</td></tr><tr><td>sameboy core</td><td><strong>VISUAL RENDERING > PALETTE</strong></td><td>Greyscale, lime, olive or teal.</td></tr><tr><td>gearboy core</td><td><strong>VISUAL RENDERING > PALETTE</strong></td><td>Original, sharp, B/W, autumn, soft, slime.</td></tr><tr><td>jgenesis</td><td><strong>VISUAL RENDERING > PALETTE</strong></td><td>Game Boy palettes.</td></tr></tbody></table>

### Game Boy screen (ghosting)

The Game Boy screen is slow: some games make objects flicker to fake transparency (waves, ghosts…). On a modern screen, this flicker becomes visible. The gambatte core reproduces the original screen by default (**VISUAL RENDERING > INTERFRAME BLENDING > ACCURATE**). With another emulator, use gambatte.

### Multiplayer

Two-player games over the Game Link cable (Tetris, F-1 Race, Pokémon…) are played in the [**Game Boy 2 Players**](game-boy-2-players.md) system (`roms\gb2players`), which shows both consoles side by side: see its page.

The DoubleCherryGB core can also link several Game Boys in that system, with **EMULATION > NUMBER OF PLAYERS** (up to 4) and **EMULATION > LINK CABLE DEVICE** (4 player adapter for F-1 Race, Faceball 2000 ring cable…).

### Other useful options

| Emulator                    | Option                                   | Effect                                                                             |
| --------------------------- | ---------------------------------------- | ---------------------------------------------------------------------------------- |
| sameboy core                | **EMULATION > GAME BOY MODEL**           | Game Boy (default), Game Boy Pocket/Light or Game Boy Color.                       |
| gambatte core, gearboy core | **EMULATION > FORCE HARDWARE**           | Runs the game on another console: Game Boy Color or GBA (gambatte), GBA (gearboy). |
| gearboy core                | **VISUAL RENDERING > NO SPRITE LIMIT**   | Removes flicker when many objects are on screen.                                   |
| jgenesis                    | **EMULATION > TARGET 60 FPS**            | Runs games at 60 frames per second (the Game Boy shows a little under 60).         |
| Mesen                       | **LATENCY REDUCTION > RUN-AHEAD FRAMES** | Reduces the delay between a button press and the action on screen.                 |

## Known issues

<table><thead><tr><th width="337.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>A <code>.gbc</code> game does not show up</td><td>Game Boy Color games go in <code>roms\gbc</code>.</td></tr><tr><td>Objects flicker (transparency)</td><td>Use the gambatte core: see <a href="game-boy.md#game-boy-screen-ghosting"><strong>Game Boy screen (ghosting)</strong></a>.</td></tr><tr><td>No Super Game Boy border</td><td>Put the game in <code>roms\sgb</code>.</td></tr><tr><td>The Nintendo logo is not shown at startup</td><td>Add <code>gb_bios.bin</code> to <code>bios</code> and enable <strong>START ORIGINAL BIOS</strong> (gambatte, gearboy).</td></tr><tr><td>The two-player game does not work</td><td>Put the game in <code>roms\gb2players</code>.</td></tr></tbody></table>
