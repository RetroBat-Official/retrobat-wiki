# Updates & Content Download

## Updates

RetroBat updates itself from the **UPDATES & DOWNLOADS** menu.

### Update settings

In **MAIN MENU > UPDATES & DOWNLOADS**, **SOFTWARE UPDATES** group:

<table><thead><tr><th width="235.25">Option</th><th>Description</th></tr></thead><tbody><tr><td><strong>CHECK FOR UPDATES</strong></td><td>Checks for a new version when RetroBat starts, and displays a message when one is available</td></tr><tr><td><strong>UPDATE TYPE</strong></td><td><strong>stable</strong> (default) or <strong>beta</strong> (test versions, can contain bugs)</td></tr></tbody></table>

<div align="left"><figure><img src="../.gitbook/assets/image (366).png" alt=""><figcaption></figcaption></figure></div>

When a new version is available, a message is displayed at the top of the screen:

<div align="left"><figure><img src="../.gitbook/assets/image (367).png" alt=""><figcaption></figcaption></figure></div>

### Updating RetroBat

1. Open **MAIN MENU > UPDATES & DOWNLOADS** and select **START UPDATE**.
2. RetroBat shows your version and the new one: confirm with **YES**.

<div align="left"><figure><img src="../.gitbook/assets/image (368).png" alt=""><figcaption></figcaption></figure></div>

3. The download and installation progress is shown in the top right corner. Wait until **UPDATE IS READY**.

<div align="left"><figure><img src="../.gitbook/assets/image (369).png" alt=""><figcaption></figcaption></figure></div>

4. Quit and start RetroBat again.

Your current version is shown in **MAIN MENU > SYSTEM SETTINGS > INFORMATION**.

<div align="left"><figure><img src="../.gitbook/assets/image (370).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
An update replaces the files provided with RetroBat. Your own files are kept: put your customisations in the `user` folder (padtokey, inputmapping, tattoos…) and in `decorations`.
{% endhint %}

### Manual update (es-update)

If the update fails from the menu (slow or blocked connection, computer offline…), you can install an update archive yourself.

1. Check your current version in `system\version.info` (or in **SYSTEM SETTINGS > INFORMATION**).
2. Download the archive(s) you need from [retrobat.org/repo/win64/stable/archives](https://www.retrobat.org/repo/win64/stable/archives/). Take the `.zip` files only (e.g. `retrobat-v8.3.0-stable-win64.zip`), and do not rename them.

<div align="left"><figure><img src="../.gitbook/assets/image (371).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="warning" %}
Only the archives of a new **major** version (the second number changes: 8.2.0, 8.3.0, 8.4.0…) are complete, and they must be installed over the previous major version (any 8.2.x for 8.3.0). The other archives (8.3.1, 8.3.1.1…) only contain the changes since the previous version.

So install the archives **in order**, one major version at a time, then the updates of the last major version. For example, to go from 8.1.2 to 8.3.1.1: install 8.2.0, then 8.3.0, then 8.3.1.1.
{% endhint %}

{% hint style="info" %}
The update is done by the `es-update.exe` of your current version. Before RetroBat 8.4.0, an Internet connection is still needed, the archive must be the one of the version proposed by **START UPDATE**, and the archive is deleted after the installation.
{% endhint %}

3. **Quit RetroBat.**
4. Open a command prompt (**Windows + R**, type `cmd`, **Enter**) and go to the `emulationstation` folder of RetroBat:

```bat
cd /d C:\RetroBat\emulationstation
```

5. Run the update with the archive (put the path between quotes):

```bat
es-update.exe -uselocalzip "C:\Users\<name>\Downloads\retrobat-v8.3.0-stable-win64.zip"
```

6. Wait for **UPDATE DONE**. If you have several archives to install, repeat step 5 with the next one.
7. Start RetroBat.

{% hint style="info" %}
The details of the update are written to `emulationstation\es-update.log`. Join this file if you ask for help on Discord or GitHub.
{% endhint %}

## Downloads

The **DOWNLOADS** group of **MAIN MENU > UPDATES & DOWNLOADS** gives access to free content.

### Content downloader

Select **CONTENT DOWNLOADER**. The content is sorted in tabs:

<table><thead><tr><th width="254">Tab</th><th>Content</th></tr></thead><tbody><tr><td><strong>Bezels</strong></td><td><a href="decorations-and-bezels.md">Decorations</a></td></tr><tr><td><strong>Games</strong></td><td>Free games (homebrews, freewares…)</td></tr><tr><td><strong>Intro Videos</strong></td><td>Videos played when RetroBat starts</td></tr><tr><td><strong>Medias and Tools</strong></td><td>Medias and tools</td></tr><tr><td><strong>Shaders and Megabezels</strong></td><td>Shader packs and Mega Bezels for RetroArch (see <a href="https://wiki.retrobat.org/advanced-features/decorations-and-bezels">Decorations</a>)</td></tr></tbody></table>

<div align="left"><figure><img src="../.gitbook/assets/image (372).png" alt=""><figcaption></figcaption></figure></div>

* **LEFT** / **RIGHT**: change tab. **UP** / **DOWN**: move in the list.
* Press **SOUTH** to install the selected content. The installed content is marked with ✔.
* Press **SOUTH** on an installed content to remove it.

The content is downloaded and installed in the right folder automatically.

### Themes

1. Select **THEMES** to open the **THEMES DOWNLOADER**.
2. Select a theme and press **SOUTH** to install it. The progress is shown in the top right corner.

<div align="left"><figure><img src="../.gitbook/assets/image (373).png" alt=""><figcaption></figcaption></figure></div>

3. Once installed, select the theme in **MAIN MENU > USER INTERFACE SETTINGS > THEME SET**.

<div align="left"><figure><img src="../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure></div>

### The Bezel Project

**THE BEZEL PROJECT** downloads bezels for each game of a system. See [Decorations (bezels)](decorations-and-bezels.md).
