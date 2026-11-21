---
description: Worlds of Wonder
---

# Actionmax

## Overview

The **Action Max** is a console by Worlds of Wonder, released in 1987. It has no game processor: games are VHS tapes, played by a VCR connected to the console. The player shoots at the TV with a light gun, and a sensor stuck on the screen detects the light flashes in the video to count the points. It disappeared as early as 1988.

Only 5 games were released:

<table><thead><tr><th width="257.75">Game</th><th>File</th></tr></thead><tbody><tr><td>.38 Ambush Alley</td><td><code>38ambushalley</code></td></tr><tr><td>Blue Thunder</td><td><code>bluethunder</code></td></tr><tr><td>Hydrosub: 2021</td><td><code>hydrosub2021</code></td></tr><tr><td>Pops 'N Pals: Pops Ghostly</td><td><code>popsghostly</code></td></tr><tr><td>Sonic Fury</td><td><code>sonicfury</code></td></tr></tbody></table>

In RetroBat, these games run with a **Singe** script that recreates the console: it plays the tape video, shows the crosshair and counts the good shots.

{% embed url="https://en.wikipedia.org/wiki/Action_Max" %}

## At a glance

<table><thead><tr><th width="195.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\actionmax</code></td></tr><tr><td><strong>Extensions</strong></td><td>.actionmax</td></tr><tr><td><strong>Default emulator</strong></td><td>hypseus</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators (player 1)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>Hypseus, Singe2</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="162">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>hypseus</strong> (default)</td><td>Reads the Hypseus version of the games (zip or folder). Several light guns, bezels.</td><td>—</td></tr><tr><td><strong>singe2</strong></td><td>The emulator by the author of Singe, with its own version of the games (<code>.mkv</code> videos).</td><td>Files differ from the Hypseus ones. Needs Windows developer mode. One light gun only.</td></tr></tbody></table>

**If in doubt, keep hypseus.**

## BIOS

No BIOS is needed.

## Which game format?

Each game starts from an **empty file** `<game>.actionmax` (for example `38ambushalley.actionmax`) that you create. This file tells RetroBat which game to start; the videos and the script are next to it.

<table><thead><tr><th width="347.25">Format</th><th width="91.5">hypseus</th><th width="74.5">singe2</th><th>Notes</th></tr></thead><tbody><tr><td><strong>Zip</strong> (<code>roms\actionmax\roms\actionmax.zip</code>)</td><td>✔</td><td>✘</td><td>Recommended method for Hypseus.</td></tr><tr><td><code>actionmax.hypseus</code> folder</td><td>✔</td><td>✘</td><td>Old method for Hypseus.</td></tr><tr><td><code>ActionMax</code> folder (Singe 2 version)</td><td>✘</td><td>✔</td><td>Only format for Singe2.</td></tr></tbody></table>

The tape videos and sound must be provided. The names of the `.actionmax` files must be exactly those of the **Overview** table, in lowercase.

