---
description: Microsoft
---

# Windows

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/windows.svg" alt=""><figcaption></figcaption></figure></div>

## Overview

RetroBat is not only for emulators: it also starts your **PC games**. A Windows game needs no emulator. RetroBat starts it, waits until it closes, then goes back to the game list.

Games are sorted into several systems:

<table><thead><tr><th width="231.25">System</th><th width="147">Folder</th><th>Content</th></tr></thead><tbody><tr><td><strong>Windows</strong></td><td><code>roms\windows</code></td><td>Your games: shortcuts, executables, <code>.game</code> files, folders…</td></tr><tr><td><strong>Steam</strong></td><td><code>roms\steam</code></td><td>Steam games</td></tr><tr><td><strong>Epic Games</strong></td><td><code>roms\epic</code></td><td>Epic Games Store games</td></tr><tr><td><strong>GOG.com</strong></td><td><code>roms\gog</code></td><td>GOG Galaxy games</td></tr><tr><td><strong>Amazon Prime Gaming</strong></td><td><code>roms\amazon</code></td><td>Amazon Games games</td></tr><tr><td><strong>EA Games</strong></td><td><code>roms\eagames</code></td><td>EA games (EA app)</td></tr></tbody></table>

The store folders can be filled automatically by RetroBat (see [**Guides**](windows.md#guides)). You can also put everything in `roms\windows`.

{% embed url="https://en.wikipedia.org/wiki/Microsoft_Windows" %}

## At a glance

<table><thead><tr><th width="245.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\windows</code> (and <code>roms\steam</code>, <code>roms\epic</code>, <code>roms\gog</code>, <code>roms\amazon</code>, <code>roms\eagames</code>)</td></tr><tr><td><strong>Extensions</strong></td><td>.exe .bat .cmd .lnk .url .game .pc .win .windows .wine .zip .7z .rar .wsquashfs (stores: .url .bat, and .lnk except Steam)</td></tr><tr><td><strong>Default emulator</strong></td><td>windows (the game is started directly)</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>No: set them in the game or in Steam</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No (depends on the game)</td></tr><tr><td><strong>Light guns</strong></td><td>DemulShooter compatible games</td></tr></tbody></table>

## Which emulator should I choose?

There is nothing to choose: the game is started directly by Windows.

## BIOS

No BIOS is needed.

## Which game format?

| Format                                          | Example                                  | What RetroBat does                                                                                               |
| ----------------------------------------------- | ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Shortcut** `.lnk`                             | `My game.lnk`                            | Starts the shortcut target, with its parameters.                                                                 |
| **Internet shortcut** `.url`                    | `My game.url` (Steam, Epic, GOG, Amazon) | Starts the game through its store, then waits for the game itself.                                               |
| **`.game` file**                                | `My game.game`                           | Text file: line 1 = executable path, next lines = parameters.                                                    |
| **Executable** `.exe`                           | `My game.exe`                            | Starts the executable.                                                                                           |
| **Script** `.bat`, `.cmd`                       | `My game.bat`                            | Starts the script, and looks for the executable it starts to wait for the end of the game.                       |
| **Folder** `.pc`, `.win`, `.windows`, `.wine`   | `My game.pc\`                            | Starts `autorun.cmd`, `autorun.bat`, `autoexec.cmd` or `autoexec.bat`, otherwise the first `.exe` of the folder. |
| **Archive** `.zip`, `.7z`, `.rar`, `.wsquashfs` | `My game.zip`                            | Extracts (or mounts) the game, then starts it like a folder.                                                     |

The `.lnk` shortcut and the `.game` file are the simplest for a game installed anywhere on the PC.

## Controls

RetroBat does not set up controllers for Windows games: set them in the game, or in Steam for Steam games.

The RetroBat control center is not available during a Windows game.

### Hotkeys

<table><thead><tr><th width="214">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Closes the game (when RetroBat found its executable)</td></tr></tbody></table>

### Light guns

For shooting games compatible with **DemulShooter** (The House of the Dead 2, 3 and Overkill, Heavy Fire, Big Buck Hunter, Operation Wolf Returns…), RetroBat starts DemulShooter from two light guns, when **GUNS > ENABLE GUN** is on. The game file name must match the expected name (for example `The House of the Dead 2.lnk`). The other options are in the same menu (**USE DEMULSHOOTER** to force it with a single gun, hide the crosshair or the weapon…). For more details, see the [**Light guns**](../../../controllers/supported-controllers/lightguns/) page.

## Folders

<table><thead><tr><th width="332.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\windows</code></td></tr><tr><td>Store games</td><td><code>roms\steam</code>, <code>roms\epic</code>, <code>roms\gog</code>, <code>roms\amazon</code>, <code>roms\eagames</code></td></tr><tr><td>Games to ignore when scanning a store</td><td><code>roms\&#x3C;store>\&#x3C;store>_ignore.txt</code></td></tr></tbody></table>

Saves stay those of the game (usually in the Windows Documents or AppData folders).

## Guides

### Add an installed game

1. Right-click the game executable, then **Send to > Desktop (create shortcut)**.
2. Move the shortcut to `roms\windows`, and rename it if needed: its name is shown in the game list.

Other method: create a text file `My game.game` in `roms\windows`, with the executable path on the first line (and, if needed, its parameters on the next lines). A path starting with `.\` starts from the folder of the `.game` file.

<div align="left"><figure><img src="../../../.gitbook/assets/image (760).png" alt=""><figcaption></figcaption></figure></div>

### Add a store game (Steam, Epic, GOG, Amazon, EA)

**Automatically**: enable **GAME SETTINGS > WINDOWS GAMES > SCAN INSTALLED STORE GAMES (STEAM, EPIC...)** (**GAME STORES AND LAUNCHERS** section). At startup, RetroBat creates a shortcut for each installed game in `roms\steam`, `roms\epic`, `roms\gog`, `roms\amazon` and `roms\eagames`, and removes those of uninstalled games.

| Option (WINDOWS GAMES)                          | Effect                                                                                                   |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| **SCAN INSTALLED STORE GAMES (STEAM, EPIC...)** | Creates shortcuts for installed games at RetroBat startup.                                               |
| **INCLUDE UNINSTALLED GAMES**                   | Also adds the Steam games of your library that are not installed.                                        |
| **KEEP GAMES ADDED MANUALLY**                   | Does not delete the shortcuts you added yourself to the store folders.                                   |
| **KILL LAUNCHER WHEN EXIT**                     | Closes Steam, Epic… when quitting the game. By default, the store is closed only if the game started it. |
| **TRY TO READ EXECUTABLE IN BAT FILES**         | Looks for the executable started by a `.bat` or `.cmd` file (on by default).                             |

To stop a game from being added by the scan, write its ID in `roms\<store>\<store>_ignore.txt` (one per line, for example `roms\steam\steam_ignore.txt`).

<div align="left"><figure><img src="../../../.gitbook/assets/image (761).png" alt=""><figcaption></figcaption></figure></div>

**Manually**: copy the game shortcut created by the store (`.url`) to `roms\windows` or to the store folder.

<div align="left"><figure><img src="../../../.gitbook/assets/image (762).png" alt=""><figcaption></figcaption></figure></div>

### Add an Xbox / Game Pass game

Microsoft Store and Game Pass games are protected applications.

* **Game installed in `C:\XboxGames`**: open its `Content` folder, make a shortcut to the game executable and put it in `roms\windows`.
* **Shortcut created by the Xbox app**: put it in `roms\windows`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (763).png" alt="" width="342"><figcaption></figcaption></figure></div>

RetroBat does not always find the game behind this shortcut. Then create next to it a text file with the same name and the `.uwp` extension, holding the application name (shown in the shortcut properties, for example `Microsoft.SeaofThieves`). RetroBat deduces the game executable from it.

<div align="left"><figure><img src="../../../.gitbook/assets/image (764).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (765).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (766).png" alt=""><figcaption></figcaption></figure></div>

### Add an Ubisoft Connect game

Create a `.bat` file in `roms\windows` that starts the game through its Ubisoft address (`uplay://launch/<id>/0`, shown in a shortcut created by Ubisoft Connect), then waits for the end of the game:

```batch
@echo OFF
REM Ubisoft game id
START uplay://launch/00000/0
TIMEOUT /t 30
:RUNNING
REM Exact name of the game executable
tasklist|findstr "MyGame.exe" > nul
IF %errorlevel%==1 timeout /t 5 & GOTO ENDLOOP
timeout /t 2
GOTO RUNNING
:ENDLOOP
```

Replace `00000` with the game ID...

<div align="left"><figure><img src="../../../.gitbook/assets/image (767).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (768).png" alt=""><figcaption></figcaption></figure></div>

... and `MyGame.exe` with the name of its executable (shown in Task Manager while playing or available in the game data folder).

<div align="left"><figure><img src="../../../.gitbook/assets/image (769).png" alt=""><figcaption></figcaption></figure></div>

To also close Ubisoft Connect when quitting, replace the `IF` line with:

```batch
IF %errorlevel%==1 timeout /t 5 & taskkill /F /IM upc.exe /T & GOTO ENDLOOP
```

Set Ubisoft Connect to sign you in automatically.

### RetroBat music plays during the game

RetroBat waits for the end of the game before going back to the game list. If it does not find the game (game started by a launcher, wrong executable detected in a store), it comes back too early and its music plays.

1. Start the game outside RetroBat, until you are in game.
2. Open Task Manager (**CTRL + SHIFT + ESC**) and note the name of the game executable.
3. Next to the game file (for example `My game.lnk`), create a text file with the same name and the `.gameexe` extension: `My game.gameexe`.
4. Write the executable name in it, with or without `.exe`. If the game starts a second program (launcher then game), write the second name on a second line.

RetroBat then waits for the end of this program. The `.gameexe` file works with all game formats.

<div align="left"><figure><img src="../../../.gitbook/assets/image (770).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../.gitbook/assets/image (771).png" alt=""><figcaption></figcaption></figure></div>

If the game takes long to start, increase **EMULATION > WAIT TIME** in the game options (30 seconds by default).

## Known issues

<table><thead><tr><th width="347.75">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>RetroBat music plays in game, or RetroBat goes back to the list too early</td><td>See <a href="windows.md#retrobat-music-plays-during-the-game"><strong>RetroBat music plays during the game</strong></a>.</td></tr><tr><td>HOTKEY + START does not close the game</td><td>RetroBat did not find the game executable: add a <code>.gameexe</code> file.</td></tr><tr><td>A store game disappears from the list</td><td>The scan removes the shortcuts of uninstalled games: enable <strong>KEEP GAMES ADDED MANUALLY</strong> for shortcuts you added yourself.</td></tr><tr><td>Steam stays open after the game</td><td>Enable <strong>KILL LAUNCHER WHEN EXIT</strong>.</td></tr><tr><td>The controller does not work in game</td><td>The game does not detect the controller: set it in the game, or add the game to Steam and use the Steam configuration.</td></tr></tbody></table>
