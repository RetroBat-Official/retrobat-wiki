---
description: NEC
---

# NEC PC-9800

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/pc98-w.svg" media="(prefers-color-scheme: dark)"><img src="https://i.imgur.com/Cn9WzBZ.png" alt=""></picture><figcaption></figcaption></figure>

</div>

Computer - Release date: 1982

{% embed url="https://en.wikipedia.org/wiki/PC-9800_series" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: np2kai</li><li>libretro: nekop2</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> pc98</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.d98 .zip .98d .fdi .fdd .2hd .tfd .d88 .88d .hdm .xdf .dup .cmd .hdi .thd .nhd .hdd .hdn</td><td></td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="193">Bios file</th><th width="173.03610108303252">Folder</th><th>md5</th></tr></thead><tbody><tr><td>BIOS.ROM</td><td><code>\bios\np2kai</code></td><td>e246140dec5124c5e404869a84caefce</td></tr><tr><td>FONT.ROM</td><td><code>\bios\np2kai</code></td><td>2af6179d7de4893ea0b705c00e9a98d6</td></tr><tr><td>SOUND.ROM</td><td><code>\bios\np2kai</code></td><td>caf90f22197aed6f14c471c21e64658d</td></tr><tr><td>ITF.ROM</td><td><code>\bios\np2kai</code></td><td>e9fc3890963b12cf15d0a2eea5815b72</td></tr><tr><td>font.bmp</td><td><code>\bios\np2kai</code></td><td>7da1e5b7c482d4108d22a5b09631d967</td></tr></tbody></table>

## Controls

Use Pad2Key for this system if you need specific mapping, see the [Pad2Key ](../../../../controllers/pad2key.md)section of this Wiki.

<table><thead><tr><th width="311">Retrobat Button</th><th>PC98 key</th></tr></thead><tbody><tr><td>START</td><td>RETURN</td></tr><tr><td>SELECT</td><td>ESCAPE</td></tr><tr><td>D-PAD</td><td>Directions</td></tr><tr><td>Left analog stick</td><td></td></tr><tr><td>Right analog stick</td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/image (43).png" alt=""></td><td>Left CTRL</td></tr><tr><td><img src="../../../../.gitbook/assets/image (25).png" alt=""></td><td>Z</td></tr><tr><td><img src="../../../../.gitbook/assets/image (11).png" alt=""></td><td>X</td></tr><tr><td><img src="../../../../.gitbook/assets/image (45).png" alt=""></td><td>SPACE</td></tr><tr><td>L1</td><td>Backspace</td></tr><tr><td>R1</td><td>Right Shift</td></tr><tr><td>L2</td><td></td></tr><tr><td>R2</td><td>Open the NP2 menu</td></tr><tr><td>L3</td><td></td></tr><tr><td>R3</td><td></td></tr></tbody></table>

## Specific system information

### Multi-disc games

Use a .cmd file.\
\
Create a text file with the extension ".cmd", write the name of the core that will execute the game, then write the name of a boot disk (.hdm), the harddisk image (.hdi), and CloneCD image (.ccd/.img/.sub) like in the example below.

`Policenauts.cmd`

```
np2kai "Policenauts (User boot disk) [for Neko Project II].hdm" "Policenauts [for Neko Project II].hdi" "Policenauts.ccd"
```

Seems to works with "Neko Project II Kai" core, not with "Neko Project II" core

