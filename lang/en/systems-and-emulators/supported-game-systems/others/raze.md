---
description: Raze
---

# Raze

<div align="left"><figure><img src="../../../.gitbook/assets/image (744).png" alt=""><figcaption></figcaption></figure></div>

## Overview

**Raze** is a modern engine, based on GZDoom, for the Build engine games: **Duke Nukem 3D**, **Blood**, **Shadow Warrior**, **Redneck Rampage**, **PowerSlave / Exhumed**, **NAM**, **World War II GI** and their add-ons.

It brings OpenGL or Vulkan rendering, high resolution, widescreen and a common interface for all games.

The game files are not provided: use the ones from your own copies.

{% embed url="https://raze.zdoom.org/about" %}

## At a glance

<table><thead><tr><th width="240.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\raze</code></td></tr><tr><td><strong>Extensions</strong></td><td>.raze</td></tr><tr><td><strong>Default emulator</strong></td><td>raze</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (Raze controls, menu on START)</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves, quick save / load with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

Raze is also offered in the [**Duke Nukem 3D**](duke-nukem-3d.md) system, with the same `.eduke32` files.

## Supported games

The list of games and recognized versions is on the ZDoom wiki:

{% embed url="https://zdoom.org/wiki/Raze#Supported_games" %}

## BIOS

No BIOS is needed. You need the files of each game (`.grp`, `.rff`, `.art`…), for example `DUKE3D.GRP` for Duke Nukem 3D or `BLOOD.RFF` and its files for Blood.

## Which game format?

A game is launched with a `.raze` text file placed in `roms\raze`.

| File content                               | Effect                                                                  |
| ------------------------------------------ | ----------------------------------------------------------------------- |
| A single line: path of the main game file  | The file is started as the main game (`-iwad`).                         |
| Several lines: one Raze parameter per line | The lines are passed as they are to Raze (for example `-file`, `-map`). |

A path starting with `/` or `\` starts from the folder of the `.raze` file. A full path (`C:\...`) is also accepted.

## Controls

### Automatic configuration

RetroBat enables the controller in Raze and keeps its default controls. START opens the menu; SELECT stays free for the RetroBat hotkeys. Controls are changed in Raze **Options > Customize Controls**.

**CONTROLS > ALWAYS RUN** (enabled by default) and **STICK DEADZONE** adjust the controller.

### Hotkeys

<table><thead><tr><th width="260.25">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr><tr><td>HOTKEY + SOUTH</td><td>Menu (Escape)</td></tr><tr><td>HOTKEY + WEST</td><td>Quick save</td></tr><tr><td>HOTKEY + NORTH</td><td>Quick load</td></tr><tr><td>HOTKEY + R3</td><td>Screenshot</td></tr></tbody></table>

See the [**Hotkeys**](../../../navigation/hotkeys.md) page for more details.

## Folders

<table><thead><tr><th width="231.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games and launch files</td><td><code>roms\raze</code></td></tr><tr><td>Saves</td><td><code>saves\raze</code></td></tr><tr><td>Screenshots</td><td><code>screenshots\raze</code></td></tr><tr><td>Configuration</td><td><code>emulators\raze\raze_portable.ini</code></td></tr></tbody></table>

## Guides

### Add a game

Create a text file, write the path of the main game file from the file's folder, then save it with the `.raze` extension:

<div align="left"><figure><img src="../../../.gitbook/assets/image (745).png" alt=""><figcaption></figcaption></figure></div>

### Launch a game with parameters

To add files (add-on, mod) or other parameters, write one parameter per line. Lines starting with `/` or `\` are paths from the file's folder:

<div align="left"><figure><img src="../../../.gitbook/assets/image (746).png" alt=""><figcaption></figcaption></figure></div>

Save the file with the `.raze` extension in `roms\raze`.

## Known issues

<table><thead><tr><th width="339">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>"raze file does not contain any launch argument"</td><td>The <code>.raze</code> file is empty: write the game file.</td></tr><tr><td>Raze shows the game list instead of starting the game</td><td>The path in the <code>.raze</code> file is wrong, or the game version is not recognized (see the supported games list).</td></tr><tr><td>The bezel is not displayed</td><td>It needs <strong>GAME ASPECT RATIO</strong> on automatic or 4/3.</td></tr></tbody></table>
