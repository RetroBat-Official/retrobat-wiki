# RetroBat Folder Structure

Once RetroBat is installed, the RetroBat installation folder contains the following folders & files:

<div align="left">

<figure><img src="https://i.imgur.com/MwQl2t9.png" alt=""><figcaption></figcaption></figure>

</div>

## bios folder

This folder is where (with few exceptions) all system bios & firmwares will need to be placed.

More on bios files can be found in each [system individual pages](../systems-and-emulators/supported-game-systems/).



## emulators folder

This is the folder where the emulators are installed.

Retroarch is provided by default when installing RetroBat, all other standalone emulators will be downloaded when running a game for the first time or when launching them from the RetroBat menu.

{% hint style="info" %}
Some emulators are not automatically provided with RetroBat automatic download capability, the following list of emulators have to be downloaded manually:

* Yuzu (& early-access)
* Ryujinx
* PICO-8
* 3DSen
* TeknoParrot
{% endhint %}

## library folder

This folder can be used to store magazines, these will appear in RetroBat in a "Library" system and can be viewed within RetroBat using the **imageviewer** libretro core.

## roms folder

This is the folder where the games rom need to be copied, each game has to be placed in the correct system subfolder and must have an extension that is accepted by the emulator.

More information can be found in each [system individual pages](../systems-and-emulators/supported-game-systems/).

## saves folder

This folder contains game saves, whenever you are using the save function in an emulator to save a game's progress.

## screenshots folder

This folder contains all screenshots one takes during gameplay.



{% hint style="info" %}
If you notice that a save or a screenshot is not recorded in the right folder, please contact the RetroBat team that will fix it if possible.
{% endhint %}
