---
description: Sony
---

# Playstation 4

<div align="left"><figure><img src="../../../../.gitbook/assets/image (503).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Presentation

The **PlayStation 4** was released in November 2013. After the very unusual processor of the PS3, Sony went back to an architecture close to a PC, simpler for developers. The DualShock 4 controller added a touchpad, a Share button and a light bar.

The console was a huge success, with more than 117 million units sold, and hosted games such as Bloodborne, God of War, Marvel's Spider-Man and The Last of Us Part II. Two revisions came out in 2016: the PS4 Slim and the more powerful PS4 Pro.

PS4 emulation is recent. **shadPS4**, the only emulator offered by RetroBat, is progressing fast but is still young: many games do not work yet.

{% embed url="https://en.wikipedia.org/wiki/PlayStation_4" %}

## At a glance

<table><thead><tr><th width="250.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\ps4</code></td></tr><tr><td><strong>Extensions</strong></td><td>.ps4 .zar .m3u .lnk .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>shadps4</td></tr><tr><td><strong>BIOS</strong></td><td>PS4 system modules in <code>emulators\shadps4\user\sys_modules</code> (not checked by RetroBat)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, handled by shadPS4</td></tr><tr><td><strong>Save states</strong></td><td>No</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr></tbody></table>

## Which emulator to choose?

shadPS4 is the only PS4 emulator in RetroBat.

<table><thead><tr><th width="177">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>shadps4</strong> (default)</td><td>Runs a growing number of games, several versions can be installed side by side.</td><td>Young emulator: many games do not start or crash. Needs a powerful PC.</td></tr></tbody></table>

