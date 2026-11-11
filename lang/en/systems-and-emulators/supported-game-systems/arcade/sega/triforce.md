---
description: Namco, Sega, Nintendo
---

# Triforce

<div align="left"><figure><img src="../../../../.gitbook/assets/image (490).png" alt=""><figcaption></figcaption></figure></div>

## Overview

The **Triforce** is an arcade system designed together by **Nintendo**, **Namco** and **Sega**, hence its name: three companies, like the three triangles of Zelda's Triforce. The first game, Virtua Striker 2002, came out in 2002.

The system uses the **GameCube** architecture (IBM "Gekko" processor, ATI "Flipper" graphics chip), with more memory and arcade cabinet electronics. Like the Naomi and Chihiro systems, most games ship on **GD-ROM**: the whole disc is copied to the memory of a DIMM board at startup, so there is no loading during gameplay.

Its library is short but memorable:

* **F-Zero AX** and **F-Zero AX Monster Ride** (Sega / Nintendo): F-Zero AX could exchange data with F-Zero GX on GameCube, through the memory card;
* **Mario Kart Arcade GP** and **Mario Kart Arcade GP 2** (Namco / Nintendo);
* **Virtua Striker 2002**, **Virtua Striker 4** and **Virtua Striker 4 Ver. 2006** (Sega);
* **Gekitou Pro Yakyuu** (Sega).

{% embed url="https://en.wikipedia.org/wiki/List_of_Sega_arcade_system_boards#Triforce" %}

## At a glance

<table><thead><tr><th width="227.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\triforce</code></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .zip .cue .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>dolphin</td></tr><tr><td><strong>BIOS</strong></td><td>None required (<code>segaboot.gcm</code> optional, for the test menu)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, Dolphin</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Wheels</strong></td><td>TeknoParrot</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="156.5">Emulator</th><th width="133.75">For whom?</th><th width="231.75">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>dolphin</strong> (default)</td><td>Everyone</td><td>Current Dolphin version, which emulates the Triforce. HD, widescreen, controls laid out for each game, test menu, game patches.</td><td>—</td></tr><tr><td><strong>lr-dolphin</strong></td><td>RetroArch users</td><td>RetroArch features (shaders, RetroArch menu).</td><td>Fewer settings.</td></tr><tr><td><strong>dolphin-triforce</strong></td><td>Special cases</td><td>Older Triforce-specific Dolphin build (the "Crediar" build), kept for games that run better on it.</td><td>Frozen version, no longer updated.</td></tr><tr><td><strong>TeknoParrot</strong></td><td>Wheel users</td><td>Wheels and force feedback for F-Zero AX and Mario Kart Arcade GP.</td><td>Requires installing TeknoParrot (see the <a href="../teknoparrot.md"><strong>TeknoParrot</strong> page</a>).</td></tr></tbody></table>

**When in doubt, keep dolphin.**

## BIOS

No BIOS is needed to play.

<table><thead><tr><th width="178.25">File</th><th width="335.25">Role</th><th>Location</th></tr></thead><tbody><tr><td><code>segaboot.gcm</code></td><td>Optional: cabinet test menu, with Dolphin</td><td><code>bios\triforce</code></td></tr></tbody></table>

* RetroBat copies `segaboot.gcm` to `emulators\dolphin-emu\User\Triforce` itself when a game is launched with Dolphin.
* RetroBat checks that this file is present.
* dolphin-triforce doesn't need it.

## Which game format?

| Format     | dolphin                 | lr-dolphin | dolphin-triforce        | Notes           |
| ---------- | ----------------------- | ---------- | ----------------------- | --------------- |
| **.iso**   | ✔                       | ✔          | ✔                       | Game image.     |
| .zip / .7z | ✔ (extracted at launch) | ✘          | ✔ (extracted at launch) | Slower loading. |

For TeknoParrot, see the [**TeknoParrot** page](../teknoparrot.md).

## Controls

### Automatic configuration

RetroBat configures player 1 and player 2 controllers automatically, for all emulators. With Dolphin and dolphin-triforce, the control layout is **picked automatically for each game**: Mario Kart, F-Zero, Virtua Striker or standard layout.

The **CONTROLS > CONTROLLER LAYOUT** option forces a layout: **STANDARD**, **MARIO KART GP**, **F ZERO**, **VIRTUA STRIKER** or **VIRTUA STRIKER 2002**.

### Cabinet buttons

<table><thead><tr><th width="152.75">RetroBat controller</th><th width="174.75">Dolphin</th><th width="194.5">dolphin-triforce</th><th width="196">lr-dolphin</th></tr></thead><tbody><tr><td>SELECT</td><td>Credit (Coin)</td><td>Credit (Coin)</td><td>Credit (Coin)</td></tr><tr><td>START</td><td>Start</td><td>Start</td><td>Start</td></tr><tr><td>L3</td><td>Service</td><td>—</td><td>—</td></tr><tr><td>R3</td><td>Test (cabinet menu)</td><td>Test (cabinet menu)</td><td>—</td></tr><tr><td>L1</td><td>—</td><td>—</td><td>Test (cabinet menu)</td></tr></tbody></table>

