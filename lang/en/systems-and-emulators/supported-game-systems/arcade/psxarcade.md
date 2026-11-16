# PSXArcade

<div align="left"><figure><img src="../../../.gitbook/assets/image (589).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Overview

The **PSX Arcade** system gathers the arcade boards built around PlayStation hardware, from 1994. Sony supplied the base (R3000A processor, the console graphics chip) and each publisher adapted it to its cabinets: more memory, sound chips, CD or memory card drives.

The main boards:

| Board                                       | Publisher                                                         | Example games                                                                |
| ------------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| **ZN-1**, **ZN-2**                          | Capcom                                                            | Street Fighter EX, Star Gladiator, Rival Schools, Strider 2, Tech Romancer   |
| ZN-1 (other publishers)                     | Taito (FX-1), Tecmo, Atlus, Raizing, Video System, Acclaim, Atari | Ray Storm, G-Darius, Dead or Alive, Fighting Layer, Brave Blade, Beastorizer |
| **System 11**, **System 12**                | Namco                                                             | Tekken, Tekken 2, Tekken 3, Soul Edge, Soul Calibur, Point Blank 2, Ehrgeiz  |
| **G-Net**                                   | Taito                                                             | Psychic Force 2012, Chaos Heat, Zoku Otenamihaiken                           |
| **GV**, **GQ**, **System 573**, **Twinkle** | Konami                                                            | Dance Dance Revolution, beatmania IIDX, Simpsons Bowling                     |

RetroBat offers five emulators: **ArcadeDuck** (default), **PSXMame**, **Zinc**, the **mame** libretro core and **MAME**. This system replaces the former **Zinc** system: since RetroBat 8.4.0, the games in `roms\zinc` are moved automatically to `roms\psxarcade`.

## At a glance

<table><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Games folder</strong></td><td><code>roms\psxarcade</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .chd</td></tr><tr><td><strong>Default emulator</strong></td><td>arcadeduck</td></tr><tr><td><strong>BIOS</strong></td><td>Board BIOS in MAME format (<code>coh1000c.zip</code>, <code>coh3002c.zip</code>…), in <code>bios</code> or next to the games</td></tr><tr><td><strong>Controller setup</strong></td><td>Automatic: ArcadeDuck, PSXMame, Zinc, mame core, MAME</td></tr><tr><td><strong>Save states</strong></td><td>ArcadeDuck (managed by RetroBat, depending on the board), mame core</td></tr><tr><td><strong>RetroAchievements</strong></td><td>No</td></tr><tr><td><strong>Netplay</strong></td><td>mame core</td></tr><tr><td><strong>Light guns</strong></td><td>ArcadeDuck</td></tr><tr><td><strong>Optional BIOS</strong></td><td>—</td></tr></tbody></table>

## Which emulator should I use?

<table><thead><tr><th width="158.25">Emulator</th><th>Strengths</th><th>Limitations</th></tr></thead><tbody><tr><td><strong>arcadeduck</strong> (default)</td><td>Dedicated emulator based on DuckStation: very compatible, higher resolution, polygon correction (PGXP), 24-bit colors, save states, light guns and trackballs, cabinet outputs (lamps, recoil). Reads current MAME sets.</td><td>Partial or no save states on some boards (System 12 with link board, Konami GV, System 573, Twinkle).</td></tr><tr><td><strong>psxmame</strong></td><td>Old MAME version dedicated to these boards, light.</td><td>Old romset, different from current MAME. Cannot read <code>.7z</code> and <code>.chd</code> files.</td></tr><tr><td><strong>zinc</strong></td><td>Long-standing emulator, very light.</td><td>71 games only, old romset. 2 players. Cannot read <code>.7z</code> and <code>.chd</code> files.</td></tr><tr><td><strong>libretro: mame</strong></td><td>MAME inside RetroArch: save states, netplay, shaders.</td><td>Slower, less compatible than ArcadeDuck for these boards. Cannot read standalone <code>.chd</code> files.</td></tr><tr><td><strong>mame</strong></td><td>Same emulation as the mame core, as a standalone emulator.</td><td>Cannot read standalone <code>.chd</code> files.</td></tr></tbody></table>

## BIOS

Each board has its BIOS in MAME format. ArcadeDuck, the mame core and MAME use the same files:

<table><thead><tr><th width="272.75">Board</th><th>File</th></tr></thead><tbody><tr><td>Capcom ZN-1</td><td><code>coh1000c.zip</code></td></tr><tr><td>Capcom ZN-2</td><td><code>coh3002c.zip</code></td></tr><tr><td>Taito FX-1</td><td><code>coh1000t.zip</code></td></tr><tr><td>Tecmo TPS</td><td><code>coh1002m.zip</code></td></tr><tr><td>Atlus ZN-1</td><td><code>coh1001l.zip</code></td></tr><tr><td>Eighting / Raizing ZN-1</td><td><code>coh1002e.zip</code></td></tr><tr><td>Video System ZN-1</td><td><code>coh1002v.zip</code></td></tr><tr><td>Acclaim ZN-1</td><td><code>coh1000a.zip</code></td></tr><tr><td>Time Warner (Atari) ZN-1</td><td><code>coh1000w.zip</code></td></tr><tr><td>Taito G-Net</td><td><code>coh3002t.zip</code></td></tr><tr><td>Konami GV</td><td><code>konamigv.zip</code></td></tr><tr><td>Konami System 573</td><td><code>sys573.zip</code></td></tr></tbody></table>

