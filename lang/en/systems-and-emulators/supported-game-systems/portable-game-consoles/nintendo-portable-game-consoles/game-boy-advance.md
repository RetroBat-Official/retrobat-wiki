---
description: Nintendo
---

# Game Boy Advance

<div align="left"><figure><img src="../../../../.gitbook/assets/image (774).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Game Boy Advance** is Nintendo's 32-bit handheld console, released in Japan in March 2001, then in North America and Europe in June 2001. Wider than the Game Boy, it adds the L and R shoulder buttons and a bigger color screen. It was followed by the **Game Boy Advance SP** (2003, lit screen, rechargeable battery) and the **Game Boy Micro** (2005), for more than 80 million units in total.

Its library mixes original games and Super Nintendo ports: Pokémon Ruby, Sapphire, Emerald, FireRed and LeafGreen, The Legend of Zelda: The Minish Cap, Metroid Fusion and Zero Mission, Advance Wars, Fire Emblem, Golden Sun, Castlevania: Aria of Sorrow, Mario Kart: Super Circuit… The Game Link cable connects up to four consoles: these games have their own system in RetroBat, [**Game Boy Advance 2 Players**](game-boy-advance-2-players.md).

The console also plays Game Boy and Game Boy Color games: they go in `roms\gb` and `roms\gbc`.

{% embed url="https://en.wikipedia.org/wiki/Game_Boy_Advance" %}

## At a glance

<table><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\gba</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gba .zip .7z .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: mgba</td></tr><tr><td><strong>BIOS</strong></td><td>None with the default emulator (<code>gba_bios.bin</code> needed for ares, jgenesis and Mesen)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, except NO$GBA</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk, jgenesis; Mesen, Mednafen and ares with hotkeys; mGBA and NO$GBA from their menu</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                     | For whom?       | Strengths                                                                                                 | Limits                                                                   |
| ---------------------------- | --------------- | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| **libretro: mgba** (default) | Everyone        | Very accurate and fast, no file to add, solar sensor, Game Boy Player rumble, RetroAchievements, netplay. | —                                                                        |
| **libretro: mednafen\_gba**  | Curious players | VBA-M version adapted by Mednafen, solar sensor.                                                          | Few options.                                                             |
| **libretro: gpsp**           | Low-end PCs     | Very light (dynamic recompiler), cartridge rumble.                                                        | Less accurate.                                                           |
| **mgba** (standalone)        | mGBA users      | mGBA for Windows: shaders, internal resolution.                                                           | No RetroAchievements. Save states from the mGBA menu.                    |
| **jgenesis**                 | Curious players | Recent and accurate multi-system emulator.                                                                | `gba_bios.bin` required. No RetroAchievements.                           |
| **mesen**                    | Mesen users     | Mesen 2: accurate emulation and debugging tools.                                                          | `gba_bios.bin` required. No RetroAchievements. Save states with hotkeys. |
| **nosgba**                   | Curious players | NO$GBA, also a Nintendo DS emulator.                                                                      | Controllers to set up in NO$GBA. No RetroAchievements.                   |
| **mednafen**                 | Mednafen users  | Same emulation as the mednafen\_gba core.                                                                 | No RetroAchievements. Save states with hotkeys.                          |
| **ares**                     | Purists         | Very accurate emulation.                                                                                  | `gba_bios.bin` required. No RetroAchievements. Save states with hotkeys. |
| **bizhawk: mGBA**            | BizHawk users   | RetroAchievements, save states in the RetroBat menu.                                                      | —                                                                        |

**If in doubt, keep libretro: mgba.**

## BIOS

The default emulator (mgba) and most others do not need the BIOS: they emulate its functions. The original BIOS shows the Game Boy logo at startup and improves the compatibility of a few games.

ares, jgenesis and Mesen do not start games without it.

<table><thead><tr><th width="132.75">File</th><th width="217.25">Description</th><th width="81.75">Folder</th><th>md5</th></tr></thead><tbody><tr><td><code>gba_bios.bin</code></td><td>Game Boy Advance BIOS</td><td><code>bios</code></td><td>a860e8c0b6d573d191e4ec7db1b1e4f6</td></tr></tbody></table>

