# Hotkeys

Hotkeys are controller or keyboard shortcuts used to perform actions while playing: saving or loading your progress (save states), pausing, rewinding, taking a screenshot… The most common one is **HOTKEY + START**, which quits the game and returns to RetroBat.

{% hint style="info" %}
**How to use a hotkey on a controller:** press and hold the **HOTKEY** button (the button you defined when configuring your controller, **SELECT** by default), then press the second button of the shortcut.

On the keyboard, shortcuts are single keys (no HOTKEY key needed).
{% endhint %}

## Default hotkeys

The RetroBat team has defined a common set of hotkeys, so that the same shortcuts work in as many emulators as possible.

Controller buttons are named by their position: **South** = B (Nintendo) / ✕ (PlayStation) / A (Xbox), **East** = A / ◯ / B, **West** = Y / ▢ / X, **North** = X / △ / Y.

| Action                                                                          | Controller                   | Keyboard       |
| ------------------------------------------------------------------------------- | ---------------------------- | -------------- |
| Quit the game                                                                   | HOTKEY + START               | `Esc`          |
| [Game Control Center](https://wiki.retrobat.org/navigation/game-control-center) | HOTKEY + East                | `Ctrl` + `F12` |
| Emulator menu (or pause if the emulator has no menu)                            | HOTKEY + South               | `F1`           |
| Save state                                                                      | HOTKEY + West                | `F2`           |
| Load state                                                                      | HOTKEY + North               | `F4`           |
| Previous save state slot                                                        | HOTKEY + D-pad down          | `F6`           |
| Next save state slot                                                            | HOTKEY + D-pad up            | `F7`           |
| Rewind                                                                          | HOTKEY + D-pad left          | `Backspace`    |
| Fast forward (hold)                                                             | HOTKEY + D-pad right         | `L`            |
| Fast forward (toggle)                                                           | (\*)                         | `Space`        |
| Screenshot                                                                      | HOTKEY + R3                  | `F8`           |
| Eject / insert disc                                                             | HOTKEY + L1                  |                |
| Previous disc                                                                   | HOTKEY + L2                  | `F9`           |
| Next disc                                                                       | HOTKEY + R2                  | `F10`          |
| AI translation service                                                          | HOTKEY + R1                  |                |
| Pause                                                                           | HOTKEY + L3 (RetroArch only) | `P`            |
| Toggle fullscreen                                                               |                              | `F`            |
| Frame advance                                                                   |                              | `K`            |
| Next / previous shader                                                          |                              | `M` / `N`      |
| Mute audio                                                                      |                              | `O`            |
| Capture / release the mouse                                                     |                              | `F11`          |
| Game focus (RetroArch, see below)                                               |                              | `Scroll Lock`  |

(\*) The **HOTKEY + D-pad right** fast forward can be switched from "hold" to "toggle" with the fast forward option in the system or game advanced settings.

<div align="left"><figure><img src="../.gitbook/assets/image (223).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Not all emulators support all these actions: each emulator only gets the actions it can handle.
{% endhint %}

### Emulators using the default hotkeys

<details>

<summary>Emulators with aligned hotkeys</summary>

Emulators marked with ✏️ can be customized (see Customizing hotkeys).

* RetroArch (all libretro cores) ✏️
* ArcadeDuck ✏️
* ares ✏️ (uses PadToKey)
* Azahar (fullscreen on `F1`)
* BigPEmu ✏️ (menu, fast forward, rewind, save/load state, screenshot only)
* BizHawk ✏️ (uses PadToKey)
* BlastEm ✏️ (uses PadToKey)
* CGenius ✏️ (save/load state only, uses PadToKey)
* Citron
* Demul
* DeSmuME ✏️ (uses PadToKey)
* Dhewm3
* Dolphin ✏️
* DuckStation ✏️
* Eden
* Flycast ✏️
* Hatari
* Jgenesis ✏️ (uses PadToKey)
* MAME
* Mednafen ✏️
* melonDS ✏️ (uses PadToKey)
* Mesen ✏️
* Model3-Vulkan ✏️ (uses PadToKey)
* Mupen64 (RMG)
* OpenMSX
* PCSX2 / PCSX2x6 ✏️
* PPSSPP ✏️
* Project64 ✏️ (uses PadToKey)
* Raine ✏️ (uses PadToKey)
* SM2-emu ✏️ (uses PadToKey)
* Snes9x ✏️ (uses PadToKey)
* Sudachi
* Suyu
* Ymir (quit with `Ctrl` + `Q`)
* Yuzu

</details>

{% hint style="info" %}
"Uses PadToKey" means that the emulator has no controller shortcuts of its own: RetroBat converts your controller hotkeys into the matching keyboard keys.
{% endhint %}

{% hint style="warning" %}
**An emulator supports hotkeys but does not follow this model?** Please report it to the RetroBat team on [Discord](https://discord.gg/GVcPNxwzuT) or the [forum](https://retrobat.forumgaming.fr/), so that it can be aligned in a future version.
{% endhint %}

## Computer systems and keyboard hotkeys

On computer systems (Amiga, Amstrad CPC, Atari ST, Commodore 64, MSX, ZX Spectrum, DOS, PC-98, X68000…), the emulated computer often needs the whole keyboard, including the function keys. Keyboard hotkeys may then conflict with the game, or may be disabled by the emulator.

* **Use your controller hotkeys** (HOTKEY + button) as much as possible: they do not use the keyboard.
* In **RetroArch**, press `Scroll Lock` to enable **Game Focus**: all keyboard keys are sent to the emulated computer, and keyboard hotkeys are disabled. Press `Scroll Lock` again to get them back.
* Some standalone emulators use modified shortcuts for these systems (for example `Alt` + key in OpenMSX).

## Customizing hotkeys

RetroBat lets you change the default hotkeys of several emulators, for the keyboard and for the controller, using two files provided in the `system\resources\inputmapping` folder of RetroBat:

* **kb\_hotkeys.yml**: keyboard hotkeys
* **controller\_hotkeys.yml**: controller hotkeys

<details>

<summary>Emulators with customizable hotkeys</summary>

ArcadeDuck, ares, BigPEmu, BizHawk, BlastEm, CGenius, DeSmuME, Dolphin, DuckStation, Flycast, Jgenesis, Mednafen, melonDS, Mesen, Model3-Vulkan, PCSX2, PPSSPP, Project64, Raine, RetroArch, SM2-emu, Snes9x.

</details>

{% hint style="warning" %}
**Never modify the files in `system\resources\inputmapping`**: they are replaced at each update. Copy them to the `user\inputmapping` folder of RetroBat and modify the copy.
{% endhint %}

### Which file is used?

You can create a file for all emulators, or a file for one emulator only, by adding the emulator name at the beginning of the file name (for example `pcsx2_controller_hotkeys.yml` or `retroarch_kb_hotkeys.yml`).

RetroBat uses the first file found, in this order:

1. `user\inputmapping\<emulator>_kb_hotkeys.yml` (or `_controller_hotkeys.yml`)
2. `system\resources\inputmapping\<emulator>_kb_hotkeys.yml`
3. `user\inputmapping\kb_hotkeys.yml`
4. `system\resources\inputmapping\kb_hotkeys.yml`

<details>

<summary>Emulator names to use in file names</summary>

`arcadeduck`, `ares`, `bigpemu`, `bizhawk`, `blastem`, `cgenius`, `desmume`, `dolphin`, `duckstation`, `flycast`, `jgenesis`, `mednafen`, `melonds`, `mesen`, `model3-vulkan`, `pcsx2`, `ppsspp`, `project64`, `raine`, `retroarch`, `sm2-emu`, `snes9x`

</details>

### File structure

The files are text files in YAML format: open them with any text editor (Notepad, Notepad++…). In the provided files, **all lines are commented** (they start with `#`): they only show the default values.

Lines are grouped in **containers**:

* The `default:` container applies to all games.
* A container named after a **core** (for example `fceumm:` or `flycast:`) only applies to this core. This is useful for emulators with several cores or systems: RetroArch, ares, BizHawk, BlastEm, Jgenesis, Mednafen, Mesen.
* For RetroArch controller hotkeys, a container can also be named after a **system** (for example `nes:`).

If no container matches the core or the system, the `default` container is used.

{% hint style="warning" %}
* Indentation matters: lines inside a container must start with **two spaces**, never with a tab.
* The action names are always the **RetroArch** names, even for other emulators: RetroBat converts them automatically.
{% endhint %}

### Remap controller hotkeys

In `controller_hotkeys.yml`, each line is written as `button: action`.

<table><thead><tr><th width="255.25">Button name</th><th>Button</th></tr></thead><tbody><tr><td><code>a</code></td><td>South</td></tr><tr><td><code>x</code></td><td>North</td></tr><tr><td><code>y</code></td><td>West</td></tr><tr><td><code>start</code></td><td>START</td></tr><tr><td><code>pageup</code> / <code>pagedown</code></td><td>L1 / R1</td></tr><tr><td><code>l2</code> / <code>r2</code></td><td>L2 / R2</td></tr><tr><td><code>l3</code> / <code>r3</code></td><td>Left / right stick click</td></tr><tr><td><code>up</code> / <code>down</code> / <code>left</code> / <code>right</code></td><td>D-pad</td></tr></tbody></table>

{% hint style="info" %}
The `b` (East) button cannot be used: HOTKEY + East is reserved for the Game Control Center.
{% endhint %}

| Action name                                   | Action                       |
| --------------------------------------------- | ---------------------------- |
| `exit_emulator`                               | Quit the game                |
| `menu_toggle`                                 | Emulator menu                |
| `pause_toggle`                                | Pause                        |
| `save_state` / `load_state`                   | Save / load state            |
| `state_slot_increase` / `state_slot_decrease` | Next / previous save slot    |
| `rewind`                                      | Rewind                       |
| `hold_fast_forward` / `toggle_fast_forward`   | Fast forward (hold / toggle) |
| `screenshot`                                  | Screenshot                   |
| `disk_eject_toggle`                           | Eject / insert disc          |
| `disk_prev` / `disk_next`                     | Previous / next disc         |
| `ai_service`                                  | AI translation service       |

**Example:** move **rewind** and **fast forward** to L1 and R1, and move **disc eject** and **AI service** to the D-pad.

1. Copy `controller_hotkeys.yml` from `system\resources\inputmapping` to `user\inputmapping`.
2. Open the copy, remove the `#` at the beginning of the `#default:` line and of all the lines of the default container below it.
3. Change the lines you want:

```yaml
default:
  start: exit_emulator
  a: menu_toggle
  x: load_state
  y: save_state
  pageup: rewind
  pagedown: hold_fast_forward
  l2: disk_prev
  r2: disk_next
  r3: screenshot
  up: state_slot_increase
  down: state_slot_decrease
  left: disk_eject_toggle
  right: ai_service
```

4. Save the file.

{% hint style="warning" %}
Always keep **all** the shortcuts you want to use in the container, not only the ones you change: for RetroArch, the container replaces the whole default list. For example, `start: exit_emulator` must stay in the list, otherwise HOTKEY + START will no longer quit the game.
{% endhint %}

**Example for one core only:** use toggle fast forward instead of hold with the Flycast core, and keep the default container for all other cores:

```yaml
default:
  start: exit_emulator
  a: menu_toggle
  x: load_state
  y: save_state
  pageup: disk_eject_toggle
  pagedown: ai_service
  l2: disk_prev
  r2: disk_next
  r3: screenshot
  up: state_slot_increase
  down: state_slot_decrease
  left: rewind
  right: hold_fast_forward

flycast:
  start: exit_emulator
  a: menu_toggle
  x: load_state
  y: save_state
  left: rewind
  right: toggle_fast_forward
```

{% hint style="info" %}
**RetroArch only — single-button shortcuts:** adding the `noHotkey: true` line in a container disables the HOTKEY button for the matching cores: each shortcut is then triggered by **its button alone** (for example START alone quits the game). Only use it for systems where these buttons are not used by the games.
{% endhint %}

### Remap keyboard hotkeys

In `kb_hotkeys.yml`, each line is written the other way round: `action: key`, and action names start with `input_`.

**Example:** save states on `F5` and load states on `F9`.

1. Copy `kb_hotkeys.yml` from `system\resources\inputmapping` to `user\inputmapping`.
2. Open the copy, remove the `#` at the beginning of the `#default:` line and of all the lines below it.
3. Change the lines you want:

```yaml
default:
  input_menu_toggle: f1
  input_toggle_fullscreen: f
  input_hold_fast_forward: l
  input_rewind: backspace
  input_toggle_fast_forward: space
  input_frame_advance: k
  input_screenshot: f8
  input_save_state: f5
  input_load_state: f9
  input_state_slot_decrease: f6
  input_state_slot_increase: f7
  input_pause_toggle: p
  input_exit_emulator: escape
  input_shader_next: m
  input_shader_prev: n
  input_disk_prev: f3
  input_disk_next: f10
  input_game_focus_toggle: scroll_lock
  input_grab_mouse_toggle: f11
  input_audio_mute: o
```

4. Save the file.

{% hint style="info" %}
* Key names follow the RetroArch naming: `a` to `z`, `f1` to `f12`, `escape`, `enter`, `space`, `backspace`, `tab`, `insert`, `del`, `home`, `end`, `pageup`, `pagedown`, `up`, `down`, `left`, `right`, `scroll_lock`…
* If a key is not supported by an emulator, its default key is used instead.
* For emulators that **use PadToKey**, controller hotkeys send the keyboard key: if you change a key in `kb_hotkeys.yml`, the matching controller hotkey follows automatically.
{% endhint %}
