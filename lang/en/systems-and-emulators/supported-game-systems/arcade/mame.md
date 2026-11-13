---
description: MAME Team
---

# MAME

<div align="left"><figure><img src="../../../.gitbook/assets/image (544).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Presentation

**MAME** (Multiple Arcade Machine Emulator) was started in 1997 by Nicola Salmoria. Its first goal is not to play but to **preserve**: documenting how arcade machines work by reproducing them faithfully, so that they do not disappear with their hardware.

Almost thirty years later, MAME emulates tens of thousands of machines: arcade cabinets from every era, and also consoles and computers since it merged with the MESS project in 2015. In RetroBat, the MAME system is for arcade only, other machines have their own system.

Each game is a file called a **romset**, whose name is set by MAME (`sf2.zip` for Street Fighter II). The content of romsets changes from one MAME version to another: a romset must match the version of the emulator you use (see the [**Arcade Guide**](../../arcade-guide.md) page).

## At a glance

<table><thead><tr><th width="247.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\mame</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: mame</td></tr><tr><td><strong>BIOS</strong></td><td>Depends on the romset type (see BIOS)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores; MAME and GroovyMAME with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores (mame)</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores (mame), MAME, GroovyMAME</td></tr></tbody></table>

## Which emulator to choose?

<table><thead><tr><th width="191.5">Emulator</th><th width="154.25">For whom?</th><th width="227.25">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: mame</strong> (default)</td><td>Everyone</td><td>Current MAME inside RetroArch: shaders, decorations, netplay, buttons set game by game by RetroBat.</td><td>Does not like long installation paths (see Known issues).</td></tr><tr><td><strong>mame64</strong></td><td>Advanced users, cabinets</td><td>The official MAME, with all its settings and its controller profiles (IPAC2, X-Arcade).</td><td>—</td></tr><tr><td><strong>groovymame</strong></td><td>CRT screens</td><td>Adapts the screen resolution and refresh rate to each game.</td><td>Needs a suitable screen and hardware.</td></tr><tr><td><strong>libretro: mame2003_plus</strong></td><td>Low-end PCs</td><td>Light, with buttons set game by game like lr-mame.</td><td>Needs its own romset (MAME 0.78 plus additions).</td></tr><tr><td><strong>libretro: mame2016, mame2014, mame2010, mame2003, mame2003_midway, mame2000</strong></td><td>Low-end PCs, old romsets</td><td>Lighter.</td><td>Each core needs the romset of its own version. No buttons set game by game.</td></tr></tbody></table>

**If in doubt, keep libretro: mame.**

### Automatic core selection

As long as you have not chosen an emulator for the system or for the game, RetroBat checks the romset before launching it:

<table><thead><tr><th width="301.5">Your romset…</th><th>Core launched</th></tr></thead><tbody><tr><td>fits libretro: mame</td><td>libretro: mame</td></tr><tr><td>comes from an old MAME version</td><td>The first compatible core, in this order: mame2016, mame2014, mame2010, mame2003_plus, mame2003, mame2000</td></tr><tr><td>is not recognized</td><td>libretro: mame</td></tr></tbody></table>

An old romset therefore starts without any setting, with the core that matches it.

* Only `.zip` files are checked.
* The check covers all the files of the game, BIOS included. With a split romset or without the BIOS files in the zip, the game is often not recognized: libretro: mame is then used.
* As soon as you choose an emulator for the system or for the game, this choice is respected and the check is no longer done.

## BIOS

### BIOS and devices

In addition to its romset, a game may need romsets shared by several games:

<table><thead><tr><th width="115.75">Type</th><th width="344.75">Role</th><th>Examples</th></tr></thead><tbody><tr><td><strong>BIOS</strong></td><td>The base program of an arcade board</td><td><code>neogeo.zip</code>, <code>pgm.zip</code>, <code>naomi.zip</code>, <code>stvbios.zip</code></td></tr><tr><td><strong>Device</strong></td><td>A component common to several boards (sound chip, controller…)</td><td><code>qsound_hle.zip</code>, <code>ym2608.zip</code>, <code>namco51.zip</code></td></tr></tbody></table>

