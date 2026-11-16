---
description: Sega
---

# Sega Model 3

<div align="left"><figure><img src="../../../../.gitbook/assets/image (571).png" alt="" width="482"><figcaption></figcaption></figure></div>

## Overview

The **Sega Model 3** is Sega's third 3D arcade board, released in 1996. Built with Lockheed Martin around a PowerPC CPU and the Real3D Pro-1000 graphics processor, it displays graphics far ahead of the consoles of the time: the Dreamcast only came out in 1998. Several revisions followed (Step 1.0, 1.5, 2.0 and 2.1), each more powerful.

The library counts around twenty games, including **Virtua Fighter 3**, **Scud Race**, **Daytona USA 2**, **Sega Rally 2**, **The Lost World: Jurassic Park**, **Star Wars Trilogy Arcade**, **Fighting Vipers 2**, **Spikeout**, **Virtua Striker 2**, **Virtual On 2: Oratorio Tangram** and **Sega Bass Fishing**.

RetroBat offers four emulators: **Supermodel** (the reference Model 3 emulator), **Keisho** (formerly sm2-emu, an emulator dedicated to Model 1, 2 and 3), the **supermodel** libretro core, and **Model3-Vulkan** (a Vulkan version of Supermodel).

{% embed url="https://en.wikipedia.org/wiki/List_of_Sega_arcade_system_boards#Sega_Model_3" %}

## At a glance

<table><thead><tr><th width="230.25"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\model3</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .decomp</td></tr><tr><td><strong>Default emulator</strong></td><td>supermodel</td></tr><tr><td><strong>BIOS</strong></td><td>None</td></tr><tr><td><strong>Controller configuration</strong></td><td>Automatic, all emulators</td></tr><tr><td><strong>Save states</strong></td><td>libretro core, Keisho, Model3-Vulkan; Supermodel with hotkeys</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>No</td></tr><tr><td><strong>Guns</strong></td><td>supermodel, Keisho, libretro core, Model3-Vulkan</td></tr><tr><td><strong>Wheels</strong></td><td>supermodel, Keisho, Model3-Vulkan</td></tr></tbody></table>

## Which emulator should I choose?

<table><thead><tr><th width="159.5">Emulator</th><th>Strengths</th><th>Limits</th></tr></thead><tbody><tr><td><strong>supermodel</strong> (default)</td><td>The reference: all games, guns, wheels and force feedback, widescreen.</td><td>Save states not managed by RetroBat. With two players, both controllers must use the same driver.</td></tr><tr><td><strong>keisho</strong></td><td>Modern emulator: Vulkan / OpenGL, upscaling, CRT filter, save states, rewind; no setting needed in the cabinet test menus.</td><td>Brand new Model 3 support (63 romsets); the Sega Rally 2 prototypes do not start.</td></tr><tr><td><strong>libretro: supermodel</strong></td><td>RetroArch features (shaders, save states).</td><td>Beta version.</td></tr><tr><td><strong>model3-vulkan</strong></td><td>Vulkan version of Supermodel: internal resolution, HD textures, CRT filter, save states.</td><td>Requires a Vulkan 1.3 graphics card.</td></tr></tbody></table>

## BIOS

The Model 3 has no BIOS: nothing to install.

## Which game format?

Games are MAME `.zip` archives, to be kept as they are: do not extract or rename them.

* Clones (`scudplus`, `vf3tb`, `dayto2pe`…) need their parent game (`scud`, `vf3`, `daytona2`) in the same folder, except with a non-merged romset. Keisho looks for the parent next to the archive.
* Keisho identifies games by their content: a merged archive holding several versions runs the one named like the archive.

The `.decomp` extension is for PC ports, see the [**Recompilations**](../../others/recomp.md) page.

## Controls

### Automatic configuration

RetroBat automatically configures controllers for all emulators. The **AUTOCONFIGURE CONTROLLERS** option keeps your own configuration.

For all games: **START** = Start, **SELECT** = coin. On the keyboard: 1 / 2 = player 1 / 2 Start, 5 / 6 = coin, 9 = Service, 0 = Test.

