# Contrôleurs spéciaux

Pour certains émulateurs, RetroBat est capable de configurer automatiquement certains contrôleurs spéciaux, comme des manettes N64 ou des manettes reprenant l'aspect des manettes Genesis.

Le mappage peut alors être défini par l'utilisateur dans des fichiers .json, certains configuration de manettes sont déjà fournis avec RetroBat.

### Emplacement des fichiers de mappage

Le mappage des contrôleurs spéciaux se trouve dans le dossier  `system\resources\inputmapping` de votre installation RetroBat, la liste actuelle se composant de :

* Contrôleur Saturn & Genesis
* Contrôleurs N64

### Contrôleurs & émulateurs actuellement supportés

Le tableau ci-dessous détaille les contrôleurs spéciaux actuellement supportés et les émulateurs pour lesquels RetroBat propose l'auto-configuration.

{% hint style="info" %}
Quand un contrôleur spécial est détecté, RetroBat ignorera complétement la configuration paramétré depuis RetroBat pour celui spécifique à la manette spéciale, de façon a utiliser le mappage original du système.
{% endhint %}



<table><thead><tr><th width="177">Type de contrôleur</th><th width="378">Contrôleur</th><th>Emulateurs</th></tr></thead><tbody><tr><td>Contrôleur N64</td><td>Nintendo Switch Online N64 Controller<br>(030000007e050000192000000000680c)</td><td>RetroArch<br>Ares<br>Bizhawk<br>Mupen64(RMG)<br>Simple64<br>Ship Of Harkinian</td></tr><tr><td></td><td>Mayflash N64 Adapter (2 joueurs)<br>(03000000d620000010a7000000000000)</td><td>RetroArch<br>Ares<br>Bizhawk<br>Mupen64(RMG)<br>Simple64<br>Ship Of Harkinian</td></tr><tr><td></td><td>Raphnet N64 Adapter (2 joueurs)<br>(030000009b2800006300000000000000)</td><td>RetroArch<br>Ares<br>Bizhawk<br>Mupen64(RMG)<br>Simple64<br>Ship Of Harkinian</td></tr><tr><td>Contrôleur Genesis </td><td>8BitDo M30 (mode xinput)<br>(030000005e040000e002000000007200)</td><td>RetroArch<br>Ares<br>Bizhawk<br>JGenesis<br>Kega-Fusion<br>Mednafen</td></tr><tr><td></td><td>8BitDo M30 (mode switch)<br>(030000007e0500000920000000006803)</td><td>RetroArch<br>Ares<br>Bizhawk<br>JGenesis<br>Kega-Fusion<br>Mednafen</td></tr><tr><td></td><td>8BitDo M30 (mode dinput)<br>(03000000c82d00005106000000000000)</td><td>RetroArch<br>Ares<br>Bizhawk<br>JGenesis<br>Kega-Fusion<br>Mednafen</td></tr><tr><td>Contrôleur Saturn</td><td>8BitDo M30 (mode xinput)<br>(030000005e040000e002000000007200)</td><td>RetroArch<br>Bizhawk<br>Kronos<br>Mednafen<br>SSF<br>YabaSanshiroRetroAr</td></tr><tr><td></td><td>8BitDo M30 (mode switch)<br>(030000007e0500000920000000006803)</td><td>RetroArch<br>Bizhawk<br>Kronos<br>SSF<br>YabaSanshiro</td></tr><tr><td></td><td>8BitDo M30 (mode dinput)<br>(03000000c82d00005106000000000000)</td><td>RetroArch<br>Bizhawk<br>Kronos<br>Mednafen<br>SSF<br>YabaSanshiro</td></tr></tbody></table>
