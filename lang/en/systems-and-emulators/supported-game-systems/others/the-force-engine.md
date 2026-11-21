# The Force Engine

<div align="left"><figure><img src="../../../.gitbook/assets/image (670).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**Star Wars: Dark Forces** (LucasArts, 1995) is a first-person shooter in the Star Wars universe.

RetroBat uses **The Force Engine**, a modern engine that recreates the original game: high resolution, widescreen, OpenGL rendering, mods.

The game files are not provided: use the ones from your own copy (DOS CD, Steam, GOG).

{% embed url="https://theforceengine.github.io/" %}

## At a glance

<table><thead><tr><th width="237.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\theforceengine</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game</td></tr><tr><td><strong>Default emulator</strong></td><td>theforceengine</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>No: The Force Engine controls</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## BIOS

No BIOS is needed. Copy the Dark Forces files (including `DARK.GOB`) to `roms\theforceengine`.

## Which game format?

A `.game` file placed in the folder of the game files starts Dark Forces. If it holds the name of a mod on its first line, the mod is started (see [**Guides**](the-force-engine.md#start-a-mod)).

## Controls

RetroBat does not configure the controller: The Force Engine recognizes it and its controls are changed in its options.

**CONTROLS > DISABLE AUTOAIM** and **DISABLE CROSSHAIR** can be set in RetroBat.

### Hotkeys

<table><thead><tr><th width="251.5">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="212.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game</td><td><code>roms\theforceengine</code></td></tr><tr><td>Mods</td><td><code>roms\theforceengine\Mods</code></td></tr><tr><td>Saves and configuration</td><td><code>emulators\theforceengine</code> (<code>settings.ini</code> makes the install portable)</td></tr></tbody></table>

## Guides

### File layout

Copy the original DOS game (or the Steam / GOG version) to `roms\theforceengine`. Example with the DOS version:

<div align="left"><figure><img src="../../../.gitbook/assets/image (673).png" alt=""><figcaption></figcaption></figure></div>

Create a text file in the same folder as the game executable, then change its extension to `.game`.

### Start a mod

Put the mod in `roms\theforceengine\Mods`:

Create a text file with an easy to recognize name (it is shown in the game list), write the full name of the mod (with its extension) on the first line, then change the extension to `.game`:

<div align="left"><figure><img src="../../../.gitbook/assets/image (671).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (672).png" alt=""><figcaption></figcaption></figure></div>

### Options

* **INTERNAL RESOLUTION** from 200p to 2160p (default: screen resolution), **VIDEO > WIDESCREEN**.
* **EMULATION > DISABLE CUTSCENES**, **USER INTERFACE > SHOW SUBTITLES**.

## Known issues

| Issue                                   | Solution                                                      |
| --------------------------------------- | ------------------------------------------------------------- |
| The Force Engine does not find the game | The `.game` file must be in the folder that holds `DARK.GOB`. |
