---
description: Sony
---

# PlayStation

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/psx-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/psx.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Game Console - Lifespan: 1994 - 2006

{% embed url="https://en.wikipedia.org/wiki/PlayStation_(console)" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Emulators</strong></td><td><ul><li>libretro: mednafen_psx_hw</li><li>libretro: swanstation</li><li>libretro: pcsx_rearmed</li><li>duckstation</li><li>mednafen</li><li>bizhawk: Nymashock</li><li>bizhawk: Octoshock</li></ul></td><td></td></tr><tr><td><strong>Games Location</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> psx</td><td></td></tr><tr><td><strong>File extensions</strong></td><td>.cue .img .mdf .pbp .toc .cbn .m3u .ccd .chd .zip .7z .iso .cso</td><td></td></tr></tbody></table>

## System Features

<table><thead><tr><th width="256">Retroachievements</th><th width="243">Netplay</th><th>Controller autoconfig</th></tr></thead><tbody><tr><td>lr-mednafen: YES<br>lr-swanstation: YES<br>lr-pcsx-rearmed: YES<br>Duckstation: YES<br>Mednafen: NO<br>BizHawk: YES</td><td>lr-mednafen: YES<br>lr-swanstation: NO<br>lr-pcsx-rearmed: YES<br>Duckstation: NO<br>Mednafen: NO<br>BizHawk: NO</td><td>lr-mednafen: YES<br>lr-swanstation: YES<br>lr-pcsx-rearmed: YES<br>Duckstation: YES<br>Mednafen: YES<br>BizHawk: YES</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="177">Bios file</th><th width="162">Folder</th><th>md5</th></tr></thead><tbody><tr><td>psxonpsp660.bin</td><td><code>\bios</code></td><td>c53ca5908936d412331790f4426c6c33</td></tr><tr><td>scph5500.bin</td><td><code>\bios</code></td><td>8dd7d5296a650fac7319bce665a6a53c</td></tr><tr><td>scph5501.bin</td><td><code>\bios</code></td><td>490f666e1afb15b7362b406ed1cea246</td></tr><tr><td>scph5502.bin</td><td><code>\bios</code></td><td>32736f17079d0b2b7024407c39bd3050</td></tr><tr><td>scph7001.bin</td><td><code>\bios</code></td><td>1e68c231d0896b7eadcad1d7d8e76129</td></tr></tbody></table>

## Controls

### Control layout

<div align="left">

<figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/psx.png?raw=true" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Alternative layout:

An alternative layout has been created in order to be able to use analog triggers to throttle and brake in driving games, the layout can be enabled with the following option:

<div align="left">

<figure><img src="https://i.imgur.com/bb3oWIA.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/psx_triggers_rstick.png?raw=true" alt="" width="375"><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
In order to use analog triggers, you need to change the controls in-game in order to map throttle and brake to the right analog stick.

This layout is only compatible with the analog gamepad.
{% endhint %}

## System Features

### Multi-disc games

To automatically load the next disc of a game, you can use a `.m3u` playlist file.&#x20;

In the m3u file, list all game discs from your game:

<div align="left">

<figure><img src="https://i.imgur.com/GGRxCI4.png" alt=""><figcaption><p>List of files</p></figcaption></figure>

</div>

Within that text file, write the names of the `.cue` sheets or `.chd` files for your game discs:

<div align="left">

<figure><img src="https://i.imgur.com/ZzJ7Ldj.png" alt=""><figcaption></figcaption></figure>

</div>

Finally save the file as a .m3u file.

### Custom textures

The mednafen\_psx\_hw core allows to load custom texture packs.

To do so you need to place the custom texture pack in the `\roms\psx` folder in a dedicated directory that has the same name than the game file with the addition of "-texture-replacements", for example:

* If your game name is `Final Fantasy VII (USA).iso`, the texture pack folder must be named `Final Fantasy VII (USA)-texture-replacements`
* If your game name is `Chrono Cross.fr.m3u`, the texture pack folder must be named `Chrono Cross.fr-texture-replacements`

<div align="left">

<figure><img src="https://i.imgur.com/GdXSRWK.png" alt=""><figcaption></figcaption></figure>

</div>

Once the texture pack in place, just enable the option within Retrobat:

<div align="left">

<figure><img src="https://i.imgur.com/WzHZPKq.png" alt=""><figcaption><p>Advanced options > Visual Rendering</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/8yktncM.png" alt=""><figcaption><p>Custom Textures = YES</p></figcaption></figure>

</div>

Finally, ensure that you use VULKAN video driver and that you set the resolution above 1X:

<div align="left">

<figure><img src="https://i.imgur.com/9hKDYKQ.png" alt=""><figcaption><p>Advanced options > Drivers</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/sJgZ14E.png" alt=""><figcaption><p>Advance Options, set internal resolution abov 1X</p></figcaption></figure>

</div>
