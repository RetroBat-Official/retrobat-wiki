---
description: NEC
---

# PC Engine/TurboGrafx-16

<div align="left"><figure><img src="../../../../.gitbook/assets/image (667).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **PC Engine** is a NEC home console, designed with Hudson Soft and released in Japan in October 1987. Its games come on **HuCards**, credit-card-sized cards. Its 8-bit CPU (HuC6280) is paired with a 16-bit graphics chip: in North America, it was released in 1989 as the **TurboGrafx-16**.

Very popular in Japan, where it competed with the Famicom and then the Super Famicom, it is famous for its shoot'em ups and arcade conversions: R-Type, Bomberman, PC Genjin (Bonk's Adventure), Gunhed (Blazing Lazers), Splatterhouse, Soldier Blade, Parasol Stars… It has a single controller port: to play with more people, you need a multitap (the TurboTap), up to 5 players.

The console came in many models (CoreGrafx, Shuttle, PC Engine GT handheld, PC Engine Duo…) and add-ons. In RetroBat, CD games have their own system ([**PC Engine CD**](pc-engine-cd-rom-turbografx-cd.md)), as do the games of the [**SuperGrafx**](supergrafx.md), an enhanced version of the console.

{% embed url="https://en.wikipedia.org/wiki/TurboGrafx-16" %}

## At a glance

<table><thead><tr><th width="207.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\pcengine</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pce .bin .zip .7z .wad .squashfs</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: mednafen_pce</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BizHawk; Mednafen, Mesen and ares with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>mednafen and geargrafx cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr></tbody></table>

## Which emulator should I choose?

| Emulator                                           | For whom?       | Strengths                                                                                                                                              | Limits                                                                            |
| -------------------------------------------------- | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- |
| **libretro: mednafen\_pce** (default)              | Everyone        | Beetle PCE, Mednafen's complete PC Engine emulation: very accurate, 6-button pad, mouse, multitap, SuperGrafx games, RetroAchievements, netplay.       | —                                                                                 |
| **libretro: mednafen\_pce\_fast**                  | Low-end PCs     | Lighter, faster version of Beetle PCE.                                                                                                                 | Less accurate. No SuperGrafx emulation.                                           |
| **libretro: geargrafx**                            | Curious users   | Recent and accurate emulator: console model choice, Avenue Pad 3 and 6 controllers, color palettes.                                                    | —                                                                                 |
| **libretro: fbneo**                                | FBNeo users     | Same settings as FBNeo's arcade games.                                                                                                                 | Only `.zip` or `.7z` archives named like FBNeo's PC Engine sets.                  |
| **mednafen** (standalone)                          | Mednafen users  | Same emulation as the mednafen\_pce core.                                                                                                              | No RetroAchievements. Save states with hotkeys.                                   |
| **mesen**                                          | Mesen users     | Mesen 2: accurate emulation and debugging tools.                                                                                                       | No RetroAchievements. Save states with hotkeys.                                   |
| **ares**                                           | Purists         | Very accurate emulation.                                                                                                                               | Single player only. No RetroAchievements. Save states with hotkeys.               |
| **bizhawk: HyperNyma**, **PCEHawk**, **TurboNyma** | BizHawk users   | HyperNyma and TurboNyma are based on Mednafen (pce\_fast and pce), PCEHawk is BizHawk's own core. RetroAchievements, save states in the RetroBat menu. | —                                                                                 |
| **magicengine**                                    | Nostalgic users | Historical PC Engine emulator, high-resolution rendering and scanlines.                                                                                | No RetroAchievements. Save states not managed by RetroBat. A single hotkey: exit. |

**If in doubt, keep libretro: mednafen\_pce.**

## BIOS

HuCard games need no BIOS. The BIOS files for CD games (System Cards) are described on the [**PC Engine CD**](pc-engine-cd-rom-turbografx-cd.md) page.

## Which game format?

<table><thead><tr><th width="191.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.pce</strong></td><td>HuCard image. Read by all emulators except FBNeo. Japanese and American (TurboGrafx-16) games go in the same folder.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>A compressed <code>.pce</code> game (one game per archive).</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong> (FBNeo)</td><td>FBNeo only reads archives named after its PC Engine sets (see FBNeo's game list).</td></tr></tbody></table>

