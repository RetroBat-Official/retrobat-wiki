---
description: Microsoft
---

# Xbox

<div align="left"><figure><img src="../../../../.gitbook/assets/image (547).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Xbox** is Microsoft's first home console. It was released in November 2001 in the United States, then in February 2002 in Japan and in March 2002 in Europe. It is built like a PC: an Intel Pentium III CPU at 733 MHz, an NVIDIA graphics chip (NV2A), 64 MB of memory and, for the first time on a console, a built-in 8 GB hard drive that stores saves and music ripped from CDs.

Its large original controller, nicknamed the "Duke", was quickly replaced by the more compact **Controller S**. In 2002, the **Xbox Live** service brought online play to consoles through the machine's Ethernet port. The Xbox sold about 24 million units before being replaced by the Xbox 360 at the end of 2005. Notable games include Halo: Combat Evolved, Halo 2, Fable, Star Wars: Knights of the Old Republic, Ninja Gaiden, Jet Set Radio Future and Project Gotham Racing.

RetroBat offers three emulators: **xemu**, which reproduces the console hardware and uses its BIOS, **xbased**, which reimplements the Xbox system and renders games with Vulkan, and **Cxbx-Reloaded**, which replaces the Xbox system with its own code. xbased and Cxbx-Reloaded need no BIOS.

{% embed url="https://en.wikipedia.org/wiki/Xbox_(console)" %}

## At a glance

<table><thead><tr><th width="216.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\xbox</code></td></tr><tr><td><strong>Extensions</strong></td><td>.xbe .iso .chd .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>xemu</td></tr><tr><td><strong>BIOS</strong></td><td><code>mcpx_1.0.bin</code> and <code>Complex_4627.bin</code> (xemu only)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>xbased (xemu: snapshots from its menu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>cxbx</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>Cerbios.bin</code>, <code>Complex_4627v1.03.bin</code> (xemu, FORCE BIOS option)</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="145.75">Emulator</th><th width="308.5">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>xemu</strong> (default)</td><td>The most compatible. Emulates the real hardware: hard drive, EEPROM, dashboard. Upscaling, Vulkan or OpenGL, snapshots.</td><td>Needs the BIOS. Only reads disc images in XISO format (<code>.iso</code>). No light guns.</td></tr><tr><td><strong>xbased</strong></td><td>No BIOS. Reads Redump and <code>.chd</code> images without conversion. Save states managed by RetroBat. Built-in patches (60 fps, widescreen) and cheats, CRT filters.</td><td>Recent emulator (first release in November 2026). Needs a Vulkan 1.1 graphics card. No light guns.</td></tr><tr><td><strong>cxbx</strong> (Cxbx-Reloaded)</td><td>No BIOS. Runs extracted games (<code>.xbe</code>). Supports the EMS TopGun light gun.</td><td>Lower compatibility, more graphics bugs. <code>.iso</code> files require Dokan 2 to be installed.</td></tr></tbody></table>

