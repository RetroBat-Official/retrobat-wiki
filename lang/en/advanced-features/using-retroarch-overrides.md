# Using RetroArch overrides

If you do not want to use RetroBat configuration for RetroArch global settings or shader configuration, RetroBat offers a way to automatically load the configuration and/or shader override files that you would have created in RetroArch.

### RetroArch configuration override <a href="#override-pour-les-options" id="override-pour-les-options"></a>

You can save an override file for a game, a content folder or a libretro core from the RetroArch quick menu.

{% hint style="warning" %}
First enable **ALLOW GAME/CORE OPTIONS OVERRIDE** in RetroBat (**MAIN MENU > GAME SETTINGS > RETROARCH OPTIONS > EMULATION**), **before** launching the game: otherwise the **Overrides** menu is hidden in RetroArch.
{% endhint %}

Enable the override option in RetroBat [MAIN MENU > GAME SETTINGS > RETROARCH OPTIONS > EMULATION](../navigation/main-menu.md#game-settings)

<div align="left"><figure><img src="https://i.imgur.com/2HGsEHB.png" alt=""><figcaption></figcaption></figure></div>

In order to save a configuration override file, open the RetroArch quick menu by pressing **HOTKEY + SOUTH** ![](https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2F466894649-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FCgoewyw8Sagl6SNUMrCG%252Fuploads%252FcFYw1e2sB0jT0mUZIx7S%252Fimage.png%3Falt%3Dmedia%26token%3Df8809c2a-5024-4c4f-b2c3-756897352eb1\&width=300\&dpr=4\&quality=100\&sign=c3cf2a80\&sv=2) on your controller (F1 on keyboard). Perform all required RetroArch general settings, then open the "**Overrides**" menu:

<div align="left"><figure><img src="https://i.imgur.com/yyJIMcH.png" alt=""><figcaption></figcaption></figure></div>

In this menu, save the override file at the desired level (game, core, content folder):

<div align="left"><figure><img src="https://i.imgur.com/xKQ4OGt.png" alt=""><figcaption></figcaption></figure></div>

RetroArch will automatically save an override configuration file in the Core config folder:

<div align="left"><figure><img src="../.gitbook/assets/image (421).png" alt=""><figcaption></figcaption></figure></div>

The overrides are saved in `emulators\retroarch\config\<core name>\`:

* `<game name>.cfg`: game override (highest priority);
* `<folder name>.cfg`: content folder override;
* `<core name>.cfg`: core override.

{% hint style="info" %}
RetroBat removes the controller and hotkey settings from the override files, so that they do not replace the automatic controller configuration of RetroBat.
{% endhint %}

### Shaders Overrides <a href="#override-pour-les-shaders" id="override-pour-les-shaders"></a>

You can save a shader preset for a game, a content folder, a core or for everything (global) from the RetroArch quick menu.

{% hint style="info" %}
Without **ALLOW GAME/CORE SHADERS OVERRIDE**, RetroBat applies its own **SHADER SET** and ignores the RetroArch presets. With this option, a preset saved in RetroArch replaces the SHADER SET chosen in RetroBat.
{% endhint %}

In order to save a Shaders override file,open the RetroArch quick menu by pressing **HOTKEY + SOUTH** ![](https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2F466894649-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FCgoewyw8Sagl6SNUMrCG%252Fuploads%252FcFYw1e2sB0jT0mUZIx7S%252Fimage.png%3Falt%3Dmedia%26token%3Df8809c2a-5024-4c4f-b2c3-756897352eb1\&width=300\&dpr=4\&quality=100\&sign=c3cf2a80\&sv=2) on your controller (F1 on the keyboard). Than open the **Shaders** menu to manage the settings:

<div align="left"><figure><img src="https://i.imgur.com/mrTZlVU.png" alt=""><figcaption></figcaption></figure></div>

Once the settings done, open the "**Save Preset**" submenu:

<div align="left"><figure><img src="https://i.imgur.com/7d9sFd3.png" alt=""><figcaption></figcaption></figure></div>

Save at the desired level (folder, core, game, global):

<div align="left"><figure><img src="../.gitbook/assets/image (422).png" alt=""><figcaption></figcaption></figure></div>

RetroArch will automatically save the shaders configuration in a file :

![](https://wiki.retrobat.org/~gitbook/image?url=https%3A%2F%2Fi.imgur.com%2FY0KTSXc.png\&width=768\&dpr=4\&quality=100\&sign=16457507\&sv=2)

Finally, enable the Shaders override option in RetroBat [MAIN MENU > GAME SETTINGS > RETROARCH OPTIONS > VISUAL RENDERING](../navigation/main-menu.md#game-settings):

<div align="left"><figure><img src="https://i.imgur.com/jZ0c4fc.png" alt=""><figcaption></figcaption></figure></div>

### RetroArch custom Aspect Ratio override <a href="#override-pour-les-options" id="override-pour-les-options"></a>

When using the "custom" aspect ratio value in **ADVANCED SETTINGS > GAME ASPECT RATIO**, it is possible to force the value of the ratio to apply in RetroArch by creating a .txt file with the following information:

* width
* height
* top
* left

The information from the file will automatically fill the following values in RetroArch:

<div align="left"><figure><img src="../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure></div>

To do so, create a text file containing the width, height, left and top position of the picture, in this format:

```json
{ "width": 1440, "height": 1080, "left": 240, "top": 0 }
```

Place the file with the right name in one of these locations:

<table><thead><tr><th width="258.5">Location</th><th width="275.75">File name</th><th>For</th></tr></thead><tbody><tr><td>Game folder (<code>roms\&#x3C;system></code>)</td><td><code>&#x3C;romname>_customratio.txt</code></td><td>One game</td></tr><tr><td>Game folder (<code>roms\&#x3C;system></code>)</td><td><code>&#x3C;system>_customratio.txt</code></td><td>The whole system</td></tr><tr><td><code>user\customratio</code> folder of RetroBat</td><td><code>&#x3C;system>_&#x3C;romname>_customratio.txt</code></td><td>One game</td></tr><tr><td><code>user\customratio</code> folder of RetroBat</td><td><code>&#x3C;system>_customratio.txt</code></td><td>The whole system</td></tr></tbody></table>

{% hint style="warning" %}
The file must keep exactly this format (braces, quotes, commas): a badly formatted file is ignored.
{% endhint %}

Finally, enable the "custom" aspect ratio value in RetroBat:

<div align="left"><figure><img src="../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure></div>
