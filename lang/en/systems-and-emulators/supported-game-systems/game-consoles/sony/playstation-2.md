---
description: Sony
---

# PlayStation 2

<div align="left"><figure><img src="../../../../.gitbook/assets/image (383).png" alt=""><figcaption></figcaption></figure></div>

### Presentation

The PlayStation 2 is the second home console from Sony, after the first PlayStation (1994). It was released in Japan on March 4, 2000, then in North America in October and in Europe in November of the same year. The launch was a huge event: stocks sold out in a few days, and the console was hard to find for months.

Inside, the PS2 is built around the **Emotion Engine**, a processor designed with Toshiba, and the **Graphics Synthesizer**, its graphics chip. It was also one of the first consoles to read **DVDs**: at a time when DVD players were still expensive, many people bought it to watch films too. It could also play **PlayStation games**, so players kept their old library. Later accessories added online play (network adapter, hard drive for Final Fantasy XI), the EyeToy camera, the SingStar microphones or the Guitar Hero guitars. In 2004, a much smaller **Slim** model replaced the original one.

With more than 155 million units sold, the PS2 is the best-selling home console of all time. It was produced until the end of 2012, and its library is one of the richest ever: Gran Turismo 3 and 4, Final Fantasy X and XII, Metal Gear Solid 2 and 3, Grand Theft Auto III, Vice City and San Andreas, Kingdom Hearts, Shadow of the Colossus, God of War, Ratchet & Clank, Jak and Daxter, Silent Hill 2, Devil May Cry, Tekken 5…

{% embed url="https://en.wikipedia.org/wiki/PlayStation_2" %}

{% hint style="info" %}
**PlayStation (PS1) games go in the PlayStation system** (`roms\psx`), not in the PlayStation 2 system, even though the PS2 could play them.
{% endhint %}

## Overview

<table><thead><tr><th width="227.75"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\ps2</code></td></tr><tr><td><strong>File extensions</strong></td><td>.iso .cso .bin .mdf .gz .chd .m3u .zip .7z .squashfs .decomp</td></tr><tr><td><strong>Emulators</strong></td><td><strong>pcsx2</strong> (default), Libretro: pcsx2, play, pcsx2-16</td></tr><tr><td><strong>BIOS</strong></td><td>Needed for pcsx2, lr-pcsx2 and pcsx2-16 (not for play)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>pcsx2, lr-pcsx2</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Lightguns</strong></td><td>pcsx2 (GunCon 2)</td></tr><tr><td><strong>Wheels</strong></td><td>pcsx2</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="145.25">Emulator</th><th width="174">For who?</th><th width="234">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>pcsx2</strong> (default)</td><td>Everyone</td><td>The most compatible. HD, widescreen patches, texture packs, lightguns, wheels, guitars, up to 8 players.</td><td>Needs a fairly recent PC for HD.</td></tr><tr><td><strong>lr-pcsx2</strong></td><td>RetroArch users</td><td>RetroArch features (shaders, RetroArch menu), paraLLEl-GS renderer.</td><td>No rewind, 2 players, no lightgun or wheel.</td></tr><tr><td><strong>play</strong></td><td>Users without a BIOS</td><td>Works without any BIOS.</td><td>Lower compatibility, 2 players, few options.</td></tr><tr><td><strong>pcsx2-16</strong></td><td>Specific cases</td><td>Old version (1.6) kept for the rare games that run better in it.</td><td>No .chd, no automatic controller configuration.</td></tr></tbody></table>

**If you are not sure, keep pcsx2.**

### BIOS

**One of these files is enough** for pcsx2, lr-pcsx2 and pcsx2-16:

<table><thead><tr><th width="253.25">BIOS file</th><th width="153.25">Region</th><th>MD5</th></tr></thead><tbody><tr><td>ps2-0230a-20080220.bin</td><td>USA</td><td>21038400dc633070a78ad53090c53017</td></tr><tr><td>ps2-0230e-20080220.bin</td><td>Europe</td><td>dc69f0643a3030aaa4797501b483d6c4</td></tr><tr><td>ps2-0230j-20080220.bin</td><td>Japan</td><td>80ac46fa7e77b8ab4366e86948e54f83</td></tr><tr><td>ps2-0250e-20100415.bin</td><td>Europe</td><td>93ea3bcee4252627919175ff1b16a1d9</td></tr><tr><td>SCPH30004R.bin</td><td>Europe</td><td>28922c703cc7d2cf856f177f2985b3a9</td></tr><tr><td>scph39001.bin</td><td>USA</td><td>d5ce2c7d119f563ce04bc04dbc3a323e</td></tr></tbody></table>

