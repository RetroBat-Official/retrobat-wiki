# Configuration of systems and games

The main advantage of using RetroBat over other front-ends or standalone emulators, is that all configuration can be managed directly from within RetroBat.

This means that, as a user, one should not have to open an emulator to access to its configuration.

{% hint style="danger" %}
Trying to manage configuration directly within the emulator will often end up with all the configuration being overwritten by RetroBat when running a game, as the default values set in RetroBat will be passed to the emulator.
{% endhint %}



The configuration elements available in RetroBat are called "features", they have the advantage that they can be set at 2 level:

* Globally for a system
* Per-game



## How to access the configuration screen:

The features menu is available from the "[View Options](view-options.md)" menu or from the "[Game Options](game-options.md)" menu:

#### when selecting the **ADVANCED SYSTEM OPTIONS** submenu:

<div align="left">

<figure><img src="https://i.imgur.com/NTx2K4c.png" alt=""><figcaption><p>How to access features from the VIEW OPTIONS</p></figcaption></figure>

</div>

\==> This will enable configuration for all games of the selected system.



#### when selecting the ADVANCED GAME OPTIONS submenu

<div align="left">

<figure><img src="https://i.imgur.com/lJNGWGh.png" alt=""><figcaption></figcaption></figure>

</div>

\==> This will enable configuration for the specified game only.



It is very important to note that the more detailed option will always be the option passed to the emulator, this means that the option set for a specific game will be used over the option set at system-level.

## The configuration options

The features available depend on the selected emulator, as they do not have the same options.

This means that for a same system, when changing the emulator, the available features will not be identical.



In most of the cases, the features will be grouped within 2 subgroups:

* General Settings
* Advanced Settings

<div align="left">

<figure><img src="https://i.imgur.com/mcSBHUD.png" alt=""><figcaption><p>Example of settings for NES with FCEUMM core</p></figcaption></figure>

</div>

### General Settings

The **General Settings** will give you access to the following configuration options, they exist for most of the emulators:

* Shaders to apply
* Bezels (decorations) to apply
* Game aspect ratio and resolution
* Vsync
* Pixel Perfect
* Disabling controller autoconfiguration (this option is on by default)



### Advanced Settings

These features will be far more specific, they are arranged in the following submenus:

* EMULATION : contains features such as language, machine emulated, region but also performance options available for the emulator
* VIDEO : General video options such as monitor index, output signal, screen orientation, ...
* SCREEN SYNC : usually containing options to avoid tearing like advanced vsync features
* VISUAL RENDERING: contains various screen effect features, upscaling configuration, anti-aliasing options...
* AUDIO : general audio settings, like sample rate, low-pass filter...
* LATENCY REDUCTION : options to reduce input lag
* USER INTERFACE : contains features such as FPS display, enabling or disabling emulator notifications...
* DRIVERS : options to change video, audio, controller drivers used by the emulator
* CONTROLS : options related with controls such as the type of joystick, lightgun options...

<div align="left">

<figure><img src="https://i.imgur.com/hGdcInG.png" alt=""><figcaption><p>Example of EMULATION features submenu for FCEUMM core</p></figcaption></figure>

</div>



In addition, some emulators will have specific submenus, this is the case for example for pcsx2 features, that have a MANUAL HACK and a GAME FIXES submenus:

<div align="left">

<figure><img src="https://i.imgur.com/Mw3E0dB.png" alt=""><figcaption></figcaption></figure>

</div>

or for the PORTS that have a dedicated per-game setting:

<div align="left">

<figure><img src="https://i.imgur.com/nCX1t0V.png" alt=""><figcaption></figcaption></figure>

</div>



## How does the magic work ?

The trick that makes all of this possible is simple : before launching the game, RetroBat will go through the options that have been set by the users, and apply these settings directly in the emulator configuration file, before running the emulator.



As an example, let's take the case of a user that needs to change the video driver to VULKAN for the duckstation emulator.

Once in the system configuration options screens

<div align="left">

<figure><img src="https://i.imgur.com/HkFOJoU.png" alt=""><figcaption></figcaption></figure>

</div>

Select the **DRIVERS** submenu in the **ADVANCED SETTINGS** group:

<div align="left">

<figure><img src="https://i.imgur.com/qthtyR1.png" alt=""><figcaption></figcaption></figure>

</div>



Then change the **VIDEO DRIVER** option to "VULKAN":

<div align="left">

<figure><img src="https://i.imgur.com/xaeKGGB.png" alt=""><figcaption></figcaption></figure>

</div>

When running a game with the duckstation emulator, RetroBat will now automatically set the following value in the Duckstation settings file before launching the game:

<div align="left">

<figure><img src="https://i.imgur.com/yYUfic3.png" alt=""><figcaption></figcaption></figure>

</div>

Et voilà !

## Great, but what does the value "AUTO" mean ?

The value "AUTO" has different meaning whether you are configuring the features at system level or at game level.

At system level, the value "AUTO" is a default value that RetroBat will set as the target option value, the RetroBat Team has usually defined the most commonly used value as default value or the most relevant for best user-experience.

At game level configuration, the value "AUTO" means that the default value set for the system/emulator should be used.

{% hint style="info" %}
Note that the "per-game" setting will take precedence over the general setting.
{% endhint %}

## Fine, but i do not see an option that i need to set !

Do not panic, if there is an option within an emulator that you wish to change, do not hesitate to contact the RetroBat team, that will include this option in the next release !

In the meantime, options that are not available in RetroBat can be changed directly in the emulator, they are usually not overwritten by RetroBat...
