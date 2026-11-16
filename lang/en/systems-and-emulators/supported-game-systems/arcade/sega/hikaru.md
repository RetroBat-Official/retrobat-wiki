---
description: Sega
---

# Sega Hikaru

<div align="left"><figure><img src="../../../../.gitbook/assets/image (586).png" alt="" width="300"><figcaption></figcaption></figure></div>

## Overview

The **Sega Hikaru** is an arcade board released in 1999. Based on the Naomi, it adds a graphics processor designed by Sega, with lighting effects well ahead of its time (per-pixel lighting, reflections). Too expensive to produce, it was soon replaced by the Naomi 2: only six games were released on it.

The library: **Brave Firefighters**, **Air Trix**, **NASCAR Arcade**, **Planet Harriers**, **Star Wars Racer Arcade** and **Cyber Troopers Virtual-On Force**.

RetroBat offers two emulators: **Odin** (default), an emulator dedicated to the Hikaru, and **Demul**.

{% embed url="https://en.wikipedia.org/wiki/List_of_Sega_arcade_system_boards#Sega_Hikaru" %}

## At a glance

<table><thead><tr><th width="252.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\hikaru</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip</td></tr><tr><td><strong>Default emulator</strong></td><td>odin</td></tr><tr><td><strong>BIOS</strong></td><td><code>hikaru.zip</code> and <code>mie.zip</code> in <code>bios</code></td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>Odin; Demul through hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>Odin (Brave Firefighters)</td></tr><tr><td><strong>Wheels</strong></td><td>Odin (NASCAR Arcade)</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>jvs13551.zip</code>, <code>18wheelr.zip</code>, <code>srally2.zip</code> (Odin)</td></tr></tbody></table>

## Which emulator to choose?

<table><thead><tr><th width="167">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>odin</strong> (default)</td><td>Low-level emulator dedicated to the Hikaru: all six games, higher resolution, CRT filter, save states, light guns (Brave Firefighters), force feedback wheel (NASCAR Arcade), controller rumble.</td><td>Recent emulator (version 0.1).</td></tr><tr><td><strong>demul</strong></td><td>Long-standing emulator, also used for the Naomi and the Atomiswave.</td><td>Lower compatibility. Save states not managed by RetroBat.</td></tr></tbody></table>

## BIOS

The games need two MAME archives, shared by all the games of the system:

<table><thead><tr><th width="147">File</th><th>Folder</th><th>Used by</th></tr></thead><tbody><tr><td><code>hikaru.zip</code></td><td><code>bios</code> (or <code>roms\hikaru</code>)</td><td>Odin, Demul</td></tr><tr><td><code>mie.zip</code></td><td><code>bios</code> (or <code>roms\hikaru</code>)</td><td>Odin, Demul</td></tr></tbody></table>

Both emulators look for these archives in `bios`, then in the games folder. Their content depends on the MAME version: there is no reference MD5 for the archives.

Odin can also use the optional `jvs13551.zip`, `18wheelr.zip` and `srally2.zip` sets.

When a file is missing, Odin shows its name and the archive that holds it (for example "missing files : 93c46.ic115 (hikaru.zip)").

## Which game format?

Games are MAME `.zip` archives, to be kept as they are, without extracting or renaming them (`airtrix.zip`, `braveff.zip`, `pharrier.zip`, `sgnascar.zip`, `swracer.zip`, `von4.zip`).

The original versions `airtrixo` and `sgnascaro` need their parent game (`airtrix`, `sgnascar`) in the same folder, unless you use a non-merged romset.

## Controls

### Automatic configuration

RetroBat configures the controllers automatically for both emulators. The **AUTOCONFIGURE CONTROLLERS** option lets you keep your own configuration.

For every game: **START** = Start, **SELECT** = coin, **L3** = Service, **R3** = Test. On the keyboard: 1 / 2 = player 1 / 2 Start, 5 / 6 = coin, 9 = Service, 0 = Test.

### Odin

Odin handles gamepads and joysticks. Each player keeps their controller from one session to the next, even with two identical controllers. Brave Firefighters is played by two players on the same cabinet; the other games are single player (linked cabinets are not emulated).

Buttons are set per game in `odin.yml` (`system\resources\inputmapping`, editable copy in `user\inputmapping`):