Other names also accepted by pcsx2: `ps3_ps2_emu_bios.bin`, `SCPH-39004_BIOS_V7_EUR_160.BIN`, `SCPH-39001_BIOS_V7_USA_160.BIN`, `SCPH-70000_BIOS_V12_JAP_200.BIN`.

{% hint style="info" %}
* **lr-pcsx2** accepts any PS2 BIOS file placed in `bios\pcsx2\bios`, whatever its name.
* When several BIOS are present, pcsx2 and lr-pcsx2 use `ps2-0230a-20080220.bin` first, otherwise the first file found.
* A BIOS of any region runs games of all regions. Choose it for the **language** (see below).
{% endhint %}

### Choosing the BIOS

To use a specific BIOS, set **EMULATION > FORCE BIOS** (pcsx2 and lr-pcsx2) in the system or game options. The list offers USA 230, EUR 230, EUR 250, JAP 230 and PS3 PS2 FIRMWARE.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (384).png" alt=""><figcaption></figcaption></figure></div>

### Changing the console language (BIOS)

On a real PS2, the language is set in the console settings, and many games use it to choose their own language. With pcsx2, it works the same way:

1. Open **START** > **GAME SETTINGS** > **PER SYSTEM ADVANCED CONFIGURATION** > **PLAYSTATION 2**, check that the emulator is **pcsx2**, then enable **EMULATION > START BIOS**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (385).png" alt=""><figcaption></figcaption></figure></div>

2. Launch any PS2 game: the console menu opens instead of the game.
3. With the D-pad, select **System Configuration**, then confirm with **SOUTH** (✕). Japanese BIOS confirm with **EAST** (○).
4. Select **Language** (or **Language Settings**), then **System Language**, and choose your language.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (386).png" alt=""><figcaption></figcaption></figure></div>

5. Quit with **HOTKEY + START**.
6. Go back to the options and disable **START BIOS**.

The language is saved next to the BIOS, in a `.nvm` file of the same name (`bios\pcsx2\bios\ps2-0230e-20080220.nvm` for example). **lr-pcsx2 and pcsx2-16 use the same file**: the language set with pcsx2 also applies to them when they use the same BIOS.

{% hint style="warning" %}
The language only changes in games that contain it. European (PAL) games are often multi-language. Most American (NTSC-U) games only contain English, and Japanese games Japanese.
{% endhint %}

Other emulators:

* **lr-pcsx2:** **EMULATION > LANGUAGE UNLOCK** unlocks more languages in some games.
* **play:** play has no BIOS. Choose the language in **EMULATION > LANGUAGE** (English by default).

## Which game format?

<table><thead><tr><th width="207.25">Format</th><th align="center">pcsx2</th><th align="center">lr-pcsx2</th><th align="center">play</th><th align="center">pcsx2-16</th></tr></thead><tbody><tr><td>.chd (recommended)</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✘</td></tr><tr><td>.iso</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>.cso</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>.zip / .7z / .squashfs</td><td align="center">✔ (extracted at launch)</td><td align="center"></td><td align="center"></td><td align="center"></td></tr></tbody></table>

* **.chd** is the best choice: the game is compressed (often 30 to 50 % smaller), and read directly without extraction.
* **.zip / .7z / .squashfs** games are extracted by RetroBat before each launch with pcsx2. It works, but loading is slower.

### Multi-disc games

Some games use two discs (Xenosaga Episode III, Metal Gear Solid 3: Subsistence…). Create a text file named `Game.m3u` in `roms\ps2`, with one disc per line:

```
Game (Disc 1).chd
Game (Disc 2).chd
```

