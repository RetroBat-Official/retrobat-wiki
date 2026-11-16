---
description: Nintendo
---

# Nintendo DS

<div align="left"><figure><img src="../../../../.gitbook/assets/image (606).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **Nintendo DS** is a Nintendo handheld console released in 2004. It has two screens: the bottom one is a touchscreen played with a stylus. It also has a microphone and a wireless link (multiplayer, DS Download Play, Nintendo Wi-Fi Connection). It was followed by the **DS Lite** (2006) and the **DSi** (2008), which adds cameras, an online shop (**DSiWare**) and a few games that only run on that model.

Among its games: **New Super Mario Bros.**, **Mario Kart DS**, **Pokémon Diamond / Pearl**, **Pokémon HeartGold / SoulSilver**, **Pokémon Black / White**, **The Legend of Zelda: Phantom Hourglass**, **Professor Layton**, **Phoenix Wright: Ace Attorney**, **Animal Crossing: Wild World**, **Nintendogs**, **Chrono Trigger**, **Dragon Quest IX**.

RetroBat offers several emulators: the **melondsds** libretro core (default), the **desmume**, **desmume2015**, **melonds** and **noods** cores, **melonDS**, **DeSmuME** and **BizHawk** (melonDS core).

{% embed url="https://en.wikipedia.org/wiki/Nintendo_DS" %}

## At a glance

<table><thead><tr><th width="217.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\nds</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nds .bin .zip .7z .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: melondsds</td></tr><tr><td><strong>BIOS</strong></td><td>None required (DSi: see below)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, every emulator</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, DeSmuME, BizHawk; melonDS with hotkeys (not managed by RetroBat)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, BizHawk</td></tr><tr><td><strong>Netplay</strong></td><td>desmume, desmume2015 cores</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>bios7.bin</code>, <code>bios9.bin</code>, <code>firmware.bin</code> (DS); <code>dsi_bios7.bin</code>, <code>dsi_bios9.bin</code>, <code>dsi_firmware.bin</code>, <code>dsi_nand.bin</code> (DSi), in <code>bios</code></td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="195.75">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: melondsds</strong> (default)</td><td>Follows the melonDS emulator closely. Higher resolution (OpenGL), two screen layouts to switch in game, automatic DSi mode for games that need it, DSiWare, real microphone, save states, RetroAchievements.</td><td>Does not launch a <code>.bin</code> NAND file.</td></tr><tr><td><strong>libretro: desmume</strong></td><td>Netplay, save states, RetroAchievements, higher resolution.</td><td>Less accurate than melonDS. No DSi mode.</td></tr><tr><td><strong>libretro: desmume2015</strong></td><td>Older, lighter DeSmuME version, for modest PCs.</td><td>Few options. No DSi mode.</td></tr><tr><td><strong>libretro: melonds</strong></td><td>Older melonDS core.</td><td>No longer updated, replaced by melondsds. No <code>.bin</code> NAND file.</td></tr><tr><td><strong>libretro: noods</strong></td><td>Recent, lightweight emulator.</td><td>No <code>.bin</code> NAND file.</td></tr><tr><td><strong>melonds</strong></td><td>Latest melonDS release. Launches a <code>.bin</code> NAND file and manages the titles installed in the NAND.</td><td>Save states not managed by RetroBat. Touchscreen with the mouse.</td></tr><tr><td><strong>desmume</strong></td><td>Save states managed by RetroBat, picture filters.</td><td>Touchscreen with the mouse. No DSi mode.</td></tr><tr><td><strong>bizhawk</strong> (melonDS)</td><td>BizHawk tools (recording, TAS), stylus on the right stick or the mouse, RetroAchievements.</td><td>Heavier than the others.</td></tr></tbody></table>

## BIOS

No BIOS is needed for DS games: the emulators have a built-in BIOS. The console files are still useful to boot to the DS menu (**EMULATION > BOOT TO BIOS**) and for **DS Download Play**.

**DS**:

