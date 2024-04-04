# Know issues & fixes

This section is constantly updated with official fixes provided by the Team for specific issues raised by users in our official support channels.

{% hint style="danger" %}
These fixes are only compatible with the latest version of RetroBat, it might brake old versions.
{% endhint %}

## Clean es\_input file

If your controller settings become messed-up and you need a clean start, here is a `es_input.cfg` file that you can copy in your `retrobat\emulationstation\.emulationstation` folder.

It contains only standard keyboard settings, you will have to perform again your controller configuration.

{% file src="../.gitbook/assets/es_input.cfg" %}

## PSP black screen when loading content with lr-ppsspp

The Libretro-ppsspp core for PSP is not compatible with the rewind functionality, disable "REWIND" and it should function properly.

<div align="left">

<figure><img src="https://i.imgur.com/f5hdMPJ.png" alt=""><figcaption></figcaption></figure>

</div>

## Other miscellaneous fixes

For all the issues below, download the emulationstation.zip file at the end of this page and unzip the full content in the emulationstation\ folder of your RetroBat installation.

* OpenBOR path error on exit
* Chihiro missing features (with Chihiro emulator)
* Incorrect MAME64 controller order
* New XBOX controllers (or ones with new firmware) not working correctly (specifically in Ryujinx or Cemu)
* Non-working Future Pinball features

{% file src="../.gitbook/assets/EmulationStation (2).zip" %}