<table><thead><tr><th width="339">Game</th><th>Controls</th></tr></thead><tbody><tr><td>Air Trix (<code>airtrix</code>, <code>airtrixo</code>)</td><td>Left stick: turn; right stick: tilt the board; D-pad left / right: left / right; L1 / R1: up / down</td></tr><tr><td>Brave Firefighters (<code>braveff</code>)</td><td>Left stick, light gun or mouse: aim the nozzle; R2: water; L2: fog</td></tr><tr><td>Planet Harriers (<code>pharrier</code>)</td><td>Left stick: flight stick; R2: shot; L2: missile; SOUTH: bomb; L1 / R1: left / right VR buttons</td></tr><tr><td>Star Wars Racer Arcade (<code>swracer</code>)</td><td>Left stick (up / down): left lever; right stick (up / down): right lever; SOUTH: boost; R2: brake; D-pad left / right: left / right buttons</td></tr><tr><td>NASCAR Arcade (<code>sgnascar</code>, <code>sgnascaro</code>)</td><td>Left stick: steering; R2 / L2: gas / brake; R1 / L1: gear up / down; NORTH: view</td></tr><tr><td>Cyber Troopers Virtual-On Force (<code>von4</code>)</td><td>Left stick: left lever; right stick: right lever; L2 / R2: left / right triggers; L1 / R1: left / right turbo; NORTH: PIB button</td></tr></tbody></table>

Options of the **CONTROLS** menu:

* **JOYSTICK DEADZONE**: deadzone of the sticks (3 % by default).
* **INVERT Y AXIS**: in Planet Harriers, the cabinet climbs when you pull the stick back; the option makes it climb when you push the stick up.
* **ENABLE RUMBLE**: the controller shakes like the cabinet (on by default).
* **EXTERNAL OUTPUTS**: sends the lamps, the nozzle vibration and the drive board to external tools (Hook Of The Reaper, QMamehook...).

### Demul

Demul uses the same layout for every game:

<table><thead><tr><th width="266.5">Cabinet button</th><th>Controller</th></tr></thead><tbody><tr><td>Buttons 1 to 4</td><td>SOUTH, EAST, WEST, NORTH</td></tr><tr><td>Buttons 5 to 8</td><td>L1, R1, L2, R2</td></tr><tr><td>Analog controls</td><td>Left stick and right stick</td></tr><tr><td>Directions</td><td>D-pad</td></tr></tbody></table>

The **CONTROLS > ANALOG DEADZONE** option sets the deadzone of the sticks.

### Light guns

Brave Firefighters is played with light guns in Odin, up to two players. Enable **GUNS > ENABLE GUN**.

* Left click (trigger): water; right click: fog; middle click: Start.
* Without a light gun, the mouse aims for player 1 (and so does the left stick of the controller).
* With a DolphinBar, the Wiimote buttons are coin and Start (first gun: left / right, second gun: down / up).
* **USE ONE GUN ONLY** sets up a single gun, **INVERT TRIGGER/RELOAD** swaps water and fog, **SINDEN BORDER SIZE** widens the white border of Sinden guns.

For more details on light guns, see the [**Lightguns**](../../../../controllers/supported-controllers/lightguns/) page.

### Wheels

NASCAR Arcade is played with a wheel in Odin, with force feedback. Enable **WHEELS > ENABLE WHEEL**: the wheel becomes player 1.

* **WHEEL ROTATION**: degrees of rotation to reach full lock (270° by default, like the cabinet).
* **FORCE FEEDBACK STRENGTH**: from 50 to 200 %, or off.
* Buttons are set per wheel type in `model3_wheels.yml` (the same file as Supermodel). Odin reads `odin_wheels.yml` first if it exists.

For more details on wheels, see the [**Wheels**](../../../../controllers/supported-controllers/wheels.md) page.

### Hotkeys

#### **Odin**

<table><thead><tr><th width="199.5">Hotkey</th><th>Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td>Escape</td></tr><tr><td><strong>HOTKEY + SOUTH</strong></td><td>Odin menu</td><td>F10</td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Load state</td><td>F4</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test</td><td>9 / 0</td></tr><tr><td>—</td><td>Pause</td><td>P</td></tr><tr><td>—</td><td>Reset</td><td>Ctrl + R</td></tr><tr><td>—</td><td>Fullscreen</td><td>F11 or Alt + Enter</td></tr><tr><td>—</td><td>Card (Virtual-On Force)</td><td>F6</td></tr><tr><td>—</td><td>Show / hide the cursor</td><td>F7</td></tr></tbody></table>

Odin's own controller shortcuts also stay available with the **Guide** button: Guide alone = menu, Guide + SELECT = pause, Guide + R1 / L1 = save / load, Guide + START = quit.

Keyboard keys can be customized, see the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

