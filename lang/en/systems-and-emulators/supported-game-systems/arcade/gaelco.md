---
description: Gaelco, S.A.
---

# Gaelco

<div align="left"><figure><img src="../../../.gitbook/assets/image (585).png" alt="" width="341"><figcaption></figcaption></figure></div>

### Overview

**Gaelco** is a Spanish arcade developer based in Barcelona, known for Big Karnak, World Rally or Radikal Bikers. In the early 2000s, its 3D games run on boards built around a PowerVR graphics chip (Neon 250 card).

The RetroBat **Gaelco PowerVR** system gathers these games: **Smashing Drive** (2000), **ATV Track** (2002) and **Gaelco Football** (2002).

RetroBat offers two emulators: **Odin** (default), a low-level emulator of the Gaelco and Hikaru boards, and **Demul**.

{% embed url="https://en.wikipedia.org/wiki/Gaelco" %}

### At a glance

<table><thead><tr><th width="265.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\gaelco</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip</td></tr><tr><td><strong>Default emulator</strong></td><td>odin</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>Odin; Demul through hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Wheels</strong></td><td>Odin (ATV Track, Smashing Drive)</td></tr></tbody></table>

### Which emulator to choose?

<table><thead><tr><th width="154.5">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>odin</strong> (default)</td><td>Low-level emulator of the Gaelco boards: all three games, controls set per game, higher resolution, CRT filters of the Gaelco monitors, save states, force feedback wheel, controller rumble.</td><td>Gaelco support is brand new (Odin 0.1.1).</td></tr><tr><td><strong>demul</strong></td><td>Long-standing emulator, also used for the Naomi and the Atomiswave.</td><td>Same button layout for every game. Save states not managed by RetroBat.</td></tr></tbody></table>

MAME does not emulate these games yet (flagged as not working and without sound): RetroBat therefore offers no MAME core for this system.

### BIOS

No BIOS is needed.

### Which game format?

Games are MAME `.zip` archives, to be kept as they are, without extracting or renaming them (`atvtrack.zip`, `gfootbal.zip`, `smashdrv.zip`).

The `atvtracka`, `smashdrvb` and `smashdrvs` versions need their parent game (`atvtrack`, `smashdrv`) in the same folder, unless you use a non-merged romset.

### Controls

#### Automatic configuration

RetroBat configures the controllers automatically for both emulators. The **AUTOCONFIGURE CONTROLLERS** option lets you keep your own configuration.

For every game: **SELECT** = coin, **L3** = Service, **R3** = Test. On the keyboard: 1 = Start, 5 = coin, 9 = Service, 0 = Test. Gaelco cabinets have a single coin input and a single Service button.

#### Odin

Buttons are set per game in `odin.yml` (`system\resources\inputmapping`, editable copy in `user\inputmapping`):

<table><thead><tr><th width="330.25">Game</th><th>Controls</th></tr></thead><tbody><tr><td>ATV Track (<code>atvtrack</code>, <code>atvtracka</code>)</td><td>Left stick: handlebar; R2: throttle; L2 / R1: left / right brakes; START: Start</td></tr><tr><td>Gaelco Football (<code>gfootbal</code>), 2 players</td><td>D-pad or left stick: move; SOUTH, EAST, WEST: buttons 1, 2, 3; right stick: kick the ball (pull the stick back first to lift the ball); START: Start</td></tr><tr><td>Smashing Drive (<code>smashdrv</code>, <code>smashdrvb</code>, <code>smashdrvs</code>)</td><td>Left stick: steering; R2 / L2: gas / brake; START: horn (Start); D-pad up / down: volume</td></tr></tbody></table>

In Gaelco Football, the right stick kicks: **R3** does not open the test menu, use the **0** key of the keyboard.

Options of the **CONTROLS** menu:

* **JOYSTICK DEADZONE**: deadzone of the sticks (3 % by default).
* **ENABLE RUMBLE**: the controller shakes like the cabinet, for example the shaking seat of ATV Track (on by default).
* **EXTERNAL OUTPUTS**: sends the lamps and the drive board to external tools (Hook Of The Reaper, QMamehook...).

#### Demul

Demul uses the same layout for every game:

<table><thead><tr><th width="270.25">Cabinet button</th><th>Controller</th></tr></thead><tbody><tr><td>Buttons 1 to 4</td><td>SOUTH, EAST, WEST, NORTH</td></tr><tr><td>Buttons 5 to 8</td><td>L1, R1, L2, R2</td></tr><tr><td>Analog controls</td><td>Left stick and right stick</td></tr><tr><td>Directions</td><td>D-pad</td></tr><tr><td>Start</td><td>START</td></tr></tbody></table>

The **CONTROLS > ANALOG DEADZONE** option sets the deadzone of the sticks.

#### Wheels

ATV Track and Smashing Drive are played with a wheel in Odin, with force feedback. Enable **WHEELS > ENABLE WHEEL**: the wheel becomes player 1.

