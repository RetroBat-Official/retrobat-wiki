# Know issues & fixes

This section is constantly updated with official fixes provided by the Team for specific issues raised by users in our official support channels.

{% hint style="danger" %}
These fixes are only compatible with the latest version of RetroBat, it might brake old versions.
{% endhint %}

## Clean es\_input file

If your controller settings become messed-up and you need a clean start, here is a `es_input.cfg` file that you can copy in your `retrobat\emulationstation\.emulationstation` folder.

It contains only standard keyboard settings, you will have to perform again your controller configuration.

{% file src="../.gitbook/assets/es_input.cfg" %}

## Graphical issues in RetroBat interface

If you own a GPU that is old and not compatible with latest OpenGL versions, it is possible that some rendering effects will not work and glitch or totally crash RetroBat.

To fix this issue, it is possible to force RetroBat interface to use OpenGL 2.1 compatible renderer.

Open the **retrobat.ini** file that is found in the root folder of your RetroBat installation and set the following value to 1:

<div align="left"><figure><img src="https://i.imgur.com/fqv5SM1.png" alt=""><figcaption></figcaption></figure></div>

Save the file and run RetroBat.

This setting is also available from BatGui:

<div align="left"><figure><img src="https://i.imgur.com/5aJ94sX.png" alt=""><figcaption></figcaption></figure></div>
