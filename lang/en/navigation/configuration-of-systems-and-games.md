# Configuration of systems and games

One of the main advantages of RetroBat is that emulators are configured **from the RetroBat menus**, for all games, for a system or for a single game. You do not need to open the emulators to configure them.

{% hint style="danger" %}
Do not change in an emulator a setting that is also available in RetroBat: RetroBat writes its own value in the emulator configuration each time a game is launched, so your change will be overwritten. See How does it work?
{% endhint %}

## The three configuration levels

The settings available in RetroBat are called **features**. They can be defined at three levels:

<table><thead><tr><th width="102">Level</th><th width="395.5">Where</th><th>Applies to</th></tr></thead><tbody><tr><td><strong>Global</strong></td><td><strong>MAIN MENU</strong> > <strong>GAME SETTINGS</strong></td><td>All systems and games</td></tr><tr><td><strong>System</strong></td><td>Game View > <strong>SELECT</strong> (<a href="view-options.md">View options</a>) > <strong>ADVANCED SYSTEM OPTIONS</strong></td><td>All games of the system</td></tr><tr><td><strong>Game</strong></td><td>Game View > hold <strong>South</strong> on a game (<a href="game-options.md">Game options</a>) > <strong>ADVANCED GAME OPTIONS</strong></td><td>This game only</td></tr></tbody></table>

**The most specific setting always wins:** a game setting overrides the system setting, which overrides the global setting.

{% hint style="info" %}
Only the most common settings (shader, decorations, aspect ratio, integer scaling, controller autoconfiguration…) exist at the global level. Emulator-specific settings are only available at the system and game levels.
{% endhint %}

## Opening the configuration

### For a system

In the Game View of the system, press **SELECT** and choose **ADVANCED SYSTEM OPTIONS**:

<div align="left"><figure><img src="../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure></div>

The settings will apply to all games of this system.

### For a game

In the Game View, hold **South** on the game and choose **ADVANCED GAME OPTIONS** (or press **North** in the Game Options menu):

<div align="left"><figure><img src="../.gitbook/assets/image (248).png" alt=""><figcaption></figcaption></figure></div>

The settings will only apply to this game.

## The configuration menu

<div align="left"><figure><img src="../.gitbook/assets/image (251).png" alt=""><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../.gitbook/assets/image (250).png" alt=""><figcaption></figcaption></figure></div>

The menu always starts with the **EMULATOR** line: choose the emulator and core to use. **Change the emulator first**: the menu is reloaded and shows the settings available for the selected emulator. Each emulator has its own settings, so the list changes from one emulator to another.

The settings are then grouped as follows:

<table><thead><tr><th width="250.25">Group</th><th>Content</th></tr></thead><tbody><tr><td><strong>GENERAL SETTINGS</strong></td><td>Settings available for most emulators: shader, decorations (bezels) and tattoo, aspect ratio, video mode, integer scaling, smoothing…</td></tr><tr><td><strong>ADVANCED SETTINGS</strong></td><td>Settings specific to the emulator or core, organized in submenus (see below)</td></tr><tr><td><strong>PORT SETTINGS</strong></td><td>For ports: settings of the selected game</td></tr></tbody></table>

The most common **ADVANCED SETTINGS** submenus are:

<table><thead><tr><th width="222.75">Submenu</th><th>Content</th></tr></thead><tbody><tr><td><strong>EMULATION</strong></td><td>Emulated machine, region, language, BIOS, performance…</td></tr><tr><td><strong>VIDEO</strong></td><td>Fullscreen, monitor index, screen orientation…</td></tr><tr><td><strong>VISUAL RENDERING</strong></td><td>Upscaling, texture filtering, anti-aliasing, screen effects…</td></tr><tr><td><strong>SCREEN SYNC</strong></td><td>V-Sync and other synchronization settings</td></tr><tr><td><strong>AUDIO</strong></td><td>Audio settings (sample rate, filters…)</td></tr><tr><td><strong>LATENCY REDUCTION</strong></td><td>Settings to reduce input lag</td></tr><tr><td><strong>USER INTERFACE</strong></td><td>FPS display, emulator notifications…</td></tr><tr><td><strong>DRIVERS</strong></td><td>Video, audio and controller drivers</td></tr><tr><td><strong>CONTROLS</strong></td><td>Controller type, analog sticks, mappings…</td></tr><tr><td><strong>GUNS</strong> / <strong>WHEELS</strong></td><td>Lightgun and steering wheel settings</td></tr><tr><td><strong>TURBO</strong></td><td>Turbo buttons</td></tr><tr><td><strong>GAME PATCHES</strong> / <strong>GAME FIXES</strong> / <strong>MANUAL HACKS</strong></td><td>Patches and fixes for specific games</td></tr></tbody></table>