<table><thead><tr><th width="242.75">File</th><th>Folder</th></tr></thead><tbody><tr><td><code>bios7.bin</code></td><td><code>bios</code></td></tr><tr><td><code>bios9.bin</code></td><td><code>bios</code></td></tr><tr><td><code>firmware.bin</code></td><td><code>bios</code></td></tr></tbody></table>

* **melondsds core**: the files are used when present; **EMULATION > USE BUILT-IN BIOS** forces the built-in BIOS.
* **melonDS, desmume core, DeSmuME, BizHawk**: enable **EMULATION > USE EXTERNAL BIOS** (DeSmuME: also **EMULATION > USE EXTERNAL FIRMWARE**).

**DSi** (DSi games, DSiWare, DSi menu):

<table><thead><tr><th width="220.25">File</th><th>Folder</th></tr></thead><tbody><tr><td><code>dsi_bios7.bin</code></td><td><code>bios</code></td></tr><tr><td><code>dsi_bios9.bin</code></td><td><code>bios</code></td></tr><tr><td><code>dsi_firmware.bin</code></td><td><code>bios</code></td></tr><tr><td><code>dsi_nand.bin</code></td><td><code>bios</code></td></tr></tbody></table>

Several NANDs can be kept: add the region to the file name (`dsi_nand_EUR.bin`, `dsi_nand_USA.bin`, `dsi_nand_JPN.bin`, `KOR`, `AUS`, `CHN`), then select it with **EMULATION > DSI NAND REGION** (melondsds core, melonDS). With the melondsds core, AUTO picks the NAND from the game region.

## Which game format?

<table><thead><tr><th width="179">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.nds</strong></td><td>Dump of a DS or DSi cartridge, or of a DSiWare.</td></tr><tr><td><strong>.bin</strong></td><td>DSi NAND file: launches the console menu and its installed titles (see <a href="nintendo-ds.md#launching-the-menu-of-a-dsi-nand-.bin"><strong>Guides</strong></a>). Only with melonDS and BizHawk.</td></tr><tr><td><strong>.zip</strong> / <strong>.7z</strong></td><td>Archive containing a <code>.nds</code>.</td></tr><tr><td><strong>.decomp</strong></td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

## Controls

### Automatic setup

Buttons are mapped by position, as on the console:

<table><thead><tr><th width="289">RetroBat controller</th><th>DS</th></tr></thead><tbody><tr><td>EAST / SOUTH / NORTH / WEST</td><td>A / B / X / Y</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>L1 / R1</td><td>L / R</td></tr><tr><td>START / SELECT</td><td>START / SELECT</td></tr></tbody></table>

The DS-specific functions (stylus, microphone, lid, screens) depend on the emulator:

<table><thead><tr><th width="161.5">Emulator</th><th width="162.25">Stylus</th><th width="129">Microphone</th><th width="98.5">Lid</th><th>Screens</th></tr></thead><tbody><tr><td><strong>melondsds core</strong></td><td>Right stick, R3 to touch</td><td>L2</td><td>L3</td><td>R2: next layout</td></tr><tr><td><strong>melonds core</strong></td><td>Right stick, R3 to touch</td><td>L2</td><td>L3</td><td>R2: swap</td></tr><tr><td><strong>desmume, desmume2015 cores</strong></td><td>Right stick, R2 to touch</td><td>L3</td><td>L2</td><td>R3: swap</td></tr><tr><td><strong>noods core</strong></td><td>Right stick, R3 to touch</td><td>L2</td><td>—</td><td>R2: swap</td></tr><tr><td><strong>melonDS</strong></td><td>Mouse</td><td>L2</td><td>L3</td><td>R2: swap</td></tr><tr><td><strong>DeSmuME</strong></td><td>Mouse</td><td>—</td><td>—</td><td>—</td></tr><tr><td><strong>BizHawk</strong></td><td>Right stick, R2 to touch (or mouse)</td><td>L2</td><td>—</td><td>—</td></tr></tbody></table>

