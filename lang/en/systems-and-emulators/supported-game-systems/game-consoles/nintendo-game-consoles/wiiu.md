---
description: Nintendo
---

# WiiU

<div align="left"><figure><img src="../../../../.gitbook/assets/image (688).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

The **Wii U** is Nintendo's home console that succeeded the Wii (2012-2017). Its distinctive feature is the **Wii U GamePad**, a controller with a touch screen used as a second screen or as the main screen. It remains compatible with Wiimotes and also accepts a classic controller, the **Wii U Pro Controller**.

Its sales (about 13.5 million consoles) were low, but many of its games remained famous: Mario Kart 8, Super Mario 3D World, Splatoon, The Legend of Zelda: Breath of the Wild or Xenoblade Chronicles X.

RetroBat uses **Cemu**, the reference Wii U emulator.

{% embed url="https://en.wikipedia.org/wiki/Wii_U" %}

## At a glance

<table><thead><tr><th width="231.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\wiiu</code></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .rpx .wud .wux .wua .m3u .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>cemu</td></tr><tr><td><strong>BIOS</strong></td><td>None (<code>keys.txt</code> for encrypted games)</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic (GamePad, Pro Controller, Wiimotes)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>keys.txt</code> in <code>bios\cemu</code></td></tr></tbody></table>

## BIOS

No BIOS is needed to play. However, **encrypted** games (`.wud`, `.wux` and disc `.iso` images) need the decryption keys of each game, in a `keys.txt` file. Without them, Cemu shows "Could not decrypt title".

<table><thead><tr><th width="139.5">File</th><th width="137.75">Folder</th><th>Required</th></tr></thead><tbody><tr><td><code>keys.txt</code></td><td><code>bios\cemu</code></td><td>No (encrypted games only)</td></tr></tbody></table>

RetroBat copies `bios\cemu\keys.txt` to the Cemu folder (`emulators\cemu\portable\keys.txt`) at each launch, when it is newer. You can also put it directly in `emulators\cemu\portable`.