* **pcsx2** starts the first disc. When the game asks for the next disc, open the pause menu (**HOTKEY + SOUTH**), choose **Change Disc**, then the next disc.
* **lr-pcsx2** uses the RetroArch disc control (**HOTKEY + L1** eject, **HOTKEY + R2** next disc, **HOTKEY + L1** insert).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (387).png" alt="" width="354"><figcaption></figcaption></figure></div>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (388).png" alt=""><figcaption></figcaption></figure></div>

## Controls

### Automatic configuration

RetroBat configures your controllers automatically: you have nothing to do.

<table><thead><tr><th width="121.5">Emulator</th><th width="154.5">RetroBat autoconfiguration</th><th width="91">Players</th><th>Notes</th></tr></thead><tbody><tr><td>pcsx2</td><td>✔</td><td>Up to 8</td><td>XInput and SDL controllers (DualShock 4, DualSense, Switch Pro, 8BitDo…). The multitap (PS2 multiplayer adapter) is enabled automatically when more than 2 controllers are connected.</td></tr><tr><td>lr-pcsx2</td><td>✔ (RetroArch)</td><td>2</td><td></td></tr><tr><td>play</td><td>✔</td><td>2</td><td></td></tr><tr><td>pcsx2-16</td><td>✘</td><td></td><td>Manual configuration in the emulator (see below).</td></tr></tbody></table>

Buttons are mapped by **position**, like a DualShock 2 controller:

| RetroBat controller         | PS2 controller |
| --------------------------- | -------------- |
| SOUTH / EAST / WEST / NORTH | ✕ / ○ / □ / △  |
| L1 / R1                     | L1 / R1        |
| L2 / R2                     | L2 / R2        |
| Left / right stick (press)  | L3 / R3        |
| SELECT / START              | SELECT / START |

<div align="left"><figure><img src="../../../../.gitbook/assets/image (389).png" alt="" width="225"><figcaption></figcaption></figure></div>

To use your own mapping made in the emulator, set **AUTOCONFIGURE CONTROLLERS** to **OFF** (pcsx2, lr-pcsx2, play). With play, the input profile `emulators\play\Play Data Files\inputprofiles\<game name>.xml` is then used if it exists, otherwise the default profile.

### Hotkeys

**pcsx2** uses the standard RetroBat hotkeys:

| Action                              | Controller               | Keyboard  |
| ----------------------------------- | ------------------------ | --------- |
| Quit the game                       | HOTKEY + START           | Esc       |
| Pause menu (change disc, settings…) | HOTKEY + SOUTH           | F1        |
| Save state                          | HOTKEY + WEST            | F2        |
| Load state                          | HOTKEY + NORTH           | F4        |
| Previous / next save slot           | HOTKEY + D-pad down / up | F6 / F7   |
| Slow motion                         | HOTKEY + D-pad left      | Backspace |
| Fast forward (hold)                 | HOTKEY + D-pad right     | L         |
| Screenshot                          | HOTKEY + R3              | F8        |
| Pause                               | HOTKEY + L3              | P         |
| Fast forward (toggle)               |                          | Space     |
| Fullscreen                          |                          | F         |

* **lr-pcsx2** uses the RetroArch hotkeys (same table on the Hotkeys page), without rewind.
* **play** and **pcsx2-16**: only **HOTKEY + START** (quit).

### pcsx2 controller options

In the options, **CONTROLS** submenu:

<table><thead><tr><th width="266.5">Option</th><th>Use</th></tr></thead><tbody><tr><td>USE MULTITAP</td><td>Forces the multitap on port 1, port 2 or both. Otherwise it is automatic.</td></tr><tr><td>USE TRIGGERS TO BRAKE/ACCELERATE</td><td>Racing games (Gran Turismo…): the analog triggers are mapped to □/✕ or to an analog stick, for a progressive throttle. Then set accelerate and brake on these buttons in the game options.</td></tr><tr><td>PRESSURE MODIFIER BUTTON</td><td>The PS2 buttons are pressure-sensitive, and some games use it (Metal Gear Solid 2 and 3: holding a weapon without shooting). Holding the chosen stick button makes the next presses "light". <strong>PRESSURE MODIFIER QUANTITY</strong> sets the strength.</td></tr><tr><td>USE LEFT STICK AS DPAD</td><td>Moves with the left stick in games that only use the D-pad.</td></tr><tr><td>JOYSTICK DEADZONE / ANALOG SENSITIVITY / TRIGGERS DEADZONE</td><td>Fine-tuning of the sticks and triggers.</td></tr><tr><td>RUMBLE STRENGTH</td><td>Vibration strength.</td></tr><tr><td>USE GUITAR</td><td>Guitar Hero / Rock Band: uses a compatible guitar (CRKD Guitar XP).</td></tr></tbody></table>

