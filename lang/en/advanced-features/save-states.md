# Save States

Save states take a snapshot of a game at any moment, so you can reload it later exactly at the same point.

{% hint style="danger" %}
Save states are not a safe way to keep your progress. They often stop working after an emulator update. Always use the save system of the game itself (memory card, save menu…) first.
{% endhint %}

## How it works

* RetroBat manages save states for **RetroArch cores** and for several standalone emulators (Dolphin, PCSX2, DuckStation, PPSSPP, Flycast…). For these emulators, you can launch a game directly from a save state from the game list.
* Save states are stored in `saves\<system>\<emulator>` (for RetroArch: `saves\<system>\libretro.<core>`), with a screenshot of the moment of the save.
* A game that has save states shows an icon in the game list.
* Save states are not shared between emulators: a state made with one emulator can only be loaded by this emulator.

## Saving and loading during a game

Use the standard RetroBat hotkeys:

| Action             | Controller          | Keyboard |
| ------------------ | ------------------- | -------- |
| Save state         | HOTKEY + WEST       | F2       |
| Load state         | HOTKEY + NORTH      | F4       |
| Previous save slot | HOTKEY + D-pad down | F6       |
| Next save slot     | HOTKEY + D-pad up   | F7       |

{% hint style="info" %}
If you customized your hotkeys, use your own combinations. See the Hotkeys page.
{% endhint %}

## Launching a game from a save state

1. In the game list, highlight the game.
2. Press **NORTH** (or **L3**) to open the **SAVESTATE MANAGER**. You can also hold **SOUTH** to open the **GAME OPTIONS**, then choose **SAVE STATES**.
3. Choose a save state, then press **SOUTH** (**LAUNCH**).

<div align="left"><figure><img src="../.gitbook/assets/image (397).png" alt=""><figcaption></figcaption></figure></div>

The manager shows:

<table><thead><tr><th width="254">Item</th><th>Use</th></tr></thead><tbody><tr><td><strong>START NEW GAME</strong></td><td>Starts the game from the beginning, without loading any save state.</td></tr><tr><td><strong>START NEW AUTO SAVE</strong></td><td>Shown when AUTO SAVE/LOAD is on and there is no auto save yet: starts the game and creates an auto save when you quit.</td></tr><tr><td><strong>AUTO SAVE</strong></td><td>The state saved automatically when you last quit the game.</td></tr><tr><td>Save states</td><td>Your save states, with their date (and their slot number when incremental save states are disabled).</td></tr></tbody></table>

In the manager:

* **SOUTH**: launch the game from the selected state.
* **WEST**: delete the selected state.
* **NORTH**: copy the selected state to a free slot.
* **EAST**: go back.

{% hint style="info" %}
- A save state made with another emulator shows the name of this emulator. When you launch it, RetroBat uses this emulator automatically.
- If you enabled **ACCESS GAME OPTIONS WITH NORTH BUTTON**, the buttons are swapped: **NORTH** opens the game options, and holding **SOUTH** opens the save states.
{% endhint %}

## Options

The options are in **MAIN MENU > GAME SETTINGS**, **SAVESTATES** group.

<div align="left"><figure><img src="../.gitbook/assets/image (398).png" alt=""><figcaption></figcaption></figure></div>

### AUTO SAVE/LOAD

When it is on:

* when you quit a game, its state is saved automatically (**AUTO SAVE**);
* when you launch it again, the game resumes exactly where you stopped.

To start from the beginning instead, open the save state manager and choose **START NEW GAME**.

This option can also be set for one system only: **MAIN MENU > GAME SETTINGS > PER SYSTEM ADVANCED CONFIGURATION > (system) > AUTO SAVE/LOAD ON GAME LAUNCH** (AUTO, ON or OFF). It only appears when the emulator of the system supports it.

### INCREMENTAL SAVESTATES

Decides when a save state can overwrite an older one:

<table><thead><tr><th width="289">Choice</th><th>Behavior</th></tr></thead><tbody><tr><td><strong>INCREMENT PER SAVE</strong> (default)</td><td>Each save creates a new save state: the older ones are never overwritten.</td></tr><tr><td><strong>INCREMENT SLOT</strong></td><td>During a game, saving overwrites the current slot, but each new game starts on a free slot.</td></tr><tr><td><strong>DO NOT INCREMENT</strong></td><td>The game uses the current slot: a new save can overwrite an older one, as in the emulator alone.</td></tr></tbody></table>

### SHOW SAVESTATE MANAGER

Opens the save state manager when you launch a game with **SOUTH**:

* **NO** (default): the game starts directly.
* **ALWAYS**: the manager opens for every game that supports save states.
* **IF NOT EMPTY**: the manager only opens when the game already has save states.

### Save state icon

To hide the icon of games with save states, disable **SHOW SAVESTATE ICON** in **MAIN MENU > USER INTERFACE SETTINGS**, **ICONS** group.

## Good to know

* **RetroAchievements:** in hardcore mode, loading a save state is disabled.
* **Emulator updates:** after an update, an old save state may no longer load. Keep a normal save of the game.
* **Emulators not managed by RetroBat:** other emulators may have their own save states, from their own menu. They do not appear in the save state manager.
