---
description: MAME Team
---

# MAME

Multi-Arcade Emulator - Release year: 1997

{% embed url="https://en.wikipedia.org/wiki/MAME" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>Libretro: mame</li><li>Libretro: mame2016</li><li>Libretro: mame2010</li><li>Libretro: mame2003_plus</li><li>Libretro: mame2003</li><li>Libretro: mame2003_midway</li><li>Libretro: mame2000</li><li>mame64</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> mame</td></tr><tr><td><strong>File extension</strong></td><td>.zip .7z</td></tr></tbody></table>

## System Features

<table><thead><tr><th width="245">Retroachievements</th><th width="200">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>lr-mame: NO<br>Mame64: YES</td></tr></tbody></table>

## Bios Information

Depending on the [romset type](../../arcade-guide.md#romsets), a BIOS can be required or not to play some games:

* **Full non-merged**: the BIOS is included in the ROM file, so no BIOS file will be needed
* **Non-merged**: same as "Full non-merged" but BIOS that are shared by multiple games are placed outside of the individual ROMs
* **Split**: BIOS files are required
* **Merged**: BIOS files (as well as multiple versions of the game) are placed inside the ROM, no separate BIOS is required

{% hint style="info" %}
Refer to the [Arcade page for more information about ROM set types](../../arcade-guide.md#rom-set-types).
{% endhint %}

**Here is a non-exhaustive list of MAME bios files (based on rom set 0.255):**

{% file src="../../../.gitbook/assets/MAME 0.255 ROMs (bios-devices).xml" %}

BIOS files must be placed at the root of the `\bios` folder of your RetroBat installation.



## MAME folders

**Rompath**: \bios & \roms\mame

**Samples**: \bios\mame\samples

**Cfg**: \saves\mame\cfg

**Ini**: \bios\mame\ini

**Hash**: \bios\mame\hash

**Artworks**: \saves\mame\artwork

**Cheats**: \cheats\mame

**Ctrl**: \saves\mame\ctrlr



## Controls

### Controller mapping

| Retrobat Button                                | Arcade Key                                                                           |
| ---------------------------------------------- | ------------------------------------------------------------------------------------ |
| START                                          | START                                                                                |
| SELECT                                         | COIN                                                                                 |
| Left analog stick                              | <p>Left Joystick<br>Paddle<br>Positional device<br>Dial<br>Trackball<br>Ad_Stick</p> |
| Right analog stick                             | Right Joystick                                                                       |
| D-PAD                                          | Directions                                                                           |
| ![](<../../../.gitbook/assets/image (48).png>) | 3                                                                                    |
| ![](<../../../.gitbook/assets/image (30).png>) | 1                                                                                    |
| ![](<../../../.gitbook/assets/image (16).png>) | 2                                                                                    |
| ![](<../../../.gitbook/assets/image (50).png>) | 4                                                                                    |
| L1                                             | 5                                                                                    |
| R1                                             | 6                                                                                    |
| L2                                             | Pedal 2 / 7                                                                          |
| R2                                             | Pedal 1 / 8                                                                          |
| L3                                             | 9                                                                                    |
| R3                                             | 10                                                                                   |

{% hint style="info" %}
Follow this guide to perform specific controller mapping for MAME64 ([refer to this guide](../../../controllers/specific_mapping/mame64-controller-mapping.md)).
{% endhint %}

## Specific system information

### ROM set versions&#x20;

Refer to the [Arcade Guide rom set section](../../arcade-guide.md#available-arcade-emulators-in-retrobat).

### CHD or IMG files

Refer to the [Arcade Guide section](../../arcade-guide.md#chd-or-img-files) about CHD.

### **Sample files**

Refer to the [Arcade Guide "sample file" section](../../arcade-guide.md#samples).

### Service Menu

Press L3 and R3 buttons to access to service menu.

## Known issues & fixes

### I only get a black screen when running games with libretro:mame core

Libretro:Mame has a limitation in the length of the paths it uses when launching a game through command lines. This limitation does not exist with standalone Mame.

In order to be able to fix this issue, ensure that your RetroBat folder path does is not installed in a path that is too long.

For example the path `C:\Emulation\Multi Emulators\FrontEnd\All-in-one\This is top\RetroBat version 7.5.3` is too long and will result in the issue.
