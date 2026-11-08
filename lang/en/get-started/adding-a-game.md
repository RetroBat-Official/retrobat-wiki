---
description: Building your library
---

# Adding a game

Adding games is a straightforward process.

{% hint style="warning" %}
RetroBat does not include any games. You must use your own game backups (ROMs).
{% endhint %}

## Adding a ROM

Place your game files (ROMs) in the folder of the corresponding system, inside the `roms` folder of RetroBat:

`<RetroBat folder>\roms\<system>\`

For example, a Super Nintendo game goes in `C:\RetroBat\roms\snes\`.

<div align="left"><figure><img src="../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
The folder name must match the system exactly (e.g. `snes`, not `Super Nintendo`). The folder name and supported file formats for each system are listed in the [Supported Game Systems](../systems-and-emulators/supported-game-systems/) section.

Some systems also require BIOS files to work: see [Adding BIOS files](adding-bios-files.md).

To keep your games in another location (another drive, a NAS…), see [Symbolic links](../tutorials/symbolic-links.md).
{% endhint %}

{% hint style="info" %}
**Multi-disc games:** create a `.m3u` text file listing the discs, one per line (for example `Game (Disc 1).chd`). RetroBat automatically hides the disc files listed in a `.m3u`, `.cue` or `.gdi` file: only one entry appears in the game list.
{% endhint %}

{% hint style="info" %}
**Compressed games:**

* For CD and DVD systems, the **.chd** format is recommended: the game is compressed and read directly by most emulators.
* **.zip / .7z** files are read directly by most RetroArch cores. With some standalone emulators (Dolphin, PCSX2, DuckStation, PPSSPP…), RetroBat mounts or extracts the archive before each launch, which makes loading slower.
* The extraction settings are in **MAIN MENU > GAME SETTINGS**, **COMPRESSION** group: **DECOMPRESSION** (keep or delete the extracted files), **DECOMPRESSION PATH** (by default `roms\.uncompressed`) and **NEVER TRY TO MOUNT AS DRIVE**.
{% endhint %}

New games are detected the next time RetroBat starts, or when you update the gamelist (**MAIN MENU** > **GAME SETTINGS** > **UPDATE GAMELISTS**).

The system then appears in the **System View**.

<div align="left"><figure><img src="../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure></div>

Select it to see your games in the [Game View](../navigation/system-view-and-game-view.md#game-view).

<div align="left"><figure><img src="../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure></div>

## Scraping game information

The next step is to scrape game information: your library will look much better with pictures, videos and descriptions.

Scraping can be done globally, per system or per game.

### Global scraping

Press **START** (**ENTER** on keyboard) to open the **MAIN MENU**, then choose **SCRAPER**.

<div align="left"><figure><img src="../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure></div>

In the **SCRAPE** tab, choose the source, the games and the systems to scrape, then select **SCRAPE NOW**.

<div align="left"><figure><img src="../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
To use ScreenScraper, we recommend creating a free account on the [ScreenScraper website](https://www.screenscraper.fr/), then entering your username and password in the **ACCOUNTS** tab.

More details in the [Scraping & Metadata](../navigation/scraping-and-metadata.md) section.
{% endhint %}

While scraping is in progress, the following message is displayed at the top right of the screen.

<div align="left"><figure><img src="https://i.imgur.com/7WXE0GL.png" alt=""><figcaption><p>Scraping in progress</p></figcaption></figure></div>

Once scraping is finished, update the gamelist: press **START** (**ENTER** on keyboard) to open the Main Menu, select **GAME SETTINGS**…

<div align="left"><figure><img src="https://i.imgur.com/X1sumBQ.png" alt=""><figcaption></figcaption></figure></div>

… then **UPDATE GAMELISTS**.

<div align="left"><figure><img src="https://i.imgur.com/B9beKo6.png" alt=""><figcaption></figcaption></figure></div>

Game information is now displayed in the [Game View](../navigation/system-view-and-game-view.md#game-view).

<div align="left"><figure><img src="../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure></div>

### Per-game scraping

To scrape a single game, highlight it in the Game View and long-press ![](<../.gitbook/assets/image (30).png>) to open the [Game Options](../navigation/game-options.md), then select **SCRAPE**.

<div align="left"><figure><img src="../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure></div>

A list of possible matches is displayed. Select the right game and confirm with ![](<../.gitbook/assets/image (30).png>).

{% hint style="info" %}
The search is based on the ROM file name by default. To search with another name, use the **INPUT** button at the bottom of the screen.
{% endhint %}

<div align="left"><figure><img src="../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure></div>

**Congratulations!** You have added your first games to RetroBat. Next step: Running a game.
