---
description: Sony
---

# Playstation 3

<div align="left"><figure><img src="../../../../.gitbook/assets/image (497).png" alt="" width="500"><figcaption></figcaption></figure></div>

## Presentation

The **PlayStation 3** was released in late 2006 in Japan and the United States, then in March 2007 in Europe. Sony bet on a very powerful in-house processor, the **Cell**, and on the **Blu-ray** drive, which also made it a high-definition movie player.

The console launched the PlayStation Network, trophies and downloadable games. It stayed in production until 2017 and sold more than 87 million units. Series such as Uncharted, The Last of Us, Demon's Souls and LittleBigPlanet were born on it.

Its very unusual architecture makes it a hard machine to emulate. **RPCS3**, started in 2011, now runs the vast majority of the library, provided you have a powerful PC.

{% embed url="https://en.wikipedia.org/wiki/PlayStation_3" %}

## At a glance

<table><thead><tr><th width="241.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\ps3</code></td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .lnk .ps3 .iso .psn .7z .zip .rar .squashfs .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>rpcs3</td></tr><tr><td><strong>BIOS</strong></td><td>PS3 firmware <code>PS3UPDAT.PUP</code> in <code>bios</code> (installed at first launch)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>RPCS3</td></tr></tbody></table>

## Which emulator to choose?

RPCS3 is the only PS3 emulator in RetroBat.

<table><thead><tr><th width="145.75">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>rpcs3</strong> (default)</td><td>Very high compatibility, increased resolution, trophies, many controllers recognized.</td><td>Needs a powerful processor. The first launch of each game is long (compilation).</td></tr></tbody></table>

