# Special controllers

For Some emulators, RetroBat is able to automatically configure special controllers such as N64 controllers or Genesis-like controllers.

The mapping can be defined by each user in json files, some controllers configuration are already provided with RetroBat.

### Mapping file location

Mapping for special controllers can be found in the `system\resources\inputmapping` folder of your RetroBat installation, the current list of special controllers is the following:

* 3DO controllers
* Megadrive/Genesis controllers
* Saturn controllers
* N64 controllers
* Gamecube controllers

{% hint style="info" %}
If you change the mapping or add controllers, place your modified file in the user\inputmapping folder of your RetroBat installation, else it might be overwritten during an update.
{% endhint %}

### Type of controllers & emulators currently supported

The following table provides a list of currently-supported type of special controllers and emulators in which RetroBat offers autoconfiguration.

{% hint style="info" %}
When a special controller is detected, RetroBat will completely ignore the configuration done in RetroBat for the controller button mapping and force mapping to match the original system.
{% endhint %}

<table><thead><tr><th width="379.0999755859375">Controller type</th><th>Emulators</th></tr></thead><tbody><tr><td>N64 Controller</td><td>RetroArch<br>Ares<br>Bizhawk<br>Mupen64(RMG)<br>Simple64<br>Ship Of Harkinian</td></tr><tr><td>Megadrive/Genesis Controller</td><td>RetroArch<br>Ares<br>Bizhawk<br>JGenesis<br>Kega-Fusion<br>Mednafen</td></tr><tr><td>Saturn Controller</td><td>RetroArch<br>Bizhawk<br>Kronos<br>Mednafen<br>SSF<br>YabaSanshiro<br>Ymir</td></tr><tr><td>GameCube controller</td><td>Dolphin (standalone)</td></tr><tr><td>3DO controller</td><td>RetroArch</td></tr></tbody></table>
