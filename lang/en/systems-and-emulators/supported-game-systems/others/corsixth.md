---
description: Corsixth
---

# Theme Hospital

<div align="left"><figure><img src="../../../.gitbook/assets/image (659).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

**Theme Hospital** (Bullfrog, 1997) is a management game: build and run a hospital, cure imaginary diseases and keep the patients happy.

RetroBat uses **CorsixTH**, a free version of the engine: high resolution, fixes, many languages.

The game files are not provided: use the ones from your own copy (CD, GOG).

{% embed url="https://corsixth.com/" %}

## At a glance

<table><thead><tr><th width="235.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\corsixth</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game</td></tr><tr><td><strong>Default emulator</strong></td><td>corsixth</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (controller turned into mouse and keyboard)</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## BIOS

No BIOS is needed. You need the content of the game's `HOSP` folder.

## Which game format?

The game is a `.game` folder holding the files of the `HOSP` folder.

<div align="left"><figure><img src="../../../.gitbook/assets/image (660).png" alt=""><figcaption></figcaption></figure></div>

## Controls

Theme Hospital is played with mouse and keyboard. RetroBat turns the player 1 controller into mouse and keyboard keys (file `system\padtokey\corsixth.keys`):

<table><thead><tr><th width="215.25">RetroBat controller</th><th>Action</th></tr></thead><tbody><tr><td>Left stick</td><td>Move the pointer</td></tr><tr><td>SOUTH</td><td>Left click</td></tr><tr><td>EAST</td><td>Right click</td></tr><tr><td>NORTH</td><td>Rotate object (Space)</td></tr><tr><td>WEST</td><td>Escape</td></tr><tr><td>D-pad</td><td>Scroll the map</td></tr><tr><td>L1 / R1</td><td>Zoom out / in</td></tr><tr><td>L2 (hold)</td><td>Transparent walls</td></tr><tr><td>R2 (hold)</td><td>Speed up time</td></tr><tr><td>START</td><td>Pause</td></tr></tbody></table>

**CONTROLS > CAPTURE MOUSE** (enabled by default) keeps the mouse in the game window.

{% hint style="info" %}
For the controller, zoom, transparent walls and speed up move to the numeric keypad (`-`, `+`, `/`, `*`) instead of `-`, `=`, `x` and `z`. With **AUTOCONFIGURE CONTROLLERS** off, the original game keys are restored.
{% endhint %}

### Hotkeys

<table><thead><tr><th width="219">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="187.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game</td><td><code>roms\corsixth\&#x3C;game>.game</code></td></tr><tr><td>Saves</td><td><code>saves\corsixth</code></td></tr><tr><td>Screenshots</td><td><code>screenshots\corsixth</code></td></tr><tr><td>Configuration</td><td><code>emulators\corsixth\config.txt</code>, <code>emulators\corsixth\hotkeys.txt</code></td></tr></tbody></table>

## Guides

### File layout

Copy the content of the `HOSP` folder (original CD or GOG version) to a folder of `roms\corsixth`, then add `.game` at the end of the folder name:

### Options

* **INTERNAL GAME RESOLUTION**: a higher resolution shows a larger part of the hospital.
* **USER INTERFACE > UI SCALE** enlarges the menus and panels.
* **EMULATION > LANGUAGE**: by default, the EmulationStation language.