<div align="left"><figure><img src="../.gitbook/assets/image (252).png" alt=""><figcaption><p>Example of EMULATION features submenu for FCEUMM core</p></figcaption></figure></div>

Some emulators have their own submenus, for example **MANUAL HACKS** and **GAME FIXES** for PCSX2:

<div align="left"><figure><img src="../.gitbook/assets/image (253).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Select a setting to display its description at the bottom of the screen.
{% endhint %}

## What does "AUTO" mean?

<table><thead><tr><th width="164">Level</th><th>AUTO means…</th></tr></thead><tbody><tr><td>Global</td><td>The default value chosen by the RetroBat team, usually the most compatible one</td></tr><tr><td>System</td><td>The global value if there is one, otherwise the RetroBat default value</td></tr><tr><td>Game</td><td>The value set for the system</td></tr></tbody></table>

To cancel a setting, set it back to **AUTO**.

## How does it work?

When you change a setting, RetroBat saves it in the `emulationstation\.emulationstation\es_settings.cfg` file.

When you launch a game, RetroBat:

1. reads the global settings, then the system settings, then the game settings (the most specific one wins);
2. writes the matching values in the emulator configuration files;
3. starts the emulator.

**Example:** use the Vulkan renderer for PlayStation games with DuckStation.

1. In the PlayStation Game View, press **SELECT** > **ADVANCED SYSTEM OPTIONS**.

<div align="left"><figure><img src="../.gitbook/assets/image (256).png" alt=""><figcaption></figcaption></figure></div>

2. Open the **DRIVERS** submenu in the **ADVANCED SETTINGS** group.

<div align="left"><figure><img src="../.gitbook/assets/image (255).png" alt=""><figcaption></figcaption></figure></div>

3. Set **VIDEO** to **VULKAN**.

<div align="left"><figure><img src="../.gitbook/assets/image (254).png" alt=""><figcaption></figcaption></figure></div>

When a game is launched, RetroBat writes `Renderer = Vulkan` in the `[GPU]` section of `emulators\duckstation\settings.ini`:

<div align="left"><figure><img src="../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure></div>

If the setting is left on **AUTO**, RetroBat writes `Renderer = Automatic`: this is why a change made directly in DuckStation would be lost.

{% hint style="warning" %}
* Settings available in RetroBat are written at each launch, with your value or the RetroBat default value: always change them in RetroBat.
* Settings that are not available in RetroBat are usually kept: you can change them in the emulator.
* To configure the controls yourself in an emulator, set **AUTOCONFIGURE CONTROLLERS** to **OFF** for this system or game.
{% endhint %}

{% hint style="info" %}
Game settings are linked to the **file name** of the game. If you rename the file, its settings are lost. Two files with the same name in the same system share the same settings.
{% endhint %}

## Troubleshooting

* **A setting has no effect:** check that it is not overridden at the game level, and that the right emulator is selected.
* **Check what RetroBat did:** the log files show the values applied at launch:
  * `emulationstation\emulatorLauncher.log` (game launch and emulator configuration)
  * `emulationstation\.emulationstation\es_log.txt` (RetroBat interface)
* **Go back to the default configuration:** set the settings back to **AUTO**.

## I cannot find the setting I need

If an emulator has a setting you would like to change from RetroBat, contact the RetroBat team on [Discord](https://discord.gg/GVcPNxwzuT) or the [forum](https://retrobat.forumgaming.fr/): it can be added in a future version.

In the meantime, you can change it directly in the emulator: settings that are not available in RetroBat are usually not overwritten.
