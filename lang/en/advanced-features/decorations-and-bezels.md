# Decorations (bezels)

Most TVs and computer screens were 4:3 until the end of the 90s. On a 16:9 screen, the games of that time are displayed with black bars on both sides. RetroBat can fill this space with **decorations** (bezels).

<div align="left"><figure><img src="../.gitbook/assets/image (362).png" alt=""><figcaption></figcaption></figure></div>

RetroBat offers:

* **Decoration sets**, provided with RetroBat, with a bezel per system.
* **The Bezel Project**, a bezel per game for many systems, to download.
* **Mega Bezels**, shader packs for RetroArch that draw the bezel with effects (reflections, glow…).
* **Tattoos**, an image of the controls displayed over the bezel.

{% hint style="info" %}
Decorations are made for wide screens (16:10, 16:9 and wider). On a 4:3 or 5:4 screen, no decoration is displayed.
{% endhint %}

## Choosing the decorations

The **DECORATIONS** option can be set:

* for all games: **MAIN MENU > GAME SETTINGS > DECORATIONS**;

<div align="left"><figure><img src="../.gitbook/assets/image (352).png" alt=""><figcaption></figcaption></figure></div>

* for a system: [View Options](../navigation/view-options.md) > **ADVANCED SYSTEM OPTIONS > DECORATIONS**;

<div align="left"><figure><img src="../.gitbook/assets/image (353).png" alt=""><figcaption></figcaption></figure></div>

* for a game: [Game Options](../navigation/game-options.md) > **ADVANCED GAME OPTIONS > DECORATIONS**.

<div align="left"><figure><img src="../.gitbook/assets/image (354).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="402.75">Choice</th><th>Result</th></tr></thead><tbody><tr><td><strong>AUTO</strong> (default)</td><td>The bezel of the game, if there is one (scraped or downloaded with The Bezel Project), otherwise the bezel of the system from <strong>DEFAULT UNGLAZED</strong></td></tr><tr><td><strong>NONE</strong></td><td>No decoration</td></tr><tr><td><strong>DEFAULT UNGLAZED</strong></td><td>Bezel of the system (default style of RetroBat)</td></tr><tr><td><strong>DEFAULT CURVE</strong>, <strong>DEFAULT CURVE NIGHT</strong>, <strong>DEFAULT NOCURVE</strong>, <strong>DEFAULT NOCURVE NIGHT</strong></td><td>Bezel of the system, with a curved or flat screen, in day or night lighting</td></tr><tr><td><strong>AMBIANCE BROADCAST</strong>, <strong>AMBIANCE GAMEROOM</strong>, <strong>AMBIANCE MONITOR 1084S</strong>, <strong>AMBIANCE NIGHT</strong>, <strong>AMBIANCE VINTAGE TV</strong></td><td>The game in a room or in an old TV / monitor</td></tr><tr><td><strong>ARCADE 1980S</strong>, <strong>ARCADE 1980S VERTICAL</strong>, <strong>ARCADE VERTICAL DEFAULT</strong></td><td>Arcade cabinet look (horizontal or vertical games)</td></tr><tr><td><strong>ANIMATED</strong></td><td>Animated bezels for RetroArch: the buttons of the drawn controller light up when you press them (Dreamcast, Game Boy Advance, Mega Drive, NES, PlayStation, Saturn, Super Nintendo)</td></tr><tr><td><strong>THEBEZELPROJECT</strong></td><td>Bezels of The Bezel Project (once downloaded, see below)</td></tr></tbody></table>

A preview of each set is displayed in the list.

<div align="left"><figure><img src="../.gitbook/assets/image (364).png" alt=""><figcaption></figcaption></figure></div>

* **Vertical arcade games** (MAME, FBNeo): with the default sets, RetroBat automatically uses a vertical bezel.
* **Standalone emulators**: the bezel is displayed with ReShade or with a window behind the emulator, depending on the emulator. The **MAIN MENU > GAME SETTINGS > RESHADE** option sets how ReShade is used: **DISABLED** (the bezel is displayed with a window instead), **USE MY OWN** (RetroBat never installs, changes or deletes ReShade files in the emulator folders).
* The DECORATIONS option appears only for the emulators that can display bezels.

## Bezels per game

### The Bezel Project

The Bezel Project provides a bezel for each game of many systems.

1. Open **MAIN MENU > UPDATES & DOWNLOADS > THE BEZEL PROJECT**.

<div align="left"><figure><img src="../.gitbook/assets/image (355).png" alt=""><figcaption></figcaption></figure></div>

2. Select the system and confirm the installation.

<div align="left"><figure><img src="../.gitbook/assets/image (356).png" alt=""><figcaption></figcaption></figure></div>

3. Wait for the end of the download.

<div align="left"><figure><img src="../.gitbook/assets/image (357).png" alt=""><figcaption></figcaption></figure></div>

The bezels are saved in `decorations\thebezelproject\games\<system>`. They are used with **AUTO** or **THEBEZELPROJECT**. For FBNeo, the MAME pack is used if the FBNeo pack is not installed.

A bezel is used for a game when its name matches the name of the game file, ignoring upper / lower case, punctuation and the text between parentheses or brackets: `Super Mario World (USA).png` is used for `Super Mario World (Europe).sfc`.

<div align="left"><figure><img src="../.gitbook/assets/image (365).png" alt=""><figcaption></figcaption></figure></div>

### Scraped bezels

ScreenScraper provides 16:9 bezels for some games. Enable **MAIN MENU > SCRAPER > BEZEL (16:9)** before scraping. The bezel is saved with the other media of the game and is used with **AUTO**.

