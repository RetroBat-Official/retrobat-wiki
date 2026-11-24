---
description: >-
  Sort the games of a system into subfolders and give them an image, a logo, a
  video
---

# Create game subfolders

## Why subfolders?

In the folder of a system (for example `roms\snes`), you can put your games in subfolders: hacks, homebrews, translations, games by region, eShop games… RetroBat can display these subfolders in the game list, and you can "dress" them with an image, a logo, a box, a video and a description, like a game.

{% hint style="info" %}
To group games **without moving their files**, use custom collections instead. For more details, see the Game Collections page.
{% endhint %}

## Creating the subfolders

1. Close RetroBat.
2. In the folder of the system, create one subfolder per category and move the games into it. In the example of this page, the `roms\snes` folder contains three subfolders: `HACKS`, `HOMEBREWS` and `TRADS`.
3. Start RetroBat again.

{% hint style="warning" %}
The information and media of games already scraped are linked to the path of the game file in `gamelist.xml`. After moving a game that was already scraped, scrape it again, or fix its `<path>` tag in `gamelist.xml` (with RetroBat closed, for example `./HACKS/Super Metroid Redesign.sfc`).
{% endhint %}

## Showing the subfolders

By default, RetroBat does not show folders: the games of the subfolders all appear together in the list of the system.

To show folders in all systems:

1. Press **START** to open the **MAIN MENU**.
2. Go to **USER INTERFACE SETTINGS** > **GAMELIST OPTIONS**.
3. Set **SHOW FOLDERS** to **ALWAYS**.

<div align="left"><figure><img src="../.gitbook/assets/image (723).png" alt=""><figcaption></figcaption></figure></div>

<table><thead><tr><th width="237.75">Choice</th><th>Effect</th></tr></thead><tbody><tr><td><strong>NEVER</strong> (default)</td><td>No folders: all the games of the system are shown in a single list.</td></tr><tr><td><strong>ALWAYS</strong></td><td>Each subfolder is shown as an entry of the list. Open it with <strong>SOUTH</strong>, go back with <strong>EAST</strong>.</td></tr><tr><td><strong>HAVING MULTIPLE GAMES</strong></td><td>Only the folders that contain several games are shown. A folder with only one game is replaced by this game, an empty folder is hidden.</td></tr></tbody></table>

With **SHOW FOLDERS FIRST** (enabled by default, same menu), folders are placed at the top of the list.

To show folders in one system only: in the game list of this system, press **SELECT**, then go to **VIEW CUSTOMIZATION** > **GAMELIST OPTIONS** > **SHOW FOLDERS**. For this system, this setting replaces the one of the **MAIN MENU** (**AUTO** uses the general setting). For more details, see the View Options page.

<div align="left"><figure><img src="../.gitbook/assets/image (724).png" alt=""><figcaption></figcaption></figure></div>

## Dressing the subfolders

A folder can get the same media as a game. Three methods, from the easiest to the most technical.

### Method 1: from RetroBat (easiest)

1. In the game list, select the folder.
2. Hold **SOUTH** to open the **GAME OPTIONS** menu (or press **NORTH** if the **ACCESS GAME OPTIONS WITH NORTH BUTTON** option is enabled).
3. Choose **EDIT FOLDER METADATA**.
4. Fill in the displayed name, the description, and link the image, logo, box, video… like for a game.

<div align="left"><figure><img src="../.gitbook/assets/image (725).png" alt=""><figcaption></figcaption></figure></div>

RetroBat saves this information in the `gamelist.xml` file of the system.

{% hint style="info" %}
The **SCRAPE** entry is also offered on a folder, but the scraping services rarely find a result for a folder name: prefer the methods of this page.
{% endhint %}

### Method 2: naming the media files

RetroBat can find the media of a folder by itself if they are named after the folder, followed by the media type.

1. Enable **SEARCH FOR LOCAL ART** in **MAIN MENU** > **SYSTEM SETTINGS** > **FRONTEND DEVELOPER OPTIONS** > **DATA MANAGEMENT**.
2. In the folder of the system (not in the subfolder), create the `images` and `videos` folders if needed. These are the folders used by the scraper: they already exist if you scraped this system.
3. Copy your files there, named after the folder:

| File                | Media              | Folder   |
| ------------------- | ------------------ | -------- |
| `HACKS-thumb.png`   | Box                | `images` |
| `HACKS-image.png`   | Image (screenshot) | `images` |
| `HACKS-marquee.png` | Logo               | `images` |
| `HACKS-video.mp4`   | Video              | `videos` |

