---
description: Let's get started!
---

# Installation & First Startup

## Installation

* Download the latest RetroBat installer from the [RetroBat website](https://www.retrobat.org/download/).
* Run the installer and click **Next**.

<div align="left"><figure><img src="../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure></div>

* Read and accept the license agreement, then click **Next**.

<div align="left"><figure><img src="../.gitbook/assets/image (184).png" alt=""><figcaption></figcaption></figure></div>

* Select the missing prerequisites to install, then click **Next**.

{% hint style="info" %}
The installer automatically installs the required prerequisites (Visual C++ Redistributables, DirectX). If they are already installed, this page will not appear.
{% endhint %}

<div align="left"><figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure></div>

* Choose the installation folder and click \*\*Install\*\*.

{% hint style="danger" %}
**Where to install RetroBat**

Install RetroBat in a short path, inside a folder, for example `C:\RetroBat` or `D:\Games\RetroBat`.

Avoid:

* Installing directly at the root of a drive (RetroBat files would end up mixed with everything else in `D:\`). Always use a folder.
* Spaces, accents or special characters in the path.
* Long paths or deeply nested folders: they cause issues with some emulators (e.g. the MAME libretro core).
* `C:\Program Files` or `C:\Program Files (x86)`: Windows restricts write access, so settings and saves may not be stored.
* Folders synchronized with OneDrive (Desktop, Documents, Pictures are often synchronized by default).
{% endhint %}

<div align="left"><figure><img src="../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure></div>

* Wait until the installation completes, then click **Finish**.

<div align="left"><figure><img src="../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure></div>

To learn what each RetroBat folder contains, see [RetroBat Folder Structure](retrobat-folder-structure.md).

## First startup

Double-click the `RetroBat.exe` file in your RetroBat folder, or use the desktop shortcut.

After the intro video, the **System View** is displayed.

<div align="left"><figure><img src="../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure></div>

{% hint style="info" %}
At first startup, RetroBat uses your Windows language if it is supported: English, French, Japanese, Spanish, German, Italian, Dutch, Portuguese, Russian, Korean, Chinese, Polish and Arabic.
{% endhint %}

You can navigate with the keyboard or with a controller (see [Navigation Keys](../navigation/navigation-keys.md)).

If your controller is not configured automatically:

* Press any button: the **CONFIGURE INPUT** screen appears.

<div align="left"><figure><img src="../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure></div>

* Press and hold any button on the controller you want to configure: the **CONFIGURING** screen appears.

<div align="left"><figure><img src="../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure></div>

* Press the corresponding button on your controller for each input. If your controller does not have a given button, press and hold any button to skip it.

{% hint style="info" %}
We recommend using **SELECT** (or **Back**/**View** on Xbox controllers) as the **hotkey**. The hotkey is combined with other buttons to trigger shortcuts, such as exiting a game or saving a state. See Hotkeys.
{% endhint %}

**Congratulations!** RetroBat is installed and running. Next step: Adding a game.
