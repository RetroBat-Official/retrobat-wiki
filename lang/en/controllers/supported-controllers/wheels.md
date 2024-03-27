---
description: Vroum vroum
---

# 🛞 Wheels

Wheels compatibility is still in early phase with Retrobat, it might be possible that for many Emulators, specific configuration is required to make it work correctly.

There are multiple wheels on the market, however, only [a few have been tested so far](wheels.md#wheel-devices-compatible-with-retrobat).

## Wheel games detection

<div align="left">

<figure><img src="https://i.imgur.com/LaVtSwP.png" alt=""><figcaption><p>Daytona USA  is compatible</p></figcaption></figure>

</div>

The list of Wheel games is stored in an .xml file inside your Retrobat folder, if you find that some games appear in the list but are not Wheel games, you can remove them from the file and manage your own list

{% hint style="warning" %}
Edit this file at your own risk.&#x20;

Be sure to save your file version as it might be overwritten by a Retrobat update.
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/2wr4B4z.png" alt=""><figcaption></figcaption></figure>

</div>

## Wheels Configuration

### Wheel Activation

Wheels can be activated for a system or for a game.

To activate Wheels for a system, from the **Game View**, open the [View Options](../../navigation/view-options.md) and select **ADVANCED SYSTEM OPTIONS**

<div align="left">

<figure><img src="https://i.imgur.com/rfmZxeu.png" alt=""><figcaption></figcaption></figure>

</div>

Navigate to **WHEELS**

<div align="left">

<figure><img src="https://i.imgur.com/95KNC6e.png" alt=""><figcaption></figcaption></figure>

</div>

Switch **WHEELS** to **ON**

<div align="left">

<figure><img src="https://i.imgur.com/0iEdlKI.png" alt=""><figcaption></figcaption></figure>

</div>

The same can be done per game from the [Game Options](../../navigation/game-options.md) menu and **ADVANCED GAME OPTIONS**

## Wheel Devices compatible with RetroBat

{% hint style="info" %}
RetroBat does not offer option to play with a wheel without throttle / brake pedals, it is required to have both devices when turning on the wheels option.

The gear stick, however, is optional.
{% endhint %}

### Logitech G29

<div align="left">

<figure><img src="https://i.imgur.com/KAmr0lK.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Logitech G920

<div align="left">

<figure><img src="https://i.imgur.com/tEJuFXl.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Logitech G923

<div align="left">

<figure><img src="https://i.imgur.com/TMaOjRK.png" alt="" width="375"><figcaption></figcaption></figure>

</div>

### Thrustmaster T300RS

<div align="left">

<figure><img src="https://i.imgur.com/Aos7B0z.jpeg" alt="" width="375"><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
It is very important for this wheel that pedals are set to split in the Thrustmaster Control Panel tool.

Also, ensure that pedals are not inverted (this can be fixed by maintaining MODE + L3 + R3 buttons).
{% endhint %}

## Emulators compatibility

The following list of emulators have been configured to be compatible with wheels autoconfiguration:

<table><thead><tr><th width="160">Emulator</th><th width="229">Force feedback</th><th>Remark</th></tr></thead><tbody><tr><td>Model 2</td><td>YES</td><td>RetroBat offers per-game specific mapping</td></tr><tr><td>Supermodel</td><td>YES</td><td></td></tr><tr><td>Flycast</td><td>NO (needs external tool)</td><td>RetroBat offers different button layouts to map throttle and brake pedals</td></tr><tr><td>PCSX2</td><td>YES but need to open menu and configure it each time</td><td>Might need to modify the wheel type in the advanced options</td></tr></tbody></table>
