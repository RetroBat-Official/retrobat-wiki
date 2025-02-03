---
description: Vroum vroum
---

# 🛞 Wheels

Wheels compatibility is still in early phase with Retrobat, it might be possible that for many Emulators, specific configuration is required to make it work correctly.

There are multiple wheels on the market, however, only [a few have been tested so far](wheels.md#wheel-devices-compatible-with-retrobat).

## Wheel games detection

<div align="left"><figure><img src="https://i.imgur.com/LaVtSwP.png" alt=""><figcaption><p>Daytona USA  is compatible</p></figcaption></figure></div>

The list of Wheel games is stored in an .xml file inside your Retrobat folder, if you find that some games appear in the list but are not Wheel games, you can remove them from the file and manage your own list

{% hint style="warning" %}
Edit this file at your own risk.&#x20;

Be sure to save your file version as it might be overwritten by a Retrobat update.
{% endhint %}

<div align="left"><figure><img src="https://i.imgur.com/2wr4B4z.png" alt=""><figcaption></figcaption></figure></div>

## Wheels Configuration

### Wheel Activation

Wheels can be activated for a system or for a game.

To activate Wheels for a system, from the **Game View**, open the [View Options](../../navigation/view-options.md) and select **ADVANCED SYSTEM OPTIONS**

<div align="left"><figure><img src="https://i.imgur.com/rfmZxeu.png" alt=""><figcaption></figcaption></figure></div>

Navigate to **WHEELS**

<div align="left"><figure><img src="https://i.imgur.com/95KNC6e.png" alt=""><figcaption></figcaption></figure></div>

Switch **WHEELS** to **ON**

<div align="left"><figure><img src="https://i.imgur.com/0iEdlKI.png" alt=""><figcaption></figcaption></figure></div>

The same can be done per game from the [Game Options](../../navigation/game-options.md) menu and **ADVANCED GAME OPTIONS**

## Wheel Devices compatible with RetroBat

{% hint style="info" %}
RetroBat does not offer option to play with a wheel without throttle / brake pedals, it is required to have both devices when turning on the wheels option.

The gear stick, however, is optional.
{% endhint %}

### Logitech G29

<div align="left"><figure><img src="https://i.imgur.com/KAmr0lK.png" alt="" width="375"><figcaption></figcaption></figure></div>

### Logitech G920

<div align="left"><figure><img src="https://i.imgur.com/tEJuFXl.png" alt="" width="375"><figcaption></figcaption></figure></div>

### Logitech G923

<div align="left"><figure><img src="https://i.imgur.com/TMaOjRK.png" alt="" width="375"><figcaption></figcaption></figure></div>

### Thrustmaster T300RS

<div align="left"><figure><img src="https://i.imgur.com/Aos7B0z.jpeg" alt="" width="375"><figcaption></figcaption></figure></div>

{% hint style="info" %}
It is very important for this wheel that pedals are set to split in the Thrustmaster Control Panel tool.

Also, ensure that pedals are not inverted (this can be fixed by maintaining MODE + L3 + R3 buttons).
{% endhint %}

## Emulators compatibility

The following list of emulators have been configured to be compatible with wheels autoconfiguration:

<table><thead><tr><th width="160">Emulator</th><th width="229">Force feedback</th><th>Remark</th></tr></thead><tbody><tr><td>Model 2</td><td>YES</td><td>RetroBat offers per-game specific mapping</td></tr><tr><td>Supermodel</td><td>YES</td><td></td></tr><tr><td>Flycast</td><td>NO (needs external tool)</td><td>RetroBat offers different button layouts to map throttle and brake pedals</td></tr><tr><td>PCSX2</td><td>YES but need to open menu and configure it each time</td><td>Might need to modify the wheel type in the advanced options</td></tr></tbody></table>

### Configuring a wheel

Wheel mapping for a specific wheel can be configured in the files located in the `system\resources\inputmapping\wheels` of your RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/iBP5mGf.png" alt=""><figcaption></figcaption></figure></div>

this is an example for Flycast:

<div align="left"><figure><img src="https://i.imgur.com/5Pq3Bn5.png" alt=""><figcaption></figcaption></figure></div>

Each wheel must be in its own container, with the buttons below it with a 2 space indent.

The LogitechG29 wheel can be used as example.

To build the file for your wheel, configure the wheel in Flycast, save, open the configuration file created in the `emulators\flycast\mappings` folder and report the values.

The name of the container for the supported wheels can be found [here](wheels.md#supported-wheels).

### Supported wheels

<details>

<summary>Supported wheels and VID/PID</summary>

VID\_2433\&PID\_F300 : AsetekInvicta\
VID\_2433\&PID\_F301 : AsetekForte\
VID\_2433\&PID\_F303 : AsetekLaPrima\
VID\_2433\&PID\_F306 : AsetekTonyKannan\
VID\_3416\&PID\_0301 : CammusC5\
VID\_3416\&PID\_0302 : CammusC12\
VID\_0EB7\&PID\_0001 : FanatecClubSportWheelBaseV2\
VID\_0EB7\&PID\_0004 : FanatecClubSportWheelBaseV25\
VID\_0EB7\&PID\_0005 : FanatecCSLElitePS4\
VID\_0EB7\&PID\_0006 : FanatecPodiumDD1\
VID\_0EB7\&PID\_0007 : FanatecPodiumDD2\
VID\_0EB7\&PID\_0011 : FanatecCSRElite\
VID\_0EB7\&PID\_0020 : FanatecDD\
VID\_0EB7\&PID\_0E03 : FanatecCSLElite\
VID\_046D\&PID\_C202 : LogitechWingmanFormula\
VID\_046D\&PID\_C20E : LogitechWingmanFormulaGP\
VID\_046D\&PID\_C24F : LogitechG29\
VID\_046D\&PID\_C260 : LogitechG29\
VID\_046D\&PID\_C262 : LogitechG920\
VID\_046D\&PID\_C266 : LogitechG923PS\
VID\_046D\&PID\_C267 : LogitechG923PS\
VID\_046D\&PID\_C26D : LogitechG923X\
VID\_046D\&PID\_C26E : LogitechG923X\
VID\_046D\&PID\_C272 :  LogitechGPro\
VID\_046D\&PID\_C293 : LogitechWingmanFormulaForce\
VID\_046D\&PID\_C294 : LogitechDrivingForce\
VID\_046D\&PID\_C295 : LogitechMomoForce\
VID\_046D\&PID\_C298 : LogitechDrivingForce\
VID\_046D\&PID\_C299 : LogitechG25\
VID\_046D\&PID\_C29A : LogitechDrivingForceGT\
VID\_046D\&PID\_C29B : LogitechG27\
VID\_046D\&PID\_C29C : LogitechSpeedForce\
VID\_046D\&PID\_CA03 : LogitechMomoRacing\
VID\_046D\&PID\_CA04 : LogitechRacingWheel\
VID\_045E\&PID\_001A : MicrosoftSideWinder\
VID\_045E\&PID\_0034 :  MicrosoftSideWinder\
VID\_346E\&PID\_0000 : MozaR16\
VID\_346E\&PID\_0002 : MozaR9\
VID\_346E\&PID\_0004 : MozaR5\
VID\_346E\&PID\_0005 : MozaR3\
VID\_346E\&PID\_0006 : MozaR12\
VID\_0483\&PID\_0522 : SimagicM10\
VID\_16D0\&PID\_0D5A : Simucube1\
VID\_16D0\&PID\_0D5F : Simucube2Ultimate\
VID\_16D0\&PID\_0D60 : Simucube2Pro\
VID\_16D0\&PID\_0D61 : Simucube2Sport\
VID\_1FC9\&PID\_804C : SimXperienceAccuForcePro\
VID\_044F\&PID\_B56A : ThrustmasterF430FF\
VID\_044F\&PID\_B56E : ThrustmasterT500RS\
VID\_044F\&PID\_B605 : ThrustmasterNascarProFF2\
VID\_044F\&PID\_B651 : ThrustmasterFGTRumbleForce\
VID\_044F\&PID\_B653 : ThrustmasterRGT\
VID\_044F\&PID\_B654 : ThrustmasterFGTFF\
VID\_044F\&PID\_B669 : ThrustmasterTX\
VID\_044F\&PID\_B66D : ThrustmasterT300RSPS4\
VID\_044F\&PID\_B66E : ThrustmasterT300RSPS3\
VID\_044F\&PID\_B66F : ThrustmasterT300RSPS3ADV\
VID\_044F\&PID\_B677 : ThrustmasterT150\
VID\_044F\&PID\_B67F : ThrustmasterTMX\
VID\_044F\&PID\_B689 : ThrustmasterTSPC\
VID\_044F\&PID\_B692 : ThrustmasterTSXW\
VID\_044F\&PID\_B696 : ThrustmasterT248\
VID\_0483\&PID\_A355 :  VRSDirectForcePro\
VID\_11FF\&PID\_0511 : PXNV9

</details>
