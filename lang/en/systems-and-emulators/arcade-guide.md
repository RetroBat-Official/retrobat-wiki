# Arcade Guide

<div align="left"><figure><img src="../.gitbook/assets/image (292).png" alt=""><figcaption></figcaption></figure></div>

Arcade games are more complex to emulate than console games: each arcade machine is different, and the game files (ROMs) must match the emulator you use. This guide explains the basics: which system and emulator to use, what romsets are, and how to check them.

## Which system should I use?

Arcade emulators can be split in two families:

* **Multi-machine emulators** (MAME, FinalBurn Neo…): they run thousands of arcade machines.
* **Dedicated emulators** (Supermodel, Flycast, Demul…): they run one family of arcade boards (Model 3, Naomi…), usually with better performance.

In RetroBat, each family of arcade games has its own folder in `roms`. Put your games in the folder that matches the emulator and the romset you have.

## Multi-machine emulators

<table><thead><tr><th width="117.75">System</th><th width="153">Folder</th><th width="261.75">Emulators / cores</th><th>Romset version</th></tr></thead><tbody><tr><td>MAME</td><td><code>roms\mame</code></td><td>MAME (standalone), lr-mame</td><td>MAME 0.289 (current version)</td></tr><tr><td></td><td></td><td>GroovyMAME</td><td>Same as MAME</td></tr><tr><td></td><td></td><td>lr-mame2016</td><td>MAME 0.174</td></tr><tr><td></td><td></td><td>lr-mame2014</td><td>MAME 0.159</td></tr><tr><td></td><td></td><td>lr-mame2010</td><td>MAME 0.139</td></tr><tr><td></td><td></td><td>lr-mame2003_plus</td><td>MAME 0.78-plus (latest)</td></tr><tr><td></td><td></td><td>lr-mame2003, lr-mame2003_midway</td><td>MAME 0.78</td></tr><tr><td></td><td></td><td>lr-mame2000</td><td>MAME 0.37b5</td></tr><tr><td>FinalBurn Neo</td><td><code>roms\fbneo</code></td><td>FBNeo (standalone), lr-fbneo</td><td>Latest FBNeo</td></tr><tr><td></td><td></td><td>lr-fbalpha</td><td>FB Alpha 0.2.97.44</td></tr><tr><td></td><td></td><td>lr-fbalpha2012</td><td>FB Alpha 0.2.97.29</td></tr><tr><td>MAME Homebrew</td><td><code>roms\hbmame</code></td><td>HBMAME, lr-mame</td><td>HBMAME</td></tr></tbody></table>

{% hint style="info" %}
* **MAME** is the most complete: use it by default.
* **FinalBurn Neo** is often lighter and very good for fighting games, beat'em ups and shoot'em ups (CPS, Neo Geo, Cave…).
{% endhint %}

### Systems by board family

These systems use the same multi-machine emulators, but group the games of one board family in their own folder:

<table><thead><tr><th width="182">System</th><th width="160.5">Folder</th><th>Emulators / cores</th></tr></thead><tbody><tr><td>CPS-1</td><td><code>roms\cps1</code></td><td>lr-fbneo, lr-fbalpha2012_cps1, lr-fbalpha, lr-fbalpha2012</td></tr><tr><td>CPS-2</td><td><code>roms\cps2</code></td><td>lr-fbneo, lr-fbalpha2012_cps2, lr-fbalpha, lr-fbalpha2012</td></tr><tr><td>CPS-3</td><td><code>roms\cps3</code></td><td>lr-fbneo, lr-fbalpha2012_cps3, lr-fbalpha, lr-fbalpha2012</td></tr><tr><td>CAVE</td><td><code>roms\cave</code></td><td>lr-fbneo, lr-fbalpha, lr-fbalpha2012, lr-mame2003_plus, lr-mame2016, lr-mame, MAME, Demul</td></tr><tr><td>Neo Geo</td><td><code>roms\neogeo</code></td><td>lr-fbneo, lr-geolith (<code>.neo</code> files), lr-fbalpha, lr-fbalpha2012_neogeo, Raine, MAME</td></tr><tr><td>Neo Geo CD</td><td><code>roms\neogeocd</code></td><td>lr-neocd, lr-fbneo, Raine</td></tr><tr><td>Hyper Neo Geo 64</td><td><code>roms\neogeo64</code></td><td>lr-mame, lr-mame2016, MAME</td></tr><tr><td>ST-V</td><td><code>roms\segastv</code></td><td>lr-kronos, lr-mame (all versions), Mednafen, MAME</td></tr></tbody></table>

