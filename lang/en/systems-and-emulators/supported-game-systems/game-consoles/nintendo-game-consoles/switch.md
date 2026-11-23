---
description: Nintendo
---

# Switch

<div align="left"><figure><img src="../../../../.gitbook/assets/image (680).png" alt="" width="420"><figcaption></figcaption></figure></div>

## Overview

The **Nintendo Switch** is a hybrid console released in March 2017: it plugs into the TV or is carried as a handheld. Its detachable controllers, the **Joy-Con**, are used together or separately, and the **Pro Controller** offers a classic controller. With more than 150 million units, it is one of the best-selling consoles in history.

Among its landmark games: The Legend of Zelda: Breath of the Wild and Tears of the Kingdom, Super Mario Odyssey, Mario Kart 8 Deluxe, Animal Crossing: New Horizons, Super Smash Bros. Ultimate or Splatoon.

RetroBat supports **Eden** (default), **Ryujinx**, **Citron**, **Sudachi** and **Yuzu**. These emulators are not provided with RetroBat: they must be installed manually (see [**Installing the emulators**](switch.md#installing-the-emulators)).

{% embed url="https://en.wikipedia.org/wiki/Nintendo_Switch" %}

## At a glance

<table><thead><tr><th width="200.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\switch</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nso .nro .nca .xci .nsp .kip .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>eden</td></tr><tr><td><strong>BIOS</strong></td><td><code>prod.keys</code> and firmware of your console, in the folder of each emulator</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No (Ryujinx: emulated local wireless multiplayer)</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

| Emulator           | Supported version                                                                     | Strengths                                                                                                                                        | Limitations                              |
| ------------------ | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------- |
| **eden** (default) | [eden-emu.dev](https://eden-emu.dev/)                                                 | Active successor of Yuzu: good performance, updates and DLC loaded from `roms\switchupdates` without installing, saves can go to `saves\switch`. |                                          |
| **ryujinx**        | Ryubing: [git.ryujinx.app/projects/Ryubing](https://git.ryujinx.app/projects/Ryubing) | Separate emulator, written from scratch. Emulated local wireless multiplayer (**NETWORK > MULTIPLAYER MODE**).                                   | Updates and DLC to add in Ryujinx.       |
| **citron**         | Citron-Neo: [github.com/citron-neo/emulator](https://github.com/citron-neo/emulator)  | Another Yuzu successor. Updates and DLC from `roms\switchupdates`, saves can go to `saves\switch`.                                               |                                          |
| **sudachi**        |                                                                                       | Yuzu successor.                                                                                                                                  | Updates and DLC to install in the NAND.  |
| **yuzu**           | Last version                                                                          | Original emulator Eden, Citron and Sudachi come from.                                                                                            | Discontinued in 2024: no longer updated. |

## Installing the emulators

RetroBat does not provide the Switch emulators, nor the console files. For each emulator you use, you need to:

1. copy the emulator to its RetroBat folder;
2. add the keys of **your** console (`prod.keys`);
3. install the firmware of **your** console.

Without the keys and the firmware, games do not start.

### Ryujinx

1. Download the Windows version of Ryujinx (Ryubing) and extract the archive.
2. Copy **the content** of the extracted folder to `emulators\ryujinx`: `Ryujinx.exe` must be directly in `emulators\ryujinx`, not in a subfolder.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (681).png" alt=""><figcaption></figcaption></figure></div>

3. Check that the `Configure Ryujinx.bat` file is in `emulators\ryujinx`. If it is missing, copy it from `system\templates\ryujinx`.
4. Run `Configure Ryujinx.bat` (double-click). It opens Ryujinx with the RetroBat data folder, `saves\switch\ryujinx\portable`, and creates it if it does not exist. You can also open Ryujinx from the RetroBat emulators menu, which does the same.
5. Quit Ryujinx, put `prod.keys` (and `title.keys` if you have it) in `saves\switch\ryujinx\portable\system`, then run `Configure Ryujinx.bat` again.
6. Install the firmware: **Tools > Install Firmware**, then **Install a firmware from XCI or ZIP** (firmware archive) or **Install a firmware from a directory** (folder of `.nca` files).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (682).png" alt=""><figcaption><p>Tools > Install Firmware</p></figcaption></figure></div>

7. Quit Ryujinx. It is ready: launch the games from RetroBat.

{% hint style="danger" %}
This step is mandatory for Ryujinx to work properly with RetroBat.

Always open Ryujinx with `Configure Ryujinx.bat` or from the RetroBat emulators menu. When started directly from `Ryujinx.exe`, it stores its data in another folder: keys, firmware and settings set there are not seen by RetroBat.
{% endhint %}

### Eden, Citron, Sudachi, Yuzu

1. Download the Windows version of the emulator and extract the archive.
2. Copy **the content** of the extracted folder to `emulators\<emulator>` (`emulators\eden`, `emulators\citron`, `emulators\sudachi` or `emulators\yuzu`): the executable (`eden.exe`, `citron.exe`, `sudachi.exe`, `yuzu.exe`) must be directly in this folder.
3. Create the `user` subfolder in the emulator folder (for example `emulators\eden\user`). The emulator then stores all its data in this folder (portable mode). Without it, it stores them in `%APPDATA%`, where RetroBat does not find them. RetroBat creates it when a game is launched for the first time, but it must exist before the emulator is opened for the first time.
4. Put `prod.keys` (and `title.keys` if you have it) in `emulators\<emulator>\user\keys`.
5. Install the firmware:
   * either from the emulator: open it from the RetroBat emulators menu, then **Tools > Install Firmware**;
   * or by copying the firmware `.nca` files to `emulators\<emulator>\user\nand\system\Contents\registered`.
6. Quit the emulator: launch the games from RetroBat.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (683).png" alt=""><figcaption></figcaption></figure></div>

## BIOS

Summary of the files of **your** console to provide (see [**Installing the emulators**](switch.md#installing-the-emulators) for the full procedure):

<table data-header-hidden><thead><tr><th width="157">Emulator</th><th></th><th></th></tr></thead><tbody><tr><td>Emulator</td><td>Keys (<code>prod.keys</code>, <code>title.keys</code>)</td><td>Firmware</td></tr><tr><td>Eden, Citron, Sudachi, Yuzu</td><td><code>emulators\&#x3C;emulator>\user\keys</code></td><td><strong>Tools > Install Firmware</strong>, or <code>.nca</code> files in <code>emulators\&#x3C;emulator>\user\nand\system\Contents\registered</code></td></tr><tr><td>Ryujinx</td><td><code>saves\switch\ryujinx\portable\system</code></td><td><strong>Tools > Install Firmware</strong> (Ryujinx opened with <code>Configure Ryujinx.bat</code>)</td></tr></tbody></table>

The firmware must be the same version as the keys, or older. After a firmware update, also update `prod.keys`.

## Which game format?

<table><thead><tr><th width="226.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.xci</strong></td><td>Cartridge image.</td></tr><tr><td><strong>.nsp</strong></td><td>Downloaded game (eShop). Updates and DLC are <code>.nsp</code> files too.</td></tr><tr><td><strong>.nca</strong> / <strong>.nso</strong> / <strong>.nro</strong> / <strong>.kip</strong></td><td>System files or homebrew programs.</td></tr><tr><td><strong>.decomp</strong></td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

Updates and DLC are not games: do not put them in `roms\switch` (see [**Game updates and DLC**](switch.md#game-updates-and-dlc)).

## Controls

### Automatic configuration

RetroBat configures the controllers for all emulators, as **Pro Controller** by default. **CONTROLS > PLAYER 1 CONTROLLER TYPE** (to 4) selects another controller, depending on the emulator: DUAL JOYCON, LEFT JOYCON, RIGHT JOYCON, GAMECUBE, or HANDHELD (player 1, controllers attached to the console).

Buttons are placed as on a Nintendo controller (position, not letter):

<table><thead><tr><th width="254">RetroBat controller</th><th>Switch</th></tr></thead><tbody><tr><td>START</td><td>+</td></tr><tr><td>SELECT</td><td>−</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>Left stick / right stick</td><td>Left stick / right stick</td></tr><tr><td>SOUTH</td><td>B (or A when inverted)</td></tr><tr><td>EAST</td><td>A (or B when inverted)</td></tr><tr><td>WEST</td><td>Y (or X when inverted)</td></tr><tr><td>NORTH</td><td>X (or Y when inverted)</td></tr><tr><td>L1 / R1</td><td>L / R</td></tr><tr><td>L2 / R2</td><td>ZL / ZR</td></tr><tr><td>L3 / R3</td><td>Left / right stick click</td></tr></tbody></table>

The **CONTROLS > INVERT FACE BUTTONS** option inverts the buttons (A on SOUTH, following the printed letters, to match Xbox controllers). With Ryujinx, Nintendo controllers are inverted automatically.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (684).png" alt=""><figcaption></figcaption></figure></div>

Other useful options:

* **EMULATION > USE UNDOCKED MODE** runs the console in handheld mode (lower resolution, faster) instead of TV mode.
* **CONTROLS > DISABLE CONTROLLER APPLET** avoids the controller selection window some games open at startup (enabled by default with Eden).
* **CONTROLS > ENABLE MOTION** (Eden) / **MOTION CONTROL** (Ryujinx) uses the gyroscope of controllers that have one.

### Hotkeys

| Hotkey         | Eden, Sudachi, Yuzu | Ryujinx    | Citron |
| -------------- | ------------------- | ---------- | ------ |
| HOTKEY + START | Quit                | Quit       | Quit   |
| HOTKEY + SOUTH | Pause               | Pause      | —      |
| HOTKEY + R3    | Screenshot          | Screenshot | —      |
| HOTKEY + L3    | Fullscreen          | —          | —      |

With Eden, Sudachi and Yuzu, these are emulator hotkeys set by RetroBat, with SELECT as the HOTKEY button. No emulator has save states: save in the game. See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="274">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\switch</code></td></tr><tr><td>Updates and DLC (Eden, Citron)</td><td><code>roms\switchupdates</code></td></tr><tr><td>Emulator user content</td><td><strong>Ryujinx</strong>: <code>saves\switch\ryujinx\portable</code><br><strong>Eden, Citron, Sudachi, Yuzu</strong>: <code>emulators\&#x3C;emulator>\user</code></td></tr><tr><td>Config file</td><td><strong>Ryujinx</strong>: <code>saves\switch\ryujinx\portable\Config.json</code><br><strong>Eden, Citron, Sudachi, Yuzu</strong>: <code>emulators\&#x3C;emulator>\user\config\qt-config.ini</code></td></tr><tr><td>Saves (Eden, Citron, with the option below)</td><td><code>saves\switch</code></td></tr><tr><td>Screenshots (Eden)</td><td><code>screenshots\eden</code></td></tr></tbody></table>

If `saves\switch\ryujinx\portable` does not exist, Ryujinx uses `emulators\ryujinx\portable`.

For Eden and Citron, saves can go to the RetroBat `saves\switch` folder instead of the emulator folder (by default they stay in the emulator folder). Switch on the **SAVES IN RETROBAT SAVES FOLDER** option, in **MAIN MENU > GAME SETTINGS** (**SWITCH** section):

## Game updates and DLC

All emulators handle game updates and DLC. They are `.nsp` files, dumped from your console.

### Eden and Citron: roms\switchupdates folder

Eden and Citron load updates and DLC from a folder, without installing them. RetroBat adds the `roms\switchupdates` folder to them: put the `.nsp` files there.

### Eden, Citron, Sudachi, Yuzu: install to the NAND

1. Open the emulator from the RetroBat emulators menu.
2. Select **File > Install Files to NAND...**

<div align="left"><figure><img src="../../../../.gitbook/assets/image (685).png" alt=""><figcaption></figcaption></figure></div>

3. Select the `.nsp` file of the update or DLC and confirm.

### Ryujinx

1. Open Ryujinx with `Configure Ryujinx.bat` or from the RetroBat emulators menu.
2. In the Ryujinx game list, right-click the game and select **Manage Title Updates** or **Manage DLC**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (686).png" alt=""><figcaption></figcaption></figure></div>

3. Add the `.nsp` file, select it and save.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (687).png" alt=""><figcaption></figcaption></figure></div>

## Known issues

| Issue                                                  | Solution                                                                                                                       |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| The emulator asks for keys or shows an error at launch | `prod.keys` is missing or does not match the firmware: see [**Installing the emulators**](switch.md#installing-the-emulators). |
| Ryujinx does not find the installed keys or firmware   | They were installed with Ryujinx started directly: do it again with `Configure Ryujinx.bat`.                                   |
| Eden (or Citron, Sudachi, Yuzu) does not find the keys | The `user` folder was missing when the emulator was first opened: create it, then put the keys and firmware back in `user`.    |
| A game shows a controller selection window             | Enable **CONTROLS > DISABLE CONTROLLER APPLET**.                                                                               |
| Stutter on the first play                              | The emulator compiles its shaders: it decreases afterwards (shader cache).                                                     |
| A game update is not taken into account                | It is in `roms\switch`: move it to `roms\switchupdates` (Eden, Citron) or install it in the emulator.                          |
