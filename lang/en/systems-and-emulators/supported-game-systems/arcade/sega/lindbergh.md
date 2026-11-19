---
description: Sega
---

# Lindbergh

<div align="left"><img src="https://images.gitbook.com/__img/dpr=2,width=760,onerror=redirect,format=auto,signature=1065403660/https%3A%2F%2Fraw.githubusercontent.com%2FRetroBat-Official%2Fes-theme-carbon%2F801d816fdf5f7286d8b717acd351964eda457a71%2Fart%2Flogos%2Flindbergh.svg" alt="" height="67" width="300"></div>

## Overview

The **Lindbergh** is a Sega arcade board released in 2005. It is a real PC (Intel Pentium 4 then Celeron processor, NVIDIA GeForce graphics card) running its games under Linux. It replaced the Naomi 2 and the Chihiro at Sega, and got about thirty games until 2010.

Its games include **The House of the Dead 4** (and Special, EX), **Virtua Fighter 5**, **Outrun 2 SP SDX**, **Initial D Arcade Stage 4** and **5**, **After Burner Climax**, **Virtua Tennis 3**, **Let's Go Jungle!**, **2 Spicy**, **Ghost Squad Evolution**, **Rambo**, **Primeval Hunt**, **Sega Race TV**, **R-Tuned**, **Hummer** and **Harley-Davidson: King of the Road**.

RetroBat offers two emulators: **Linuxloader** (default), which runs the games' Linux programs on Windows, and **TeknoParrot**.

{% embed url="https://en.wikipedia.org/wiki/List_of_Sega_arcade_system_boards#Sega_Chihiro" %}

## At a glance

<table><thead><tr><th width="212.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\lindbergh</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game</td></tr><tr><td><strong>Default emulator</strong></td><td>linuxloader</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, every emulator (mapping per game type for Linuxloader)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>Linuxloader (1 gun, 4 with DemulShooter), TeknoParrot</td></tr><tr><td><strong>Wheels</strong></td><td>Linuxloader, TeknoParrot</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

| Emulator                  | Strengths                                                                                                                                                                         | Limitations                                                                                    |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| **linuxloader** (default) | Runs the games directly, no profile to install. Controllers, wheels and light guns set up automatically, arcade layouts, white border for Sinden light guns, game-specific fixes. | Only one light gun without DemulShooter.                                                       |
| **teknoparrot**           | TeknoParrot interface and profiles, many games from other boards.                                                                                                                 | Needs a TeknoParrot profile for each game (see the [**TeknoParrot**](../teknoparrot.md) page). |

## BIOS

No BIOS is needed: Lindbergh games hold everything they need.

## Which game format?

A Lindbergh game is a folder, which usually holds a `disk0` folder. RetroBat recognizes it in two ways:

<table><thead><tr><th width="131.5">Method</th><th>How to do it</th></tr></thead><tbody><tr><td><strong><code>.game</code> folder</strong></td><td>Rename the game folder with the <code>.game</code> extension (for example <code>hotd4.game</code>). RetroBat looks for the game program in <code>disk0</code> if it exists, otherwise directly in the folder, and in the right subfolder for known games (see below).</td></tr><tr><td><strong><code>.game</code> file</strong></td><td>Create an empty file with the <code>.game</code> extension (for example <code>hummerxt.game</code>) next to the game program (the <code>elf</code> file). The game folder must not have the <code>.game</code> extension.</td></tr></tbody></table>

<table><thead><tr><th width="450.25">Example</th><th>Explanation</th></tr></thead><tbody><tr><td>roms\lindbergh\hotd4.game\disk0\elf\hod4M.elf</td><td>.game folder with disk0</td></tr><tr><td>roms\lindbergh\hummerxt.game\hummer_master.elf</td><td>.game folder without disk0</td></tr><tr><td>roms\lindbergh\hummerxt\hummerxt.game</td><td>.game file next to the elf file</td></tr></tbody></table>

Give the `.game` folder or file the short name of the game: it lets DemulShooter recognize the game and, for a folder, lets RetroBat find the program when it is in a subfolder (for example `disk0\elf`).

<details>

<summary>Recognized game names</summary>

