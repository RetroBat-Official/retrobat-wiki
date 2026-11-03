# Game Control Center

The Game Control Center is an in-game overlay. It gives quick access to information about the game you are playing: box art, description, controls (tattoo), map and manual. It also lets you quit the game.

## Opening the Game Control Center

While playing, press:

* **HOTKEY + East** ![](<../.gitbook/assets/image (287).png>) on the controller,
* or **Ctrl + F12** on the keyboard.

<div align="left"><figure><img src="../.gitbook/assets/image (286).png" alt=""><figcaption></figcaption></figure></div>

While the Game Control Center is open:

<table><thead><tr><th width="169">Button</th><th>Action</th></tr></thead><tbody><tr><td>D-pad</td><td>Move between the buttons</td></tr><tr><td>South</td><td>Validate</td></tr><tr><td>East or North</td><td>Close the Game Control Center and go back to the game</td></tr><tr><td>L1 / R1</td><td>Previous / next page</td></tr></tbody></table>

## Buttons

<table><thead><tr><th width="155.25">Button</th><th>Action</th></tr></thead><tbody><tr><td><strong>Tattoo</strong> / <strong>Box</strong></td><td>Show the controls of the system or game instead of the box art. The button then becomes <strong>Box</strong>: press it to show the box art again</td></tr><tr><td><strong>Map</strong></td><td>Open the game map</td></tr><tr><td><strong>Manual</strong></td><td>Open the game manual (PDF)</td></tr><tr><td><strong>Back to game</strong></td><td>Close the Game Control Center</td></tr><tr><td><strong>Kill emulator</strong></td><td>Quit the emulator and go back to RetroBat</td></tr></tbody></table>

<div align="left"><figure><img src="../.gitbook/assets/image (288).png" alt="" width="563"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (289).png" alt="" width="563"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (290).png" alt="" width="563"><figcaption></figcaption></figure></div>

{% hint style="info" %}
* **Map** and **Manual** are only displayed when the game has these media (downloaded by the [scraper](scraping-and-metadata.md) or added with **EDIT THIS GAME'S METADATA**).
* **Tattoo** is only displayed when a tattoo exists for the system or the game. You can add your own tattoos in `user\tattoos\games\<system>\` (one game) or `user\tattoos\default\` (whole system): see [RetroBat folder structure](../get-started/retrobat-folder-structure.md).
* **Kill emulator** closes the emulator without saving: save your game first, or use **HOTKEY + START** to quit normally.
{% endhint %}

{% hint style="warning" %}
Most emulators pause automatically when the Game Control Center is displayed (MAME, Model 2 and Hypseus are suspended by RetroBat). If **NEVER PAUSE EMULATION ON LOST FOCUS** is enabled in **GAME SETTINGS**, the game may keep running behind the Game Control Center.
{% endhint %}

## Disabling the Game Control Center

The Game Control Center uses the **HOTKEY + East** combination: while it is enabled, this combination cannot be used for another shortcut, in any emulator (see [Hotkeys](hotkeys.md)).

If you do not use it, you can disable it in **MAIN MENU** > **GAME SETTINGS** > **DISABLE GAME CENTER**. **HOTKEY + East** is then free, and you can assign it to another shortcut in the hotkey files (see [Customizing hotkeys](hotkeys.md#customizing-hotkeys)).

<div align="left"><figure><img src="../.gitbook/assets/image (291).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
The Game Control Center is not available for Pinball FX and for Windows games.
{% endhint %}
