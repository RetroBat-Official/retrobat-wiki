---
description: Sega
---

# Sega Titan-Video

<div align="left"><figure><img src="../../../../.gitbook/assets/image (609).png" alt="" width="376"><figcaption></figcaption></figure></div>

## Overview

The **ST-V** (Sega Titan Video) is an arcade board released by Sega in 1994. Its hardware is almost identical to the Saturn (two SH-2 CPUs, VDP1 and VDP2 graphics chips), so its games could be quickly ported to the console. Games come on cartridges. Being cheap, the board was used by Sega and many publishers until the early 2000s.

Its games include **Radiant Silvergun**, **Die Hard Arcade**, **Virtua Fighter Remix**, **Shienryu**, **Cotton 2**, **Final Fight Revenge**, **Astra Superstars**, **Decathlete**, **Golden Axe: The Duel**, **Puyo Puyo Sun**, **Columns '97**, **Baku Baku Animal**, **Groove on Fight** and **Funky Head Boxers**.

RetroBat offers several emulators: the **kronos** (default) and **mednafen\_saturn** libretro cores, the **mame** libretro core (and its older versions), **Mednafen** and **MAME**.

{% embed url="https://en.wikipedia.org/wiki/List_of_Sega_arcade_system_boards#Sega_ST-V" %}

## At a glance

<table><thead><tr><th width="222.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\segastv</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: kronos</td></tr><tr><td><strong>BIOS</strong></td><td><code>stvbios.zip</code> in <code>bios</code>; <code>epr-20091.ic8</code>, <code>epr-17952a.ic8</code>, <code>epr-17954a.ic8</code> in <code>bios</code> (Mednafen)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, every emulator (per-game mapping for the mednafen_saturn, mame and mame2003_plus cores)</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="189.5">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: kronos</strong> (default)</td><td>Fast Saturn and ST-V emulator, upscaling (up to 8x), BIOS region selection.</td><td>Requires an OpenGL 4.3 graphics card. No per-game button placement.</td></tr><tr><td><strong>libretro: mednafen_saturn</strong></td><td>Very accurate emulation, buttons placed as on the cabinet for each game, arcade layouts.</td><td>More demanding.</td></tr><tr><td><strong>libretro: mame</strong></td><td>Wide compatibility, BIOS version selection, per-game mapping, arcade layouts.</td><td>Current MAME romset.</td></tr><tr><td><strong>libretro: mame2016</strong>, <strong>mame2014</strong>, <strong>mame2010</strong>, <strong>mame2003_plus</strong>, <strong>mame2003</strong></td><td>Older MAME versions, lighter (per-game mapping with mame2003_plus).</td><td>Each core requires the romset of its MAME version, fewer working games.</td></tr><tr><td><strong>mednafen</strong></td><td>Same emulation as the mednafen_saturn core, as a standalone emulator.</td><td>About forty supported games. Requires the BIOS files outside the archive. No per-game button placement.</td></tr><tr><td><strong>mame</strong></td><td>Standalone MAME.</td><td>Current MAME romset. No per-game button placement for ST-V.</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="284.5">File</th><th width="148.5">Folder</th><th>Used by</th></tr></thead><tbody><tr><td><code>stvbios.zip</code></td><td><code>bios</code></td><td>every emulator except Mednafen (the kronos core also accepts <code>bios\kronos</code>)</td></tr><tr><td><code>stvbios.zip</code> of the core's version</td><td><code>roms\segastv</code></td><td>older mame cores (mame2016, mame2014, mame2010, mame2003_plus, mame2003)</td></tr><tr><td><code>epr-20091.ic8</code> (Japan)</td><td><code>bios</code></td><td>Mednafen</td></tr><tr><td><code>epr-17952a.ic8</code> (USA)</td><td><code>bios</code></td><td>Mednafen</td></tr><tr><td><code>epr-17954a.ic8</code> (Europe)</td><td><code>bios</code></td><td>Mednafen</td></tr></tbody></table>

