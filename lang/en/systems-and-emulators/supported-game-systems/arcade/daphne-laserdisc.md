# LaserDisc

<div align="left"><figure><img src="../../../.gitbook/assets/image (515).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

In the early 1980s, some arcade cabinets did not display graphics computed by the machine: they played a film recorded on a **LaserDisc**. The player has to react at the right moment, and the cabinet jumps to the next sequence or to the failure scene.

The genre was launched in 1983 by **Dragon's Lair**, an interactive cartoon made by former Disney animator Don Bluth, with a picture quality nothing else could match at the time. It was followed by Space Ace, Cliff Hanger, Astron Belt, M.A.C.H. 3, Cobra Command, Thayer's Quest and Super Don Quix-ote, then Dragon's Lair II: Time Warp in 1991.

The system is named after **Daphne**, the first LaserDisc arcade emulator, created by Matt Ownby. By default RetroBat uses **Hypseus Singe**, its modern version, which also runs **Singe** games (see the [**Singe**](../game-engines/singe.md) page).

A LaserDisc game is made of two parts: the cabinet ROM and the video and audio files taken from the disc.

{% embed url="http://www.daphne-emu.com/site3/index_hi.php" %}

## At a glance

<table><thead><tr><th width="237.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\daphne</code></td></tr><tr><td><strong>Extensions</strong></td><td>.daphne .hypseus .7z .rar .squashfs</td></tr><tr><td><strong>Default emulator</strong></td><td>hypseus</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, except daphne</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>Hypseus (Singe games)</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="132.75">Emulator</th><th width="156.75">For whom?</th><th width="231.5">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>hypseus</strong> (default)</td><td>Everyone</td><td>Modern version of Daphne, still updated. Controller configured automatically, decorations, Daphne games and Singe games, light guns.</td><td>—</td></tr><tr><td><strong>daphne</strong></td><td>Special cases</td><td>The original emulator.</td><td>No longer updated. RetroBat doesn't configure the controller: it is played with the keyboard. No Singe games.</td></tr><tr><td><strong>singe2</strong></td><td>Games in Singe 2 format</td><td>See the <a href="../game-engines/singe.md"><strong>Singe</strong></a> page.</td><td>Doesn't run Daphne games.</td></tr></tbody></table>

**When in doubt, keep hypseus.**

## BIOS

No BIOS is needed. Each game does need its ROM, to be placed in `roms\daphne\roms` (see below).

## Which game format?

A Daphne game is made of two items, which share the **same name**:

<table><thead><tr><th width="125.75">Item</th><th width="261">Location</th><th>Content</th></tr></thead><tbody><tr><td>Game folder</td><td><code>roms\daphne\&#x3C;name>.daphne</code></td><td>The videos (<code>.m2v</code>), the sound (<code>.ogg</code>) and the <code>&#x3C;name>.txt</code> file, which gives the order of the videos</td></tr><tr><td>Cabinet ROM</td><td><code>roms\daphne\roms\&#x3C;name>.zip</code></td><td>The game program</td></tr></tbody></table>

Example for Dragon's Lair (`lair`):

```
roms\daphne\
├─ roms\
│  └─ lair.zip
└─ lair.daphne\
   ├─ lair.txt
   ├─ lair.m2v
   └─ lair.ogg
```

The name is the one expected by the emulator: `lair` for Dragon's Lair, `ace` for Space Ace, `cliff` for Cliff Hanger… The `.daphne` folder is what shows up in the RetroBat game list.

<table><thead><tr><th width="185.5">Format</th><th width="86.5">hypseus</th><th width="74.25">daphne</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.daphne folder</strong></td><td>✔</td><td>✔</td><td>The normal format.</td></tr><tr><td>.hypseus folder</td><td>✔</td><td>✔</td><td>Same content, other extension name.</td></tr><tr><td>.7z / .rar / .squashfs</td><td>✔</td><td>✔</td><td>Compressed game folder, extracted at launch.</td></tr></tbody></table>

Singe games (American Laser Games, Time Gal…) also work here with Hypseus, but they have their own system: see the [**Singe**](../game-engines/singe.md) page.

## Controls

### Automatic configuration

With **Hypseus**, RetroBat automatically configures the player 1 controller. The keyboard always remains usable.

<table><thead><tr><th width="148.25">Action</th><th width="246.5">RetroBat controller</th><th>Keyboard</th></tr></thead><tbody><tr><td>Directions</td><td>D-pad / left stick</td><td>Arrow keys</td></tr><tr><td>Button 1</td><td>SOUTH</td><td>Left CTRL</td></tr><tr><td>Button 2</td><td>EAST</td><td>Left ALT</td></tr><tr><td>Button 3</td><td>R1</td><td>SPACE</td></tr><tr><td>Skill 1</td><td>WEST</td><td>Left SHIFT</td></tr><tr><td>Skill 2</td><td>NORTH</td><td>Z</td></tr><tr><td>Skill 3</td><td>L1</td><td>X</td></tr><tr><td>Coin player 1</td><td>SELECT</td><td>5</td></tr><tr><td>Start player 1</td><td>START</td><td>1</td></tr><tr><td>Coin player 2</td><td>—</td><td>6</td></tr><tr><td>Start player 2</td><td>—</td><td>2</td></tr><tr><td>Service</td><td>L3</td><td>9</td></tr><tr><td>Test</td><td>R3</td><td>0</td></tr><tr><td>Pause</td><td>—</td><td>P</td></tr><tr><td>Reset</td><td>—</td><td>F3</td></tr><tr><td>Screenshot</td><td>—</td><td>F12</td></tr></tbody></table>