The `keys.txt` file is dumped from your Wii U console: see the [Cemu guide](https://wiki.cemu.info/wiki/Obtaining_Keys_for_Keys.txt).

Games in `.wua` format and decrypted game folders (`.rpx`) do not need keys.

## Which game format?

| Format              | Description                                                                                                                                                                                                                                                            |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **.rpx**            | Decrypted game in "Loadiine" (or "Bootloader") format: a folder with the `code`, `content` and `meta` subfolders, as dumped from your console with the Dumpling tool. The `.rpx` file is in `code`. Recommended format (see [**Adding games**](wiiu.md#adding-games)). |
| **.wua**            | Cemu archive: game, update and DLC in a single file, not encrypted.                                                                                                                                                                                                    |
| **.wud** / **.wux** | Disc image (`.wux` = compressed). Encrypted: needs `keys.txt`.                                                                                                                                                                                                         |
| **.iso**            | Disc image. Encrypted: needs `keys.txt`.                                                                                                                                                                                                                               |
| **.m3u**            | Text file giving the path of the `.rpx` to launch (see [**Adding games**](wiiu.md#adding-games)).                                                                                                                                                                      |
| **.decomp**         | PC port, see the [**Recompilations**](../../others/recomp.md) page.                                                                                                                                                                                                    |

## Controls

### Automatic configuration

{% hint style="info" %}
RetroBat automatically configures for Cemu:

* XInput controllers;
* DualShock and DualSense controllers;
* the Nintendo Switch Pro controller.
{% endhint %}

Player 1 plays with an emulated Wii U **GamePad**, players 2 to 4 with a **Pro Controller**. **CONTROLS > PLAYER 1 CONTROLLER TYPE** (to 4) changes this choice: GAMEPAD, PRO CONTROLLER or HORIZONTAL WIIMOTE. Some multiplayer games reject the GamePad for player 1: switch it to Pro Controller.

Buttons are placed as on a Nintendo controller (position, not letter):

<table><thead><tr><th width="230.25">RetroBat controller</th><th>Wii U</th></tr></thead><tbody><tr><td>START</td><td>+</td></tr><tr><td>SELECT</td><td>−</td></tr><tr><td>D-pad</td><td>D-pad</td></tr><tr><td>Left stick / right stick</td><td>Left stick / right stick</td></tr><tr><td>SOUTH</td><td>B (or A when inverted)</td></tr><tr><td>EAST</td><td>A (or B when inverted)</td></tr><tr><td>WEST</td><td>Y (or X when inverted)</td></tr><tr><td>NORTH</td><td>X (or Y when inverted)</td></tr><tr><td>L1 / R1</td><td>L / R</td></tr><tr><td>L2 / R2</td><td>ZL / ZR</td></tr><tr><td>L3 / R3</td><td>Left / right stick click</td></tr></tbody></table>

The **CONTROLS > INVERT FACE BUTTONS** option inverts the buttons (A on SOUTH, following the printed letters):

<div align="left"><figure><img src="../../../../.gitbook/assets/image (705).png" alt=""><figcaption></figcaption></figure></div>

### Playing with Wiimotes

Cemu allows playing with real Wiimotes connected to the PC (DolphinBar or Bluetooth).

Select the number of Wiimotes in **CONTROLS > REAL WIIMOTES** (advanced system or game options). Other controllers are then no longer used.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (704).png" alt=""><figcaption></figcaption></figure></div>

**CONTROLS > WIIMOTE 1 TYPE** (to 4) gives, for each player, the connected Wiimote: MOTION PLUS, MOTION PLUS + NUNCHUK, STANDARD or STANDARD + NUNCHUK.

### Motion controls

Some games require the controller gyroscope to progress (for example some shrines of Zelda: Breath of the Wild).

Enable **CONTROLS > MOTION CONTROL** in the advanced system or game options. Tested controllers: Switch Pro, 8BitDo (in Switch / Pro Controller mode) and DualSense.

The [Cemu wiki](https://wiki.cemu.info/wiki/Motion_controls) covers the other solutions.

### Microphone

Games that ask you to blow into the GamePad microphone:

* **CONTROLS > MAP BUTTON TO MICROPHONE BLOW** maps a button to the microphone (L3 or R3);
* **AUDIO > ENABLE COMPUTER MICROPHONE** uses the PC microphone.

{% hint style="info" %}
The microphone button only works with the Wii U GamePad as emulated controller.
{% endhint %}

### Show the GamePad screen

The GamePad has its own screen. Two ways to show it:

* **CONTROLS > DISPLAY GAMEPAD SCREEN** selects a button (L3, R3 or SELECT) that shows the GamePad screen instead of the main screen, as long as it is held. With **CONTROLS > GAMEPAD SCREEN TOGGLE**, each press switches between the screens.
* **USER INTERFACE > SEPARATE GAMEPAD VIEW** opens the GamePad screen in a second window (handy with two displays).

{% hint style="info" %}
The screen button only works with the Wii U GamePad as emulated controller.
{% endhint %}

### Hotkeys

HOTKEY + START quits the game. Cemu has no save states: save in the game. See the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="321.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\wiiu</code></td></tr><tr><td>mlc01 (saves, installed games, updates and DLC)</td><td><code>saves\wiiu\cemu\mlc01</code></td></tr><tr><td>Keys of encrypted games</td><td><code>bios\cemu\keys.txt</code> (copied to <code>emulators\cemu\portable</code>)</td></tr><tr><td>Config file</td><td><code>emulators\cemu\portable\settings.xml</code></td></tr><tr><td>Controller config</td><td><code>emulators\cemu\portable\controllerProfiles</code> (one <code>.xml</code> file per controller)</td></tr><tr><td>Graphic packs</td><td><code>emulators\cemu\portable\graphicPacks</code></td></tr></tbody></table>

## Adding games

The recommended format is the **Loadiine** (or "Bootloader") format: this is the format of games dumped from your Wii U console with Dumpling. The game is a folder with 3 subfolders, `code`, `content` and `meta`. For example:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (703).png" alt=""><figcaption><p>Example of dumped Zelda game</p></figcaption></figure></div>

There are two ways to add these games to RetroBat.

### Method 1: install the game in Cemu and use a .m3u file

This method simulates the installation of the game in the Wii U memory, as for a game bought in digital version. The original game folder is no longer needed after the installation.

1. Open Cemu from the RetroBat emulators menu (or directly `emulators\cemu\Cemu.exe`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (702).png" alt=""><figcaption></figcaption></figure></div>

2. Select **File > Install game title, update or DLC**, go to the `meta` folder of the game and select the `meta.xml` file.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (701).png" alt=""><figcaption></figcaption></figure></div>

3. Wait for the installation to finish: the game appears in the Cemu list.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (700).png" alt=""><figcaption></figcaption></figure></div>

4. Right-click on the game and select **Game directory**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (699).png" alt=""><figcaption></figcaption></figure></div>

5. Windows Explorer opens the game folder, which contains the `.rpx` file (in `code`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (698).png" alt=""><figcaption></figcaption></figure></div>

6. Quit Cemu. In `roms\wiiu`, create a `<game name>.m3u` text file containing the path of the `.rpx`:

`\..\..\saves\wiiu\cemu\mlc01\usr\title\`<mark style="color:red;">`<path to the game>`</mark>`\code\`<mark style="color:red;">`<file name>`</mark>`.rpx`

For example for Zelda: Breath of the Wild:

The path can also be absolute (`C:\...`), or relative to the folder of the `.m3u` file. The `example-to-edit.m3u.txt` file of the `roms\wiiu` folder is a template.

7. Save the `.m3u` file: the game is available in RetroBat, ready to be scraped and played.

### Method 2: place the game folder in roms\wiiu

This method simulates the presence of the disc in the console.

Copy the game folder (Loadiine format) to `roms\wiiu`:

RetroBat finds the **.rpx** file of the `code` folder: the game is available in RetroBat, ready to be scraped and played.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (697).png" alt=""><figcaption></figcaption></figure></div>

ScreenScraper recognizes the file name: for example, `U-King` is Zelda: Breath of the Wild.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (696).png" alt=""><figcaption></figcaption></figure></div>

### Other formats

`.wua`, `.wud`, `.wux` and `.iso` files go directly in `roms\wiiu`. For `.wud`, `.wux` and `.iso`, add the game keys to `bios\cemu\keys.txt` (see **BIOS**).

## Game updates and DLC

Updates and DLC are installed in Cemu with the **Install game title, update or DLC** option. They come in the same format as games: Loadiine folders. With the `.wua` format, they are already in the game file.

1. Open Cemu from the RetroBat emulators menu and select **Install game title, update or DLC**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (695).png" alt=""><figcaption><p>Select the install option</p></figcaption></figure></div>

2. Go to the `meta` folder of the update or DLC and select the `meta.xml` file.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (694).png" alt=""><figcaption><p>search for the meta.xml file in the meta folder</p></figcaption></figure></div>

3. Wait until the installation finishes.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (693).png" alt=""><figcaption></figcaption></figure></div>

4. Cemu shows the version and DLC level in the **Version** and **DLC** columns.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (692).png" alt=""><figcaption></figcaption></figure></div>

Everything is installed in `saves\wiiu\cemu\mlc01`.

## Graphic packs

Cemu graphic packs enhance rendering (resolution, 60 frames per second) and also fix bugs in some games.

RetroBat does not manage them: enable them in Cemu. They are then applied each time the game is launched from RetroBat.

1. Open Cemu and select **Options > Graphic packs**:

<div align="left"><figure><img src="../../../../.gitbook/assets/image (691).png" alt=""><figcaption></figcaption></figure></div>

2. Click **Download latest community graphic packs** (bottom of the window) and wait for the download to finish.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (690).png" alt=""><figcaption></figcaption></figure></div>

3. Check the packs available for your game and enable the ones you need.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (689).png" alt=""><figcaption></figcaption></figure></div>

In this example, the "Title Screen Crash Fix" pack is mandatory to avoid a crash after the title screen of New Super Mario Bros. U.

4. Quit Cemu: the pack settings are saved automatically.

{% hint style="info" %}
The Cemu compatibility page gives, for each game, the useful settings and packs:

[https://compat.cemu.info/](https://compat.cemu.info/)
{% endhint %}

## Known issues

| Issue                                          | Solution                                                                                                         |
| ---------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| "Could not decrypt title"                      | The game is encrypted: add its keys to `bios\cemu\keys.txt`, or use the Loadiine or `.wua` format.               |
| A multiplayer game does not recognize player 1 | Set **CONTROLS > PLAYER 1 CONTROLLER TYPE** to PRO CONTROLLER.                                                   |
| Game profiles created in Cemu are not applied  | Expected: RetroBat disables them during the game to apply its own options. Set the game in the RetroBat options. |
| A game crashes or displays badly               | Check [compat.cemu.info](https://compat.cemu.info/): many games need a graphic pack (see **Graphic packs**).     |
| Stutter on the first play                      | Cemu compiles its shaders. With Vulkan, **VISUAL RENDERING > ASYNCHRONOUS TEXTURE COMPILATION** reduces it.      |
