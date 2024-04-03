# Know issues & fixes

This section is constantly updated with official fixes provided by the Team for specific issues raised by users in our official support channels.

## Clean es\_input file

If your controller settings become messed-up and you need a clean start, here is a `es_input.cfg` file that you can copy in your `retrobat\emulationstation\.emulationstation` folder.

It contains only standard keyboard settings, you will have to perform again your controller configuration.

{% file src="../.gitbook/assets/es_input.cfg" %}

## PSP black screen when loading content with lr-ppsspp

The Libretro-ppsspp core for PSP is not compatible with the rewind functionality, disable "REWIND" and it should function properly.

<div align="left">

<figure><img src="https://i.imgur.com/f5hdMPJ.png" alt=""><figcaption></figcaption></figure>

</div>

## openBor path error on exit

Unzip the following file in the emulationstation\ folder of your RetroBat installation:

{% file src="../.gitbook/assets/EmulationStation (2).zip" %}
