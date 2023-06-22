---
description: Microsoft
---

# DOS

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/pc.svg" alt=""><figcaption></figcaption></figure>

</div>

Computer Operating System - Lifespan: 1981 - 2000

{% embed url="https://en.wikipedia.org/wiki/MS-DOS" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>Libretro: dosbox_pure</li><li>dosbox</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> dos</td></tr><tr><td><strong>File extension</strong></td><td>.dosbox .pc .dos .dosz .zip .m3u8 .bat .cmd</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

DOS games offered Keyboard and mouse controls.&#x20;

Use [pad2key ](../../../controllers/pad2key.md)to map Gamepad with Keyboard controls.

In some games there might be some controller prompts (there was an official PC Gamepad that could be plugged in the computer serial port).&#x20;

Blue = ![North button (X SNES)](https://wiki.batocera.org/\_media/wiki:north.png?w=20\&tok=be3bd1), Red = ![West button (Y SNES)](https://wiki.batocera.org/\_media/wiki:west.png?w=20\&tok=aee81f), Yellow = ![South button (B SNES)](https://wiki.batocera.org/\_media/wiki:south.png?w=20\&tok=c3eef3) and Green = ![East button (A SNES)](https://wiki.batocera.org/\_media/wiki:east.png?w=20\&tok=2276b1).

## Specific system information

### Zip games

DOSBox Pure can load games directly from **ZIP** files without the need to extract them.

### Load Games

This is the first screen that appears when loading a game. It offers a gamepad controllable list of all executable files for the loaded game. By pressing right an item can be selected as the default which will skip the menu on the next launch.

<div align="left">

<figure><img src="https://i.imgur.com/Ykgv1UU.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
If there is only a single executable, the menu will not show.
{% endhint %}

### Mount ZIP as A or D drive <a href="#mount-zip-as-a-or-d-drive" id="mount-zip-as-a-or-d-drive"></a>

If you have a ZIP file you want to load as a fake floppy disk or fake CD-ROM, there are multiple options, rename the file from `.ZIP` to e.g., `.D.ZIP` (to use the D: drive).

### Multi-disc

Use a `.m3u8` file, all files listed in it will be added to the disc swap hotkeys.&#x20;

The first image will automatically get mounted as the A: or D: drive depending on whether it is a CD or floppy disk image.