| Game                                          | Folder name         |
| --------------------------------------------- | ------------------- |
| 2 Spicy                                       | `2spicy`            |
| After Burner Climax (SDX)                     | `abclisdx`          |
| Ghost Squad Evolution                         | `gsevo`             |
| Harley-Davidson: King of the Road             | `hdkotr`            |
| The House of the Dead 4 (Rev A)               | `hotd4`             |
| The House of the Dead 4 Special               | `hotd4sp`           |
| The House of the Dead EX                      | `hotdex`            |
| Hummer                                        | `hummer`            |
| Hummer Extreme Edition                        | `hummerxt`          |
| Initial D Arcade Stage 4 (Rev B)              | `initiad4b`         |
| Initial D 4 Export (Rev D)                    | `initiad4ex`        |
| Initial D 5 Export (2.0)                      | `initiad5exa`       |
| Let's Go Jungle!                              | `lgj`               |
| Let's Go Jungle! Special                      | `lgjsp`             |
| Outrun 2 SP SDX (Rev A)                       | `outr2sdx`          |
| Outrun 2 SP SDX (bootleg)                     | `outr2sdxg`         |
| Primeval Hunt                                 | `primevah`          |
| R-Tuned: Ultimate Street Racing               | `rtuned`            |
| Rambo (Export)                                | `rambo`             |
| Sega Race TV (Export)                         | `segartv`           |
| Virtua Fighter 5                              | `vf5`               |
| Virtua Fighter 5 (Rev E, ver C)               | `vf5e`              |
| Virtua Fighter 5 Final Showdown (Rev A, v2.0) | `vf5fsa2`           |
| Virtua Fighter 5 R (Rev G)                    | `vf5r`              |
| Virtua Tennis 3 (Rev C)                       | `vt3` or `vtennis3` |

</details>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (605).png" alt=""><figcaption></figcaption></figure></div>

## Controls

### Automatic setup (Linuxloader)

RetroBat writes the Linuxloader `controls.ini` file at each launch, for 2 players (button games) or 1 player (driving, flying). The button positions come from `linuxloader.yml`, with one section per game type.

**Common controls**

| Cabinet       | Controller              | Keyboard  |
| ------------- | ----------------------- | --------- |
| Start         | START                   | `1` / `2` |
| Coin          | SELECT                  | `5` / `6` |
| Test          | R3 (with **TEST MODE**) | `0`       |
| Service       | L3 (with **TEST MODE**) | `9`       |
| Exit the game | START + SELECT          | Esc       |

**Button games** (Virtua Fighter 5, Virtua Tennis 3…)

| Cabinet    | Controller        | Player 1 keyboard | Player 2 keyboard |
| ---------- | ----------------- | ----------------- | ----------------- |
| Directions | D-pad, left stick | Arrows            | `R` `F` `D` `G`   |
| Button 1   | SOUTH             | Left Ctrl         | `A`               |
| Button 2   | EAST              | Left Alt          | `S`               |
| Button 3   | WEST              | Space             | `Q`               |
| Card       | GUIDE             | `F7`              | `F8`              |

**Driving games** (Outrun 2, Initial D, Sega Race TV…)

| Cabinet             | Controller   | Keyboard             |
| ------------------- | ------------ | -------------------- |
| Wheel               | Left stick   | Left / right arrows  |
| Gas / brake         | R2 / L2      | Up / down arrows     |
| View change         | NORTH        | Left Shift           |
| Boost / right boost | SOUTH / EAST | Left Ctrl / Left Alt |
| Gear up / down      | R1 / L1      | `X` / `Z`            |
| Music change        | WEST         | Space                |
| Selection buttons   | D-pad        | `R` `F` `D` `G`      |
| Card                | GUIDE        | `F7`                 |

**Flying games** (After Burner Climax)

| Cabinet                | Controller                      | Keyboard             |
| ---------------------- | ------------------------------- | -------------------- |
| Stick                  | Left stick, d-pad               | Arrows               |
| Throttle               | Right stick (vertical), R2 / L2 | —                    |
| Accelerate / slow down | R1 / L1                         | `X` / `Z`            |
| Gun / missile          | SOUTH / EAST                    | Left Ctrl / Left Alt |
| Climax                 | NORTH                           | Left Shift           |

* **CONTROLS > CONTROLLER LAYOUT** places the buttons for an arcade stick (6 or 8 buttons): wheel and pedals then move to the d-pad and buttons. See the [**Arcade Guide**](../../../arcade-guide.md) page.
* **CONTROLS > INVERT P1 AND P2** swaps the two controllers. **STEERING DEADZONE**, **GAS/BRAKE DEADZONE** and **FLIGHT STICK DEADZONE** set the deadzones.
* **CONTROLS > CUSTOM CONTROLS INI FILE** uses your own `controls.ini` file instead of the RetroBat one.
* Mahjong games are played with the keyboard.

### Light guns