The xemu compatibility list ([xemu.app](https://xemu.app/#compatibility)) shows the status of each game. If a game has problems, try another emulator.

## BIOS

Only **xemu** needs the BIOS. xbased and Cxbx-Reloaded do not use any.

<table><thead><tr><th>File</th><th width="102.75">Folder</th><th>Role</th><th>MD5</th></tr></thead><tbody><tr><td><code>mcpx_1.0.bin</code></td><td><code>bios</code></td><td>Boot ROM (MCPX), required</td><td><code>d49c52a4102f6df7bcf8d0617ac475ed</code></td></tr><tr><td><code>Complex_4627.bin</code></td><td><code>bios</code></td><td>BIOS (flash) used by default</td><td><code>39cee882148a87f93cb440b99dde3ceb</code></td></tr><tr><td><code>Cerbios.bin</code></td><td><code>bios</code></td><td>Alternative BIOS, optional</td><td></td></tr><tr><td><code>Complex_4627v1.03.bin</code></td><td><code>bios</code></td><td>Alternative BIOS, optional</td><td></td></tr></tbody></table>

RetroBat checks `mcpx_1.0.bin` and `Complex_4627.bin`. The alternative BIOS files are only used if you select them with the xemu **EMULATION > FORCE BIOS** option.

The console hard drive and EEPROM are not BIOS files to add: on first launch, RetroBat creates `xbox_hdd.qcow2` (a formatted hard drive, without a dashboard) and `eeprom.bin` in `saves\xbox`. xbased likewise creates its own hard drive, with its EEPROM, in `saves\xbox\xbased\hdd`.

### Console language

The game language is the one stored in the console EEPROM. RetroBat sets it at each launch, for all three emulators:

* by default, it is the RetroBat language (English if the Xbox does not have it);
* the **EMULATION > LANGUAGE** option forces a language: English, Japanese, German, French, Spanish, Italian, Korean, Chinese or Portuguese.

A game that does not exist in the selected language is displayed in its default language, often English.

## Which game format should I use?

<table><thead><tr><th width="172.75">Format</th><th width="81.25">xemu</th><th width="87">xbased</th><th width="79.5">cxbx</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.iso</strong> (XISO)</td><td>✅</td><td>✅</td><td>✅</td><td>Disc image in Xbox format (XISO). With Cxbx, the image is mounted as a drive with Dokan 2 (see Guides, "Running .iso files with Cxbx").</td></tr><tr><td><strong>.iso</strong> (Redump)</td><td>❌</td><td>✅</td><td>❌</td><td>Full disc image, including the video partition. xbased reads it as is; for xemu and Cxbx, convert it to XISO (see Guides, "Converting a Redump image to XISO").</td></tr><tr><td><strong>.chd</strong></td><td>❌</td><td>✅</td><td>❌</td><td>Compressed image, created with <code>chdman createdvd</code> from an XISO or Redump image.</td></tr><tr><td><strong>.xbe</strong></td><td>❌</td><td>✅</td><td>✅</td><td>Executable of an extracted game. xbased only runs the game's <code>default.xbe</code> file, Cxbx accepts any <code>.xbe</code>.</td></tr><tr><td><strong><code>.decomp</code> folder</strong></td><td>-</td><td>-</td><td>-</td><td>PC port, see the <strong>Recompilations</strong> page.</td></tr></tbody></table>

`.zip` and `.7z` archives are not accepted: Xbox games must stay uncompressed. To save space, xbased accepts the `.chd` format.

## Controls

### Automatic configuration

RetroBat automatically configures controllers for all three emulators, up to 4 players, in the RetroBat player order. The **AUTOCONFIGURE CONTROLLERS** option disables this configuration to keep the one made in the emulator.

<table><thead><tr><th width="297.75">Xbox</th><th>Controller</th></tr></thead><tbody><tr><td>A</td><td>SOUTH</td></tr><tr><td>B</td><td>EAST</td></tr><tr><td>X</td><td>WEST</td></tr><tr><td>Y</td><td>NORTH</td></tr><tr><td>White</td><td>L1</td></tr><tr><td>Black</td><td>R1</td></tr><tr><td>Left and right triggers</td><td>L2, R2</td></tr><tr><td>Back</td><td>SELECT</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Stick clicks</td><td>L3, R3</td></tr><tr><td>D-pad, sticks</td><td>D-pad, sticks</td></tr></tbody></table>

* **xemu** uses the layout of each controller recognized by SDL: Xbox, DualShock 4, DualSense and Switch Pro controllers work without any setting. Rumble is enabled.
* **xbased** also uses the layout of each controller recognized by SDL. **CONTROLS > STICK DEADZONE** sets the stick dead zone (10% by default) and **CONTROLS > ENABLE RUMBLE** the rumble (on by default). A key configuration made for a game in xbased takes priority.
* **Cxbx** emulates a **Controller S** by default. The **CONTROLS > PLAYER 1 CONTROLLER TYPE** option (up to 4) selects **GAMEPAD S** or **GAMEPAD DUKE**. Rumble is enabled with **CONTROLS > ENABLE RUMBLE**.

### Keyboard

A keyboard assigned to a player in RetroBat is configured with these keys. xbased uses the keyboard for player 1 when no controller is connected:

| Xbox                                | xemu             | xbased                  | cxbx         |
| ----------------------------------- | ---------------- | ----------------------- | ------------ |
| A, B, X, Y                          | A, B, X, Y       | SPACE, LEFT SHIFT, Q, E | S, D, W, E   |
| White, Black                        | 1, 2             | Z, C                    | X, C         |
| Left, right triggers                | W, O             | 1, 3                    | Q, R         |
| Back, Start                         | BACKSPACE, ENTER | BACKSPACE, ENTER        | SPACE, ENTER |
| D-pad                               | Arrow keys       | Arrow keys              | Arrow keys   |
| Left stick (up, left, down, right)  | E, S, D, F       | W, A, S, D              | T, F, G, H   |
| Right stick (up, left, down, right) | I, J, K, L       | I, J, K, L              | I, J, K, L   |
| Stick clicks                        | 3, 4             | F, H                    | B, M         |

For xemu and Cxbx, keys are given for a QWERTY keyboard: these emulators use the key position, not its letter. xbased uses the letter: on another layout, these are the keys marked with these letters.

### Light guns

Light guns only work with **Cxbx**, which emulates the **EMS TopGun** light gun on player 1's port. It is used by games such as The House of the Dead III, Silent Scope Complete or Starsky & Hutch.

Enable the **GUNS > ENABLE GUN** option (or select **EMS TOPGUN** in **PLAYER 1 CONTROLLER TYPE**).

<table><thead><tr><th width="256.5">EMS TopGun</th><th>Light gun / mouse</th></tr></thead><tbody><tr><td>Aim</td><td>Light gun or mouse</td></tr><tr><td>Trigger</td><td>Trigger (left click)</td></tr><tr><td>Grip</td><td>Reload button (right click)</td></tr><tr><td>START</td><td>Key 1</td></tr><tr><td>SE/BA</td><td>Key 5</td></tr><tr><td>A, B</td><td>S, D keys</td></tr><tr><td>Gun stick</td><td>Arrow keys</td></tr></tbody></table>

* **GUNS > INVERT TRIGGER/RELOAD** swaps the trigger and the grip (useful with a WiiZapper).
* With a Wiimote on a DolphinBar, the D-pad is the stick, START is on button 1 or on + depending on the DolphinBar mode, and SE/BA on button 2 (mode 1 only).
* With a Sinden light gun, RetroBat starts the Sinden software automatically.

For more details on light guns, see the [**Lightguns**](../../../../controllers/supported-controllers/lightguns/) page.

### Hotkeys

#### **xemu**

| Hotkey                           | Action                                                        | Keyboard         |
| -------------------------------- | ------------------------------------------------------------- | ---------------- |
| **HOTKEY + START**               | Exit                                                          | CTRL + Q         |
| **GUIDE**, or **SELECT + START** | xemu quick menu (screenshot, snapshot, pause, settings, exit) | F2               |
| —                                | xemu main menu (settings, snapshots)                          | F1               |
| —                                | Load the snapshot bound to the key                            | F5 to F8         |
| —                                | Create the snapshot bound to the key                          | SHIFT + F5 to F8 |
| —                                | Screenshot                                                    | F12              |
| —                                | Pause                                                         | CTRL + P         |
| —                                | Restart                                                       | CTRL + R         |
| —                                | Fullscreen                                                    | F11              |

#### **xbased**

| Hotkey                    | Action                                             | Keyboard                  |
| ------------------------- | -------------------------------------------------- | ------------------------- |
| **HOTKEY + START**        | Exit                                               | —                         |
| **HOTKEY + SOUTH**        | xbased menu (save states, settings, restart, exit) | F1                        |
| **HOTKEY + WEST**         | Save state                                         | F2 (SHIFT + F2: 2nd slot) |
| **HOTKEY + NORTH**        | Load state                                         | F4 (SHIFT + F4: 2nd slot) |
| **HOTKEY + RIGHT** (held) | Fast forward                                       | L (held)                  |
| **HOTKEY + R3**           | Screenshot                                         | F8                        |
| —                         | Pause                                              | P                         |
| —                         | Fullscreen                                         | F or ALT + ENTER          |

The GUIDE button is not used in RetroBat: the xbased menu opens with **HOTKEY + SOUTH**.

#### **cxbx**

| Hotkey             | Action                                            | Keyboard |
| ------------------ | ------------------------------------------------- | -------- |
| **HOTKEY + START** | Exit                                              | F6       |
| —                  | Show the Cxbx interface (frame counter, settings) | F1       |
| —                  | Unlock the frame rate limit                       | F9       |

## Folders

<table><thead><tr><th width="405.25">Content</th><th>Folder</th></tr></thead><tbody><tr><td>xemu BIOS</td><td><code>bios</code></td></tr><tr><td>xemu: console hard drive (game saves, snapshots)</td><td><code>saves\xbox\xbox_hdd.qcow2</code></td></tr><tr><td>xemu: EEPROM (console language and settings)</td><td><code>saves\xbox\eeprom.bin</code></td></tr><tr><td>xemu: screenshots</td><td><code>screenshots\xemu</code></td></tr><tr><td>xemu: configuration</td><td><code>emulators\xemu\xemu.toml</code></td></tr><tr><td>xbased: hard drive and EEPROM (saves in <code>Partition1\UDATA</code>)</td><td><code>saves\xbox\xbased\hdd</code></td></tr><tr><td>xbased: save states managed by RetroBat</td><td><code>saves\xbox\xbased\sstates</code></td></tr><tr><td>xbased: emulator save states</td><td><code>emulators\xbased\states</code></td></tr><tr><td>xbased: shader cache</td><td><code>saves\xbox\xbased\hle</code></td></tr><tr><td>xbased: screenshots (<code>.bmp</code>)</td><td><code>emulators\xbased\screenshots</code></td></tr><tr><td>xbased: patches (IPS) and cheats</td><td><code>emulators\xbased\mods</code>, <code>emulators\xbased\cheats</code></td></tr><tr><td>xbased: configuration (global, per game)</td><td><code>emulators\xbased\xbased.ini</code>, <code>emulators\xbased\games</code></td></tr><tr><td>cxbx: emulated hard drive (saves in <code>Partition1\UDATA</code>)</td><td><code>emulators\cxbx-reloaded\EmuDisk</code></td></tr><tr><td>cxbx: EEPROM</td><td><code>emulators\cxbx-reloaded\EEPROM.bin</code></td></tr><tr><td>cxbx: configuration</td><td><code>emulators\cxbx-reloaded\settings.ini</code></td></tr></tbody></table>

Game saves are stored on each emulator's hard drive: they are not shared between emulators.

## Guides

### Adding a game

1. For xemu and Cxbx, check that the game is in XISO format (see below). xbased also reads Redump and `.chd` images.
2. Copy the `.iso` file to `roms\xbox`.
3. For xemu, add `mcpx_1.0.bin` and `Complex_4627.bin` to `bios`.
4. Update the RetroBat game list and launch the game.

### Converting a Redump image to XISO

"Redump" images contain the whole disc, including a video partition that the Xbox does not read. xbased reads them as is, but neither xemu nor Cxbx accept them. To convert them, use [**extract-xiso**](https://github.com/xboxdev/extract-xiso) or [**xdvdfs**](https://github.com/antangelo/xdvdfs), two free tools:

* with extract-xiso: `extract-xiso -r "Game name.iso"` rewrites the image in XISO format;
* with xdvdfs: `xdvdfs pack "Game name.iso" "Game name (xiso).iso"` creates a new image.

Both tools can also create an XISO image from an extracted game folder, to run it with xemu.

### Running .iso files with Cxbx

Cxbx cannot read disc images directly: RetroBat mounts them as a drive with the `xbox-iso-vfs` tool, which requires **Dokan 2**.

1. Install Dokan 2 ("DokanSetup" installer on the [releases page of the dokany project](https://github.com/dokan-dev/dokany/releases)).
2. Launch the game from RetroBat. The drive is mounted during the game and removed when the game closes.

If Dokan 2 is not installed, RetroBat opens the Dokan download page and the game does not start.

### xemu snapshots

xemu can save the full state of the console (a "snapshot"). RetroBat does not manage them from the game list: everything is done in xemu.

* To create a snapshot: open the quick menu (**GUIDE** or **SELECT + START**) and select **Save Snapshot**.
* To load one: open the main menu (**F1**), **Snapshots** tab. You can also bind a snapshot to the F5 to F8 keys to load it from the keyboard.

Snapshots are stored on the `saves\xbox\xbox_hdd.qcow2` hard drive.

### xbased save states

xbased save states are managed by RetroBat:

* in game, **HOTKEY + WEST** creates a save state. RetroBat copies it right away to `saves\xbox\xbased\sstates`, with a picture, as a new slot;
* from the game list, the save states menu shows these states: the game starts directly at the selected point;
* **HOTKEY + NORTH** reloads the last state saved with **HOTKEY + WEST**.

The xbased menu (**HOTKEY + SOUTH**) also offers 10 slots: states saved from this menu are copied the same way.

An xbased save state needs the `blobs` folder next to it (it holds the game's cache drives): do not delete it.

### xbased patches and cheats

xbased comes with per-game patches (60 fps, widescreen, 480p…) and cheats for more than 500 games. They are enabled game by game in the xbased interface:

1. Start xbased from the RetroBat menu: its library shows the games of `roms\xbox` (after a first game launched from RetroBat).
2. Select the game, then **Mods & patches**.
3. Enable the patches or cheats you want. They are kept for the games launched from RetroBat.

You can add your own IPS patches to `emulators\xbased\mods\<TITLE ID>` and your cheats to `emulators\xbased\cheats\<TITLE ID>`.

The **FRAMERATE** option lifts the frame rate cap for all games; a 60 fps patch is safer when one exists for the game.

### Using your own hard drive

The hard drive created by RetroBat is empty and has no dashboard. To use the hard drive of a console (with its dashboard and saves) or an image prepared for xemu, replace `saves\xbox\xbox_hdd.qcow2` with your image, using the same name. Keep a copy of the old file: it contains your saves.

### Other useful options

#### **xemu**

<table><thead><tr><th width="330.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Increases the rendering resolution (up to 10X). The native resolution is 640x480.</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td><strong>NATIVE</strong>, <strong>4:3</strong> or <strong>16:9</strong>. By default, xemu chooses automatically.</td></tr><tr><td><strong>EMULATION > MEMORY</strong></td><td>128 MB (RetroBat default, like development kits) or 64 MB (original console).</td></tr><tr><td><strong>EMULATION > SKIP BOOT</strong></td><td>On by default: skips the Xbox boot animation.</td></tr><tr><td><strong>VIDEO > DISPLAY MODE</strong></td><td>Picture placement: scaled (default), centered or stretched.</td></tr><tr><td><strong>VIDEO > EMULATED VIDEO SIGNAL</strong></td><td>Emulated video cable: HDTV (default), SCART, VGA, RFU, S-VIDEO or COMPOSITE.</td></tr><tr><td><strong>VISUAL RENDERING > SHADER CACHE</strong></td><td>On by default: less stuttering once shaders are saved.</td></tr><tr><td><strong>AUDIO > DSP EMULATION</strong></td><td>More accurate sound (effects, reverb), but more demanding. <strong>DSP JIT ENGINE</strong> speeds up this emulation (experimental).</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td>OPENGL (default) or VULKAN.</td></tr><tr><td><strong>USER INTERFACE > SHOW MENU BAR</strong></td><td>Shows the xemu menu bar at the top of the screen.</td></tr></tbody></table>

#### **xbased**

<table><thead><tr><th width="324">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Increases the rendering resolution (up to 8X). The native resolution is 640x480.</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td><strong>AUTO</strong> (default), <strong>4:3</strong>, <strong>16:9</strong> or <strong>STRETCH</strong>. Bezels are only shown in AUTO or 4:3, without WIDESCREEN.</td></tr><tr><td><strong>FRAME RATE</strong></td><td><strong>ORIGINAL</strong> (default), <strong>UP TO 60 FPS</strong>, <strong>UP TO 120 FPS</strong> or <strong>UNLIMITED</strong>, where the game allows it. Anything but original can break a game.</td></tr><tr><td><strong>EMULATION > MEMORY</strong></td><td>64 MB (default, original console) or 128 MB (development kits, for development builds).</td></tr><tr><td><strong>EMULATION > FAST DISC LOADING</strong></td><td>Faster loading. Some games may not expect it.</td></tr><tr><td><strong>VIDEO > WIDESCREEN</strong></td><td>Sets the console to widescreen (16:9), for the games that support it.</td></tr><tr><td><strong>VIDEO > HD VIDEO MODES</strong></td><td>Modes offered to the games: 480P (default), 480P + 720P or 480P + 720P + 1080I. HD modes need the <strong>HDTV</strong> signal.</td></tr><tr><td><strong>VIDEO > EMULATED VIDEO SIGNAL</strong></td><td>Emulated video cable: HDTV (default), COMPOSITE, S-VIDEO, SCART or VGA.</td></tr><tr><td><strong>VIDEO > PAL GAMES REFRESH RATE</strong></td><td>60 Hz (default) or 50 Hz.</td></tr><tr><td><strong>VISUAL RENDERING > UPSCALE FILTER</strong></td><td>BILINEAR (default), AMD FSR 1 or NEAREST.</td></tr><tr><td><strong>VISUAL RENDERING > CRT FILTER</strong></td><td>Soft scanlines, classic TV or arcade monitor.</td></tr><tr><td><strong>VISUAL RENDERING > OVERSCAN</strong></td><td>Hides the picture edges like a TV, or adds a border (negative values).</td></tr><tr><td><strong>VISUAL RENDERING > ASYNCHRONOUS SHADERS</strong></td><td>Less stuttering, but objects can be missing for a moment.</td></tr><tr><td><strong>AUDIO > AUDIO CHANNELS</strong></td><td>STEREO (default) or SURROUND 5.1.</td></tr></tbody></table>

#### **cxbx**

| Option                                      | Effect                                                                     |
| ------------------------------------------- | -------------------------------------------------------------------------- |
| **INTERNAL RESOLUTION**                     | Increases the rendering resolution (up to 12X).                            |
| **GAME ASPECT RATIO**                       | **KEEP ASPECT RATIO** (default) or **STRETCHED**.                          |
| **VIDEO > VIDEO STANDARD**                  | NTSC-M, NTSC-J or PAL, written to the EEPROM.                              |
| **EMULATION > DISABLE XBE SIGNATURE CHECK** | Enable it for homebrews.                                                   |
| **EMULATION > DISABLE PIXEL SHADERS**       | Can prevent some games from crashing. Only enable it if the game needs it. |
| **EMULATION > USE ALL CORES**               | Can improve performance, but can make some games crash.                    |

## Known issues

<table><thead><tr><th width="326.5">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>xemu stays on an Xbox error screen instead of starting the game</td><td>The image is not in XISO format: convert it (see <a href="xbox.md#converting-a-redump-image-to-xiso">Guides</a>) or run the game with xbased. <code>.xbe</code> files only run with xbased (<code>default.xbe</code>) and Cxbx.</td></tr><tr><td>xemu closes at launch</td><td>Check that <code>mcpx_1.0.bin</code> and <code>Complex_4627.bin</code> (or the BIOS selected in FORCE BIOS) are in <code>bios</code>.</td></tr><tr><td>xbased shows an error at launch or stays on a black screen</td><td>xbased needs a Vulkan 1.1 graphics card (1.3 recommended) with up-to-date drivers. Otherwise, use xemu or Cxbx.</td></tr><tr><td>A setting changed in the xbased menu is not kept</td><td>RetroBat applies its options at each launch: change the setting in the RetroBat Xbox system options. Patches, cheats and keys set for a game in xbased are kept.</td></tr><tr><td>Cxbx opens the Dokan page and the game does not start</td><td>Dokan 2 is not installed: it is required for <code>.iso</code> files (see <a href="xbox.md#running-.iso-files-with-cxbx">Guides</a>).</td></tr><tr><td>The game is not in the right language</td><td>Select the language with <strong>EMULATION > LANGUAGE</strong>. Some games only exist in English or in the languages of their region.</td></tr><tr><td>Stuttering at the start of a game with xemu</td><td>Shaders are compiled the first time they are used: keep <strong>SHADER CACHE</strong> enabled, the next sessions will be smoother.</td></tr><tr><td>Graphics bugs or crash with xemu</td><td>Change the video driver (<strong>DRIVERS > VIDEO</strong>), then try the game with xbased or Cxbx.</td></tr><tr><td>Saves made with one emulator do not appear in another</td><td>Each emulator has its own hard drive: saves are not shared. The xemu save import offered by xbased only looks for xemu in <code>AppData</code>: it does not find the RetroBat xemu.</td></tr><tr><td>Controller settings made in the emulator are lost</td><td>RetroBat redoes the configuration at each launch: disable <strong>AUTOCONFIGURE CONTROLLERS</strong> to keep yours.</td></tr></tbody></table>

The Sega **Chihiro**, an arcade board based on the Xbox, has its own page: see the [**Sega Chihiro**](../../arcade/sega/sega-chihiro.md) page.
