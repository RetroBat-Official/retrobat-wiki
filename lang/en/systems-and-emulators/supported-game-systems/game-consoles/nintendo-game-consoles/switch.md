---
description: Nintendo
---

# Switch

<div align="left">

<figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/switch.svg" alt=""><figcaption></figcaption></figure>

</div>

Hybrid Game Console - Lifespan: 2017 - present

{% embed url="https://en.wikipedia.org/wiki/Nintendo_Switch" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>yuzu</li><li>yuzu early access</li><li>ryujinx</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> switch</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.nso .nro .nca .xci .nsp .kip</td><td></td></tr></tbody></table>

{% hint style="info" %}
You need to be a Yuzu Patreon to use Yuzu Early Access.
{% endhint %}

## Features

| Retroachievements | NetPlay |
| ----------------- | ------- |
| NO                | NO      |

## BIOS

Switch firmware files and prod.keys need to be dumped from your console and placed in dedicated directories in the emulator folders:

### Yuzu and Yuzu Early Access

Place prod.keys file in `\emulators\yuzu\user\keys`

Place firmware .nca files in `\emulators\yuzu\user\nand\system\Contents\registered`

### Ryujinx

Place prod.keys file in `\emulators\ryujinx\portable\system`

Install firmware directly in the emulator

<div align="left">

<figure><img src="https://i.imgur.com/CVXr1y7.png" alt=""><figcaption><p>Tools > Install Firmware</p></figcaption></figure>

</div>

## Controls

{% hint style="info" %}
The following controllers can be autoconfigured from Retrobat to Yuzu/Ryujinx:

* XInput controllers
* Dualshock & DualSense controllers
* Nintendo Switch Pro controller
{% endhint %}

| RetroBat key                                                                       | Switch Key  |
| ---------------------------------------------------------------------------------- | ----------- |
| START                                                                              | +           |
| SELECT / BACK                                                                      | -           |
| D-PAD                                                                              | D-PAD       |
| Left Analog Stick                                                                  | Left stick  |
| Right Analog Stick                                                                 | Right stick |
| ![A](<../../../../.gitbook/assets/image (25).png>)                                 | B           |
| ![B](<../../../../.gitbook/assets/image (11).png>)                                 | A           |
| <img src="../../../../.gitbook/assets/image (45).png" alt="" data-size="original"> | X           |
| <img src="../../../../.gitbook/assets/image (43).png" alt="" data-size="line">     | Y           |
| LB (L1)                                                                            | L           |
| RB (R1)                                                                            | R           |
| L2                                                                                 | ZL          |
| R2                                                                                 | ZR          |
| L3                                                                                 | Left Thumb  |
| R3                                                                                 | Right Thumb |

{% hint style="info" %}
For Ryujinx, the controller is done directly in the emulator.
{% endhint %}

## Specific system information

All information related to emulator setup, install guide, game dumping guides can be found on the emulator websites.

{% embed url="https://yuzu-emu.org/help/quickstart/" %}

{% embed url="https://github.com/Ryujinx/Ryujinx/wiki/Ryujinx-Setup-&-Configuration-Guide" %}

### How-to install Yuzu

To install Yuzu, follow the guide on the [Yuzu website](https://yuzu-emu.org/help/quickstart/#downloading-and-installing-yuzu).

Yuzu will be installed by default in the appdata folder on your computer:

* `Appdata\local\yuzu` for yuzu program executable files
* `Appdata\roaming\yuzu` for yuzu user data (game saves, settings...)

#### Program executable files

<div align="left">

<figure><img src="https://i.imgur.com/P8Pi1Ut.png" alt=""><figcaption></figcaption></figure>

</div>

The content of the `yuzu-windows-msvc` folder must be copied to the `\emulators\yuzu` directory in your Retrobat folder.

For Early Access, copy the content of the `yuzu-windows-msvc-early-access` must be copied to the `\emulators\yuzu-early-access` directory in your Retrobat folder.

<div align="left">

<figure><img src="https://i.imgur.com/fq2gxNH.png" alt=""><figcaption></figcaption></figure>

</div>

#### User data

<div align="left">

<figure><img src="https://i.imgur.com/CQhfYCR.png" alt=""><figcaption></figcaption></figure>

</div>

User data must be copied to the `\emulators\yuzu\user` folder of your RetroBat installation.

### Installing game updates

Game updates can be installed both in Yuzu and Ryujinx. They are dumped from your Switch in the format of .nsp files.

#### Yuzu

In Yuzu, go to `Files > Install Files to NAND...`

<div align="left">

<figure><img src="https://i.imgur.com/B6jQIqZ.png" alt=""><figcaption></figcaption></figure>

</div>

The next screen will invite you to search for your update or DLC .nsp file on your computer, just select it and save.

#### Ryujinx

In Ryujinx Game list, right-click the game line and select **Manage Title Updates** or **Manage DLC**

<div align="left">

<figure><img src="https://i.imgur.com/uRMjmAE.png" alt=""><figcaption></figcaption></figure>

</div>

The next screen will invite you to select your update or DLC .nsp file, search for it on your computer, add it and save.
