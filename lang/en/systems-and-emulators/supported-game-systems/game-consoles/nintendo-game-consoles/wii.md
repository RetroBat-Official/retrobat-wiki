---
description: Nintendo
---

# Wii

<div align="left"><figure><img src="../../../../.gitbook/assets/image (487).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Wii** is Nintendo's fifth home console, after the GameCube. It launched in North America in November 2006, and in Japan and Europe in December 2006. Rather than raw power, Nintendo bet on a new way to play: the **Wii Remote** (Wiimote), a remote that detects motion and works as a pointer thanks to an infrared bar (the _Sensor Bar_) placed near the TV.

It is held upright like a TV remote, sideways like a NES controller, or with the **Nunchuk**, a second handle with a stick, plugged into it. Other accessories followed: the **Classic Controller**, the Wii Fit **Balance Board**, the Wii Wheel, the Guitar Hero and Rock Band guitars and drums…

A worldwide hit, it sold more than 100 million units. It also plays GameCube games, and offers downloadable games: **WiiWare** and **Virtual Console** (NES, Super Nintendo, Nintendo 64, Mega Drive games…). Its library has many classics: Wii Sports, Mario Kart Wii, Super Mario Galaxy 1 and 2, New Super Mario Bros. Wii, The Legend of Zelda: Twilight Princess and Skyward Sword, Super Smash Bros. Brawl, Metroid Prime 3, Donkey Kong Country Returns, Xenoblade Chronicles, Wii Fit…

**GameCube games go in the** [**GameCube system**](gamecube.md) (`roms\gamecube`), not in the Wii system.

{% embed url="https://en.wikipedia.org/wiki/Wii" %}

## At a glance

<table><thead><tr><th width="241.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\wii</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gcz .iso .ciso .dol .wbfs .wad .rvz .wia .zip .7z .squashfs .json .elf .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>dolphin</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, Dolphin</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores, Dolphin</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>Dolphin</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="164">Emulator</th><th width="126.75">For whom?</th><th width="251.75">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>dolphin</strong> (default)</td><td>Everyone</td><td>The most compatible and complete: real Wiimotes (DolphinBar), emulated Wiimote set per game, accessories (guitar, drums, uDraw…), light guns, HD, texture packs, modified games (Riivolution).</td><td>—</td></tr><tr><td><strong>lr-dolphin</strong></td><td>RetroArch users</td><td>RetroArch features (shaders, RetroArch menu).</td><td>Based on an older Dolphin version, less compatible, fewer Wiimote types. Doesn't read .zip, .7z and .json.</td></tr></tbody></table>

**When in doubt, keep dolphin.**

## BIOS

No BIOS is needed: Dolphin starts Wii games directly.

