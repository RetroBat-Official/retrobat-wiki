---
description: Before you start...
---

# Prerequisites

Before installing RetroBat, make sure your PC meets the following requirements. RetroBat will not work properly without them.

<table><thead><tr><th width="160.25"></th><th></th></tr></thead><tbody><tr><td><strong>Operating system</strong></td><td>Windows 10 or Windows 11 (64-bit).<br>Windows 8.1 (64-bit) may work, but several recent emulators no longer support it.</td></tr><tr><td><strong>Processor</strong></td><td>64-bit CPU with SSE2 support (minimum).<br>A 3 GHz dual-core CPU from 2008 or later is recommended. Some recent emulators require newer instruction sets (e.g. SSE4.1).</td></tr><tr><td><strong>Graphics</strong></td><td>Graphics card supporting Direct3D 11.1, OpenGL 4.4 or Vulkan.<br>Install the latest drivers from your manufacturer's website (NVIDIA, AMD or Intel), not only those provided by Windows Update.</td></tr><tr><td><strong>Dependencies</strong></td><td>Visual C++ Redistributables and DirectX are installed automatically by the RetroBat installer.<br>If an emulator does not start, you can reinstall them manually:</td></tr><tr><td></td><td><a href="https://www.techpowerup.com/download/visual-c-redistributable-runtime-package-all-in-one/">Visual C++ Redistributable Runtimes All-in-One</a>: installs all required versions (2010, 2015-2022, 32 and 64-bit) at once.</td></tr><tr><td></td><td><a href="https://www.microsoft.com/download/details.aspx?id=35">DirectX End-User Runtime</a>: required even on Windows 10/11, which do not include the legacy DirectX 9 components used by some emulators.</td></tr><tr><td><strong>Controllers</strong></td><td>XInput (Xbox-compatible) controllers are recommended for the best compatibility.<br>Most other controllers (PlayStation, Switch Pro…) also work, but may need extra configuration in some emulators.<br>You can test your controller on <a href="https://gamepad-tester.com/">gamepad-tester.com</a>.</td></tr></tbody></table>

{% hint style="warning" %}
**Where to install RetroBat**

Install RetroBat in a short path without spaces or special characters, for example `C:\RetroBat` or `D:\RetroBat`.

Avoid:

* `C:\Program Files` or `C:\Program Files (x86)` (Windows restricts write access, so settings and saves may not be stored)
* Folders synchronized with OneDrive (Desktop, Documents, Pictures are often synchronized by default)
{% endhint %}
