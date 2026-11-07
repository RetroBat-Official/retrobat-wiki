# PadToKey

With **PadToKey**, the buttons of your controller send **keyboard keys** (or mouse actions) to the game. Use it for games that cannot be played with a controller: old computer games, Windows games, some standalone emulators or ports.

A PadToKey profile can be made for a **whole system** or for **one game**, for up to 4 players. While the game runs, RetroBat sends the keys to the emulator window.

{% hint style="info" %}
The PadToKey options appear only for the systems and emulators that support it (computers, DOS, Windows games, pinball, ports, some standalone emulators…). They can be edited only when the interface is in **FULL** mode.
{% endhint %}

## Creating or editing a profile

### For a system

1. In the game list of the system, press **SELECT** to open the [View Options](../navigation/view-options.md).
2. Select **ADVANCED SYSTEM OPTIONS**.
3. Select **CREATE PADTOKEY PROFILE** (or **EDIT PADTOKEY PROFILE** if the system already has one).

### For a game

1. In the game list, hold **SOUTH** on the game to open the [Game Options](../navigation/game-options.md).
2. Select **CREATE PADTOKEY PROFILE** (or **EDIT PADTOKEY PROFILE**).

A new game profile starts from the profile of the system, if there is one: you only change the keys this game needs.

### The editor

The **PAD TO KEYBOARD CONFIGURATION** window lists the buttons of the controller, with a tab per player (**PLAYER 1** to **PLAYER 4**).

<div align="left"><figure><img src="../.gitbook/assets/image (347).png" alt=""><figcaption></figcaption></figure></div>

* Select a button and press **SOUTH** ![](<../.gitbook/assets/image (348).png>) : a virtual keyboard opens.
  * Move to a key and press **SOUTH** ![](<../.gitbook/assets/image (349).png>) to assign it.
  * To send several keys at once (e.g. **Shift + F1**), press **NORTH** (**ADD COMBINATION KEY**) on each extra key, then **SOUTH** ![](<../.gitbook/assets/image (350).png>) on the last one.
  * Press **WEST** (**RESET**) to remove the key of the button.
  * The mouse buttons are on the right of the virtual keyboard.
* **COMBINATIONS**: assign keys to **HOTKEY + START**, **HOTKEY + SOUTH**, **HOTKEY + EAST**, **HOTKEY + NORTH** or **HOTKEY + WEST**.
* **MOUSE CURSOR** > **EMULATE MOUSE CURSOR**: moves the mouse pointer with the **LEFT ANALOG STICK** or the **RIGHT ANALOG STICK**.
* On a button: **NORTH** deletes its mapping, **WEST** edits its description (a reminder of the action in the game, e.g. "Fire").
* **SAVE** (or **START**) saves the profile, **DELETE** deletes the whole profile.

<div align="left"><figure><img src="../.gitbook/assets/image (351).png" alt=""><figcaption></figcaption></figure></div>

## Where the profiles are saved

<table><thead><tr><th width="154">Profile</th><th>File</th></tr></thead><tbody><tr><td>Game</td><td>Next to the game: <code>roms\&#x3C;system>\&#x3C;game>.keys</code> (e.g. <code>roms\amiga500\Turrican.keys</code>). For a game that is a folder: <code>padto.keys</code> inside the folder</td></tr><tr><td>System</td><td><code>system\padtokey\&#x3C;system>.keys</code></td></tr></tbody></table>

{% hint style="warning" %}
The `system\padtokey` folder is overwritten by RetroBat updates. To keep a system profile, copy it to `user\padtokey`: this folder is read first and is never overwritten.
{% endhint %}

### Which profile is used

At launch, RetroBat uses the **first profile found**, in this order:

1. The profile of the game (`<game>.keys` or `padto.keys`).
2. `user\padtokey\<system>.<core>.keys`, then `user\padtokey\<system>.keys`.
3. `emulationstation\.emulationstation\padtokey` (same names).
4. `system\padtokey` (same names).

A `<system>.<core>.keys` profile applies only when the game runs with this core or emulator (e.g. `amiga500.puae.keys` for the puae core only). It cannot be created from EmulationStation: copy a `<system>.keys` file and rename it.

RetroBat provides ready-made profiles in `system\padtokey` for some systems (Amiga, Apple II, Atari ST, FM Towns, X68000, Sam Coupé…).

## Profiles from ScreenScraper

