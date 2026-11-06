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

* RetroBat provides ready-made profiles for some systems (Amiga, Apple II, Atari ST, FM Towns…).
* You can create or modify a profile from EmulationStation:
  * for a whole system: in the advanced options of the system, **CREATE PADTOKEY PROFILE** (or **EDIT PADTOKEY PROFILE** if one exists);
  * for one game: in the [Game Options](../../navigation/game-options.md), **CREATE PADTOKEY PROFILE** / **EDIT PADTOKEY PROFILE**. The profile of a game is saved next to the game, in a `<game>.keys` file (`padto.keys` inside the folder for a game that is a folder).

In the **PAD TO KEYBOARD CONFIGURATION** screen, select a button of the controller and choose the keyboard key (or the mouse action) it must send.

{% hint style="info" %}
The PadToKey options appear only for the systems and emulators that support it.
{% endhint %}
