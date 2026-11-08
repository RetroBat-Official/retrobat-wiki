# Kiosk and Kid mode

RetroBat (EmulationStation) has three **user interface modes**:

<table><thead><tr><th width="88.25">Mode</th><th width="213.75">For</th><th>What it does</th></tr></thead><tbody><tr><td><strong>Full</strong></td><td>You (default)</td><td>Everything is available.</td></tr><tr><td><strong>Kiosk</strong></td><td>Guests, arcade cabinets</td><td>All games can be played, but settings, metadata, collections and game deletion are locked. Hidden games stay hidden.</td></tr><tr><td><strong>Kid</strong></td><td>Children</td><td>Same locks as Kiosk, and <strong>only the games marked as "Kidgame"</strong> are shown. Favorites can't be changed.</td></tr></tbody></table>

## Before switching to Kid mode: mark the kid games

Kid mode only shows the games whose **Kidgame** metadata is on. Do this while you are still in **Full** mode:

1. In a game list, select the game and open the [**GAME OPTIONS**](../navigation/game-options.md) menu.
2. Select **EDIT THIS GAME'S METADATA**.
3. Switch **Kidgame** on, then save.

<div align="left"><figure><img src="../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure></div>

> **Tip:** You can also add `<kidgame>true</kidgame>` to the games in the system's `gamelist.xml` (with EmulationStation closed).

If no game is marked, Kid mode has nothing to show, and EmulationStation switches back to **Full** mode automatically.

## Switching to Kiosk or Kid mode

1. Open the **MAIN MENU** (START) > **SYSTEM SETTINGS**.

<div align="left"><figure><img src="../.gitbook/assets/image (377).png" alt=""><figcaption></figcaption></figure></div>

2. Set **USER INTERFACE MODE** to **Kiosk** or **Kid**.

<div align="left"><figure><img src="../.gitbook/assets/image (378).png" alt=""><figcaption></figcaption></figure></div>

3. Close the menu. A message shows the **unlock code**. Write it down, then confirm with **YES**.

<div align="left"><figure><img src="../.gitbook/assets/image (380).png" alt=""><figcaption></figcaption></figure></div>

## What is locked

<table><thead><tr><th width="493.25"></th><th align="center">Kiosk</th><th align="center">Kid</th></tr></thead><tbody><tr><td>Main menu reduced to RETROACHIEVEMENTS, INFORMATION, UNLOCK USER INTERFACE MODE and QUIT</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Game options: no metadata editing, no collections, no game deletion</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Game list filters and options reduced</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Empty systems and collections hidden</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>PadToKey editor read-only</td><td align="center">✔</td><td align="center">✔</td></tr><tr><td>Hidden games never shown</td><td align="center">✔</td><td align="center"></td></tr><tr><td>Only "Kidgame" games shown</td><td align="center"></td><td align="center">✔</td></tr><tr><td>SELECT options and the favorites shortcut disabled</td><td align="center"></td><td align="center">✔</td></tr><tr><td>"MENU" prompt hidden (START still opens the reduced menu)</td><td align="center"></td><td align="center">✔</td></tr></tbody></table>

Save states stay available in both modes.

<div align="left"><figure><img src="../.gitbook/assets/image (381).png" alt=""><figcaption></figcaption></figure></div>

## Going back to Full mode

1. Open the **MAIN MENU** (START) > **UNLOCK USER INTERFACE MODE**.
2. When **ENTER THE CODE NOW TO UNLOCK** is shown, press the code buttons one after the other.

<div align="left"><figure><img src="../.gitbook/assets/image (382).png" alt=""><figcaption></figcaption></figure></div>

The default code is **A, A, A, B, A**. The letters mean **button positions**, not printed labels:

| Code | Position      | Xbox | PlayStation | Nintendo |
| ---- | ------------- | ---- | ----------- | -------- |
| A    | bottom button | A    | ✕           | B        |
| B    | right button  | B    | ○           | A        |

So the code is **A A A B A** on an Xbox pad, **✕ ✕ ✕ ○ ✕** on a PlayStation pad and **B B B A B** on a Nintendo pad.

## Changing the unlock code (advanced)

1. Close EmulationStation.
2. Open `emulationstation\.emulationstation\es_settings.cfg`.
3. Add this line before `</config>` (it is not in the file while the default code is used):

```xml
<string name="UIMode_passkey" value="aaaba" />
```

4. Replace `aaaba` with your sequence, using `a` (bottom button) and `b` (right button), then restart RetroBat.

> **Note:** If you press a wrong button while typing the code, start the sequence again from the beginning.

## Forcing the mode with retrobat.ini

To lock a cabinet or a kids' setup for good, set the mode in `retrobat.ini` (RetroBat root folder), section `[EmulationStation]`:

```ini
[EmulationStation]
InterfaceMode=2
```

<table><thead><tr><th width="187.75">Value</th><th>Mode</th></tr></thead><tbody><tr><td>0</td><td>Normal (uses the USER INTERFACE MODE setting)</td></tr><tr><td>1</td><td>Kiosk</td></tr><tr><td>2</td><td>Kid</td></tr></tbody></table>

> **Warning:** When `InterfaceMode` is 1 or 2, the mode is **forced at every start**, and the unlock code has no effect. To get Full mode back, close RetroBat and set `InterfaceMode=0`.