ScreenScraper provides PadToKey profiles for some games. To get them, enable **MAIN MENU > SCRAPER > PADTOKEY SETTINGS** before scraping.

The profile is saved next to the game as `<game>.p2k.cfg` (or `.p2k.cfg` inside the folder of a game that is a folder) and is used automatically. If you edit it in EmulationStation, your changes are saved in a `.keys` file, which is then used instead of the ScreenScraper profile.

## The .keys file

A `.keys` file is a text file (JSON). You can edit it with a text editor, for example to make a `<system>.<core>.keys` profile.

```json
{
    "actions_player1": [
        { "trigger": "a", "type": "key", "target": "KEY_SPACE", "description": "Jump" },
        { "trigger": "b", "type": "key", "target": "KEY_LEFTCTRL", "description": "Fire" },
        { "trigger": "start", "type": "key", "target": "KEY_ENTER" },
        { "trigger": ["hotkey", "a"], "type": "key", "target": ["KEY_LEFTSHIFT", "KEY_F1"] },
        { "trigger": "joystick2", "type": "mouse" },
        { "trigger": "r3", "type": "key", "target": "BTN_LEFT" }
    ],
    "actions_player2": [
        { "trigger": "a", "type": "key", "target": "KEY_RIGHTCTRL" }
    ]
}
```

* `actions_player1` to `actions_player4`: the actions of the controller of each player.
* `trigger`: the controller button, or a list of buttons pressed together (e.g. `["hotkey", "a"]`).
* `type`: `key` to send keys, `mouse` to move the mouse pointer with a stick.
* `target`: the key, or a list of keys sent together.
* `description` (optional): text shown in the editor.

| Trigger                                                           | Controller button                      |
| ----------------------------------------------------------------- | -------------------------------------- |
| `up`, `down`, `left`, `right`                                     | D-pad                                  |
| `a`, `b`, `x`, `y`                                                | SOUTH, EAST, NORTH, WEST               |
| `start`, `select`, `hotkey`                                       | START, SELECT, HOTKEY                  |
| `pageup`, `pagedown`                                              | LEFT SHOULDER, RIGHT SHOULDER (L1, R1) |
| `l2`, `r2`                                                        | LEFT TRIGGER, RIGHT TRIGGER            |
| `l3`, `r3`                                                        | LEFT STICK PRESS, RIGHT STICK PRESS    |
| `joystick1up`, `joystick1down`, `joystick1left`, `joystick1right` | Left analog stick                      |
| `joystick2up`, `joystick2down`, `joystick2left`, `joystick2right` | Right analog stick                     |
| `joystick1`, `joystick2` (with `"type": "mouse"`)                 | Stick that moves the mouse pointer     |

**Targets**:

* Keys: `KEY_A` to `KEY_Z`, `KEY_0` to `KEY_9`, `KEY_F1` to `KEY_F12`, `KEY_ENTER`, `KEY_ESC`, `KEY_SPACE`, `KEY_TAB`, `KEY_BACKSPACE`, `KEY_UP`, `KEY_DOWN`, `KEY_LEFT`, `KEY_RIGHT`, `KEY_LEFTSHIFT`, `KEY_LEFTCTRL`, `KEY_LEFTALT`, `KEY_KP0` to `KEY_KP9` (numeric keypad)…
* Mouse buttons: `BTN_LEFT`, `BTN_RIGHT`, `BTN_MIDDLE`.
* Special actions (Windows games, ports): `(%{CLOSE})` closes the game window, `(%{KILL})` kills the game process, `(%{F4})` sends Alt + F4.

{% hint style="warning" %}
- The key names are the names of the keys of a **QWERTY** keyboard, by position: on an AZERTY keyboard, `KEY_Q` is the **A** key and `KEY_A` is the **Q** key.
- The special actions can only be written by hand: if you open and save the profile in EmulationStation, they are removed.
{% endhint %}

## Troubleshooting

* The keys are sent only to the window of the emulator or game launched by RetroBat, when it is in the foreground.
* If **JoyToKey** is running, PadToKey is disabled.
* RetroBat already uses PadToKey for the shortcuts of some standalone emulators (e.g. **HOTKEY + START** to quit). A button of your profile replaces the RetroBat shortcut on the same button.
* `emulationstation\emulatorLauncher.log` shows the profile used (line `[PadToKey] Using mapping file`) and each key sent (lines `[SendKey]`).
