# MAME controller mapping

MAME emulator control mapping is very complexe because each machine it emulates had a different control layout.

RetroBat offers multiple ways to change controller mapping for MAME, as well as libretro-mame. Each method is described in this page.

## MAME (standalone)

RetroBat offers multiple ways to manage MAME controller configuration, either manually, or with automatic configuration:

* RetroBat standard autoconfiguration
* RetroBat xml override files (per-game)
* Specific configuration for special controller types
* Manual Game specific configuration
* Manual Custom configuration

### RetroBat autoconfiguration

By default, RetroBat will try to autoconfigure controls in MAME either by using RetroBat-provided per-game configuration, or by setting a default configuration.

Autoconfiguration can change depending on the controller layout that you specify in **ADVANCED SETTINGS > CONTROLS**:

<div align="left"><figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure></div>

**The default button for each layout is the following:**

**Controller**: this profile is adapted to gamepads, where ![](<../../.gitbook/assets/image (3).png>) is assigned to button 1, ![](<../../.gitbook/assets/image (4).png>) is assigned to button 2, ![](<../../.gitbook/assets/image (5).png>) is assigned to button 3, ![](<../../.gitbook/assets/image (6).png>) is assigned to button 4, L1 to button 5, R1 to button 6, L2 to button 7 and R2 to button 8

**Modern 8 buttons**: this profile is the most common one for modern arcade sticks, upper 4 buttons are buttons 1 (![](<../../.gitbook/assets/image (7).png>)), 2(![](<../../.gitbook/assets/image (8).png>)), 3(R1) and 7(L1), lower 4 buttons are buttons 4(![](<../../.gitbook/assets/image (9).png>)), 5(![](<../../.gitbook/assets/image (10).png>)), 6(R2) and 8(L2)

**Classic 8 buttons**: upper 4 buttons are buttons 1 (![](<../../.gitbook/assets/image (7).png>)), 2(![](<../../.gitbook/assets/image (8).png>)), 3(L1) and 7(L2), lower 4 buttons are buttons 4(![](<../../.gitbook/assets/image (9).png>)), 5(![](<../../.gitbook/assets/image (10).png>)), 6(R1) and 8(R2)

**6 buttons**: similar to classic 8 buttons but without buttons 7 and 8

**8 buttons alternative**: default is the same as Controller mapping

### Per-Game automatic xml overrides

RetroBat ships with adapted per-game configuration, for each of the layouts described above, for approximately 130 games, the override files shipped with RetroBat are located in the `\system\resources\inputmapping\mame` folder:

<div align="left"><figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
You can create your own file and share it with the RetroBat team, or save it in the `\user\inputmapping\mame` folder of your RetroBat installation if you need a variation of the profile provided by RetroBat.
{% endhint %}

The override file is a xml file, almost similar to the MAME format used for its own config files, but with generic button names, that will be converted by RetroBat based on your connected controller and selected profile:

<div align="left"><figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure></div>

Each file contains multiple "_layout_" sections, which corresponds to the available layouts in RetroBat. Based on the selected value in RetroBat controls settings, the corresponding layout from the file will be picked.

Each layout contains the specific button mappings to use for the game, for example the following line means that the **button 3** of the arcade machine "_altbeast_", for the player 1, will be mapped to the **east face button** of the controller when using the _default_ layout:

<div align="left"><figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure></div>

In the same file you can see that this button is mapped to the **R1 button** when using the modern8 layout (which corresponds to the 3rd button of the upper range of the arcade stick):

<div align="left"><figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure></div>

