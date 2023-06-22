---
description: ScummVM Team
---

# ScummVM

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/scummvm.svg" alt=""><figcaption></figcaption></figure>

</div>

Emulator - Creation year: 2001

{% embed url="https://en.wikipedia.org/wiki/ScummVM" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>Libretro: scummvm</li><li>scummvm</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> scummvm</td></tr><tr><td><strong>File extension</strong></td><td>.scummvm .7z .zip .rar .squashfs</td></tr></tbody></table>

## Features

| Retroachievements | NetPlay |
| ----------------- | ------- |
| NO                | NO      |

## BIOS

<table><thead><tr><th width="221">BIOS file</th><th width="177">Folder</th><th>md5</th></tr></thead><tbody><tr><td>MT32_CONTROL.ROM</td><td><code>\bios\scummvm\extra</code></td><td>5626206284b22c2734f3e9efefcd2675</td></tr><tr><td>MT32_PCM.ROM</td><td><code>\bios\scummvm\extra</code></td><td>89e42e386e82e0cacb4a2704a03706ca</td></tr></tbody></table>

## Controls

Most of the games are point-and-click games designed to be played with a mouse. If you don't have a mouse, the left analog stick can be used too.

Manual controls can be configured by adding a [pad2key ](../../../controllers/pad2key.md)profile for the game.

## System Features

### Adding games

Scummvm games must be in separate folders, in the `\roms\scummvm` folder.

<div align="left">

<figure><img src="https://i.imgur.com/qfDZ5Np.png" alt=""><figcaption></figcaption></figure>

</div>

In each games folder, create a .txt file with the name of the game, for example **Full Throttle.txt** for Full Throttle.

<div align="left">

<figure><img src="https://i.imgur.com/k4GhSoC.png" alt=""><figcaption></figcaption></figure>

</div>

In the .txt file, enter the ScummVM **game shortname**, refer to [https://www.scummvm.org/compatibility/](https://www.scummvm.org/compatibility/) to get the correct shortname.

{% hint style="info" %}
The shortname contains the engine followed by the game short ID, separated by :
{% endhint %}

Finally, rename the \*._txt_ files into \*._scummvm_ file, for example:\
\
Full Throttle.**txt**  **==>** Full Throttle.**scummvm**



### Running a specific version of a game with dedicated per-game options

Some games have been issued on multiple platforms, SCUMMVM is able to run most of these versions.

If you own multiple versions of the same game and want to be able to select the version to run, you will first need to add the games to SCUMMVM directly within the emulator.

To do so, proceed as follows.

* Open SCUMMVM and select "add games":

<div align="left">

<figure><img src="https://i.imgur.com/iJoG99n.png" alt=""><figcaption></figcaption></figure>

</div>

Locate your game folder.

* Pick the version of the game to be added (if multiple versions exist in your game file):

<div align="left">

<figure><img src="https://i.imgur.com/AOzAJp2.png" alt=""><figcaption></figcaption></figure>

</div>

* Define the game short ID and the options to enable when running this game

<div align="left">

<figure><img src="https://i.imgur.com/SSQCrt7.png" alt=""><figcaption></figcaption></figure>

</div>

Click OK once finished

The game is now added to SCUMMVM:

<div align="left">

<figure><img src="https://i.imgur.com/Ok0JkMy.png" alt=""><figcaption></figcaption></figure>

</div>

* Create a dedicated .scummvm file to run this specific version of the game:

<div align="left">

<figure><img src="https://i.imgur.com/nCNTake.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/5DiPExS.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="warning" %}
The name inside the .scummvm file must match the short ID specified when adding the game in the emulator.
{% endhint %}

* In RetroBat, both versions will now be available

<div align="left">

<figure><img src="https://i.imgur.com/OTcJf0h.png" alt=""><figcaption></figcaption></figure>

</div>

Note that you can check all installed games and their short-ID in the scummvm.ini file, this file is located in:

* \emulators\scummvm folder (for SCUMMVM standalone)
* \bios folder for libretro:scummvm

<div align="left">

<figure><img src="https://i.imgur.com/YUsciw5.png" alt=""><figcaption></figcaption></figure>

</div>