Each method is detailed in [**Guides**](actionmax.md#guides).

## Controls

RetroBat sets up the player 1 controller automatically for both emulators.

The Action Max is played with a **light gun** or the **mouse**: aim, then shoot. On the mode selection screen, shoot the left half for the normal mode, the right half for the limited ammo mode.

| Action | Hypseus                                                 | Singe2                        |
| ------ | ------------------------------------------------------- | ----------------------------- |
| Shoot  | Gun trigger, left mouse click, **R1** on the controller | Gun trigger, left mouse click |
| Aim    | Light gun or mouse                                      | Light gun or mouse            |
| Exit   | **HOTKEY + START**, ESC                                 | **HOTKEY + START**, ESC       |

The **SHOW CROSSHAIR** option shows or hides the crosshair.

### Light guns

To connect and set up a light gun in RetroBat, see the [**Light guns**](../../../controllers/supported-controllers/lightguns/) page.

* **Hypseus**: several light guns are detected automatically (one mouse per gun). The **GUNS > USE ONE GUN ONLY** option keeps only one. With a Sinden gun, RetroBat starts the Sinden software and shows the white border.
* **Singe2**: one light gun only. The **GUNS > FORCE INDEX** option picks the mouse to use.

## Folders

| Content                                | Folder                              |
| -------------------------------------- | ----------------------------------- |
| `.actionmax` files (zip method)        | `roms\actionmax\vldp\actionmax`     |
| `.actionmax` files (other methods)     | `roms\actionmax`                    |
| Zip script                             | `roms\actionmax\roms\actionmax.zip` |
| Videos (zip method)                    | `roms\actionmax\vldp\actionmax`     |
| Script and videos (old Hypseus method) | `roms\actionmax\actionmax.hypseus`  |
| Script and videos (Singe2)             | `roms\actionmax\ActionMax`          |
| Hypseus keys                           | `emulators\hypseus\hypinput.ini`    |
| Hypseus bezels                         | `emulators\hypseus\bezels`          |
| Hypseus screenshots (F12)              | `emulators\hypseus\screenshots`     |

## Guides

### Install the zip games (Hypseus)

1. Get `actionmax.zip` from the `00-zip-roms\00-Elder-Modernized-zip-rom` folder of the Hypseus `hypseus_singe_data` repository on GitHub, and copy it to `roms\actionmax\roms`.
2. Create the `roms\actionmax\vldp\actionmax` folder.
3. Copy the games' `.txt` files (`38ambushalley.txt`…, `00-singe1\actionmax` folder of the same repository) and the tape videos there. Keep the names and subfolders given in the `.txt` files: for example `video_actionmaxintro.m2v`, `video_menu.m2v` and `38ambushalley\video_38ambushalley.m2v`.
4. In the same folder, create one empty file per game: `38ambushalley.actionmax`, `bluethunder.actionmax`…

```
roms\
└─ actionmax\
   ├─ roms\
   │  └─ actionmax.zip
   └─ vldp\
      └─ actionmax\
         ├─ 38ambushalley.actionmax
         ├─ 38ambushalley.txt
         ├─ video_actionmaxintro.m2v
         ├─ video_menu.m2v
         └─ 38ambushalley\
            ├─ video_38ambushalley.m2v
            └─ video_38ambushalley.ogg
```

<div align="left"><figure><img src="../../../.gitbook/assets/image (669).png" alt=""><figcaption></figcaption></figure></div>

### Install the folder games (old Hypseus method)

1. Create the `roms\actionmax\actionmax.hypseus` folder.
2. Copy into it the content of the `00-singe1\actionmax` folder of the `hypseus_singe_data` repository (`.singe` scripts, `.txt` files, sounds, images, fonts) and the tape videos, with the same subfolders.
3. In `roms\actionmax`, create one empty file per game: `38ambushalley.actionmax`, `bluethunder.actionmax`…

RetroBat then starts the `<game>.singe` script of the `actionmax.hypseus` folder.

### Install the games for Singe2

1. Download the ActionMax version of Singe 2 from the emulator website (kangaroopunch.com).
2. Copy the `ActionMax` folder to `roms\actionmax` (the name `ActionMax.singe` is also accepted). It holds the scripts (`38AmbushAlley.singe`…) and the videos (`video_38AmbushAlley.mkv`…).
3. In `roms\actionmax`, create one empty file per game: `38ambushalley.actionmax`, `bluethunder.actionmax`…
4. Select the **singe2** emulator for the system or for the game.

Singe2 needs Windows **developer mode** to be enabled (Windows Settings): RetroBat creates a link to the `ActionMax` folder in `emulators\singe2`.

The `.actionmax` files in `roms\actionmax` are also used by the old Hypseus method: if both the `actionmax.hypseus` and `ActionMax` folders are present, each game can start with both emulators.

## Known issues

| Problem                                    | Solution                                                                                                                                                                                                                              |
| ------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| "Unable to find singe file for actionmax"  | With the old method, the `roms\actionmax\actionmax.hypseus` folder or the `<game>.singe` file is missing. With the zip method, the `.actionmax` file must be in `roms\actionmax\vldp\actionmax` and the zip in `roms\actionmax\roms`. |
| "Framefile (.txt) does not exist"          | Copy the `<game>.txt` file next to the `.actionmax` file, in `roms\actionmax\vldp\actionmax`.                                                                                                                                         |
| Black screen or missing video              | A video is missing or not in the subfolder given by the `.txt` file.                                                                                                                                                                  |
| "ActionMax rom folder not found" (Singe2)  | The `roms\actionmax\ActionMax` folder is missing.                                                                                                                                                                                     |
| Singe2 does not start, symbolic link error | Enable developer mode in Windows Settings.                                                                                                                                                                                            |
| The game does not react to shots           | Aim with the mouse or a configured light gun (see [**Light guns**](actionmax.md#light-guns)).                                                                                                                                         |
| The crosshair is in the way                | Disable **SHOW CROSSHAIR**.                                                                                                                                                                                                           |