* ATV Track: the wheel is the handlebar; the brake pedal and the right paddle work the right brake, the left paddle the left brake.
* **WHEEL ROTATION**: degrees of rotation to reach full lock (270° by default).
* **FORCE FEEDBACK STRENGTH**: from 50 to 200 %, or off.
* Buttons are set per wheel type in `model3_wheels.yml` (the same file as Supermodel). Odin reads `odin_wheels.yml` first if it exists.

For more details on wheels, see the [**Wheels**](../../../controllers/supported-controllers/wheels.md) page.

#### Hotkeys

**Odin**

<table><thead><tr><th width="192">Hotkey</th><th>Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td>Escape</td></tr><tr><td><strong>HOTKEY + SOUTH</strong></td><td>Odin menu</td><td>F10</td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Load state</td><td>F4</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test</td><td>9 / 0</td></tr><tr><td>—</td><td>Pause</td><td>P</td></tr><tr><td>—</td><td>Reset</td><td>Ctrl + R</td></tr><tr><td>—</td><td>Fullscreen</td><td>F11 or Alt + Enter</td></tr></tbody></table>

Odin's own controller shortcuts also stay available with the **Guide** button: Guide alone = menu, Guide + SELECT = pause, Guide + R1 / L1 = save / load, Guide + START = quit. Keyboard keys can be customized, see the [**Hotkeys**](../../../navigation/hotkeys.md) page.

**Demul**

<table><thead><tr><th width="193.25">Hotkey</th><th>Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td><td></td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Demul save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Demul load state</td><td>F4</td></tr><tr><td><strong>HOTKEY + L3</strong></td><td>Fullscreen</td><td>Alt + Enter</td></tr></tbody></table>

Demul save states stay in Demul: they do not show up in the save state manager.

### Folders

| Content                                           | Folder                                                                                            |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| Odin: NVRAM (cabinet settings and high scores)    | `saves\gaelco\odin`                                                                               |
| Odin: save states (managed by RetroBat)           | `saves\gaelco\odin\sstates`                                                                       |
| Odin: save states (emulator folder, one per game) | `saves\gaelco\odin\states`                                                                        |
| Odin: configuration                               | `emulators\odin\odin.ini`                                                                         |
| Odin: log (launch errors)                         | `emulators\odin\odin.log`                                                                         |
| Odin: button mapping                              | `system\resources\inputmapping\odin.yml` (editable copy in `user\inputmapping`)                   |
| Odin: wheel buttons                               | `system\resources\inputmapping\wheels\model3_wheels.yml` (or `user\inputmapping\odin_wheels.yml`) |
| Demul: NVRAM                                      | `saves\gaelco\demul`                                                                              |
| Demul: configuration                              | `emulators\demul\Demul.ini`, `padDemul.ini`                                                       |

### Guides

#### Service menu

The test menu of each cabinet gives access to the game settings (difficulty, credits, volume...). **R3** (or **0** on the keyboard) opens the test menu, **L3** (or **9**) moves in it.

#### Smashing Drive volume (Odin)

Smashing Drive sets its volume at each power-on (75 by default). Change it with D-pad up / down during the game.

#### Save states (Odin)

Odin keeps a single save state per game, replaced at each **HOTKEY + WEST**. RetroBat copies each new state to a new slot: you find them all in the save state manager and can start the game from any of them.

#### Other useful options (Odin)

<table><thead><tr><th width="305.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Raises the rendering resolution (up to 6x).</td></tr><tr><td><strong>VISUAL RENDERING > CRT FILTER</strong></td><td>Look of a Gaelco monitor (28 or 34 inch).</td></tr><tr><td><strong>AUDIO > SOUND BOARDS</strong></td><td>Woofer of the Gaelco cabinets: main board only, mix or 4 channels.</td></tr><tr><td><strong>USE EMULATOR BEZELS</strong></td><td>Bezels of the Odin-Artwork pack (to be extracted in <code>emulators\odin</code>) instead of the RetroBat decorations.</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td>OpenGL (default) or Vulkan.</td></tr></tbody></table>

**Demul**: **INTERNAL RESOLUTION**, **GAME ASPECT RATIO** (4:3, 16:9 or stretched). Demul always uses its old graphics plugin for these games.

### Known issues

<table><thead><tr><th width="349">Issue</th><th>Solution</th></tr></thead><tbody><tr><td><code>atvtracka</code>, <code>smashdrvb</code> or <code>smashdrvs</code> does not start</td><td>Put the parent game (<code>atvtrack</code>, <code>smashdrv</code>) in <code>roms\gaelco</code>, or use a non-merged romset.</td></tr><tr><td>Gaelco Football: R3 does not open the test menu</td><td>The right stick kicks: use the <strong>0</strong> key of the keyboard.</td></tr><tr><td>Odin is not shown on the right monitor</td><td>Enable <strong>VIDEO > DISABLE FULLSCREEN</strong>.</td></tr></tbody></table>
