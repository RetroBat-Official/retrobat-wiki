# Sonic 3 AIR

<div align="left"><figure><img src="../../../../.gitbook/assets/image (665).png" alt="" width="349"><figcaption></figcaption></figure></div>

## Overview

**Sonic 3 A.I.R.** (Angel Island Revisited) is an enhanced PC version of **Sonic 3 & Knuckles** (Sega, 1994), made by Eukaryot. It keeps the exact physics of the original game and adds widescreen, high resolution, many fixes, options (Tails as an assistant, new game modes), a two-player mode and mod support.

The game is not supplied: Sonic 3 A.I.R. reads the data from your own Sonic 3 & Knuckles ROM.

{% embed url="https://sonic3air.org/" %}

## At a glance

<table><thead><tr><th width="237.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\sonic3-air</code></td></tr><tr><td><strong>Extensions</strong></td><td>.bin</td></tr><tr><td><strong>Default emulator</strong></td><td>sonic3air</td></tr><tr><td><strong>BIOS</strong></td><td>None (Sonic 3 &#x26; Knuckles ROM required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (2 players)</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## BIOS

No BIOS is needed.

## Which game format?

A **Sonic 3 & Knuckles** ROM in **.bin** format. The recommended ROM is the one from the Steam version of Sonic 3 & Knuckles, `Sonic_Knuckles_wSonic3.bin`. Put it in `roms\sonic3-air`: RetroBat gives its location to the game at each launch.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (666).png" alt=""><figcaption></figcaption></figure></div>

## Controls

RetroBat sets up the controllers of players 1 and 2 automatically:

<table><thead><tr><th width="239">RetroBat controller</th><th>Sonic 3 A.I.R.</th></tr></thead><tbody><tr><td>D-pad</td><td>Move</td></tr><tr><td>SOUTH, EAST, WEST</td><td>Jump and character abilities</td></tr><tr><td>NORTH</td><td>Super transformation</td></tr><tr><td>START</td><td>Pause</td></tr></tbody></table>

Two controllers of the same model cannot be used at the same time: Sonic 3 A.I.R. mixes them up.

**CONTROLS > RUMBLE STRENGTH** sets the rumble of both controllers.

### Hotkeys

<table><thead><tr><th width="199">Action</th><th>Controller</th></tr></thead><tbody><tr><td>Exit</td><td>HOTKEY + START</td></tr></tbody></table>

No save states: progress is saved by the game.

## Folders

<table><thead><tr><th width="310.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game saves</td><td><code>emulators\sonic3air\savedata\storage</code>, copied by RetroBat to <code>saves\sonic3air\storage</code></td></tr><tr><td>Settings (written by RetroBat)</td><td><code>emulators\sonic3air\savedata\settings.json</code>, <code>settings_input.json</code></td></tr><tr><td>Mods</td><td><code>emulators\sonic3air\savedata\mods</code></td></tr><tr><td>Remastered soundtrack (downloaded from the game)</td><td><code>emulators\sonic3air\savedata\data</code></td></tr></tbody></table>

## Guides

### Remastered soundtrack

The remastered soundtrack is no longer included in the game: it is downloaded once from the game's **Options** menu. It then stays in the emulator's `savedata` folder.

### Mods

Sonic 3 A.I.R. manages its own mods. Put the mod (folder or `.zip`) in `emulators\sonic3air\savedata\mods`, then enable it in the game's **Mods** menu.

### Useful options

<table><thead><tr><th width="310.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>SHADER SET</strong></td><td>Picture filter (sharp, soft, xBRZ, HQx).</td></tr><tr><td><strong>VISUAL RENDERING > SCANLINES</strong></td><td>Scanlines; not with the HQ and xBRZ filters.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="281.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game asks for the ROM</td><td>Check that the Sonic 3 &#x26; Knuckles ROM is in <code>roms\sonic3-air</code> and launch it from RetroBat.</td></tr><tr><td>Player 2 also controls player 1</td><td>Both controllers are the same model: use two different models.</td></tr><tr><td>No remastered music</td><td>Download it from the game's <strong>Options</strong> menu (see <a href="sonic3air.md#remastered-soundtrack"><strong>Remastered soundtrack</strong></a>).</td></tr></tbody></table>
