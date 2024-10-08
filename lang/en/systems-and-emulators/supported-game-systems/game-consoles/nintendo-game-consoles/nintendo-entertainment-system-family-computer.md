---
description: Nintendo
---

# Nintendo Entertainment System - Family Computer

<table data-header-hidden><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><p></p><p><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/nes-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/nes.svg" alt="" data-size="original"></picture></p></td><td><p></p><p><img src="https://upload.wikimedia.org/wikipedia/commons/7/7d/Family_Computer_logo.svg" alt="" data-size="original"></p></td><td></td></tr></tbody></table>

Game Console - Lifespan: 1983 - 2003

{% embed url="https://en.wikipedia.org/wiki/Nintendo_Entertainment_System" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: fceumm</li><li>libretro: nestopia</li><li>libretro: mesen</li><li>mednafen</li><li>mesen</li><li>ares</li><li>bizhawk: NesHawk</li><li>bizhawk: QuickNes</li><li>jgenesis</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> nes</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.fds .nes .wad .zip .7z</td><td></td></tr></tbody></table>

## Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>lr-fceumm: YES<br>lr-nestopia: YES<br>lr-mesen: YES<br>Mednafen: NO<br>Mesen: NO<br>Ares: NO<br>BizHawk: YES<br>Jgenesis: NO</td><td>lr-fceumm: YES<br>lr-nestopia: YES<br>lr-mesen: YES<br>Mednafen: NO<br>Mesen: NO<br>Ares: NO<br>BizHawk: NO<br>Jgenesis: NO</td><td>lr-fceumm: YES<br>lr-nestopia: YES<br>lr-mesen: YES<br>Mednafen: YES<br>Mesen: YES<br>Ares: YES<br>BizHawk: YES<br>Jgenesis: YES</td></tr></tbody></table>

## BIOS

There is no BIOS files needed to run games.

## Controls

Some emulators allow to rotate face buttons and/or to enable the turbo function:

<div align="left">

<figure><img src="https://i.imgur.com/2zxeeZ9.png" alt=""><figcaption></figcaption></figure>

</div>

### Available control layouts:

| Option / emulator                                                           | Control layout                                                                                                                                |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Défaut <br>(tous les émulateurs)</p>                                     | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes.png?raw=true" alt="" data-size="original">              |
| <p>TURBO<br>- libretro (retroarch)<br>- mesen<br>- mednafen</p>             | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_turbo.png?raw=true" alt="" data-size="original">        |
| <p>ROTATION<br>(tous les émulateurs)</p>                                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_rotate.png?raw=true" alt="" data-size="original">       |
| <p>ROTATION et TURBO<br>- libretro (retroarch)<br>- mesen<br>- mednafen</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_rotate_turbo.png?raw=true" alt="" data-size="original"> |

## Specific System Information

### Custom textures



The libretro:mesen core allows to load custom texture packs.

To do so you need to place the custom texture pack in the `\bios\HdPacks` folder in a dedicated directory that has the same name than the game file, for example if your game name is `Mega Man (USA).nes`, the texture pack folder must be named `Mega Man (USA)`

<div align="left">

<figure><img src="https://i.imgur.com/0t1gw0h.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
It is very important that the sha1 hash of your game file matches the sha1 located in the "hires.txt" file from the texture pack folder:
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/KAQVQlV.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/b04EdoH.png" alt=""><figcaption></figcaption></figure>

</div>

Then, select the **Libretro: mesen** emulator for the game or the system:

<div align="left">

<figure><img src="https://i.imgur.com/QUAN6n2.png" alt=""><figcaption></figcaption></figure>

</div>

Next you need to enable the Custom Textures options in the Advanced Settings > Visual Rendering section of the Game Options or Advanced Systems Options:

<div align="left">

<figure><img src="https://i.imgur.com/Un77eUl.png" alt=""><figcaption></figcaption></figure>

</div>
