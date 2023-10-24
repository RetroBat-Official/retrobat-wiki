---
description: Sony
---

# PlayStation 2

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/ps2-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/ps2.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Game Console - Lifespan: 2000 - 2013

{% embed url="https://en.wikipedia.org/wiki/PlayStation_2" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>pcsx2</li><li>pcsx2-16</li><li>play</li><li>Libretro: pcsx2</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> ps2</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.iso .cso .bin .mdf .gz .chd</td><td></td></tr></tbody></table>

## Features

| Retroachievements         | NetPlay |
| ------------------------- | ------- |
| YES (with PCSX2 1.7 only) | NO      |

## BIOS

<table><thead><tr><th width="196">Bios file</th><th width="113">Folder</th><th>md5</th></tr></thead><tbody><tr><td>SCPH30004R.bin</td><td><code>\bios</code></td><td>28922c703cc7d2cf856f177f2985b3a9</td></tr><tr><td>SCPH30004R.MEC</td><td><code>\bios</code></td><td>3faf7c064a4984f53e2ef5e80ed543bc</td></tr><tr><td>scph39001.bin</td><td><code>\bios</code></td><td>d5ce2c7d119f563ce04bc04dbc3a323e</td></tr><tr><td>scph39001.MEC</td><td><code>\bios</code></td><td>3faf7c064a4984f53e2ef5e80ed543bc</td></tr><tr><td>EROM.BIN</td><td><code>\bios</code></td><td>9a9e8ed7668e6adfc8f7766c08ab9cd0</td></tr><tr><td>rom1.bin</td><td><code>\bios</code></td><td>44552702b05697a14ccbe2ca22ee7139</td></tr><tr><td>ROM2.BIN</td><td><code>\bios</code></td><td>b406d05922dac2eaf3c2e68157b1b468</td></tr></tbody></table>

### Other possible non-mandatory BIOS files

<table><thead><tr><th width="379">Bios file</th><th width="347">Folder</th></tr></thead><tbody><tr><td>SCPH-39004_BIOS_V7_EUR_160.BIN</td><td><code>\bios</code></td></tr><tr><td>SCPH-39001_BIOS_V7_USA_160.BIN</td><td><code>\bios</code></td></tr><tr><td>SCPH-70000_BIOS_V12_JAP_200.BIN</td><td><code>\bios</code></td></tr></tbody></table>

{% hint style="info" %}
For lr-pcsx2, bios files need to be placed in `\bios\pcsx2\bios` folder.
{% endhint %}

## Controls

{% hint style="info" %}
The following controllers can be autoconfigured from Retrobat to PCSX2:

* XInput controllers
* Dualshock & DualSense controllers
* Nintendo Switch Pro controller
{% endhint %}

| RetroBat key                                                                       | Playstation 2 key  |
| ---------------------------------------------------------------------------------- | ------------------ |
| START                                                                              | START              |
| SELECT / BACK                                                                      | SELECT             |
| D-PAD                                                                              | D-PAD              |
| Left analog stick                                                                  | Left analog stick  |
| Right analog stick                                                                 | Right analog stick |
| ![A](<../../../../.gitbook/assets/image (25).png>)                                 | Cross              |
| ![B](<../../../../.gitbook/assets/image (11).png>)                                 | Circle             |
| <img src="../../../../.gitbook/assets/image (45).png" alt="" data-size="original"> | Triangle           |
| <img src="../../../../.gitbook/assets/image (43).png" alt="" data-size="line">     | Square             |
| L1                                                                                 | L1                 |
| R1                                                                                 | R1                 |
| L2                                                                                 | L2                 |
| R2                                                                                 | R2                 |
| L3                                                                                 | L3                 |
| R3                                                                                 | R3                 |

<div align="left">

<figure><img src="https://i.imgur.com/9sz2VFM.png" alt=""><figcaption></figcaption></figure>

</div>



{% hint style="warning" %}
Only PCSX2 1.7 offers autoconfiguration, for Play! and pcsx2 1.6, you need to configure controls directly within the emulator.
{% endhint %}

## System Features

### Custom textures

PCSX2 allows to load custom texture packs.

To do so you need to place the custom texture pack in the `\bios\pcsx2\textures` folder in a dedicated directory that has the same code as the game.

<div align="left">

<figure><img src="https://i.imgur.com/nOBWsbc.png" alt=""><figcaption></figcaption></figure>

</div>

The texture files must be placed in a sub-directory called "replacements":

<div align="left">

<figure><img src="https://i.imgur.com/H7dUscl.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
To get the code of the game, you can launch the game a first time directly from the emulator executable located in the `\emulators\pcsx2` folder with the "dump textures" option on, PCSX2 will automatically create the game texture folder in the `\bios\pcsx2\textures` folder.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/hHyR18f.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/6IeWCXM.png" alt=""><figcaption></figcaption></figure>

</div>

Once the texure pack in the right folder, set Retrobat to load custom textures, this is achieved from the **VISUAL RENDERING** menu in the [Advanced System Options](../../../../navigation/view-options.md#advanced-system-options) or in the [Advanced Game Options](../../../../navigation/game-options.md#advanced-game-options) menu :

<div align="left">

<figure><img src="https://i.imgur.com/kMCqWFr.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/zLj3F55.png" alt=""><figcaption></figcaption></figure>

</div>

### Multi-disc games

PCSX2 does not support m3u usage for multi-disc games.

<div align="left">

<figure><img src="https://i.imgur.com/5n2VsbQ.png" alt=""><figcaption></figcaption></figure>

</div>

In order to swap disc in PCSX2, the following must be used within the emulator:

When the game prompts you to swap disc,access the PCSX2 quick menu by pressing SELECT + ![A](<../../../../.gitbook/assets/image (25).png>) on your controller, select the "**Change Disc**" option

<div align="left">

<figure><img src="https://i.imgur.com/fihyt1U.png" alt=""><figcaption></figcaption></figure>

</div>

In the next screen, choose the right disc image and press ![A](<../../../../.gitbook/assets/image (25).png>)

<div align="left">

<figure><img src="https://i.imgur.com/leMX1Ob.png" alt=""><figcaption></figcaption></figure>

</div>
