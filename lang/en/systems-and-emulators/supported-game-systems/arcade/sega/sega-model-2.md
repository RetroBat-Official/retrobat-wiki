---
description: Sega
---

# Sega Model 2

<div align="left"><figure><img src="../../../../.gitbook/assets/image (570).png" alt="" width="259"><figcaption></figcaption></figure></div>

## Overview

The **Sega Model 2** is Sega's second 3D arcade board, released in 1994. It follows the Model 1 and adds texture mapping, filtering and anti-aliasing, giving its games a look far ahead of the consoles of the time. Several revisions followed (Model 2, 2A-CRX, 2B-CRX, 2C-CRX).

The library counts around forty games, including many arcade classics: **Daytona USA**, **Virtua Fighter 2**, **Virtua Cop** 1 and 2, **Sega Rally Championship**, **The House of the Dead**, **Dead or Alive**, **Fighting Vipers**, **Virtual On** and **Sega Touring Car Championship**.

RetroBat offers six emulators: **m2emulator** (ElSemi's historical emulator, in a multi-core or single-core version), **Keisho** (formerly sm2-emu, an emulator dedicated to Model 1, 2 and 3), the **sm2** libretro core (derived from sm2-emu), **Supermodel**, and **MAME** as a standalone emulator or as a libretro core.

{% embed url="https://en.wikipedia.org/wiki/List_of_Sega_arcade_system_boards#Sega_Model_2" %}

## At a glance

<table><thead><tr><th width="232.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\model2</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>m2emulator (multicpu)</td></tr><tr><td><strong>BIOS</strong></td><td>None (the sm2 libretro core uses <code>bios\sm2-emu\games.xml</code>, see BIOS)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, Keisho; Supermodel and MAME with hotkeys; not with m2emulator</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>libretro mame core</td></tr><tr><td><strong>Guns</strong></td><td>m2emulator, Keisho, sm2 libretro core, MAME</td></tr><tr><td><strong>Wheels</strong></td><td>m2emulator, Keisho, Supermodel</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="212">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>m2emulator</strong> (default)</td><td>The reference: all games, per-game controls, guns (with DemulShooter), wheels and force feedback.</td><td>Old (Direct3D 9). No save states.</td></tr><tr><td><strong>Keisho</strong> / <strong>libretro: sm2</strong></td><td>Modern emulators: the four Model 2 boards (original, 2A, 2B, 2C), upscaling, Vulkan / OpenGL, CRT filter, save states, rewind.</td><td>Recent development.</td></tr><tr><td><strong>supermodel</strong></td><td>Also handles Model 2 (about 90 romsets), widescreen mode.</td><td>Recent Model 2 support. Save states with the keyboard only.</td></tr><tr><td><strong>libretro: mame</strong> / <strong>mame64</strong></td><td>The only emulator with netplay (libretro core).</td><td>Slower, compatibility varies between games.</td></tr></tbody></table>

**m2emulator** comes in two versions: **multicpu** (default) spreads emulation over several CPU cores; **singlecpu** is worth a try if a game misbehaves.

## BIOS

The Model 2 has no BIOS.

The **sm2 libretro core** needs its game database `bios\sm2-emu\games.xml`, installed with the core. It must match the core version: if something goes wrong, update the core rather than replacing this file by hand. RetroBat checks it as an optional BIOS.

## Which game format?

Games are MAME `.zip` archives, to be kept as they are: do not extract or rename them.

* Clones (`daytonas`, `vf2b`, `srallycb`…) need their parent game (`daytona`, `vf2`, `srallyc`) in the same folder, except with a non-merged romset.
* m2emulator only reads `.zip` archives.

The `.decomp` extension is for PC ports, see the [**Recompilations**](../../others/recomp.md) page.

## Controls

### Automatic configuration

RetroBat automatically configures controllers for all emulators. With m2emulator, the configuration is written game by game, for the games listed below; other games keep the configuration made in the emulator.

The **AUTOCONFIGURE CONTROLLERS** option keeps your own configuration.

### Controller driver (m2emulator)

m2emulator uses the XInput driver by default. If your controller is not XInput compatible, select **DRIVERS > CONTROLLER > DINPUT** in the system advanced settings. RetroBat also switches to DInput by itself when no XInput controller is found.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (568).png" alt=""><figcaption></figcaption></figure></div>

### Per-game controls (m2emulator)

For all games: **START** = Start, **SELECT** = coin.

**Fighting games**

Movement with the D-pad.

| Game                          | SOUTH   | EAST    | WEST  | NORTH |
| ----------------------------- | ------- | ------- | ----- | ----- |
| Virtua Fighter 2 (`vf2`)      | Guard   | —       | Punch | Kick  |
| Dead or Alive (`doa`)         | Kick    | Hold    | Punch | —     |
| Fighting Vipers (`fvipers`)   | Guard   | Guard 2 | Punch | Kick  |
| Last Bronx (`lastbrnx`)       | Guard   | —       | Punch | Kick  |
| Sonic the Fighters (`schamp`) | Barrier | —       | Punch | Kick  |

**Standard games**

Movement with the D-pad.

| Game                        | SOUTH     | EAST  | WEST       | NORTH |
| --------------------------- | --------- | ----- | ---------- | ----- |
| Dynamite Cop (`dynamcop`)   | Jump      | —     | Punch      | Kick  |
| Pilot Kids (`pltkids`)      | Bomb      | —     | Shot       | —     |
| Virtua Striker (`vstriker`) | Long pass | Shoot | Short pass | —     |
| Zero Gunner (`zerogun`)     | Bomb      | —     | Shot       | —     |

**CONTROLLER LAYOUT** adapts the buttons of these games to arcade sticks (modern8, 8alternative, 6alternative). For more details on arcade layouts, see the [**Arcade Guide**](../../../arcade-guide.md) page. Buttons are set in the `system\resources\inputmapping\model2.yml` file, which you can copy to `user\inputmapping` to edit it.

**Racing games**

For all racing games: left stick = steering, **R2** = accelerator, **L2** = brake.

| Game                                                                                          | SOUTH     | EAST | WEST    | NORTH | Gears                                      |
| --------------------------------------------------------------------------------------------- | --------- | ---- | ------- | ----- | ------------------------------------------ |
| Daytona USA (`daytona`)                                                                       | VR2       | VR4  | VR3     | VR1   | Right stick: up 1, down 2, left 3, right 4 |
| Sega Rally Championship (`srallyc`)                                                           | —         | —    | —       | View  | Right stick: up 1, down 2, left 3, right 4 |
| Indianapolis 500 (`indy500`), Sega Touring Car Championship (`stcc`), Super GT 24h (`sgt24h`) | Gear down | View | Gear up | View  | SOUTH / WEST                               |
| Over Rev (`overrev`)                                                                          | Gear down | View | Gear up | —     | SOUTH / WEST                               |
| Manx TT Superbike (`manxtt`)                                                                  | Gear down | —    | Gear up | —     | SOUTH / WEST                               |
| Motor Raid (`motoraid`)                                                                       | Kick      | —    | Punch   | —     | —                                          |

The **CONTROLS > USE SHOULDER BUTTONS FOR RACING GAMES** option puts the accelerator and the brake on R1 / L1; it only works with the game's automatic gearbox.

**Other games**

<table><thead><tr><th width="292.75">Game</th><th>Controls</th></tr></thead><tbody><tr><td>Desert Tank (<code>desert</code>)</td><td>Left stick: move and turn; right stick: turret; L2: reverse; R2: cannon; R1: machine gun; NORTH, SOUTH, WEST: VR1, VR2, VR3 buttons</td></tr><tr><td>Dynamite Baseball 97 (<code>dynabb97</code>)</td><td>Left stick: movement; R2: bat / pitch; SOUTH: Hold; WEST: throw the ball</td></tr><tr><td>Sega Ski Super G (<code>skisuprg</code>)</td><td>Left stick: turn; right stick: turn harder; WEST, SOUTH, EAST: Select 1, 2, 3</td></tr><tr><td>Sega Water Ski (<code>segawski</code>)</td><td>Left stick: turn; L2 / R2: left / right pedals</td></tr><tr><td>Sky Target (<code>skytargt</code>)</td><td>Left stick: movement; R2: machine gun; L2: missiles; NORTH: view</td></tr><tr><td>Top Skater (<code>topskatr</code>)</td><td>Left stick: turn; right stick: turn harder; SOUTH: ollie; NORTH: nollie; WEST / EAST: Select left / right</td></tr><tr><td>Virtual On Cybertroopers (<code>von</code>)</td><td>Left and right sticks: the two control sticks; L2 / R2: left / right weapons; WEST / EAST: left / right turbo</td></tr><tr><td>Wave Runner (<code>waverunr</code>)</td><td>Left stick: turn; right stick: turn harder; R2: accelerate; NORTH: view</td></tr></tbody></table>

### Keisho, sm2 libretro core and Supermodel

Keisho, the sm2 libretro core and Supermodel follow the same logic: steering on the left stick, accelerator / brake on R2 / L2, gears on L1 / R1 or on the right stick for 4-speed gearboxes, Start / coin on START / SELECT, Service / Test on L3 / R3. The buttons of each game are set in `keisho.yml` and `supermodel.yml` (`system\resources\inputmapping`), which you can copy to `user\inputmapping` to edit them (the sm2 libretro core has its own layout). **CONTROLLER LAYOUT** is also available. For more details on `keisho.yml`, see the [**Keisho controller mapping**](../../../../controllers/specific_mapping/keisho-controller-mapping.md) page.

With Keisho, gun games can also be played with a controller: left or right stick = aim, **SOUTH** or **R2** = shoot, **EAST** or **L2** = reload / missiles. In driving games, the view buttons (VR1 to VR4) always stay on the face buttons. Virtual On, Desert Tank, Sky Target, Ski Super G and Water Ski use a Keisho layout of their own, which cannot be changed.

With the sm2 libretro core:

* **CONTROLS > TEST/SERVICE ON L3/R3** (on by default): L3 = Service, R3 = Test.
* **CONTROLS > 4-SPEED SHIFTER**: **H-GATE** (diagonals, like a real gate) or **DIRECTIONS** (up 1, down 2, left 3, right 4). L1 / R1 always shift down and up.

### Guns

Gun games: Behind Enemy Lines (`bel`), Gunblade NY (`gunblade`), The House of the Dead (`hotd`), Rail Chase 2 (`rchase2`), Virtua Cop (`vcop`), Virtua Cop 2 (`vcop2`).

Enable **GUNS > ENABLE GUN**.

**m2emulator**

<table><thead><tr><th width="271.5">Action</th><th>Control</th></tr></thead><tbody><tr><td>Shoot</td><td>Trigger / left click</td></tr><tr><td>Reload, missiles</td><td>Secondary button / right click</td></tr><tr><td>Player 1 / player 2 Start</td><td>1 / 2</td></tr><tr><td>Player 1 / player 2 coin</td><td>5 / 6</td></tr></tbody></table>

* With a Wiimote and a DolphinBar: D-pad right = Start, D-pad left = coin (player 2: up = Start, down = coin).
* **GUNS > FORCE KEYBOARD FOR START/COIN** keeps 1 / 2 and 5 / 6 whatever the gun.
* DemulShooter starts automatically with two guns (**GUNS > USE DEMULSHOOTER** option).
* **GUNS > P1 MOUSE INDEX** / **P2 MOUSE INDEX** selects each player's gun if it is not detected correctly.
* **GUNS > SHOW CROSSHAIR** displays the crosshair (DS types only work with DemulShooter).

**Keisho**: without the **ENABLE GUN** option, Keisho is in automatic mode: it shows the crosshair in gun games, and you aim with the mouse or a controller stick. With the option, it uses the connected guns (players 1 and 2) and also hides the cursor in other games. **SHOW CROSSHAIR** and **HIDE SHOT FLASH** options (with or without a gun), **SINDEN BORDER SIZE**, **ENABLE GUN RECOIL**, **RECOIL STRENGTH** (with a gun). Start and coin stay on the keyboard (1 / 5 player 1, 2 / 6 player 2).

**sm2 libretro core**: **SHOW CROSSHAIR**, **HIDE INACTIVE CROSSHAIR**, **HIDE SHOT FLASH** options. Without a gun, it aims with the stick (**CONTROLS > STICK AIMING**: **RELATIVE** or **ABSOLUTE**).

Each game must be calibrated in its test menu (see [**Calibrate the guns**](sega-model-2.md#calibrate-the-guns) below). For more details on guns, see the [**Guns**](../../../../controllers/supported-controllers/lightguns/) page.

### Wheels

m2emulator, Keisho and Supermodel support wheels, with the **WHEELS > ENABLE WHEEL** option.

* m2emulator: **ENABLE FORCE FEEDBACK** (on by default with a wheel), **HOLD GEARS** (back to neutral when the gear lever is released), choice of a separate shifter. Controls are set per wheel type and per game in `model2_wheels.yml`.
* Keisho: **ENABLE FORCE FEEDBACK** and **FORCE FEEDBACK STRENGTH**. The buttons are set per wheel type in `keisho_wheels.yml`; steering and pedals are detected by Keisho.
* Supermodel: **ENABLE FORCE FEEDBACK**.

For more details on wheels, see the [**Wheels**](../../../../controllers/supported-controllers/wheels.md) page.

### Hotkeys

**m2emulator**

<table><thead><tr><th width="173.25">Hotkey</th><th width="352">Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Exit</td><td>ESC</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test (<strong>EMULATION > ENABLE SERVICE MENU</strong> option)</td><td>9 / 0</td></tr><tr><td>—</td><td>Leave fullscreen and show the emulator menu</td><td>ALT + ENTER</td></tr></tbody></table>

**Keisho and Supermodel**: same hotkeys as for the Model 1, see the [**Sega Model 1**](sega-model-1.md) page.

**libretro cores**: usual RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page). **MAME**: see the [**MAME**](../mame.md#hotkeys) page.

## Folders

<table><thead><tr><th width="356.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>m2emulator: configuration</td><td><code>emulators\m2emulator\Emulator.ini</code></td></tr><tr><td>m2emulator: controls of each game</td><td><code>emulators\m2emulator\CFG</code> (one <code>.input</code> file per game)</td></tr><tr><td>m2emulator: control templates</td><td><code>emulators\m2emulator\templatescfg\xinput</code>, <code>templatescfg\dinput</code></td></tr><tr><td>m2emulator: NVRAM (cabinet settings and high scores)</td><td><code>emulators\m2emulator\NVDATA</code></td></tr><tr><td>m2emulator: game scripts (widescreen…)</td><td><code>emulators\m2emulator\scripts</code></td></tr><tr><td>m2emulator: copy of the running game</td><td><code>emulators\m2emulator\roms</code> (emptied at each launch)</td></tr><tr><td>Keisho: NVRAM</td><td><code>saves\model2\keisho</code></td></tr><tr><td>Keisho: save states (managed by RetroBat)</td><td><code>saves\model2\keisho\sstates</code></td></tr><tr><td>Keisho: save states (emulator folder)</td><td><code>saves\model2\keisho\states</code></td></tr><tr><td>Keisho: screenshots</td><td><code>screenshots\keisho</code></td></tr><tr><td>Keisho: configuration</td><td><code>emulators\keisho\keisho.ini</code></td></tr><tr><td>sm2 libretro core: game database</td><td><code>bios\sm2-emu\games.xml</code></td></tr><tr><td>Supermodel: configuration</td><td><code>emulators\supermodel\Config\Supermodel.ini</code></td></tr><tr><td>Supermodel: NVRAM</td><td><code>emulators\supermodel\NVRAM</code></td></tr><tr><td>Supermodel: save states</td><td><code>emulators\supermodel\Saves</code></td></tr><tr><td>Per-game button mapping</td><td><code>system\resources\inputmapping\model2.yml</code>, <code>keisho.yml</code>, <code>supermodel.yml</code> (editable copy in <code>user\inputmapping</code>)</td></tr><tr><td>Wheel buttons</td><td><code>system\resources\inputmapping\wheels\model2_wheels.yml</code> (m2emulator), <code>keisho_wheels.yml</code> (Keisho)</td></tr></tbody></table>

For the MAME folders, see the [**MAME**](../mame.md) page.

## Guides

### Service menu

The test menu of each cabinet gives access to the game settings (difficulty, number of lives, gun calibration…).

* **m2emulator**: on the keyboard, **9** (Service) and **0** (Test). To use the controller, enable **EMULATION > ENABLE SERVICE MENU**: **R3** (Test) opens the menu, **L3** (Service) moves from one line to the next.
* **sm2 libretro core**: L3 / R3, on by default (**CONTROLS > TEST/SERVICE ON L3/R3**).
* **Keisho**, **Supermodel**: see the [**Sega Model 1**](sega-model-1.md) page.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (567).png" alt=""><figcaption></figcaption></figure></div>

### Calibrate the guns

Gun games must be calibrated in the game: open the test menu, then **GUN SETTINGS**, and follow the on-screen instructions.

### Use your own key configuration (m2emulator)

1. Start the game, press **ALT + ENTER** to show the emulator menu, then open **Game > Configure Controls** and set the keys.
2. Exit the emulator: the `<game>.input` file is saved in `emulators\m2emulator\CFG`.
3. Copy it to `emulators\m2emulator\templatescfg\xinput` or `templatescfg\dinput`, depending on the selected driver, and give it **the name of the parent game** (for example `daytona.input` for `daytonas`).
4. In the system advanced settings, select **CONTROLS > TYPE OF AUTOCONFIGURATION > TEMPLATES**.

RetroBat then copies this file at each launch (except when guns are enabled). The full guide, with the `model2.yml` per-game mapping, is on the [**m2emulator controller mapping**](../../../../controllers/specific_mapping/model2-controller-mapping.md) page.

### Other useful options

**m2emulator**

<table><thead><tr><th width="352.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>WIDESCREEN HACK</strong></td><td>Displays games in 16:9 (best results with full 3D games).</td></tr><tr><td><strong>VISUAL RENDERING > FORCE MANAGED TEXTURES</strong></td><td>Enable it if the emulator crashes after loading or does not show anything.</td></tr><tr><td><strong>VISUAL RENDERING > ANTI-ALIASING</strong></td><td>Smooths polygon edges.</td></tr><tr><td><strong>CONTROLS > SWITCH JOYPAD INDEX</strong></td><td>Swaps the player 1 and player 2 controllers (XInput).</td></tr><tr><td><strong>CONTROLS > FORCE PLAYER 1 PAD INDEX</strong> / <strong>PLAYER 2</strong></td><td>Selects each player's controller, useful on a cabinet.</td></tr></tbody></table>

**Keisho and sm2 libretro core**

| Option                                            | Effect                                                                                    |
| ------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **INTERNAL RESOLUTION**                           | Increases the rendering resolution (Vulkan and OpenGL).                                   |
| **NATIVE REFRESH RATE (57.5 HZ)** (libretro core) | Original cabinet refresh rate instead of 60 Hz; can stutter on a 60 Hz screen.            |
| **VISUAL RENDERING > CRT FILTER** (Keisho)        | Look of a CRT screen.                                                                     |
| **VISUAL RENDERING > TRANSLUCENCY** (Keisho)      | **BLENDED**: smooth transparency instead of the cabinet checkerboard (Vulkan and OpenGL). |
| **VISUAL RENDERING > DRAW DISTANCE** (Keisho)     | Draws the scenery up to the end of the course in supported games (Daytona USA).           |
| **AUDIO > MUSIC VOLUME** (Keisho)                 | Volume of the music board (Daytona USA, Sega Rally).                                      |
| **EMULATION > REWIND** (Keisho)                   | Enables rewind.                                                                           |

For the Keisho and Supermodel options, see also the [**Sega Model 1**](sega-model-1.md) page.

## Known issues

<table><thead><tr><th width="355.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>"Network Board Not Present" message</td><td>Open the test menu, then <strong>Game System > Link ID</strong>, and select <strong>Single</strong><br><img src="../../../../.gitbook/assets/image (569).png" alt=""></td></tr><tr><td>A clone does not start</td><td>Put the parent game in <code>roms\model2</code>, or use a <a href="../../../arcade-guide.md#romset-types">non-merged romset</a>.</td></tr><tr><td>The controller does not respond with m2emulator</td><td>Select <strong>DRIVERS > CONTROLLER > DINPUT</strong>.</td></tr><tr><td>Player 1 and player 2 controllers are swapped</td><td>Enable <strong>CONTROLS > SWITCH JOYPAD INDEX</strong>, or force the index of each controller.</td></tr><tr><td>A game crashes or stays black with m2emulator</td><td>Enable <strong>VISUAL RENDERING > FORCE MANAGED TEXTURES</strong>, or try the <strong>singlecpu</strong> version.</td></tr><tr><td>Files disappeared from <code>emulators\m2emulator\roms</code></td><td>This folder is emptied at each launch: keep your games in <code>roms\model2</code>.</td></tr><tr><td>The sm2 libretro core does not start any game</td><td>Check that <code>bios\sm2-emu\games.xml</code> is present; update the core if needed.</td></tr></tbody></table>