The **Wii Menu** (the console home screen, with its channels) is optional: see [Guides](wii.md#using-the-wii-menu).

### Changing the game language

This is the console language: games use it when they offer it (most European games do).

In the system or game advanced options (Dolphin), set **EMULATION > LANGUAGE**: Japanese, English, German, French, Spanish, Italian or Dutch. By default, it is RetroBat's language.

{% hint style="info" %}
Dolphin creates the console settings the first time a Wii game is launched. The selected language therefore applies from the second launch onward.
{% endhint %}

## Which game format?

<table><thead><tr><th width="201">Format</th><th width="131.5">dolphin</th><th width="104.25">lr-dolphin</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.iso</strong> (recommended)</td><td>✔</td><td>✔</td><td>Uncompressed disc image (4.4 GB, or 8 GB for dual-layer discs).</td></tr><tr><td><strong>.rvz</strong> (recommended)</td><td>✔</td><td>✔</td><td>Dolphin's lossless compressed format.</td></tr><tr><td>.wbfs</td><td>✔</td><td>✔</td><td>Format used by Wii USB loaders.</td></tr><tr><td>.gcz / .wia / .ciso</td><td>✔</td><td>✔</td><td>Other compressed formats.</td></tr><tr><td>.wad</td><td>✔</td><td>✔</td><td><strong>WiiWare</strong> and <strong>Virtual Console</strong> games, channels.</td></tr><tr><td>.dol / .elf</td><td>✔</td><td>✔</td><td>Homebrew programs.</td></tr><tr><td>.zip / .7z / .squashfs</td><td>✔ (extracted at launch)</td><td>✘</td><td>Slower loading.</td></tr><tr><td>.json</td><td>✔</td><td>✘</td><td>Games modified with Riivolution patches.</td></tr></tbody></table>

To convert a game to .rvz, open Dolphin (`emulators\dolphin-emu\Dolphin.exe`), right-click the game, choose **Convert File…** and pick the **RVZ** format.

## Controls

### Three ways to play

The **CONTROLS > WIIMOTE TYPE** option sets how you play:

<table><thead><tr><th width="206.5">WIIMOTE TYPE</th><th>What you use</th></tr></thead><tbody><tr><td><strong>EMULATED</strong> (default)</td><td>Your controller (Xbox, PlayStation…) acts as the Wiimote and its accessories. RetroBat configures it automatically, up to 4 players.</td></tr><tr><td><strong>REAL</strong></td><td>Real Wiimotes, connected through a <strong>DolphinBar</strong> or Bluetooth. Your controllers then act as <strong>GameCube controllers</strong> (for Wii games that accept them).</td></tr><tr><td><strong>REAL AS EMULATED</strong></td><td>Real Wiimotes, read by Dolphin as an emulated Wiimote. The <strong>(NUNCHUK)</strong> and <strong>(CC)</strong> variants add an emulated Nunchuk or Classic Controller.</td></tr></tbody></table>

### Emulated Wiimote: picking the right controller

Wii games aren't all played the same way: some hold the Wiimote upright, others sideways, with a Nunchuk or with the Classic Controller. The **CONTROLS > EMULATED DEVICES** option, to set [**per game**](../../../../navigation/game-options.md), chooses the controller the game receives.

The name of the **WIIMOTE: X/Y** modes gives the role of your controller's two sticks, left stick first, then right stick:

<table><thead><tr><th width="151.5">Word</th><th>Stick role</th></tr></thead><tbody><tr><td><strong>CURSOR</strong></td><td>Aim at the screen (infrared pointer).</td></tr><tr><td><strong>SWING</strong></td><td>Swing the Wiimote in a direction (sword stroke, throw…).</td></tr><tr><td><strong>TILT</strong></td><td>Tilt the Wiimote.</td></tr><tr><td><strong>NUNCHUK</strong></td><td>Nunchuk stick.</td></tr></tbody></table>

For example, **WIIMOTE: NUNCHUK/CURSOR** puts the Nunchuk stick on the left stick and the pointer on the right stick.

A few setting examples:

| Game                                                                    | EMULATED DEVICES        |
| ----------------------------------------------------------------------- | ----------------------- |
| New Super Mario Bros. Wii, Kirby's Return to Dream Land, Mario Kart Wii | WIIMOTE: HORIZONTAL     |
| Super Mario Galaxy, Zelda: Twilight Princess, Metroid Prime 3           | WIIMOTE: NUNCHUK/CURSOR |
| Wii Sports                                                              | WIIMOTE: CURSOR/SWING   |
| Xenoblade Chronicles, Monster Hunter Tri                                | CLASSIC CONTROLLER      |

### Upright Wiimote (default)

Without any specific setting, the Wiimote is held upright, with no accessory:

| RetroBat controller | Wiimote                     |
| ------------------- | --------------------------- |
| SOUTH               | A                           |
| EAST                | B                           |
| WEST                | 1                           |
| NORTH               | 2                           |
| L1 / R1             | − / +                       |
| SELECT              | HOME                        |
| D-pad               | D-pad                       |
| Left stick          | Pointer (aim at the screen) |
| Right stick         | Tilt                        |
| L3                  | Freeze the pointer          |
| R3                  | Reduced tilt                |

### Sideways Wiimote

**WIIMOTE: HORIZONTAL** mode, for games played like a NES controller:

| RetroBat controller | Wiimote           |
| ------------------- | ----------------- |
| SOUTH               | 2                 |
| WEST                | 1                 |
| NORTH               | A                 |
| EAST                | B                 |
| L2                  | Shake             |
| L1 / R1             | Tilt left / right |
| SELECT / START      | − / +             |
| D-pad               | D-pad             |

### Wiimote + Nunchuk

**WIIMOTE: NUNCHUK/…** and **WIIMOTE: …/NUNCHUK** modes. A, B, 1 and 2 stay as on the upright Wiimote:

<table><thead><tr><th width="321.5">RetroBat controller</th><th>Wiimote + Nunchuk</th></tr></thead><tbody><tr><td>SOUTH / EAST / WEST / NORTH</td><td>A / B / 1 / 2</td></tr><tr><td>L1 / R1</td><td>C / Z (Nunchuk)</td></tr><tr><td>SELECT / START</td><td>− / +</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>Stick on the NUNCHUK side</td><td>Nunchuk stick</td></tr><tr><td>Other stick</td><td>Cursor, swing or tilt, depending on the mode</td></tr><tr><td>L2 / R2 (NUNCHUK/… mode)</td><td>Shake the Nunchuk / shake the Wiimote</td></tr><tr><td>L2 / R2 (…/NUNCHUK mode)</td><td>Shake the Wiimote / shake the Nunchuk</td></tr></tbody></table>

**NUNCHUK SWING** replaces the "shake the Nunchuk" gesture with a swing, for games that need it.

### Classic Controller

**CLASSIC CONTROLLER** mode:

<table><thead><tr><th width="199">RetroBat controller</th><th width="179.5">Classic Controller</th><th>With INVERT FACE BUTTONS = XBOX LAYOUT</th></tr></thead><tbody><tr><td>EAST</td><td>A</td><td>B</td></tr><tr><td>SOUTH</td><td>B</td><td>A</td></tr><tr><td>NORTH</td><td>X</td><td>Y</td></tr><tr><td>WEST</td><td>Y</td><td>X</td></tr><tr><td>L1 / R1</td><td>ZL / ZR</td><td>ZL / ZR</td></tr><tr><td>L2 / R2</td><td>L / R</td><td>L / R</td></tr><tr><td>SELECT / START</td><td>− / +</td><td>− / +</td></tr><tr><td>Sticks, D-pad</td><td>Sticks, D-pad</td><td>Sticks, D-pad</td></tr></tbody></table>

### Accessories

<table><thead><tr><th width="287.75">Mode</th><th>Controls</th></tr></thead><tbody><tr><td><strong>WIIMOTE: Guitar</strong></td><td>Frets: green = SOUTH or L2, red = L1 or EAST, yellow = R1, blue = R2, orange = WEST. Pressing a fret also strums. Whammy: sticks left / right. Star Power: SELECT or sticks up / down. + = START.</td></tr><tr><td><strong>WIIMOTE: Drums(RockBand)</strong></td><td>Red = L2 or EAST, yellow = L1 or D-pad up / left, blue = R1 or D-pad down / right, green = R2 or SOUTH, pedal = sticks left / right.</td></tr><tr><td><strong>WIIMOTE: Drums(GuitarHero)</strong></td><td>Red = L2 or EAST, yellow = L1, blue = R1, orange = R2, green = SOUTH, pedal = sticks left / right.</td></tr><tr><td><strong>WIIMOTE: TaikoDrum</strong></td><td>Drum center (Don) = L2 / R2, rim (Ka) = L1 / R1.</td></tr><tr><td><strong>WIIMOTE: uDraw</strong> and <strong>WIIMOTE: Drawsome tablet</strong></td><td>Stylus = left stick, press = SOUTH, lift = EAST (uDraw: rocker = L1 / R1).</td></tr><tr><td><strong>WIIMOTE: DJ TURNTABLE</strong></td><td>Green / red / blue buttons = L1 / R1 / WEST, turntable = sticks, crossfader = L2 / R2, effects = L3 / R3.</td></tr></tbody></table>

### Picking the mode with the file name

Instead of setting the option for each game, you can add a code to the game's file name, just before the extension. For example, `Super Mario Galaxy.ni.rvz` starts the game in WIIMOTE: NUNCHUK/CURSOR mode.

<table><thead><tr><th width="314">Code</th><th>Mode</th></tr></thead><tbody><tr><td><code>.side.</code></td><td>Sideways Wiimote</td></tr><tr><td><code>.cc.</code></td><td>Classic Controller</td></tr><tr><td><code>.is.</code> <code>.it.</code> <code>.in.</code></td><td>Cursor on the left stick, then swing, tilt or Nunchuk on the right stick</td></tr><tr><td><code>.si.</code> <code>.ti.</code> <code>.ni.</code></td><td>Swing, tilt or Nunchuk on the left stick, cursor on the right stick</td></tr><tr><td><code>.st.</code> <code>.ts.</code> <code>.sn.</code> <code>.ns.</code> <code>.tn.</code> <code>.nt.</code></td><td>Other combinations (s = swing, t = tilt, n = Nunchuk)</td></tr><tr><td><code>.guitar.</code> <code>.drumsrb.</code> <code>.drumsgh.</code> <code>.tatacon.</code> <code>.udraw.</code> <code>.ds.</code> <code>.tt.</code></td><td>Guitar, Rock Band drums, Guitar Hero drums, Taiko drum, uDraw, Drawsome tablet, DJ turntable</td></tr></tbody></table>

### Other emulated Wiimote settings

* **NUMBER OF WIIMOTES**: some games switch to multiplayer as soon as several controllers are connected. Set it to **1** to prevent that.
* **USE MOTION**: with a controller that has a motion sensor (DualShock 4, DualSense, Switch Pro…), moving the controller replaces the Wiimote tilt and shake.
* **RELATIVE IR CURSOR**: turn it off so the pointer goes back to the center when you release the stick.
* **HIDE WIIMOTE POINTER**: the pointer disappears from the screen when you stop moving it.

### Real Wiimotes (DolphinBar)

The easiest way to use real Wiimotes is the Mayflash **DolphinBar**, which is both a receiver and a Sensor Bar:

1. Set the DolphinBar to **mode 4**.
2. Press the sync button on the DolphinBar, then on the Wiimote.
3. In RetroBat, set **CONTROLS > WIIMOTE TYPE** to **REAL**.
4. If needed, set **SENSOR BAR POSITION** (**TOP** or **BOTTOM**) depending on where the DolphinBar sits, and **WIIMOTE IR SENSITIVITY**.



* When a DolphinBar is plugged in, RetroBat turns off continuous Wiimote scanning. **DISABLE WIIMOTE CONTINUOUS SCANNING** forces this setting.
* **BALANCE BOARD**: turn it on only if you use a real Balance Board.
* **BLUETOOTH PASSTHROUGH**: for advanced users who dedicate a Bluetooth adapter to Dolphin.

#### GameCube controllers in REAL mode

With **WIIMOTE TYPE** set to **REAL**, your controllers act as GameCube controllers, for Wii games that accept them (Super Smash Bros. Brawl, Mario Kart Wii…). **GAMECUBE FACE BUTTON LAYOUT** works as on the [GameCube page](gamecube.md#controls).

**USE GAMECUBE CONTROLLERS** uses real GameCube controllers instead, connected through an adapter (Zadig driver, [see the GameCube page](gamecube.md#using-a-real-gamecube-controller-adapter)).

#### REAL AS EMULATED mode

This mode uses real Wiimotes, read by Dolphin as an emulated Wiimote. Hotkeys are then done from the Wiimote:

<table><thead><tr><th width="319">Action</th><th>Wiimote</th></tr></thead><tbody><tr><td>Quit the game</td><td>− + HOME</td></tr><tr><td>Pause</td><td>− + B</td></tr><tr><td>Fullscreen</td><td>− + A</td></tr><tr><td>Save state (with screenshot) / Load state</td><td>− + 1 / − + 2</td></tr><tr><td>Next / previous state slot</td><td>− + UP / − + DOWN</td></tr></tbody></table>

### Light guns

With **GUNS > ENABLE GUN**, Dolphin uses your light gun (Sinden, Gun4IR…) as player 1's Wiimote: the gun aims at the screen, the trigger presses **B**, right click presses **A** and middle click shakes the Wiimote.

For recognized games, RetroBat adapts the buttons with the `system\resources\gamesdb.xml` file. See the [**Gun controls** page](../../../../controllers/gun_controls.md).

To use a Wiimote as a light gun, see the [**Wiimote & DolphinBar** page](../../../../controllers/supported-controllers/lightguns/wiimoteandbar.md).

### lr-dolphin

lr-dolphin offers fewer modes. Pick each player's controller with **CONTROLS > PLAYER 1 CONTROLLER TYPE** (to 4): **WIIMOTE** (default), **WIIMOTE SIDEWAYS**, **WIIMOTE + NUNCHUK**, **CLASSIC CONTROLLER**, **CLASSIC CONTROLLER PRO**, **REAL WIIMOTE** or **GAMECUBE CONTROLLER**.

In **WIIMOTE** mode:

<table><thead><tr><th width="264">RetroBat controller</th><th>Wiimote</th></tr></thead><tbody><tr><td>SOUTH / EAST</td><td>B / A</td></tr><tr><td>NORTH / WEST</td><td>1 / 2</td></tr><tr><td>R2</td><td>Shake</td></tr><tr><td>SELECT / START</td><td>− / +</td></tr><tr><td>R3</td><td>HOME</td></tr><tr><td>Left stick</td><td>Tilt</td></tr><tr><td>Right stick</td><td>Pointer (see <strong>IR MODE</strong>)</td></tr></tbody></table>

The details of the other modes are shown in the RetroArch menu (**Controls > Port 1 Controls**).

### Hotkeys

With a controller, **Dolphin** uses the same hotkeys as on GameCube:

| Action                                    | Controller                     |
| ----------------------------------------- | ------------------------------ |
| Quit the game                             | HOTKEY + START                 |
| Pause                                     | HOTKEY + EAST                  |
| Save state (with screenshot) / Load state | HOTKEY + WEST / HOTKEY + NORTH |
| Next / previous state slot                | HOTKEY + UP / HOTKEY + DOWN    |
| Speed up / slow down                      | HOTKEY + RIGHT / HOTKEY + LEFT |
| Change disc / eject                       | HOTKEY + L2 / HOTKEY + L1      |
| Fullscreen                                | HOTKEY + L3                    |

**lr-dolphin** uses the RetroArch hotkeys (see the [Hotkeys page](../../../../navigation/hotkeys.md)).

## Folders

### Saves

The Wii saves to its internal memory (the **NAND**). Dolphin and lr-dolphin use the same one:

| Content                | Folder                           |
| ---------------------- | -------------------------------- |
| Saves (Wii NAND)       | `saves\wii\dolphin-emu\User\Wii` |
| Dolphin save states    | `saves\wii\dolphin`              |
| lr-dolphin save states | `saves\wii\libretro.dolphin`     |

### Other useful folders

| Content                                  | Folder                                        |
| ---------------------------------------- | --------------------------------------------- |
| Virtual SD card                          | `saves\wii\dolphin-emu\User\Load\WiiSD.raw`   |
| Folder synced with the SD card           | `saves\wii\dolphin-emu\User\Load\WiiSDSync`   |
| Texture packs                            | `saves\wii\dolphin-emu\User\Load\Textures`    |
| Riivolution patches                      | `saves\wii\dolphin-emu\User\Load\Riivolution` |
| Resource packs                           | `saves\wii\dolphin-emu\User\ResourcePacks`    |
| Texture and video dumps                  | `saves\wii\dolphin-emu\User\Dump`             |
| Dolphin controller profiles and settings | `emulators\dolphin-emu\User\Config`           |
| Per-game light gun settings              | `system\resources\gamesdb.xml`                |

**EMULATION > SD CARD PATH** lets you use another SD card image.

## Guides

### Achievements (RetroAchievements) and .rvz games

As on GameCube, RetroBat doesn't recognize .rvz Wii games when indexing achievements. The `system\tools\indexcheevosrvz.bat` tool also processes `roms\wii`: see the [**GameCube** page](gamecube.md#achievements-retroachievements-and-.rvz-games).

### Custom textures and modified games (Riivolution)

Same procedure as on GameCube (see the [**GameCube** page](gamecube.md#custom-textures-dolphin)), with the Wii folders:

* texture packs in `saves\wii\dolphin-emu\User\Load\Textures`;
* Riivolution patches in `saves\wii\dolphin-emu\User\Load\Riivolution`, .json presets in `roms\wii`.

For modified games, first launch a **Wii** game from RetroBat before opening Dolphin, so it uses the Wii folders.

### Using the Wii Menu

1. Open Dolphin (`emulators\dolphin-emu\Dolphin.exe`) and install the Wii Menu with **Tools > Perform Online System Update**, choosing your region.
2. In RetroBat, turn on **EMULATION > RUN WII MENU** in a game's options: the Wii Menu opens instead of the game.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (488).png" alt="" width="563"><figcaption></figcaption></figure></div>

The Wii Menu is installed in the NAND (`saves\wii\dolphin-emu\User\Wii`). For it to be found, first launch a Wii game from RetroBat before opening Dolphin.

To check if the wii menu is correctly installed, try to run it directly from dolphin executable:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (489).png" alt=""><figcaption></figcaption></figure></div>

### WiiWare and Virtual Console games

Put the .wad files in `roms\wii`: they start like other games.

## Known issues

<table><thead><tr><th width="314">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game doesn't respond to controls, or asks to plug in a Nunchuk</td><td>The game expects another controller: set <strong>EMULATED DEVICES</strong> in the game options (<a href="wii.md#controls">see Controls</a>).</td></tr><tr><td>The HOME button doesn't respond</td><td>In Nunchuk or Classic Controller mode, SELECT and START are used for the − and + buttons: the HOME button isn't available.</td></tr><tr><td>The game switches to multiplayer on its own</td><td>Set <strong>NUMBER OF WIIMOTES</strong> to <strong>1</strong>.</td></tr><tr><td>The language doesn't change</td><td>It applies from the second launch of a Wii game (<a href="wii.md#bios">see BIOS</a>).</td></tr><tr><td>Real Wiimotes aren't detected</td><td>Check that the DolphinBar is in <strong>mode 4</strong>, that the Wiimotes are synced and that <strong>WIIMOTE TYPE</strong> is set to <strong>REAL</strong>.</td></tr><tr><td>lr-dolphin doesn't start the game</td><td>lr-dolphin doesn't read .zip, .7z or .json games: extract them, or use Dolphin.</td></tr></tbody></table>