SuperGrafx games go in `roms\supergrafx`, CD games in `roms\pcenginecd`.

## Controls

RetroBat automatically configures controllers for all emulators. The PC Engine pad has a D-pad, two buttons **I** and **II**, a **SELECT** button and a **RUN** button. A few fighting games use a 6-button pad (Avenue Pad 6, buttons **III** to **VI**), such as Street Fighter II' Champion Edition.

<table><thead><tr><th width="246.5">RetroBat controller</th><th>PC Engine</th></tr></thead><tbody><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>EAST</td><td>I</td></tr><tr><td>SOUTH</td><td>II</td></tr><tr><td>WEST</td><td>III (6-button pad)</td></tr><tr><td>NORTH</td><td>IV (6-button pad)</td></tr><tr><td>L1</td><td>V (6-button pad)</td></tr><tr><td>R1</td><td>VI (6-button pad)</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>RUN</td></tr><tr><td>L2</td><td>2 / 6-button switch (mednafen cores, Mednafen); 2-button pad (BizHawk)</td></tr><tr><td>R2</td><td>6-button pad (BizHawk)</td></tr></tbody></table>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/pcengine_simple_6buttons.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Hotkeys

The libretro cores use the standard RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

Mednafen, Mesen, ares and BizHawk use the RetroBat hotkeys:

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

With MagicEngine, only HOTKEY + START (or `Esc`) is available, to exit.

## Folders

<table><thead><tr><th width="301.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores, Mednafen, Mesen: game saves</td><td><code>saves\pcengine</code></td></tr><tr><td>libretro cores: save states</td><td><p><code>saves\pcengine\libretro.&#x3C;core></code></p><p>(e.g. <code>saves\pcengine\libretro.mednafen_pce</code>)</p></td></tr><tr><td>Mednafen: save states</td><td><code>saves\pcengine\mednafen\sstates</code></td></tr><tr><td>Mesen: save states</td><td><code>saves\pcengine\mesen\SaveStates</code></td></tr><tr><td>ares: game saves and save states</td><td><code>saves\pcengine\ares</code></td></tr><tr><td>BizHawk: game saves</td><td><code>saves\pcengine\bizhawk</code></td></tr><tr><td>BizHawk: save states</td><td><code>saves\pcengine\bizhawk\sstates\&#x3C;core></code></td></tr><tr><td>MagicEngine: saves</td><td><code>saves\pcengine\magicengine</code></td></tr><tr><td>Cheat codes</td><td><p><code>cheats\mednafen</code> (Mednafen)</p><p><code>cheats\bizhawk\pcengine</code> (BizHawk)</p><p><code>cheats\magicengine\pcengine</code> (MagicEngine)</p></td></tr><tr><td>Screenshots</td><td><p><code>screenshots\mednafen</code></p><p><code>screenshots\mesen</code></p><p><code>screenshots\ares</code></p><p><code>screenshots\bizhawk\pcengine</code></p><p><code>screenshots\magicengine</code></p></td></tr></tbody></table>

## Guides

### Multiplayer (multitap)

The PC Engine has a single controller port: from 2 players on, the multitap (TurboTap) is needed. RetroBat plugs it in for you, up to 5 players:

<table><thead><tr><th width="269">Emulator</th><th>Multitap</th></tr></thead><tbody><tr><td>mednafen_pce core</td><td>Plugged in as soon as a 2nd controller is connected (<strong>CONTROLS > ENABLE MULTITAP</strong> to force it)</td></tr><tr><td>mednafen_pce_fast core</td><td>Always plugged in</td></tr><tr><td>geargrafx core</td><td>Plugged in as soon as a 2nd controller is connected (<strong>CONTROLS > USE TURBO-TAP</strong> to force it)</td></tr><tr><td>Mednafen</td><td>Plugged in as soon as a 2nd controller is connected (<strong>CONTROLS > USE MULTITAP</strong> to force it)</td></tr><tr><td>Mesen</td><td>Plugged in as soon as a 2nd controller is connected (<strong>CONTROLS > USE MULTITAP</strong> to force it)</td></tr><tr><td>BizHawk</td><td>Handled automatically</td></tr><tr><td>ares</td><td>Single player only</td></tr></tbody></table>

