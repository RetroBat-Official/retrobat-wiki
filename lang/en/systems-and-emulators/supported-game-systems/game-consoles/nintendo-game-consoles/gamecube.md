---
description: Nintendo
---

# GameCube

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/gc-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/gc.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Game Console - Lifespan: 2001 - 2007

{% embed url="https://en.wikipedia.org/wiki/GameCube" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>dolphin</li><li>libretro: dolphin</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> gamecube</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.gcz .iso .ciso .wbfs .wad .rvz .wia .m3u</td><td></td></tr></tbody></table>

## Features

| RetroAchievements | Netplay |
| ----------------- | ------- |
| NO                | NO      |

## BIOS

The BIOS files are not mandatory to launch games but some require at least one of their region for better graphic effects and font support.

<table data-header-hidden><thead><tr><th width="169">File</th><th width="625">Location &#x26; MD5</th><th data-hidden>MD5 Hash</th></tr></thead><tbody><tr><td><code>IPL.bin</code><br>Europe</td><td><p>location: <code>\emulators\dolphin-emu\User\GC\EUR</code></p><p>libretro location: <code>\saves\gamecube\User\GC\EUR</code><br>md5: <code>0cdda509e2da83c85bfe423dd87346cc</code></p></td><td></td></tr><tr><td><code>IPL.bin</code><br>Japan</td><td><p>location: <code>\emulators\dolphin-emu\User\GC\JAP</code></p><p>libretro location: <code>\saves\gamecube\User\GC\JAP</code><br>md5: <code>fc924a7c879b661abc37cec4f018fdf3</code></p></td><td></td></tr><tr><td><code>IPL.bin</code><br>USA</td><td><p>location: <code>\emulators\dolphin-emu\User\GC\USA</code></p><p>libretro location: <code>\saves\gamecube\User\GC\USA</code><br>md5: <code>019e39822a9ca3029124f74dd4d55ac4</code></p></td><td></td></tr></tbody></table>

## Controls

{% hint style="info" %}
The following controllers can be autoconfigured from RetroBat to Dolphin:

* XInput controllers
* Dualshock 4 and Dualsense controllers
* Nintendo Switch Pro controller
* Original Gamecube controller through Gamecube Adapter
{% endhint %}

| RetroBat key                                                                       | GameCube key             |
| ---------------------------------------------------------------------------------- | ------------------------ |
| START                                                                              | START                    |
| D-PAD                                                                              | D-PAD                    |
| Analog Stick - Left                                                                | Analog Stick - Left      |
| Analog Stick - Right                                                               | Analog Stick  - C-Stick  |
| ![A](<../../../../.gitbook/assets/image (25).png>)                                 | B                        |
| ![B](<../../../../.gitbook/assets/image (11).png>)                                 | A                        |
| <img src="../../../../.gitbook/assets/image (45).png" alt="" data-size="original"> | X                        |
| <img src="../../../../.gitbook/assets/image (43).png" alt="" data-size="line">     | Y                        |
| RB (R1)                                                                            | Z                        |
| LT (L2)                                                                            | L                        |
| RT (R2)                                                                            | R                        |

{% hint style="info" %}
Rumble can be activated in the advanced options.
{% endhint %}

### Creating a game-specific control profile

It is possible to create a custom controller profile in Dolphin and assign it to a specific game, [follow this guide if required](../../../../controllers/specific\_mapping/dolphin-controller-mapping.md).

## Specific system information

### Multi-disc games

To automatically load the next disc of a game, you can use a `.m3u` playlist file.&#x20;

In the m3u file, list all game discs from your game:

<div align="left">

<figure><img src="https://i.imgur.com/Hh12kWj.png" alt=""><figcaption></figcaption></figure>

</div>

Within that text file, write the names of the game files for your game discs:

<div align="left">

<figure><img src="https://i.imgur.com/aBZpJ4W.png" alt=""><figcaption></figcaption></figure>

</div>

Finally save the file as a .m3u file.

### Custom Textures

It is possible to launch Custom Texture packs with the Dolphin Emulator.

The texture pack needs to be placed in the `\saves\gamecube\User\Load\Textures` folder.

<div align="left">

<figure><img src="https://i.imgur.com/3Zr8SS4.png" alt=""><figcaption></figcaption></figure>

</div>

The name of the custom texture folder must be strictly identical to the **Game ID** that can be found in the game properties inside Dolphin.

<div align="left">

<figure><img src="https://i.imgur.com/wWaNFxC.png" alt=""><figcaption></figcaption></figure>

</div>

Once the custom texture pack is correctly named and placed, activate the **CUSTOM TEXTURES** setting.

<div align="left">

<figure><img src="https://i.imgur.com/R5SWtvS.png" alt=""><figcaption><p>Go to the View Options from the Gamecube System</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/K5NInuR.png" alt=""><figcaption><p>Select "Visual Rendering"</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/UPixWDa.png" alt=""><figcaption><p>Set Custom Textures to YES</p></figcaption></figure>

</div>
