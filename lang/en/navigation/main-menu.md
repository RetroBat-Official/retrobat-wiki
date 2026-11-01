---
description: Configure RetroBat
---

# Main Menu

The **MAIN MENU** is opened by pressing **START** (**Enter** on the keyboard) in the System View or the Game View.

<div align="left"><figure><img src="../.gitbook/assets/image (240).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="269">Entry</th><th>Content</th></tr></thead><tbody><tr><td><a href="../advanced-features/retroachievements.md"><strong>RETROACHIEVEMENTS</strong></a></td><td>Your RetroAchievements profile and progress (only shown when a RetroAchievements account is configured)</td></tr><tr><td><a href="main-menu.md#game-settings"><strong>GAME SETTINGS</strong></a></td><td>Default settings for all games and emulators, save states, BIOS, accounts</td></tr><tr><td><a href="main-menu.md#user-interface-settings"><strong>USER INTERFACE SETTINGS</strong></a></td><td>Theme, screensaver, game list display</td></tr><tr><td><a href="main-menu.md#controller-settings"><strong>CONTROLLER SETTINGS</strong></a></td><td>Controller configuration, player assignment, guns</td></tr><tr><td><a href="main-menu.md#sound-settings"><strong>SOUND SETTINGS</strong></a></td><td>Volume, music, interface sounds</td></tr><tr><td><a href="main-menu.md#game-collection-settings"><strong>GAME COLLECTION SETTINGS</strong></a></td><td>Systems and collections displayed, grouped systems, sorting</td></tr><tr><td><a href="main-menu.md#scraper"><strong>SCRAPER</strong></a></td><td>Download game information and media</td></tr><tr><td><a href="main-menu.md#updates-and-downloads"><strong>UPDATES &#x26; DOWNLOADS</strong></a></td><td>RetroBat updates, themes, bezels and free content</td></tr><tr><td><a href="main-menu.md#system-settings"><strong>SYSTEM SETTINGS</strong></a></td><td>Language, interface mode, advanced settings</td></tr><tr><td><strong>QUIT</strong></td><td>Quit RetroBat, restart or shut down the computer</td></tr></tbody></table>

{% hint style="info" %}
In **Kid** or **Kiosk** mode (see User interface mode), the menu only shows **INFORMATION**, **UNLOCK USER INTERFACE MODE** and **QUIT**.
{% endhint %}

## Game settings

Settings defined here apply to **all systems and games**. They can be changed for one system ([View options](view-options.md) > **ADVANCED SYSTEM OPTIONS**) or one game ([Game options](game-options.md) > **ADVANCED GAME OPTIONS**).

