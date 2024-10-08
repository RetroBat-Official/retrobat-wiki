# Decorations (bezels)

Most of the TVs and computer screens in the 80s and 90s were 4:3. When you run them today on a 16:9 format monitor, there will be empty space on both sides.

The remaining space on the left and right side of the game can be filled with decorations (bezels).

Retrobat offers 3 types of decorations:

* Decorations
* The Bezel Project
* Mega-Bezels

It is also possible for some systems to enable "**tattoos**", which are overlays that show the control layout for the emulated machine.

## Decorations

Standard decorations are the simplest way to fill the left and right space.

They can be enabled from the [MAIN MENU](../navigation/main-menu.md#game-settings) (Game Settings > Decorations), from the [VIEW OPTIONS](../navigation/view-options.md#advanced-system-options) (Advanced System Options > Decorations) or from the [GAME OPTIONS](../navigation/game-options.md#advanced-game-options) (Advanced Game Options > Decorations).

The following options are available:

<table><thead><tr><th width="272">Setting</th><th>Remark</th></tr></thead><tbody><tr><td>AUTO</td><td><a href="decorations-and-bezels.md#default-search-logic">Default search logic</a></td></tr><tr><td>NONE</td><td>No decoration</td></tr><tr><td>AMBIANCE BROADCAST</td><td></td></tr><tr><td>AMBIANCE GAMEROOM</td><td></td></tr><tr><td>AMBIANCE MONITOR 1084S</td><td></td></tr><tr><td>AMBIANCE NIGHT</td><td></td></tr><tr><td>AMBIANCE VINTAGE TV</td><td></td></tr><tr><td>ARCADE 1980S</td><td></td></tr><tr><td>ARCADE 1980S VERTICAL</td><td></td></tr><tr><td>ARCADE VERTICAL DEFAULT</td><td></td></tr><tr><td>DEFAULT CURVE</td><td></td></tr><tr><td>DEFAULT CURVE NIGHT</td><td></td></tr><tr><td>DEFAULT NOCURVE</td><td></td></tr><tr><td>DEFAULT NOCURVE NIGHT</td><td></td></tr><tr><td>DEFAULT UNGLAZED</td><td></td></tr><tr><td>THEBEZELPROJECT</td><td>See The Bezel Project section</td></tr></tbody></table>

Here is an example of the AUTO setting for Super Nintendo:

<div align="left">

<figure><img src="https://i.imgur.com/Ew1Ax7s.png" alt=""><figcaption></figcaption></figure>

</div>

### Default search logic:

* retrobat\decorations\\\<bezel type>\games\\\<system>\\\<rom>.png
* retrobat\system\decorations\\\<bezel type>\games\\\<system>\\\<rom>.png
* retrobat\decorations\\\<bezel type>\games\\\<rom>.png
* retrobat\system\decorations\\\<bezel type>\games\\\<rom>.png
* retrobat\decorations\\\<bezel type>\games\\\<system>\\\<indexedRomName>.png
* retrobat\system\decorations\\\<bezel type>\games\\\<system>\\\<indexedRomName>.png
* retrobat\decorations\\\<bezel type>\games\\\<indexedRomName>.png
* retrobat\system\decorations\\\<bezel type>\games\\\<indexedRomName>.png
* retrobat\decorations\\\<bezel type>\\\<system>\\\<system>.png
* retrobat\system\decorations\\\<bezel type>\\\<system>\\\<system>.png
* retrobat\decorations\\\<bezel type>\default.png
* retrobat\system\decorations\\\<bezel type>\default.png
* retrobat\decorations\default\_unglazed\\\<system>\\\<system>.png
* retrobat\system\decorations\default\_unglazed\\\<system>\\\<system>.png
* retrobat\decorations\default\\\<system>\\\<system>.png
* retrobat\system\decorations\default\\\<system>\\\<system>.png

## The Bezel Project

The Bezel Project provides personalized bezels per gaming system, and for many of them even personalized bezels per game.

### Downloading Bezels

You can download the bezels from the [UPDATES & DOWNLOADS](updates-and-content-download.md#download-content) menu

<div align="left">

<figure><img src="https://i.imgur.com/uGK5lHJ.png" alt=""><figcaption></figcaption></figure>

</div>

Select THE BEZEL PROJECT and choose the system for which you want to download bezels.

<div align="left">

<figure><img src="https://i.imgur.com/DEaOLJT.png" alt=""><figcaption></figcaption></figure>

</div>

Press ![](<../.gitbook/assets/image (30).png>) and confirm installation.

<div align="left">

<figure><img src="https://i.imgur.com/uKqTGOn.png" alt=""><figcaption></figcaption></figure>

</div>

The download starts

<div align="left">

<figure><img src="https://i.imgur.com/zBioOvM.png" alt=""><figcaption></figcaption></figure>

</div>

Wait until completion of the installation

<div align="left">

<figure><img src="https://i.imgur.com/HpZj7Se.png" alt=""><figcaption></figcaption></figure>

</div>

The downloaded Bezels are stored in the `\decorations\thebezelproject\games` folder:

<div align="left">

<figure><img src="https://i.imgur.com/WPD5p2r.png" alt=""><figcaption></figcaption></figure>

</div>

### Enabling Bezels

See the [Decorations](decorations-and-bezels.md#decorations) section.

Set the decoration option to **THEBEZELPROJECT**

<div align="left">

<figure><img src="https://i.imgur.com/wg3490A.png" alt=""><figcaption></figcaption></figure>

</div>

Example of decoration from The Bezel Project:

<div align="left">

<figure><img src="https://i.imgur.com/edBZRpf.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
To use per game Bezels, the rom file needs to have the exact same name as the bezel in the `\decorations\thebezelproject\games` folder.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/j2LoA0W.png" alt=""><figcaption></figcaption></figure>

</div>

## Mega Bezels

The MegaBezel pack combines both Shaders and Bezels, it adds dynamic reflections on the bezel.

{% hint style="info" %}
Mega Bezels can only be used with Libretro cores, it does not work with standalone emulators.
{% endhint %}

### Downloading a MegaBezel pack

From the [CONTENT DOWNLOADER](updates-and-content-download.md#download-content), select **Megabezels**

<div align="left">

<figure><img src="https://i.imgur.com/QmWLsNg.png" alt=""><figcaption></figcaption></figure>

</div>

The pack is downloaded in the `\emulators\retroarch\shaders` folder

<div align="left">

<figure><img src="https://i.imgur.com/z8WoJp8.png" alt=""><figcaption></figcaption></figure>

</div>

### Enabling Mega Bezels

Mega Bezels can be enabled from the [MAIN MENU](../navigation/main-menu.md#game-settings) (Game Settings > Shader Set), from the [VIEW OPTIONS](../navigation/view-options.md#advanced-system-options) (Advanced System Options > Shader Set) or from the [GAME OPTIONS](../navigation/game-options.md#advanced-game-options) (Advanced Game Options > Shader Set)

<div align="left">

<figure><img src="https://i.imgur.com/lXvxZPy.png" alt=""><figcaption></figcaption></figure>

</div>

There are multiple options available for each pack.

In addition, set **DECORATIONS** to **NONE** and **GAME ASPECT RATIO** to **FULL**

<div align="left">

<figure><img src="https://i.imgur.com/xFINt8C.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
You can leave GAME ASPECT RATIO on "AUTO" if you are using a 4/3 screen.
{% endhint %}

Last but not least, Mega Bezels only work with **VULKAN** video driver, so ensure it is set properly in the [**Advanced Settings > Drivers** menu](../navigation/view-options.md#advanced-system-options)

<div align="left">

<figure><img src="https://i.imgur.com/nuSg307.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/HVJIY6D.png" alt=""><figcaption></figcaption></figure>

</div>

Here are some examples of Mega Bezel:

<div align="left">

<figure><img src="https://i.imgur.com/nnAzMON.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/HYSzHRZ.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/mmaoUzW.png" alt=""><figcaption></figcaption></figure>

</div>

### Customize Mega-bezels

Refer to [section "Customize Mega-bezels"](../tutorials/customize-mega-bezels.md#adding-a-new-mega-bezel-preset-entry-to-retrobat)

## Tattoos

Tattoos are a bezel overlay that can help with identifying the controls for the emulated system:

<div align="left">

<figure><img src="https://i.imgur.com/0kO2KQv.png" alt=""><figcaption></figcaption></figure>

</div>

To enable tattoos,open the **MAIN MENU** > **GAME SETTINGS**:

<div align="left">

<figure><img src="https://i.imgur.com/fIip7cs.png" alt=""><figcaption></figcaption></figure>

</div>

then **GLOBAL OPTIONS** > **TATTOO**:

<div align="left">

<figure><img src="https://i.imgur.com/dIv1Ety.png" alt=""><figcaption></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/GgZipNc.png" alt=""><figcaption></figcaption></figure>

</div>

It is possible to configure the corner in which the tattoo will be displayed.

{% hint style="info" %}
Tattoos will only work in combination with bezels : no bezels, no tattoos.
{% endhint %}