Light gun games (**The House of the Dead 4**, **Let's Go Jungle!**, **2 Spicy**, **Ghost Squad Evolution**, **Rambo**, **Primeval Hunt**…) are played with a light gun or the mouse (**GUNS > ENABLE GUN**):

<table><thead><tr><th width="231.5">Cabinet</th><th>Light gun / mouse</th></tr></thead><tbody><tr><td>Trigger</td><td>Left click</td></tr><tr><td>Reload</td><td>Right click (<strong>RELOAD MAPPING</strong>)</td></tr><tr><td>Gun button</td><td>Middle click (<strong>GUN BUTTON MAPPING</strong>)</td></tr><tr><td>Action button</td><td>Start (<strong>ACTION BUTTON MAPPING</strong>)</td></tr><tr><td>Left / right pedals</td><td>Left / right arrows</td></tr></tbody></table>

Linuxloader supports only one light gun. To play with several, enable **GUNS > USE DEMULSHOOTER** (DemulShooter is installed from the RetroBat download menu): the `.game` folder or file name must then be the one in the list (`hotd4`, `lgj`, `2spicy`…). With a Sinden light gun, RetroBat enables the Linuxloader white border (**ENABLE WHITE BORDER**). For more details, see the [**Light gun controls**](../../../../controllers/gun_controls.md) page.

### Wheels

With **WHEELS > ENABLE WHEEL**, the DirectInput wheel is set up from `linuxloader_wheels.yml` (wheel, pedals, gears, buttons). XInput wheels, seen as gamepads, use the controller mapping. For the supported wheels, see the [**Wheels**](../../../../controllers/supported-controllers/wheels.md) page.

### Hotkeys

<table><thead><tr><th width="236.5">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="244">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Configuration</td><td><code>emulators\linuxloader\linuxloader.ini</code></td></tr><tr><td>Controls (written by RetroBat)</td><td><code>emulators\linuxloader\controls.ini</code></td></tr><tr><td>Light gun crosshairs</td><td><code>emulators\linuxloader\cross</code></td></tr><tr><td>Button positions</td><td><code>system\resources\inputmapping\linuxloader.yml</code> (editable copy in <code>user\inputmapping</code>)</td></tr><tr><td>Wheels</td><td><code>system\resources\inputmapping\wheels\linuxloader_wheels.yml</code> (editable copy in <code>user\inputmapping</code>)</td></tr><tr><td>Recognized game names</td><td><code>system\tools\linuxloaderconfig.yml</code></td></tr></tbody></table>

## Guides

### Test menu

The cabinet test menu lets you calibrate light guns, pick the difficulty or check the controls. Enable **EMULATION > TEST MODE**: the game starts directly in the test menu, and R3 / L3 become Test / Service (`0` / `9` on the keyboard).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (604).png" alt="" width="387"><figcaption></figcaption></figure></div>

### Game-specific fixes

| Option                                     | Effect                                                                                                                                            |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **EMULATION > CPU FREQUENCY**              | The House of the Dead 4: processor frequency in GHz (for example `4.3`) if the game runs too fast or too slow. Detected automatically by default. |
| **GAME FIXES > HUMMER FLICKER FIX**        | Removes the picture flickering in Hummer.                                                                                                         |
| **GAME FIXES > PRIMEVAL HUNT SCREEN MODE** | Display of the second (touch) screen of Primeval Hunt: side by side (default), no touch screen, 3DS modes.                                        |
| **GAME FIXES > OUTRUN SKIP CABINET CHECK** | Outrun 2 SP SDX starts without the cabinet drive board and tower.                                                                                 |
| **GAME FIXES > RAMBO GUNS SWITCH**         | Changes how the guns are shown in Rambo.                                                                                                          |

### Other useful options

<table><thead><tr><th width="316.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>EMULATION > REGION</strong></td><td>Export, US or Japan.</td></tr><tr><td><strong>EMULATION > FREE PLAY</strong></td><td>Play without credits.</td></tr><tr><td><strong>KEEP ASPECT RATIO</strong></td><td>Keeps the picture shape instead of stretching it (on by default).</td></tr><tr><td><strong>VIDEO > BOOST RENDER RESOLUTION</strong></td><td>Renders at the screen resolution (on by default).</td></tr><tr><td><strong>VIDEO > LIMIT FPS</strong>, <strong>FPS TARGET</strong></td><td>Limits to 60 or 30 frames per second.</td></tr><tr><td><strong>GUNS > ENABLE INTERNAL CROSSHAIR</strong></td><td>Shows a crosshair on screen; <strong>P1 CROSSHAIR PATH</strong> / <strong>P2</strong> picks the picture.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="285.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game goes straight back to the game list</td><td>Check that the <code>.game</code> folder or file has the short name of the game. If the game program is in an unusual subfolder, put a <code>.game</code> file next to it. See the <a href="lindbergh.md#which-game-format"><strong>Which game format?</strong></a> section.</td></tr><tr><td>The House of the Dead 4 runs too fast</td><td>Set <strong>EMULATION > CPU FREQUENCY</strong>.</td></tr><tr><td>DemulShooter does not recognize the game</td><td>Rename the <code>.game</code> folder or file with the expected name (<code>hotd4</code>, <code>lgj</code>, <code>rambo</code>…).</td></tr><tr><td>Players 1 and 2 are swapped</td><td>Enable <strong>CONTROLS > INVERT P1 AND P2</strong>.</td></tr><tr><td>Outrun 2 SP SDX stops on a cabinet error</td><td>Enable <strong>GAME FIXES > OUTRUN SKIP CABINET CHECK</strong>.</td></tr></tbody></table>