This file is optional (except for ares, jgenesis and Mesen) and checked by RetroBat. With gpsp, choose **EMULATION > BIOS > EXTERNAL** to use it; with Mednafen, **EMULATION > USE EXTERNAL BIOS**. **EMULATION > SKIP BIOS** (mgba, mGBA, jgenesis, BizHawk) or **SKIP BOOT** (Mesen) skips the boot screen.

## Which game format?

<table><thead><tr><th width="154">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gba</strong></td><td>Game Boy Advance cartridge image.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive).</td></tr></tbody></table>

## Controls

RetroBat sets up the controllers automatically for all emulators except NO$GBA. The buttons keep their position on the Super Nintendo controller:

<table><thead><tr><th width="209">RetroBat controller</th><th>Game Boy Advance</th></tr></thead><tbody><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>SOUTH</td><td>B</td></tr><tr><td>EAST</td><td>A</td></tr><tr><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

Some emulators add turbo buttons or the solar sensor keys (Boktai):

| Emulator                                                                           | Layout                                                                              |
| ---------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| mgba core, Mesen                                                                   | <img src="../../../../.gitbook/assets/image (777).png" alt="" data-size="original"> |
| mednafen\_gba core                                                                 | <img src="../../../../.gitbook/assets/image (776).png" alt="" data-size="original"> |
| gpsp core                                                                          | ![](<../../../../.gitbook/assets/image (779).png>)                                  |
| Mednafen                                                                           | ![](<../../../../.gitbook/assets/image (780).png>)                                  |
| mGBA, ares, jgenesis, BizHawk (with **CONTROLS > ENABLE TURBO**: mgba core layout) | <img src="../../../../.gitbook/assets/image (775).png" alt="" data-size="original"> |

To get the letters of your controller (A at the bottom, B on the right), enable **CONTROLS > INVERT FACE BUTTONS** (all emulators except NO$GBA).

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

jgenesis has no screenshot hotkey. With mGBA and NO$GBA, only HOTKEY + START (exit) is set up: save states are made from their menu.

## Folders

<table><thead><tr><th width="341.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores, mGBA, Mesen, Mednafen, NO$GBA: game saves</td><td><code>saves\gba</code></td></tr><tr><td>libretro cores: save states</td><td><p><code>saves\gba\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\gba\libretro.mgba</code>)</p></td></tr><tr><td>mGBA: save states</td><td><code>saves\gba\mgba\sstates</code></td></tr><tr><td>Mesen: save states</td><td><code>saves\gba\mesen\SaveStates</code></td></tr><tr><td>Mednafen: save states</td><td><code>saves\gba\mednafen\sstates</code></td></tr><tr><td>NO$GBA: save states</td><td><code>saves\gba\nosgba\sstates</code></td></tr><tr><td>ares: game saves and save states</td><td><code>saves\gba\ares</code></td></tr><tr><td>jgenesis: game saves</td><td><code>saves\gba\jgenesis</code></td></tr><tr><td>BizHawk: game saves</td><td><code>saves\gba\bizhawk</code></td></tr><tr><td>BIOS</td><td><code>bios</code> (copied by RetroBat to <code>emulators\mesen\Firmware</code> for Mesen)</td></tr><tr><td>Cheats</td><td><p><code>cheats\mgba</code> (mGBA)</p><p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\jgenesis</code>(jgenesis)</p><p><code>cheats\bizhawk\gba</code> (BizHawk)</p></td></tr><tr><td>Screenshots</td><td><p><code>screenshots\mgba</code></p><p><code>screenshots\mesen</code></p><p><code>screenshots\mednafen</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\gba</code></p></td></tr></tbody></table>

## Guides

### Screen colors

The screen of the first Game Boy Advance was not lit: games use very bright colors, which look garish on a modern screen.

