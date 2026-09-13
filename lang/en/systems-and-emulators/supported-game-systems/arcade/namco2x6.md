---
description: Namco
---

# Namco 246/256

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/namco2x6.svg" alt="" width="563"><figcaption></figcaption></figure></div>

Playstation-based hardware arcade games emulator

{% embed url="https://en.wikipedia.org/wiki/Namco_System_246" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>pcsx2x6</li><li>play!</li><li>teknoparrot</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> namco2x6</td></tr><tr><td><strong>File extension</strong></td><td>.zip .m3u .acgame</td></tr></tbody></table>

## System Features

<table><thead><tr><th width="212">Retroachievements</th><th width="210">Netplay</th><th>Controller autoconfiguration</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>PCSX2X6: YES<br>PLAY: NO<br>TEKNOPARROT: YES</td></tr></tbody></table>

## Bios Information

<table><thead><tr><th width="214">BIOS file</th><th width="245">Folder</th><th>md5</th></tr></thead><tbody><tr><td>r27v1602f.7d</td><td><code>\bios\pcsx2\bios</code></td><td>​52CCA0058626569C7A9699838BAAB2D8</td></tr><tr><td>r27v1602f.8g</td><td><code>\bios\pcsx2\bios</code></td><td>A58676C6BD79229BDA967D07B4EC2E16</td></tr></tbody></table>

## Controls

### Play! controls

You can create your own .xml input profile file (for each game) and name it like the game file, RetroBat will then automatically load the file when loading the game.

Input profiles are stored in the following folder: `\emulators\play\Play Data Files\inputprofiles`:

<div align="left"><figure><img src="https://i.imgur.com/2F3itrK.png" alt=""><figcaption><p>Example of an Input Profile for Bloady Roar 3 game</p></figcaption></figure></div>

{% hint style="info" %}
If no input profile exists for the game, RetroBat will configure a default profile (Retrobat.xml) similar to a PS2 layout.
{% endhint %}

## Specific system information

#### Pcsx2x6: Adding games <a href="#pcsx2x6-ajouter-des-jeux" id="pcsx2x6-ajouter-des-jeux"></a>

Place the file with the .acgame extension in the `roms\namco2x6` folder, as well as the folder containing the game data :

<div align="left"><figure><img src="../../../.gitbook/assets/image (161).png" alt=""><figcaption><p>Example for Ace Driver 3</p></figcaption></figure></div>

**GAME FOLDER:** Each game folder must contain the following files:

* the game rom itself (.chd, .bin, .iso)
* an .elf file (can vary depending on the game : proverb.elf or boot.elf)
* A sram.bin file (this contains the saved data and configuration for the emulated arcade machine). If the file is missing, it will be generated at first launch.

<div align="left"><figure><img src="../../../.gitbook/assets/image (162).png" alt=""><figcaption><p>Example for the Ace Driver 3 folder</p></figcaption></figure></div>

**.ACGAME FILE:** the .acgame file contains the instructions for pcsx2x6 to run the particular game, you can check the content and edit it if necessary with a text editor such as Notepad++.&#x20;

The content of an .acgame file is :

**`[game]`**

This section contains the game's general information.

* `name` : name of the game displayed by pcsx2x6.
* `gameid` : unique game ID. This is mandatory.
* `platform` : emulated arcade platform : `246`, `256` or `super256`.

**`[data]`**

This section contains information about the game's files.

* `subdir` : name of the subfolder containing the game data.
* `elf` : file used to launch the game : `boot.elf` or `proverb.elf`.
* `dongle` : name of the file containing the game security data.
* `card` : (optional) can be used to load a secondary memory card (such as the conquest mode for SoulCalibur II).
* `mediasrc` : name of the file containing the game data (rom).
* `media` : specify the media type : `CD`, `DVD` or `HDD`.

<div align="left"><figure><img src="../../../.gitbook/assets/image (163).png" alt=""><figcaption><p>Example of an .acgame file for Ace Driver 3</p></figcaption></figure></div>

**.PS2 FILES :** .ps2 files are not memory cards, they are images of the game security dongle. They need to be placed in the  `saves\namco2x6\memcards` folder.

***

All these information can be found on the PCSX2X6 emulator website :

{% embed url="https://ps2homebrew-arcade.github.io/pcsx2x6/game_config/" %}

### Play!: Running games that do not have a ZIP file

For games without a .zip file, create a .m3u file named after the arcade profile name.

Arcade profile names can be found in the `emulators\play\arcadedefs` folder.