In most games, only the directions and button 1 are used (the sword in Dragon's Lair, the shot in Space Ace). The Skill buttons pick the difficulty level in games that offer it.

For flight games, the **CONTROLS > INVERT UP AND DOWN** option swaps up and down.

With **daphne**, RetroBat doesn't configure the controller: the game is played with the keyboard.

To configure the Hypseus keys yourself, turn off **AUTOCONFIGURE CONTROLLERS**.

### Hotkeys

<table><thead><tr><th width="272.75">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr><tr><td>ESC</td><td>Quit (keyboard)</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="301.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game ROMs</td><td><code>roms\daphne\roms</code></td></tr><tr><td>Videos and sound of a game</td><td><code>roms\daphne\&#x3C;name>.daphne</code></td></tr><tr><td>Settings of a game</td><td><code>roms\daphne\&#x3C;name>.commands</code></td></tr><tr><td>Hypseus keys</td><td><code>emulators\hypseus\hypinput.ini</code></td></tr><tr><td>Hypseus decorations</td><td><code>emulators\hypseus\bezels</code></td></tr><tr><td>Hypseus screenshots (F12)</td><td><code>emulators\hypseus\screenshots</code></td></tr></tbody></table>

## Guides

### Adding a game

1. Copy the game ROM, for example `lair.zip`, to `roms\daphne\roms`.
2. Copy the folder holding the videos to `roms\daphne`.
3. Rename this folder with the ROM name followed by `.daphne`: `lair.daphne`.
4. Check that the folder contains a `.txt` file with the same name: `lair.txt`.
5. Update the game list in RetroBat.

<div align="left"><figure><img src="../../../.gitbook/assets/image (516).png" alt=""><figcaption></figcaption></figure></div>

On first launch, the emulator analyses the videos and creates `.dat` files in the game folder: startup takes longer that time.

### Tuning a game with a .commands file

Cabinets were set up with switches (number of lives, difficulty, credits). To change them, or to pass other parameters to the emulator, create a text file named after the game with the `.commands` extension, **next to** the game folder:

```
roms\daphne\lair.daphne\
roms\daphne\lair.commands
```

Write the parameters on a single line, separated by spaces. For example, to set the two banks of switches:

```
-bank 0 xxxxxxxx -bank 1 xxxxxxxx
```

Each `x` is 0 or 1 and matches one switch. Their meaning depends on the game and on the version of its ROM.

In this file, RetroBat ignores the parameters it handles itself (fullscreen, paths, rendering type…).

### Decorations with Hypseus

Hypseus displays a decoration around the picture. RetroBat picks it in this order:

1. the file chosen with the **FORCE BEZEL** option;
2. a `<name>.png` file in `emulators\hypseus\bezels`;
3. a `.png` file whose name contains `bezel`, in the game folder;
4. the RetroBat decoration of the game or the system.

Steps 2 and 3 only apply if you have not picked a specific decoration in RetroBat. If decorations are disabled, only the **FORCE BEZEL** option applies.

## Known issues

<table><thead><tr><th width="339">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game is listed but doesn't start</td><td>Check the three names, which must be identical: <code>roms\daphne\roms\&#x3C;name>.zip</code>, the <code>&#x3C;name>.daphne</code> folder and the <code>&#x3C;name>.txt</code> file inside it.</td></tr><tr><td>The first launch is very long</td><td>This is normal: the emulator analyses the videos once and for all.</td></tr><tr><td>The controller doesn't respond</td><td>Only Hypseus is configured by RetroBat, and for player 1. With daphne, use the keyboard or switch to Hypseus.</td></tr><tr><td>Up and down are inverted in a flight game</td><td>Turn on <strong>INVERT UP AND DOWN</strong>.</td></tr><tr><td>The picture doesn't fill the screen</td><td>Turn on <strong>STRETCH TO SCREEN</strong>.</td></tr><tr><td>Scenes are cut off too early</td><td>Add <code>-latency</code> followed by a delay in milliseconds to the game's <code>.commands</code> file.</td></tr><tr><td>High scores are not kept</td><td>RetroBat deletes the emulator's <code>ram</code> folder (the arcade board memory) when the game closes.</td></tr><tr><td>F12 doesn't create a screenshot with Hypseus</td><td>Create the <code>emulators\hypseus\screenshots</code> folder if it doesn't exist. Screenshots only work on the primary display.</td></tr></tbody></table>
