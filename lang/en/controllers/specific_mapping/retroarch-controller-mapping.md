# RetroArch controller mapping

If the configuration of the buttons does not suit you for a game or a system managed by Retroarch (libretro cores), it is possible to create a specific mapping for a game.

Here is how to proceed.

## Remap Retroarch controls for a game

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

Should you need to add new keys that were not configured in RetroBat, you would need to also change the mapping in the general settings of RetroArch.

([click here to find this option](retroarch-controller-mapping.md#retroarch-mapping-principle))
{% endhint %}

Once the mapping is performed, exit and go back to the **CONTROLS** menu, then select the "_Manage Remap Files_" option:

<div align="left"><figure><img src="https://i.imgur.com/g5xiFro.png" alt=""><figcaption></figcaption></figure></div>

In the next submenu, save the remap file for the game (it will apply to this game only)

Once saved, the new remap will now be used next time you run the game.

{% hint style="info" %}
You cannot use the option to "save for core", as this would automatically be erased by RetroBat upon next launch.
{% endhint %}

<div align="left"><figure><img src="https://i.imgur.com/4WyqBdQ.png" alt=""><figcaption></figcaption></figure></div>

## Remap Retroarch Hotkeys

If you want to change the assignment of Retroarch hotkeys to controller or keyboard buttons, RetroBat offers a way to do so by appending dedicated files, here is how to proceed.

Template files can be found in the `\system\resources\inputmapping\` folder of your RetroBat installation:

<div align="left"><figure><img src="https://i.imgur.com/7arWxJQ.png" alt=""><figcaption></figcaption></figure></div>

The file **retroarch\_controller\_hotkeys.yml** can be used to overwrite controller hotkeys assignment, and the file **retroarch\_kb\_hotkeys.yml** to overwrite keyboard hotkeys.

### Remap controller hotkeys

Copy the file **retroarch\_controller\_hotkeys.yml** to the `\user\inputmapping\` folder of your RetroBat installation.

Open the file with your preferred text editor.

<div align="left"><figure><img src="https://i.imgur.com/56fMWG9.png" alt=""><figcaption></figcaption></figure></div>

The file is a yml-formatted file, by default all values are commented.

The first thing to do is to uncomment the actual section where the buttons are defined, as well as the container section, this is done by removing the # character on all lines after the `#default:` line, including the latter:

<div align="left"><figure><img src="https://i.imgur.com/sKvwNrH.png" alt=""><figcaption></figcaption></figure></div>

In this example, we will replace the **fast-forward** and **rewind** hotkeys with R1 and L1 buttons, and move the **disk\_eject** and **ai\_service** to the d-pad:

to do this, just assign the **rewind** feature to pageup (L1) and the **hold\_fast\_forward** to pagedown (R1), and then assign the **disk\_eject\_toggle** and **ai\_service** to their respective d-pad buttons (left & right):

<div align="left"><figure><img src="https://i.imgur.com/2ChUyvp.png" alt=""><figcaption></figcaption></figure></div>

Now save the file:

<div align="left"><figure><img src="https://i.imgur.com/FuOpezx.png" alt=""><figcaption></figcaption></figure></div>

Next time you run a game, the hotkeys will be the ones defined in the file:

<div align="left"><figure><img src="https://i.imgur.com/QngnHVJ.png" alt=""><figcaption></figcaption></figure></div>

In addition, it is also possible to perform a specific hotkey mapping for a single retroarch core, in this example, the mapping is different between the flycast core, by using toggle instead of hold for fast forward:

<div align="left"><figure><img src="https://i.imgur.com/74WCTF9.png" alt=""><figcaption></figcaption></figure></div>

### Remap keyboard hotkeys

Copy the file **retroarch\_kb\_hotkeys.yml** to the `\user\inputmapping\` folder of your RetroBat installation.

Open the file with your preferred text editor.

<div align="left"><figure><img src="https://i.imgur.com/3PElZkI.png" alt=""><figcaption></figcaption></figure></div>

The file is a yml-formatted file, by default all values are commented.

The first thing to do is to uncomment the actual section where the buttons are defined, as well as the container section, this is done by removing the # character on all lines after the `#default:` line, including the latter:

<div align="left"><figure><img src="https://i.imgur.com/Iw4cFSw.png" alt=""><figcaption></figcaption></figure></div>

In this example, we will replace the **fast-forward** and **rewind** hotkeys with F9 and F10 keys:

to do this, just assign the **rewind** feature to F9 and the **hold\_fast\_forward** to F10:

<div align="left"><figure><img src="https://i.imgur.com/TEFpuRj.png" alt=""><figcaption></figcaption></figure></div>

Now save the file:

<div align="left"><figure><img src="https://i.imgur.com/jpb23KY.png" alt=""><figcaption></figcaption></figure></div>

Next time you run a game, the hotkeys will be the ones defined in the file:

<div align="left"><figure><img src="https://i.imgur.com/pqvfj3r.png" alt=""><figcaption></figcaption></figure></div>

In addition, it is also possible to perform a specific hotkey mapping for a single retroarch core, in this example, the mapping is different between the flycast core, by using toggle instead of hold for fast forward:

<div align="left"><figure><img src="https://i.imgur.com/7MvE8bh.png" alt=""><figcaption></figcaption></figure></div>

## Additional information

### Location of the the remap file

Remap files are stored in the following folder of your RetroBat installation:

`\emulators\retroarch\config\remaps\<core shortname>\`

<div align="left"><figure><img src="https://i.imgur.com/ljP0sMO.png" alt=""><figcaption></figcaption></figure></div>

_As you can see in this example: the value for "input\_player1\_stk\_l\_y-" is the value 8 (which corresponds to the change i have done above)._

### RetroArch mapping principle

Information on how RetroArch manages controls can be found here:

{% embed url="https://docs.libretro.com/guides/input-and-controls/" %}

RetroArch has a 2-step approach with controllers mapping:

* Step 1: mapping of your physical gamepad with RetroArch "RetroPad"
* Step 2: mapping of the Retropad with the original console or computer game controller

The guide in this page only treats about the second step, as it is assumed that RetroBat is passing all your physical gamepad buttons to RetroArch (this should always be the case if you have correctly configured your controller in RetroBat).



The mapping done in Step 1 can be found in the following section of RetroArch configuration:

<div align="left"><figure><img src="https://i.imgur.com/rdZbOuz.png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Changing the Step 1 mapping is not recommended, moreover the mapping would automatically be overwritten by RetroBat upon next launch of RetroArch.
{% endhint %}