The shadPS4 compatibility list ([shadps4.net](https://shadps4.net/compatibility/)) gives the status of each game.

**Emulator version**: the **EMULATION > EMULATOR VERSION** option lets you choose which shadPS4 version is used. By default, RetroBat starts the most recent stable version installed. The **LAUNCHER SELECTION** choice uses the version selected in the shadPS4 launcher, **PRE-RELEASE** the most recent pre-release.

## BIOS

The PS4 has no BIOS to provide, but shadPS4 can load **system modules** from the console (`.sprx` files), needed for some games to run properly. They must be dumped from your own PS4.

<table><thead><tr><th width="290.25">Files</th><th>Location</th></tr></thead><tbody><tr><td><code>.sprx</code> modules (<code>libSceNgs2.sprx</code>, <code>libSceFont.sprx</code>…)</td><td><code>emulators\shadps4\user\sys_modules</code></td></tr></tbody></table>

The list of supported modules is in the shadPS4 documentation. RetroBat does not check these files.

## Which game format?

<table><thead><tr><th width="165.25">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong><code>.ps4</code> folder</strong></td><td>The game folder, which contains <code>eboot.bin</code>, renamed with <code>.ps4</code> at the end: <code>roms\ps4\My game.ps4</code>.</td></tr><tr><td><strong>.zar</strong></td><td>The game compressed into a single file (ZArchive), read directly by shadPS4.</td></tr><tr><td>.m3u</td><td>Text file whose first line gives the path of the game, from <code>roms\ps4</code> (see <a href="playstation-4.md#use-an-.m3u-file">Guides</a>).</td></tr><tr><td>.lnk</td><td>Windows shortcut: its arguments are passed to shadPS4.</td></tr><tr><td>.decomp</td><td>PC port, see the <a href="../../others/recomp.md"><strong>Recompilations</strong></a> page.</td></tr></tbody></table>

shadPS4 does not install `.pkg` files: the game must first be extracted to a folder.

## Controls

### Automatic configuration

RetroBat does not configure controllers for shadPS4: the emulator detects them itself. Xbox and DualShock controllers work without any setting.

* Player order may differ from the RetroBat one.
* To change buttons, open the shadPS4 settings (Controller button). Settings are saved per game.
* The **CONTROLS > ENABLE MOTION** option, on by default, uses the gyroscope of compatible controllers.

### Hotkeys

| Hotkey             | Action                                 | Keyboard  |
| ------------------ | -------------------------------------- | --------- |
| **HOTKEY + START** | Quit                                   | —         |
| —                  | Fullscreen                             | F11       |
| —                  | FPS counter                            | F10       |
| —                  | Screenshot                             | F12       |
| —                  | Screenshot including dialogs and menus | ALT + F12 |

## Folders

<table><thead><tr><th width="297.75">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Additional content (DLC)</td><td><code>roms\ps4\DLC</code></td></tr><tr><td>Saves (PS4 "home" folder)</td><td><code>saves\ps4\shadps4\home</code></td></tr><tr><td>System modules</td><td><code>emulators\shadps4\user\sys_modules</code></td></tr><tr><td>shadPS4 configuration</td><td><code>emulators\shadps4\user\config.json</code></td></tr><tr><td>shadPS4 per-game configurations</td><td><code>emulators\shadps4\user\custom_configs</code></td></tr><tr><td>Patches and cheats</td><td><code>emulators\shadps4\user\patches</code>, <code>emulators\shadps4\user\cheats</code></td></tr><tr><td>Screenshots</td><td><code>emulators\shadps4\user\screenshots</code></td></tr><tr><td>shadPS4 versions</td><td><code>emulators\shadps4\launcher\versions</code></td></tr></tbody></table>

## Guides

### Add a game

1. Copy the game folder to `roms\ps4`. It is usually named after the game ID (for example `CUSA00900`) and contains the `eboot.bin` file.
2. Rename it by adding `.ps4` at the end, for example `My game.ps4`.
3. Update the RetroBat game list.

### Compress a game to .zar

A PS4 game is made of thousands of files. The ZArchive format gathers them into a single compressed file, which shadPS4 reads without extracting it.

1. Compress the game folder with the ZArchive tool.
2. Put the resulting `.zar` file in `roms\ps4`.

This format needs shadPS4 0.17.0 or newer.

### Use an .m3u file

The `.m3u` file lets you keep the game folder under its original name. Its first line gives the path of the file to launch, from `roms\ps4`:

```
CUSA00900\eboot.bin
```

Empty lines and lines starting with `#` are ignored.

### shadPS4 per-game settings

shadPS4 can save settings specific to each game, and uses them by default. The **EMULATION > IGNORE PER-GAME SETTINGS** option ignores them and always applies the RetroBat settings.

### Other useful options

<table><thead><tr><th width="309">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>EMULATION > LANGUAGE</strong></td><td>Language of the emulated console. By default, it is the RetroBat language.</td></tr><tr><td><strong>EMULATION > RED-ZONE PATCHING</strong></td><td>Experimental: can fix crashes in some games. Leave it off unless needed.</td></tr><tr><td><strong>USER INTERFACE > SHOW GUI</strong></td><td>Shows the shadPS4 window. It stays open after the game: <strong>HOTKEY + START</strong> closes it.</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (504).png" alt=""><figcaption></figcaption></figure></div>

## Known issues

<table><thead><tr><th width="322.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>The game does not start or crashes</td><td>Check its status in the shadPS4 compatibility list. Try another version with <strong>EMULATOR VERSION</strong>, and add the system modules (see <a href="playstation-4.md#bios">BIOS</a>).</td></tr><tr><td>"Unable to find any game in the provided folder" message</td><td>The <code>.ps4</code> folder has no <code>eboot.bin</code> file.</td></tr><tr><td>A <code>.zar</code> file does not start</td><td>Use shadPS4 0.17.0 or newer.</td></tr><tr><td>Controllers are not in the right order</td><td>The order is handled by shadPS4 and may differ from the RetroBat one.</td></tr><tr><td>My RetroBat settings are not applied to a game</td><td>A shadPS4 per-game setting takes priority: turn on <strong>IGNORE PER-GAME SETTINGS</strong>.</td></tr></tbody></table>

