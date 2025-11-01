---
description: Nintendo
---

# Switch

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/switch.svg" alt=""><figcaption></figcaption></figure></div>

Hybrid Game Console - Lifespan: 2017 - present

{% embed url="https://en.wikipedia.org/wiki/Nintendo_Switch" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>citron</li><li>ryujinx</li><li>eden</li><li>sudachi</li><li>suyu</li><li>yuzu</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> switch</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.nso .nro .nca .xci .nsp .kip</td><td></td></tr></tbody></table>

## Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>Ryujinx: YES<br>Eden: YES<br>Sudachi: YES<br>Citron: YES<br>Suyu: YES<br>Yuzu: YES</td></tr></tbody></table>

## Emulators

### Ryujinx

Copy Ryujinx emulator files in the `emulators\ryujinx` folder of your RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/KSvr9sk.png" alt=""><figcaption></figcaption></figure></div>

### Citron, Eden, Sudachi, Yuzu, Suyu

Copy emulator data in the `emulators\citron` (or eden, suyu, yuzu, sudachi) folder of your RetroBat installation, then create the "user" subfolder:

### Files location

<table><thead><tr><th width="276">Files</th><th>Path (relative to the RetroBat root folder)</th></tr></thead><tbody><tr><td>Emulator user content</td><td><strong>Ryujinx</strong>: saves\switch\ryujinx\portable<br><strong>Eden, Yuzu, Suyu, Sudachi, Citron:</strong> <br>emulators\&#x3C;emulator name>\user</td></tr><tr><td>Config file</td><td><strong>Ryujinx</strong>: saves\switch\ryujinx\portable\Config.json<br><strong>Eden, Yuzu, Suyu, Sudachi, Citron:</strong> <br>emulators\&#x3C;emulator name>\user\config\qt-config.ini</td></tr></tbody></table>

For Citron, Sudachi, Eden, Yuzu and Suyu emulators, SDMC, LOAD, NAND folders can be merged in the`saves\switch` folder of your RetroBat installation.

To merge, switch on the following option:

<div align="left"><figure><img src="https://i.imgur.com/tyMuoRl.png" alt=""><figcaption></figcaption></figure></div>

## BIOS

Switch firmware files and prod.keys need to be dumped from your console and placed in dedicated directories depending on the emulator:

### Ryujinx

Place prod.keys file in `\saves\switch\ryujinx\portable\system`

Install firmware directly in the emulator, using the "**Configure Ryujinx.bat**" file to run Ryujinx.

<div align="left"><figure><img src="https://i.imgur.com/CVXr1y7.png" alt=""><figcaption><p>Tools > Install Firmware</p></figcaption></figure></div>

{% hint style="danger" %}
This step is mandatory for Ryujinx to work properly with RetroBat.

If the "Configure Ryujinx.bat" does not exist in the `emulators\ryujinx` folder, you can find it in the `system\templates\ryujinx` folder and copy it in the emulator folder.
{% endhint %}

### Eden, Sudachi, Suyu, Yuzu and Citron

Place prod.keys file in `\emulators\`<mark style="color:purple;">`<emulator>`</mark>`\user\keys`

Place firmware .nca files in `\emulators\`<mark style="color:purple;">`<emulator>`</mark>`\user\nand\system\Contents\registered`

## Controls

{% hint style="info" %}
The following controllers can be autoconfigured from Retrobat to Switch emulators:

* XInput controllers
* Dualshock & DualSense controllers
* Nintendo Switch Pro controller
{% endhint %}

| RetroBat key                                                                       | Switch Key                     |
| ---------------------------------------------------------------------------------- | ------------------------------ |
| START                                                                              | +                              |
| SELECT / BACK                                                                      | -                              |
| D-PAD                                                                              | D-PAD                          |
| Left Analog Stick                                                                  | Left stick                     |
| Right Analog Stick                                                                 | Right stick                    |
| ![A](<../../../../.gitbook/assets/image (30).png>)                                 | <p>B<br>Or A when inverted</p> |
| ![B](<../../../../.gitbook/assets/image (16).png>)                                 | <p>A<br>Or B when inverted</p> |
| <img src="../../../../.gitbook/assets/image (50).png" alt="" data-size="original"> | <p>X<br>Or Y when inverted</p> |
| <img src="../../../../.gitbook/assets/image (48).png" alt="" data-size="line">     | <p>Y<br>Or X when inverted</p> |
| LB (L1)                                                                            | L                              |
| RB (R1)                                                                            | R                              |
| L2                                                                                 | ZL                             |
| R2                                                                                 | ZR                             |
| L3                                                                                 | Left Thumb                     |
| R3                                                                                 | Right Thumb                    |

Use the following option to invert face buttons (to match xbox controllers):

<div align="left"><figure><img src="https://i.imgur.com/tFOOo3r.png" alt=""><figcaption></figcaption></figure></div>

## Specific system information

### Installing game updates & DLC

Game updates can be installed both in Yuzu and Ryujinx. They are dumped from your Switch in the format of .nsp files.

#### Ryujinx

In Ryujinx Game list, right-click the game line and select **Manage Title Updates** or **Manage DLC**

<div align="left"><figure><img src="https://i.imgur.com/uRMjmAE.png" alt=""><figcaption></figcaption></figure></div>

The next screen will invite you to select your update or DLC .nsp file, search for it on your computer, add it and save.

<div align="left"><figure><img src="https://i.imgur.com/Vk2lwA3.png" alt=""><figcaption></figcaption></figure></div>

#### Eden, Citron, Sudachi, Suyu, Yuzu

Go to `Files > Install Files to NAND...`

<div align="left"><figure><img src="https://i.imgur.com/B6jQIqZ.png" alt=""><figcaption></figcaption></figure></div>

The next screen will invite you to search for your update or DLC .nsp file on your computer, just select it and save.
