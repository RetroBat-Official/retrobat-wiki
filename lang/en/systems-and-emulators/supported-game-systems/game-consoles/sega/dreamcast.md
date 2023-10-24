---
description: Sega
---

# Dreamcast

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/dreamcast-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/dreamcast.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Game Console - Lifespan: 1998 - 2001

{% embed url="https://en.wikipedia.org/wiki/Dreamcast" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>Libretro: flycast</li><li>flycast</li><li>redream</li><li>demul</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> dreamcast</td></tr><tr><td><strong>File extension</strong></td><td>.mds .mdf .cue .cdi .gdi .chd .m3u</td></tr></tbody></table>

## Features

| Retroachievements | NetPlay                      |
| ----------------- | ---------------------------- |
| YES               | YES (libretro: redream only) |

## Bios Information

<table><thead><tr><th width="160.55555555555557">bios file</th><th width="155">Folder</th><th>md5</th></tr></thead><tbody><tr><td>dc_boot.bin</td><td><code>\bios\dc</code></td><td>e10c53c2f8b90bab96ead2d368858623</td></tr><tr><td>dc_flash.bin</td><td><code>\bios\dc</code></td><td>0a93f7940c455905bea6e392dfde92a4</td></tr><tr><td>dc.zip</td><td><code>\bios\dc</code></td><td>See below (required for demul only)</td></tr></tbody></table>

{% hint style="info" %}
For Flycast standalone, BIOS file must be placed in `emulators\flycast\data` folder.
{% endhint %}

#### Content of BIOS file

```
dc.zip
- 1_01d_01.bin "E10C53C2F8B90BAB96EAD2D368858623"
- 1_01d_02.bin "A5C6A00818F97C5E3E91569EE22416DC"
- 1_004_01.bin "37C921EB47532CAE8FB70E5D987CE91C"
- 1_011_01.bin "EAFCA1EED2D7F76C487E940597C2A786"
```

## Controls

| Retrobat Button                                   | Dreamcast key |
| ------------------------------------------------- | ------------- |
| START                                             | START         |
| D-PAD                                             | D-PAD         |
| Left analog stick                                 | Analog stick  |
| Right analog stick                                |               |
| ![](<../../../../.gitbook/assets/image (43).png>) | X             |
| ![](<../../../../.gitbook/assets/image (25).png>) | A             |
| ![](<../../../../.gitbook/assets/image (11).png>) | B             |
| ![](<../../../../.gitbook/assets/image (45).png>) | Y             |
| L1                                                |               |
| R1                                                |               |
| L2                                                | L1            |
| R2                                                | R1            |
| L3                                                |               |
| R3                                                |               |

<div align="left">

<figure><img src="https://i.imgur.com/g71xmgZ.png" alt=""><figcaption></figcaption></figure>

</div>

## Specific system information

### Multi-disc

You can use a m3u file to manage multi-disc games.

For example for _Alone In The Dark_, if the ROM contains the following files:

<div align="left">

<figure><img src="https://i.imgur.com/LUmmLpf.png" alt=""><figcaption></figcaption></figure>

</div>

create a `Alone in the dark The new nightmare.m3u` text file with the following content and save it to the /roms/dreamcast folder:

<div align="left">

<figure><img src="https://i.imgur.com/9dQJhD9.png" alt=""><figcaption></figcaption></figure>

</div>

Retrobat will automatically detect the m3u file and hide the individual .gdi files from the Game List.

### Custom textures

Custom textures can be used with the flycast core.

The texture pack must be placed in the `\bios\dc\textures\` folder:

<div align="left">

<figure><img src="https://i.imgur.com/65bX2kT.png" alt=""><figcaption></figcaption></figure>

</div>

Then, enable **CUSTOM TEXTURES** in **ADVANCED SYSTEM OPTIONS** or in **ADVANCED GAME OPTIONS**.

<div align="left">

<figure><img src="https://i.imgur.com/ppkZ9bw.png" alt=""><figcaption><p>Enter the Dreamcast System View Options</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/qVMX2Ly.png" alt=""><figcaption><p>Select Visual Rendering</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/SbsPMz1.png" alt=""><figcaption><p>Set Custom Textures to YES</p></figcaption></figure>

</div>