### Alternative layouts:

Alternative layouts have been created in order to be able to use analog triggers to throttle and brake in driving games, the layouts can be enabled with the following option:

<div align="left"><figure><img src="https://i.imgur.com/5TFeO14.png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="342.75">Option</th><th>Control layout</th></tr></thead><tbody><tr><td>TRIGGERS AS SQUARE AND CROSS</td><td><img src="../../../../.gitbook/assets/image (390).png" alt="" data-size="original"></td></tr><tr><td>TRIGGERS AS RIGHT STICK</td><td><img src="../../../../.gitbook/assets/image (391).png" alt="" data-size="original"></td></tr><tr><td>TRIGGERS AS LEFT STICK</td><td><img src="../../../../.gitbook/assets/image (392).png" alt="" data-size="original"></td></tr></tbody></table>

{% hint style="info" %}
In order to use analog triggers, you need to change the controls in-game in order to map throttle and brake to the right buttons/axis.
{% endhint %}

### lr-pcsx2 controller options

| Option                                             | Use                                                                                                                               |
| -------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| START IN ANALOG MODE                               | Starts the controller in analog mode (the ANALOG button of the DualShock 2). Disable it for games that only work in digital mode. |
| ANALOG SENSITIVITY (CORE) / ANALOG DEADZONE (CORE) | Sensitivity and dead zone of the sticks.                                                                                          |
| ENABLE RUMBLE                                      | Vibrations.                                                                                                                       |

### play controller options

| Option         | Use                      |
| -------------- | ------------------------ |
| DISABLE RUMBLE | Disables the vibrations. |

### pcsx2-16: manual configuration

pcsx2-16 is not configured by RetroBat:

1. Open `emulators\pcsx2-16` and start `pcsx2.exe`.
2. Menu **Config** > **Controllers (PAD)** > **Plugin Settings**.
3. In the **Pad 1** tab, click each button and press the matching button of your controller.
4. Close the window: the configuration is kept for your next games.

### Lightguns (pcsx2)

pcsx2 emulates the **GunCon 2** (Time Crisis 2 and 3, Vampire Night, Ninja Assault…).

1. Enable **CONTROLS > ENABLE GUN** in the options of the system or the game.
2. Check your lightgun model on the Lightguns and Gun controls pages.
3. Optional settings in the **GUNS** submenu:
   * **PLAYER 1 GUN PORT**: USB port of the gun, USB 1 or USB 2. Some games expect the gun on the second port.
   * **GUNCON BUTTON MAPPING**: where the A, B and START buttons of the GunCon go (mouse and keyboard, or controller).
   * **INVERT TRIGGER/RELOAD**, **CALIBRATION BUTTON**.
   * **CROSSHAIR**: no crosshair, mouse cursor, or custom image. For a custom crosshair, put a `crosshair.png` file in `emulators\pcsx2\cross`, or choose a file with **CUSTOM CROSSHAIR FILE**. **CUSTOM CROSSHAIR SIZE** sets its size.

### Wheels (pcsx2)

1. Enable **WHEELS > ENABLE WHEEL**.
2. Check that your wheel is supported on the Wheels page.
3. Useful settings: **WHEEL TYPE PLAYER 1** (Driving Force, Driving Force Pro, GT Force: Gran Turismo 4 recognizes the Driving Force Pro), **ENABLE FORCE FEEDBACK**, **STEERING DEADZONE**…
4. Without a wheel, **SIMULATE WHEEL WITH GAMEPAD** makes the game believe a wheel is connected.

## Folders

All paths start from your RetroBat folder.

### Saves

On the PS2, games save on a **memory card**. The emulators create it for you: you have nothing to format.

