# RetroArch controller mapping

RetroArch controller mapping is very specific, before going into details, it is important to understand the general RetroArch mapping principles.

## RetroArch mapping principle

Information on how RetroArch manages controls can be found here:

{% embed url="https://docs.libretro.com/guides/input-and-controls/" %}

RetroArch has a 2-step approach with controllers mapping:

* Step 1: mapping of your physical gamepad with RetroArch "RetroPad"
* Step 2: mapping of the Retropad with the original console or computer game controller

<div align="left"><figure><img src="../../.gitbook/assets/retroarch remap principle.png" alt=""><figcaption></figcaption></figure></div>

The guide in this page mostly treats about the second step, as it is assumed that RetroBat is passing all your physical gamepad buttons to RetroArch (this should always be the case if you have correctly configured your controller in RetroBat).

#### General Binding

The mapping done in Step 1 can be found in the following section of RetroArch configuration:

<div align="left"><figure><img src="https://i.imgur.com/rdZbOuz.png" alt="" width="375"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (2) (1) (1).png" alt="" width="375"><figcaption></figcaption></figure></div>

{% hint style="info" %}
General binding is stored in the "**retroarch.cfg**" file located in `/emulators/retroarch`
{% endhint %}

#### Remap

The remap information (step 2) can be found in the Quick Settings menu of RetroArch, while a core is running:

<div align="left"><figure><img src="../../.gitbook/assets/image (2) (1).png" alt="" width="294"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1).png" alt="" width="342"><figcaption></figcaption></figure></div>

{% hint style="info" %}
Remap files are saved as .rmp files in `/emulators/retroarch/config/remaps` folder.
{% endhint %}

## How to change mapping for RetroArch when using RetroBat ?

RetroBat allows multiple ways to modify mapping of your controller in RetroArch, the wiki will guide you through the following methods:

