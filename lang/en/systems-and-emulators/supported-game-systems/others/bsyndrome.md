# Bermuda Syndrome

<div align="left"><figure><img src="../../../.gitbook/assets/image (643).png" alt="" width="514"><figcaption></figcaption></figure></div>

## Overview

**Bermuda Syndrome** (Century Interactive / BMG, 1995) is a 2D action-adventure game: pilot Jack Thompson crashes into a world of dinosaurs, in the heart of the Bermuda Triangle.

RetroBat uses **Bermuda**, a free rewrite of the game engine.

The game files are not provided: use the ones from your own copy.

{% embed url="https://github.com/cyxx/bermuda" %}

## At a glance

<table><thead><tr><th width="260.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\bsyndrome</code></td></tr><tr><td><strong>Extensions</strong></td><td>.game</td></tr><tr><td><strong>Default emulator</strong></td><td>bsyndrome</td></tr><tr><td><strong>BIOS</strong></td><td>None (game files to provide)</td></tr><tr><td><strong>Controller setup</strong></td><td>No: keyboard</td></tr><tr><td><strong>Save states</strong></td><td>No: in-game saves (S / L keys)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>—</td></tr><tr><td><strong>Wheels</strong></td><td>—</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## BIOS

No BIOS is needed. The music files (`.ogg`) go to `bios\bsyndrome\MUSIC`.

## Which game format?

An empty `.game` file placed in `roms\bsyndrome` starts the game of the `roms\bsyndrome\DATA` folder.

## Controls

The game reads the **first controller** it recognizes by itself, with fixed buttons: RetroBat does not set it up. The keyboard stays active.

| Controller                 | Keyboard      | Action                    |
| -------------------------- | ------------- | ------------------------- |
| D-pad, left or right stick | Arrows        | Move Jack                 |
| START                      | Tab           | Show the bag              |
| NORTH                      | Ctrl          | Show the status bar       |
| EAST / WEST                | Space / Shift | Use the weapon            |
| SOUTH                      | Enter         | Skip dialogs              |
| SELECT                     | Esc           | Esc key                   |
| —                          | C             | Screenshot (`.tga`)       |
| —                          | S             | Save                      |
| —                          | L             | Load a save               |
| —                          | + / -         | Next / previous save slot |
| —                          | F             | Fast mode                 |
| —                          | W             | Fullscreen / window       |

{% hint style="warning" %}
The game uses the gamecontrollerdb.txt file located near the engine executable `\emulators\bsyndrome`, without such file only Xinput controllers might work.
{% endhint %}

### Hotkeys

| Hotkey         | Action |
| -------------- | ------ |
| HOTKEY + START | Quit   |

## Folders

| Content   | Folder                 |
| --------- | ---------------------- |
| Game data | `roms\bsyndrome\DATA`  |
| Music     | `bios\bsyndrome\MUSIC` |
| Saves     | `saves\bsyndrome`      |

## Guides

### File layout

```
roms\bsyndrome\
├── DATA\                    (files of the game's BERMUDA folder)
│   ├── (subfolders)
│   ├── BERMUDA.OVR
│   ├── BERMUDA.SPR
│   └── BERMUDA.WGP
└── Bermuda Syndrome.game    (empty file)

bios\bsyndrome\
└── MUSIC\                   (.ogg files)
```

**GAME ASPECT RATIO** switches the picture to 4/3 or 16/9.

## Known issues

| Issue                                           | Solution                                                                |
| ----------------------------------------------- | ----------------------------------------------------------------------- |
| "DATA folder not found in roms\bsyndrome\DATA." | Copy the files of the game's `BERMUDA` folder to `roms\bsyndrome\DATA`. |