| Emulator | Memory cards                                                                     | Save states                             | Screenshots         |
| -------- | -------------------------------------------------------------------------------- | --------------------------------------- | ------------------- |
| pcsx2    | `saves\ps2\pcsx2\memcards`                                                       | `saves\ps2\pcsx2`                       | `screenshots\pcsx2` |
| lr-pcsx2 | `bios\pcsx2\memcards` (shared cards, default) or `saves\ps2` (one card per game) | `saves\ps2\libretro.pcsx2`              | `screenshots`       |
| play     | `emulators\play\Play Data Files\vfs\mc0`                                         | `emulators\play\Play Data Files\states` |                     |
| pcsx2-16 | `saves\ps2\pcsx2-16\memcards`                                                    | `saves\ps2\pcsx2-16\sstates`            | `screenshots\pcsx2` |

{% hint style="warning" %}
Each emulator has its own memory cards. If you change emulator, your progress does not follow. Keep the same emulator for a game, or copy the memory card yourself (pcsx2, lr-pcsx2 and pcsx2-16 use the same `.ps2` format).
{% endhint %}

* To keep a memory card from another PCSX2 install, copy its `Mcd001.ps2` file into `saves\ps2\pcsx2\memcards` (replace the existing file after making a copy of it).
* Save states made with pcsx2 and lr-pcsx2 also appear in the RetroBat save state menu: see the Save states page.

### Other useful folders

| Content                               | Folder                           |
| ------------------------------------- | -------------------------------- |
| BIOS and console language (`.nvm`)    | `bios\pcsx2\bios`                |
| Texture packs (pcsx2)                 | `bios\pcsx2\textures`            |
| Cheats (pcsx2)                        | `cheats\pcsx2\cheats`            |
| Custom crosshair (pcsx2)              | `emulators\pcsx2\cross`          |
| play configuration and input profiles | `emulators\play\Play Data Files` |

## Guides

### Playing in HD (internal resolution)

The PS2 displays its games in about 480 lines, which looks blurry on a modern screen. **INTERNAL RESOLUTION** renders the 3D in a higher resolution:

* pcsx2 and lr-pcsx2: 2x ≈ 720p, 3x ≈ 1080p, 4x ≈ 1440p, 6x ≈ 4K.
* play: x2, x4…

Start with **3x** (1080p). If the game slows down, go back to 2x. Some games show lines or offset pictures in HD: try the **MANUAL HACKS** submenu, or go back to native resolution.

### Playing in widescreen (16:9)

PS2 games were made for 4:3 TVs. Many of them can be patched to 16:9:

* **pcsx2:** **VIDEO > WIDESCREEN PATCHES** is on by default. When a patch exists for the game, pcsx2 switches to 16:9 by itself. **VIDEO > NO-INTERLACING PATCHES** removes the flickering of interlaced games that have a patch.
* **lr-pcsx2:** **VIDEO > WIDESCREEN PATCHES** (16:9, 16:10, 21:9, 32:9).
* **play:** **VIDEO > WIDESCREEN HACK** (best with full 3D games).
* **pcsx2-16:** **GAME ASPECT RATIO** set to 16/9 (stretches the picture).

{% hint style="info" %}
With pcsx2, **decorations** (bezels) are hidden in AUTO mode, because a game can switch to 16:9 by itself. To show them, set **GAME ASPECT RATIO** to 4:3, or disable **WIDESCREEN PATCHES**.
{% endhint %}

### Custom textures (pcsx2)

Fans have redrawn the textures of some games in HD. To use a pack:

