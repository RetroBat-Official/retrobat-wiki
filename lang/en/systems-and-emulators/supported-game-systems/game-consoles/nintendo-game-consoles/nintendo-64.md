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

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: mupen64plus next</li><li>libretro: parallel</li><li>mupen64 (RMG)</li><li>simple64</li><li>ares</li><li>bizhawk: Ares64</li><li>bizhawk: Mupen64Plus</li><li>project64</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> n64</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.v64 .z64 .n64 .wad .zip .7z </td><td></td></tr></tbody></table>

## System Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>lr-mupen64: YES<br>lr-parallel: YES<br>RMG: NO<br>Simple64: NO<br>Ares: NO<br>BizHawk: YES<br>Project64: NO</td><td>lr-mupen64: YES<br>lr-parallel: YES<br>RMG: NO<br>Simple64: NO<br>Ares: NO<br>BizHawk: NO<br>Project64: NO</td><td>lr-mupen64: YES<br>lr-parallel: YES<br>RMG: YES<br>Simple64: YES<br>Ares: YES<br>BizHawk: YES<br>Project64: NO</td></tr></tbody></table>

## Features

| Retroachievements | Netplay |
| ----------------- | ------- |
| YES               | NO      |

## BIOS

There is no BIOS files needed to run games.

## Controls

| RetroBat key                                                                       | Nintendo 64 key             |
| ---------------------------------------------------------------------------------- | --------------------------- |
| START                                                                              | START                       |
| SELECT / BACK                                                                      |                             |
| D-PAD                                                                              | D-PAD                       |
| Analog Stick - Left                                                                | Analog Stick                |
| Analog Stick - Right                                                               | C-Buttons                   |
| ![A](<../../../../.gitbook/assets/image (30).png>)                                 | <p>A<br>C-mode: c-down</p>  |
| ![B](<../../../../.gitbook/assets/image (16).png>)                                 | <p>B<br>C-mode: c-right</p> |
| <img src="../../../../.gitbook/assets/image (50).png" alt="" data-size="original"> | C-mode: c-up                |
| <img src="../../../../.gitbook/assets/image (48).png" alt="" data-size="line">     | C-mode: c-left              |
| LB (L1)                                                                            | L                           |
| RB (R1)                                                                            | R                           |
| LT (L2)                                                                            | Z                           |
| RT (R2)                                                                            | Enable C-mode               |
| L-Click (L3)                                                                       |                             |
| R-Click (R3)                                                                       |                             |

<div align="left">

<figure><img src="https://i.imgur.com/NZ91mQ9.png" alt=""><figcaption></figcaption></figure>

</div>

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

## Specific System Information

### Custom textures

mupen64plus next core allows the use of custom textures.

The texture pack must be placed in the `bios\Mupen64Plus\cache\` folder if the pack comes as a .hts or .htc file.

<div align="left">

<figure><img src="https://i.imgur.com/H878WjR.png" alt=""><figcaption></figcaption></figure>

</div>

If it comes as a uncompressed pack (folder with .png files), it must be placed in the `bios\Mupen64Plus\hires_texture\` folder.

<div align="left">

<figure><img src="https://i.imgur.com/1sqG9H4.png" alt=""><figcaption></figcaption></figure>

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
