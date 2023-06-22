# Dolphin controller mapping

The Gamecube and the Wii are known to have a very specific control layout, which varies greatly from one game to another.

This results in a complex situation when it comes to emulators controller configuration.

The following guide will help you to setup and use a specific controller layout for a game with the Dolphin emulator.

{% hint style="info" %}
All information can be found on the Dolphin wiki:

[https://wiki.dolphin-emu.org/index.php?title=GameINI\_(Controller\_Settings)](https://wiki.dolphin-emu.org/index.php?title=GameINI\_\(Controller\_Settings\))
{% endhint %}

### STEP 1: Creation of a profile in Dolphin

Run _Dolphin.exe_, the executable is located in the `emulators\dolphin-emu` folder of your RetroBat installation.

Click on the "Controllers" icon in the taskbar, then select "Configure" (pick the right system depending on the game, this works both for Gamecube and Wii)

<div align="left">

<figure><img src="https://i.imgur.com/6LtuBLq.png" alt=""><figcaption></figcaption></figure>

</div>

In the next screen, configure the mapping you want.

Once configured, enter a profile name and click the "SAVE" button

<div align="left">

<figure><img src="https://i.imgur.com/J2aSCzj.png" alt=""><figcaption></figcaption></figure>

</div>

### STEP 2: Assign the profile to the game

Close the controller configuration windows.

In the game list, right-click on the game to which you want to apply the specific profile and select "Properties"

<div align="left">

<figure><img src="https://i.imgur.com/eEWCDpa.png" alt=""><figcaption></figcaption></figure>

</div>

In the next screen, select the editor and in the "User Config" section, specify the profile to use

<div align="left">

<figure><img src="https://i.imgur.com/sWKvW1P.png" alt=""><figcaption></figcaption></figure>

</div>

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

<div align="left">

<figure><img src="https://i.imgur.com/r72aRwA.png" alt=""><figcaption></figcaption></figure>

</div>
