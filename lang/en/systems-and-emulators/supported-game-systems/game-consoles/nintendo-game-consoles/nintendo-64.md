---
description: Nintendo
---

# Nintendo 64

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/n64.svg" alt=""><figcaption></figcaption></figure>

</div>

Game Console - Lifespan: 1996 - 2002

{% embed url="https://en.wikipedia.org/wiki/Nintendo_64" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: mupen64plus next</li><li>libretro: parallel</li><li>mupen64 (RMG)</li><li>simple64</li><li>ares</li><li>bizhawk: Ares64</li><li>bizhawk: Mupen64Plus</li><li>project64</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> n64</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.v64 .z64 .n64 .wad .zip .7z</td><td></td></tr></tbody></table>

## System Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>lr-mupen64: YES<br>lr-parallel: YES<br>RMG: NO<br>Simple64: NO<br>Ares: NO<br>BizHawk: YES<br>Project64: NO</td><td>lr-mupen64: YES<br>lr-parallel: YES<br>RMG: NO<br>Simple64: NO<br>Ares: NO<br>BizHawk: NO<br>Project64: NO</td><td>lr-mupen64: YES<br>lr-parallel: YES<br>RMG: YES<br>Simple64: YES<br>Ares: YES<br>BizHawk: YES<br>Project64: NO</td></tr></tbody></table>

## Features

| Retroachievements | Netplay |
| ----------------- | ------- |
| YES               | NO      |

## BIOS

There is no BIOS files needed to run games.

## Controls

### Libretro (Mupen64plus\_next and parallel)

<div align="left">

<figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64.png?raw=true" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Mupen64 (RMG), Simple64, Ares and Bizhawk

Standalone emulators (Mupen64 RMG & Simple64) have 4 different layouts available that can be switched through this option:

<div align="left">

<figure><img src="https://i.imgur.com/QgyGghe.png" alt=""><figcaption></figcaption></figure>

</div>

Ares and Bizhawk have 2 layout options:

<div align="left">

<figure><img src="https://i.imgur.com/A15fcOj.png" alt=""><figcaption></figcaption></figure>

</div>

Details of the 4 layouts:

| Option                                                                                                            | Layout                                                                                                                                              |
| ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Default<br><br>C-BUTTONS=RIGHT-STICK Z=LEFT-TRIGGER<br><br><strong>Ares/Bizhawk</strong><br>Z=LEFT-TRIGGER</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone.png?raw=true" alt="" data-size="original">         |
| C-BUTTONS=FACE Z=LEFT-TRIGGER                                                                                     | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_face_zl.png?raw=true" alt="" data-size="original"> |
| <p>C-BUTTONS=RIGHT-STICK Z=RIGHT-TRIGGER<br><br><strong>Ares/Bizhawk</strong><br>Z=RIGHT-TRIGGER</p>              | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_zr.png?raw=true" alt="" data-size="original">      |
| C-BUTTONS=FACE Z=RIGHT-TRIGGER                                                                                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/n64-standalone_face_zr.png?raw=true" alt="" data-size="original"> |

### Using a N64 controller

RetroBat will automatically detect and configure the following N64 controllers:

* Original N64 pad with Raphnet adapter
* Original N64 pad with Mayflash adapter
* Nintendo Switch Online N64 Gamepad (only on standalone emulators, not with RetroArch)

Additionaly, RMG Mupen64 and Simple64 can leverage the Raphnet direct access feature with a dedicated plugin, this can be enabled in RetroBat features:

<div align="left">

<figure><img src="https://i.imgur.com/q5F7GM3.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
When using Mayflash adapter, controllers must be plugged in reverse order, meaning player 1 will be assigned to the last port of the adapter.
{% endhint %}

The mapping for N64 controllers can be found in the file "**n64Controllers.json**" that is located in the `\system\resources\inputmapping` folder of the RetroBat installation, it is possible to add your own controller mapping within this file.

## Specific System Information

### Custom textures

mupen64plus next core allows the use of custom textures.

The texture pack must be placed in the `bios\Mupen64Plus\cache\` folder if the pack comes as a .hts or .htc file.

<div align="left">

<figure><img src="https://i.imgur.com/H878WjR.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

If it comes as a uncompressed pack (folder with .png files), it must be placed in the `bios\Mupen64Plus\hires_texture\` folder.

<div align="left">

<figure><img src="https://i.imgur.com/1sqG9H4.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

For htc or hts files, the file name must be `GAMEID"__HIRESTEXTURES.hts` or .htc (for example : `MARIOKART64_HIRESTEXTURES.htc`).

For uncompressed folder, the folder name must be similar to the gameID (for example  `MARIOKART64`).

Once the texture pack in the right folder, enable **CUSTOM TEXTURES** in Retrobat.

<div align="left">

<figure><img src="https://i.imgur.com/jBt3sjA.png" alt=""><figcaption><p>Advanced System Options (can also be done per game)</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/hzikBUa.png" alt=""><figcaption><p>Visual Rendering</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/TXJ3fti.png" alt=""><figcaption></figcaption></figure>

</div>

Select RICE if the texture pack is compressed (htc or hts).&#x20;

Select CACHE if the texture pack is uncompressed (folder).

{% hint style="info" %}
At first launch of a game with an uncompressed texture pack, Mupen64Plus-next will generate a .hts file in `CACHE` folder, upon next launch of the game, it is possible to use RICE instead of CACHE.
{% endhint %}