<table><thead><tr><th width="129.5">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>mgba core</td><td><strong>VISUAL RENDERING > COLOR CORRECTION</strong></td><td><strong>GBA</strong>: colors of the original screen.</td></tr><tr><td>gpsp core</td><td><strong>VISUAL RENDERING > COLOR CORRECTION</strong></td><td>Turns the correction on or off.</td></tr><tr><td>jgenesis</td><td><strong>VISUAL RENDERING > COLOR CORRECTION</strong></td><td>Colors of the original screen (enabled by default).</td></tr><tr><td>NO$GBA</td><td><strong>VISUAL RENDERING > COLOR MODE</strong></td><td><strong>BACKLIGHT</strong> (Game Boy Advance SP, default), <strong>NO BACKLIGHT</strong>, <strong>BLURRY</strong> or <strong>POPPY</strong> (Nintendo DS / DS Lite).</td></tr></tbody></table>

Some games make objects flicker to fake transparency: **VISUAL RENDERING > INTERFRAME BLENDING** (mgba and gpsp cores, mGBA) or **FRAME BLENDING** (jgenesis, enabled by default) reproduces the original screen.

### Solar sensor and rumble

A few cartridges include a sensor or a motor:

<table><thead><tr><th width="197">Cartridge</th><th>Games</th><th>Emulator</th></tr></thead><tbody><tr><td>Solar sensor</td><td>Boktai 1 to 3</td><td>mednafen_gba core (keys shown on its layout, see <strong>Controls</strong>), mgba core</td></tr><tr><td>Rumble</td><td>Drill Dozer, WarioWare: Twisted!</td><td>gpsp core (automatic detection)</td></tr><tr><td>Game Boy Player rumble</td><td>Game Boy Player compatible games (Pokémon Pinball: Ruby &#x26; Sapphire…)</td><td>mgba core: <strong>CONTROLS > ENABLE RUMBLE</strong> (may cause slowdowns)</td></tr></tbody></table>

### Multiplayer

Game Link cable games (Mario Kart: Super Circuit, Pokémon trades, The Legend of Zelda: Four Swords…) are played in the **Game Boy Advance 2 Players** system (`roms\gba2players`): see [its page](game-boy-advance-2-players.md).

### Other useful options

<table><thead><tr><th width="120.75">Emulator</th><th>Option</th><th>Effect</th></tr></thead><tbody><tr><td>gpsp core</td><td><strong>EMULATION > DYNAMIC RECOMPILER</strong></td><td>Enabled by default: much faster.</td></tr><tr><td>gpsp core</td><td><strong>VISUAL RENDERING > NO SPRITE LIMIT</strong></td><td>Removes flicker when many objects are on screen.</td></tr><tr><td>mgba core</td><td><strong>AUDIO > AUDIO FILTER</strong></td><td>Softens the harsh sound of some games.</td></tr><tr><td>mGBA</td><td><strong>INTERNAL RESOLUTION</strong></td><td>Picture size before shaders (4X by default).</td></tr><tr><td>mGBA</td><td><strong>SHADER SET</strong></td><td>mGBA image filters (AGB-001 and AGS-001 screens, LCD…).</td></tr><tr><td>mGBA</td><td><strong>DRIVERS > VIDEO</strong></td><td><strong>OPENGL</strong> (default) or <strong>SOFTWARE</strong>. OpenGL is required for shaders and internal resolution.</td></tr><tr><td>jgenesis</td><td><strong>AUDIO > AUDIO INTERPOLATION</strong></td><td>Sound quality.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="344">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>ares, jgenesis or Mesen does not start the game</td><td>Add <code>gba_bios.bin</code> to <code>bios</code>.</td></tr><tr><td>The controller does not respond with NO$GBA</td><td>RetroBat does not set up NO$GBA: set the keys in its options, or use another emulator.</td></tr><tr><td>Colors are too bright</td><td>See <a href="game-boy-advance.md#screen-colors"><strong>Screen colors</strong></a>.</td></tr><tr><td>A <code>.gb</code> or <code>.gbc</code> game does not show up</td><td>Game Boy and Game Boy Color games go in <code>roms\gb</code> and <code>roms\gbc</code>.</td></tr><tr><td>The multiplayer game does not work</td><td>Put the game in <code>roms\gba2players</code>.</td></tr></tbody></table>