`stvbios.zip` is the ST-V BIOS in MAME format. Placed in `bios`, it is used by the kronos core, the mednafen\_saturn core (which reads the file of the game's region directly from it), the mame core and MAME.\
Its content depends on the MAME version: older mame cores need the `stvbios.zip` of their romset, next to the games.\
Mednafen (standalone emulator) does not read the archive: copy `epr-20091.ic8`, `epr-17952a.ic8` and `epr-17954a.ic8`, found in `stvbios.zip`, to `bios`.\
Each game uses the one of its region.

<details>

<summary>Content of stvbios.zip</summary>

```
epr-17740.ic8
epr-17740a.ic8
epr-17741a.ic8
epr-17742a.ic8
epr-17951a.ic8
epr-17952a.ic8
epr-17953a.ic8
epr-17954a.ic8
epr-19730.ic8
epr-19854.ic8
epr-20091.ic8
epr-23603.ic8
stv110.bin
stv1061.bin
stvbios.nv
```

</details>

## Which game format?

Games are `.zip` archives in MAME format, to keep as they are, without extracting or renaming them (`rsgun.zip`, `diehard.zip`, `shienryu.zip`…). Clones need their parent game in the same folder.

The kronos core, the mednafen\_saturn core, Mednafen, the mame core and MAME use the current MAME romset. The older mame cores (mame2016, mame2014, mame2010, mame2003\_plus, mame2003) need the romset of their version.

## Controls

### Automatic setup

<table><thead><tr><th width="234">Cabinet</th><th>Controller</th></tr></thead><tbody><tr><td>Joystick</td><td>D-pad, left stick</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Coin</td><td>SELECT</td></tr><tr><td>Test / Service</td><td>R3 / L3 (mame cores: keyboard, see below)</td></tr></tbody></table>

* **mednafen\_saturn**, **mame** and **mame2003\_plus cores**: button placement is defined per game, to match the cabinet layout (default: buttons 1 to 4 on WEST, SOUTH, EAST, NORTH, buttons 5 and 6 on L1 and R1). **CONTROLS > CONTROLLER LAYOUT** selects the layout for an arcade stick (6 or 8 buttons). Files used: `libretro_mednafen_saturn_segastv.yml` (mednafen\_saturn core), `libretro_mame.yml` (mame and mame2003\_plus cores), see the [**MAME controller mapping**](../../../../controllers/specific_mapping/mame64-controller-mapping.md) page.
* **kronos core**: buttons 1 to 4 on SOUTH, EAST, WEST, NORTH; 6-button games: WEST, NORTH, L1, SOUTH, EAST, R1. Test and Service are on by default; **EMULATION > ENABLE SERVICE MENU** turns them off.
* **Mednafen**: cabinet buttons on the Saturn pad buttons, adjustable with **CONTROLS > BUTTON LAYOUT** and **CONTROLS > INVERT TRIGGERS AND SHOULDERS**. Test and Service also on `0` and `9` on the keyboard.
* **MAME**: cabinet buttons in controller order. Test and Service also on `0` and `9` on the keyboard; **CONTROLS > TEST/SERVICE ON L3/R3** removes them from the controller.
* **mame2016**, **mame2014**, **mame2010**, **mame2003 cores**: default core configuration, no per-game placement.
* **mame cores** (all versions): Test and Service are not on the controller; with the mame core, use `0` (Test) and `9` (Service) on the keyboard.

### Hotkeys

All emulators use the default RetroBat hotkeys (save, load, screenshot…). For more details, see the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="261.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>BIOS</td><td><code>bios</code> (kronos core: also <code>bios\kronos</code>; older mame cores: <code>roms\segastv</code>)</td></tr><tr><td>libretro cores: save states</td><td><code>saves\segastv\libretro.&#x3C;core></code></td></tr><tr><td>Per-game mapping (mednafen_saturn core)</td><td><code>system\resources\inputmapping\libretro_mednafen_saturn_segastv.yml</code> (editable copy in <code>user\inputmapping</code>)</td></tr></tbody></table>

## Guides

### Test menu

The cabinet test menu lets you set credits, difficulty or check the controls. In game, press **R3** (Test); **L3** (Service) adds a service credit. With the mame cores, use the keyboard (see [**Controls**](sega-stv.md#controls)).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (610).png" alt=""><figcaption></figcaption></figure></div>

### BIOS region

The region changes the language and sometimes the game content (texts, censorship).

* **kronos core**: **EMULATION > ST-V REGION** (Europe by default, USA, Japan, Taiwan). The region is ignored if the game does not support it.
* **mame core**: **EMULATION > ST-V BIOS** selects the exact BIOS version (Japan, Europe, USA, Taiwan, development).
* **Mednafen**, **mednafen\_saturn core**, **older mame cores**: the region follows the game.

### Other useful options

<table><thead><tr><th width="394">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong> (kronos core)</td><td>2x, 4x or 8x rendering.</td></tr><tr><td><strong>VISUAL RENDERING > IMPROVED MESH</strong> (kronos and mednafen_saturn cores)</td><td>Replaces meshed transparency with real transparency.</td></tr><tr><td><strong>VISUAL RENDERING > IMPROVED BANDING</strong> (kronos core)</td><td>Gouraud shading instead of flat shading.</td></tr><tr><td><strong>VIDEO > DEINTERLACING METHOD</strong> (mednafen_saturn core)</td><td>For games in interlaced high resolution.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="345.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The kronos core does not start the game</td><td>Check <code>stvbios.zip</code> in <code>bios</code> (or <code>bios\kronos</code>), and OpenGL 4.3 support of the graphics card.</td></tr><tr><td>Mednafen does not start the game</td><td>Copy <code>epr-20091.ic8</code>, <code>epr-17952a.ic8</code> and <code>epr-17954a.ic8</code> (from <code>stvbios.zip</code>) to the root of <code>bios</code>.</td></tr><tr><td>The mednafen_saturn core, the mame core or MAME does not start the game</td><td>Put <code>stvbios.zip</code> in <code>bios</code>: <code>bios\kronos</code> is only used by the kronos core.</td></tr><tr><td>Astra Superstars, Decathlete, Final Fight Revenge, Steep Slope Sliders, Tecmo World Cup '98 or Touryuu Densetsu Elan Doree do not work with Mednafen</td><td>These games are not supported by Mednafen: use the kronos core or the mame core.</td></tr><tr><td>A game does not start with an older mame core</td><td>Use the romset of the core's MAME version, or the mame core.</td></tr><tr><td>Test and Service do not respond with the kronos core</td><td>Check that <strong>EMULATION > ENABLE SERVICE MENU</strong> is not turned off.</td></tr></tbody></table>