| Emulator                   | Tattoo                                                                                                                                                 |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| melondsds core             | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melondsds.png?raw=true" alt="" data-size="original">             |
| desmume, desmume2015 cores | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds.png?raw=true" alt="" data-size="original">                       |
| melonds core               | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds.png?raw=true" alt="" data-size="original">               |
| noods core                 | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_noods.png?raw=true" alt="" data-size="original">                 |
| melonDS                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds_standalone.png?raw=true" alt="" data-size="original">    |
| melonDS (left stick)       | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds_standalone_ls.png?raw=true" alt="" data-size="original"> |
| BizHawk                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_bizhawk.png?raw=true" alt="" data-size="original">               |
| BizHawk (mouse)            | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_bizhawk_mouse.png?raw=true" alt="" data-size="original">         |

### Control options

* **melondsds core**: **CONTROLS > TOUCH MODE** (POINTER: mouse; JOYSTICK: right stick), **CONTROLS > CURSOR MODE**, **CONTROLS > MICROPHONE EMULATION** (real microphone, blow, noise, silence) and **CONTROLS > MICROPHONE BUTTON MODE**.
* **melonds core**: **CONTROLS > TOUCH MODE** (JOYSTICK by default) and **CONTROLS > MICROPHONE EMULATION**.
* **desmume, desmume2015 cores**: **CONTROLS > EMULATE STYLUS WITH RIGHT STICK** (on by default).
* **noods core**: **CONTROLS > TOUCH MODE**, **CONTROLS > SHOW TOUCHSCREEN POINTER**, **CONTROLS > SWAP SCREEN BUTTON MODE**.
* **melonDS**: **CONTROLS > USE ANALOG STICK** (left stick instead of the D-pad), **CONTROLS > XBOX LAYOUT** (buttons by their name on an Xbox controller), **CONTROLS > MICROPHONE EMULATION**.
* **DeSmuME**: **CONTROLS > USE ANALOG STICK**, **CONTROLS > INVERT FACE BUTTONS**.
* **BizHawk**: **CONTROLS > USE MOUSE** (stylus with the mouse instead of the right stick).

### Hotkeys

melonDS, DeSmuME and BizHawk use the RetroBat hotkeys (through PadToKey):

<table><thead><tr><th>Action</th><th>Controller</th><th width="149">melonDS</th><th>DeSmuME, BizHawk</th></tr></thead><tbody><tr><td>Exit</td><td>HOTKEY + START</td><td>yes</td><td>yes</td></tr><tr><td>Pause</td><td>HOTKEY + SOUTH</td><td>yes</td><td>yes</td></tr><tr><td>Save state</td><td>HOTKEY + WEST</td><td>slot 1</td><td>yes</td></tr><tr><td>Load state</td><td>HOTKEY + NORTH</td><td>slot 1</td><td>yes</td></tr><tr><td>Previous / next slot</td><td>HOTKEY + Down / Up</td><td>—</td><td>yes</td></tr><tr><td>Slow motion (melonDS) / rewind (BizHawk)</td><td>HOTKEY + Left</td><td>yes</td><td>BizHawk</td></tr><tr><td>Fast forward (hold)</td><td>HOTKEY + Right</td><td>yes</td><td>yes</td></tr><tr><td>Screenshot</td><td>HOTKEY + R3</td><td>—</td><td>yes</td></tr><tr><td>Fullscreen</td><td>HOTKEY + L3</td><td>yes</td><td>BizHawk</td></tr></tbody></table>

The libretro cores use the RetroArch hotkeys.

