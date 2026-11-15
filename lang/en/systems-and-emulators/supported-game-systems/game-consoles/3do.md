---
description: The 3do Company
---

# 3DO

<div align="left"><figure><img src="../../../.gitbook/assets/image (583).png" alt=""><figcaption></figcaption></figure></div>

### Overview

The **3DO Interactive Multiplayer** is a home console released in 1993. The 3DO Company, founded by Trip Hawkins (founder of Electronic Arts), did not build it itself: it licensed the design to manufacturers such as Panasonic (FZ-1, FZ-10), Goldstar or Sanyo. It runs on a 12.5 MHz ARM60 processor and reads its games on CD-ROM. Sold at a high price, it disappeared in 1996.

Among its games: **Gex**, **Road Rash**, **The Need for Speed**, **Star Control II**, **Super Street Fighter II Turbo**, **Return Fire**, **Wing Commander III**, **Samurai Shodown**, and American Laser Games light gun games (**Mad Dog McCree**, **Crime Patrol**, **Who Shot Johnny Rock?**).

RetroBat offers two emulators: the **opera** libretro core (default) and **Phoenix**.

{% embed url="https://en.wikipedia.org/wiki/3DO_Interactive_Multiplayer" %}

### At a glance

<table><thead><tr><th width="246.5"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\3do</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .iso .chd</td></tr><tr><td><strong>Default emulator</strong></td><td>libretro: opera</td></tr><tr><td><strong>BIOS</strong></td><td>None required (BIOS built into the opera core)</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro core</td></tr><tr><td><strong>RetroAchievements</strong></td><td>libretro core</td></tr><tr><td><strong>Netplay</strong></td><td>libretro core</td></tr><tr><td><strong>Light guns</strong></td><td>libretro core (up to 4)</td></tr><tr><td><strong>Optional BIOS</strong></td><td>Console BIOS (<code>panafz1.bin</code>, <code>panafz10.bin</code>...) and Kanji ROMs in <code>bios</code>; <code>panafz10.bin</code> needed by Phoenix</td></tr></tbody></table>

### Which emulator to choose?

<table><thead><tr><th width="157">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>libretro: opera</strong> (default)</td><td>Works without BIOS, save states, RetroAchievements, netplay, light guns, mouse and flight stick, RetroArch shaders and hotkeys.</td><td>—</td></tr><tr><td><strong>phoenix</strong></td><td>Standalone emulator, several renderers.</td><td>Needs <code>panafz10.bin</code>. No save states managed by RetroBat, no light guns.</td></tr></tbody></table>

### BIOS

The opera core includes **Opera Boot**, a free BIOS: no file is needed. An original BIOS remains the most compatible: when one is in `bios`, RetroBat uses it automatically (in the order of the table below), otherwise the core starts with Opera Boot. The **EMULATION > BIOS** option forces a BIOS.

<table><thead><tr><th width="190.75">File</th><th width="245.5">Console</th><th>MD5</th></tr></thead><tbody><tr><td><code>panafz1.bin</code></td><td>Panasonic FZ-1 (USA)</td><td>f47264dd47fe30f73ab3c010015c155b</td></tr><tr><td><code>panafz10.bin</code></td><td>Panasonic FZ-10 (USA), <strong>needed by Phoenix</strong></td><td>51f2f43ae2f3508a14d9f56597e2d3ce</td></tr><tr><td><code>panafz1j.bin</code></td><td>Panasonic FZ-1 (Japan)</td><td>a496cfdded3da562759be3561317b605</td></tr><tr><td><code>panafz10e-anvil.bin</code></td><td>Panasonic FZ-10 ANVIL (Europe)</td><td>a48e6746bd7edec0f40cff078f0bb19f</td></tr><tr><td><code>goldstar.bin</code></td><td>Goldstar GDO-101M</td><td>8639fd5e549bd6238cfee79e3e749114</td></tr><tr><td><code>sanyotry.bin</code></td><td>Sanyo TRY IMP-21J</td><td>35fa1a1ebaaeea286dc5cd15487c13ea</td></tr><tr><td><code>panafz10-norsa.bin</code></td><td>Panasonic FZ-10, RSA check disabled</td><td>1477bda80dc33731a65468c1f5bcbee9</td></tr><tr><td><code>panafz1j-norsa.bin</code></td><td>Panasonic FZ-1 (Japan), RSA check disabled</td><td>f6c71de7470d16abe4f71b1444883dc8</td></tr><tr><td><code>panafz10e-anvil-norsa.bin</code></td><td>Panasonic FZ-10 ANVIL, RSA check disabled</td><td>cf11bbb5a16d7af9875cca9de9a15e09</td></tr><tr><td><code>3do_arcade_saot.bin</code></td><td>Shootout at Old Tucson arcade cabinet</td><td>8970fc987ab89a7f64da9f8a8c4333ff</td></tr></tbody></table>

