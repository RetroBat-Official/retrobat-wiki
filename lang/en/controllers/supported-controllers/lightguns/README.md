---
description: Bang bang
---

# 🔫 Lightguns

Lightgun compatibility is still in early phase with Retrobat, it might be possible that for many Emulators, specific configuration is required to make it work correctly.

There are several lightguns on the market, however, only a few have been tested so far.

## Lightgun detection

When a lightgun is connected to the system, a small gun icon appears on the top left corner near the Gamepad icon : ![](<../../../.gitbook/assets/image (8).png>)

Also, a crosshair will appear on the screen as well as a collection called **LIGHT GUN** in the **System View**.

<div align="left">

<figure><img src="https://i.imgur.com/YDBWOrd.png" alt=""><figcaption></figcaption></figure>

</div>

LightGun compatible games will have a specific icon next to their name in the **Game View**

<div align="left">

<figure><img src="https://i.imgur.com/rbFVyjA.png" alt=""><figcaption><p>Duck Hunt is compatible</p></figcaption></figure>

</div>

The list of LightGun games is stored in an .xml file inside your Retrobat folder, if you find that some games appear in the list but are not LightGun games, you can remove them from the file and manage your own list

{% hint style="info" %}
Be sure to save your file version as it might be overwritten by a Retrobat update.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/WrtdDbz.png" alt=""><figcaption><p>gungames.xml folder</p></figcaption></figure>

</div>

{% hint style="info" %}
Some games appear in the list but the LightGun functionality is available only in some levels or some mini-games.
{% endhint %}

## Lightgun Configuration

### Lightgun Activation

Lightguns can be activated for a system or for a game.

To activate Lightguns for a system, from the **Game View**, open the [View Options](../../../navigation/view-options.md) and select **ADVANCED SYSTEM OPTIONS**

<div align="left">

<figure><img src="https://i.imgur.com/rfmZxeu.png" alt=""><figcaption></figcaption></figure>

</div>

Navigate to **CONTROLS**

<div align="left">

<figure><img src="https://i.imgur.com/lbqvjVS.png" alt=""><figcaption></figcaption></figure>

</div>

Switch **LIGHTUN** to **ON**

<div align="left">

<figure><img src="https://i.imgur.com/rpt8cBZ.png" alt=""><figcaption></figcaption></figure>

</div>

The same can be done per game from the [Game Options](../../../navigation/game-options.md) menu and **ADVANCED GAME OPTIONS**

{% hint style="info" %}
For some systems the option will be directly in the **ADVANCED OPTIONS** list (e.g. 3DO), for other systems the option will be named **LIGHTGUN MODE** (e.g. MAME).
{% endhint %}

## Lightgun Devices

### WiiMote & Mayflash DolphinBar

![](<../../../.gitbook/assets/image (40).png>)![](<../../../.gitbook/assets/image (23).png>)

The Wiimote and DolphinBar is actually a great way to enjoy your Lightgun game library.

There are 2 ways of using the Wiimote as a Lightgun:

* By using the mode 2 of the Mayflash Dolphinbar
* By using the mode 4 of the Mayflash Dolphinbar and activating the [WiimoteGun software](wiimotegun.md).

{% hint style="info" %}
This guide assumes that you already know how to connect your Mayflash Dolphinbar and your Wiimotes. If not you can find all instructions on the [Mayflash Website](https://www.mayflash.com/product/6.html).
{% endhint %}

Both of these options will serve the same purpose : it will convert your Wiimotes movements and buttons into Mouse & Keyboard keys. This means that emulators that can use a mouse as a gun will be able to work with the Wiimote.

When using the Dolphinbar in mode 4 with WiimoteGun, you will be able to calibrate your Wiimote with a long-press on the "Home" button of the Wiimote.

{% hint style="info" %}
For better accuracy, it is recommended to place your Dolphinbar UNDER your screen, as close as possible to the display (do not forget to set your Dolphinbar switch at the back to the BOTTOM position).
{% endhint %}

{% hint style="info" %}
For Dolphin standalone emulator, you need to set the Dolphinbar in mode 4 as this is the native Wiimote mode supported by Dolphin and allowing you to use your wiimotes as **REAL WIIMOTES** for best possible experience. See the Wii section of the wiki for more information.
{% endhint %}

{% hint style="danger" %}
Note that Wiimote mode 4 is not compatible with using multiple Wiimotes for multigun games.
{% endhint %}

### Sinden Lightgun

<div align="left">

<figure><img src="https://i.imgur.com/B4s3AIf.png" alt="" width="188"><figcaption></figcaption></figure>

</div>

The Sinden Lightgun works with RetroBat and should be automatically detected, it is however necessary to have the Sinden Software running in parallel of RetroBat.

{% embed url="https://sindenlightgun.com/drivers/" %}

When using Sinden Lightguns, the gun requires a white border to be displayed around the game screen. This border is necessary for the gun to detect the placement of the target on screen.&#x20;

* The border should appear automatically for libretro cores (RetroArch)
* For "standalone" emulators, RetroBat uses Reshade to manage the boder. For that select the "sindenborder" shader in the list of available shaders in the RetroBat menu:

<div align="left">

<figure><img src="https://i.imgur.com/Tx26Eal.png" alt=""><figcaption></figcaption></figure>

</div>

### Gun4IR

{% embed url="https://www.gun4ir.com/" %}
