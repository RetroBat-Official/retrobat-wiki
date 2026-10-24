# Zelda Classic

<div align="left"><figure><img src="../../../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure></div>

Game engine - Released: 1999

{% embed url="https://zquestclassic.com" %}

Zelda Classic (now called ZQuest Classic) is a game engine that recreates the original _The Legend of Zelda_. Thousands of fan-made adventures, called **quests**, have been created with it. RetroBat plays these quests.

RetroBat does not ship any quest. Quests can be found on the community sites (for example [PureZC](https://www.purezc.net)).

## Information

| **Emulators**      | <ul><li>zquestclassic (default)</li><li>Libretro: zc255</li></ul> |
| ------------------ | ----------------------------------------------------------------- |
| **File folder**    | :open\_file\_folder: roms \ :open\_file\_folder: zeldaclassic     |
| **File extension** | .qst .zip .7z                                                     |

| Emulator      | Quests supported         | Savestates | Notes                                     |
| ------------- | ------------------------ | ---------- | ----------------------------------------- |
| zquestclassic | All versions, up to 2.55 | No         | Official ZQuest Classic player (zplayer). |
| zc255         | 2.55 and older           | Yes        | Libretro core (RetroArch).                |

If the emulator is not installed yet, RetroBat offers to download it when the first game is launched.

## Bios Information

No BIOS required. The engine data, the soundfont and the sound effects are included in both emulators.

## Adding quests

* Put the `.qst` file directly in `roms\zeldaclassic`, or keep it compressed in a `.zip` or `.7z` archive.
* One quest per archive: RetroBat starts the first `.qst` file found in the archive.
* **Enhanced music**: some quests come with music files. Keep them next to the `.qst` file, or in a folder named after the quest followed by `_music` (for `Adventure.qst`: `Adventure.qst_music`). Inside an archive, keep the same layout: RetroBat extracts the whole archive before starting the quest.

```
roms\zeldaclassic\
   Adventure.qst
   Adventure.qst_music\
   Other Quest.zip
```

## Controls

RetroBat configures the controller of **player 1** automatically. Zelda Classic is a single-player engine.

| RetroBat controller           | zquestclassic     | zc255 (libretro)               |
| ----------------------------- | ----------------- | ------------------------------ |
| D-PAD                         | Move              | Move                           |
| Left analog stick             | Move              | Move (see options)             |
| Bottom button (Xbox A / PS ✕) | A                 | A                              |
| Right button (Xbox B / PS ◯)  | B                 | B                              |
| Left button (Xbox X / PS ▢)   | EX1               | EX1                            |
| Top button (Xbox Y / PS △)    | EX2               | EX2                            |
| START                         | Start (subscreen) | Start (subscreen)              |
| SELECT                        | Map               | Map                            |
| L1                            | L                 | L                              |
| R1                            | R                 | R                              |
| L2                            | EX3               | -                              |
| R2                            | EX4               | Refill (only if cheats are on) |
| Guide / Home                  | Engine menu       | -                              |

A, B and the EX buttons are used by the quest itself: their action depends on the quest (sword, item, extra items...).

The **SWAP A/B AND X/Y** option swaps the face buttons, for example to get a Nintendo-like layout.

### Hotkeys

| Hotkey         | zquestclassic               | zc255 (libretro)                                         |
| -------------- | --------------------------- | -------------------------------------------------------- |
| HOTKEY + START | Quit and return to RetroBat | Quit and return to RetroBat                              |
| Other hotkeys  | -                           | Standard RetroArch hotkeys (savestates, rewind, menu...) |

With the **zquestclassic** emulator, the keyboard keeps the engine's own keys: arrows = move, `Z` = A, `X` = B, `Enter` = Start, `Space` = Map, `Q` / `W` = L / R, `A` `S` `D` `C` = EX1 to EX4, `Esc` = engine menu.

## Saves

Each quest has its own save, created by the quest itself (save points, continue screen...).

<table><thead><tr><th width="165.75">Emulator</th><th width="328.5">Save location</th><th>Save file named after</th></tr></thead><tbody><tr><td>zquestclassic</td><td><code>saves\zeldaclassic\zquestclassic\</code></td><td>the game file name (<code>Adventure.sav</code>)</td></tr><tr><td>zc255</td><td><code>saves\zeldaclassic\</code></td><td>the quest content (<code>zc255-&#x3C;number>.sav</code>)</td></tr></tbody></table>

{% hint style="warning" %}
The two emulators do not share their saves. Keep using the same emulator for a quest.

With **zquestclassic**, renaming the game file starts a new save. With **zc255**, renaming is safe, but a new version of the quest starts a new save.
{% endhint %}

## Options

The cheat options of the core (invulnerability, walk through walls, R2 refills) are not handled by RetroBat. They can be changed in the RetroArch menu, under **Core Options**.

## Specific system information

* **zquestclassic** is the recommended emulator: it is the official player and reads every quest version.
* **zc255** is useful to get savestates and RetroArch features (shaders, rewind...). A few quests do not support savestates.