The "norsa" versions run unsigned software (homebrews).

Some Japanese games also need a Kanji font ROM, to be selected with **EMULATION > KANJI FONT ROM**:

<table><thead><tr><th width="249">File</th><th>MD5</th></tr></thead><tbody><tr><td><code>panafz1-kanji.bin</code></td><td>b8dc97f778a6245c58e064b0312e8281</td></tr><tr><td><code>panafz1j-kanji.bin</code></td><td>c23fb5d5e6bb1c240d02cf968972be37</td></tr><tr><td><code>panafz10ja-anvil-kanji.bin</code></td><td>428577250f43edc902ea239c50d2240d</td></tr></tbody></table>

All these files go in `bios`.

### Which game format?

<table><thead><tr><th width="185.25">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.cue</strong> / <strong>.bin</strong></td><td>Most common format. Keep the <code>.cue</code> and its <code>.bin</code> files together.</td></tr><tr><td><strong>.iso</strong></td><td>Single track image.</td></tr><tr><td><strong>.chd</strong></td><td>Compressed format, recommended to save space.</td></tr></tbody></table>

The opera core does not handle `.m3u` files: each disc of a multi-disc game is started on its own (see [**Multi-disc games**](3do.md#multi-disc-games) below).

### Controls

#### Automatic configuration

RetroBat configures the controllers automatically for both emulators. The **AUTOCONFIGURE CONTROLLERS** option lets you keep your own configuration.

<table><thead><tr><th width="219">3DO controller</th><th>Controller</th></tr></thead><tbody><tr><td>A</td><td>WEST</td></tr><tr><td>B</td><td>SOUTH</td></tr><tr><td>C</td><td>EAST</td></tr><tr><td>L / R</td><td>L1 / R1</td></tr><tr><td>P (Play / Pause)</td><td>START</td></tr><tr><td>X (Stop)</td><td>SELECT</td></tr><tr><td>D-pad</td><td>D-pad or left stick</td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (584).png" alt="" width="225"><figcaption></figcaption></figure></div>

With Phoenix, directions are on the left stick; enable **CONTROLS > USE DPAD** to play with the D-pad.

#### opera core: devices

The **CONTROLS** menu sets the device of each player with **PLAYER 1 CONTROLLER TYPE** (to 4):

* **3DO JOYPAD**: standard controller (default).
* **3DO FLIGHTSTICK**: left stick = stick, right stick = throttle, R2 = fire, A / B / C and the D-pad as on the controller.
* **3DO MOUSE**: for mouse games.
* **3DO LIGHTGUN**: for light gun games (see **Light guns**).

**NUMBER OF DEVICES** sets the number of devices seen by the console (1 by default): some games crash when several devices are plugged in.

#### Six-button controllers

With a Mega Drive style controller (8BitDo M30, Retro-bit 2.4 GHz controllers), RetroBat puts A, B and C on the bottom row. For some of these controllers, enable **CONTROLS > USE 3DO-LIKE CONTROLLER**.

#### Light guns

Light gun games (Mad Dog McCree, Crime Patrol, Corpse Killer, Drug Wars, Space Pirates, Who Shot Johnny Rock?...) work with the opera core, up to 4 guns. Enable **GUNS > ENABLE GUN**.

* Left click: fire; right click or shooting off-screen: reload.
* On the keyboard: 1 = Start, 5 = Select.
* **SHOW CROSSHAIR** shows the crosshair, **GUN A/B BUTTONS MAPPING** sets the auxiliary buttons (mouse, Wiimote D-pad or keyboard), **USE ONE GUN ONLY** sets up a single gun.
* With the cabinet BIOS (`3do_arcade_saot.bin`), RetroBat uses the arcade gun of the cabinet (coins, Start, service).

For more details on light guns, see the [**Lightguns**](../../../controllers/supported-controllers/lightguns/) page.

#### Hotkeys

**opera core**: usual RetroArch hotkeys (save, load, rewind...). For more details, see the [**Hotkeys**](../../../navigation/hotkeys.md) page.

**Phoenix**

<table><thead><tr><th width="254">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr></tbody></table>

RetroBat powers on the console and switches Phoenix to fullscreen automatically at launch.

### Folders

<table><thead><tr><th width="346.5">Content</th><th>Folder</th></tr></thead><tbody><tr><td>BIOS and Kanji ROMs</td><td><code>bios</code></td></tr><tr><td>opera core: game saves (NVRAM, one per game)</td><td><code>saves\3do\opera\per_game</code></td></tr><tr><td>opera core: game saves (shared NVRAM)</td><td><code>saves\3do\opera\shared</code></td></tr><tr><td>opera core: save states</td><td><code>saves\3do\libretro.opera</code></td></tr><tr><td>Screenshots</td><td><code>screenshots</code></td></tr><tr><td>Phoenix: configuration</td><td><code>emulators\phoenix\phoenix.config.xml</code></td></tr></tbody></table>

### Guides

#### Multi-disc games

The opera core does not swap discs during a game: start each disc on its own. To keep your progress from one disc to the next, the discs must share the same NVRAM:

* When the file name contains "Disc" (for example `Wing Commander III (Disc 1).cue`), RetroBat uses the shared NVRAM automatically.
* Otherwise, set **EMULATION > NVRAM STORAGE** to **SHARED** for this game.

#### Smoother games

The 3DO often shows few frames per second. **EMULATION > CPU CLOCK** raises the speed of the emulated processor (up to 4x): many games run smoother, at the cost of performance, and a few games may show glitches.

#### Other useful options (opera core)

<table><thead><tr><th width="281.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>EMULATION > VIDEO FORMAT</strong></td><td>NTSC (60 Hz) or PAL (50 Hz). Some European games need a European BIOS.</td></tr><tr><td><strong>EMULATION > CD READ SPEED</strong></td><td>Faster disc reads (2x originally); some games do not support it.</td></tr><tr><td><strong>EMULATION > OS HLE</strong></td><td>High level emulation of some system functions, may improve performance.</td></tr><tr><td><strong>EMULATION > DSP THREADED</strong></td><td>Sound runs on another processor core (on by default).</td></tr><tr><td><strong>VIDEO > HIGH RESOLUTION</strong></td><td>Rendering at doubled resolution (on by default).</td></tr></tbody></table>

**Phoenix**: **DRIVERS > VIDEO** (approximate software, original software or experimental hardware), **VERTICAL SYNC**, **VISUAL RENDERING > BILINEAR FILTERING**.

### Known issues

<table><thead><tr><th width="297.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>A game does not start or freezes with the built-in BIOS</td><td>Add an original BIOS to <code>bios</code> (for example <code>panafz10.bin</code>), or select it with <strong>EMULATION > BIOS</strong>.</td></tr><tr><td>A game crashes when several controllers are plugged in</td><td>Keep <strong>CONTROLS > NUMBER OF DEVICES</strong> on 1.</td></tr><tr><td>Missing text in a Japanese game</td><td>Add a Kanji ROM to <code>bios</code> and select it with <strong>EMULATION > KANJI FONT ROM</strong>.</td></tr><tr><td>An old save state no longer loads</td><td>The opera core changed its save state format at the end of 2026: older ones are no longer compatible. Game saves (NVRAM) are not affected.</td></tr><tr><td>Phoenix does not start</td><td>Put <code>panafz10.bin</code> in <code>bios</code>.</td></tr><tr><td>With Phoenix, the D-pad does not respond</td><td>Enable <strong>CONTROLS > USE DPAD</strong>.</td></tr></tbody></table>