In our example, the files are therefore `roms\snes\images\HACKS-thumb.png`, `roms\snes\images\HACKS-image.png`, `roms\snes\images\HACKS-marquee.png` and `roms\snes\videos\HACKS-video.mp4`.

<div align="left"><figure><img src="../.gitbook/assets/image (726).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
* Images can be `.png` or `.jpg`, videos `.mp4`.
* The name must be exactly the name of the folder, including upper case.
* These files are used only if the folder does not already have a media of this type in `gamelist.xml` (for example a media linked with method 1).
* For more details on media names, see the Scraping & Metadata page.
{% endhint %}

### Method 3: editing the gamelist.xml file (advanced)

The `gamelist.xml` file of the system (for example `roms\snes\gamelist.xml`) links the games, the folders and their media. RetroBat creates it (scraping, metadata editing) and it can be edited with a text editor (Notepad, Notepad++…).

1. **Close RetroBat**: RetroBat saves the game lists when it quits, and would overwrite your changes.
2. Make a backup copy of `gamelist.xml`.
3. Add a `<folder>` block just before the last line, `</gameList>`. If the file already contains a `<folder>` block with the same `<path>`, complete this one instead of adding a second one.

Example for the `HACKS` folder:

```xml
    <folder>
        <path>./HACKS</path>
        <name>HACKS</name>
        <desc>Super Nintendo game hacks.</desc>
        <image>./images/HACKS-image.png</image>
        <thumbnail>./images/HACKS-thumb.png</thumbnail>
        <marquee>./images/HACKS-marquee.png</marquee>
        <video>./videos/HACKS-video.mp4</video>
    </folder>
```

| Tag                                              | Content                                                                                               |
| ------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| `<path>`                                         | Path of the subfolder from the system folder, starting with `./`. Must match the folder name exactly. |
| `<name>`                                         | Name displayed in the game list.                                                                      |
| `<desc>`                                         | Description.                                                                                          |
| `<image>`, `<thumbnail>`, `<marquee>`, `<video>` | Paths of the media from the system folder. With this method, the files can have any name.             |

Only the tags you need are required. The other game tags (`<fanart>`, `<boxback>`, `<manual>`…) are also accepted.

## Bonus: flags in a folder name

RetroBat replaces some special characters with a flag. These flags are the images of the `emulationstation\resources\flags` folder of RetroBat.

<div align="left"><figure><img src="../.gitbook/assets/image (727).png" alt=""><figcaption></figcaption></figure></div>

Copy the character from the **Character to copy** column and paste it in the folder name (in Windows Explorer), or in the displayed name of the folder (method 1 or `<name>` tag of method 3).

| Country        | File     | Code     | Character to copy |
| -------------- | -------- | -------- | ----------------- |
| Australia      | `au.png` | `0xF300` | ``               |
| Brazil         | `br.png` | `0xF301` | ``               |
| Canada         | `ca.png` | `0xF302` | ``               |
| China          | `cn.png` | `0xF303` | ``               |
| Germany        | `de.png` | `0xF304` | ``               |
| Spain          | `es.png` | `0xF305` | ``               |
| Europe         | `eu.png` | `0xF306` | ``               |
| France         | `fr.png` | `0xF307` | ``               |
| Greece         | `gr.png` | `0xF308` | ``               |
| India          | `in.png` | `0xF309` | ``               |
| Italy          | `it.png` | `0xF30A` | ``               |
| Japan          | `jp.png` | `0xF30B` | ``               |
| South Korea    | `kr.png` | `0xF30C` | ``               |
| Netherlands    | `nl.png` | `0xF30D` | ``               |
| Norway         | `no.png` | `0xF30E` | ``               |
| Portugal       | `pt.png` | `0xF30F` | ``               |
| Russia         | `ru.png` | `0xF310` | ``               |
| Sweden         | `sw.png` | `0xF311` | ``               |
| United Kingdom | `uk.png` | `0xF312` | ``               |
| United States  | `us.png` | `0xF313` | ``               |
| World          | `wr.png` | `0xF314` | ``               |

{% hint style="info" %}
* These characters are not visible on this page nor in Windows (empty box or square): they are displayed as a flag only in RetroBat.
* They also work in the displayed name of a game.
* If you change the name of a folder, also rename its media files (method 2) or its `<path>` (method 3).
{% endhint %}