<div align="left"><figure><img src="../.gitbook/assets/image (358).png" alt=""><figcaption></figcaption></figure></div>

You can also choose an image for a game in **EDIT THIS GAME'S METADATA > Bezel (16:9)**.

## How RetroBat finds the bezel

For the selected set (`<set>`), RetroBat uses the first image found:

1. `decorations\<set>\games\<system>\<game>.png`, then `system\decorations\<set>\games\<system>\<game>.png`
2. `decorations\<set>\games\<game>.png`, then `system\decorations\<set>\games\<game>.png`
3. Same folders, with a name that matches (see The Bezel Project above)
4. `decorations\<set>\systems\<system>.png`, then `system\decorations\<set>\systems\<system>.png`
5. `decorations\<set>\default.png`, then `system\decorations\<set>\default.png`
6. `decorations\default_unglazed\systems\<system>.png`, then `system\decorations\default_unglazed\systems\<system>.png`

`system\decorations` contains the sets provided with RetroBat, and is overwritten by updates. `decorations` (at the root of RetroBat) is for your own bezels and for The Bezel Project: it is never overwritten and it is read first.

## Creating your own bezels

### A bezel for one game or one system

Copy your image (PNG, 1920×1080 for a 16:9 screen, transparent where the game is displayed) to:

* `decorations\<set>\games\<system>\<game>.png` for a game (the name of the game file, without extension);
* `decorations\<set>\systems\<system>.png` for a system.

For example, `decorations\default_unglazed\games\snes\Super Mario World.png`.

### Your own set

Any folder in `decorations` appears as a set in the DECORATIONS list (in upper case, `_` replaced by spaces). For example, `decorations\my_bezels` appears as **MY BEZELS**:

```
decorations\my_bezels\default.png                   → bezel for all systems
decorations\my_bezels\systems\snes.png              → bezel for Super Nintendo
decorations\my_bezels\games\snes\Super Metroid.png  → bezel for one game
```

### The .info file

By default, RetroBat places the game in the transparent area of the image. To set the position yourself, add a `.info` file with the same name next to the image (e.g. `snes.info` next to `snes.png`):

```json
{
 "width":1920,
 "height":1080,
 "top":24,
 "left":273,
 "bottom":24,
 "right":273,
 "opacity":1.0,
 "messagex":0.22,
 "messagey":0.12
}
```

* `width`, `height`: size of the image.
* `top`, `left`, `bottom`, `right`: margins, in pixels, between the edges of the image and the game.
* `opacity`: opacity of the bezel (RetroArch).
* `messagex`, `messagey`: position of the RetroArch messages.

## Mega Bezels

Mega Bezels are RetroArch shader packs that draw the bezel and the screen effects themselves (reflections, curve, glow…). They work only with RetroArch cores.

<div align="left"><figure><img src="../.gitbook/assets/image (363).png" alt=""><figcaption></figcaption></figure></div>

1. Download a pack from **MAIN MENU > UPDATES & DOWNLOADS > CONTENT DOWNLOADER**. The packs are saved in `emulators\retroarch\shaders`.

<div align="left"><figure><img src="../.gitbook/assets/image (359).png" alt=""><figcaption></figcaption></figure></div>

2. Select it in **SHADER SET** (in **GAME SETTINGS**, or in the advanced options of a system or game).

<div align="left"><figure><img src="../.gitbook/assets/image (360).png" alt=""><figcaption></figcaption></figure></div>

With a Mega Bezel pack, RetroBat automatically sets **DECORATIONS** to **NONE**, the **GAME ASPECT RATIO** to full screen and the **Vulkan** video driver, unless you changed these options yourself. If you change the video driver, do not use **OPENGL**: Mega Bezels do not work with it (OPENGL CORE or DirectX 10, 11, 12 can work).

To customise them, see [Customize Mega Bezels](../tutorials/customize-mega-bezels.md).

## Tattoos

A tattoo is an image of the controls, displayed over the bezel.

<div align="left"><figure><img src="../.gitbook/assets/image (361).png" alt=""><figcaption></figcaption></figure></div>

Options in **MAIN MENU > GAME SETTINGS > TATTOO** (or in the advanced options of a system or game):

<table><thead><tr><th width="262.75">Option</th><th>Description</th></tr></thead><tbody><tr><td><strong>SHOW TATTOO OVER BEZEL</strong></td><td>Displays the tattoo</td></tr><tr><td><strong>TATTOO CORNER</strong></td><td>Corner of the screen: <strong>TOP LEFT</strong> (default), <strong>TOP RIGHT</strong>, <strong>BOTTOM RIGHT</strong>, <strong>BOTTOM LEFT</strong></td></tr><tr><td><strong>RESIZE TATTOO</strong></td><td>Keeps the original size of the tattoo (reduced only if it is larger than the screen). By default, the tattoo is resized to a fixed width</td></tr></tbody></table>

* A tattoo is displayed only with a bezel: no bezel, no tattoo.
* The tattoo provided by RetroBat follows the controller and button layout used (e.g. 3 or 6 buttons on Mega Drive).
* **Your own tattoos**: put them in `user\tattoos\games\<system>\<game>.png` (one game) or `user\tattoos\default\<system>.png` (a system). They are used first and are not overwritten by updates.
* When **AUTOCONFIGURE CONTROLLERS** is set to **OFF**, only your own tattoos are displayed (the RetroBat tattoos would not match your configuration).
