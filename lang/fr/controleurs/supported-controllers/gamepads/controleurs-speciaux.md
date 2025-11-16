# Contrôleurs spéciaux

Pour certains émulateurs, RetroBat est capable de configurer automatiquement certains contrôleurs spéciaux, comme des manettes N64 ou des manettes reprenant l'aspect des manettes Genesis.

Le mappage peut alors être défini par l'utilisateur dans des fichiers .json, certaines configurations de manettes sont déjà fournies avec RetroBat.

### Emplacement des fichiers de mappage

Le mappage des contrôleurs spéciaux se trouve dans le dossier  `system\resources\inputmapping` de votre installation RetroBat, la liste actuelle se composant de :

* Contrôleurs 3DO
* Contrôleurs Megadrive (Genesis)
* Contrôleurs Saturn
* Contrôleurs N64
* Contrôleurs Gamecube

### Type de contrôleurs & émulateurs actuellement supportés

Le tableau ci-dessous détaille les types de contrôleurs spéciaux actuellement supportés et les émulateurs pour lesquels RetroBat propose l'auto-configuration.

{% hint style="info" %}
Quand un contrôleur spécial est détecté, RetroBat ignorera complétement la configuration paramétré depuis RetroBat pour celui spécifique à la manette spéciale, de façon a utiliser le mappage original du système.
{% endhint %}

<table><thead><tr><th width="337.5333251953125">Type de contrôleur</th><th>Emulateurs</th></tr></thead><tbody><tr><td>Contrôleur N64</td><td>RetroArch<br>Ares<br>Bizhawk<br>Mupen64(RMG)<br>Simple64<br>Ship Of Harkinian</td></tr><tr><td>Contrôleur Megadrive/Genesis </td><td>RetroArch<br>Ares<br>Bizhawk<br>JGenesis<br>Kega-Fusion<br>Mednafen</td></tr><tr><td>Contrôleur Saturn</td><td>RetroArch<br>Bizhawk<br>Kronos<br>Mednafen<br>SSF<br>YabaSanshiro<br>Ymir</td></tr><tr><td>Contrôleurs GameCube</td><td>Dolphin (standalone)</td></tr><tr><td>Contrôleurs 3DO</td><td>RetroArch</td></tr></tbody></table>