A few games misbehave with the multitap plugged in, such as Cho Aniki (PC Engine CD): to play them with several controllers connected, set the multitap option to **NO**. mednafen\_pce\_fast does not allow removing it.

### 6-button pad

For the games that use it (Street Fighter II' Champion Edition…), enable the 6-button pad:

| Emulator                                 | Setting                                                       |
| ---------------------------------------- | ------------------------------------------------------------- |
| mednafen\_pce, mednafen\_pce\_fast cores | **CONTROLS > USE 6-BUTTON PAD**, or L2 in game                |
| geargrafx core                           | **CONTROLS > CONTROLLER TYPE > AVENUE PAD 6**                 |
| Mednafen                                 | L2 in game                                                    |
| Mesen                                    | **CONTROLS > PLAYER 1 CONTROLLER TYPE > 6-BUTTON CONTROLLER** |
| ares                                     | **CONTROLS > USE 6-BUTTON PAD**                               |
| BizHawk (HyperNyma, TurboNyma)           | R2 in game (L2 to go back to 2 buttons)                       |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (668).png" alt=""><figcaption></figcaption></figure></div>

### Mouse

A few games use the PC Engine mouse. With the mednafen cores, choose **CONTROLS > PLAYER 1 CONTROLLER TYPE > MOUSE**.

### Other useful options

<table><thead><tr><th width="223.25">Emulator</th><th width="247">Option</th><th>Effect</th></tr></thead><tbody><tr><td>mednafen_pce core</td><td><strong>VIDEO > EMULATED SIGNAL TYPE</strong></td><td><strong>COMPOSITE</strong> (RetroBat default) recreates the console's original output, <strong>RGB</strong> gives a sharper picture.</td></tr><tr><td>mednafen cores, Mesen</td><td><strong>VIDEO > NO SPRITE LIMIT</strong></td><td>Removes flickering when many objects are on screen (geargrafx core: in <strong>EMULATION</strong>).</td></tr><tr><td>mednafen_pce core</td><td><strong>EMULATION > CPU OVERCLOCK</strong></td><td>Reduces slowdown, but may cause glitches.</td></tr><tr><td>geargrafx core</td><td><strong>EMULATION > CONSOLE TYPE</strong></td><td><strong>PC ENGINE (JP)</strong>, <strong>SUPERGRAFX (JP)</strong> or <strong>TURBOGRAFX-16 (US)</strong>. By default, the core picks it from the game.</td></tr><tr><td>geargrafx core</td><td><strong>VISUAL RENDERING > PALETTE</strong></td><td><strong>STANDARD RGB</strong>, <strong>TURBOXRAY</strong> or <strong>KITRINX</strong>.</td></tr><tr><td>Mesen</td><td><strong>EMULATION > CONSOLE TYPE</strong></td><td>Same choice as geargrafx.</td></tr><tr><td>mednafen_pce, mednafen_pce_fast cores</td><td><strong>TURBO</strong></td><td>RetroArch autofire.</td></tr></tbody></table>

## Known issues

| Issue                                 | Solution                                                                                                                                                                                      |
| ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Player 2 does not respond             | The multitap is needed: see [**Multiplayer (multitap)**](pc-engine-turbografx-16.md#multiplayer-multitap). Check that it has not been disabled in the options. ares only emulates one player. |
| Buttons III to VI do not respond      | Enable the 6-button pad: see [**6-button pad**](pc-engine-turbografx-16.md#id-6-button-pad).                                                                                                  |
| A game does not start with FBNeo      | FBNeo only reads archives named after its PC Engine sets. Use another core.                                                                                                                   |
| A SuperGrafx game has broken graphics | mednafen\_pce\_fast does not emulate the SuperGrafx: put the game in `roms\supergrafx`.                                                                                                       |
| A CD game does not start              | CD games go in `roms\pcenginecd`.                                                                                                                                                             |
