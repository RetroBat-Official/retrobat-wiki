# Commander Genius

<div align="left"><figure><img src="../../../.gitbook/assets/image (653).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

**Commander Keen** (id Software / Apogee, 1990-1991) is a PC platform game series. **Commander Genius** is a modern engine that runs episodes 1 to 6, **Keen Dreams** and fan games.

Commander Genius adds high resolution, picture filters, controller play and quick save.

Games (Keen Dreams, fan games…) can be downloaded from Commander Genius; the episodes of the series come from your own copies.

{% embed url="https://clonekeenplus.sourceforge.io/" %}

## At a glance

<table><thead><tr><th width="240.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\cgenius\games</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cgenius</td></tr><tr><td><strong>Default emulator</strong></td><td>cgenius</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic</td></tr><tr><td><strong>Save states</strong></td><td>No: quick save / load with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which game format?

Each game is a folder of `roms\cgenius\games`. An empty `.cgenius` file placed in the game folder starts it directly.

```
roms\cgenius\
└── games\
    ├── keen1\
    │   ├── ...
    │   └── Commander Keen.cgenius
    ├── keen2\
    │   ├── ...
    │   └── Commander Keen 2.cgenius
    └── keen7\
        ├── ...
        └── Commander Keen 7.cgenius
```

## Controls

### Automatic configuration

<table><thead><tr><th width="200.25">RetroBat controller</th><th>Commander Keen</th></tr></thead><tbody><tr><td>D-pad</td><td>Directions</td></tr><tr><td>SOUTH</td><td>Jump</td></tr><tr><td>EAST</td><td>Fire</td></tr><tr><td>WEST</td><td>Run</td></tr><tr><td>NORTH</td><td>Pogo</td></tr><tr><td>L1</td><td>Status</td></tr><tr><td>R1</td><td>Camera (Camlead)</td></tr><tr><td>START</td><td>Help</td></tr><tr><td>SELECT</td><td>Back</td></tr></tbody></table>

**CONTROLS > TWO BUTTON FIRE**, **SUPER POGO**, **IMPOSSIBLE POGO** and **AUTO FIRE** change the game.

### Hotkeys

<table><thead><tr><th width="235.25">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quit</td></tr><tr><td>HOTKEY + WEST</td><td>Quick save</td></tr><tr><td>HOTKEY + NORTH</td><td>Quick load</td></tr></tbody></table>

## Folders

<table><thead><tr><th width="210.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Games</td><td><code>roms\cgenius\games</code></td></tr><tr><td>Saves</td><td><code>emulators\cgenius\save</code> (copied to <code>saves\cgenius</code>)</td></tr><tr><td>Configuration</td><td><code>emulators\cgenius\cgenius.cfg</code></td></tr></tbody></table>

{% hint style="info" %}
If Commander Genius was used outside RetroBat, its `Documents\Commander Genius\cgenius.cfg` file would take priority: RetroBat renames it during the game, then puts it back.
{% endhint %}

## Guides

### Download games from Commander Genius

1. Start `CGenius.exe` in `emulators\cgenius`:

<div align="left"><figure><img src="../../../.gitbook/assets/image (658).png" alt="" width="375"><figcaption></figcaption></figure></div>

2. Click **+ MORE**:

<div align="left"><figure><img src="../../../.gitbook/assets/image (657).png" alt="" width="375"><figcaption></figcaption></figure></div>

3. Select the game and click **Download**. The game is downloaded to `emulators\cgenius\games`:

<div align="left"><figure><img src="../../../.gitbook/assets/image (656).png" alt=""><figcaption></figcaption></figure></div>

4. Copy the game folder (KeenDreams in the example) to `roms\cgenius\games`:

<div align="left"><figure><img src="../../../.gitbook/assets/image (655).png" alt=""><figcaption></figcaption></figure></div>

5. Create a `.cgenius` file in the game folder:

<div align="left"><figure><img src="../../../.gitbook/assets/image (654).png" alt=""><figcaption></figcaption></figure></div>

### Options

* **SHADER SET** (SCALE2X to SCALE4X) smooths the picture, **INTERNAL GAME RESOLUTION** widens the view.
* The bezel is only displayed with the 4/3 **GAME ASPECT RATIO**.

## Known issues

<table><thead><tr><th width="289">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start directly</td><td>The game must be in a subfolder of <code>roms\cgenius\games</code>.</td></tr></tbody></table>
