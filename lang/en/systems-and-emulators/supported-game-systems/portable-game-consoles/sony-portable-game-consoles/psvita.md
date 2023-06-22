---
description: Sony
---

# PlayStation Vita

<div align="left">

<figure><img src="https://i.imgur.com/as0rgjr.png" alt=""><figcaption></figcaption></figure>

</div>

Portable Game Console - Lifespan: 2011 - 2019

{% embed url="https://en.wikipedia.org/wiki/PlayStation_Vita" %}

## Features

| RetroAchievements | NetPlay |
| ----------------- | ------- |
| NO                | NO      |

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>vita3k</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> psvita</td></tr><tr><td><strong>File extension</strong></td><td>.m3u .psvita .vpk</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="193">Bios file</th><th width="142.03610108303252">Folder</th><th>md5</th></tr></thead><tbody><tr><td>PSP2UPDAT.PUP</td><td><code>\bios</code></td><td>8B5F60B56C3DA8365B973DBA570C53A5</td></tr><tr><td>PSVUPDAT.PUP</td><td><code>\bios</code></td><td>F2C7B12FE85496EC88A0391B514D6E3B</td></tr></tbody></table>

## Controls

Vita3K auto-detects connected controllers, there is no configuration required.

## System Features

### Installation & first setup

Use Retrobat Menu to download Vita3k or download the latest build of Vita3K emulator on the vita3k website : [https://vita3k.org/#download](https://vita3k.org/#download)

{% hint style="warning" %}
Do not run directly a game without installing from RetroBat menu first, as you will not be able to install firmware files.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/k9c9vpN.png" alt=""><figcaption></figcaption></figure>

</div>

Upon first startup, the emulator will need to be setup, first step is to select the language:

<div align="left">

<figure><img src="https://i.imgur.com/UiqGo28.png" alt=""><figcaption></figcaption></figure>

</div>

**Very important step**, set the pref-path to the `\emulators\vita3k` folder of your RetroBat installation:

<div align="left">

<figure><img src="https://i.imgur.com/e5JxlMn.png" alt=""><figcaption></figcaption></figure>

</div>

Download both _Firmware_ and _Font Package_ files on the Sony website and install them with the **INSTALL FIRMWARE FILE** button:

<div align="left">

<figure><img src="https://i.imgur.com/TecEwYu.png" alt=""><figcaption></figcaption></figure>

</div>

Installed status will change to V:

<div align="left">

<figure><img src="https://i.imgur.com/JmQbJpH.png" alt=""><figcaption></figcaption></figure>

</div>

Click the "NEXT" button until the end of the configuration:

<div align="left">

<figure><img src="https://i.imgur.com/oJgHNvm.png" alt=""><figcaption></figcaption></figure>

</div>

CONGRATULATIONS: you have succesfully initialised Vita3k emulator:

<div align="left">

<figure><img src="https://i.imgur.com/9NmozWv.png" alt=""><figcaption></figcaption></figure>

</div>

### Adding games

PS Vita games first have to be installed within the emulator, a more detailed guide can be read on the Vita3K website: [https://vita3k.org/quickstart.html](https://vita3k.org/quickstart.html)

Vita3K currently supports .pkg, NoNpDrm, FAGDec, or manually decrypted games.&#x20;

2 cases need to be distinguished:

1. The game is already installed in vita3k
2. The game is in your roms\psvita folder and is not yet installed in vita3k emulator

{% hint style="info" %}
Games are installed in the `emulators\vita3k\ux0\app` folder of your RetroBat installation.
{% endhint %}

#### Case 1 : game is already installed in vita3k

Create a .m3u file in the `\roms\psvita` folder of your RetroBat installation with game name:

<div align="left">

<figure><img src="https://i.imgur.com/tfILs19.png" alt=""><figcaption></figcaption></figure>

</div>

Inside the file, copy the **Title ID** of the game and save:

<div align="left">

<figure><img src="https://i.imgur.com/Fs8a98E.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
The title ID can be retrieved by running directly the Vita3k emulator.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/edf1nck.png" alt=""><figcaption></figcaption></figure>

</div>

#### Case 2 : game is in your roms folder and not yet installed in the emulator

RetroBat will automatically take care of the installation when you run the game for the first time, provided that the games are in the correct format.



2 formats are accepted and will allow automatic installation:

* game folders
* .vpk packages

{% hint style="warning" %}
It is mandatory that your .psvita folder name or .vpk filename contains the gameID between brackets as illustrated in the examples below, else the installation will not work.
{% endhint %}

If you are using a game folder, the folder must be renamed with ".psvita" at then end, also ensure that there is a eboot.bin directly inside the folder. Here is an example of a correct structure:

<div align="left">

<figure><img src="https://i.imgur.com/Anjm21x.png" alt=""><figcaption></figcaption></figure>

</div>

If you are using a .vpk file, just be sure that the file is correctly named with the gameID between brackets:

```
Street fighter [PCSE00005].vpk
```

When running the game for the first time, Retrobat will automatically install it inside the emulator, wait until the operation finishes (this might take some time):

<div align="left">

<figure><img src="https://i.imgur.com/bYSh81f.png" alt=""><figcaption></figcaption></figure>

</div>

