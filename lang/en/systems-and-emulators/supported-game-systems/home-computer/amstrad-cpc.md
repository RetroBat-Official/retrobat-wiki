---
description: Amstrad
---

# Amstrad CPC

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/amstradcpc-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/amstradcpc.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Computer - Lifespan: 1984 - 1990

{% embed url="https://en.wikipedia.org/wiki/Amstrad_CPC" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: cap32</li><li>libretro: crocods</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> amstradcpc</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.dsk .sna .tap .cdt .voc .m3u .zip .7z</td><td></td></tr></tbody></table>

## Features

| RetroAchievements | NetPlay |
| ----------------- | ------- |
| YES               | YES     |

## BIOS

No BIOS files required for Amstrad CPC.

## Controls

Cap32 & crocods cores allow you to choose between the following controller types:

* JOYSTICK
* KEYBOARD (Consider enabling Game Focus feature for keyboard games)
* LIGHTGUN (cap32 only)

| Retrobat Button                                | Amstrad CPC key |
| ---------------------------------------------- | --------------- |
| START                                          | RETURN          |
| SELECT                                         | SPARE           |
| D-PAD                                          | D-PAD           |
| Left analog stick                              | D-PAD           |
| Right analog stick                             |                 |
| ![](<../../../.gitbook/assets/image (43).png>) |                 |
| ![](<../../../.gitbook/assets/image (25).png>) | Fire 2          |
| ![](<../../../.gitbook/assets/image (11).png>) | Fire 1          |
| ![](<../../../.gitbook/assets/image (45).png>) |                 |
| L1                                             | cap32: CTRL     |
| R1                                             | cap32: INTRO    |
| L2                                             | cap32: F1       |
| R2                                             | cap32: F2       |
| L3                                             |                 |
| R3                                             |                 |

## Specific system information

### Force Cap32 core to use a specific command line when running a game

Cap32 libretro core offers an "autorun" fonctionnality that would automatically type the command line to execute the game in the Amstrad BIOS. However, in some cases for .dsk files, the command line might be incorrect.

To solve this issue, it is possible to use a .m3u file to force a different command line, proceed as follows:

Create a .m3u file with any text editor and specify:\
\- the command line to be executed\
\- the filename of your game

**Exemple:**

```
#COMMAND:RUN"COMMANDO.BIN
Commando (Europe).dsk
```

With this file, RetroBat will inform the emulator to run the "Commando (Europe).dsk" file and to write the command line `RUN"COMMANDO.BIN`

Once the .m3u is created, you can run it from within RetroBat with the Cap32 core.