A game can refuse to start because a device romset is missing, even when its BIOS is there.

The need depends on the romset type:

<table><thead><tr><th width="269">Romset type</th><th>Separate BIOS and devices needed?</th></tr></thead><tbody><tr><td>Full non-merged</td><td>No: everything is in the game romset</td></tr><tr><td>Non-merged</td><td>Yes, for files shared by several games</td></tr><tr><td>Split</td><td>Yes</td></tr><tr><td>Merged</td><td>Not for BIOS</td></tr></tbody></table>

See the [**Arcade Guide**](../../arcade-guide.md) page for details on romset types.

### Where to put them?

BIOS and device romsets go at the **root of the** `bios` **folder**, or next to the games in `roms\mame`. MAME searches both folders.

RetroBat does not check that MAME BIOS files are present.

## Which game format?

<table><thead><tr><th width="130.25">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.zip</strong></td><td>The game romset. Do not rename it and do not extract it.</td></tr><tr><td>.7z</td><td>Romset compressed in 7z.</td></tr><tr><td>.chd</td><td>Hard disk, CD or LaserDisc of a game. It goes in a folder named after the game, next to the romset (see the <a href="../../arcade-guide.md"><strong>Arcade Guide</strong></a> page).</td></tr></tbody></table>

Some games also use **samples** (recorded sounds), to place in `bios\mame\samples`.

## Controls

### Automatic configuration

RetroBat configures controllers automatically for all MAME emulators.

Every arcade cabinet has a different panel. RetroBat therefore works in two steps:

1. **The game has a dedicated configuration**: RetroBat ships one for more than 3,000 games, with buttons placed as on the original cabinet. If the game is a clone without configuration, the one of its parent game is used.
2. **Otherwise**, RetroBat applies the default configuration below.

This applies to lr-mame, mame2003\_plus, MAME and GroovyMAME. Other libretro cores keep the core layout.

<table><thead><tr><th width="165.75">Cabinet button</th><th width="259.75">RetroBat controller</th><th>Keyboard</th></tr></thead><tbody><tr><td>Directions</td><td>D-pad / left stick</td><td>Arrows</td></tr><tr><td>Button 1</td><td>WEST</td><td>Left CTRL</td></tr><tr><td>Button 2</td><td>SOUTH</td><td>Left ALT</td></tr><tr><td>Button 3</td><td>EAST</td><td>SPACE</td></tr><tr><td>Button 4</td><td>NORTH</td><td>Left SHIFT</td></tr><tr><td>Button 5</td><td>L1</td><td>Z</td></tr><tr><td>Button 6</td><td>R1</td><td>X</td></tr><tr><td>Button 7</td><td>L2 (MAME, GroovyMAME, mame2003_plus)</td><td>C</td></tr><tr><td>Button 8</td><td>R2 (MAME, GroovyMAME, mame2003_plus)</td><td>V</td></tr><tr><td>Coin</td><td>SELECT</td><td>5</td></tr><tr><td>Start</td><td>START</td><td>1</td></tr><tr><td>Service</td><td>L3 (MAME, GroovyMAME)</td><td>9</td></tr><tr><td>Test</td><td>R3 (MAME, GroovyMAME)</td><td>0</td></tr><tr><td>Pedal 1 / Pedal 2</td><td>R2 / L2 (MAME, GroovyMAME), R1 / L1 (mame2003_plus)</td><td>—</td></tr><tr><td>Wheel, dial, trackball, analog stick</td><td>Left stick</td><td>Mouse</td></tr><tr><td>Second joystick</td><td>Right stick</td><td>—</td></tr></tbody></table>

### Arcade sticks and custom buttons

On an arcade stick, set **CONTROLS > CONTROLLER LAYOUT** to match your panel: RetroBat reproduces the layout of the original cabinet on it. This option applies to lr-mame, mame2003\_plus, MAME and GroovyMAME.

