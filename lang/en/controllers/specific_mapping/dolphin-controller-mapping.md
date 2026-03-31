# Dolphin controller mapping

The Gamecube and the Wii are known to have a very specific control layout, which varies greatly from one game to another.

This results in a complex situation when it comes to emulators controller configuration.

The following guide will help you understand and guide you on how to setup and use a specific controller layout for a game with the Dolphin emulator.

{% hint style="info" %}
All information can be found on the Dolphin wiki:

[https://wiki.dolphin-emu.org/index.php?title=GameINI\_(Controller\_Settings)](https://wiki.dolphin-emu.org/index.php?title=GameINI_\(Controller_Settings\))
{% endhint %}

## Using RetroBat autoconfiguration

Most of the controller mapping requirements are managed automatically with RetroBat, here are some details for both Gamecube and Wii Systems.

### GameCube

RetroBat offers several input layouts for GameCube, these profiles have an impact on the face button placement on your physical controller.

The option is available in the **ADVANCED SETTINGS > CONTROLS** menu:

<div align="left"><figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
More detail about the profiles can be found on the [Gamecube system page](../../systems-and-emulators/supported-game-systems/game-consoles/nintendo-game-consoles/gamecube.md#controls).
{% endhint %}



In addition to the face button profiles, RetroBat also offers an option to change the type of controller:

<div align="left"><figure><img src="../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure></div>

This will automatically change the type of controller connected within the Dolphin emulator:

<div align="left"><figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
More information about using a Gamecube adapter can be found [here](../../systems-and-emulators/supported-game-systems/game-consoles/nintendo-game-consoles/gamecube.md#using-a-gamecube-adapter)
{% endhint %}

### Wii

RetroBat offers several input layouts for emulated wiimotes, these profiles have an impact on the way your controller is mapped to the Wii original controller (wiimote or classic controller).

<div align="left"><figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure></div>

More information can be found [here](../../systems-and-emulators/supported-game-systems/game-consoles/nintendo-game-consoles/wii.md#emulated-wiimote).

Certain Wii games were also compatible with the GameCube controller, in order to enable GameCube Controller emulation for Wii, enable the option in **ADVANCED SETTINGS > CONTROLS**:

<div align="left"><figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
This will enable the same options as for Gamecube controllers, including Gamecube layouts and using an original console controller.
{% endhint %}

## Using an original console controller

### Gamecube

RetroBat is shipped with a file named "**GCControllers.json**" located in the `\system\resources\inputmapping` folder of your RetroBat installation:

<div align="left"><figure><img src="../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure></div>

This file can be used to automatically configure a specific controller, based on its GUID, in the Dolphin emulator.

The above example is for the Mayflash GC 2 player adapters, the different values required in the file are the following:

* **Emulator:** dolphin (the file can also be used for libretro)
* **Name**: for information only
* **Guid**: allows RetroBat to enable the specific mapping based on the connected controller (the SDL GUID of the controller can be found in the es\_input.cfg file or in the emulatorlauncher.log after having launched a game). Multiple guids can be entered if a controller has multiple revisions.
* **Driver**: can be used to force the Dolphin driver to use for the controller
* **Mapping**: the actual mapping to be set in `GCPadNew.ini` file, for each button. In order to know the mapping for the controller, perform the configuration manually by running dolphin.exe, exit Dolphin, and open the GCPadNew.ini file.
* **HotkeyMapping**: the mapping for hotkeys for the controller (will modify `Hotkeys.ini` file)
* **ControllerInfo**: can be used to define if the setting needs to be activated in the RetroBat menu:

<div align="left"><figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure></div>

### Wii

RetroBat can set Dolphin to use Real Wiimotes. The best way to use real wiimotes with Dolphin is through the Mayflash Dolphin, however it is also possible to do so by syncing real wiimotes to windows via Bluetooth and using a standard IR bar.

If you are using real wiimotes, use the following setting in **ADVANCED SETTINGS > CONTROLS** to enable them:

<div align="left"><figure><img src="../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure></div>



## Using a personnalized input profile

Defining a personnalized input profile will completely bypass RetroBat autoconfiguration mechanism.

### STEP 1: Creation of a profile in Dolphin

Run _Dolphin.exe_, the executable is located in the `emulators\dolphin-emu` folder of your RetroBat installation.

Click on the "Controllers" icon in the taskbar, then select "Configure" (pick the right system depending on the game, this works both for Gamecube and Wii)

<div align="left"><figure><img src="https://i.imgur.com/6LtuBLq.png" alt=""><figcaption></figcaption></figure></div>

In the next screen, configure the mapping you want.

Once configured, enter a profile name and click the "SAVE" button

<div align="left"><figure><img src="https://i.imgur.com/J2aSCzj.png" alt=""><figcaption></figcaption></figure></div>

### STEP 2: Assign the profile to the game

Close the controller configuration windows.

In the game list, right-click on the game to which you want to apply the specific profile and select "Properties"

<div align="left"><figure><img src="https://i.imgur.com/eEWCDpa.png" alt=""><figcaption></figcaption></figure></div>

In the next screen, select the editor and in the "User Config" section, specify the profile to use

<div align="left"><figure><img src="https://i.imgur.com/sWKvW1P.png" alt=""><figcaption></figcaption></figure></div>

Type the following code:

```
[Controls]
 %ControllerType% = %ProfileName%
```

For %ControllerType%, tthe following options can be used:

* PadProfile1 to PadProfile4 : for Gamecube controllers 1 to 4
* WiimoteProfile1 to WiimoteProfile4 : for Wiimotes 1 to 4

%ProfileName% must be equal to the profile created in step 1 of this guide.



Click Close.

The profile saved will be used everytime the game is launched.



#### NB: location of profile files

Saved profile files are stored in the `\emulators\dolphin-emu\User\Config\Profiles` folder of your RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/r72aRwA.png" alt=""><figcaption></figcaption></figure></div>