For more details, see the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="265.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>libretro cores, melonDS: saves</td><td><code>saves\nds</code></td></tr><tr><td>libretro cores: save states</td><td><code>saves\nds\libretro.&#x3C;core></code></td></tr><tr><td>melonDS: save states</td><td><code>saves\nds\melonds\sstates</code></td></tr><tr><td>DeSmuME: saves</td><td><code>saves\nds\DeSmuME</code> (save states: <code>saves\nds\DeSmuME\stateslots</code>)</td></tr><tr><td>BizHawk: saves</td><td><code>saves\nds\bizhawk</code> (save states: <code>saves\nds\bizhawk\sstates\melonDS</code>)</td></tr><tr><td>Cheats</td><td><code>cheats\melonds</code> (melonDS), <code>cheats\desmume</code> (DeSmuME)</td></tr><tr><td>DeSmuME: screenshots</td><td><code>screenshots\DeSmuME</code></td></tr></tbody></table>

## Guides

### Playing DSi games and DSiWare

1. Place the DSi files in `bios` (see **BIOS**).
2. **melondsds core**: leave **EMULATION > CONSOLE TYPE** on AUTO, the DSi is selected for games that need it. For a DSiWare, select DSI for that game.
3. **melonDS**: select **EMULATION > CONSOLE TYPE** DSi for that game.

### Launching the menu of a DSi NAND (.bin)

A NAND file holds the DSi menu and the titles installed in its memory (DSiWare). Place it in `roms\nds`, with the `.bin` extension, then launch it with **melonDS** (the simplest) or **BizHawk**: the console boots to its menu. The NAND is used as is: DSiWare saves and installed titles stay in it.

* The DSi files (`dsi_bios7.bin`, `dsi_bios9.bin`, `dsi_firmware.bin`) must be in `bios`.
* At least one `.nds` game must be present: in `roms\nds` for melonDS, in the same folder as the NAND for BizHawk (the console boots with that cartridge inserted).
* The libretro cores do not launch NANDs: RetroBat warns at launch, select melonDS or BizHawk for that file.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (607).png" alt="" width="544"><figcaption></figcaption></figure></div>

### Adding titles to a NAND

Only melonDS can add or remove titles in a NAND:

1. Launch melonDS from the `emulators\melonds` folder.
2. **Config > Emu settings** menu, **DSi mode** tab: select the NAND to edit with **Browse…**, then **OK**.
3. **System > Manage DSi titles** menu: **Import title…**, select the DSiWare to install, then **OK**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (608).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="danger" %}
A NAND is easily corrupted by a wrong operation, and its size is limited: keep a copy. If melonDS shows a black screen when launching a NAND, it is not valid.
{% endhint %}

### Screen layouts

* **melondsds core**: **VIDEO > SCREEN LAYOUT POSITIONING 1** and **VIDEO > SCREEN LAYOUT POSITIONING 2** set two layouts (top-bottom and right-left by default); R2 switches between them in game.
* **Other emulators**: **VIDEO > SCREEN LAYOUT POSITIONING** and **VIDEO > SWAP SCREEN**.

## Known issues

<table><thead><tr><th width="366.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>RetroBat says the emulator does not support this format when launching a <code>.bin</code></td><td>NANDs only launch with melonDS or BizHawk: select one of them for that file.</td></tr><tr><td>melonDS refuses to launch a game in DSi mode ("dsi bios files are missing")</td><td>Place <code>dsi_bios7.bin</code>, <code>dsi_bios9.bin</code>, <code>dsi_firmware.bin</code> and the NAND in <code>bios</code>.</td></tr><tr><td>melonDS refuses to launch a NAND (no <code>.nds</code> game found)</td><td>Add at least one <code>.nds</code> game (see <a href="nintendo-ds.md#launching-the-menu-of-a-dsi-nand-.bin"><strong>Launching the menu of a DSi NAND</strong></a>).</td></tr><tr><td><strong>EMULATION > BOOT TO BIOS</strong> has no effect</td><td>Place <code>bios7.bin</code>, <code>bios9.bin</code> and <code>firmware.bin</code> in <code>bios</code>, and enable <strong>EMULATION > USE EXTERNAL BIOS</strong> (melonDS, DeSmuME, BizHawk).</td></tr><tr><td>The stylus does not respond to the controller with melonDS or DeSmuME</td><td>These emulators use the mouse: use a libretro core or BizHawk to play with the right stick.</td></tr></tbody></table>
