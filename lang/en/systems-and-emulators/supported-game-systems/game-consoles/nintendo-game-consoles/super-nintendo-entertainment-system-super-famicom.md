---
description: Nintendo
---

# Super Nintendo Entertainment System - Super Famicom

<table data-header-hidden><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><img src="https://i.imgur.com/inZ65eS.png" alt="" data-size="original"></td><td><img src="https://i.imgur.com/fcfmfq4.png" alt="" data-size="original"></td><td></td></tr></tbody></table>

## Overview

The **Super Nintendo** (Super Famicom in Japan) is Nintendo's 16-bit console, released in Japan in November 1990, in North America in 1991 and in Europe in 1992. With nearly 50 million units sold, it is one of the most popular consoles of its time, the direct rival of the Mega Drive / Genesis.

Its controller introduced the **X** and **Y** buttons and the **L** and **R** shoulder buttons, found on almost every controller since. **Mode 7**, which rotates and scales a whole background, gives Super Mario Kart and F-Zero their tracks. Some cartridges carry an extra chip: **Super FX** (Star Fox, Yoshi's Island), **DSP** (Super Mario Kart, Pilotwings), **SA-1** (Super Mario RPG, Kirby Super Star), **Cx4** (Mega Man X2 and X3).

Its library holds many classics: Super Mario World, The Legend of Zelda: A Link to the Past, Super Metroid, Donkey Kong Country, Chrono Trigger, Final Fantasy VI, Street Fighter II… In Japan, the console received two add-ons that have their own system in RetroBat: the **Satellaview** (games broadcast by satellite) and Bandai's **Sufami Turbo** (mini-cartridges). **MSU-1** games and hacks, which add a CD-quality soundtrack, also have their own system.

{% embed url="https://en.wikipedia.org/wiki/Super_Nintendo_Entertainment_System" %}

## At a glance

<table><thead><tr><th width="191.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\snes</code></td></tr><tr><td><strong>Extensions</strong></td><td>.smc .fig .sfc .gd3 .gd7 .dx2 .bsx .swc .rom .wad .zip .7z .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: snes9x</td></tr><tr><td><strong>BIOS</strong></td><td>None (DSP chip firmwares optional for Mesen-S and Mesen)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk, jgenesis; Snes9x, Mesen, Mednafen and ares with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, Snes9x, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr><tr><td><strong>Light guns</strong></td><td>snes9x, bsnes, bsnes_hd_beta, bsnes-jg, mesen-s cores; Snes9x, Mesen, Mednafen, jgenesis, BizHawk</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                                  | For whom?            | Strengths                                                                                                                                                                  | Limits                                                                                                                                        |
| ----------------------------------------- | -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **libretro: snes9x** (default)            | Everyone             | Fast and very compatible: cartridge chips emulated with no file to add, MSU-1, Super Scope, Justifier, mouse, automatic multitap, RetroAchievements, netplay.              | —                                                                                                                                             |
| **libretro: bsnes-jg**                    | Purists              | Updated version of bsnes 115, very accurate, internal run-ahead.                                                                                                           | More demanding than snes9x.                                                                                                                   |
| **libretro: bsnes**                       | Purists              | bsnes 115: very accurate emulation, NTSC filters, overclocking.                                                                                                            | More demanding than snes9x.                                                                                                                   |
| **libretro: bsnes\_hd\_beta**             | High definition fans | bsnes with [**high resolution Mode 7**](super-nintendo-entertainment-system-super-famicom.md#high-definition-mode-7-bsnes_hd_beta) (Super Mario Kart, F-Zero, Pilotwings). | Beta version.                                                                                                                                 |
| **libretro: mednafen\_snes**              | Curious players      | Old version of bsnes adapted by Mednafen.                                                                                                                                  | Few options, no mouse or light gun. No advantage over the other cores.                                                                        |
| **libretro: mesen-s**                     | Purists              | Accurate Mesen-S emulation.                                                                                                                                                | DSP chip games need a firmware (see [**DSP chip games**](super-nintendo-entertainment-system-super-famicom.md#dsp-chip-games-mesen-s-mesen)). |
| **libretro: snes9x2005**                  | Low-end PCs          | Old version of snes9x, very light.                                                                                                                                         | Less accurate.                                                                                                                                |
| **mednafen** (standalone)                 | Mednafen users       | Same emulation as the mednafen\_snes core.                                                                                                                                 | No RetroAchievements. Save states with hotkeys.                                                                                               |
| **mesen**                                 | Mesen users          | Mesen 2: accurate emulation and debugging tools.                                                                                                                           | No RetroAchievements. Save states with hotkeys. DSP chip games: firmware needed.                                                              |
| **snes9x** (standalone)                   | Snes9x users         | Snes9x for Windows (SuperSnes9x version): image filters, RetroAchievements.                                                                                                | Save states with hotkeys.                                                                                                                     |
| **jgenesis**                              | Curious players      | Recent and accurate multi-system emulator.                                                                                                                                 | Two players max. No RetroAchievements.                                                                                                        |
| **ares**                                  | Purists              | Very accurate emulation, built-in chips (no file to add).                                                                                                                  | Two players max. No RetroAchievements. Save states with hotkeys.                                                                              |
| **bizhawk: BSNES**, **Faust**, **Snes9x** | BizHawk users        | Three emulations to choose from, RetroAchievements, save states in the RetroBat menu.                                                                                      | —                                                                                                                                             |

**If in doubt, keep libretro: snes9x.**

## BIOS

The Super Nintendo has no BIOS: no file is needed with the default emulator.

Only Mesen-S (libretro core) and Mesen (standalone) need the DSP chip firmwares for the few games that use them (see [**DSP chip games**](super-nintendo-entertainment-system-super-famicom.md#dsp-chip-games-mesen-s-mesen)). snes9x, bsnes and ares emulate them with no file. RetroBat reports them as optional when checking the BIOS.

| File                    | Chip               | Game examples                                 | Folder |
| ----------------------- | ------------------ | --------------------------------------------- | ------ |
| `dsp1.rom`, `dsp1b.rom` | DSP-1, DSP-1B      | Super Mario Kart, Pilotwings, Super Air Diver | `bios` |
| `dsp2.rom`              | DSP-2              | Dungeon Master                                | `bios` |
| `dsp3.rom`              | DSP-3              | SD Gundam GX                                  | `bios` |
| `dsp4.rom`              | DSP-4              | Top Gear 3000                                 | `bios` |
| `st010.rom`             | ST010              | F1 ROC II: Race of Champions                  | `bios` |
| `st011.rom`             | ST011              | Hayazashi Nidan Morita Shougi                 | `bios` |
| `st018.rom`             | ST018 (Mesen only) | Hayazashi Nidan Morita Shougi 2               | `bios` |

All these files are optional and checked by RetroBat.

## Which game format?

| Format                                           | Description                                                                                                                         |
| ------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| **.sfc**, **.smc**                               | Cartridge image (`.smc`: with a copier header, read by all emulators). Japanese, American and European games go in the same folder. |
| **.fig**, **.swc**, **.gd3**, **.gd7**, **.dx2** | Old cartridge copier formats, read like `.smc` files.                                                                               |
| **.zip**, **.7z**                                | A compressed game (one game per archive).                                                                                           |

Satellaview games (`.bs`) go in `roms\satellaview`, Sufami Turbo games (`.st`) in `roms\sufami`, MSU-1 games in `roms\snes-msu1`.

## Controls

RetroBat automatically configures controllers for all emulators. Buttons keep their position on the Super Nintendo controller:

<table><thead><tr><th width="202.75">RetroBat controller</th><th>Super Nintendo</th></tr></thead><tbody><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>SOUTH</td><td>B</td></tr><tr><td>EAST</td><td>A</td></tr><tr><td>WEST</td><td>Y</td></tr><tr><td>NORTH</td><td>X</td></tr><tr><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/snes.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

On an Xbox controller, the A button (bottom) is therefore the Super Nintendo B. To get the letters of your controller (A at the bottom, B on the right), turn on **CONTROLS > INVERT FACE BUTTONS**:

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/snes_invert.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Hotkeys

libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

Snes9x, Mesen, Mednafen, ares, jgenesis and BizHawk use the RetroBat hotkeys:

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

Snes9x has no fullscreen hotkey, jgenesis has no screenshot hotkey.

## Folders

| Content                                             | Folder                                                                                                            |
| --------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| libretro cores, Snes9x, Mesen, Mednafen: game saves | `saves\snes`                                                                                                      |
| libretro cores: save states                         | <p><code>saves\snes\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\snes\libretro.snes9x</code>)</p>          |
| Snes9x: save states                                 | `saves\snes\snes9x\sstates`                                                                                       |
| Mesen: save states                                  | `saves\snes\mesen\SaveStates`                                                                                     |
| Mednafen: save states                               | `saves\snes\mednafen\sstates`                                                                                     |
| ares: game saves and save states                    | `saves\snes\ares`                                                                                                 |
| jgenesis: game saves                                | `saves\snes\jgenesis`                                                                                             |
| jgenesis: save states                               | `saves\snes\jgenesis\states`                                                                                      |
| BizHawk: game saves                                 | `saves\snes\bizhawk`                                                                                              |
| BizHawk: save states                                | `saves\snes\bizhawk\sstates\<core>`                                                                               |
| DSP chip firmwares                                  | `bios` (copied by RetroBat to `emulators\mesen\Firmware` for Mesen)                                               |
| Cheat codes                                         | <p><code>cheats\snes9x</code> (Snes9x)</p><p><code>cheats\mednafen</code> (Mednafen)</p>                          |
| Screenshots                                         | `screenshots\snes9x`, `screenshots\mesen`, `screenshots\mednafen`, `screenshots\ares`, `screenshots\bizhawk\snes` |

## Guides

### Multiplayer (multitap)

The Super Nintendo has two controller ports. Games for more than two players (Super Bomberman, Micro Machines, NBA Jam…) use a multitap, plugged into the player 2 port: up to 5 players.

<table><thead><tr><th width="285.25">Emulator</th><th>Multitap</th></tr></thead><tbody><tr><td>snes9x core</td><td>Plugged in as soon as a 3rd controller is connected</td></tr><tr><td>bsnes, bsnes_hd_beta, bsnes-jg, mesen-s cores</td><td>Plugged in as soon as a 3rd controller is connected (<strong>CONTROLS > PLAYER 2 CONTROLLER TYPE > MULTITAP</strong> to force it)</td></tr><tr><td>Snes9x</td><td>Plugged in as soon as a 3rd controller is connected</td></tr><tr><td>Mesen</td><td><strong>CONTROLS > USE MULTITAP</strong> (<strong>SINGLE MULTITAP</strong> up to 5 players, <strong>DUAL MULTITAP</strong> up to 8)</td></tr><tr><td>Mednafen</td><td><strong>CONTROLS > USE MULTITAP</strong> (<strong>PORT 1</strong>, <strong>PORT 2</strong> or <strong>BOTH PORTS</strong>)</td></tr><tr><td>ares, jgenesis</td><td>Two players max</td></tr></tbody></table>

### Light guns (Super Scope, Justifier)

About twenty games use Nintendo's Super Scope (Super Scope 6, Yoshi's Safari, Battle Clash, T2: The Arcade Game…) or Konami's Justifier (Lethal Enforcers). Turn on **GUNS > ENABLE GUN**: RetroBat plugs in the right gun for known games. For another game, choose it in **GUNS > GUN TYPE** (libretro cores, Snes9x).

<table><thead><tr><th width="307.75">Emulator</th><th>Light guns</th></tr></thead><tbody><tr><td>snes9x core</td><td>Super Scope, Justifier, two Justifiers, M.A.C.S. Rifle</td></tr><tr><td>bsnes, bsnes_hd_beta, bsnes-jg cores</td><td>Super Scope, Justifier</td></tr><tr><td>mesen-s core, Mesen</td><td>Super Scope (Mesen: <strong>GUNS > GUN PORT</strong>, port 2 by default)</td></tr><tr><td>Snes9x</td><td>Super Scope, Justifier, two Justifiers</td></tr><tr><td>Mednafen, jgenesis, BizHawk</td><td>Super Scope</td></tr></tbody></table>

Without a light gun, the mouse is used as the crosshair. For more details, see the [**Light guns**](../../../../controllers/supported-controllers/lightguns/) page.

### Mouse (Mario Paint)

Mario Paint and a few other games use the Super Nintendo mouse:

<table><thead><tr><th width="296.5">Emulator</th><th>Setting</th></tr></thead><tbody><tr><td>snes9x, bsnes, bsnes_hd_beta, bsnes-jg cores</td><td><strong>CONTROLS > PLAYER 1 CONTROLLER TYPE > MOUSE</strong></td></tr><tr><td>mesen-s core, Mesen</td><td><strong>CONTROLS > PLAYER 1 CONTROLLER TYPE > MOUSE</strong></td></tr><tr><td>Snes9x</td><td><strong>CONTROLS > USE MOUSE > PORT 1</strong></td></tr></tbody></table>

### DSP chip games (Mesen-S, Mesen)

Mesen-S and Mesen need a firmware for DSP or ST01x chip games (Super Mario Kart, Pilotwings, Top Gear 3000…). Without it, these games don't start with Mesen-S, and Mesen asks for the file at launch. Copy the files listed in the [**BIOS**](super-nintendo-entertainment-system-super-famicom.md#bios) section to `bios`: RetroBat gives them to Mesen-S and copies them for Mesen.

snes9x (default), bsnes and ares need no file.

### High definition Mode 7 (bsnes\_hd\_beta)

The bsnes\_hd\_beta core displays Mode 7 backgrounds (Super Mario Kart, F-Zero, Pilotwings, Final Fantasy VI…) at a higher resolution than the console:

| Option                                               | Effect                                                      |
| ---------------------------------------------------- | ----------------------------------------------------------- |
| **VISUAL RENDERING > MODE 7 SCALE**                  | Mode 7 resolution (2x by default, 1x = original rendering). |
| **VISUAL RENDERING > MODE 7 SUPERSAMPLING**          | Smooths Mode 7 (2x by default).                             |
| **VISUAL RENDERING > MODE 7 PERSPECTIVE CORRECTION** | Fixes the distortion of the ground in the distance.         |

### Other useful options

| Emulator                               | Option                                          | Effect                                                                                          |
| -------------------------------------- | ----------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| snes9x core                            | **EMULATION > CPU OVERCLOCK**                   | Reduces slowdowns (Gradius III, Super R-Type), but can cause bugs.                              |
| snes9x core                            | **EMULATION > SUPERFX CHIP OVERCLOCK**          | Higher frame rate in Super FX games (Star Fox, Stunt Race FX).                                  |
| snes9x core                            | **VIDEO > EMULATED VIDEO SIGNAL**               | Recreates the original output (RF, composite, S-Video, RGB).                                    |
| snes9x core                            | **VISUAL RENDERING > PIXEL BLENDING**           | **MERGE**: needed for the transparencies of a few high resolution games (Kirby's Dream Land 3). |
| snes9x core                            | **AUDIO > AUDIO INTERPOLATION**                 | **GAUSSIAN** (default) reproduces the console sound.                                            |
| snes9x core                            | **EMULATION > UNSAFE HACKS**                    | For a few homebrews and hacks that don't start. Keep it off for commercial games.               |
| bsnes, bsnes\_hd\_beta cores           | **EMULATION > OVERCLOCKING**                    | Speeds up the CPU, the SA-1 and the Super FX.                                                   |
| bsnes, bsnes\_hd\_beta cores           | **VIDEO > NO SPRITE LIMIT**                     | Removes flickering when many objects are on screen.                                             |
| bsnes, bsnes\_hd\_beta, bsnes-jg cores | **LATENCY REDUCTION > RUN-AHEAD FRAMES (CORE)** | Reduces the delay between a button press and the action on screen.                              |
| snes9x2005 core                        | **VIDEO > FRAMESKIP**                           | For low-end PCs.                                                                                |
| Snes9x                                 | **SHADER SET**                                  | Snes9x image filters (NTSC, hq2x, xBRZ…).                                                       |

## Known issues

| Issue                                                              | Solution                                                                                                                                                                         |
| ------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Players 3 to 5 don't respond                                       | The multitap is needed: see [**Multiplayer (multitap)**](super-nintendo-entertainment-system-super-famicom.md#multiplayer-multitap). ares and jgenesis only emulate two players. |
| Super Mario Kart or Pilotwings doesn't start with Mesen-S or Mesen | Add the DSP chip firmware: see [**DSP chip games**](super-nintendo-entertainment-system-super-famicom.md#dsp-chip-games-mesen-s-mesen), or use snes9x.                           |
| Mario Paint doesn't respond                                        | Plug in the mouse: see [**Mouse (Mario Paint)**](super-nintendo-entertainment-system-super-famicom.md#mouse-mario-paint).                                                        |
| Super FX games slow down                                           | Raise **SUPERFX CHIP OVERCLOCK** (snes9x) or **OVERCLOCKING** (bsnes).                                                                                                           |
| Transparencies are missing (Kirby's Dream Land 3)                  | snes9x: **PIXEL BLENDING > MERGE**; bsnes: **BLUR EMULATION**.                                                                                                                   |
| A `.bs` or `.st` game doesn't start                                | Put it in `roms\satellaview` or `roms\sufami`.                                                                                                                                   |
