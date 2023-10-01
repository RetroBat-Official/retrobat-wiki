# Model2 controller mapping

If the configuration of the buttons does not suit you for a game or if the controller you are using is not correctly autoconfigured, it is possible to create a specific mapping for a game.

Here is how to proceed.



### Create controller configuration

From the RetroBat menu, configure the input driver depending on your controller (use XINPUT for XBOX compatible controllers, DINPUT for others like Dualshock, etc.):

<div align="left">

<figure><img src="https://i.imgur.com/0joCHBX.png" alt=""><figcaption></figcaption></figure>

</div>

Then run the game from within RetroBat, and once in the game press ALT + ENTER to exit fullscreen mode and access the emulator menu:

<div align="left">

<figure><img src="https://i.imgur.com/MdPZYlG.png" alt=""><figcaption></figcaption></figure>

</div>

Go to **Game > Configure Controls**

<div align="left">

<figure><img src="https://i.imgur.com/Zklxxw2.png" alt=""><figcaption></figcaption></figure>

</div>

From there configure the controls as per your preference

<div align="left">

<figure><img src="https://i.imgur.com/mkomNgQ.png" alt=""><figcaption></figcaption></figure>

</div>

Once finished : close the window and quit the emulator.

The game input configuration file is created in the `emulators\m2emulator\CFG`folder :

<div align="left">

<figure><img src="https://i.imgur.com/VzxUIcv.png" alt=""><figcaption></figcaption></figure>

</div>

### Copy the file in the right folder

Depending on the driver that was used when creating the file (DINPUT or XINPUT), the file created in the previous step needs to be copied to the right destination folder:

* `\emulators\m2emulator\templatescfg\dinput` - for dinput driver
* `\emulators\m2emulator\templatescfg\xinput` - for xinputdriver

<div align="left">

<figure><img src="https://i.imgur.com/1OhA1pS.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
RetroBat provides default files that are compatible with XBOX controller for xinput and with Dualshock controller for dinput, you can safely erase these with your newly-created file.
{% endhint %}

### Switch on usage of custom files in RetroBat

Once your configuration file has been placed in the correct folder, run RetroBat and open the model2 advanced system configuration:

<div align="left">

<figure><img src="https://i.imgur.com/vo1MmDF.png" alt=""><figcaption></figcaption></figure>

</div>

Go to CONTROLS and change the settings named "**TYPE OF CONFIGURATION**" to "**TEMPLATES**":

<div align="left">

<figure><img src="https://i.imgur.com/b5XP7Gj.png" alt=""><figcaption></figcaption></figure>

</div>

RetroBat will now use the template you created in previous steps when running the game.
