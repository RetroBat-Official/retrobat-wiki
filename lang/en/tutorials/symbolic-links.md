---
description: Store your games in a different folder
---

# Symbolic links

Windows supports **symbolic links**: a folder that points to another folder, elsewhere on the computer or on the network.

**How is this interesting for RetroBat?** You can keep your games outside the `roms` folder of RetroBat (on a larger hard drive, or on a NAS), while RetroBat still sees them in `roms`.

**Example:**

<div align="left"><figure><img src="../.gitbook/assets/image (418).png" alt=""><figcaption></figcaption></figure></div>

## Creating a symbolic link

There are three methods: the **Link Shell Extension** tool (simplest), or the **Command Prompt** with a junction or a symbolic link.

{% hint style="warning" %}
Before creating a link, move your games to the new location and check that the folder you replace in `roms` contains nothing you want to keep: it must be deleted, because a link cannot be created over an existing folder.
{% endhint %}

### Download Link Shell Extension

The program can be downloaded from the following website : [https://schinagl.priv.at/nt/hardlinkshellext/linkshellextension.html#download](https://schinagl.priv.at/nt/hardlinkshellext/linkshellextension.html#download)

### Use Link Shell Extension

After the installation, restart your computer (or restart the `explorer.exe` process). New options appear when you right-click:

* **Pick Link Source**

<div align="left"><figure><img src="../.gitbook/assets/image (416).png" alt=""><figcaption></figcaption></figure></div>

* **Drop As...**

<div align="left"><figure><img src="../.gitbook/assets/image (415).png" alt=""><figcaption></figcaption></figure></div>

### Create a symbolic link with Link Shell Extension

In this example, the 3DO games are in `D:\Retrobat\3do`, and RetroBat is installed in `C:\Retrobat`.

1. Copy all your games to `D:\Retrobat\3do`. Check that `C:\Retrobat\roms\3do` contains nothing you want to keep.
2. Delete the `C:\Retrobat\roms\3do` folder.
3. Right-click `D:\Retrobat\3do` and choose **Pick Link Source**.
4. Open `C:\Retrobat\roms`, right-click in the folder and choose **Drop As... > Symbolic Link**.
5. The `3do` folder now appears in `C:\Retrobat\roms` with a small arrow on its icon:

<div align="left"><figure><img src="../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure></div>

**CONGRATULATIONS**: you have just created a symbolic link! Do the same for every folder you want to store elsewhere.

### Create a link with the Command Prompt

Same example as above. Do steps 1 and 2 above first, then use one of these commands.

#### Local drive: junction (no administrator rights needed)

Open a **Command Prompt** (`cmd`) and type:

```
mklink /J "C:\Retrobat\roms\3do" "D:\Retrobat\3do"
```

#### Network share (NAS): symbolic link

Open a **Command Prompt as administrator** (right-click on **Command Prompt** > **Run as administrator**) and type:

```
mklink /D "C:\Retrobat\roms\3do" "\\NAS\Games\3do"
```

{% hint style="info" %}
* Use the network path (`\\NAS\...`), not a mapped drive letter (`Z:\`): mapped drives are not visible from a Command Prompt run as administrator.
* `mklink /D` also works for a local drive, but needs administrator rights (or the **Developer Mode** of Windows).
{% endhint %}

The `3do` folder now appears in `C:\Retrobat\roms` with a small arrow on its icon:

<div align="left"><figure><img src="../.gitbook/assets/image (426).png" alt=""><figcaption></figcaption></figure></div>

## Linking the whole roms folder

To store all your games elsewhere at once, link the whole `roms` folder instead of each system:

1. Move the content of `C:\Retrobat\roms` to `D:\Retrobat\roms`.
2. Delete the empty `C:\Retrobat\roms` folder.
3. Create the link: `mklink /J "C:\Retrobat\roms" "D:\Retrobat\roms"` (or `/D` for a network share).

## Good to know

* **Game data:** the game lists (`gamelist.xml`) and the scraped pictures and videos are stored in the game folders, so they are also saved on the target drive.
* **Removing a link:** delete the link folder in `roms` (the one with the arrow), or type `rmdir "C:\Retrobat\roms\3do"`. Only the link is removed: your games stay in `D:\Retrobat\3do`.

{% hint style="danger" %}
Do not delete the **content** of the link folder: the files you see in it are your real games, and they would be deleted from the target drive.
{% endhint %}

* **Network share:** loading the game lists is slower over the network. If the NAS is not available when RetroBat starts, the linked systems appear empty.
