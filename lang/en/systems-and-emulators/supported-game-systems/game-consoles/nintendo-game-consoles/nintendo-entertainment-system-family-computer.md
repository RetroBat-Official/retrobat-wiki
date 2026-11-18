---
description: Nintendo
---

# Nintendo Entertainment System - Family Computer

<table data-header-hidden><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><p></p><p><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/nes-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/nes.svg" alt="" data-size="original"></picture></p></td><td><p></p><p><img src="https://upload.wikimedia.org/wikipedia/commons/7/7d/Family_Computer_logo.svg" alt="" data-size="original"></p></td><td></td></tr></tbody></table>

## Overview

The **Famicom** (Family Computer) is Nintendo's 8-bit home console, released in Japan in July 1983. It was sold in the West as the **Nintendo Entertainment System** (NES), in 1985 in North America and in 1986 in Europe. It revived the video game market and sold more than 60 million units.

Its library includes Super Mario Bros. 1 to 3, The Legend of Zelda, Metroid, Mega Man, Castlevania, Final Fantasy, Dragon Quest, Punch-Out!!, Contra… The **Zapper** light gun (Duck Hunt, Hogan's Alley) and the **Four Score** four-player adapter are emulated.

**Famicom Disk System** games have their own system, `roms\fds`, but `.fds` files are also accepted here.

{% embed url="https://en.wikipedia.org/wiki/Nintendo_Entertainment_System" %}

## At a glance

<table><thead><tr><th width="241.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\nes</code></td></tr><tr><td><strong>Extensions</strong></td><td>.fds .nes .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: fceumm</td></tr><tr><td><strong>BIOS</strong></td><td>None (<code>disksys.rom</code> for <code>.fds</code> games)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk, jgenesis; Mesen, Mednafen and ares with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                             | For whom?       | Strengths                                                                                                 | Limits                                          |
| ------------------------------------ | --------------- | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| **libretro: fceumm** (default)       | Everyone        | Very compatible, Zapper, four players, HD packs, Game Genie add-on, RetroAchievements, netplay.           | —                                               |
| **libretro: nestopia**               | Everyone        | Very accurate, Zapper, Arkanoid, four players, RetroAchievements, netplay.                                | —                                               |
| **libretro: mesen**                  | Purists         | Very accurate, Zapper, Power Pad, Arkanoid, HD packs, RetroAchievements, netplay.                         | —                                               |
| **mednafen**                         | Mednafen users  | Solid emulation, Zapper.                                                                                  | No RetroAchievements. Save states with hotkeys. |
| **mesen**                            | Mesen users     | Mesen 2: accurate emulation, Zapper, four players, debugging tools.                                       | No RetroAchievements. Save states with hotkeys. |
| **jgenesis**                         | Curious players | Recent and accurate multi-system emulator, Zapper.                                                        | No RetroAchievements.                           |
| **ares**                             | Purists         | Very accurate emulation.                                                                                  | No RetroAchievements. Save states with hotkeys. |
| **bizhawk: NesHawk**, **quickerNES** | BizHawk users   | Accurate NesHawk, fast quickerNES, Zapper (NesHawk), RetroAchievements, save states in the RetroBat menu. | —                                               |

**If in doubt, keep libretro: fceumm.**

## BIOS

The NES has no BIOS: no file is needed for cartridges.

Famicom Disk System games (`.fds`) need the drive BIOS, see the [**Famicom Disk System**](family-computer-disk-system.md) page.

<table><thead><tr><th width="124">File</th><th width="221.25">Description</th><th width="73.5">Folder</th><th>md5</th></tr></thead><tbody><tr><td><code>disksys.rom</code></td><td>Famicom Disk System BIOS</td><td><code>bios</code></td><td>ca30b50f880eb660a320674ed365ef7a</td></tr></tbody></table>

This file is optional here and checked by RetroBat.

## Which game format?

<table><thead><tr><th width="200.25">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.nes</strong></td><td>Cartridge image.</td></tr><tr><td><strong>.fds</strong></td><td>Famicom Disk System disk image.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed game (one game per archive).</td></tr></tbody></table>

## Controls

RetroBat sets up the controllers automatically for all emulators. Default layout:

<table><thead><tr><th width="191.5">RetroBat controller</th><th>NES</th></tr></thead><tbody><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>SOUTH</td><td>A</td></tr><tr><td>WEST</td><td>B</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

Layout options:

| Option                        | Emulators                                                            | Effect                                                         |
| ----------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------- |
| **CONTROLS > ROTATE BUTTONS** | All                                                                  | A on EAST, B on SOUTH.                                         |
| **CONTROLS > XBOX LAYOUT**    | fceumm, nestopia, mesen cores                                        | A on SOUTH, B on EAST, like the letters of an Xbox controller. |
| **CONTROLS > ENABLE TURBO**   | fceumm and nestopia cores, Mesen, Mednafen; mesen core: speed choice | Adds turbo A and turbo B on the remaining buttons.             |

| Layout                    | Diagram                                                                                                                                       |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Default                   | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes.png?raw=true" alt="" data-size="original">              |
| Turbo                     | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_turbo.png?raw=true" alt="" data-size="original">        |
| Rotated buttons           | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_rotate.png?raw=true" alt="" data-size="original">       |
| Rotated buttons and turbo | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_rotate_turbo.png?raw=true" alt="" data-size="original"> |
| Xbox                      | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_xbox.png?raw=true" alt="" data-size="original">         |
| Xbox and turbo            | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_xbox_turbo.png?raw=true" alt="" data-size="original">   |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (621).png" alt=""><figcaption></figcaption></figure></div>

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

jgenesis has no screenshot hotkey.

## Folders

<table><thead><tr><th width="311.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores, Mesen, Mednafen: game saves</td><td><code>saves\nes</code></td></tr><tr><td>libretro cores: save states</td><td><p><code>saves\nes\libretro.&#x3C;core></code> </p><p>(e.g. <code>saves\nes\libretro.fceumm</code>)</p></td></tr><tr><td>Mesen: save states</td><td><code>saves\nes\mesen\SaveStates</code></td></tr><tr><td>Mednafen: save states</td><td><code>saves\nes\mednafen\sstates</code></td></tr><tr><td>ares: game saves and save states</td><td><code>saves\nes\ares</code></td></tr><tr><td>jgenesis: game saves</td><td><code>saves\nes\jgenesis</code></td></tr><tr><td>BizHawk: game saves</td><td><code>saves\nes\bizhawk</code></td></tr><tr><td>BIOS</td><td><code>bios</code> (copied by RetroBat to <code>emulators\mesen\Firmware</code> for Mesen)</td></tr><tr><td>HD packs</td><td><code>bios\HdPacks</code> (fceumm and mesen cores)</td></tr><tr><td>Cheats</td><td><p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\jgenesis</code> (jgenesis)</p><p><code>cheats\bizhawk\nes</code> (BizHawk)</p></td></tr><tr><td>Screenshots</td><td><code>screenshots\mesen</code>, <code>screenshots\mednafen</code>, <code>screenshots\ares</code>, <code>screenshots\bizhawk\nes</code></td></tr></tbody></table>

## Guides

### Zapper

Several games use the Zapper light gun (Duck Hunt, Hogan's Alley, Wild Gunman, Gumshoe…). Enable **GUNS > ENABLE GUN** with the fceumm, nestopia or mesen cores, Mesen, Mednafen, jgenesis or BizHawk NesHawk: RetroBat plugs the Zapper, in port 2 as on the real console. With Mesen, **GUNS > GUN PORT** lets you choose port 1.

For more details, see the [**Lightguns**](../../../../controllers/supported-controllers/lightguns/) page.

### Four-player games

Four-player games (Gauntlet II, Nintendo World Cup, Super Spike V'Ball…) need the Four Score (NES) or the Famicom four-player adapter:

<table><thead><tr><th width="179">Emulator</th><th>Option</th></tr></thead><tbody><tr><td>fceumm core</td><td><strong>CONTROLS > USE MULTITAP</strong>: <strong>NTSC</strong> (Four Score) or <strong>FAMICOM</strong>; automatic by default</td></tr><tr><td>nestopia core</td><td><strong>CONTROLS > USE MULTITAP</strong>: <strong>NTSC</strong> (Four Score) or <strong>FAMICOM</strong>; automatic by default</td></tr><tr><td>Mesen</td><td><strong>CONTROLS > USE MULTITAP</strong>: <strong>FOURSCORE</strong> or <strong>FOURSCORE + FOURPLAYER EXPANSION</strong></td></tr></tbody></table>

### HD packs

Mesen-format HD packs replace the original graphics. Put the pack in `bios\HdPacks`, in a folder named after the game file without its extension (for example `bios\HdPacks\Mega Man (USA)` for `Mega Man (USA).nes`), then:

* fceumm core: nothing to do, **VISUAL RENDERING > HD TEXTURE PACKS** is on by default;
* mesen core: enable **VISUAL RENDERING > CUSTOM TEXTURES**.

The pack only works with the game version it was made for: compare the sha1 of the game with the one in the `hires.txt` file of the pack.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (620).png" alt=""><figcaption></figcaption></figure></div>

## Known issues

<table><thead><tr><th width="352.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The Zapper does not work</td><td>Enable <strong>GUNS > ENABLE GUN</strong> (see <a href="nintendo-entertainment-system-family-computer.md#zapper"><strong>Zapper</strong></a>).</td></tr><tr><td>Players 3 and 4 do not respond</td><td>See <a href="nintendo-entertainment-system-family-computer.md#four-player-games"><strong>Four-player games</strong></a>.</td></tr><tr><td>A <code>.fds</code> game does not start</td><td>Add <code>disksys.rom</code> to <code>bios</code>.</td></tr><tr><td>A and B are swapped compared with your controller</td><td>See the layout options (<a href="nintendo-entertainment-system-family-computer.md#controls"><strong>Controls</strong></a>).</td></tr></tbody></table>
