---
description: Microsoft
---

# Xbox 360

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/xbox360.svg" alt=""><figcaption></figcaption></figure>

</div>

Game Console - Lifespan: 2005 - 2016

{% embed url="https://en.wikipedia.org/wiki/Xbox_360" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>xenia</li><li>xenia-canary</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> xbox360</td></tr><tr><td><strong>File extension</strong></td><td>.iso .xex .xcp .zar .m3u .xbox360</td></tr></tbody></table>

## System Features

<table><thead><tr><th width="245">Retroachievements</th><th width="200">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>NO</td></tr></tbody></table>

## Bios Information

No specific BIOS requirements to play Xbox 360 games on xenia / xenia-canary emulators.

## Controls

Xenia does not offer any manual configuration of controls.

From Retrobat System Options you can select the type of controller to use, select:

* XBOX CONTROLLER for Xbox Controllers post Xbox 360 models
* KEYBOARD for Keyboard
* OTHER for all other type of controllers (NINTENDO, DualShocks, etc.)

## Specific system information

### Content folders

<table><thead><tr><th width="254">Data</th><th>Path (relative to retrobat root path)</th></tr></thead><tbody><tr><td>Content path</td><td>saves\xbox360\xenia</td></tr></tbody></table>

### Adding XBLA (Xbox Live Arcade) games

Xbox360 **XBLA** games (**XB**ox **L**ive **A**rcade) are presented in the form of a succession of several folders, which end in a file that has no extension.

For example for _Banjo Tooie_ game, the filepath is the following:

**\Banjo Tooie\58410955\000D0000\ABB9CAB336175357D09F2D922735D23C62F90DDD**

For Retrobat to be able to launch the game, you must create a **\*.m3u** file to be placed at the root of the `\roms\xbox360` folder.

<div align="left">

<figure><img src="https://i.imgur.com/tfzS8Rt.png" alt=""><figcaption><p>Example for Banjo Tooie</p></figcaption></figure>

</div>

The content of the .m3u file is the following:

```
\Banjo Tooie\58410955\000D0000\ABB9CAB336175357D09F2D922735D23C62F90DDD
```

{% hint style="info" %}
BATGUI tool offers an automatic m3u creation tool. Refer to the [BATGUI ](../../../../advanced-features/batgui.md)section of the wiki.
{% endhint %}

### Xenia Manager

RetroBat allows running the Xenia-Manager, to do that you need to download the Xenia-Manager from [RetroBat's content manager](../../../../advanced-features/updates-and-content-download.md#download-content):

<div align="left">

<figure><img src="https://i.imgur.com/NftT8E2.png" alt=""><figcaption></figcaption></figure>

</div>

Once downloaded, refresh the gamelist, now Xenia Manager is available from the RetroBat menu:

<div align="left">

<figure><img src="https://i.imgur.com/G4xuhPy.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="warning" %}
Do not use another version of Xenia-Manager fournie as the one provided by RetroBat is the only one with the right paths to the xenia emulators.

If you install it outside of RetroBat, the emulators will be in a subpath of the manager and will not work with RetroBat.
{% endhint %}
