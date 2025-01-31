---
description: Sega
---

# Saturn

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/saturn.svg" alt=""><figcaption></figcaption></figure></div>

Game Console - Lifespan: 1994 - 2000

{% embed url="https://en.wikipedia.org/wiki/Sega_Saturn" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: kronos</li><li>libretro: mednafen saturn</li><li>libretro: yabasanshiro</li><li>mednafen</li><li>bizhawk: saturnus</li><li>yabasanshiro</li><li>kronos</li><li>ssf</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> saturn</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.zip .cue .toc .m3u .ccd .chd .iso .cso .mds .chd .squashfs</td><td></td></tr></tbody></table>

## System Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>lr-kronos: YES<br>lr_mednafen: YES<br>lr-yabasanshiro: YES<br>Mednafen: NO<br>BizHawk: YES<br>Yabasanshiro: NO<br>Kronos: NO<br>SSF: NO</td><td>lr-kronos: YES<br>lr_mednafen: YES<br>lr-yabasanshiro: NO<br>Mednafen: NO<br>BizHawk: NO<br>Yabasanshiro: NO<br>Kronos: NO<br>SSF: NO</td><td>lr-kronos: YES<br>lr_mednafen: YES<br>lr-yabasanshiro: YES<br>Mednafen: YES<br>BizHawk: YES<br>Yabasanshiro: YES<br>Kronos: YES<br>SSF: YES</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="266">BIOS File</th><th width="140">Location</th><th width="341">MD5</th></tr></thead><tbody><tr><td>saturn_bios.bin</td><td>\bios</td><td>af5828fdff51384f99b3c4926be27762</td></tr><tr><td>mpr-17933.bin</td><td>\bios</td><td>3240872c70984b6cbfda1586cab68dbe</td></tr><tr><td>sega_101.bin</td><td>\bios</td><td>85ec9ca47d8f6807718151cbcca8b964</td></tr><tr><td>mpr-18811-mx.ic1</td><td>\bios</td><td></td></tr><tr><td>mpr-19367-mx.ic1</td><td>\bios</td><td></td></tr><tr><td>saturn_bios.bin</td><td>\bios\kronos</td><td>af5828fdff51384f99b3c4926be27762</td></tr></tbody></table>

## Controls

### Standard control layout:

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Trigger inversion:

It is possible to invert triggers and shoulder buttons with the following option:

<div align="left"><figure><img src="https://i.imgur.com/X1fv94k.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_invert_triggers.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Alternative control layouts:

Alternative control layouts can be enabled with the following option:

<div align="left"><figure><img src="https://i.imgur.com/W7qP14u.png" alt=""><figcaption></figcaption></figure></div>

| Option                | Control layout                                                                                                                                            |
| --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| L/R AS Y/Z            | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_yz.png?raw=true" alt="" data-size="original">                 |
| L/R AS Y/Z (inverted) | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_yz_invert_triggers.png?raw=true" alt="" data-size="original"> |
| L/R AS X/Z            | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_xz.png?raw=true" alt="" data-size="original">                 |
| L/R AS X/Z (inverted) | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/saturn_lr_xz_invert_triggers.png?raw=true" alt="" data-size="original"> |

### Using a Saturn-like controller

RetroBat can be used to automatically configure the following type of "Saturn-like" controllers:

* 8Bitdo M30

To do so, use the following option:

<div align="left"><figure><img src="https://i.imgur.com/NFa4xEU.png" alt=""><figcaption></figcaption></figure></div>

Saturn-like controller configuration is managed within the "**saturnControllers.json**" file located in the `\system\resources\inputmapping` folder of the RetroBat installation, it is possible to extend this file to configure automatically additional controllers.

## Specific System Information

### Multi-disc games

You can use a m3u file to manage multi-disc games.

For example for _Panzer Dragoon Saga_, if the ROM contains the following files:&#x20;

<div align="left"><figure><img src="https://i.imgur.com/o3QZPs0.png" alt=""><figcaption></figcaption></figure></div>

create a `Panzer Dragoon Saga.m3u` text file with the following content and save it to the /roms/saturn folder:

<div align="left"><figure><img src="https://i.imgur.com/gy9LuLH.png" alt=""><figcaption></figcaption></figure></div>