### Game controls

Controls are placed the same way with Dolphin and dolphin-triforce:

<table><thead><tr><th width="344">Game</th><th>Controls</th></tr></thead><tbody><tr><td><strong>Mario Kart Arcade GP 1 and 2</strong></td><td>Wheel = left stick, accelerate = R2, brake = L2, item = EAST, cancel = SOUTH.</td></tr><tr><td><strong>F-Zero AX</strong>, <strong>F-Zero AX Monster Ride</strong></td><td>Wheel = left stick, accelerate = R2, brake = L2, left / right paddles = L1 / R1, boost = WEST, views = D-pad.</td></tr><tr><td><strong>Virtua Striker 4</strong>, <strong>Virtua Striker 4 Ver. 2006</strong></td><td>Move = left stick, short pass = SOUTH, long pass = WEST, shoot = EAST, dash = NORTH, tactics = D-pad up / right / down.</td></tr><tr><td><strong>Virtua Striker 2002</strong></td><td>Move = D-pad, short pass = SOUTH, long pass = EAST, shoot = WEST.</td></tr><tr><td><strong>Gekitou Pro Yakyuu</strong></td><td>D-pad, EAST and SOUTH buttons, WEST = Gekitou.</td></tr><tr><td>Other games (STANDARD)</td><td>GameCube controller layout: A = EAST, B = SOUTH, Y = WEST, L / R triggers = L2 / R2, sticks and D-pad.</td></tr></tbody></table>

To configure your controllers yourself, turn off **AUTOCONFIGURE CONTROLLERS**.

### Hotkeys

**Dolphin** and **dolphin-triforce** use the same hotkeys as on GameCube: **HOTKEY + START** to quit, **HOTKEY + WEST** / **HOTKEY + NORTH** for save states (Dolphin)…

**lr-dolphin** uses the RetroArch hotkeys (see the [Hotkeys page](../../../../navigation/hotkeys.md)).

## Folders

<table><thead><tr><th width="339">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Dolphin save states</td><td><code>saves\triforce\dolphin</code></td></tr><tr><td>lr-dolphin save states</td><td><code>saves\triforce\libretro.dolphin</code></td></tr><tr><td>Cabinet data (Dolphin)</td><td><code>emulators\dolphin-emu\User\Triforce</code></td></tr><tr><td>Per-game settings and patches (Dolphin)</td><td><code>emulators\dolphin-emu\User\GameSettings</code></td></tr><tr><td>List of patches offered by RetroBat</td><td><code>system\tools\triforce_patches.json</code></td></tr><tr><td>dolphin-triforce</td><td><code>emulators\dolphin-triforce</code></td></tr></tbody></table>

## Guides

### Game patches

Some games get stuck at startup, wait for cabinet hardware that isn't there (F-Zero seat motor, Mario Kart GP 2 camera, cabinet link…) or slow down. RetroBat offers patches for these games, in the game options, under **GAME PATCHES**:

<table><thead><tr><th width="272.75">Game</th><th>Patches</th></tr></thead><tbody><tr><td>F-Zero AX</td><td>Disable the motor setup (rev D or rev E, depending on your version).</td></tr><tr><td>F-Zero AX Monster Ride</td><td>Disable the motor, bypass the Cycraft seat, fix slowdowns.</td></tr><tr><td>Mario Kart Arcade GP</td><td>Loop fix, skip the cabinet link, fix slowdowns, skip the boot check.</td></tr><tr><td>Mario Kart Arcade GP 2</td><td>Disable the camera (NamCam), loop fix, slowdown fix, skip the cabinet link and boot checks (US or JAP versions).</td></tr><tr><td>Virtua Striker 4 / Ver. 2006</td><td>Bypass boot (2006 version: US or JAP).</td></tr></tbody></table>

All patches are off by default: only turn on the ones matching your game and its version.

## Known issues

| Issue                                                   | Solution                                                                                 |
| ------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| The game is stuck on a check or error screen at startup | Turn on the matching patch in **GAME PATCHES** (see [Guides](triforce.md#game-patches)). |
| The test menu doesn't open with Dolphin                 | Put `segaboot.gcm` in `bios\triforce`.                                                   |
| The controls don't match the game                       | Pick the right **CONTROLLER LAYOUT** in the game options.                                |
| A game doesn't work with Dolphin                        | Try **dolphin-triforce**.                                                                |
| lr-dolphin doesn't start the game                       | lr-dolphin doesn't read .zip or .7z games: extract them, or use Dolphin.                 |
