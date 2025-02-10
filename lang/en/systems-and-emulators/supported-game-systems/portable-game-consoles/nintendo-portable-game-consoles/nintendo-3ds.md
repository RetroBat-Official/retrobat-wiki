---
description: Nintendo
---

# Nintendo 3DS

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/3ds-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/3ds.svg" alt="" width="563"></picture><figcaption></figcaption></figure></div>

Portable Game Console - Lifespan: 2011 - 2020

{% embed url="https://en.wikipedia.org/wiki/Nintendo_3DS" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>citra</li><li>lime3ds</li><li>mandarine</li><li>libretro-citra</li><li>bizhawk: encore</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> 3ds</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.3ds .3dsx .elf .axf .cci .cxi .app .m3u .zip .7z .squashfs</td><td></td></tr></tbody></table>

## System Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>NO</td><td>NO</td><td>Citra: YES<br>Lime3DS: YES<br>Mandarine: YES<br>lr-citra: YES<br>BizHawk: YES</td></tr></tbody></table>

## BIOS

No BIOS required.

## Controls

{% hint style="info" %}
The following controllers can be autoconfigured from RetroBat in lime3ds/citra/mandarine standalone:

* XInput controllers
* Dualshock 4 and Dualsense controllers
* Nintendo Switch Pro controller
{% endhint %}

{% hint style="info" %}
The 3DS has a touchpad that is difficult to emulate, the best way to use it is with a mouse connected.

With some emulators, it is possible to use the right joystick for the touchpad screen.
{% endhint %}

### Standard control layout

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

The following option can be used to invert face buttons to match XBOX button names:

<div align="left"><figure><img src="https://i.imgur.com/IKTTaQo.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_revert.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Touchscreen Management:

Depending on the emulator, the options hereunder can be used to simulate touchscreen movement with the right analog stick.

#### Citra, Lime3DS and Mandarine

Use the following option:

<div align="left"><figure><img src="https://i.imgur.com/uAWxiGx.png" alt=""><figcaption></figcaption></figure></div>

| Option                       | Control layout                                                                                                                                        |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Without face button inverted | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick.png?raw=true" alt="" data-size="original">        |
| With face button inverted    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick_revert.png?raw=true" alt="" data-size="original"> |

#### Libretro-citra & BizHawk

Use the following option:

<div align="left"><figure><img src="https://i.imgur.com/MchmbEh.png" alt=""><figcaption></figcaption></figure></div>

| Option                                                   | Control layout                                                                                                                                        |
| -------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>C-STICK AND TOUCHSCREEN POINTER<br>(no inversion)</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick.png?raw=true" alt="" data-size="original">        |
| <p>C-STICK AND TOUCHSCREEN POINTER<br>(inversion)</p>    | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_cstick_revert.png?raw=true" alt="" data-size="original"> |
| <p>TOUCHSCREEN POINTER<br>(no inversion)</p>             | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus.png?raw=true" alt="" data-size="original">               |
| <p>TOUCHSCREEN POINTER<br>(inversion)</p>                | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/3ds_stylus_revert.png?raw=true" alt="" data-size="original">        |
| C-STICK                                                  | Same as standard layout                                                                                                                               |

## Specific System Information

### Files location

<table><thead><tr><th width="254">Data</th><th>Path (relative to retrobat root path)</th></tr></thead><tbody><tr><td>nand path</td><td>saves\3ds\&#x3C;emulator>\nand</td></tr><tr><td>sdmc path</td><td>saves\3ds\&#x3C;emulator>\sdmc</td></tr><tr><td>config file</td><td>emulators\&#x3C;emulator>\user\config\qt-config.ini</td></tr></tbody></table>

### Running installed apps

It is possible to use a .m3u file to run games that have been installed to the console NAND, the .m3u file must contain the full path to the .app file of the game.

Example of a game installed in the console NAND:

<div align="left"><figure><img src="https://i.imgur.com/PF0szhC.png" alt=""><figcaption></figcaption></figure></div>

Create a shortcut to the desktop for the installed game (right-click):

<div align="left"><figure><img src="https://i.imgur.com/ZEajnv8.png" alt=""><figcaption></figcaption></figure></div>

On the windows desktop, right-click on the the shortcut to copy its path and paste it in a .txt file (only keep the last part which is the path to the installed app, without the ""):

<div align="left"><figure><img src="https://i.imgur.com/o7E5uFQ.png" alt=""><figcaption></figcaption></figure></div>

Save the text file with the .m3u extension and place it in the roms\3ds folder:

<div align="left"><figure><img src="https://i.imgur.com/g2xUhcm.png" alt=""><figcaption></figcaption></figure></div>

### Custom Textures

It is possible to launch Custom Texture packs with the Citra standalone Emulator and Lime3DS.

The texture pack needs to be placed in the `\emulators\`<mark style="color:purple;">`<emulator>`</mark>`\User\Load\Textures\<gameID>` folder, example for Super Mario 3D Land:

<div align="left"><figure><img src="https://i.imgur.com/6dLxUWC.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
When using the libretro core, textures must be placed in:

`\saves\3ds\citra\Load\Textures\<gameID>`
{% endhint %}

The name of the custom texture folder can be found by right-clicking on the game in the emulator and selecting "Open Custom Texture Location".

<div align="left"><figure><img src="https://i.imgur.com/xijuvR0.png" alt=""><figcaption></figcaption></figure></div>

Once the custom texture pack is correctly named and placed, activate the **CUSTOM TEXTURES** setting.

<div align="left"><figure><img src="https://i.imgur.com/R5SWtvS.png" alt=""><figcaption><p>Go to the View Options from the Citra System</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/Q0aI7p0.png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/WIDc4VR.png" alt=""><figcaption></figcaption></figure></div>
