# Sonic Mania

<div align="left"><figure><img src="../../../../.gitbook/assets/image (663).png" alt="" width="269"><figcaption></figcaption></figure></div>

## Overview

**Sonic Mania** (Sega, 2017) is a 2D Sonic game developed by Christian Whitehead, Headcannon and PagodaWest Games, in the spirit of the Mega Drive games. RetroBat runs it with **RSDKv5U**, the PC version of the Retro Engine from the decompilation of the game (RSDKModding project).

The game is not supplied: you need the `Data.rsdk` data file of your own copy of the game.

{% embed url="https://github.com/Rubberduckycooly/Sonic-Mania-Decompilation" %}

## At a glance

<table><thead><tr><th width="220.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\sonic-mania</code></td></tr><tr><td><strong>Extensions</strong></td><td>.rsdk</td></tr><tr><td><strong>Default emulator</strong></td><td>sonicmania</td></tr><tr><td><strong>BIOS</strong></td><td>None (game <code>Data.rsdk</code> required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Handled by the game</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## BIOS

No BIOS is needed.

## Which game format?

The **Data.rsdk** file of Sonic Mania (PC version, Steam or Epic Games Store, with or without Sonic Mania Plus). Copy it to `roms\sonic-mania`:

```
roms\
└── sonic-mania\
    └── Data.rsdk
```

<div align="left"><figure><img src="../../../../.gitbook/assets/image (664).png" alt=""><figcaption></figcaption></figure></div>

## Controls

The controller is recognized directly by the engine: RetroBat does not set it up. D-pad or left stick = move, face buttons = jump, START = pause.

### Hotkeys

<table><thead><tr><th width="212.75">Action</th><th>Controller</th></tr></thead><tbody><tr><td>Exit</td><td>HOTKEY + START</td></tr></tbody></table>

No save states: progress is saved by the game.

## Folders

<table><thead><tr><th width="264">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game saves</td><td><code>roms\sonic-mania</code> (<code>SaveData.bin</code>, <code>Achievements.bin</code>), copied by RetroBat to <code>saves\sonicmania</code></td></tr><tr><td>Settings (written by RetroBat)</td><td><code>roms\sonic-mania\Settings.ini</code></td></tr><tr><td>Mods</td><td><code>roms\sonic-mania\mods</code></td></tr></tbody></table>

## Guides

### Mods

Mods made for the decompilation (RSDKv5) go to `roms\sonic-mania\mods`, one folder per mod, with a `mod.ini` file inside:

```
roms\
└── sonic-mania\
    ├── Data.rsdk
    └── mods\
        └── MyMod\
            └── mod.ini
```

With **EMULATION > ENABLE MODS** (on by default), RetroBat enables every mod of the folder; when off, the game runs without mods. To keep a mod from loading, move its folder out of `mods`. Mods load in the order of the `mods\modconfig.ini` file; new mods are added at the end.

Mods made for the original Steam version (Mania Mod Loader) do not work with this engine.

### Useful options

<table><thead><tr><th width="245.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>EMULATION > LANGUAGE</strong></td><td>Game language.</td></tr><tr><td><strong>SHADER SET</strong></td><td>Picture filter (sharp, CRT).</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="240.25">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start</td><td>Check that <code>Data.rsdk</code> is in <code>roms\sonic-mania</code>.</td></tr><tr><td>A mod is not loaded</td><td>Check that its folder has a <code>mod.ini</code>, that it is made for the decompilation (RSDKv5) and that <strong>ENABLE MODS</strong> is not off.</td></tr></tbody></table>
