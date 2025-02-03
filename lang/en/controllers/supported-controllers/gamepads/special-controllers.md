# Special controllers

For Some emulators, RetroBat is able to automatically configure special controllers such as N64 controllers or Genesis-like controllers.

The mapping can be user-defined in json files, some controllers configuration are already provided with RetroBat.



### Mapping file location

Mapping for special controllers can be found in the `system\resources\inputmapping` folder of your RetroBat installation, the current list of special controllers is the following:

* Saturn & Genesis controllers
* N64 controllers



### Controllers & emulators currently supported

The following table provides a list of currently-supported special controllers and emulators in which RetroBat offers autoconfiguration.

{% hint style="info" %}
When a special controller is detected, RetroBat will completely ignore the configuration done in RetroBat for the controller button mapping and force mapping to match the original system.
{% endhint %}



<table><thead><tr><th width="177">Controller type</th><th width="378">Controller</th><th>Emulators</th></tr></thead><tbody><tr><td>N64 Controller</td><td>Nintendo Switch Online N64 Controller<br>(030000007e050000192000000000680c)</td><td>RetroArch<br>Ares<br>Bizhawk<br>Mupen64(RMG)<br>Simple64<br>Ship Of Harkinian</td></tr><tr><td></td><td>Mayflash N64 Adapter (2 players)<br>(03000000d620000010a7000000000000)</td><td>RetroArch<br>Ares<br>Bizhawk<br>Mupen64(RMG)<br>Simple64<br>Ship Of Harkinian</td></tr><tr><td></td><td>Raphnet N64 Adapter (2 players)<br>(030000009b2800006300000000000000)</td><td>RetroArch<br>Ares<br>Bizhawk<br>Mupen64(RMG)<br>Simple64<br>Ship Of Harkinian</td></tr><tr><td>Genesis Controller</td><td>8BitDo M30 (xinput mode)<br>(030000005e040000e002000000007200)</td><td>RetroArch<br>Ares<br>Bizhawk<br>JGenesis<br>Kega-Fusion<br>Mednafen</td></tr><tr><td></td><td>8BitDo M30 (switch mode)<br>(030000007e0500000920000000006803)</td><td>RetroArch<br>Ares<br>Bizhawk<br>JGenesis<br>Kega-Fusion<br>Mednafen</td></tr><tr><td></td><td>8BitDo M30 (dinput mode)<br>(03000000c82d00005106000000000000)</td><td>RetroArch<br>Ares<br>Bizhawk<br>JGenesis<br>Kega-Fusion<br>Mednafen</td></tr><tr><td>Saturn Controller</td><td>8BitDo M30 (xinput mode)<br>(030000005e040000e002000000007200)</td><td>RetroArch<br>Bizhawk<br>Kronos<br>Mednafen<br>SSF<br>YabaSanshiroRetroAr</td></tr><tr><td></td><td>8BitDo M30 (switch mode)<br>(030000007e0500000920000000006803)</td><td>RetroArch<br>Bizhawk<br>Kronos<br>SSF<br>YabaSanshiro</td></tr><tr><td></td><td>8BitDo M30 (dinput mode)<br>(03000000c82d00005106000000000000)</td><td>RetroArch<br>Bizhawk<br>Kronos<br>Mednafen<br>SSF<br>YabaSanshiro</td></tr></tbody></table>
