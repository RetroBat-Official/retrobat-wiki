---
description: Microsoft
---

# Xbox

<div align="left"><figure><img src="../../../../.gitbook/assets/image (547).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Overview

The **Xbox** is Microsoft's first home console. It was released in November 2001 in the United States, then in February 2002 in Japan and in March 2002 in Europe. It is built like a PC: an Intel Pentium III CPU at 733 MHz, an NVIDIA graphics chip (NV2A), 64 MB of memory and, for the first time on a console, a built-in 8 GB hard drive that stores saves and music ripped from CDs.

Its large original controller, nicknamed the "Duke", was quickly replaced by the more compact **Controller S**. In 2002, the **Xbox Live** service brought online play to consoles through the machine's Ethernet port. The Xbox sold about 24 million units before being replaced by the Xbox 360 at the end of 2005. Notable games include Halo: Combat Evolved, Halo 2, Fable, Star Wars: Knights of the Old Republic, Ninja Gaiden, Jet Set Radio Future and Project Gotham Racing.

RetroBat offers two emulators: **xemu**, which reproduces the console hardware and uses its BIOS, and **Cxbx-Reloaded**, which replaces the Xbox system with its own code and needs no BIOS.

{% embed url="https://en.wikipedia.org/wiki/Xbox_(console)" %}

## At a glance

<table><thead><tr><th width="216.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\xbox</code></td></tr><tr><td><strong>Extensions</strong></td><td>.xbe .iso .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>xemu</td></tr><tr><td><strong>BIOS</strong></td><td><code>mcpx_1.0.bin</code> and <code>Complex_4627.bin</code> (xemu only)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>No (xemu: snapshots from its menu)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Light guns</strong></td><td>cxbx</td></tr><tr><td><strong>Optional BIOS</strong></td><td><code>Cerbios.bin</code>, <code>Complex_4627v1.03.bin</code> (xemu, FORCE BIOS option)</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="145.75">Emulator</th><th width="308.5">Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>xemu</strong> (default)</td><td>The most compatible. Emulates the real hardware: hard drive, EEPROM, dashboard. Upscaling, Vulkan or OpenGL, snapshots.</td><td>Needs the BIOS. Only reads disc images in XISO format (<code>.iso</code>). No light guns.</td></tr><tr><td><strong>cxbx</strong> (Cxbx-Reloaded)</td><td>No BIOS. Runs extracted games (<code>.xbe</code>, <code>.decomp</code> folders). Supports the EMS TopGun light gun.</td><td>Lower compatibility, more graphics bugs. <code>.iso</code> files require Dokan 2 to be installed.</td></tr></tbody></table>

