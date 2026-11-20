# Sonic Retro

<div align="left"><figure><img src="../../../../.gitbook/assets/image (661).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

This system runs the remastered versions of **Sonic the Hedgehog** (1991), **Sonic the Hedgehog 2** (1992) and **Sonic CD** (1993), released on mobile then on PC (Sonic CD in 2011, Sonic 1 and 2 in 2013, then in **Sonic Origins** in 2022). They run on Christian Whitehead's Retro Engine; RetroBat uses the decompilations of the RSDKModding project:

* **RSDKv4** (`sonicretro` emulator) for Sonic 1 and Sonic 2;
* **RSDKv3** (`sonicretrocd` emulator) for Sonic CD.

The games are not supplied: you need the `Data.rsdk` data file of your own copy of each game.

{% embed url="https://github.com/Rubberduckycooly/Sonic-1-2-2013-Decompilation" %}

{% embed url="https://github.com/Rubberduckycooly/Sonic-CD-11-Decompilation" %}

## At a glance

<table><thead><tr><th width="242.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\sonicretro</code></td></tr><tr><td><strong>Extensions</strong></td><td>.rsdk</td></tr><tr><td><strong>Default emulator</strong></td><td>sonicretro (sonicretrocd for Sonic CD, chosen automatically)</td></tr><tr><td><strong>BIOS</strong></td><td>None (<code>Data.rsdk</code> of each game required)</td></tr><tr><td><strong>Controller setup</strong></td><td>Handled by the game</td></tr><tr><td><strong>Save states</strong></td><td>No (in-game saves)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="245.25">Emulator</th><th>Games</th></tr></thead><tbody><tr><td><strong>sonicretro</strong> (RSDKv4)</td><td>Sonic the Hedgehog, Sonic the Hedgehog 2</td></tr><tr><td><strong>sonicretrocd</strong> (RSDKv3)</td><td>Sonic CD</td></tr></tbody></table>

RetroBat runs Sonic CD with sonicretrocd when the game folder is named `soniccd` (case and spaces ignored: `SonicCD`, `Sonic CD` work). Otherwise, enable **EMULATION > FORCE SONIC CD**.

## BIOS

No BIOS is needed.

## Which game format?

One folder per game in `roms\sonicretro`, with the game's **Data.rsdk** file inside:

```
roms\
└── sonicretro\
    ├── sonic1\
    │   └── Data.rsdk
    ├── sonic2\
    │   └── Data.rsdk
    └── soniccd\
        └── Data.rsdk
```

Where the files come from:

* Sonic 1 and Sonic 2: mobile versions (iOS, Android) or Sonic Origins (Steam, Epic Games Store);
* Sonic CD: 2011 Steam version, mobile versions or Sonic Origins.

With **Sonic Origins** data, choose **EMULATION > GAME TYPE > ORIGINS RELEASE**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (662).png" alt=""><figcaption></figcaption></figure></div>

## Controls

The controller is recognized directly by the engine: RetroBat does not set it up. D-pad or left stick = move, face buttons = jump, START = pause.

### Hotkeys

<table><thead><tr><th width="182.75">Action</th><th>Controller</th></tr></thead><tbody><tr><td>Exit</td><td>HOTKEY + START</td></tr></tbody></table>

No save states: progress is saved by the game.

## Folders

<table><thead><tr><th width="269">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Game saves</td><td>game folder (<code>SData.bin</code>), copied by RetroBat to <code>saves\sonicretro\&#x3C;game folder></code></td></tr><tr><td>Settings (written by RetroBat)</td><td>game folder (<code>Settings.ini</code>)</td></tr><tr><td>Mods</td><td>game folder, <code>mods</code> subfolder</td></tr></tbody></table>

## Guides

### Mods

Mods made for the decompilations (RSDKv4 for Sonic 1 and 2, RSDKv3 for Sonic CD) go to the game's `mods` folder, one folder per mod, with a `mod.ini` file inside:

```
roms\
└── sonicretro\
    └── sonic2\
        ├── Data.rsdk
        └── mods\
            └── MyMod\
                └── mod.ini
```

With **EMULATION > ENABLE MODS** (on by default), RetroBat enables every mod of the folder; when off, the game runs without mods. To keep a mod from loading, move its folder out of `mods`. Mods load in the order of the `mods\modconfig.ini` file; new mods are added at the end.

A mod with its own saves keeps them in its folder: RetroBat does not copy them to `saves`.

### Useful options

<table><thead><tr><th width="270.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>EMULATION > LANGUAGE</strong></td><td>Game language (Sonic CD: English, French, Italian, German, Spanish, Japanese).</td></tr><tr><td><strong>EMULATION > GAME TYPE</strong></td><td><strong>ORIGINS RELEASE</strong> for Sonic Origins data.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="257.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>Sonic CD does not start</td><td>Name its folder <code>soniccd</code>, or enable <strong>FORCE SONIC CD</strong>.</td></tr><tr><td>The game does not start</td><td>Check that the game folder contains <code>Data.rsdk</code>.</td></tr><tr><td>A mod is not loaded</td><td>Check that its folder has a <code>mod.ini</code>, that it is made for the right engine (RSDKv4 or RSDKv3) and that <strong>ENABLE MODS</strong> is not off.</td></tr></tbody></table>
