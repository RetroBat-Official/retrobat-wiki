# ⌨️ Keyboard

A standard keyboard is recognised out of the box, to navigate in RetroBat and to play.

## Navigating in RetroBat

The default keys are listed on the [Navigation](https://app.gitbook.com/s/exdzL60ZuqPLldz2AYta/navigation) page. To change them, go to **MAIN MENU > CONTROLLER SETTINGS > CONTROLLER MAPPING** and press a key of the keyboard to configure it like a controller.

## Playing with the keyboard

The keyboard configuration of RetroBat is also used in the games: RetroArch and most emulators get it automatically.

{% hint style="info" %}
For some standalone emulators, the keyboard is not configured automatically: configure the keys directly in the emulator itself.
{% endhint %}

## Computers: the keyboard focus

For computer systems (Amiga, Commodore 64, Amstrad CPC, MSX, Atari ST, ZX Spectrum, DOS…), the keyboard is the keyboard of the emulated computer: games often need many keys.

In RetroArch, some keys are also RetroArch shortcuts (F1 menu, Escape to quit, F2 / F4 save states…, see [Hotkeys](../../navigation/hotkeys.md)). To give the **whole keyboard** to the emulated computer, enable **KEYBOARD FOCUS** in the advanced options of the system (or of the game) > **CONTROLS**:

* the keyboard keys are all sent to the game, and the RetroArch keyboard shortcuts are disabled;
* press **Scroll Lock** to turn the focus off (to use the shortcuts again) and back on, while playing;
* the controller hotkeys still work (for example **HOTKEY + START** to quit).

This option is available for the RetroArch cores of computers, and for ScummVM and the Quake / Doom ports.

## Playing computer games with a controller (PadToKey)

Many computer games are played with the keyboard only. With [**PadToKey**](../pad2key.md), the buttons of your controller send keyboard keys, so you can play these games with a controller.

* RetroBat provides ready-made profiles for some systems (Amiga, Apple II, Atari ST, FM Towns…), in `system\padtokey`.
* You can create or modify a profile from EmulationStation:
  * for a whole system: in the advanced options of the system, **CREATE PADTOKEY PROFILE** (or **EDIT PADTOKEY PROFILE** if one exists). The profile is saved in `system\padtokey\<system>.keys`;
  * for one game: in the [Game Options](../../navigation/game-options.md), **CREATE PADTOKEY PROFILE** / **EDIT PADTOKEY PROFILE**. The profile is saved next to the game, in the `roms\<system>` folder: `<game>.keys` (for example `roms\amiga500\Turrican.keys`), or `padto.keys` inside the folder of a game that is a folder.

{% hint style="warning" %}
The `system\padtokey` folder is **overwritten by RetroBat updates**. To keep your system profiles, copy them to `user\padtokey`: RetroBat reads this folder first.
{% endhint %}

RetroBat uses the first profile found, in this order:

1. the profile of the game (`roms\<system>\<game>.keys`);
2. `user\padtokey\<system>.<core>.keys`, then `user\padtokey\<system>.keys`;
3. `emulationstation\.emulationstation\padtokey` (same names);
4. `system\padtokey` (same names).

The `<system>.<core>.keys` name is used for a profile that only applies to one core or emulator (for example `amiga500.puae.keys`).

{% hint style="info" %}
The PadToKey options appear only for the systems and emulators that support it.
{% endhint %}