## Dedicated emulators

<table><thead><tr><th width="203.25">Arcade machine(s)</th><th width="198.25">Folder</th><th>Emulators</th></tr></thead><tbody><tr><td>Laserdisc (FMV games)</td><td><code>roms\daphne</code></td><td>Hypseus, Daphne, Singe 2</td></tr><tr><td>Singe</td><td><code>roms\singe</code></td><td>Hypseus, Singe 2</td></tr><tr><td>ActionMax</td><td><code>roms\actionmax</code></td><td>Hypseus, Singe 2</td></tr><tr><td>DICE</td><td><code>roms\dice</code></td><td>lr-dice</td></tr><tr><td>Sega Model 2</td><td><code>roms\model2</code></td><td>Model 2 Emulator (multi CPU / single CPU), SM2-emu, lr-sm2, lr-mame, MAME</td></tr><tr><td>Sega Model 3</td><td><code>roms\model3</code></td><td>Supermodel, lr-supermodel, Model3-Vulkan</td></tr><tr><td>Atomiswave</td><td><code>roms\atomiswave</code></td><td>Flycast, lr-flycast, Demul</td></tr><tr><td>Sega Naomi</td><td><code>roms\naomi</code></td><td>Flycast, lr-flycast, Demul</td></tr><tr><td>Sega Naomi 2</td><td><code>roms\naomi2</code></td><td>Flycast, lr-flycast, Demul</td></tr><tr><td>Sega Hikaru</td><td><code>roms\hikaru</code></td><td>Odin, Demul</td></tr><tr><td>Gaelco PowerVR</td><td><code>roms\gaelco</code></td><td>Demul, lr-mame, lr-mame2016, lr-mame2014</td></tr><tr><td>Triforce</td><td><code>roms\triforce</code></td><td>Dolphin, lr-dolphin, Dolphin-Triforce, TeknoParrot</td></tr><tr><td>Sega Chihiro</td><td><code>roms\chihiro</code></td><td>xemu-chihiro, Cxbx-Reloaded, TeknoParrot</td></tr><tr><td>Sega Lindbergh</td><td><code>roms\lindbergh</code></td><td>Linuxloader, TeknoParrot</td></tr><tr><td>PSX Arcade (ZN-1/ZN-2…)</td><td><code>roms\psxarcade</code></td><td>ArcadeDuck, PSXMame, Zinc, lr-mame, MAME</td></tr><tr><td>Namco 246/256</td><td><code>roms\namco2x6</code></td><td>PCSX2x6, Play!, TeknoParrot</td></tr><tr><td>Namco 357/369</td><td><code>roms\namco3xx</code></td><td>TeknoParrot</td></tr><tr><td>PC-based arcade</td><td><code>roms\teknoparrot</code></td><td>TeknoParrot</td></tr></tbody></table>

{% hint style="info" %}
Each system has its own page in [Supported Game Systems](supported-game-systems/), with the file formats and BIOS needed.
{% endhint %}

## Understanding romsets

### Terminology

* **ROM, romset**: an arcade game is usually a `.zip` file containing several ROM files (the chips of the original board). That is why an arcade game is often called a **romset**.
* **Romset version**: each emulator version expects ROMs from **the same version**. For example, lr-mame2000 needs MAME 0.37b5 ROMs: MAME 0.139 ROMs (for lr-mame2010) will not work correctly with it, and vice versa. **Your romset version must match the emulator or core you use.**
* **Parent / clone**: a game often exists in several versions (regions, revisions, bootlegs). One of them is the **parent** (for example `sf2.zip`), the others are **clones** (`sf2ua.zip`, `sf2j.zip`…). Clones only contain the files that differ from the parent.
* **BIOS**: some boards share a BIOS, also stored as a romset (`neogeo.zip`, `naomi.zip`, `pgm.zip`…). It must be in the same folder as the games (or in `bios`, depending on the emulator).

### Romset types