<table><thead><tr><th width="218.25">Section</th><th width="246.5">Setting</th><th>Description</th></tr></thead><tbody><tr><td>Tools</td><td>Update gamelists</td><td>Refresh the game lists: detect added or removed games, newly scraped media…</td></tr><tr><td>Accounts</td><td>RetroAchievements settings</td><td>Enable and configure <a href="../advanced-features/retroachievements.md">RetroAchievements</a></td></tr><tr><td>Accounts</td><td>Netplay settings</td><td>Enable and configure online play (Netplay)</td></tr><tr><td>BIOS settings</td><td>Missing BIOS check</td><td>List the missing or invalid BIOS files (see <a href="../get-started/adding-bios-files.md">Adding BIOS files</a>)</td></tr><tr><td>BIOS settings</td><td>Check BIOS files before running a game</td><td>Warn when a BIOS file is missing when launching a game</td></tr><tr><td>Savestates</td><td>Auto save/load</td><td>Load the latest save state when a game starts, and save when you quit</td></tr><tr><td>Savestates</td><td>Incremental savestates</td><td>Never overwrite save states / use a new slot for each session / always use the current slot</td></tr><tr><td>Savestates</td><td>Show savestate manager</td><td>Show the save state list before launching a game (never, always, or only if save states exist)</td></tr><tr><td>Global options</td><td>Shader set</td><td>Video filter applied to games (CRT effect, scanlines…)</td></tr><tr><td>Global options</td><td>Decorations</td><td>Bezels displayed around the game</td></tr><tr><td>Global options</td><td>Tattoo</td><td>Show a controller layout image over the bezel, its corner and size</td></tr><tr><td>Global options</td><td>Video mode</td><td>Screen resolution and refresh rate used for games</td></tr><tr><td>Global options</td><td>Game aspect ratio</td><td>Image format (4:3, 16:9…)</td></tr><tr><td>Global options</td><td>Force fullscreen</td><td>Force emulators in fullscreen, even if RetroBat is windowed</td></tr><tr><td>Global options</td><td>Prefer exclusive fullscreen</td><td>Use exclusive fullscreen when the emulator supports it</td></tr><tr><td>Global options</td><td>Never pause emulation on lost focus</td><td>Keep the game running when another window takes the focus</td></tr><tr><td>Global options</td><td>Disable Game Center</td><td>Disable the <a href="game-control-center.md">Game Control Center</a> (HOTKEY + East or <code>Ctrl</code> + <code>F12</code>)</td></tr><tr><td>Global options</td><td>ReShade</td><td>ReShade is used by RetroBat to display bezels and shaders in some standalone emulators</td></tr><tr><td>Global options</td><td>Integer scaling (pixel perfect)</td><td>Scale the image by whole numbers only, for sharp pixels</td></tr><tr><td>Global options</td><td>Smooth games (bilinear filtering)</td><td>Smooth the image</td></tr><tr><td>Global options</td><td>Discord Rich Presence</td><td>Show the game you are playing in your Discord status</td></tr><tr><td>Global options</td><td>Autoconfigure controllers</td><td>Let RetroBat configure controllers in all emulators (enabled by default, untick to disable)</td></tr><tr><td>Global options</td><td>Gamepads before arcade sticks</td><td>Gamepads become players 1, 2…, arcade sticks are assigned to the next players</td></tr><tr><td>Global options > Switch</td><td>Saves in RetroBat saves folder</td><td>Use <code>saves\switch</code> for Citron and Eden saves</td></tr><tr><td>Game stores and launchers > Windows games</td><td>Scan installed store games…</td><td>Add your Steam, Epic, GOG… games to RetroBat automatically</td></tr><tr><td>Game stores and launchers > Game launchers</td><td>eXoDOS, eXoWin3x, eXoWin9x, AGS</td><td>Scan and path of these collections</td></tr><tr><td>Game stores and launchers</td><td>Scan recompilation (QuiverLauncher)</td><td>Add the N64 recompiled games</td></tr><tr><td>Compression</td><td>Decompression, decompression path, never try to mount as drive</td><td>How compressed games (7z, squashfs…) are extracted and where</td></tr><tr><td>Controls > Special controllers</td><td>D-pad as analog, N64 trigger invert, PS4/PS5 enhanced</td><td>Options for special controllers (N64, Mega Drive, DualShock 4, DualSense…)</td></tr><tr><td>Guns > Sinden</td><td>Sinden software path, buttons configuration, kill Sinden software</td><td>Sinden lightgun options</td></tr><tr><td>Guns > Wiimote</td><td>Wiimote connection mode, Wiimote fix association</td><td>Wiimote and DolphinBar options</td></tr><tr><td>RetroArch options > Video</td><td>Aspect ratio, screen orientation, monitor index, GPU index, CRT output, HDR, integer scale type…</td><td>Video settings for RetroArch</td></tr><tr><td>RetroArch options > Visual rendering</td><td>Allow game/core shaders override</td><td>Keep the shaders defined in RetroArch</td></tr><tr><td>RetroArch options > Screen sync</td><td>V-Sync, hard sync, swap interval, black frame insertion, G-Sync/FreeSync…</td><td>Synchronization settings</td></tr><tr><td>RetroArch options > Audio</td><td>Resampler, quality, volume gain, DSP plugin, audio sync</td><td>Audio settings for RetroArch</td></tr><tr><td>RetroArch options > Emulation</td><td>Rewind, fast forward ratio, fast forward behavior, softpatching, allow game/core options override</td><td>Emulation settings for RetroArch</td></tr><tr><td>RetroArch options > Latency reduction</td><td>Run-ahead, preemptive frames, automatic frame delay, input polling</td><td>Settings to reduce input lag</td></tr><tr><td>RetroArch options > AI game translation</td><td>Enable, target language, service URL, pause on translated screen</td><td>In-game translation service</td></tr><tr><td>RetroArch options > User interface</td><td>Notifications, statistics, RetroArch menu elements, press hotkeys twice to exit…</td><td>RetroArch interface settings</td></tr><tr><td>RetroArch options > Drivers</td><td>Video, audio, controllers</td><td>Drivers used by RetroArch</td></tr><tr><td>RetroArch options > Controls</td><td>Pause on disconnect, RetroArch controller profiles, deadzone, sensitivity, pad index…</td><td>Controller settings for RetroArch</td></tr><tr><td>RetroArch options > Guns</td><td>P1 to P4 mouse/gun index</td><td>Mouse or lightgun used by each player</td></tr><tr><td>System settings</td><td>Per system advanced configuration</td><td>Open the advanced settings of a system</td></tr></tbody></table>

{% hint style="info" %}
Most options have a short description, displayed at the bottom of the screen when the option is selected.
{% endhint %}

## User interface settings

