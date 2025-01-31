---
description: Namco
---

# Namco 246/256

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/namco2x6.svg" alt="" width="563"><figcaption></figcaption></figure></div>

Playstation-based hardware arcade games emulator

{% embed url="https://en.wikipedia.org/wiki/Namco_System_246" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>play</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> namco2x6</td></tr><tr><td><strong>File extension</strong></td><td>.zip .m3u</td></tr></tbody></table>

The list of compatible games can be found in the following folder: `\emulators\play\arcadedefs`

{% hint style="danger" %}
Do not rename zip files, the name of the file must be exactly the name expected by the emulator.
{% endhint %}

## System Features

<table><thead><tr><th width="212">Retroachievements</th><th width="210">Netplay</th><th>Controller autoconfiguration</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>YES</td></tr></tbody></table>

## Bios Information

No BIOS required.

## Controls

You can create your own .xml input profile file (for each game) and name it like the game file, RetroBat will then automatically load the file when loading the game.

Input profiles are stored in the following folder: `\emulators\play\Play Data Files\inputprofiles`:

<div align="left"><figure><img src="https://i.imgur.com/2F3itrK.png" alt=""><figcaption><p>Example of an Input Profile for Bloady Roar 3 game</p></figcaption></figure></div>

{% hint style="info" %}
If no input profile exists for the game, RetroBat will configure a default profile (Retrobat.xml) similar to a PS2 layout.
{% endhint %}

## Specific system information

### Running games that do not have a ZIP file

For games without a .zip file, create a .m3u file named after the arcade profile name.

Arcade profile names can be found in the `emulators\play\arcadedefs` folder.

