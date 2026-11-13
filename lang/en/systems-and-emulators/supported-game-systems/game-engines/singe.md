# Singe

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/fb69ee3e5daf0db1c90d85d4a743edf1cc8a1843/art/logos/singe.svg" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

**Singe** (Somewhat Interactive Nostalgic Game Engine) is a game engine created by Scott Duensing as an addition to the Daphne emulator. It runs filmed video games that don't rely on an arcade board ROM: the game logic is described by a script, which drives the video.

Singe first made it possible to replay the shooting games from **American Laser Games**, which reached arcades in 1990 with Mad Dog McCree, followed by Who Shot Johnny Rock?, Crime Patrol and Space Pirates. It also runs Time Gal, Ninja Hayate and many games adapted by enthusiasts.

In RetroBat, these games run with **Hypseus Singe**, which plays Singe and Singe 2 games, or with **Singe2**.

Classic LaserDisc cabinets (Dragon's Lair, Space Ace…) are on the [**LaserDisc**](../arcade/daphne-laserdisc.md) page.

## At a glance

<table><thead><tr><th width="230.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\singe</code></td></tr><tr><td><strong>Extensions</strong></td><td>.hypseus .zip</td></tr><tr><td><strong>Default emulator</strong></td><td>hypseus</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators (player 1)</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>Hypseus, Singe2</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="114">Emulator</th><th width="174">For whom?</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>hypseus</strong> (default)</td><td>Everyone</td><td>Runs games in zip format and in folder format. Controller configured automatically, several light guns, decorations.</td><td>—</td></tr><tr><td><strong>singe2</strong></td><td>Games offered on the Singe 2 website</td><td>The emulator from the author of Singe.</td><td>Only runs the games from its website, in their own format. Requires Windows developer mode.</td></tr></tbody></table>

**When in doubt, keep hypseus.**

## BIOS

No BIOS is needed.

RetroBat provides the `Framework.zip` and `FrameworkKimmy.zip` files in `roms\singe`. They are used by Singe 2 games: don't delete them.

## Which game format?

<table><thead><tr><th width="155.25">Format</th><th width="87.5">hypseus</th><th width="79.5">singe2</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.zip</strong></td><td>✔</td><td>✘</td><td>Easiest method: the game in <code>roms\singe\roms</code>, the videos in <code>roms\singe\vldp</code>.</td></tr><tr><td>.hypseus folder</td><td>✔</td><td>✔</td><td>Older method for Hypseus. Only format for Singe2, with the games from its website.</td></tr></tbody></table>

In both cases, you have to provide the video (`.m2v`) and audio (`.ogg`) files of the game.

## Controls

### Automatic configuration

RetroBat automatically configures the player 1 controller for both emulators.

**Hypseus**

<table><thead><tr><th width="170.75">Action</th><th width="211.75">RetroBat controller</th><th>Keyboard</th></tr></thead><tbody><tr><td>Directions</td><td>D-pad / left stick</td><td>Arrow keys</td></tr><tr><td>Button 1</td><td>SOUTH</td><td>Left CTRL</td></tr><tr><td>Button 2</td><td>EAST</td><td>Left ALT</td></tr><tr><td>Button 3</td><td>R1</td><td>SPACE</td></tr><tr><td>Skill 1</td><td>WEST</td><td>Left SHIFT</td></tr><tr><td>Skill 2</td><td>NORTH</td><td>Z</td></tr><tr><td>Skill 3</td><td>L1</td><td>X</td></tr><tr><td>Coin player 1</td><td>SELECT</td><td>5</td></tr><tr><td>Start player 1</td><td>START</td><td>1</td></tr><tr><td>Coin player 2</td><td>—</td><td>6</td></tr><tr><td>Start player 2</td><td>—</td><td>2</td></tr><tr><td>Service</td><td>L3</td><td>9</td></tr><tr><td>Test</td><td>R3</td><td>0</td></tr><tr><td>Pause</td><td>—</td><td>P</td></tr><tr><td>Screenshot</td><td>—</td><td>F12</td></tr></tbody></table>

**Singe2**

<table><thead><tr><th width="194.5">Action</th><th width="209.75">RetroBat controller</th><th>Keyboard</th></tr></thead><tbody><tr><td>Directions</td><td>D-pad / sticks</td><td>Arrow keys</td></tr><tr><td>Action 1</td><td>SOUTH</td><td>SPACE or Left CTRL</td></tr><tr><td>Action 2</td><td>EAST</td><td>Left ALT</td></tr><tr><td>Action 3</td><td>WEST</td><td>Left SHIFT</td></tr><tr><td>Action 4</td><td>NORTH</td><td>Right SHIFT</td></tr><tr><td>Coin player 1</td><td>SELECT</td><td>5</td></tr><tr><td>Start player 1</td><td>START</td><td>1</td></tr><tr><td>Coin player 2</td><td>—</td><td>6</td></tr><tr><td>Start player 2</td><td>—</td><td>2</td></tr><tr><td>Pause</td><td>—</td><td>P</td></tr></tbody></table>

To configure the keys yourself, turn off **AUTOCONFIGURE CONTROLLERS**.

### Light guns

Shooting games are played with the mouse or a light gun. To connect and set up a light gun in RetroBat, see the [**Lightguns**](../../../controllers/supported-controllers/lightguns/) page.

* **Hypseus**: several light guns are detected automatically. The **GUNS > USE ONE GUN ONLY** option keeps a single one. With a Sinden light gun, RetroBat starts the Sinden software and displays the white border.
* **Wiimotes on a DolphinBar** (Hypseus): the D-pad sends coin (left) and start (right). For a second Wiimote: coin on down, start on up.
* **Singe2**: one light gun only. The **GUNS > FORCE INDEX** option picks which mouse is used. Left click is the Action 3 button, right click Action 1 and middle click Action 2.

The **SHOW CROSSHAIR** option shows or hides the crosshair.

### Hotkeys

<table><thead><tr><th width="271.5">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr><tr><td>ESC</td><td>Quit (keyboard)</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="272.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games in zip format</td><td><code>roms\singe\roms</code></td></tr><tr><td>Videos of zip games</td><td><code>roms\singe\vldp\&#x3C;game></code></td></tr><tr><td>Games in folder format</td><td><code>roms\singe\&#x3C;game>.hypseus</code></td></tr><tr><td>Framework files</td><td><code>roms\singe</code></td></tr><tr><td>Hypseus keys</td><td><code>emulators\hypseus\hypinput.ini</code></td></tr><tr><td>Hypseus decorations</td><td><code>emulators\hypseus\bezels</code></td></tr><tr><td>Hypseus screenshots (F12)</td><td><code>emulators\hypseus\screenshots</code></td></tr><tr><td>Singe2 keys</td><td><code>emulators\singe2\Singe\controls.cfg</code> (copied to the game folder)</td></tr></tbody></table>

The order in which RetroBat picks the Hypseus decoration is described on the [**LaserDisc**](../arcade/daphne-laserdisc.md#decorations-with-hypseus) page.

## Guides

### Adding a game in zip format (Hypseus)

This is the easiest method, but not all games are available as zip yet.

1. Get the game zip file from the `00-zip-roms` folder of the Hypseus `hypseus_singe_data` repository on GitHub: [https://github.com/DirtBagXon/hypseus\_singe\_data/tree/master/00-zip-roms](https://github.com/DirtBagXon/hypseus_singe_data/tree/master/00-zip-roms)
2. Copy this zip to `roms\singe\roms`.
3. Create a folder named after the game in `roms\singe\vldp` and copy the `.txt` file and the video and audio files into it.

```
roms\
└─ singe\
   ├─ roms\
   │  └─ timegal.zip
   └─ vldp\
      └─ timegal\
         ├─ timegal.dat
         ├─ timegal.m2v
         ├─ timegal.ogg
         └─ timegal.txt
```

The zip, the folder in `vldp` and the `.txt` file share the same name. In RetroBat, launch the zip file.

### Adding a game in folder format (Hypseus)

The game is a folder placed in `roms\singe`, whose name ends with `.hypseus`. It must contain two files named after the game:

* `<game>.singe`
* `<game>.txt`

To make things easier, start from the files of the `hypseus_singe_data` repository:

{% embed url="https://github.com/DirtBagXon/hypseus_singe_data/" %}

1. Download the content of the repository and extract it to a temporary folder.

<div align="left"><figure><img src="../../../.gitbook/assets/image (517).png" alt=""><figcaption></figcaption></figure></div>

2. Open the game folder. Example: Asterix, in the `00-singe2` sub-folder.

<div align="left"><figure><img src="../../../.gitbook/assets/image (518).png" alt=""><figcaption></figcaption></figure></div>

3. The folder contains a text file listing the missing files and where to put them. For Asterix, `asterix.m2v` goes in the `Video` folder.
4. Add the requested files (`.m2v`, or `.m2v` and `.ogg`).
5. Rename the folder by adding `.hypseus` at the end: `Asterix.hypseus`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (519).png" alt=""><figcaption></figcaption></figure></div>

6. Move this folder to `roms\singe`.

### Passing parameters to Hypseus (.commands)

Create a text file holding the parameters to add, on a single line, and name it after the game with the `.commands` extension:

* folder format: next to the game folder, for example `roms\singe\Asterix.commands` for `Asterix.hypseus`;
* zip format: next to the zip, for example `roms\singe\roms\timegal.commands`.

The name must be exactly the game name, without the `.hypseus` or `.zip` extension.

<div align="left"><figure><img src="../../../.gitbook/assets/image (520).png" alt=""><figcaption></figcaption></figure></div>

### Adding a game for Singe2

Singe2 doesn't run games in Hypseus format. Only the games offered on the emulator website (kangaroopunch.com) work.

1. Download the game from the Singe 2 website.

{% embed url="https://kangaroopunch.com/view/ShowSoftware?id=7" %}

2. Add the requested video and audio files.
3. **Keep the folder name as downloaded** and add `.hypseus` at the end.

<div align="left"><figure><img src="../../../.gitbook/assets/image (521).png" alt=""><figcaption></figcaption></figure></div>

4. Move the folder to `roms\singe` and pick the **singe2** emulator for this game.

Singe2 needs Windows **developer mode** to be enabled (Windows Settings): RetroBat creates a link to the game folder in `emulators\singe2`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (522).png" alt=""><figcaption></figcaption></figure></div>

## Known issues

<table><thead><tr><th width="334">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>A zip game doesn't start</td><td>Check that <code>roms\singe\vldp\&#x3C;game>\&#x3C;game>.txt</code> exists and has the same name as the zip.</td></tr><tr><td>A game in folder format doesn't start</td><td>The folder must contain a <code>.singe</code> file and a <code>.txt</code> file whose names start with the folder name.</td></tr><tr><td>Singe2 shows a symbolic link error</td><td>Enable developer mode in Windows settings.</td></tr><tr><td>Singe2 doesn't start a game that works with Hypseus</td><td>The formats are different: Singe2 only runs the games from its website.</td></tr><tr><td>The controller doesn't respond with Singe2</td><td>Pick the right number in <strong>CONTROLS > FORCE GAMEPAD INDEX</strong>.</td></tr><tr><td>The light gun crosshair is in the way</td><td>Turn off <strong>SHOW CROSSHAIR</strong>.</td></tr><tr><td>"Framework" and "FrameworkKimmy" appear in the game list</td><td>They are not games, but they are required. Hide them: game menu > <strong>EDIT THIS GAME'S METADATA</strong> > <strong>HIDDEN</strong>.</td></tr><tr><td>F12 doesn't create a screenshot with Hypseus</td><td>Screenshots only work on the primary display.</td></tr></tbody></table>