The RPCS3 compatibility list ([rpcs3.net](https://rpcs3.net/compatibility)) gives the status of each game.

## BIOS

The PS3 has no BIOS as such, but RPCS3 needs the console **firmware**.

<table><thead><tr><th width="211.5">File</th><th>Location</th></tr></thead><tbody><tr><td><code>PS3UPDAT.PUP</code></td><td><code>bios</code></td></tr></tbody></table>

The firmware is a free download from the PlayStation website (PS3 system software update).

**Automatic installation**: at the first launch of a game, if the firmware is not installed yet, RetroBat opens RPCS3 to install it from `bios\PS3UPDAT.PUP`. When the installation is done, launch the game again.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (498).png" alt=""><figcaption></figcaption></figure></div>

If the firmware is neither installed nor present in `bios`, RetroBat shows an error message and the game does not start.

## Which game format?

<table><thead><tr><th width="128.25">Format</th><th width="205.25">For what?</th><th>Notes</th></tr></thead><tbody><tr><td><strong><code>.ps3</code> folder</strong></td><td>Disc game</td><td>The game copied as a folder, renamed with <code>.ps3</code> at the end: <code>roms\ps3\My game.ps3\PS3_GAME\USRDIR\EBOOT.BIN</code>.</td></tr><tr><td><strong>.iso</strong></td><td>Disc game</td><td>Disc image, read directly by RPCS3.</td></tr><tr><td><strong>.psn</strong></td><td>PSN game</td><td>Text file holding the ID of a game installed in RPCS3 (see <a href="playstation-3.md#add-a-psn-game">Guides</a>).</td></tr><tr><td>.m3u</td><td>PSN game or game stored elsewhere</td><td>Text file whose first line tells where the game is (see <a href="playstation-3.md#use-an-.m3u-file">Guides</a>).</td></tr><tr><td>.squashfs</td><td>Disc or PSN game</td><td>Compressed image, mounted without extraction.</td></tr><tr><td>.7z .zip .rar</td><td>Disc game</td><td>Extracted before launch: slow for big games.</td></tr><tr><td>.lnk</td><td>Windows shortcut</td><td>Launched as is.</td></tr><tr><td>.decomp</td><td>PC port</td><td>See the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

PSN games (`.pkg` files) must first be installed in RPCS3.

## Controls

### Automatic configuration

RetroBat configures controllers automatically, up to 7 players. Buttons are placed as on the PS3 controller: **SOUTH** = Cross, **EAST** = Circle, **WEST** = Square, **NORTH** = Triangle.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (499).png" alt="" width="338"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="284">Controller</th><th>Driver used in RPCS3</th></tr></thead><tbody><tr><td>DualSense (PS5)</td><td>DualSense</td></tr><tr><td>DualShock 4 (PS4)</td><td>DualShock 4</td></tr><tr><td>DualShock 3 (PS3)</td><td>DualShock 3</td></tr><tr><td>XInput controllers (Xbox)</td><td>XInput</td></tr><tr><td>Other controllers</td><td>SDL</td></tr></tbody></table>

Useful options, in **CONTROLS**:

<table><thead><tr><th width="350.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>ENABLE RUMBLE</strong></td><td>Rumble is off by default.</td></tr><tr><td><strong>CONFIRM BUTTON</strong></td><td>Cross or Circle to confirm in system dialogs. On AUTO, follows the selected region.</td></tr><tr><td><strong>INVERT FACE BUTTONS</strong></td><td>Swaps the face buttons.</td></tr><tr><td><strong>PS MOVE HANDLER</strong>, <strong>CAMERA TYPE</strong></td><td>For PlayStation Move and camera games.</td></tr><tr><td><strong>BUZZ! BUZZERS</strong>, <strong>DJ HERO TURNTABLE</strong>, <strong>GUITAR HERO LIVE GUITAR</strong></td><td>Emulates these accessories with your controllers.</td></tr></tbody></table>

**Pressure-sensitive buttons**: the PS3 controller measures how hard its buttons are pressed, which some games use (Gran Turismo for example). RPCS3 only handles it with a genuine DualShock 3 or Sixaxis and the DsHidMini driver (see the [RPCS3 wiki, "Controller Configuration"](https://wiki.rpcs3.net/index.php?title=Help:Controller_Configuration)).

### Light guns

The **GUNS > ENABLE GUN** option offers two modes:

<table><thead><tr><th width="175.25">Mode</th><th>Use</th></tr></thead><tbody><tr><td><strong>RAW MOUSE</strong></td><td>GunCon 3 games (Time Crisis 4…). Up to 2 guns, plugged by default into ports 3 and 4 of the console. The <strong>USE PORT 1 FOR GUNCON</strong> option puts them on ports 1 and 2.</td></tr><tr><td><strong>PS EYE</strong></td><td>PlayStation Move games: the gun replaces the Move controller.</td></tr></tbody></table>

The Sinden software is started automatically when a Sinden gun is connected.

To connect and set up a light gun in RetroBat, see the [**Lightguns**](../../../../controllers/supported-controllers/lightguns/) page.

### Hotkeys

| Hotkey                               | Action                                     | Keyboard |
| ------------------------------------ | ------------------------------------------ | -------- |
| **HOTKEY + START**                   | Quit                                       | ESC      |
| HOTKEY + L3                          | Pause                                      | P        |
| HOTKEY + R3                          | Screenshot                                 | F8       |
| SELECT + SOUTH, or PS / Guide button | PS button (RPCS3 Home menu)                | F1       |
| —                                    | Fullscreen                                 | F        |
| —                                    | Mute                                       | M        |
| —                                    | RPCS3 save state (not managed by RetroBat) | F2       |

## Folders

<table><thead><tr><th width="250.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Firmware to install</td><td><code>bios\PS3UPDAT.PUP</code></td></tr><tr><td>PS3 hard disk: PSN games, saves, trophies</td><td><code>saves\ps3\rpcs3\dev_hdd0</code></td></tr><tr><td>Installed PSN games</td><td><code>saves\ps3\rpcs3\dev_hdd0\game</code></td></tr><tr><td>Game saves</td><td><code>saves\ps3\rpcs3\dev_hdd0\home\00000001\savedata</code></td></tr><tr><td>Trophies</td><td><code>saves\ps3\rpcs3\dev_hdd0\home\00000001\trophy</code></td></tr><tr><td>Installed firmware</td><td><code>emulators\rpcs3\dev_flash</code></td></tr><tr><td>RPCS3 configuration</td><td><code>emulators\rpcs3\config\config.yml</code></td></tr><tr><td>RPCS3 per-game configurations</td><td><code>emulators\rpcs3\config\custom_configs</code></td></tr><tr><td>Controller configuration</td><td><code>emulators\rpcs3\config\input_configs\global\Retrobat.yml</code></td></tr><tr><td>Interface settings</td><td><code>emulators\rpcs3\GuiConfigs\CurrentSettings.ini</code></td></tr><tr><td>Game patches</td><td><code>emulators\rpcs3\patches</code></td></tr><tr><td>Game compilation cache</td><td><code>emulators\rpcs3\cache</code></td></tr><tr><td>Screenshots</td><td><code>emulators\rpcs3\screenshots</code></td></tr></tbody></table>

If the `saves\ps3\rpcs3` folder does not exist, RetroBat uses the `dev_hdd0` folder of the emulator (`emulators\rpcs3\dev_hdd0`).

## Guides

### Add a disc game

1. Copy the game folder to `roms\ps3`. It contains a `PS3_GAME` folder.
2. Rename it by adding `.ps3` at the end, for example `My game.ps3`.
3. Update the RetroBat game list.

An `.iso` image goes as is in `roms\ps3`.

### Add a PSN game

1. Run `rpcs3.exe` from the `emulators\rpcs3` folder.
2. In the **File** menu, choose **Install Packages/Raps/Edats** and select the `.pkg` file of the game (and its `.rap` file if it has one).
3. The game appears in the RPCS3 list. Note its ID, in the **Serial** column (for example `NPEB00623`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (500).png" alt=""><figcaption></figcaption></figure></div>

1. In `roms\ps3`, create a text file named after the game with the `.psn` extension, for example `My game.psn`.
2. Write only the ID in it:

```
NPEB00623
```

### Use an .m3u file

An `.m3u` file is a text file whose first line tells which game to launch. It can hold:

<table><thead><tr><th width="426.5">First line</th><th>Game launched</th></tr></thead><tbody><tr><td><code>GAMEID:NPEB01234</code></td><td>The installed game with this ID</td></tr><tr><td><code>\dev_hdd0\game\NPEB01234\USRDIR\EBOOT.BIN</code></td><td>Path searched in <code>roms\ps3</code>, then <code>saves\ps3\rpcs3</code>, then <code>emulators\rpcs3</code></td></tr><tr><td><code>ROMPATH\My game\PS3_GAME\USRDIR\EBOOT.BIN</code></td><td>Path from <code>roms\ps3</code></td></tr><tr><td><code>SAVESPATH\dev_hdd0\game\NPEB01234\USRDIR\EBOOT.BIN</code></td><td>Path from <code>saves\ps3\rpcs3</code></td></tr><tr><td><code>EMULATORPATH\dev_hdd0\game\NPEB01234\USRDIR\EBOOT.BIN</code></td><td>Path from <code>emulators\rpcs3</code></td></tr><tr><td><code>D:\Games\My game\PS3_GAME\USRDIR\EBOOT.BIN</code></td><td>Full path</td></tr></tbody></table>

The `example-to-edit.m3u.txt` file in the `roms\ps3` folder is a template. The **BatGui** tool can create these files for games already installed (M3U Creator menu): see the [**BatGui**](../../../../advanced-features/batgui.md) page.

### Keep your per-game settings made in RPCS3

By default, RetroBat applies the options set in its menu and ignores per-game configurations created in RPCS3. The **EMULATION > CONFIG TO USE** option changes this behavior:

<table><thead><tr><th width="219">Choice</th><th>Effect</th></tr></thead><tbody><tr><td><strong>DEFAULT</strong></td><td>RetroBat options, RPCS3 per-game configurations ignored.</td></tr><tr><td><strong>GAME OVERRIDE</strong></td><td>The RPCS3 per-game configuration is used when it exists.</td></tr><tr><td><strong>ONLY CONFIG YML</strong></td><td>Only the <code>config.yml</code> file is used.</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (502).png" alt=""><figcaption></figcaption></figure></div>

### Install the firmware by hand

1. Run `rpcs3.exe` from the `emulators\rpcs3` folder.
2. In the **File** menu, choose **Install Firmware**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (501).png" alt=""><figcaption></figcaption></figure></div>

3. Select the `PS3UPDAT.PUP` file.

## Known issues

| Issue                                                                     | Solution                                                                                                                     |
| ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| "PS3 firmware is not installed" message                                   | Put `PS3UPDAT.PUP` in `bios`, or install the firmware by hand (see [Guides](playstation-3.md#install-the-firmware-by-hand)). |
| At first launch, RPCS3 installs the firmware instead of starting the game | This is normal. Launch the game again once the installation is done.                                                         |
| The first launch of a game is very long                                   | RPCS3 compiles the game the first time. Later launches are fast.                                                             |
| No rumble                                                                 | Turn on **ENABLE RUMBLE**.                                                                                                   |
| Cross and Circle are swapped to confirm                                   | Set **CONFIRM BUTTON**.                                                                                                      |
| Xbox controller not recognized properly                                   | Turn on **DRIVERS > FORCE SDL DRIVER FOR GAMEPAD**.                                                                          |
| My per-game settings made in RPCS3 are ignored                            | Choose **CONFIG TO USE**: GAME OVERRIDE.                                                                                     |
| A `.psn` or `.m3u` game does not start                                    | Check the ID, and that the game is installed in `saves\ps3\rpcs3\dev_hdd0\game`.                                             |
