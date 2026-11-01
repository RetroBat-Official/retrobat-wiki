# Scraping & Metadata

Scraping downloads the information (name, description, release date, genre…) and the media (images, videos, manuals, maps…) of your games from online databases.

## Scraping services

<table><thead><tr><th width="230.25">Service</th><th>Account</th></tr></thead><tbody><tr><td><a href="https://www.screenscraper.fr/">ScreenScraper</a> (default)</td><td>Free account recommended (faster, fewer limits)</td></tr><tr><td><a href="https://thegamesdb.net/">TheGamesDB</a></td><td>Not required</td></tr><tr><td><a href="https://db.hfsplay.fr/">HFSDB</a></td><td>Not required</td></tr><tr><td>ArcadeDB</td><td>Not required (arcade games only)</td></tr><tr><td><a href="https://www.igdb.com/">IGDB</a></td><td><strong>Required</strong>: Client ID and Client Secret, see <a href="https://api-docs.igdb.com/#getting-started">Setting up IGDB</a></td></tr></tbody></table>

## Information that can be scraped

* Game information: name, description, release date, developer, publisher, genre, number of players, rating…
* Images: box (2D or 3D), box backside, screenshot or title screen, logo (wheel or marquee), fan art, map, cartridge, bezel (16:9)
* Video
* Manual
* PadToKey settings

## How to scrape