#### **Demul**

<table><thead><tr><th width="208.25">Hotkey</th><th>Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td></td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Demul save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Demul load state</td><td>F4</td></tr><tr><td><strong>HOTKEY + L3</strong></td><td>Fullscreen</td><td>Alt + Enter</td></tr></tbody></table>

Demul save states stay in Demul: they do not show up in the save state manager.

## Folders

<table><thead><tr><th width="362.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>BIOS</td><td><code>bios</code> (<code>hikaru.zip</code>, <code>mie.zip</code>)</td></tr><tr><td>Odin: NVRAM (cabinet settings and high scores)</td><td><code>saves\hikaru\odin</code></td></tr><tr><td>Odin: save states (managed by RetroBat)</td><td><code>saves\hikaru\odin\sstates</code></td></tr><tr><td>Odin: save states (emulator folder, one per game)</td><td><code>saves\hikaru\odin\states</code></td></tr><tr><td>Odin: configuration</td><td><code>emulators\odin\odin.ini</code></td></tr><tr><td>Odin: log (launch errors)</td><td><code>emulators\odin\odin.log</code></td></tr><tr><td>Odin: button mapping</td><td><code>system\resources\inputmapping\odin.yml</code> (editable copy in <code>user\inputmapping</code>)</td></tr><tr><td>Odin: wheel buttons</td><td><code>system\resources\inputmapping\wheels\model3_wheels.yml</code> (or <code>user\inputmapping\odin_wheels.yml</code>)</td></tr><tr><td>Demul: NVRAM</td><td><code>saves\hikaru\demul</code></td></tr><tr><td>Demul: configuration</td><td><code>emulators\demul\Demul.ini</code>, <code>padDemul.ini</code></td></tr></tbody></table>

## Guides

### Service menu

The test menu of each cabinet gives access to the game settings (difficulty, credits, calibration...). **R3** (or **0** on the keyboard) opens the test menu, **L3** (or **9**) moves in it.

### Save states (Odin)

Odin keeps a single save state per game, replaced at each **HOTKEY + WEST**. RetroBat copies each new state to a new slot: you find them all in the save state manager and can start the game from any of them. Odin does not save a screenshot: the manager shows the RetroBat save state icon.

### Decorations

By default, Odin shows the RetroBat decorations. The **USE EMULATOR BEZELS** option shows the bezels of the Odin-Artwork pack instead, to be extracted in `emulators\odin`.

### Other useful options (Odin)

<table><thead><tr><th width="335.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Raises the rendering resolution (up to 6x).</td></tr><tr><td><strong>VERTICAL SYNC</strong></td><td>Off by default; <strong>ADAPTIVE</strong> does not wait for the display when a frame is late.</td></tr><tr><td><strong>VISUAL RENDERING > CRT FILTER</strong></td><td>Look of a Sega monitor (29 inch) or a Sega projector (50 inch).</td></tr><tr><td><strong>VISUAL RENDERING > ANISOTROPIC FILTERING</strong></td><td>Sharper textures seen at an angle.</td></tr><tr><td><strong>VISUAL RENDERING > 2D LAYER UPSCALING</strong></td><td>Filter of the 2D layers (HUD, backgrounds) at higher resolutions.</td></tr><tr><td><strong>AUDIO > SOUND BOARDS</strong></td><td>Planet Harriers, NASCAR Arcade, Star Wars Racer Arcade: main board only, mix or 4 channels.</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td>OpenGL (default) or Vulkan.</td></tr></tbody></table>

#### **Demul**

**INTERNAL RESOLUTION**, **GAME ASPECT RATIO** (4:3, 16:9 or stretched), **EMULATION > CPU MODE**.

## Known issues

<table><thead><tr><th width="326.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Odin shows "missing files" at launch</td><td>The message gives the missing file and archive: add <code>hikaru.zip</code> / <code>mie.zip</code> to <code>bios</code>, or update the game romset.</td></tr><tr><td><code>airtrixo</code> or <code>sgnascaro</code> does not start</td><td>Put the parent game (<code>airtrix</code>, <code>sgnascar</code>) in <code>roms\hikaru</code>, or use a <a href="../../../arcade-guide.md#romset-types">non-merged romset</a>.</td></tr><tr><td>Planet Harriers: the stick is inverted</td><td>Enable <strong>CONTROLS > INVERT Y AXIS</strong>.</td></tr><tr><td>Odin is not shown on the right monitor</td><td>Enable <strong>VIDEO > DISABLE FULLSCREEN</strong>.</td></tr></tbody></table>
