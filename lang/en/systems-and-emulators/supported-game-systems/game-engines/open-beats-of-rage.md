---
description: Senile Team
---

# Open Beats Of Rage

<div align="left"><figure><img src="../../../.gitbook/assets/image (548).png" alt="" width="530"><figcaption></figcaption></figure></div>

## Overview

**Beats of Rage** is a side-scrolling beat 'em up created in 2003 by Senile Team, as a tribute to Streets of Rage. Its source code was released the following year, and the community turned it into a full game engine: **OpenBOR** (Open Beats of Rage).

Since then, hundreds of fan games have been made with OpenBOR, often inspired by Streets of Rage, Final Fight, Double Dragon or Capcom arcade games. Each game comes in a `.pak` file that contains its graphics, sounds and scripts.

The engine has changed a lot, and each game was written for a specific OpenBOR version. RetroBat offers the **AnyBOR** core, which bundles many engine versions and automatically picks the right one, and the **OpenBOR** program itself.

{% embed url="https://en.wikipedia.org/wiki/Beats_of_Rage#OpenBOR" %}

## At a glance

<table><thead><tr><th width="244"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\openbor</code></td></tr><tr><td><strong>Extensions</strong></td><td>.pak .exe</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: anybor</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic (except specific OpenBOR versions)</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="234.5">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>libretro: anybor</strong> (default)</td><td>Contains about thirty engine versions and automatically picks the one of the game. Save states, special move macros, rumble.</td><td>—</td></tr><tr><td><strong>openbor</strong></td><td>The official OpenBOR engine, recent version provided by RetroBat.</td><td>Games written for an older version may not work properly. No save states.</td></tr><tr><td><strong>openbor-specific-version</strong></td><td>Runs the game with an OpenBOR version you installed yourself (see <a href="open-beats-of-rage.md#using-a-specific-openbor-version">Guides</a>).</td><td>Controllers and settings are set up in OpenBOR.</td></tr></tbody></table>

Keep **anybor**: it is the easiest, as it finds the engine version by itself. If a game does not work, try forcing its version (see [Guides](open-beats-of-rage.md#choosing-the-engine-version-anybor)), then the **openbor** emulator.

## BIOS

No BIOS is needed.

## Which game format should I use?

<table><thead><tr><th width="117.75">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.pak</strong></td><td>The full game in a single file. The most common format.</td></tr><tr><td><strong>.exe</strong></td><td>Game shipped with its own OpenBOR executable, in a folder that also contains its data (<code>data</code> folder or <code>Paks</code> folder).</td></tr></tbody></table>

## Controls

### Automatic configuration

RetroBat configures the controllers automatically with anybor and openbor. Specific OpenBOR versions (**openbor-specific-version**) are set up in OpenBOR.

| RetroBat controller | anybor (AUTO layout)             | openbor, and anybor with the OPENBOR STANDALONE layout |
| ------------------- | -------------------------------- | ------------------------------------------------------ |
| D-pad / left stick  | Move                             | Move                                                   |
| WEST                | Attack                           | Attack                                                 |
| SOUTH               | Jump                             | Jump                                                   |
| EAST                | Special                          | Attack 2                                               |
| NORTH               | Attack 2                         | Special                                                |
| L1                  | Attack 3                         | Attack 4                                               |
| R1                  | Attack 4                         | Attack 3                                               |
| L2, R2, L3, R3      | Character special moves (macros) | —                                                      |
| START               | START                            | START                                                  |
| HOTKEY              | —                                | Escape (OpenBOR menu)                                  |

* The anybor **CONTROLS > BUTTON LAYOUT** option selects the layout: automatic, or **OPENBOR STANDALONE** to get the buttons of the openbor emulator.
* With anybor, **CONTROLS > SPECIAL MOVE MACROS** puts the character special moves on L2, R2, L3 and R3, when the game describes them (enabled by default).
* With anybor, **CONTROLS > USE LEFT STICK AS DPAD** (enabled by default) and **CONTROLS > ENABLE RUMBLE** set the left stick and rumble.

### Hotkeys

anybor uses the standard RetroArch hotkeys (see the [**Hotkeys**](../../../navigation/hotkeys.md) page).

With openbor:

<table><thead><tr><th width="143.25">Hotkey</th><th>Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY</strong></td><td>OpenBOR menu (pause, quit)</td><td>ESC</td></tr><tr><td>—</td><td>Screenshot</td><td>F12</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="279">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Saves (anybor)</td><td><code>saves\openbor</code></td></tr><tr><td>Save states (anybor)</td><td><code>saves\openbor\libretro.anybor</code></td></tr><tr><td>Saves (openbor)</td><td><code>saves\openbor</code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr><tr><td>openbor configuration</td><td><code>emulators\openbor\config.ini</code></td></tr><tr><td>Specific OpenBOR versions</td><td><code>emulators\openbor\&#x3C;version number></code></td></tr></tbody></table>

## Guides

### Adding a game

1. Copy the game `.pak` file to `roms\openbor`.
2. Update the RetroBat game list.
3. Launch the game.

### Game shipped with its executable

Some games are distributed with their own `OpenBOR.exe`. Copy the whole game folder to `roms\openbor`, for example `roms\openbor\My game\OpenBOR.exe`, and update the game list: the executable is what shows up in RetroBat.

* With **anybor**, RetroBat loads the game data (`data\models.txt` or the first `.pak` of the `Paks` folder) without running the executable.
* With **openbor**, RetroBat runs the provided executable.

### Choosing the engine version (anybor)

anybor detects the engine version from the game data. If the detection is wrong:

* Give the version between square brackets at the end of the file name, for example `My game [4086].pak`. It is the same tag as for openbor-specific-version.
* Or select the version in **EMULATION > ENGINE BUILD**.

The game documentation, or the page you downloaded it from, usually gives the OpenBOR version used.

### Using a specific OpenBOR version

1. Download the OpenBOR version you need and place it in a folder named after its version number, for example `emulators\openbor\4153\OpenBOR.exe`.
2. Add this number between square brackets at the end of the game name: `My game [4153].pak`.
3. Select the **openbor-specific-version** emulator for this game.

RetroBat copies the game to the `Paks` folder of this version before running it (the other files of this folder are deleted), then removes it at the end of the session. Controllers and settings are set up in OpenBOR.

### Other useful options

| Option                                     | Effect                                                                                                       |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| **EMULATION > ENGINE BUILD** (anybor)      | Forces the OpenBOR version used for the game.                                                                |
| **VIDEO > ADJUST FOR 4:3 CRT TV** (anybor) | Fits high resolution or widescreen games inside a 640x480 frame with black borders. Only useful on a CRT TV. |
| **SHADER SET** (openbor)                   | OpenBOR picture filters: Bilinear, HQ2X, Scanlines…                                                          |
| **GAME ASPECT RATIO** (openbor)            | **STRETCH** stretches the picture to the whole screen.                                                       |
| **DECORATIONS** (openbor)                  | Shows a bezel around the picture.                                                                            |

## Known issues

| Issue                                                          | Solution                                                                                     |
| -------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| The game crashes, displays incorrectly or does not start       | It needs another engine version: give it in the file name (`[4086]`) or in **ENGINE BUILD**. |
| An `.exe` game does not start with anybor                      | The game folder must contain `data\models.txt` or a `Paks` folder with a `.pak` file.        |
| The buttons do not match those of openbor                      | Set **BUTTON LAYOUT** to **OPENBOR STANDALONE**.                                             |
| With openbor-specific-version, the controller does not respond | RetroBat does not configure specific versions: set the keys in the OpenBOR menu.             |