You can also fix the buttons of one game, use an IPAC2 or X-Arcade panel, create your own profile or keep the buttons set in the MAME menu. These methods, and the MAME `.cfg` files, are described on the [**MAME controller mapping**](../../../controllers/specific_mapping/mame64-controller-mapping.md) page.

### Light guns

Turn on **GUNS > ENABLE GUN**. To connect and set up a light gun in RetroBat, see the [**Lightguns**](../../../controllers/supported-controllers/lightguns/) page.

<table><thead><tr><th width="162">Emulator</th><th>How it works</th><th>Useful options</th></tr></thead><tbody><tr><td><strong>libretro: mame</strong></td><td><strong>LIGHTGUN MODE</strong> selects light gun or touch screen.</td><td><strong>SINDEN BUTTONS CONFIGURATION</strong>, <strong>DISABLE CROSSHAIR</strong></td></tr><tr><td><strong>mame64</strong>, <strong>groovymame</strong></td><td>Up to 4 guns. As soon as several guns are connected, each one is assigned to a player.</td><td><strong>FORCE ONE GUN ONLY</strong>, <strong>P1 MOUSE/GUN INDEX</strong> (to P4) to choose which gun goes to which player, <strong>DISABLE CROSSHAIR</strong>, <strong>USE MAMEHOOKER</strong> for recoil and outputs</td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (545).png" alt=""><figcaption></figcaption></figure></div>

### Hotkeys

**MAME and GroovyMAME**

<table><thead><tr><th width="208.25">Hotkey</th><th width="224">Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td>ESC</td></tr><tr><td>HOTKEY + SOUTH</td><td>MAME menu</td><td>TAB</td></tr><tr><td>HOTKEY + WEST</td><td>Save state</td><td>F2</td></tr><tr><td>HOTKEY + NORTH</td><td>Load state</td><td>F4</td></tr><tr><td>HOTKEY + RIGHT</td><td>Fast forward</td><td>SPACE</td></tr><tr><td>HOTKEY + LEFT</td><td>Rewind</td><td>BACKSPACE</td></tr><tr><td>HOTKEY + R1</td><td>Tilt</td><td>T</td></tr><tr><td>—</td><td>Pause</td><td>P</td></tr></tbody></table>

In the MAME menu, **SOUTH** confirms and **EAST** goes back.

**lr-mame** uses RetroArch hotkeys (see the [Hotkeys](../../../navigation/hotkeys.md) page). The MAME menu opens with **START + SOUTH**.

**mame2003\_plus** also uses RetroArch hotkeys. The MAME menu opens with **L3**.

### Service menu

On the keyboard, key **0** opens the test menu of the cabinet and key **9** is the Service button used to move in it.

With MAME and GroovyMAME, both functions are also on the controller: **R3** for test, **L3** for service. The **CONTROLS > TEST/SERVICE ON L3/R3** option, on by default, lets you remove them.

## Folders

<table><thead><tr><th width="351.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>BIOS and devices</td><td><code>bios</code> (root) or <code>roms\mame</code></td></tr><tr><td>Samples</td><td><code>bios\mame\samples</code></td></tr><tr><td>Ini files</td><td><code>bios\mame\ini</code> (GroovyMAME: <code>bios\groovymame\ini</code>)</td></tr><tr><td>Software lists (hash)</td><td><code>bios\mame\hash</code></td></tr><tr><td>Per-game settings (cfg)</td><td><code>saves\mame\cfg</code> (or <code>saves\mame\cfg64</code>)</td></tr><tr><td>Cfg backups</td><td><code>saves\mame\cfgbackup</code> (lr-mame), <code>saves\mame\cfgbackupmame64</code> (MAME)</td></tr><tr><td>Controller profiles</td><td><code>saves\mame\ctrlr</code></td></tr><tr><td>Cabinet memory (NVRAM)</td><td><code>saves\mame\nvram</code></td></tr><tr><td>MAME save states</td><td><code>saves\mame\states</code></td></tr><tr><td>lr-mame save states</td><td><code>saves\mame\libretro.mame</code></td></tr><tr><td>mame2003_plus settings, memory and high scores</td><td><code>saves\mame\mame2003-plus</code></td></tr><tr><td>Your artworks</td><td><code>saves\mame\artwork</code></td></tr><tr><td>Cheats</td><td><code>cheats\mame</code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr><tr><td>RetroBat per-game configurations</td><td><code>system\resources\inputmapping</code></td></tr><tr><td>Your per-game configurations</td><td><code>user\inputmapping</code></td></tr></tbody></table>

