---
description: Nintendo
---

# WiiU

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/wiiu-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/wiiu.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Hybrid Game Console - Lifespan: 2012 - 2017

{% embed url="https://en.wikipedia.org/wiki/Wii_U" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>cemu</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> wiiu</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.iso .rpx .wud .wux .wua .m3u</td><td></td></tr></tbody></table>

## Features

| Retroachievements | NetPlay |
| ----------------- | ------- |
| NO                | NO      |

## BIOS

There is no BIOS files needed to run games, however, when using .wud or .wux game files, it is necessary to have a keys.txt file in the emulator folder with the right game keys.

The Game keys can be dumped from your WiiU console, see [CEMU guide](https://wiki.cemu.info/wiki/Obtaining\_Keys\_for\_Keys.txt) for more information.

## Controls

{% hint style="info" %}
The following controllers can be autoconfigured from Retrobat to Cemu:

* XInput controllers
* Dualshock & DualSense controllers
* Nintendo Switch Pro controller
{% endhint %}

| RetroBat key                                                                       | WiiU Key    |
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

### Motion controls

Some Games do require motion control to play in some levels (e.g. Zelda Breath of The Wild contains dungeons which can only be beaten using motion).

There are several options to manage motion control, [CEMU wiki](https://wiki.cemu.info/wiki/Motion\_controls) has great documentation to cover motion control.

DualSense and Switch Pro controllers are tested options.

{% hint style="info" %}
If you own a controller that supports motion control, you can activate motion controls in the Advanced system options or advanced game options.
{% endhint %}

## Specific system information

### Adding Games in Loadiine format

The best way to add WiiU games is to use the format known as "Bootloader" format. This is the format of games dumped from your console with Dumpling tool.

This consists of a game folder with 3 subfolders

<div align="left">

<figure><img src="https://i.imgur.com/CIYaICX.png" alt=""><figcaption><p>Example of dumped Zelda game</p></figcaption></figure>

</div>

There are 2 options to add these games in Retrobat

#### Install the game in Cemu and use m3u file

This method will simulate the installation of the game in the NAND of the WiiU.

From the Retrobat Game View, open the CEMU emulator



<div align="left">

<figure><img src="https://i.imgur.com/rdJUos9.png" alt=""><figcaption><p>File > Install</p></figcaption></figure>

</div>

Navigate to the \meta folder of your dumped game directory and install the meta.xml file

<div align="left">

<figure><img src="https://i.imgur.com/C1KGhKQ.png" alt=""><figcaption></figcaption></figure>

</div>

Wait for the installation to finish and you will see the game added to Cemu

<div align="left">

<figure><img src="https://i.imgur.com/rG2IJvR.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/9ygBgJP.png" alt=""><figcaption></figcaption></figure>

</div>

Right-click on the Game and select **Game directory**

<div align="left">

<figure><img src="https://i.imgur.com/6ALGNnR.png" alt=""><figcaption></figcaption></figure>

</div>

This will show you the path of the game executable .rpx file

<div align="left">

<figure><img src="https://i.imgur.com/EN9JEKf.png" alt=""><figcaption></figcaption></figure>

</div>

Exit Cemu and open you `\roms\wiiu` folder and create a `zelda breath of the wild.m3u` file with the following content

`\..\..\emulators\cemu\mlc01\usr\title\`<mark style="color:red;">`<path to the game>`</mark>`\`<mark style="color:red;">`*`</mark>`.rpx`

For example for Zelda Breath of the Wild:

<div align="left">

<figure><img src="https://i.imgur.com/DjHV0Gt.png" alt=""><figcaption></figcaption></figure>

</div>

The game will now be available in Retrobat for scraping and playing.

#### Place the Game folder in the roms directory

This method will simulate the presence of a WiiU cartridge.&#x20;

Place the game folder in the `\roms\wiiu` folder

<div align="left">

<figure><img src="https://i.imgur.com/8BsrI9F.png" alt=""><figcaption></figcaption></figure>

</div>

The game will now be available in Retrobat for scraping and playing.

Retrobat will detect the **.rpx** file in the `\code` folder

<div align="left">

<figure><img src="https://i.imgur.com/iSQdk4o.png" alt=""><figcaption></figcaption></figure>

</div>

The Screenscraper service will recognize U-King as Zelda Breath of the Wild

<div align="left">

<figure><img src="https://i.imgur.com/9srVWOF.png" alt=""><figcaption></figcaption></figure>

</div>

### Game Updates & DLC

Updates & DLC must be installed in the Cemu emulator directory using the install title, update or DLC option, they come in the same structure as the game itself

Open Cemu and choose **install game title, update or DLC**

<div align="left">

<figure><img src="https://i.imgur.com/Y53KGT4.png" alt=""><figcaption><p>Select the install option</p></figcaption></figure>

</div>

Navigate to the \meta folder of your dumped DLC or Update directory and install the meta.xml file

<div align="left">

<figure><img src="https://i.imgur.com/Y6adbtz.png" alt=""><figcaption><p>search for the meta.xml file in the meta folder</p></figcaption></figure>

</div>

Wait until the installation finishes

<div align="left">

<figure><img src="https://i.imgur.com/8U7YvAk.png" alt=""><figcaption></figcaption></figure>

</div>

You should now see the Update or DLC information in the gamelist

<div align="left">

<figure><img src="https://i.imgur.com/OY3g3cd.png" alt=""><figcaption></figcaption></figure>

</div>

### Graphic packs

Cemu emulator uses Graphic Packs to enhance games graphics but also to fix bugs in some games.

Graphic Packs are not managed automatically from RetroBat and need to be enabled in the emulator, once enabled, they will be used when launching the game from RetroBat.

Proceed as follows to enable Graphic Packs.

* Open CEMU and select "Graphic Packs":

<div align="left">

<figure><img src="https://i.imgur.com/6706fCT.png" alt=""><figcaption></figcaption></figure>

</div>

* Click the "Download latest community graphic packs" in the bottom left corner of the screen:

<div align="left">

<figure><img src="https://i.imgur.com/Y98rMBK.png" alt=""><figcaption></figcaption></figure>

</div>

This will automatically download the graphic packs for the games you own

* Check the list of items available and enable the ones required for the game (or the ones you want to activate)

<div align="left">

<figure><img src="https://i.imgur.com/CKKBWGK.png" alt=""><figcaption></figcaption></figure>

</div>

In this example, the option ticked is mandatory to avoid a crash after the title screen in the game "New Super Mario Bros WiiU"

* Once done: quit the emulator

The settings will automatically be saved

{% hint style="info" %}
You can check the specific requirements on the CEMU compatibility wiki:

[https://compat.cemu.info/](https://compat.cemu.info/)
{% endhint %}