Namco System 11 and System 12 games have no separate BIOS.

* **ArcadeDuck** looks for the BIOS next to the game, then in `bios`. When it is missing, RetroBat shows the expected file name.
* **mame core** and **MAME** look for it in `bios` and in the games folder.
* **PSXMame** uses its own BIOS, in its romset format, in `bios\psxmame\bios`.
* **Zinc** needs no BIOS.

## Which game format?

<table><thead><tr><th width="126.5">Format</th><th>Notes</th></tr></thead><tbody><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>MAME format games, to keep as they are, neither unzipped nor renamed (<code>sfex.zip</code>, <code>tekken3.zip</code>, <code>raystorm.zip</code>…). Clones need the parent game in the same folder. Zinc and PSXMame only read <code>.zip</code> files.</td></tr><tr><td><strong>.chd</strong></td><td>Discs of the games that have one (Konami System 573, Twinkle, Taito G-Net…), in a folder named after the game (see <a href="psxarcade.md#games-with-a-disc-chd"><strong>Guides</strong></a>). A standalone Taito G-Net <code>.chd</code> game starts directly with ArcadeDuck.</td></tr></tbody></table>

The romsets are not the same for every emulator:

* **ArcadeDuck**, **mame core** and **MAME**: current MAME romset.
* **PSXMame**: romset of its MAME version, older.
* **Zinc**: old romset and fixed game list (see [**Guides**](psxarcade.md#games-compatible-with-zinc)).

A game that works with one emulator does not necessarily work with another.

## Controls

### Automatic setup

RetroBat sets up the controllers for every emulator. Default button layout (ArcadeDuck, mame core, MAME):

<table><thead><tr><th width="232.75">Cabinet</th><th>Controller</th></tr></thead><tbody><tr><td>Joystick</td><td>D-pad, left stick</td></tr><tr><td>Buttons 1 to 4</td><td>WEST, SOUTH, EAST, NORTH</td></tr><tr><td>Buttons 5, 6</td><td>L1, R1</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Coin</td><td>SELECT</td></tr><tr><td>Test</td><td>R3</td></tr><tr><td>Service</td><td>L3</td></tr></tbody></table>

* **ArcadeDuck**: up to 4 players. The controls of each game come from the ArcadeDuck database (joysticks, light guns, trackballs, cabinet menu buttons). The button positions are set in `arcadeduck.yml` (for example Tekken 3: punches on WEST and NORTH, kicks on SOUTH and EAST, Tag on R1), and **CONTROLS > CONTROLLER LAYOUT** picks the layout (gamepad, 6 or 8 buttons). See the [**Arcade Guide**](../../arcade-guide.md#arcade-controls) page.
* **PSXMame**: buttons 1 to 4 on SOUTH, EAST, WEST, NORTH, buttons 5 and 6 on L1 and R1. **L3 + R3**: service. **SELECT + EAST**: pause. **CONTROLS > CONTROLLER PROFILE > GAME SPECIFIC** uses the game file in `emulators\psxmame\ctrlr` (`<game>.cfg`) when it exists. **ANALOG TO D-PAD** uses the left stick as a d-pad.
* **Zinc**: 2 players. **CONTROLS > CONTROLLER CONFIGURATION METHOD**: dynamic profile (default), pre-defined files from the `emulators\zinc\cfg` folder, or no configuration. **CONTROLS > CONTROL SCHEME** picks the dynamic profile: standard, Street Fighter, Soul Edge or Tekken. Zinc uses the left stick for movement: **CONTROLS > USE DPAD** switches to the d-pad.
* **mame core**, **MAME**: MAME per-game configuration, see the [**MAME controller mapping**](../../../controllers/specific_mapping/mame64-controller-mapping.md) page.

### Light guns

ArcadeDuck supports light guns and the mouse for the light gun games of these boards (**GUNS > ENABLE GUN**), with several guns. **GUNS > CROSSHAIR** shows or hides the crosshair, **SWITCH P1 AND P2 GUNS** swaps the players. **CONTROLS > EXTERNAL OUTPUTS** sends lamps and recoil to MameHooker or DemulShooter. For more details, see the [**Light gun controls**](../../../controllers/gun_controls.md) page.

### Hotkeys

#### **ArcadeDuck**, **mame core**, **MAME**

RetroBat default hotkeys (save, load, menu, screenshot…). For more details, see the [**Hotkeys**](../../../navigation/hotkeys.md) page.

#### **PSXMame**, **Zinc**

<table><thead><tr><th width="202.75">Hotkey</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quit</td></tr></tbody></table>

## Folders

| Content                               | Folder                                                                                |
| ------------------------------------- | ------------------------------------------------------------------------------------- |
| BIOS (ArcadeDuck, mame core, MAME)    | `bios` (or games folder)                                                              |
| BIOS (PSXMame)                        | `bios\psxmame\bios`                                                                   |
| ArcadeDuck: save states               | `saves\psxarcade\arcadeduck`                                                          |
| ArcadeDuck: screenshots               | `screenshots\arcadeduck`                                                              |
| ArcadeDuck: configuration             | `emulators\arcadeduck\settings.ini`                                                   |
| ArcadeDuck: button positions          | `system\resources\inputmapping\arcadeduck.yml` (editable copy in `user\inputmapping`) |
| mame core: save states                | `saves\psxarcade\libretro.mame`                                                       |
| PSXMame: saves (NVRAM, states)        | `saves\psxmame\nvram`, `saves\psxmame\states`                                         |
| PSXMame: per-game controller profiles | `emulators\psxmame\ctrlr`                                                             |
| Zinc: per-game controller profiles    | `emulators\zinc\cfg`                                                                  |

## Guides

### Games with a disc (CHD)

Some games have a disc on top of their `.zip` (Konami System 573 and Twinkle CDs, Taito G-Net memory cards…). Place the `.chd` in a folder named after the game, as for MAME:

```
roms\
└─ psxarcade\
   ├─ <game>\
   │  └─ <disc>.chd
   └─ <game>.zip
```

If the `.chd` shows up in the game list, launching it starts the game it belongs to with ArcadeDuck.

### Test menu

In game, **R3** (Test) opens the cabinet test menu (credits, difficulty, controls) and **L3** (Service) adds a service credit, with ArcadeDuck, the mame core and MAME. On the keyboard: `0` (Test) and `9` (Service) with ArcadeDuck.

### Games compatible with Zinc

Zinc only starts the games of this list, with this exact file name:

<details>

<summary>List of the 71 Zinc games</summary>

```
starglad sfex sfexj sfexa sfexp sfexpu1 sfexpj sfex2 sfex2j sfex2p
sfex2pj sfex2pa plsmaswd stargld2 rvschola jgakuen rvschool shiryu2 strider2 kikaioh
techromn ts2 ts2j tgmj sncwgltd beastrzb beastrzr bldyror2 brvblade psyforcj
psyforce psyfrcex mgcldtex raystorj raystorm ftimpcta gdarius gdarius2 danceyes xevi3dg
starswep myangel3 tekkenb tekkena tekken tekken2a tekken2b tekken2 souledga souledgb
souledge dunkmnia dunkmnic primglex weddingr hyperath pbball96 susume fgtlayer ehrgeiz
tekken3 mrdrillr aquarush pacapp glpracr3 shngmtkb cbaj doapp tondemo mfjump
hvnsgate
```

</details>

### Other useful options (ArcadeDuck)

<table><thead><tr><th width="336.5">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>INTERNAL RESOLUTION</strong></td><td>From 1x (native) to 9x (4K).</td></tr><tr><td><strong>GAME ASPECT RATIO</strong></td><td>Native, 4/3, 16/9, square pixels or stretched.</td></tr><tr><td><strong>VISUAL RENDERING > TEXTURE CORRECTION (PGXP)</strong></td><td>Reduces wobbly polygons and texture warping.</td></tr><tr><td><strong>VISUAL RENDERING > TRUE COLORS (24 BITS)</strong></td><td>24-bit rendering, without dithering.</td></tr><tr><td><strong>VISUAL RENDERING > OUTPUT SCALING</strong></td><td>Nearest, bilinear, integer, AMD FSR, NVIDIA NIS.</td></tr><tr><td><strong>VIDEO > DISABLE FULLSCREEN</strong></td><td>Use it if ArcadeDuck is not displayed on the right screen.</td></tr></tbody></table>

## Known issues

<table><thead><tr><th width="307.75">Issue</th><th>Solution</th></tr></thead><tbody><tr><td>ArcadeDuck reports a missing BIOS</td><td>Place the listed BIOS (for example <code>coh1000c.zip</code>) next to the game or in <code>bios</code>.</td></tr><tr><td>ArcadeDuck reports "not a set supported by ArcadeDuck"</td><td>The set name or version does not match: use the current MAME set, without renaming it.</td></tr><tr><td>ArcadeDuck reports "Missing CHD"</td><td>Place the <code>.chd</code> in the folder named after the game (see <a href="psxarcade.md#games-with-a-disc-chd"><strong>Guides</strong></a>).</td></tr><tr><td>Zinc reports "Game name not known"</td><td>The game is not in the Zinc list, or its file name is different (see <a href="psxarcade.md#games-compatible-with-zinc"><strong>Guides</strong></a>).</td></tr><tr><td>A game only works with one emulator</td><td>The romsets differ (see <a href="psxarcade.md#which-game-format"><strong>Which game format?</strong></a>): use the romset of the chosen emulator.</td></tr><tr><td>The save state fails with ArcadeDuck</td><td>Some boards do not support save states yet (System 573, Twinkle, part of the Konami GV and System 12 games).</td></tr></tbody></table>

