---
description: Configure the Game View and apply specific settings to a system
---

# View Options

The **VIEW OPTIONS** menu is opened by pressing **SELECT** in the [Game View](system-view-and-game-view.md#game-view).

<div align="left"><figure><img src="../.gitbook/assets/image (241).png" alt=""><figcaption></figcaption></figure></div>

Its settings only apply to the **system** (or collection) you are browsing.

## Navigation

<table><thead><tr><th width="237.75">Setting</th><th>Description</th></tr></thead><tbody><tr><td><strong>FILTER GAMES BY TEXT</strong></td><td>Only show the games whose name contains the text you type</td></tr><tr><td><strong>OTHER FILTERS</strong></td><td>Filter the list by favorites, genre, number of players, already played games, region, language, games with RetroAchievements, missing media, kid games, lightgun games…</td></tr><tr><td><strong>SELECT RANDOM GAME</strong></td><td>Go to a random game of the list</td></tr><tr><td><strong>JUMP TO GAME BEGINNING WITH THE LETTER</strong></td><td>Go directly to the games starting with a letter</td></tr><tr><td><strong>SORT GAMES BY</strong></td><td>Sort the list by name, rating, times played, last played, number of players, release date, genre, developer, publisher, game time… (ascending or descending)</td></tr></tbody></table>

{% hint style="info" %}
Filters are kept until you reset them. If some games seem to be missing from a system, check that no filter is active.
{% endhint %}

### In a collection

When you browse a collection, an additional group is displayed:

* In a **dynamic collection**: **EDIT DYNAMIC COLLECTION FILTERS** lets you change the criteria of the collection.
* In an **editable collection**: **DELETE COLLECTION**.
* In other systems: **CREATE NEW DYNAMIC COLLECTION** creates a collection from the filters currently applied.

See [Game Collections](game-collections.md).

## View options

<table><thead><tr><th width="230.25">Setting</th><th>Description</th></tr></thead><tbody><tr><td><strong>GAMELIST VIEW STYLE</strong></td><td>Display of the game list for this system (list, detailed, grid…). <strong>AUTOMATIC</strong> uses the style defined in the theme configuration. Only shown when the theme offers several styles.</td></tr><tr><td><strong>VIEW CUSTOMIZATION</strong></td><td>Customize the display of this system, see below</td></tr></tbody></table>

### View customization

<table><thead><tr><th width="170.25">Section</th><th>Settings</th></tr></thead><tbody><tr><td>Gamelist style</td><td>Gamelist view style, default grid size</td></tr><tr><td>Theme options</td><td>Options offered by the theme for the game lists (layout, colors…)</td></tr><tr><td>Gamelist options</td><td>Show favorites on top, hidden files, folders, <code>..</code> parent folder, icons (region flag, save state, manual, RetroAchievements, gun, wheel…), file names instead of game names, <strong>FILE EXTENSIONS</strong> (hide some file types for this system)</td></tr><tr><td>Tools</td><td><strong>RESET CUSTOMIZATIONS</strong>: go back to the global settings</td></tr></tbody></table>

{% hint style="info" %}
These settings override, for this system only, the ones defined in **MAIN MENU** > **USER INTERFACE SETTINGS**.
{% endhint %}

## Options

<table><thead><tr><th width="227.75">Setting</th><th>Description</th></tr></thead><tbody><tr><td><strong>VIEW PAD TO KEYBOARD INFORMATION</strong></td><td>Show the controller-to-keyboard mapping used for this system or game (only shown when a <a href="../controllers/pad2key.md">PadToKey</a> profile exists)</td></tr><tr><td><strong>ADVANCED SYSTEM OPTIONS</strong></td><td>Emulator and emulation settings for this system, see below</td></tr></tbody></table>

### Advanced system options

<div align="left"><figure><img src="../.gitbook/assets/image (242).png" alt=""><figcaption></figcaption></figure></div>

1. **EMULATOR**: choose the emulator and the core used for this system. **AUTO** uses the default emulator chosen by RetroBat. See [Running a game](../get-started/running-a-game.md).
2. **General settings**: the settings shared by most emulators (shader set, decorations, aspect ratio, video mode, controller autoconfiguration…).
3. **Emulator settings**: the settings specific to the selected emulator or core, which RetroBat writes to the emulator configuration when a game is launched.

{% hint style="info" %}
* The available settings depend on the selected emulator: change the emulator first, then the menu shows the matching settings.
* **AUTO** means that the setting defined in **MAIN MENU** > **GAME SETTINGS** is used.
* To change a setting for one game only, use the [Game options](game-options.md) > **ADVANCED GAME OPTIONS**: game settings override system settings, which override global settings.
{% endhint %}

{% hint style="warning" %}
The **VIEW OPTIONS** group is only displayed in **Full** user interface mode. **ADVANCED SYSTEM OPTIONS** is only displayed for systems that have settings or several emulators.
{% endhint %}
