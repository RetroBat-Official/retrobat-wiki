---
description: Sega
---

# Megadrive - Genesis (MSU)

<div align="left"><figure><img src="../../../../.gitbook/assets/image (476).png" alt="" width="375"><figcaption></figcaption></figure></div>

## Overview

MSU-MD is a fan-made driver that lets MegaDrive / Genesis games play CD-quality music. The game runs from the cartridge as usual, and the Mega-CD is only used to play audio tracks (this is called "Mode 1"). The community has patched many games this way (Sonic, Streets of Rage, OutRun, Castlevania Bloodlines…) with arranged or original soundtracks.

RetroBat also runs **MD+** patches (made for the MegaSD flash cart) from the same folder: they work the same way, but don't need a BIOS.

In EmulationStation, MSU-MD appears inside the **MegaDrive** group.

## At a glance

<table><thead><tr><th width="241.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\megadrive-msu</code></td></tr><tr><td><strong>Extensions</strong></td><td>.68k .sgd .smd .bin .gen .md .zip .7z</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: genesis_plus_gx</td></tr><tr><td><strong>BIOS</strong></td><td><code>bios_CD_U.bin</code> (or E / J) required for MSU-MD, none for MD+</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro cores, BlastEm</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro cores (patched ROM usually not recognized)</td></tr><tr><td><strong>Netplay</strong></td><td>libretro cores</td></tr><tr><td><strong>Light guns</strong></td><td>libretro cores (genesis_plus_gx)</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="290.25">Emulator</th><th>When to use it</th></tr></thead><tbody><tr><td><strong>Genesis Plus GX</strong> (libretro, default)</td><td>Best choice. Supports MSU-MD and MD+, and reads BIN, WAV and OGG tracks.</td></tr><tr><td><strong>Genesis Plus GX Wide</strong> (libretro)</td><td>Same as above, with a widescreen display. Some games show graphical glitches on the sides.</td></tr><tr><td><strong>Genesis Plus GX Expanded</strong> (libretro)</td><td>Fork made mainly for Paprium. Nothing extra for MSU-MD.</td></tr><tr><td><strong>BlastEm</strong></td><td>Very accurate emulator. MSU-MD works, MD+ does not. Some soundpacks may not play (see Known issues).</td></tr></tbody></table>

To change the emulator: select the system or the game, press **SELECT** › **ADVANCED SYSTEM OPTIONS** (or **ADVANCED GAME OPTIONS**) › **EMULATOR**.

## BIOS

MSU-MD uses the real Mega-CD, so it needs a Mega-CD BIOS in the `bios` folder (the same files as the Mega-CD system):

<table><thead><tr><th width="168.25">File</th><th width="371.5">MD5</th><th>Region</th></tr></thead><tbody><tr><td><code>bios_CD_U.bin</code></td><td><code>854b9150240a198070150e4566ae1290</code></td><td>USA (Sega CD)</td></tr><tr><td><code>bios_CD_E.bin</code></td><td><code>e66fa1dc5820d254611fdcdba0662372</code></td><td>Europe</td></tr><tr><td><code>bios_CD_J.bin</code></td><td><code>278a9397d192149e84e820ac621a8edd</code></td><td>Japan</td></tr></tbody></table>

The emulator uses the BIOS matching the console region. Most MSU-MD patches refuse to run on a PAL console, so **`bios_CD_U.bin` is the one you really need**.

MD+ games do not use any BIOS.

## Formats

An MSU-MD game is made of three things, all in the same folder:

* the **patched ROM** (`.md`, `.bin`, `.gen`, `.smd`);
* a **`.cue` file with exactly the same name** as the ROM;
* the **audio tracks** listed in the `.cue` (`.ogg`, `.wav` or `.bin`).

Example:

```
roms\megadrive-msu\
├── Sonic the Hedgehog (MSU-MD).md
├── Sonic the Hedgehog (MSU-MD).cue
├── Sonic the Hedgehog (MSU-MD)-01.ogg
├── Sonic the Hedgehog (MSU-MD)-02.ogg
└── ...
```

You can also put each game in its own subfolder.

{% hint style="warning" %}
* Only the ROM appears in the game list: this is normal, the `.cue` is loaded automatically.
* Do **not** zip the ROM: the emulator may no longer find the `.cue` and the game will play its original music.
* The patch must be applied to the ROM beforehand: RetroBat does not soft-patch MSU-MD games.
{% endhint %}

Genesis Plus GX also accepts a `.chd` with the same name instead of the `.cue` and its tracks.

## Controls

Controls are exactly the same as on the **MegaDrive**: controllers are **automatically configured**, and the same options are available (button layout, 3-button mode, multitap, special controllers, light guns).

👉 See the [MegaDrive page](megadrive-genesis.md) for the full layout and options, and the [Special controllers page](../../../../controllers/supported-controllers/gamepads/special-controllers.md) for the Sega 6-button pads.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (477).png" alt="" width="225"><figcaption></figcaption></figure></div>

## Folders

<table><thead><tr><th width="282.75">Content</th><th>Location</th></tr></thead><tbody><tr><td>ROMs, <code>.cue</code> and tracks</td><td><code>roms\megadrive-msu</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>Saves and save states (libretro)</td><td><code>saves\megadrive-msu</code></td></tr><tr><td>Saves and save states (BlastEm)</td><td><code>saves\megadrive-msu\blastem\&#x3C;game name></code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### Creating an MSU-MD game

1. Download the MSU-MD patch and its soundpack (the patch is usually distributed with its audio tracks and a `.cue`).
2. Read the patch's readme: it tells you **exactly which ROM version** is needed (name, revision or checksum). A wrong ROM is the main cause of failure.
3. Apply the patch to your ROM with the tool given by the author (Floating IPS / Flips for `.ips` and `.bps` files, or the provided script).
4. Rename the patched ROM so that it has **the same name** as the `.cue` (or rename the `.cue`, without changing the track names written inside it).
5. Copy the ROM, the `.cue` and the tracks into `roms\megadrive-msu`.
6. Update the game lists (**START** › **GAME SETTINGS** › **UPDATE GAMELISTS**).

## Known issues

**"MSU-MD lockout" screen, or a message saying no Mega-CD was found**

* The Mega-CD BIOS is missing: add `bios_CD_U.bin`.
* The console is in PAL mode (European ROM): set **CONSOLE REGION** to **NTSC US** in the game's advanced options (Genesis Plus GX), or **REGION** with BlastEm.

**The game runs but with its original music**

* The ROM and the `.cue` don't have exactly the same name.
* The ROM is zipped: unzip it.
* A track name written in the `.cue` doesn't match the files.
* **CD ADD-ON** has been forced to the wrong add-on: leave it on automatic (MD+ patches need MegaSD, MSU-MD patches need Mega CD).

**No music with BlastEm** BlastEm doesn't support MD+ patches, and some soundpacks may not play. Use Genesis Plus GX.

**No achievements** RetroAchievements identifies games by their ROM: a patched ROM is usually not recognized.