**CONTROLLER LAYOUT** adapts the buttons to arcade sticks (modern8, 8alternative, 6alternative). For more details on arcade layouts, see the [**Arcade Guide**](https://app.gitbook.com/s/Cgoewyw8Sagl6SNUMrCG/systemes-and-emulateurs/arcade-guide) page.

### Supermodel and Model3-Vulkan

Both emulators share the same layout, set per game in `supermodel.yml` (`system\resources\inputmapping`, editable copy in `user\inputmapping`). Model3-Vulkan first reads a `model3vulkan.yml` file if there is one.

<table><thead><tr><th width="319">Game</th><th>Controls</th></tr></thead><tbody><tr><td>Virtua Fighter 3 (<code>vf3</code>, <code>vf3tb</code>), Fighting Vipers 2 (<code>fvipers2</code>)</td><td>D-pad or left stick: movement; WEST: punch; SOUTH: kick; EAST: guard; NORTH: escape</td></tr><tr><td>Spikeout (<code>spikeout</code>, <code>spikeofe</code>)</td><td>D-pad or left stick: movement; SOUTH: beat; WEST: charge; EAST or R1: shift; NORTH: jump</td></tr><tr><td>Virtua Striker 2 (<code>vs2</code>, <code>vs298</code>, <code>vs2v991</code>…)</td><td>D-pad or left stick: movement; SOUTH: long pass; EAST: shoot; WEST: short pass</td></tr><tr><td>Daytona USA 2 (<code>daytona2</code>), Scud Race (<code>scud</code>, <code>scudplus</code>…)</td><td>Left stick: steering; R2 / L2: accelerate / brake; R1 / L1: gear up / down; NORTH, SOUTH, WEST, EAST: gears 1, 2, 3, 4; D-pad up, down, left, right: VR1 to VR4</td></tr><tr><td>Sega Rally 2, Le Mans 24, Dirt Devils, Emergency Call Ambulance</td><td>Left stick: steering; R2 / L2: accelerate / brake; R1 / L1: gear up / down; right stick: gears (up 1, down 2, left 3, right 4); NORTH: view; SOUTH: handbrake</td></tr><tr><td>Harley-Davidson &#x26; L.A. Riders (<code>harley</code>)</td><td>Same as the other driving games; SOUTH: rear brake; EAST: music select; NORTH: view</td></tr><tr><td>The Lost World (<code>lostwsga</code>), The Ocean Hunter (<code>oceanhun</code>), L.A. Machineguns (<code>lamachin</code>)</td><td>Gun or mouse: aim; left click: shoot; right click: reload (The Lost World) or 2nd trigger; aiming off-screen also reloads</td></tr><tr><td>Star Wars Trilogy Arcade (<code>swtrilgy</code>)</td><td>Left stick or mouse: flight stick; R2, WEST or left click: shoot; SOUTH or right click: event button</td></tr><tr><td>Virtual On 2 (<code>von2</code>)</td><td>Left stick: forward, back, strafe; right stick: turn; L2 / R2: left / right shot; WEST or L1 / EAST or R1: left / right turbo; NORTH: jump; SOUTH: crouch</td></tr><tr><td>Ski Champ (<code>skichamp</code>)</td><td>Left stick: turn; right stick: turn harder; L2 / R2: left / right pole; WEST, SOUTH, EAST: Select 1, 2, 3</td></tr><tr><td>Sega Bass Fishing / Get Bass (<code>bassdx</code>)</td><td>Left stick: rod; right stick: cabinet stick; R2: reel; SOUTH: cast; EAST: Select</td></tr><tr><td>Magical Truck Adventure (<code>magtruck</code>)</td><td>Left stick: lever; SOUTH: pedal</td></tr></tbody></table>

The **CONTROLS > USE SHOULDER BUTTONS FOR RACING GAMES** option puts the accelerator and brake on R1 / L1, and the gears on the D-pad (except Daytona USA 2 and Scud Race, whose layout is set by `supermodel.yml`).

### Keisho

Keisho follows the same logic, with its own buttons set in `keisho.yml`. For more details, see the [**Keisho controller mapping**](../../../../controllers/specific_mapping/keisho-controller-mapping.md) page.

<table><thead><tr><th width="256.5">Game</th><th>Controls</th></tr></thead><tbody><tr><td>Virtua Fighter 3, Fighting Vipers 2</td><td>Same as Supermodel: WEST: punch; SOUTH: kick; EAST: guard; NORTH: escape</td></tr><tr><td>Spikeout</td><td>Same as Supermodel: SOUTH: beat; WEST: charge; EAST: shift; NORTH: jump</td></tr><tr><td>Virtua Striker 2</td><td>Same as Supermodel: SOUTH: long pass; EAST: shoot; WEST: short pass</td></tr><tr><td>Driving games</td><td>Left stick: steering; R2 / L2: accelerate / brake; R1 / L1: gear up / down; SOUTH, EAST, WEST, NORTH: VR1 to VR4 buttons or view (Harley-Davidson: SOUTH = music select, EAST = view)</td></tr><tr><td>Gun games</td><td>Gun, mouse or stick: aim; SOUTH or R2: shoot; EAST or L2: reload</td></tr><tr><td>Star Wars Trilogy Arcade</td><td>Left stick: flight stick; R2 / L2: flight stick triggers; SOUTH / EAST: events 1 / 2</td></tr><tr><td>Sega Bass Fishing</td><td>Left stick: rod; right stick: cabinet stick; triggers: reel and line tension; SOUTH: cast; EAST: Select</td></tr><tr><td>Magical Truck Adventure</td><td>Left stick: lever; SOUTH: pedal</td></tr><tr><td>Virtual On 2 (fixed layout)</td><td>Left stick or D-pad: left lever; right stick or face buttons: right lever; L1 / R1: turbo; L2 / R2: shots</td></tr><tr><td>Ski Champ (fixed layout)</td><td>Left stick: turn; L1 / R1: poles; WEST, NORTH, EAST: Select 1, 2, 3</td></tr></tbody></table>

The Virtual On 2 and Ski Champ layouts belong to Keisho and cannot be changed.

### supermodel libretro core

The core uses the RetroArch layout, adjusted by RetroBat for Daytona USA 2, Scud Race, Fighting Vipers 2, Spikeout and Virtua Fighter 3 (`libretro_supermodel.yml` file). The **CONTROLS > SERVICE BUTTONS** option puts Service / Test on L3 / R3 (default) or on the shoulder buttons.

### Guns

Gun games: The Lost World, The Ocean Hunter, L.A. Machineguns.

Enable **GUNS > ENABLE GUN**.

* **Supermodel**: **MULTIGUN (RAW INPUT)** for two guns, **GUN 1 INDEX** / **GUN 2 INDEX** if the guns are not detected in the right order, **SHOW CROSSHAIR**, **USE MAMEHOOKER** and **OUTPUT GAME DATA** for feedback (recoil, lamps).
* **Model3-Vulkan**: **SHOW CROSSHAIR**, **CROSSHAIR STYLE**, **SINDEN BORDER SIZE**, **USE ONE GUN ONLY**, and the same MameHooker options.
* **Keisho**: without the option, Keisho is in automatic mode: it shows the crosshair in gun games, and you aim with the mouse or a controller stick. With the option, it uses the connected guns. **SHOW CROSSHAIR**, **HIDE SHOT FLASH**, **SINDEN BORDER SIZE**, **ENABLE GUN RECOIL** options.
* **libretro core**: **SHOW CROSSHAIR**, **USE ONE GUN ONLY**.

With Supermodel, Model3-Vulkan and the libretro core, gun games must be calibrated in their test menu (see [**Calibrate the guns**](sega-model-3.md#calibrate-the-guns) below). For more details on guns, see the [**Guns**](../../../../controllers/supported-controllers/lightguns/) page.

### Wheels

Supermodel, Keisho and Model3-Vulkan support wheels, with the **WHEELS > ENABLE WHEEL** option.

* Supermodel and Model3-Vulkan: **ENABLE FORCE FEEDBACK**, separate shifter; buttons set per wheel type in `model3_wheels.yml` (Model3-Vulkan first reads `model3vulkan_wheels.yml` if there is one). **FORCE WHEEL INDEX** selects the wheel if it is not detected.
* Keisho: **ENABLE FORCE FEEDBACK** and **FORCE FEEDBACK STRENGTH**; buttons set per wheel type in `keisho_wheels.yml`, steering and pedals detected by Keisho.
* libretro core: **ENABLE FORCE FEEDBACK**.

For more details on wheels, see the [**Wheels**](../../../../controllers/supported-controllers/wheels.md) page.

### Hotkeys

**Supermodel**

<table><thead><tr><th width="183.25">Hotkey</th><th>Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Exit</td><td>ESC</td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Save state</td><td>F5</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Load state</td><td>F7</td></tr><tr><td><strong>HOTKEY + UP</strong></td><td>Change save slot</td><td>F6</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test (<strong>EMULATION > ENABLE SERVICE MENU</strong> option)</td><td>9 / 0</td></tr><tr><td>—</td><td>Pause</td><td>ALT + P</td></tr><tr><td>—</td><td>Reset</td><td>ALT + R</td></tr><tr><td>—</td><td>Screenshot</td><td>ALT + S</td></tr><tr><td>—</td><td>Fullscreen</td><td>ALT + ENTER</td></tr><tr><td>—</td><td>Clear NVRAM</td><td>ALT + N</td></tr></tbody></table>

**Model3-Vulkan**

<table><thead><tr><th width="185.75">Hotkey</th><th>Action</th><th>Keyboard</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Exit</td><td>ESC</td></tr><tr><td><strong>HOTKEY + SOUTH</strong></td><td>Model3-Vulkan menu</td><td>F1</td></tr><tr><td><strong>HOTKEY + WEST</strong></td><td>Save state</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORTH</strong></td><td>Load state</td><td>F4</td></tr><tr><td><strong>HOTKEY + UP</strong></td><td>Change save slot</td><td>F7</td></tr><tr><td><strong>L3</strong> / <strong>R3</strong></td><td>Service / Test (<strong>EMULATION > ENABLE SERVICE MENU</strong> option)</td><td>9 / 0</td></tr><tr><td>—</td><td>Screenshot</td><td>F8</td></tr><tr><td>—</td><td>Pause</td><td>P</td></tr><tr><td>—</td><td>Fullscreen</td><td>ALT + ENTER</td></tr><tr><td>—</td><td>Toggle HD textures</td><td>ALT + H</td></tr><tr><td>—</td><td>Reload HD textures</td><td>F3</td></tr></tbody></table>

**Keisho**: same hotkeys as for the Model 1 (see the **Sega Model 1** page). In driving games, F1 to F5 shift gears on the keyboard: the menu moves to F10, save to F6 and load to F7, and the controller hotkeys follow automatically.

**libretro core**: usual RetroArch hotkeys (see the [**Hotkeys**](../../../../navigation/hotkeys.md) page).

Keisho and Model3-Vulkan keyboard keys can be customized, see the [**Hotkeys**](../../../../navigation/hotkeys.md) page.

## Folders

<table><thead><tr><th width="324">Content</th><th>Folder</th></tr></thead><tbody><tr><td>Supermodel: configuration</td><td><code>emulators\supermodel\Config\Supermodel.ini</code></td></tr><tr><td>Supermodel: NVRAM (cabinet settings and high scores)</td><td><code>emulators\supermodel\NVRAM</code></td></tr><tr><td>Supermodel: save states</td><td><code>emulators\supermodel\Saves</code></td></tr><tr><td>Keisho: NVRAM</td><td><code>saves\model3\keisho</code></td></tr><tr><td>Keisho: save states (managed by RetroBat)</td><td><code>saves\model3\keisho\sstates</code></td></tr><tr><td>Keisho: save states (emulator folder)</td><td><code>saves\model3\keisho\states</code></td></tr><tr><td>Keisho: screenshots</td><td><code>screenshots\keisho</code></td></tr><tr><td>Keisho: configuration</td><td><code>emulators\keisho\keisho.ini</code></td></tr><tr><td>Model3-Vulkan: configuration</td><td><code>emulators\model3-vulkan\Data\Config\Model3-Vulkan.ini</code></td></tr><tr><td>Model3-Vulkan: save states (managed by RetroBat)</td><td><code>saves\model3\model3-vulkan</code></td></tr><tr><td>Model3-Vulkan: save states (emulator folder)</td><td><code>emulators\model3-vulkan\Data\Saves</code></td></tr><tr><td>Model3-Vulkan: NVRAM</td><td><code>emulators\model3-vulkan\Data\NVRAM</code></td></tr><tr><td>Model3-Vulkan: screenshots</td><td><code>emulators\model3-vulkan\Data\Screenshots</code></td></tr><tr><td>Model3-Vulkan: HD textures</td><td><code>emulators\model3-vulkan\Data\Assets\HDTextures\&#x3C;game></code></td></tr><tr><td>Per-game button mapping</td><td><code>system\resources\inputmapping\supermodel.yml</code>, <code>keisho.yml</code>, <code>libretro_supermodel.yml</code> (editable copy in <code>user\inputmapping</code>)</td></tr><tr><td>Wheel buttons</td><td><code>system\resources\inputmapping\wheels\model3_wheels.yml</code> (Supermodel, Model3-Vulkan), <code>keisho_wheels.yml</code> (Keisho)</td></tr></tbody></table>

## Guides

### Service menu

The test menu of each cabinet gives access to the game settings (difficulty, gun calibration, network…).

* On the keyboard: **9** (Service) and **0** (Test), with all standalone emulators.
* On the controller: **L3** (Service) and **R3** (Test). With Supermodel and Model3-Vulkan, first enable **EMULATION > ENABLE SERVICE MENU**; with the libretro core, it is the default setting of **CONTROLS > SERVICE BUTTONS**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (572).png" alt=""><figcaption></figcaption></figure></div>

### Calibrate the guns

With Supermodel, Model3-Vulkan and the libretro core, open the test menu, then **GUN SETTINGS**, and follow the on-screen instructions. Keisho does not need it.

### HD textures (Model3-Vulkan)

Model3-Vulkan can replace the original textures with HD texture packs. Put the pack in `emulators\model3-vulkan\Data\Assets\HDTextures\<game>` (`<game>` = romset name, for example `scud`) and enable **VISUAL RENDERING > HD TEXTURE PACKS**.

### Other useful options

**Supermodel**

<table><thead><tr><th width="326.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>VIDEO > WIDESCREEN HACK</strong></td><td>Displays games in 16:9 (or stretched).</td></tr><tr><td><strong>VISUAL RENDERING > SUPERSAMPLING</strong></td><td>Smooths the picture, at the cost of performance.</td></tr><tr><td><strong>VIDEO > NEW 3D ENGINE</strong></td><td>On by default; turn it off only if the game shows an OpenGL error on an old graphics card.</td></tr><tr><td><strong>EMULATION > POWERPC FREQUENCY</strong></td><td>Automatic by default; increase it if a game slows down.</td></tr></tbody></table>

**Model3-Vulkan**

<table><thead><tr><th width="352.75">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>Increases the rendering resolution.</td></tr><tr><td><strong>WIDESCREEN HACK</strong></td><td>Displays games in 16:9 (or stretched).</td></tr><tr><td><strong>VISUAL RENDERING > CRT FILTER</strong> / <strong>CRT COLORS</strong></td><td>Look and colors of a CRT screen.</td></tr><tr><td><strong>VISUAL RENDERING > DISABLE WHITE FLASH</strong></td><td>Removes the white flash of the shots.</td></tr><tr><td><strong>CONTROLS > STEERING SMOOTHING</strong> / <strong>STEERING SENSITIVITY</strong></td><td>Controller steering settings in driving games (no effect on a wheel).</td></tr><tr><td><strong>CONTROLS > CHASE CAMERA STABILIZER</strong></td><td>Damps the chase camera swing in driving games, whatever the controller.</td></tr><tr><td><strong>AUDIO > AUDIO CHANNELS</strong></td><td><strong>QUADRAPHONIC</strong> (default, folded down to stereo on a 2-channel output), <strong>STEREO</strong> or <strong>SURROUND 5.1</strong>.</td></tr><tr><td><strong>VIDEO > LOW LATENCY</strong></td><td>Reduces display lag.</td></tr></tbody></table>

**Keisho**: **INTERNAL RESOLUTION**, **GAME ASPECT RATIO**, **VISUAL RENDERING > CRT FILTER**, **ADJUST BRIGHTNESS** (also on Model 3), **EMULATION > REWIND**. **TRANSLUCENCY** and **DRAW DISTANCE** only apply to Model 1 and Model 2. See also the [**Sega Model 1**](sega-model-1.md) page.

**libretro core**: **INTERNAL RESOLUTION**, **VIDEO > WIDESCREEN HACK**, **EMULATION > POWERPC FREQUENCY**.

## Known issues

<table><thead><tr><th width="342.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>"Network Board Not Present" message</td><td>Open the test menu, then <strong>Game Assignments > Link ID</strong>, and select <strong>Single</strong>. Keisho does not have this issue.</td></tr><tr><td>With Supermodel, the player 2 controller does not respond</td><td>Both controllers must use the same driver as the player 1 controller (two XInput controllers, or two non-XInput controllers). Change the driver in <strong>DRIVERS > INPUT</strong>, or try Model3-Vulkan or Keisho.</td></tr><tr><td>Player 1 and player 2 controllers are swapped (Supermodel)</td><td>Enable <strong>CONTROLS > SWITCH JOYPAD INDEX</strong>, or force the index of each controller.</td></tr><tr><td>A clone does not start</td><td>Put the parent game in <code>roms\model3</code>, or use a <a href="../../../arcade-guide.md#romset-types">non-merged romset</a>.</td></tr><tr><td>The crosshair of gun games does not follow the gun</td><td>Calibrate the gun in the test menu (<strong>GUN SETTINGS</strong>).</td></tr><tr><td>Model3-Vulkan does not start</td><td>Check that the graphics card and its driver support Vulkan 1.3, otherwise use Supermodel or Keisho.</td></tr><tr><td>Sega Rally 2 prototypes (<code>srally2p</code>, <code>srally2pa</code>): black screen with Keisho</td><td>These romsets do not work with Keisho yet: use Supermodel.</td></tr></tbody></table>