<table><thead><tr><th width="189">Section</th><th>Main settings</th></tr></thead><tbody><tr><td>Appearance</td><td><strong>Theme set</strong>, <strong>theme configuration</strong> (colors, layout, <strong>gamelist view style</strong>…)</td></tr><tr><td>Display options</td><td>Screensaver settings, list and game launch transitions, game media during fast scrolling, show clock, on-screen help, battery status</td></tr><tr><td>Gamelist options</td><td>Show favorites on top, hidden files, folders, file names instead of game names, ignore leading articles when sorting, icons (region flag, save state, manual, RetroAchievements, gun, wheel…)</td></tr></tbody></table>

## Controller settings

* **CONTROLLER MAPPING**: configure a new controller or reconfigure a controller.
* Assign a controller to each player.
* **SINDEN GUN SETTINGS** / **WIIMOTE GUN SETTINGS**: lightgun settings.
* **DISPLAY OPTIONS**: show controller notifications, activity and battery level, gun notifications and crosshair.
* **BEHAVIOR**: joystick hotkeys, global hotkeys.

See the [Controllers](https://app.gitbook.com/s/exdzL60ZuqPLldz2AYta/controllers) section.

## Sound settings

<table><thead><tr><th width="131.5">Section</th><th>Main settings</th></tr></thead><tbody><tr><td>Volume</td><td>System volume, music volume, show volume overlay</td></tr><tr><td>Music</td><td>Frontend music, display song titles, only play system-specific music folder, lower music when playing video, favorite songs</td></tr><tr><td>Sounds</td><td>Navigation sounds, video preview audio</td></tr></tbody></table>

Music files are stored in `emulationstation\.emulationstation\music`: see [RetroBat folder structure](../get-started/retrobat-folder-structure.md).

## Game collection settings

<table><thead><tr><th width="224">Section</th><th>Description</th></tr></thead><tbody><tr><td>Collections to display</td><td><strong>Systems displayed</strong>, automatic, editable and dynamic collections to display, <strong>grouped systems</strong></td></tr><tr><td>Create custom collection</td><td>Create an editable or dynamic collection, or a collection from the theme</td></tr><tr><td>Options</td><td>Sort systems, start on a system or a game list, group custom collections, show empty systems, show games of hidden systems in collections…</td></tr></tbody></table>

{% hint style="info" %}
More information in the [Game collections](game-collections.md) section.
{% endhint %}

## Scraper

Configure the scraper (source, filters, media to download) and start scraping.

{% hint style="info" %}
More information in the [Scraping & metadata](scraping-and-metadata.md) section.
{% endhint %}

## Updates and downloads

* **CONTENT DOWNLOADER**: free games and other content
* **THEMES**: download themes
* **THE BEZEL PROJECT**: download bezels
* **CHECK FOR UPDATES**: update RetroBat

{% hint style="warning" %}
RetroBat does not provide any copyrighted content: only free games, or games whose authors allow distribution, are available for download.
{% endhint %}

## System settings

<table><thead><tr><th width="152">Section</th><th width="270.5">Setting</th><th>Description</th></tr></thead><tbody><tr><td>System</td><td>Information</td><td>Hardware and software information</td></tr><tr><td>System</td><td>Language (region)</td><td>Language of the RetroBat interface</td></tr><tr><td>System</td><td>Show clock in 12-hour format</td><td>12 or 24-hour clock</td></tr><tr><td>System</td><td>Power saving mode</td><td>Reduce power consumption when idle</td></tr><tr><td>System</td><td>Screen reader (text to speech)</td><td>Read the menus aloud (<code>F3</code> on the keyboard)</td></tr><tr><td>System</td><td>User interface mode</td><td><strong>Full</strong>, <strong>Kiosk</strong> (no settings) or <strong>Kid</strong> (no settings, limited content)</td></tr><tr><td>Advanced</td><td>Frontend developer options</td><td>Advanced EmulationStation settings, see below</td></tr></tbody></table>

### Frontend developer options

<table><thead><tr><th width="195.25">Section</th><th>Main settings</th></tr></thead><tbody><tr><td>Video options</td><td>VRAM limit, show framerate, V-Sync, anti-aliasing, FPS limit</td></tr><tr><td>Tools</td><td>Log level, create a support file, reset file extensions, clear caches…</td></tr><tr><td>Display settings</td><td>Menu and theme font scale, fullscreen menus</td></tr><tr><td>Data management</td><td>Ignore multi-file disk content (cue/gdi/ccd/m3u), save metadata on exit</td></tr><tr><td>User interface</td><td>Carousel transitions, <strong>quick system select</strong>, <strong>quick jump letter</strong>, on-screen keyboard, hide EmulationStation when running a game, <strong>switch confirm &#x26; cancel buttons</strong>, <strong>access game options with North button</strong>, right analog stick changes volume…</td></tr><tr><td>Optimizations</td><td>Threaded loading, async image loading, VRAM optimizations, filesystem cache</td></tr></tbody></table>

{% hint style="warning" %}
These settings are intended for advanced users: change them only if you know what they do.
{% endhint %}
