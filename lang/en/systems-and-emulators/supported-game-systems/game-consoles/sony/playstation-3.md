---
description: Sony
---

# Playstation 3

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/ps3-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/ps3.svg" alt=""></picture><figcaption></figcaption></figure></div>

Game Console - Lifespan: 2006 - 2017

{% embed url="https://en.wikipedia.org/wiki/PlayStation_3" %}

## Information

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>rpcs3</li></ul></td></tr><tr><td><strong>File folder</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> ps3</td></tr><tr><td><strong>File extension</strong></td><td>.m3u .lnk .ps3 .iso .7z .zip .rar .squashfs</td></tr></tbody></table>

## System Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>YES</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="187">BIOS file</th><th width="109">Folder</th><th>md5</th></tr></thead><tbody><tr><td>PS3UPDAT.PUP</td><td><code>\bios</code></td><td>3694eb3fb8d9915c112e6ab41a60c69f</td></tr></tbody></table>

#### Automatic firmware installation

The first time the rpcs3 emulator is launched, if the PS3UPDAT.PUP file is present in you \bios folder, the emulator will automatically prompt to install the firmware, once the firmware installed you can close and relaunch the game.

<div align="left"><figure><img src="https://i.imgur.com/1ovzizA.png" alt=""><figcaption></figcaption></figure></div>

#### Manual firmware installation

Run rpcs3.exe file in `\emulators\rpcs3` folder and **install firmware**

<div align="left"><figure><img src="https://i.imgur.com/18HE0DC.png" alt=""><figcaption></figcaption></figure></div>

Select the **PS3UPDAT.PUP** and run firmware installation.

Firmware will appear at the bottom of the emulator:

<div align="left"><figure><img src="https://i.imgur.com/JFjxamH.png" alt=""><figcaption></figcaption></figure></div>

## Controls

{% hint style="info" %}
The following controllers can be autoconfigured from Retrobat to RPCS3:

* XInput controllers
* Dualshock & DualSense controllers
* Nintendo Switch Pro controller
{% endhint %}

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/psx.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Pressure sensitivity

RPCS3 can manage pressure sensitivity only with a genuine Dualshock (or sisaxis) controller.

You need to install DsHidMini drivers to handle PS3 controller, as described here:

{% embed url="https://wiki.rpcs3.net/index.php?title=Help:Controller_Configuration#Using_Nefarius'_DsHidMini" %}

## System Features

### File locations

<table><thead><tr><th width="254">Data</th><th>Path (relative to retrobat root path)</th></tr></thead><tbody><tr><td>dev_hdd0</td><td>saves\ps3\rpcs3\dev_hdd0</td></tr><tr><td>config file</td><td>emulators\rpcs3\config.yml</td></tr><tr><td>gui config file</td><td>emulators\rpcs3\GuiConfigs\CurrentSettings.ini</td></tr><tr><td>Controller configuration file</td><td>emulators\rpcs3\config\input_configs\global\Default.yml</td></tr></tbody></table>

{% hint style="info" %}
To use the `emulators\rpcs3\dev_hdd0` folder instead of the one in "saves", delete the `saves\ps3\rpcs3`folder. This will tell RetroBat to keep dev\_hdd0 inside emulator folder.
{% endhint %}

### Adding PS3 games

There are 2 types of PS3 games available: Blu-Ray discs and PlayStation Network titles (PSN):

* Title IDs that start with a B are Blu-Ray disc titles.
* Title IDs that start with a N are PSN titles.

<div align="left"><figure><img src="https://i.imgur.com/EsmEoB4.png" alt=""><figcaption></figcaption></figure></div>

Blu-ray disc titles can be copied directly in the  `\roms\ps3` folder while PSN titles need to be added in the `\saves\ps3\rpcs3\dev_hdd0\game` folder of your RetroBat installation.

{% hint style="danger" %}
PSN titles need to be decrypted to be used with RPCS3 emulator.
{% endhint %}

#### Adding Blu-ray disc title

Simply copy the game folder to the `\roms\ps3` folder of your RetroBat installation and rename the folder with a .ps3 extension:

<div align="left"><figure><img src="https://i.imgur.com/E98BUs9.png" alt=""><figcaption></figcaption></figure></div>

The game will directly be available in RetroBat.

#### Adding PSN titles - option 1

\
Once the game has been added to the emulator from the "**Install package**" or/and "**Add games**" menu and the game is working succesfully from the emulator, create a m3u file in the `\roms\ps3` folder that points to the **EBOOT.BIN** file of the game in the `\saves\ps3\rpcs3\dev_hdd0\game` game folder:



<div align="left"><figure><img src="https://i.imgur.com/qV3GMuC.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/LmL6NUh.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
BATGUI tool offers an automatic m3u creation tool. Refer to the [BATGUI ](../../../../advanced-features/batgui.md)section of the wiki.
{% endhint %}

#### Adding PSN titles - option 2

Create a m3u file and place it in the `\roms\ps3` folder.

The m3u file must contain "GAMEID:" followed by the game ID :

<div align="left"><figure><img src="https://i.imgur.com/DanYmrt.png" alt=""><figcaption></figcaption></figure></div>

The game ID can be found in the emulator game list:

<div align="left"><figure><img src="https://i.imgur.com/2dAJlIN.png" alt=""><figcaption></figcaption></figure></div>

### Use emulator game configuration

By default, RetroBat runs games with the RetroBat features defined within RetroBat advanced options menu, thus ignoring any game specific configuration performed directly in RPCS3 emulator.

If you want RetroBat to use a specific game configuration saved directly in rpcs3, enable the following option in RetroBat advanced options: "**USE CUSTOM CONFIG**"

<div align="left"><figure><img src="https://i.imgur.com/8PSzWko.png" alt=""><figcaption></figcaption></figure></div>
