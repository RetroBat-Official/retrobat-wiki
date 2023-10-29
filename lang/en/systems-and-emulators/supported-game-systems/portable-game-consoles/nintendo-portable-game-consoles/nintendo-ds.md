---
description: Nintendo
---

# Nintendo DS

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/nds.svg" alt=""><figcaption></figcaption></figure>

</div>

Portable Game Console - Lifespan: 2004- 2011

{% embed url="https://en.wikipedia.org/wiki/Nintendo_DS" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: desmume</li><li>libretro: desmume2015</li><li>libretro: melonds</li><li>melonds</li><li>bizhawk: melonDS</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> nds</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.nds .bin .zip .7z</td><td></td></tr></tbody></table>

## Features

| Retroachievements | NetPlay            |
| ----------------- | ------------------ |
| YES               | YES (only DesMUme) |

## BIOS

<table><thead><tr><th width="187">Bios file</th><th width="98">Folder</th><th>md5</th></tr></thead><tbody><tr><td>firmware.bin</td><td><code>\bios</code></td><td>145eaef5bd3037cbc247c213bb3da1b3</td></tr><tr><td>bios7.bin</td><td><code>\bios</code></td><td>df692a80a5b1bc90728bc3dfc76cd948</td></tr><tr><td>bios9.bin</td><td><code>\bios</code></td><td>a392174eb3e572fed6447e956bde4b25</td></tr><tr><td>dsi_bios9.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_bios7.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_firmware.bin</td><td><code>\bios</code></td><td></td></tr><tr><td>dsi_nand.bin</td><td><code>\bios</code></td><td></td></tr></tbody></table>

## Controls

{% hint style="info" %}
Stylus movement can be simulated with mouse or with right analog stick (if the feature is enabled).
{% endhint %}

| RetroBat key                                                                       | Nintendo DS key                                         |
| ---------------------------------------------------------------------------------- | ------------------------------------------------------- |
| START                                                                              | START                                                   |
| SELECT / BACK                                                                      | SELECT                                                  |
| D-PAD                                                                              | D-PAD                                                   |
| Left analog stick                                                                  |                                                         |
| Right analog stick                                                                 | Stylus (if option is set)                               |
| ![A](<../../../../.gitbook/assets/image (25).png>)                                 | B                                                       |
| ![B](<../../../../.gitbook/assets/image (11).png>)                                 | A                                                       |
| <img src="../../../../.gitbook/assets/image (45).png" alt="" data-size="original"> | X                                                       |
| <img src="../../../../.gitbook/assets/image (43).png" alt="" data-size="line">     | Y                                                       |
| L1                                                                                 | L                                                       |
| R1                                                                                 | R                                                       |
| L2                                                                                 | DesMUme: LID close/open                                 |
| R2                                                                                 | <p>DesMUme: TAP Stylus<br>MelonDS: Swap Screens</p>     |
| L3                                                                                 | <p>DesMUme: Toggle Microphone<br>MelonDS: Close LID</p> |
| R3                                                                                 | DesMUme: Screen Swap                                    |

<div align="left">

<figure><img src="https://i.imgur.com/5Fa7LxI.png" alt=""><figcaption></figcaption></figure>

</div>

## Specific System Information

### Running DSi games

RetroBat allows you to run DSi nand files (.bin) with melonDS core and melonDS standalone emulators.

In order to do that, you need to place a '.bin' dsi nand file in the `roms\nds` folder, the file will be detected by RetroBat and will automatically launch to the DSi firmware when running the game, from there you will be able to select the game from the nand and run it:

#### Example of a nand file:

<div align="left">

<figure><img src="https://i.imgur.com/gzpnw8S.png" alt=""><figcaption></figcaption></figure>

</div>

When running from RetroBat, you will be directly booted in the DSi nand:

<div align="left">

<figure><img src="https://i.imgur.com/m2XG9ZQ.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/CUHgynR.png" alt=""><figcaption></figcaption></figure>

</div>

<figure><img src="https://i.imgur.com/sPQNh6q.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Note that melonDS is able to run nand files directly, libretro:melonds, however, will require you to have a least 1 .nds game file in the folder (it will use this game as starter to run the nand file).
{% endhint %}

### Adding games to a nand\_file

Only the standalone melonDS emulator allows to install games to a nand, in order to do this, proceed as follows:

* Run melonDS (`emulators\melonds`)
* Open the config > emu settings windows and navigate to the DSi-mode tab:

<div align="left">

<figure><img src="https://i.imgur.com/KlcN2nS.png" alt=""><figcaption></figcaption></figure>

</div>

* Browse to any firmware file you want to modify and click "OK"
* Close the setting window and navigate to system > Manage DSi titles

<div align="left">

<figure><img src="https://i.imgur.com/z8t4zHy.png" alt=""><figcaption></figcaption></figure>

</div>

* In the next window, you can delete or import titles

<div align="left">

<figure><img src="https://i.imgur.com/1Y5RUtd.png" alt=""><figcaption></figcaption></figure>

</div>

* Press "import title..." and in the next screen, select the title to import to nand

<div align="left">

<figure><img src="https://i.imgur.com/tGcMnSu.png" alt=""><figcaption></figcaption></figure>

</div>

* Confirm with "OK", the title is now install to the nand and you can close the emulator

<div align="left">

<figure><img src="https://i.imgur.com/goIa0vj.png" alt=""><figcaption></figcaption></figure>

</div>

Next time you run the .bin nand file from RetroBat, the added title will be available in the nand menu for you to play.



{% hint style="danger" %}
DS nand files have a limited size, running nand files that are heavier than the maximum authorized number of blocks will lead to a black screen.
{% endhint %}
