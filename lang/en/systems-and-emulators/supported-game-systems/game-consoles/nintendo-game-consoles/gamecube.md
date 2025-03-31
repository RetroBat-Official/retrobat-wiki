---
description: Nintendo
---

# GameCube

<div align="left"><figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/gc-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/gc.svg" alt=""></picture><figcaption></figcaption></figure></div>

Game Console - Lifespan: 2001 - 2007

{% embed url="https://en.wikipedia.org/wiki/GameCube" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>dolphin</li><li>libretro: dolphin</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> gamecube</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.gcz .iso .ciso .wbfs .wad .rvz .wia .m3u .zip .7z</td><td></td></tr></tbody></table>

## Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>Dolphin: YES<br>lr-dolphin: NO</td><td>Dolphin: NO<br>lr-dolphin: NO</td><td>Dolphin: YES<br>lr-dolphin: YES</td></tr></tbody></table>

## BIOS

The BIOS files are not mandatory to launch games but some require at least one of their region for better graphic effects and font support.

<table data-header-hidden><thead><tr><th width="169">File</th><th width="625">Location &#x26; MD5</th><th data-hidden>MD5 Hash</th></tr></thead><tbody><tr><td><code>IPL.bin</code><br>Europe</td><td><p>location: <code>\emulators\dolphin-emu\User\GC\EUR</code></p><p>libretro location: <code>\saves\dolphin\User\GC\EUR</code><br>md5: <code>0cdda509e2da83c85bfe423dd87346cc</code></p></td><td></td></tr><tr><td><code>IPL.bin</code><br>Japan</td><td><p>location: <code>\emulators\dolphin-emu\User\GC\JAP</code></p><p>libretro location: <code>\saves\dolphin\User\GC\JAP</code><br>md5: <code>fc924a7c879b661abc37cec4f018fdf3</code></p></td><td></td></tr><tr><td><code>IPL.bin</code><br>USA</td><td><p>location: <code>\emulators\dolphin-emu\User\GC\USA</code></p><p>libretro location: <code>\saves\dolphin\User\GC\USA</code><br>md5: <code>019e39822a9ca3029124f74dd4d55ac4</code></p></td><td></td></tr></tbody></table>

## Folders

### Saves

By default, Dolphin stores saves as GCI folders in the following location:

`saves\dolphin\User\GC\EUR\Card A`

<div align="left"><figure><img src="https://i.imgur.com/EGlIpe4.png" alt=""><figcaption></figcaption></figure></div>

The region subfolder can be amended with the following [RetroBat setting](../../../../navigation/configuration-of-systems-and-games.md):

<div align="left"><figure><img src="https://i.imgur.com/Hg5Kwy8.png" alt=""><figcaption></figcaption></figure></div>

It is possible to use classic memcard SRAM files instead of CGI folders by enabling the following option:

<div align="left"><figure><img src="https://i.imgur.com/XHG2UiZ.png" alt=""><figcaption></figcaption></figure></div>

In that case, the save file will be located in the following folder:

`saves\dolphin\User\GC\`

## Controls

{% hint style="info" %}
The following controllers can be autoconfigured from RetroBat to Dolphin:

* XInput controllers
* Dualshock 4 and Dualsense controllers
* Nintendo Switch Pro controller
* Original Gamecube controller through Gamecube Adapter
{% endhint %}

### Control layouts

RetroBat offers multiple control layouts, they can be switched in [**advanced system options**](../../../../navigation/view-options.md#advanced-system-options) **> controls**:

<div align="left"><figure><img src="https://i.imgur.com/bJxzFof.png" alt=""><figcaption></figcaption></figure></div>

| Option                              | Layout                                                                                                                                         |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>NINTENDO LAYOUT<br>(default)</p> | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gamecube.png?raw=true" alt="" data-size="original">          |
| POSITIONAL                          | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gamecube_position.png?raw=true" alt="" data-size="original"> |
| XBOX LAYOUT                         | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gamecube_xbox.png?raw=true" alt="" data-size="original">     |
| MIX                                 | <img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gamecube_xy.png?raw=true" alt="" data-size="original">       |

{% hint style="info" %}
Rumble can be activated in the advanced options.
{% endhint %}

### Using a Gamecube adapter

Dolphin can be set to use a genuine GameCube controller, to do so, it is necessary to install "Zadig" drivers for the adapter used to connect the GameCube pad:

**1.** Download Zadig here: [https://zadig.akeo.ie/](https://zadig.akeo.ie/)&#x20;

**2.** Run Zadig. Go to `Options`, select `List All Devices`.&#x20;

**3.** Find the relevant device in the device list (e.g. GC adapter - **WUP-028**, Bluetooth adapter - **CSR-XXXX**).&#x20;

**4.** Select the correct driver to replace. **libusbK** is recommended.&#x20;

**5.** Use the down and up **arrows** in the right-hand section to select a driver.&#x20;

**6.** Click `Replace Driver`. This can take a bit, at most 5 minutes. Be patient!&#x20;

**7.** Configure RetroBat to use the Adapter:

<div align="left"><figure><img src="https://i.imgur.com/i9238LM.png" alt=""><figcaption></figcaption></figure></div>

If the adapter does not work, it might mean that Dolphin does not currently support the model.

{% hint style="info" %}
RetroBat is also able to automatically detect the Raphnet and Mayflash adapters.&#x20;

They should ideally be configured with the procedure described above.&#x20;

However, they can be configured by RetroBat without updating the Zadig drivers, in such case, the feature "**USE GAMECUBE ADAPTER**" should **not** be switched ON.
{% endhint %}

### Creating a game-specific control profile

It is possible to create a custom controller profile in Dolphin and assign it to a specific game, [follow this guide if required](../../../../controllers/specific_mapping/dolphin-controller-mapping.md).

## Specific system information

### Multi-disc games

To automatically load the next disc of a game, you can use a `.m3u` playlist file.&#x20;

In the m3u file, list all game discs from your game:

<div align="left"><figure><img src="https://i.imgur.com/Hh12kWj.png" alt=""><figcaption></figcaption></figure></div>

Within that text file, write the names of the game files for your game discs:

<div align="left"><figure><img src="https://i.imgur.com/aBZpJ4W.png" alt=""><figcaption></figcaption></figure></div>

Finally save the file as a .m3u file.

### Custom Textures

It is possible to launch Custom Texture packs with the Dolphin Emulator.

The texture pack needs to be placed in the `\saves\dolphin\User\Load\Textures` folder.

<div align="left"><figure><img src="https://i.imgur.com/jJm7Htu.png" alt=""><figcaption></figcaption></figure></div>

The name of the custom texture folder must be strictly identical to the **Game ID** that can be found in the game properties inside Dolphin.

<div align="left"><figure><img src="https://i.imgur.com/wWaNFxC.png" alt=""><figcaption></figcaption></figure></div>

Once the custom texture pack is correctly named and placed, activate the **CUSTOM TEXTURES** setting.

<div align="left"><figure><img src="https://i.imgur.com/R5SWtvS.png" alt=""><figcaption><p>Go to the View Options from the Gamecube System</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/K5NInuR.png" alt=""><figcaption><p>Select "Visual Rendering"</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/UPixWDa.png" alt=""><figcaption><p>Set Custom Textures to YES</p></figcaption></figure></div>

### Adding cheevos trophy indicator when missing (retroachievements)

For some file extensions (like .gcz or .rvz), RetroBat does not recognize games as compatible with retroachievements, whereas Dolphin displays a prompt saying that you got achievement available for this game.&#x20;

<div align="left"><figure><img src="https://i.imgur.com/ThQfwGy.png" alt=""><figcaption></figcaption></figure></div>

As a result, the trophy indicator is missing in RetroBat in the system view for this particular game.

If you want to force the display of the trophy indicator, you can edit the file `gamelist.xml` available in the `roms\<system>` folder, and add the following line :&#x20;

```
<cheevosId>XXXXX</cheevosId>
```

The ID `XXXXX` above must be replaced by the corresponding game ID that you can retrieve on [https://retroachievements.org](https://retroachievements.org), while browsing the game. It appears in the address bar of the browser.

In our exemple :

<div align="left"><figure><img src="https://i.imgur.com/t1Vyf3Y.png" alt=""><figcaption></figcaption></figure></div>

Example of the gamelist.xml file after editing it to add the correct cheevos ID :

<div align="left"><figure><img src="https://i.imgur.com/sh46QjQ.png" alt=""><figcaption></figcaption></figure></div>

The trophy icon will now appear next to the name of the game :&#x20;

<div align="left"><figure><img src="https://i.imgur.com/81lKuBq.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="danger" %}
The `gamelist.xml` file is a sensible document. Don't hesitate to create a backup before doing some change on it.
{% endhint %}