You can use the [same method as described below](mame64-controller-mapping.md#creating-a-specific-controller-configuration-file-for-mame) to create your own mapping file, however you will need to change the button values with the generic ones from RetroBat:

<details>

<summary>List of generic RetroBat button values</summary>

* JOY\_west
* JOY\_north
* JOY\_east
* JOY\_south
* JOY\_down (dpad down)
* JOY\_lsdown (left stick down)
* JOY\_up / JOY\_lsup
* JOY\_left / JOY\_lsleft
* JOY\_right / JOY\_lsright
* JOY\_r1
* JOY\_l1
* JOY\_r2trigger
* JOY\_l2trigger
* JOY\_r3
* JOY\_l3
* JOY\_leftstickx (left stick horizontal axis) / JOY\_rightstickx
* JOY\_leftsticky (left stick vertical axis) / JOY\_leftstickx
* JOY\_lsup / JOY\_lsdown / JOY\_lsleft / JOY\_lsright (left stick directions)

It is also possible to add "reverse" after and axis in order to set \_REVERSE in MAME config file.

</details>

### Using manual specific configuration

Use the following setting in RetroBat **ADVANCED SETTINGS > CONTROLS** menu to enable specific configuration:

<div align="left"><figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure></div>

All the settings other than RetroBat Auto can be used to point MAME to use a controller config file in the `\saves\mame\ctrlr\` folder of your retrobat installation.

RetroBat ships with 2 files, one for the IPAC2 controller and one for the X-Arcade TankStick controller, if you own one of these controllers, you can use these options to autoconfigure these.

The other profiles can be used to point to files that you need to create, either custom files, or per-game files (named after the game rom). Such files are not provided with RetroBat and need to be created, here is the procedure:

### Creating a specific controller configuration file for MAME

#### STEP 1 : Preliminary explanations

MAME standalone will read the controller configuration files in the following ordre of priority (from less priority to highest priority - meaning the last file found will override what is found before):

1. Native controller configuration
2. Default.cfg file located in `\bios\mame\cfg` folder
3. Game specific config files located in `\bios\mame\cfg` folder
4. Controller configuration file located in `\saves\mame\ctrlr` folder as per selection in RetroBat options

#### STEP 2 : Create controller mapping file in MAME

Run _mame.exe_, the executable is located in the `emulators\mame` folder of your RetroBat installation.

Click on "General Settings":

<div align="left"><figure><img src="https://i.imgur.com/7FfrAyr.png" alt=""><figcaption></figcaption></figure></div>

Select "Input Assignments"

<div align="left"><figure><img src="https://i.imgur.com/P23EUU1.png" alt=""><figcaption></figcaption></figure></div>

Select the controls you want to assign:

* User Interface section lets you map buttons to actions in the MAME Menu
* Player X Controls allows you to map in-game controls

<div align="left"><figure><img src="https://i.imgur.com/pgXcIQM.png" alt=""><figcaption></figcaption></figure></div>

Map controls as you would like them:

<div align="left"><figure><img src="https://i.imgur.com/kxVLMtw.png" alt=""><figcaption></figcaption></figure></div>

When using left and right buttons (or keys), you can select whether to add a key to the same button or whether to reset the mapping for the control.

<div align="left"><figure><img src="https://i.imgur.com/ubjsXry.png" alt=""><figcaption><p>You can APPEND</p></figcaption></figure></div>

<div align="left"><figure><img src="https://i.imgur.com/6pGoFrF.png" alt=""><figcaption><p>Are clear and reset</p></figcaption></figure></div>

Once the mapping done, go back and click on "Save Settings":

<div align="left"><figure><img src="https://i.imgur.com/pDLsvFJ.png" alt=""><figcaption></figcaption></figure></div>

A file name "default.cfg" has been saved in the `\emulators\mame\cfg` folder.

<div align="left"><figure><img src="https://i.imgur.com/PmZJO4I.png" alt=""><figcaption></figcaption></figure></div>



#### STEP 3 : Manage the cfg file

Open the default.cfg file and check the content:

<div align="left"><figure><img src="https://i.imgur.com/tYgSbfM.png" alt=""><figcaption></figcaption></figure></div>

The file has an xml format, the mapping that you have performed is located in the \<input> section of the file.

_In the example, the keyboard key "Q" has been assigned to the action "UI\_MENU" that opens the MAME menu._

Finally, copy the default.cfg file in the `\bios\mame\cfg` folder of your installation : this will now be the default controller configuration.

#### STEP 4 : Create a dedicated profile

Proceed as explained in step 1, then rename the file to one of the following values:

* custom1.cfg
* custom2.cfg
* custom3.cfg
* ...
* custom8.cfg

Move the file in the `\saves\mame\ctrlr` folder of your RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/15wt2XH.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
You can also perform the mapping directly in the cfg file if you feel comfortable with xml document processing.

Additional information on the file structure can be found here:

[http://mirrors.arcadecontrols.com/easyemu/mameguidenew/mameguide-controlini.htm](http://mirrors.arcadecontrols.com/easyemu/mameguidenew/mameguide-controlini.htm)

[https://docs.mamedev.org/advanced/ctrlr\_config.html](https://docs.mamedev.org/advanced/ctrlr_config.html)
{% endhint %}

#### STEP 5 : Select the controller profile in RetroBat

From the MAME [Game view](../../navigation/system-view-and-game-view.md#game-view), press SELECT to open the [View Options](../../navigation/view-options.md) menu and select "ADVANCED SYSTEM OPTIONS"

<div align="left"><figure><img src="https://i.imgur.com/Y3mGW33.png" alt=""><figcaption></figcaption></figure></div>

Ensure the MAME64 emulator is set as EMULATOR and navigate to the CONTROLS submenu:

<div align="left"><figure><img src="https://i.imgur.com/3xCkZOg.png" alt=""><figcaption></figcaption></figure></div>

Select the "CONTROLLER PROFILE" option and choose the profile used for the file that you have created:

{% hint style="info" %}
RetroBat provides 8 custom profiles as well as the ability to use a per\_game cfg file.

When using "per\_game", the name of the file must match the name of the game file (without extension), for example name the file "wjammers.cfg" for the game file "wjammers.zip" (WindJammers).
{% endhint %}

<div align="left"><figure><img src="https://i.imgur.com/mD9Dn89.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Do not hesitate to share the files you have created with the RetroBat team if you have a general profile that can be shared with other users.
{% endhint %}
