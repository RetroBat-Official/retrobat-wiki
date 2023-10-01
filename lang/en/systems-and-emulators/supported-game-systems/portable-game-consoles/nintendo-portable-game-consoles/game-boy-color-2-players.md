---
description: Nintendo
---

# Game Boy Color 2 players

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/gbc2players.svg" alt=""><figcaption></figcaption></figure>

</div>

This system is used to emulate the use of the link cable that allows two people to play two-player games on 2 Game Boys connected with the cable.

Only a limited list of titles are compatible.

{% embed url="https://en.wikipedia.org/wiki/List_of_multiplayer_Game_Boy_games" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: tgbdual</li><li>libretro: sameboy</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> gbc2players</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.gbc .zip .m3u .7z</td><td></td></tr></tbody></table>

## BIOS

Same BIOS as Game Boy Color system.

<table><thead><tr><th width="187">Bios file</th><th width="98">Folder</th><th>md5</th></tr></thead><tbody><tr><td>gb_bios.bin</td><td><code>\bios</code></td><td>32fbbd84168d3482956eb3c5051637f5</td></tr><tr><td>gbc_bios.bin</td><td><code>\bios</code></td><td>dbfce9db9deaa2567f6a84fde55f9680</td></tr></tbody></table>

## Controls

| RetroBat key                                                                       | Game Boy Color key |
| ---------------------------------------------------------------------------------- | ------------------ |
| START                                                                              | START              |
| SELECT / BACK                                                                      | SELECT             |
| D-PAD                                                                              | D-PAD              |
| Left analog stick                                                                  | D-PAD              |
| Right analog stick                                                                 |                    |
| ![A](<../../../../.gitbook/assets/image (25).png>)                                 | B                  |
| ![B](<../../../../.gitbook/assets/image (11).png>)                                 | A                  |
| <img src="../../../../.gitbook/assets/image (45).png" alt="" data-size="original"> |                    |
| <img src="../../../../.gitbook/assets/image (43).png" alt="" data-size="line">     |                    |
| L1                                                                                 |                    |
| R1                                                                                 |                    |
| L2                                                                                 |                    |
| R2                                                                                 |                    |
| L3                                                                                 |                    |
| R3                                                                                 |                    |

<div align="left">

<figure><img src="https://i.imgur.com/ptx8LTP.png" alt=""><figcaption></figcaption></figure>

</div>

## Specific system information

### How to link 2 different game cartridges (Pokemon)

Libretro: sameboy can simulate a cable link with 2 different cartridges. To do that, create a .m3u file that lists both game files to use (1 game file per line):



<div align="left">

<figure><img src="https://i.imgur.com/obmo6y9.png" alt=""><figcaption></figcaption></figure>

</div>

The 2 game files listed in the .m3u must exist in the `roms\gb2players` folder.