1. **Find the serial of the game.** It is written on the disc and on the case (for example `SLES-52725` or `SLUS-20946`). It is also shown in the game list of pcsx2.
2. **Create the folder** `bios\pcsx2\textures\<SERIAL>\replacements` (for example `bios\pcsx2\textures\SCES-51719\replacements`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (393).png" alt=""><figcaption></figcaption></figure></div>

3. **Copy the content of the pack** into `replacements`. If the pack already contains a folder named after the serial, copy this folder directly into `bios\pcsx2\textures`.
4. **Enable the option** **VISUAL RENDERING > CUSTOM TEXTURES** in the options of the game:
   * **YES (PRECACHE)**: loads the whole pack at startup. Smoother in game, but uses a lot of memory.
   * **YES (NO PRECACHE)**: loads the textures when needed. For very large packs or PCs with little memory.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (394).png" alt=""><figcaption></figcaption></figure></div>

5. Launch the game. For a good result, also raise the **INTERNAL RESOLUTION**.

### Memory card options

**pcsx2:** **EMULATION > SLOT 1 MEMORY CARD**:

* **STANDARD MEMORY CARD**: a single card (`Mcd001.ps2`) for all games (default). Like on a real console, it can become full (8 MB).
* **PER GAME MEMORY CARD**: one card per game, named after the game.
* **FOLDER**: a "folder" card that is never full.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (395).png" alt=""><figcaption></figcaption></figure></div>

**lr-pcsx2:** **EMULATION > SHARED MEMORY CARDS** is on by default (one card for all games). Disable it to get one card per game in `saves\ps2`.

{% hint style="warning" %}
Changing the memory card type does not move your saves: the games no longer see the old card. Change it before you start playing.
{% endhint %}

### Cheats

* **pcsx2:** put the cheat files (`.pnach`) in `cheats\pcsx2\cheats`, then enable **EMULATION > ENABLE CHEATS**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (396).png" alt=""><figcaption></figcaption></figure></div>

* **lr-pcsx2:** **EMULATION > ENABLE CHEATS**.

Cheats are disabled in RetroAchievements hardcore mode.

### BIOS screen and boot

* **SKIP BIOS** (pcsx2, lr-pcsx2, pcsx2-16) is on by default: the game starts directly, without the Sony animation. Disable it to see the boot animation.
* **START BIOS** (pcsx2) opens the console menu instead of the game (to change the language, manage the memory cards…).

### Performance and display problems

* **DRIVERS > VIDEO** (pcsx2), **DRIVERS > VIDEO CORE RENDERER** (lr-pcsx2), **DRIVERS > VIDEO** (play): renderer used. Vulkan or Direct3D 11/12 are usually the fastest. Try another one if a game shows glitches or a black screen.
* **pcsx2-16:** **EMULATION > GRAPHICS PLUGINS**: choose AVX2 if your processor supports it, otherwise SSE4 or SSE2.
* **lr-pcsx2:** the **paraLLEl-GS** renderer reproduces the PS2 picture very accurately. Its **PARALLEL-GS** submenu offers supersampling for a sharper picture.
* **GAME FIXES** (pcsx2): fixes for specific games. pcsx2 already applies the right fixes automatically for known games: only change them if a guide tells you to.

## Known issues

<table><thead><tr><th width="305.25">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>"No BIOS found in bios/pcsx2/bios folder"</td><td>The BIOS is missing or, with pcsx2, its name is not in the list. See BIOS.</td></tr><tr><td>"WARNING: THE SYSTEM HAS MISSING BIOS FILE(S)…" at launch</td><td>No accepted BIOS was found in <code>bios\pcsx2\bios</code>. Check the file name and folder. With play, choose YES. See Checking the BIOS.</td></tr><tr><td>The game stays in English</td><td>The game only contains English (US version), or the console language is not set. See Changing the console language.</td></tr><tr><td>The game does not start with pcsx2-16</td><td>pcsx2-16 cannot read .chd files. Use pcsx2, or an .iso.</td></tr><tr><td>The controller does nothing with pcsx2-16</td><td>pcsx2-16 is not configured by RetroBat. See pcsx2-16: manual configuration.</td></tr><tr><td>.zip / .7z games take long to start</td><td>They are extracted before each launch. Convert them to .chd.</td></tr><tr><td>The game asks for disc 2</td><td>Use a .m3u file and change the disc from the pause menu. See Multi-disc games.</td></tr><tr><td>Lines, blur or offset picture in HD</td><td>Go back to native resolution, or try the <strong>MANUAL HACKS</strong> options of the game.</td></tr><tr><td>The game is slow</td><td>Lower the internal resolution, try another video renderer, or disable custom textures.</td></tr><tr><td>No decoration with pcsx2</td><td>Normal in AUTO mode: see Playing in widescreen.</td></tr></tbody></table>