* **All games or several systems**: see [Global scraping](../get-started/adding-a-game.md#global-scraping).
* **One game**: see [Per-game scraping](../get-started/adding-a-game.md#per-game-scraping).

## The scraper menu

Open **MAIN MENU** > **SCRAPER**. The menu has three tabs.

<div align="left"><figure><img src="../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure></div>

### SCRAPE tab

<table><thead><tr><th width="295.25">Setting</th><th>Description</th></tr></thead><tbody><tr><td><strong>SCRAPE FROM</strong></td><td>Service to use</td></tr><tr><td><strong>GAMES TO SCRAPE FOR</strong></td><td>All games, games missing any media, or games missing all media</td></tr><tr><td><strong>IGNORE RECENTLY SCRAPED GAMES</strong></td><td>Skip the games scraped during the last day, week, month…</td></tr><tr><td><strong>SYSTEMS INCLUDED</strong></td><td>Systems to scrape</td></tr><tr><td><strong>SCRAPE NOW</strong></td><td>Start scraping</td></tr></tbody></table>

### OPTIONS tab

The available settings depend on the selected service.

<div align="left"><figure><img src="../.gitbook/assets/image (259).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="192.75">Section</th><th>Settings</th></tr></thead><tbody><tr><td>Settings</td><td><strong>IMAGE SOURCE</strong> (screenshot, title screen, mix, box…), <strong>BOX SOURCE</strong> (2D or 3D box), <strong>LOGO SOURCE</strong> (wheel, HD wheel, marquee), <strong>PREFERED REGION</strong>, <strong>OVERWRITE NAMES / DESCRIPTIONS / MEDIAS</strong></td></tr><tr><td>Scrape for</td><td>Media and information to download: short name, community rating, video, fan art, bezel (16:9), box backside, map, title shot, cartridge, manual, PadToKey settings</td></tr><tr><td>Manual scrape</td><td><strong>INCLUDED SCRAPERS</strong>: services queried when you scrape a single game</td></tr></tbody></table>

{% hint style="info" %}
Keep **OVERWRITE NAMES / DESCRIPTIONS / MEDIAS** disabled if you have edited your games manually: otherwise your changes will be replaced.
{% endhint %}

### ACCOUNTS tab

<div align="left"><figure><img src="../.gitbook/assets/image (260).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="167.75">Section</th><th>Settings</th></tr></thead><tbody><tr><td>ScreenScraper</td><td><strong>USERNAME</strong> and <strong>PASSWORD</strong> of your <a href="https://www.screenscraper.fr/">ScreenScraper</a> account</td></tr><tr><td>IGDB</td><td><strong>CLIENT ID</strong> and <strong>CLIENT SECRET</strong>, see below</td></tr></tbody></table>

## Setting up IGDB

IGDB belongs to Twitch: to use it, you need to create a (free) "application" on the Twitch developer website, which gives you a **Client ID** and a **Client Secret**.

1. **Create a Twitch account** on [twitch.tv](https://www.twitch.tv/) if you do not have one, and verify your email address.
2. **Enable two-factor authentication (2FA)**: Twitch **Settings** > **Security and Privacy** > **Set Up Two-Factor Authentication** (a phone number is required). The developer console does not work without 2FA.
3. Open the [Twitch developer console](https://dev.twitch.tv/console) and log in.
4. In the **Applications** tab, click **Register Your Application** and fill in the form:
   * **Name**: a unique name, for example `retrobat-` followed by random characters (if the name is already used, the creation fails)
   * **OAuth Redirect URLs**: `http://localhost`
   * **Category**: **Application Integration**
   * **Client Type**: **Confidential**
5. Validate the captcha, then click **Create**.
6. In the list of applications, click **Manage** on your application:
   * copy the **Client ID**;
   * click **New Secret**, confirm, then copy the **Client Secret**.
7. In RetroBat, open **MAIN MENU** > **SCRAPER** > **ACCOUNTS** and enter the **CLIENT ID** and **CLIENT SECRET** in the **IGDB** section.
8. In the **SCRAPE** tab, select **IGDB** in **SCRAPE FROM**.

{% hint style="info" %}
**Easier than typing with a controller:** close RetroBat, open `emulationstation\.emulationstation\es_settings.cfg` with a text editor, and add (or complete) these two lines:

```xml
<string name="IGDBClientID" value="your client id" />
<string name="IGDBSecret" value="your client secret" />
```
{% endhint %}

{% hint style="warning" %}
* Keep your Client Secret private.
* Clicking **New Secret** again creates a new secret and invalidates the previous one: you then need to enter it again in RetroBat.
{% endhint %}

## Storage of scraped media

Media are stored in the folder of each system, in subfolders. Each file is named after the game file, followed by the media type.

<div align="left"><figure><img src="../.gitbook/assets/image (261).png" alt=""><figcaption></figcaption></figure></div>

<table data-header-hidden><thead><tr><th width="153.25"></th><th width="252"></th><th></th></tr></thead><tbody><tr><td><strong>Folder</strong></td><td><strong>Media</strong></td><td>Example for <code>roms\snes\Super Metroid.zip</code></td></tr><tr><td><code>images</code></td><td>Box, box backside, screenshot, logo, fan art, map, cartridge, title shot, bezel…</td><td><code>images\Super Metroid-thumb.png</code>, <code>-image</code>, <code>-marquee</code>, <code>-fanart</code>, <code>-boxback</code>, <code>-box</code>, <code>-wheel</code>, <code>-map</code>, <code>-cartridge</code>, <code>-titleshot</code>, <code>-bezel</code></td></tr><tr><td><code>videos</code></td><td>Videos</td><td><code>videos\Super Metroid-video.mp4</code></td></tr><tr><td><code>manuals</code></td><td>Manuals (PDF)</td><td><code>manuals\Super Metroid-manual.pdf</code></td></tr><tr><td><code>magazines</code></td><td>Magazines</td><td><code>magazines\Super Metroid-magazine.pdf</code></td></tr></tbody></table>

The game information and the links to the media are saved in the `gamelist.xml` file of the system folder (for example `roms\snes\gamelist.xml`).

## Using your own media

You can use images and videos you already have, or that you have created yourself.

1. Name each file exactly like the game file (without its extension), followed by the media type:

| File                        | Media                   | Folder   |
| --------------------------- | ----------------------- | -------- |
| `Super Metroid-thumb.png`   | Box                     | `images` |
| `Super Metroid-image.png`   | Game image (screenshot) | `images` |
| `Super Metroid-marquee.png` | Logo                    | `images` |
| `Super Metroid-video.mp4`   | Video                   | `videos` |

2. Copy the files to the `images` or `videos` folder of the system (for example `roms\snes\images`). Images can be `.png` or `.jpg`.
3. Enable **SEARCH FOR LOCAL ART** in **MAIN MENU** > **SYSTEM SETTINGS** > **FRONTEND DEVELOPER OPTIONS** > **DATA MANAGEMENT**.

<div align="left"><figure><img src="../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
Your files are only used when the game has no media of this type in the game list. To use your own media for a game that has already been scraped, attach them with **EDIT THIS GAME'S METADATA** (see below).
{% endhint %}

## Editing game metadata manually

In the [Game options](game-options.md) menu, choose **EDIT THIS GAME'S METADATA**:

<div align="left"><figure><img src="../.gitbook/assets/image (263).png" alt=""><figcaption></figcaption></figure></div>

You can:

* change the game information: name, description, rating, release date, developer, publisher, game family, genres, arcade system, number of players, languages, region;
* attach other media files (image, video, logo, box, fan art, manual, map…);
* add the game to favorites;
* hide the game;
* mark the game as a **kid game**, to display it in [Kid mode](../advanced-features/kiosk-and-kid-mode.md#kid-mode).