The xemu compatibility list ([xemu.app](https://xemu.app/#compatibility)) shows the status of each game. If a game has problems, try the other emulator.

## BIOS

Only **xemu** needs the BIOS. Cxbx-Reloaded does not use any.

<table><thead><tr><th>File</th><th width="102.75">Folder</th><th>Role</th><th>MD5</th></tr></thead><tbody><tr><td><code>mcpx_1.0.bin</code></td><td><code>bios</code></td><td>Boot ROM (MCPX), required</td><td><code>d49c52a4102f6df7bcf8d0617ac475ed</code></td></tr><tr><td><code>Complex_4627.bin</code></td><td><code>bios</code></td><td>BIOS (flash) used by default</td><td><code>39cee882148a87f93cb440b99dde3ceb</code></td></tr><tr><td><code>Cerbios.bin</code></td><td><code>bios</code></td><td>Alternative BIOS, optional</td><td></td></tr><tr><td><code>Complex_4627v1.03.bin</code></td><td><code>bios</code></td><td>Alternative BIOS, optional</td><td></td></tr></tbody></table>

RetroBat checks `mcpx_1.0.bin` and `Complex_4627.bin`. The alternative BIOS files are only used if you select them with the xemu **EMULATION > FORCE BIOS** option.

The console hard drive and EEPROM are not BIOS files to add: on first launch, RetroBat creates `xbox_hdd.qcow2` (a formatted hard drive, without a dashboard) and `eeprom.bin` in `saves\xbox`.

### Console language

The game language is the one stored in the console EEPROM. RetroBat writes it at each launch, for both emulators:

* by default, it is the RetroBat language (English if the Xbox does not have it);
* the **EMULATION > LANGUAGE** option forces a language: English, Japanese, German, French, Spanish, Italian, Korean, Chinese or Portuguese.

A game that does not exist in the selected language is displayed in its default language, often English.

## Which game format should I use?

<table><thead><tr><th width="172.75">Format</th><th width="101.25">xemu</th><th width="79.5">cxbx</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.iso</strong> (XISO)</td><td>✅</td><td>✅</td><td>Disc image in Xbox format (XISO). With Cxbx, the image is mounted as a drive with Dokan 2 (see <a href="xbox.md#running-.iso-files-with-cxbx">Guides</a>).</td></tr><tr><td><strong>.iso</strong> (Redump)</td><td>❌</td><td>❌</td><td>Full disc image, including the video partition: convert it to XISO (see <a href="xbox.md#converting-a-redump-image-to-xiso">Guides</a>).</td></tr><tr><td><strong>.xbe</strong></td><td>❌</td><td>✅</td><td>Executable of an extracted game (usually <code>default.xbe</code>).</td></tr><tr><td><strong><code>.decomp</code> folder</strong></td><td>❌</td><td>✅</td><td>Folder of an extracted game, renamed with <code>.decomp</code> at the end. Cxbx runs the <code>default.xbe</code> it contains.</td></tr></tbody></table>

`.zip` and `.7z` archives are not accepted: Xbox games must stay uncompressed.

## Controls

### Automatic configuration

RetroBat automatically configures controllers for both emulators, up to 4 players, in the RetroBat player order. The **AUTOCONFIGURE CONTROLLERS** option disables this configuration to keep the one made in the emulator.

<table><thead><tr><th width="297.75">Xbox</th><th>Controller</th></tr></thead><tbody><tr><td>A</td><td>SOUTH</td></tr><tr><td>B</td><td>EAST</td></tr><tr><td>X</td><td>WEST</td></tr><tr><td>Y</td><td>NORTH</td></tr><tr><td>White</td><td>L1</td></tr><tr><td>Black</td><td>R1</td></tr><tr><td>Left and right triggers</td><td>L2, R2</td></tr><tr><td>Back</td><td>SELECT</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Stick clicks</td><td>L3, R3</td></tr><tr><td>D-pad, sticks</td><td>D-pad, sticks</td></tr></tbody></table>

* **xemu** uses the layout of each controller recognized by SDL: Xbox, DualShock 4, DualSense and Switch Pro controllers work without any setting. Rumble is enabled.
* **Cxbx** emulates a **Controller S** by default. The **CONTROLS > PLAYER 1 CONTROLLER TYPE** option (up to 4) selects **GAMEPAD S** or **GAMEPAD DUKE**. Rumble is enabled with **CONTROLS > ENABLE RUMBLE**.

### Keyboard

A keyboard assigned to a player in RetroBat is configured with these keys:

| Xbox                                | xemu             | cxbx         |
| ----------------------------------- | ---------------- | ------------ |
| A, B, X, Y                          | A, B, X, Y       | S, D, W, E   |
| White, Black                        | 1, 2             | X, C         |
| Left, right triggers                | W, O             | Q, R         |
| Back, Start                         | BACKSPACE, ENTER | SPACE, ENTER |
| D-pad                               | Arrow keys       | Arrow keys   |
| Left stick (up, left, down, right)  | E, S, D, F       | T, F, G, H   |
| Right stick (up, left, down, right) | I, J, K, L       | I, J, K, L   |
| Stick clicks                        | 3, 4             | B, M         |

Keys are given for a QWERTY keyboard: both emulators use the key position, not its letter.

### Light guns

Light guns only work with **Cxbx**, which emulates the **EMS TopGun** light gun on player 1's port. It is used by games such as The House of the Dead III, Silent Scope Complete or Starsky & Hutch.

Enable the **GUNS > ENABLE GUN** option (or select **EMS TOPGUN** in **PLAYER 1 CONTROLLER TYPE**).

<table><thead><tr><th width="256.5">EMS TopGun</th><th>Light gun / mouse</th></tr></thead><tbody><tr><td>Aim</td><td>Light gun or mouse</td></tr><tr><td>Trigger</td><td>Trigger (left click)</td></tr><tr><td>Grip</td><td>Reload button (right click)</td></tr><tr><td>START</td><td>Key 1</td></tr><tr><td>SE/BA</td><td>Key 5</td></tr><tr><td>A, B</td><td>S, D keys</td></tr><tr><td>Gun stick</td><td>Arrow keys</td></tr></tbody></table>

* **GUNS > INVERT TRIGGER/RELOAD** swaps the trigger and the grip (useful with a WiiZapper).
* With a Wiimote on a DolphinBar, the D-pad is the stick, START is on button 1 or on + depending on the DolphinBar mode, and SE/BA on button 2 (mode 1 only).
* With a Sinden light gun, RetroBat starts the Sinden software automatically.

For more details on light guns, see the [**Lightguns**](../../../../controllers/supported-controllers/lightguns/) page.

### Hotkeys

**xemu**

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

**cxbx**

| Hotkey             | Action                                            | Keyboard |
| ------------------ | ------------------------------------------------- | -------- |
| **HOTKEY + START** | Exit                                              | F6       |
| —                  | Show the Cxbx interface (frame counter, settings) | F1       |
| —                  | Unlock the frame rate limit                       | F9       |

## Folders

| Content                                                 | Folder                                 |
| ------------------------------------------------------- | -------------------------------------- |
| xemu BIOS                                               | `bios`                                 |
| xemu: console hard drive (game saves, snapshots)        | `saves\xbox\xbox_hdd.qcow2`            |
| xemu: EEPROM (console language and settings)            | `saves\xbox\eeprom.bin`                |
| xemu: screenshots                                       | `screenshots\xemu`                     |
| xemu: configuration                                     | `emulators\xemu\xemu.toml`             |
| cxbx: emulated hard drive (saves in `Partition1\UDATA`) | `emulators\cxbx-reloaded\EmuDisk`      |
| cxbx: EEPROM                                            | `emulators\cxbx-reloaded\EEPROM.bin`   |
| cxbx: configuration                                     | `emulators\cxbx-reloaded\settings.ini` |

Game saves are stored on each emulator's hard drive: they are not shared between xemu and Cxbx.

## Guides

### Adding a game

1. Check that the game is in XISO format (see below).
2. Copy the `.iso` file to `roms\xbox`.
3. For xemu, add `mcpx_1.0.bin` and `Complex_4627.bin` to `bios`.
4. Update the RetroBat game list and launch the game.

### Converting a Redump image to XISO

"Redump" images contain the whole disc, including a video partition that the Xbox does not read. Neither xemu nor Cxbx accept them. To convert them, use [**extract-xiso**](https://github.com/xboxdev/extract-xiso) or [**xdvdfs**](https://github.com/antangelo/xdvdfs), two free tools:

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

### Using your own hard drive

The hard drive created by RetroBat is empty and has no dashboard. To use the hard drive of a console (with its dashboard and saves) or an image prepared for xemu, replace `saves\xbox\xbox_hdd.qcow2` with your image, using the same name. Keep a copy of the old file: it contains your saves.

### Other useful options

**xemu**

<table><thead><tr><th width="330.25">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Increases the rendering resolution (up to 10X). The native resolution is 640x480.</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td><strong>NATIVE</strong>, <strong>4:3</strong> or <strong>16:9</strong>. By default, xemu chooses automatically.</td></tr><tr><td><strong>EMULATION > MEMORY</strong></td><td>128 MB (RetroBat default, like development kits) or 64 MB (original console).</td></tr><tr><td><strong>EMULATION > SKIP BOOT</strong></td><td>On by default: skips the Xbox boot animation.</td></tr><tr><td><strong>VIDEO > DISPLAY MODE</strong></td><td>Picture placement: scaled (default), centered or stretched.</td></tr><tr><td><strong>VIDEO > EMULATED VIDEO SIGNAL</strong></td><td>Emulated video cable: HDTV (default), SCART, VGA, RFU, S-VIDEO or COMPOSITE.</td></tr><tr><td><strong>VISUAL RENDERING > SHADER CACHE</strong></td><td>On by default: less stuttering once shaders are saved.</td></tr><tr><td><strong>AUDIO > DSP EMULATION</strong></td><td>More accurate sound (effects, reverb), but more demanding. <strong>DSP JIT ENGINE</strong> speeds up this emulation (experimental).</td></tr><tr><td><strong>DRIVERS > VIDEO</strong></td><td>OPENGL (default) or VULKAN.</td></tr><tr><td><strong>USER INTERFACE > SHOW MENU BAR</strong></td><td>Shows the xemu menu bar at the top of the screen.</td></tr></tbody></table>

**cxbx**

| Option                                      | Effect                                                                     |
| ------------------------------------------- | -------------------------------------------------------------------------- |
| **INTERNAL RESOLUTION**                     | Increases the rendering resolution (up to 12X).                            |
| **GAME ASPECT RATIO**                       | **KEEP ASPECT RATIO** (default) or **STRETCHED**.                          |
| **VIDEO > VIDEO STANDARD**                  | NTSC-M, NTSC-J or PAL, written to the EEPROM.                              |
| **EMULATION > DISABLE XBE SIGNATURE CHECK** | Enable it for homebrews.                                                   |
| **EMULATION > DISABLE PIXEL SHADERS**       | Can prevent some games from crashing. Only enable it if the game needs it. |
| **EMULATION > USE ALL CORES**               | Can improve performance, but can make some games crash.                    |

## Known issues

| Issue                                                           | Solution                                                                                                                                                      |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| xemu stays on an Xbox error screen instead of starting the game | The image is not in XISO format: convert it (see [Guides](xbox.md#converting-a-redump-image-to-xiso)). `.xbe` files and `.decomp` folders only run with Cxbx. |
| xemu closes at launch                                           | Check that `mcpx_1.0.bin` and `Complex_4627.bin` (or the BIOS selected in FORCE BIOS) are in `bios`.                                                          |
| Cxbx opens the Dokan page and the game does not start           | Dokan 2 is not installed: it is required for `.iso` files (see [Guides](xbox.md#running-.iso-files-with-cxbx)).                                               |
| The game is not in the right language                           | Select the language with **EMULATION > LANGUAGE**. Some games only exist in English or in the languages of their region.                                      |
| Stuttering at the start of a game with xemu                     | Shaders are compiled the first time they are used: keep **SHADER CACHE** enabled, the next sessions will be smoother.                                         |
| Graphics bugs or crash with xemu                                | Change the video driver (**DRIVERS > VIDEO**), then try the game with Cxbx.                                                                                   |
| Saves made with xemu do not appear in Cxbx                      | Each emulator has its own hard drive: saves are not shared.                                                                                                   |
| Controller settings made in the emulator are lost               | RetroBat redoes the configuration at each launch: disable **AUTOCONFIGURE CONTROLLERS** to keep yours.                                                        |

The Sega **Chihiro**, an arcade board based on the Xbox, has its own page: see the [**Sega Chihiro**](../../arcade/sega/sega-chihiro.md) page.
