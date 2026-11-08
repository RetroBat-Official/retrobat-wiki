# Retroachievements

RetroAchievements adds achievements (trophies) to retro games, like on modern consoles. To use it, create a free account on the [RetroAchievements](https://retroachievements.org) website.

## Compatible emulators

* **RetroArch:** most libretro cores.
* **Standalone emulators:** BizHawk, Dolphin, DuckStation, Flycast, Gopher64, PCSX2, PPSSPP and Snes9x.

You only log in once, in RetroBat: RetroBat sends your account to all these emulators automatically.

## Enabling RetroAchievements

1. Open the [**MAIN MENU**](../navigation/main-menu.md) > **GAME SETTINGS** > **RETROACHIEVEMENTS SETTINGS**.
2. Turn on **RETROACHIEVEMENTS**.
3. Enter your **USERNAME** and **PASSWORD** of the RetroAchievements website.

<div align="left"><figure><img src="../.gitbook/assets/image (399).png" alt=""><figcaption></figcaption></figure></div>

4. Go back: RetroBat connects to your account, then indexes your games. A message appears when it is finished.

{% hint style="info" %}
If the message **UNABLE TO ACTIVATE RETROACHIEVEMENTS** appears, check your username and password, and your Internet connection.
{% endhint %}

## Options

<table><thead><tr><th width="304">Option</th><th>Effect</th></tr></thead><tbody><tr><td><strong>HARDCORE MODE</strong></td><td>Disables save states, rewind and cheats. Achievements unlocked in this mode give more points.</td></tr><tr><td><strong>LEADERBOARDS</strong></td><td>Takes part in the score and time leaderboards of the games. Needs the hardcore mode.</td></tr><tr><td><strong>VERBOSE MODE</strong></td><td>Shows your progress in the game at launch, and more notifications.</td></tr><tr><td><strong>RICH PRESENCE</strong></td><td>Shows on your RetroAchievements profile what you are doing in the game.</td></tr><tr><td><strong>ENCORE MODE</strong></td><td>Achievements you already unlocked can be unlocked again.</td></tr><tr><td><strong>AUTOMATIC SCREENSHOT</strong></td><td>Takes a screenshot when you unlock an achievement.</td></tr><tr><td><strong>CHALLENGE INDICATORS</strong></td><td>Shows icons at the bottom right of the screen when an achievement can be unlocked.</td></tr><tr><td><strong>UNOFFICIAL ACHIEVEMENTS</strong></td><td>Also enables the achievements that are not official yet.</td></tr><tr><td><strong>UNLOCK SOUND</strong></td><td>Sound played when you unlock an achievement (RetroArch only). The sounds are the <code>.ogg</code> files of the <code>sounds\retroachievements</code> folder of RetroBat: you can add your own.</td></tr><tr><td><strong>SHOW RETROACHIEVEMENTS ENTRY IN MAIN MENU</strong></td><td>Shows the RETROACHIEVEMENTS entry in the main menu (on by default).</td></tr></tbody></table>

{% hint style="warning" %}
With **HARDCORE MODE**, loading a save state is impossible. Use the save system of the game.
{% endhint %}

## Game indexes

Indexing checks which of your games have achievements. These games then show a **trophy** icon in the game list.

* **INDEX NEW GAMES AT STARTUP** (on by default): new games are checked each time RetroBat starts.
* **INDEX GAMES**: checks your games now (useful after adding many games).

<div align="left"><figure><img src="../.gitbook/assets/image (400).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
To hide the trophy icon, disable **SHOW RETROACHIEVEMENTS ICON** in **MAIN MENU > USER INTERFACE SETTINGS**, **ICONS** group.
{% endhint %}

## Achievements of a game

1. In the game list, highlight the game and hold **SOUTH** to open the **GAME OPTIONS**.

<div align="left"><figure><img src="../.gitbook/assets/image (403).png" alt=""><figcaption></figcaption></figure></div>

2. Choose **VIEW THIS GAME'S ACHIEVEMENTS**.

<div align="left"><figure><img src="../.gitbook/assets/image (401).png" alt=""><figcaption></figcaption></figure></div>

## Your profile

Open the **MAIN MENU** > **RETROACHIEVEMENTS** to see your points, your rank and the progress of your last games. You can launch a game directly from this list.

<div align="left"><figure><img src="../.gitbook/assets/image (404).png" alt=""><figcaption></figcaption></figure></div>

## Common problems

<table><thead><tr><th width="296.5">Problem</th><th>Solution</th></tr></thead><tbody><tr><td>No achievement in a game</td><td>Check that the game shows the trophy icon, and that the selected emulator is compatible. Only the versions of games known by RetroAchievements work: translated, patched or modified games are usually not recognized.</td></tr><tr><td>The trophy icon does not appear</td><td>Run <strong>INDEX GAMES</strong>, then check the version of the game on the RetroAchievements website.</td></tr><tr><td>Save states do not load</td><td>The hardcore mode is on. Disable it, or use the save system of the game.</td></tr><tr><td>UNABLE TO ACTIVATE RETROACHIEVEMENTS</td><td>Wrong username or password, or no Internet connection.</td></tr></tbody></table>
