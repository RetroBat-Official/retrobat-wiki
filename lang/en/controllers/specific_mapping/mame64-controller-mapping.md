# MAME64 controller mapping

MAME64 emulator is compatible natively with XInput controllers.

When using another type of controllers (or to simply use a specific mapping for a game), it is possible to perform a dedicated mapping within the emulator.

## STEP 0 : Preliminary explanations

MAME standalone will read the controller configuration files in the following ordre of priority (from less priority to highest priority - meaning the last file found will override what is found before):

1. Native controller configuration
2. Default.cfg file located in `\bios\mame\cfg` folder
3. Game specific config files located in `\bios\mame\cfg` folder
4. Controller configuration file located in `\saves\mame\ctrlr` folder as per selection in RetroBat options

## STEP 1 : Create controller mapping file in MAME

Run _mame.exe_, the executable is located in the `emulators\mame` folder of your RetroBat installation.

Click on "General Settings":

<div align="left">

<figure><img src="https://i.imgur.com/7FfrAyr.png" alt=""><figcaption></figcaption></figure>

</div>

Select "Input Assignments"

<div align="left">

<figure><img src="https://i.imgur.com/P23EUU1.png" alt=""><figcaption></figcaption></figure>

</div>

Select the controls you want to assign:

* User Interface section lets you map buttons to actions in the MAME Menu
* Player X Controls allows you to map in-game controls

<div align="left">

<figure><img src="https://i.imgur.com/pgXcIQM.png" alt=""><figcaption></figcaption></figure>

</div>

Map controls as you would like them:

<div align="left">

<figure><img src="https://i.imgur.com/kxVLMtw.png" alt=""><figcaption></figcaption></figure>

</div>

When using left and right buttons (or keys), you can select whether to add a key to the same button or whether to reset the mapping for the control.

<div align="left">

<figure><img src="https://i.imgur.com/ubjsXry.png" alt=""><figcaption><p>You can APPEND</p></figcaption></figure>

</div>

<div align="left">

<figure><img src="https://i.imgur.com/6pGoFrF.png" alt=""><figcaption><p>Are clear and reset</p></figcaption></figure>

</div>

Once the mapping done, go back and click on "Save Settings":

<div align="left">

<figure><img src="https://i.imgur.com/pDLsvFJ.png" alt=""><figcaption></figcaption></figure>

</div>

A file name "default.cfg" has been saved in the `\emulators\mame\cfg` folder.

<div align="left">

<figure><img src="https://i.imgur.com/PmZJO4I.png" alt=""><figcaption></figcaption></figure>

</div>



## STEP 2 : Manage the cfg file

Open the default.cfg file and check the content:

<div align="left">

<figure><img src="https://i.imgur.com/tYgSbfM.png" alt=""><figcaption></figcaption></figure>

</div>

The file has an xml format, the mapping that you have performed is located in the \<input> section of the file.

_In the example, the keyboard key "Q" has been assigned to the action "UI\_MENU" that opens the MAME menu._

Finally, copy the default.cfg file in the `\bios\mame\cfg` folder of your installation : this will now be the default controller configuration.

## STEP 3 : Create a dedicated profile

Proceed as explained in step 1, then rename the file to one of the following values:

* custom1.cfg
* custom2.cfg
* custom3.cfg
* custom4.cfg

Move the file in the `\saves\mame\ctrlr` folder of your RetroBat installation:

<div align="left">

<figure><img src="https://i.imgur.com/15wt2XH.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
You can also perform the mapping directly in the cfg file if you feel comfortable with xml document processing.

Additional information on the file structure can be found here:

[http://mirrors.arcadecontrols.com/easyemu/mameguidenew/mameguide-controlini.htm](http://mirrors.arcadecontrols.com/easyemu/mameguidenew/mameguide-controlini.htm)

[https://docs.mamedev.org/advanced/ctrlr\_config.html](https://docs.mamedev.org/advanced/ctrlr\_config.html)
{% endhint %}

## STEP 4 : Select the controller profile in RetroBat

From the MAME [Game view](../../navigation/system-view-and-game-view.md#game-view), press SELECT to open the [View Options](../../navigation/view-options.md) menu and select "ADVANCED SYSTEM OPTIONS"

<div align="left">

<figure><img src="https://i.imgur.com/Y3mGW33.png" alt=""><figcaption></figcaption></figure>

</div>

Ensure the MAME64 emulator is set as EMULATOR and navigate to the CONTROLS submenu:

<div align="left">

<figure><img src="https://i.imgur.com/3xCkZOg.png" alt=""><figcaption></figcaption></figure>

</div>

Select the "CONTROLLER PROFILE" option and choose the profile used for the file that you have created:

{% hint style="info" %}
RetroBat provides 4 custom profiles as well as the ability to use a per\_game cfg file.

When using "per\_game", the name of the file must match the name of the game file (without extension), for example name the file "wjammers.cfg" for the game file "wjammers.zip" (WindJammers).
{% endhint %}

<div align="left">

<figure><img src="https://i.imgur.com/ltkfOQt.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
Do not hesitate to share the files you have created with the RetroBat team if you have a general profile that can be shared with other users.
{% endhint %}
