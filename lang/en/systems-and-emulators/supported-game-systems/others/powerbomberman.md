# Power Bomberman

<div align="left"><figure><img src="../../../.gitbook/assets/image (772).png" alt=""><figcaption></figcaption></figure></div>

## Overview

**Power Bomberman** is a free game made by Bomberman fans, released in 2013 and still updated. It recreates the battle mode of the series, with many characters, stages and items (kick, glove, special bombs…), and is played with several players locally or online.

RetroBat installs the game and starts it like the other systems.

{% embed url="https://www.bombermanboard.com/viewtopic.php?t=1925" %}

## At a glance

<table><thead><tr><th width="247.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\pb</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pb</td></tr><tr><td><strong>Default emulator</strong></td><td>powerbomberman</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>In the game (online)</td></tr></tbody></table>

## Which emulator should I choose?

There is nothing to choose: the game itself, `emulators\powerbomberman\Power Bomberman.exe`. It is not an emulator.

## BIOS

No BIOS is needed.

## Which game format?

RetroBat starts the game from an **empty** `.pb` **file** in `roms\pb`, for example `Power Bomberman.pb`. If `roms\pb` is empty, create this file: its name is the one shown in the game list.

## Controls

RetroBat sets up controllers automatically (up to 16), DirectInput controllers first, then XInput controllers.

<table><thead><tr><th width="240.25">RetroBat controller</th><th>Power Bomberman</th></tr></thead><tbody><tr><td>D-pad, left stick</td><td>Move</td></tr><tr><td>START</td><td>Start</td></tr><tr><td>EAST</td><td>Action button 1</td></tr><tr><td>SOUTH</td><td>Action button 2</td></tr><tr><td>WEST</td><td>Action button 3</td></tr><tr><td>NORTH</td><td>Action button 4</td></tr><tr><td>L1</td><td>Action button 5</td></tr><tr><td>R1</td><td>Action button 6</td></tr></tbody></table>

The role of each button (drop a bomb, punch, stop a bomb…) is shown and can be changed in the game options.

Without a controller, player 1 plays with the keyboard: arrows to move, **ENTER** for Start, **D**, **S**, **A**, **W**, **Q** and **E** for the action buttons (QWERTY keyboard; **D**, **S**, **Q**, **Z**, **A** and **E** on AZERTY).

To set the keys yourself in the game, disable **AUTOCONFIGURE CONTROLLERS**: otherwise RetroBat replaces the settings at each launch.

### Hotkeys

<table><thead><tr><th width="229">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Exit</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="229">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Launch file</td><td><code>roms\pb</code></td></tr><tr><td>Game</td><td><code>emulators\powerbomberman</code></td></tr><tr><td>Settings and keys</td><td><code>%LOCALAPPDATA%\pb\config.ini</code></td></tr></tbody></table>

Power Bomberman keeps its settings in the Windows folder `%LOCALAPPDATA%\pb` (usually `C:\Users\<name>\AppData\Local\pb`), not in the RetroBat folder. At first launch, RetroBat copies a suitable settings file there.

## Guides

### Options

<table><thead><tr><th width="282.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>VERTICAL SYNC</strong></td><td>On by default. Avoids screen tearing.</td></tr><tr><td><strong>VIDEO > FORCE FULLSCREEN</strong></td><td>Fullscreen even when RetroBat is windowed.</td></tr></tbody></table>

### Playing online

Online play starts from the game menu. Your nickname and online settings are in `%LOCALAPPDATA%\pb\config.ini` (`[NETPLAY]` section).

## Known issues

<table><thead><tr><th width="280.25">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>The system does not show</td><td>Create an empty <code>Power Bomberman.pb</code> file in <code>roms\pb</code>.</td></tr><tr><td>Keys set in the game are lost</td><td>RetroBat replaces them at each launch: disable <strong>AUTOCONFIGURE CONTROLLERS</strong>.</td></tr><tr><td>Players are not in controller order</td><td>The game numbers DirectInput controllers first, then XInput controllers.</td></tr></tbody></table>