<table><thead><tr><th width="180.75">Type</th><th width="329.25">Content</th><th>Use in RetroBat</th></tr></thead><tbody><tr><td><strong>Non-merged</strong></td><td>Each zip contains everything needed by the game, including the files of its parent. Only BIOS are separate.</td><td>✅ <strong>Recommended</strong>: each game works on its own</td></tr><tr><td><strong>Full non-merged</strong></td><td>Like non-merged, but each zip also contains the BIOS.</td><td>✅ Works, but takes more space</td></tr><tr><td><strong>Split</strong></td><td>Clones only contain their own files: the <strong>parent zip is required</strong> in the same folder (for example <code>sf2ua.zip</code> needs <code>sf2.zip</code>).</td><td>⚠️ Works if you keep the parents</td></tr><tr><td><strong>Merged</strong></td><td>All the clones are inside the parent zip.</td><td>❌ Not supported: only the parent game appears in RetroBat</td></tr></tbody></table>

{% hint style="warning" %}
* Use **non-merged** romsets whenever possible.
* **Do not rename** the zip files: the emulators and the scrapers recognize the games by their file name.
* **Do not unzip** arcade games.
{% endhint %}

### Checking and rebuilding your romsets

If a game does not start, the most common cause is a romset that does not match the emulator version. Tools like [clrmamepro](https://mamedev.emulab.it/clrmamepro/) check your romsets against a **DAT file** (the official list of files for one emulator version) and can rebuild them in the right format.

1. **Get the DAT file** for your emulator version:
   * MAME: on [Progetto Snaps](https://www.progettosnaps.net/dats/MAME/), or generate it with MAME: `mame.exe -listxml > mame.xml` (from the `emulators\mame` folder);
   * FinalBurn Neo: in the [FBNeo repository](https://github.com/libretro/FBNeo/tree/master/dats);
   * older libretro cores (mame2003, mame2010, fbalpha2012…): in the repository of each core, or in the [libretro arcade guide](https://docs.libretro.com/guides/arcade-getting-started/).
2. In clrmamepro, **Add DatFile**, then load it.
3. **Settings**: add your ROM folder (for example `roms\mame`).
4. **Scanner**: check your romsets. Missing or wrong files are listed.
5. **Rebuilder**: rebuild your romsets in **non-merged** format into a new folder, then copy them to the RetroBat folder.

{% hint style="info" %}
The [libretro arcade guide](https://docs.libretro.com/guides/arcade-getting-started/) explains romsets and clrmamepro in more detail.
{% endhint %}

## Additional files

### Samples

Some games need **samples** (recorded sounds) to play their sounds. Place the samples zip files (for example `galaga.zip`) in the folder of your emulator:

<table><thead><tr><th width="331.5">Emulator / core</th><th>Folder</th></tr></thead><tbody><tr><td>MAME (standalone), lr-mame</td><td><code>bios\mame\samples</code></td></tr><tr><td>lr-mame2016</td><td><code>bios\mame2016\samples</code></td></tr><tr><td>lr-mame2014</td><td><code>bios\mame2014\samples</code></td></tr><tr><td>lr-mame2010</td><td><code>bios\mame2010\samples</code></td></tr><tr><td>lr-mame2003_plus</td><td><code>bios\mame2003-plus\samples</code></td></tr><tr><td>lr-mame2003</td><td><code>bios\mame2003\samples</code></td></tr><tr><td>HBMAME</td><td><code>bios\hbmame\samples</code></td></tr><tr><td>FBNeo, lr-fbneo</td><td><code>bios\fbneo\samples</code></td></tr><tr><td>lr-fbalpha2012</td><td><code>bios\fba\samples</code></td></tr></tbody></table>

### CHD files

Some arcade games also need a **CHD** file (a hard disk, CD or laserdisc image of the original machine).

Put the CHD file in a folder named exactly like the game zip, next to the zip. For example, for `kinst.zip`: `roms\mame\kinst\kinst.chd`.

<div align="left"><figure><img src="../.gitbook/assets/image (293).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
The CHD version must also match the emulator version, like the romsets.
{% endhint %}

## Arcade controls

RetroBat uses the same arcade controls for most arcade emulators:

<table><thead><tr><th width="302.75">Function</th><th width="220.75">Controller</th><th>Keyboard</th></tr></thead><tbody><tr><td>Insert a coin (player 1 / player 2)</td><td>SELECT</td><td><code>5</code> / <code>6</code></td></tr><tr><td>Start (player 1 / player 2)</td><td>START</td><td><code>1</code> / <code>2</code></td></tr><tr><td>Test (operator menu)</td><td>R3</td><td><code>9</code></td></tr><tr><td>Service (free credit)</td><td>L3</td><td><code>0</code></td></tr><tr><td>Quit the game</td><td>HOTKEY + START</td><td><code>Esc</code></td></tr></tbody></table>

{% hint style="warning" %}
Test and Service on the controller (R3 / L3) can be enabled or disabled in the [ADVANCED SYSTEM OPTIONS](../navigation/configuration-of-systems-and-games.md#for-a-system) of some emulators, to avoid opening the operator menu by mistake:

* MAME and SM2-emu: **CONTROLS** > **TEST/SERVICE ON L3/R3** (enabled by default);
* Supermodel / Model3-Vulkan, Flycast, PCSX2x6, lr-kronos: **EMULATION** > **ENABLE SERVICE MENU** (disabled by default).

The keyboard keys `0` (Test) and `9` (Service) always work.
{% endhint %}

### Arcade stick layouts

For many arcade emulators (MAME, lr-mame, FBNeo, Flycast, Supermodel, TeknoParrot…), RetroBat can place the buttons like on the original arcade cabinet, according to your controller. Choose the layout in **ADVANCED SYSTEM OPTIONS** > **CONTROLS** > **CONTROLLER LAYOUT**:

<table><thead><tr><th width="245.25">Layout</th><th>For</th></tr></thead><tbody><tr><td><strong>CONTROLLER (SNES)</strong></td><td>A gamepad (default)</td></tr><tr><td><strong>MODERN 8 BUTTONS</strong></td><td>8-button arcade stick: X, Y, RB, LB on the top row / A, B, RT, LT on the bottom row</td></tr><tr><td><strong>8 BUTTONS ALTERNATIVE</strong></td><td>8-button arcade stick: X, Y, LB, LT on the top row / A, B, RB, RT on the bottom row</td></tr><tr><td><strong>6 BUTTONS</strong></td><td>6-button arcade stick: X, Y, LB on the top row / A, B, RB on the bottom row</td></tr><tr><td><strong>CLASSIC 8 BUTTONS</strong></td><td>Same as <strong>6 BUTTONS</strong></td></tr></tbody></table>

The list of compatible emulators and the stick setup are detailed on the [Arcade Sticks](../controllers/supported-controllers/arcade-sticks.md) page.

### Customizing arcade controls

For many arcade emulators, RetroBat maps the controls **game by game**, using mapping files provided in `system\resources\inputmapping`:

<table><thead><tr><th width="307.75">Emulator</th><th>Mapping file</th></tr></thead><tbody><tr><td>MAME (standalone)</td><td><code>mame\&#x3C;game>.xml</code> (one file per game)</td></tr><tr><td>lr-mame and other libretro cores</td><td><code>libretro_&#x3C;core>.yml</code> (for example <code>libretro_mame.yml</code>), <code>libretro_&#x3C;core>_&#x3C;system>.yml</code> (for example <code>libretro_flycast_naomi.yml</code>)</td></tr><tr><td>FBNeo (standalone)</td><td><code>fbneo.yml</code></td></tr><tr><td>Flycast (Naomi, Atomiswave)</td><td><code>flycast_Arcade.yml</code></td></tr><tr><td>Supermodel / Model3-Vulkan</td><td><code>supermodel.yml</code> / <code>model3vulkan.yml</code></td></tr><tr><td>SM2-emu</td><td><code>sm2emu.yml</code></td></tr><tr><td>Odin</td><td><code>odin.yml</code></td></tr><tr><td>ArcadeDuck</td><td><code>arcadeduck.yml</code></td></tr><tr><td>Play! (Namco 246/256)</td><td><code>play_Arcade.yml</code></td></tr><tr><td>TeknoParrot</td><td><code>teknoparrot.yml</code></td></tr></tbody></table>

To change the mapping of a game, **copy the file to `user\inputmapping`** (keeping the same name and subfolder, for example `user\inputmapping\mame\sf2.xml`) and modify the copy: RetroBat uses your file first. Files in `system\resources\inputmapping` are replaced at each update.

{% hint style="info" %}
* For MAME, if no file exists for a clone, the file of its parent game is used.
* Steering wheel mappings are in separate files (`*_wheels.yml`, `wheels` folder): see [Wheels](../controllers/supported-controllers/wheels.md).
{% endhint %}

Detailed guides: [Emulator specific controls mapping](../controllers/specific_mapping/).

## Links and references

{% hint style="info" %}
**Credits**

Part of this page is based on the libretro documentation: [https://docs.libretro.com/guides/arcade-getting-started/](https://docs.libretro.com/guides/arcade-getting-started/)
{% endhint %}
