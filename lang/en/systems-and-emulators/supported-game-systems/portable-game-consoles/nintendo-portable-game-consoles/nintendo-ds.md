---
description: Nintendo
---

# Nintendo DS

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/nds.svg" alt=""><figcaption></figcaption></figure></div>

Portable Game Console - Lifespan: 2004- 2011

{% embed url="https://en.wikipedia.org/wiki/Nintendo_DS" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: melonds DS</li><li>libretro: desmume</li><li>libretro: desmume2015</li><li>libretro: melonds</li><li>libretro: noods</li><li>melonds</li><li>desmume</li><li>bizhawk: melonDS</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> nds</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.nds .bin .zip .7z</td><td></td></tr></tbody></table>

## System Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>lr-melondsds: YES<br>lr-desmume: YES<br>lr-desmume2015: YES<br>lr-melonds: YES<br>lr-noods: YES<br>MelonDS: NO<br>DesMume: NO<br>BizHawk: YES</td><td>lr-melondsds: NO<br>lr-desmume: YES<br>lr-desmume2015: YES<br>lr-melonds: NO<br>lr-noods: NO<br>MelonDS: NO<br>DesMume: NO<br>BizHawk: NO</td><td>lr-melondsds: YES<br>lr-desmume: YES<br>lr-desmume2015: YES<br>lr-melonds: YES<br>lr-noods: YES<br>MelonDS: YES<br>DesMume: YES<br>BizHawk: YES</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="187">Bios file</th><th width="98">Folder</th><th>md5</th></tr></thead><tbody><tr><td>firmware.bin</td><td><code>\bios</code></td><td>145eaef5bd3037cbc247c213bb3da1b3</td></tr><tr><td>bios7.bin</td><td><code>\bios</code></td><td>df692a80a5b1bc90728bc3dfc76cd948</td></tr><tr><td>bios9.bin</td><td><code>\bios</code></td><td>a392174eb3e572fed6447e956bde4b25</td></tr><tr><td>dsi_bios9.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_bios7.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_firmware.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_nand.bin</td><td><code>\bios</code></td><td></td></tr></tbody></table>

## Controls

Except standalone MelonDS emulator, all emulators can simulate touchscreen with the joystick, this can usually be enabled in the advanced options > controls:

<div align="left"><figure><img src="https://i.imgur.com/2BUwdga.png" alt=""><figcaption></figcaption></figure></div>

| Option / emulator                   | Control layout                                                                                                                                         |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| lr-melondsds                        | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melondsds.png?raw=true" alt="" data-size="original">             |
| <p>lr-desmume<br>lr-desmume2015</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds.png?raw=true" alt="" data-size="original">                       |
| lr-melonds                          | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds.png?raw=true" alt="" data-size="original">               |
| MelonDS standard                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds_standalone.png?raw=true" alt="" data-size="original">    |
| MelonDS (left stick)                | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_melonds_standalone_ls.png?raw=true" alt="" data-size="original"> |
| BizHawk standard                    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_bizhawk.png?raw=true" alt="" data-size="original">               |
| BizHawk (mouse)                     | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nds_bizhawk_mouse.png?raw=true" alt="" data-size="original">         |

## Specific System Information

### Running DSi games

RetroBat allows you to run DSi nand files (.bin) with libretro:melonDS\_ds, libretro:melonDS and melonDS standalone emulators.

libretro:MelonDS\_ds has native support, there is nothing special to do except run the game.

For libretro:melonDS and MelonDS, you need to place a '.bin' dsi nand file in the `roms\nds` folder, the file will be detected by RetroBat and will automatically launch to the DSi firmware when running the game, from there you will be able to select the game from the nand and run it:

#### Example of a nand file:

<div align="left"><figure><img src="https://i.imgur.com/gzpnw8S.png" alt=""><figcaption></figcaption></figure></div>

When running from RetroBat, you will be directly booted in the DSi nand:

<div align="left"><figure><img src="https://i.imgur.com/m2XG9ZQ.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/CUHgynR.png" alt=""><figcaption></figcaption></figure></div>

<figure><img src="https://i.imgur.com/sPQNh6q.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note that melonDS is able to run nand files directly, libretro:melonds, however, will require you to have a least 1 .nds game file in the folder (it will use this game as starter to run the nand file).
{% endhint %}

### Adding games to a nand\_file

Only the standalone melonDS emulator allows to install games to a nand, in order to do this, proceed as follows:

* Run melonDS (`emulators\melonds`)
* Open the config > emu settings windows and navigate to the DSi-mode tab:

<div align="left"><figure><img src="https://i.imgur.com/KlcN2nS.png" alt=""><figcaption></figcaption></figure></div>

* Browse to any firmware file you want to modify and click "OK"
* Close the setting window and navigate to system > Manage DSi titles

<div align="left"><figure><img src="https://i.imgur.com/z8t4zHy.png" alt=""><figcaption></figcaption></figure></div>

* In the next window, you can delete or import titles

<div align="left"><figure><img src="https://i.imgur.com/1Y5RUtd.png" alt=""><figcaption></figcaption></figure></div>

* Press "import title..." and in the next screen, select the title to import to nand

<div align="left"><figure><img src="https://i.imgur.com/tGcMnSu.png" alt=""><figcaption></figcaption></figure></div>

* Confirm with "OK", the title is now install to the nand and you can close the emulator

<div align="left"><figure><img src="https://i.imgur.com/goIa0vj.png" alt=""><figcaption></figcaption></figure></div>

Next time you run the .bin nand file from RetroBat, the added title will be available in the nand menu for you to play.



{% hint style="danger" %}
DS nand files have a limited size, running nand files that are heavier than the maximum authorized number of blocks will lead to a black screen.
{% endhint %}