* [Manually saving a remap file for a game](retroarch-controller-mapping.md#manually-create-a-remap-file-for-a-game) (remap)
* [Using a YAML core override file](retroarch-controller-mapping.md#using-a-core-override-remap-file) (remap)
* [Forcing a controller binding configuration](retroarch-controller-mapping.md#force-a-controller-binding-configuration) (change controller binding)
* [Enabling a special controller type](retroarch-controller-mapping.md#enable-a-special-controller-type) (for some systems/cores only)
* [Using a different input layout provided by RetroBat](retroarch-controller-mapping.md#use-a-pre-defined-layout)

### Manually create a remap file for a game

Open RetroBat and launch the game for which you require a specific remapping.

Once in the game, press SELECT + ![](<../../.gitbook/assets/image (30).png>) buttons simultaneously to open the RetroArch menu, and select **Quick Menu**:

<div align="left"><figure><img src="https://i.imgur.com/HiJ66mI.png" alt=""><figcaption></figcaption></figure></div>

In the QUICK MENU list, you will find " **Controls** "

<div align="left"><figure><img src="https://i.imgur.com/8jpwjmZ.png" alt=""><figcaption></figcaption></figure></div>

From there, proceed with the required remapping:

<div align="left"><figure><img src="https://i.imgur.com/k78mZCY.png" alt=""><figcaption></figcaption></figure></div>

In this example, i have mapped the RetroPad left analog up input to the key defined for A in RetroBat (which is W on my keyboard):

<div align="left"><figure><img src="https://i.imgur.com/yTnHq8K.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Note that you can only remap the keys that have been passed by RetroBat to retroArch based on your controller.
{% endhint %}

Once the mapping is performed, exit and go back to the **CONTROLS** menu, then select the "_Manage Remap Files_" option:

<div align="left"><figure><img src="https://i.imgur.com/g5xiFro.png" alt=""><figcaption></figcaption></figure></div>

In the next submenu, save the remap file for the game (it will apply to this game only)

<div align="left"><figure><img src="https://i.imgur.com/4WyqBdQ.png" alt=""><figcaption></figcaption></figure></div>

Once saved, the new remap will now be used next time you run the game.

{% hint style="info" %}
You cannot use the option to "save for core", as this would automatically be erased by RetroBat upon next launch.
{% endhint %}

### Using a core override remap file

Read [this chapter](../controller-configuration.md#file-override-general-principle) for general information.

RetroArch core remap files provided with RetroBat are located in the `\system\resources\inputmapping` folder of your RetroBat installation, they start with the "**libretro\_**" prefix.

The logic RetroBat uses to find a file is the following:

1. Search in `\user\inputmapping` for a file named **libretro\_\<core>\_\<system>.yml**
2. Search in `\user\inputmapping` for a file named **libretro\_\<core>.yml**
3. Search in `\user\inputmapping` for a file named **libretro.yml**
4. Search in `\system\resources\inputmapping` for a file named **libretro\_\<core>\_\<system>.yml**
5. Search in `\system\resources\inputmapping` for a file named **libretro\_\<core>.yml**
6. Search in `\system\resources\inputmapping` for a file named **libretro.yml**

If a yaml file is found, RetroBat reads the file and searches for a container matching the name of the game rom file:

<div align="left"><figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure></div>

If no container exists for the game, RetroBat tries to get the "default" container:

<div align="left"><figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
For arcade systems, a single game can have multiple layouts based on the option set in RetroBat interface ADVANCED SETTINGS > CONTROLS:

![](<../../.gitbook/assets/image (6) (1).png>)

RetroBat will first look for the container with the selected layout, before falling back to the game specific container:

![](<../../.gitbook/assets/image (7) (1).png>)
{% endhint %}

When a specific container is found, RetroBat automatically generates and modifies the core remap file when running a game, which automatically applies the selected remap:

<div align="left"><figure><img src="../../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure></div>

### Force a controller binding configuration

It is possible to force a controller with a specific binding in RetroArch, this is useful in case a specific controller would not be correctly configured by RetroBat or in case it is unknownn by RetroArch but working correctly when perforing a manual mapping in RetroArch binding options.

RetroBat ships with a specificfile named "**retroarch\_controller.json**" located in the `\system\resources\inputmapping` folder of the RetroBat installation.

This file is a json-formatted file, it contains the exact mapping required in the `retroarch.cfg` file based on the controller SDL guid:

<div align="left"><figure><img src="../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure></div>

The above example is for the NSO N64 controller, the different values required in the file are the following:

* **Name**: for information only
* **Guid**: allows RetroBat to enable the specific mapping based on the connected controller (the SDL GUID of the controller can be found in the es\_input.cfg file or in the emulatorlauncher.log after having launched a game). Multiple guids can be entered if a controller has multiple revisions.
* **Driver**: can be used if the RetroArch mapping is different depending on the selected Joyapd Driver in RetroArch, possible values are : sdl2 (RetroBat default), xinput, dinput
* **Mapping**: the actual mapping to be set in `retroarch.cfg file`, for each button. In order to know the mapping for the controller, perform the configuration manually by running retroarch.exe, exit retroarch, and open the retroarch.cfg file, search for the lines starting with input\_player1\_ and ending with btn or axis.
* **HotkeyMapping**: the mapping for hotkeys for the controller
* **ControllerInfo**: can be used to adjust analog sensitivity or for other specific purposes (ask the RetroBat team if a feature is required)

{% hint style="info" %}
Do not hesitate to share with the RetroBat team any specific controller mapping that you have created.
{% endhint %}

### Enable a special controller type

Look at [this wiki page](../supported-controllers/gamepads/special-controllers.md) for more details.

### Use a pre-defined layout

RetroBat does offer, for multiple systems, the ability to change the button mapping layout.

The option can usually be found in the RetroBat **advanced settings > controls** menu:

<div align="left"><figure><img src="../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../.gitbook/assets/image (11) (1).png" alt="" width="245"><figcaption><p>Example for megadrive</p></figcaption></figure></div>

More information about the different layouts can be found on the [page for the system](../../systems-and-emulators/supported-game-systems/).