RetroBat uses the `bios\mame\artwork` folder to build decorations: do not store your artworks there, they would be overwritten.

## Guides

### Play on a CRT screen with GroovyMAME

GroovyMAME is a MAME version made for CRT screens: it sets the screen resolution and refresh rate to those of the original cabinet.

1. Choose the **groovymame** emulator for the system or for the game.
2. In **VIDEO > SCREEN PROFILE**, choose the profile of your screen:

<table><thead><tr><th width="335.25">Profile</th><th>Screen</th></tr></thead><tbody><tr><td>LCD Arcade (Vewlix) / PC / Modern TV</td><td>Flat screen</td></tr><tr><td>LCD Arcade (vertical)</td><td>Flat screen mounted vertically</td></tr><tr><td>CRT TV 15 kHz</td><td>CRT television</td></tr><tr><td>CRT TV PAL</td><td>PAL CRT television</td></tr><tr><td>CRT Arcade 15 kHz</td><td>Standard arcade monitor</td></tr><tr><td>CRT Arcade 25 kHz</td><td>Medium resolution arcade monitor</td></tr><tr><td>CRT Arcade 31 kHz VGA</td><td>High resolution arcade monitor</td></tr><tr><td>CRT 15 kHz + 25 kHz Combo</td><td>Dual-sync monitor</td></tr><tr><td>CRT 15/25/31 kHz</td><td>Tri-sync monitor</td></tr><tr><td>CRT PC 31 kHz 120 Hz</td><td>PC CRT monitor</td></tr><tr><td>PVM / BVM</td><td>Professional monitor</td></tr></tbody></table>

GroovyMAME has its own ini files, in `bios\groovymame\ini`. Decorations are off by default with this emulator.

## Known issues

<table><thead><tr><th width="351.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Black screen at launch with libretro: mame</td><td>The RetroBat installation path is too long. Install RetroBat in a short folder, for example <code>C:\RetroBat</code>, or use mame64.</td></tr><tr><td>The game starts with another core than libretro: mame</td><td>Its romset comes from an old MAME version and RetroBat chose the compatible core (see Automatic core selection). To force a core, choose it in the game options.</td></tr><tr><td>The game does not start</td><td>The romset does not match the emulator version, or a BIOS or device is missing (see BIOS and the <a href="../../arcade-guide.md"><strong>Arcade Guide</strong></a> page).</td></tr><tr><td>Buttons are not in the right place on my arcade stick</td><td>Set <strong>CONTROLLER LAYOUT</strong> to match your panel (see the <a href="../../../controllers/specific_mapping/mame64-controller-mapping.md"><strong>MAME controller mapping</strong></a> page).</td></tr><tr><td>My settings made in the MAME menu are lost</td><td>Automatic configuration replaces them: see the <a href="../../../controllers/specific_mapping/mame64-controller-mapping.md"><strong>MAME controller mapping</strong></a> page.</td></tr><tr><td>The test menu opens when I press a stick</td><td>With MAME and GroovyMAME, turn off <strong>TEST/SERVICE ON L3/R3</strong>.</td></tr><tr><td>My artworks disappear</td><td>Store them in <code>saves\mame\artwork</code>, not in <code>bios\mame\artwork</code>.</td></tr></tbody></table>
