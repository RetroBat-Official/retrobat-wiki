# Configuration des touches Dolphin

## Présentation

Les jeux GameCube et Wii utilisent la manette de façons très différentes : manette GameCube, Wiimote tenue à la verticale ou à l'horizontale, Nunchuk, manette classique… RetroBat règle Dolphin automatiquement, mais certains cas demandent un réglage à part.

Cette page explique deux choses :

* comment faire reconnaître une manette ou un adaptateur particulier, avec le fichier `GCControllers.json` ;
* comment utiliser votre propre profil de manette Dolphin pour un jeu.

{% hint style="info" %}
Toutes les informations ci-dessous proviennent du wiki Dolphin :

[https://wiki.dolphin-emu.org/index.php?title=GameINI\_(Controller\_Settings)](https://wiki.dolphin-emu.org/index.php?title=GameINI_\(Controller_Settings\))
{% endhint %}

## Configuration automatique

RetroBat configure les manettes à chaque lancement. Les réglages se trouvent dans les options avancées du système, sous-menu **CONTRÔLES** :

* **GameCube** : **DISPOSITION DES BOUTONS** et **TYPE DE CONTRÔLEUR JOUEUR 1** (à 4). Voir la page [**GameCube**](../../systemes-and-emulateurs/supported-game-systems/consoles-de-jeu/nintendo-consoles-de-jeu/gamecube.md#controles).

<div align="left"><figure><img src="../../.gitbook/assets/image (541).png" alt=""><figcaption></figcaption></figure></div>

* **Wii** : **TYPE DE WIIMOTE** et **TYPE DE WIIMOTE ÉMULÉE**, pour choisir la façon de tenir la Wiimote, et les vraies Wiimotes avec une DolphinBar. Voir la page [**Wii**](../../systemes-and-emulateurs/supported-game-systems/consoles-de-jeu/nintendo-consoles-de-jeu/wii.md#controles).

<div align="left"><figure><img src="../../.gitbook/assets/image (540).png" alt=""><figcaption></figcaption></figure></div>

Dans la plupart des cas, ces options suffisent.

## Manettes et adaptateurs particuliers (GCControllers.json)

Certains adaptateurs de manettes GameCube, par exemple ceux de Mayflash ou de raphnet, se présentent à Windows comme une manette ordinaire. Leurs boutons ne sont alors pas à la bonne place avec la configuration automatique.

Le fichier `GCControllers.json` donne à RetroBat le mapping exact de ces adaptateurs. RetroBat le reconnaît par son identifiant (GUID) et l'applique à la place de la configuration automatique.

RetroBat fournit ce fichier dans `system\resources\inputmapping`, avec deux adaptateurs : **MAYFLASH GameCube Controller Adapter** et **raphnet technologies Dual Gamecube to USB v3.6**.

Pour un adaptateur qui fonctionne avec le pilote Zadig et le mode **ADAPTATEUR GAMECUBE** de Dolphin, ce fichier n'est pas utile : voir la page [**GameCube**](../../systemes-and-emulateurs/supported-game-systems/consoles-de-jeu/nintendo-consoles-de-jeu/gamecube.md#utiliser-une-vraie-manette-gamecube-adaptateur).

### Ajouter un adaptateur

1. Copiez `GCControllers.json` de `system\resources\inputmapping` vers `user\inputmapping`. Votre copie remplace alors entièrement le fichier de RetroBat : gardez les adaptateurs existants dedans.
2. Ajoutez une entrée pour votre adaptateur, sur le modèle de celles du fichier :

```json
{
    "Emulator": "dolphin",
    "Name": "MAYFLASH GameCube Controller Adapter",
    "Guid": "03000000790000004318000000016800",
    "Driver": "DInput",
    "Mapping": {
        "Buttons/A": "`Button 1`",
        "Buttons/B": "`Button 2`",
        "Main Stick/Up": "`Axis Y-`"
    },
    "HotKeyMapping": {
        "General/Exit": "@(`Button 9`+`Button 7`)"
    },
    "ControllerInfo": {
        "needActivationSwitch": "false"
    }
}
```

<table><thead><tr><th width="162.75">Champ</th><th>Contenu</th></tr></thead><tbody><tr><td><code>Emulator</code></td><td><code>dolphin</code> pour Dolphin, <code>libretro</code> pour lr-dolphin.</td></tr><tr><td><code>Name</code></td><td>Nom exact de l'adaptateur tel que Dolphin l'affiche dans sa liste de périphériques. RetroBat s'en sert pour désigner le périphérique à Dolphin : un nom approximatif ne fonctionne pas.</td></tr><tr><td><code>Guid</code></td><td>Identifiant de l'adaptateur (voir plus bas).</td></tr><tr><td><code>Driver</code></td><td>Pilote de Dolphin à utiliser : <code>SDL</code> (par défaut), <code>DInput</code>…</td></tr><tr><td><code>Mapping</code></td><td>Les lignes à écrire dans <code>GCPadNew.ini</code> pour ce port.</td></tr><tr><td><code>HotKeyMapping</code></td><td>Les raccourcis de Dolphin à écrire dans <code>Hotkeys.ini</code>, quand l'adaptateur est utilisé par le joueur 1. Ils remplacent alors les raccourcis de RetroBat.</td></tr><tr><td><code>ControllerInfo</code></td><td><code>needActivationSwitch</code> : <code>true</code> pour que le mapping ne s'applique que si l'option <strong>UTILISER UNE MANETTE DE TYPE GAMECUBE</strong> est activée, <code>false</code> pour qu'il s'applique toujours.</td></tr></tbody></table>

Avec Dolphin, le champ `ControllerInfo` doit être présent, ainsi que `HotKeyMapping` pour l'adaptateur du joueur 1 : sinon le mapping n'est pas appliqué.

### Trouver le GUID et le mapping

**Le GUID** : lancez un jeu GameCube avec l'adaptateur branché, puis ouvrez le fichier `emulationstation\emulatorLauncher.log`. Cherchez la ligne `Checking specific Gamecube mapping for controller` : le GUID est à la fin de cette ligne.

**Le mapping** : réglez une fois l'adaptateur à la main dans Dolphin.

1. Désactivez **AUTOCONFIGURER LES MANETTES** pour le système GameCube.
2. Lancez `Dolphin.exe` depuis le dossier `emulators\dolphin-emu`.
3. Ouvrez **Controllers**, choisissez **Standard Controller** pour le port 1, puis **Configure**.
4. Choisissez l'adaptateur dans la liste **Device** et réglez chaque bouton.
5. Fermez Dolphin et ouvrez `emulators\dolphin-emu\User\Config\GCPadNew.ini` : la section `[GCPad1]` contient les lignes à recopier dans `Mapping`, et la ligne `Device` donne le pilote et le nom exact (`DInput/0/MAYFLASH GameCube Controller Adapter`).
6. Réactivez **AUTOCONFIGURER LES MANETTES**.

<div align="left"><figure><img src="../../.gitbook/assets/image (542).png" alt=""><figcaption></figcaption></figure></div>

## Profil de manette par jeu

Un profil Dolphin est un réglage complet de la manette, enregistré sous un nom. Associé à un jeu, il remplace la configuration de RetroBat pour ce jeu uniquement. C'est utile pour un jeu qui demande un réglage très particulier.

Cette méthode ne vaut que pour Dolphin, pas pour lr-dolphin.

### Étape 1 : créer le profil

1. Lancez `Dolphin.exe` depuis le dossier `emulators\dolphin-emu`.
2. Ouvrez **Controllers**, puis **Configure** à côté du port à régler :
   * **GameCube Controllers** pour un jeu GameCube ;
   * **Wii Remotes** (Wiimote émulée) pour un jeu Wii.

<div align="left"><figure><img src="../../.gitbook/assets/image (543).png" alt=""><figcaption></figcaption></figure></div>

3. Choisissez votre manette dans la liste **Device** et réglez les boutons.
4. Dans la zone **Profile**, tapez un nom, par exemple `Mario Kart DD`, puis cliquez sur **Save**.

<div align="left"><figure><img src="../../.gitbook/assets/image (544).png" alt=""><figcaption></figcaption></figure></div>

Le profil garde la manette choisie dans **Device**. Il ne fonctionnera qu'avec cette manette.

### Étape 2 : associer le profil au jeu

1. Toujours dans Dolphin, faites un clic droit sur le jeu dans la liste, puis **Properties**.
2. Ouvrez l'onglet **Game Config**, puis **Editor**.
3. Dans la zone **User Config**, ajoutez :

```ini
[Controls]
PadProfile1 = Mario Kart DD
```

<table><thead><tr><th width="311.5">Ligne</th><th>Pour</th></tr></thead><tbody><tr><td><code>PadProfile1</code> à <code>PadProfile4</code></td><td>Manette GameCube du joueur 1 à 4</td></tr><tr><td><code>WiimoteProfile1</code> à <code>WiimoteProfile4</code></td><td>Wiimote du joueur 1 à 4</td></tr></tbody></table>

Le nom après le signe `=` doit être exactement celui de l'étape 1.

<div align="left"><figure><img src="../../.gitbook/assets/image (545).png" alt=""><figcaption></figcaption></figure></div>

4. Fermez Dolphin. Le profil est chargé à chaque lancement du jeu depuis RetroBat.

Dolphin enregistre ce réglage dans `emulators\dolphin-emu\User\GameSettings\<ID du jeu>.ini`, par exemple `GALE01.ini` pour Super Smash Bros. Melee. Pour revenir à la configuration de RetroBat, retirez la section `[Controls]` de ce fichier.

## Dossiers

<table><thead><tr><th width="265.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Fichier des adaptateurs fourni par RetroBat</td><td><code>system\resources\inputmapping\GCControllers.json</code></td></tr><tr><td>Votre fichier des adaptateurs</td><td><code>user\inputmapping\GCControllers.json</code></td></tr><tr><td>Réglages des manettes écrits par RetroBat</td><td><code>emulators\dolphin-emu\User\Config\GCPadNew.ini</code> (GameCube), <code>WiimoteNew.ini</code> (Wii), <code>Hotkeys.ini</code> (raccourcis)</td></tr><tr><td>Profils GameCube</td><td><code>emulators\dolphin-emu\User\Config\Profiles\GCPad</code></td></tr><tr><td>Profils Wiimote</td><td><code>emulators\dolphin-emu\User\Config\Profiles\Wiimote</code></td></tr><tr><td>Réglages par jeu</td><td><code>emulators\dolphin-emu\User\GameSettings</code></td></tr><tr><td>Journal de RetroBat (GUID des manettes)</td><td><code>emulationstation\emulatorLauncher.log</code></td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="266.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Mes réglages faits dans Dolphin disparaissent au lancement suivant</td><td>RetroBat réécrit <code>GCPadNew.ini</code> et <code>WiimoteNew.ini</code> à chaque lancement. Utilisez un profil par jeu, ou désactivez <strong>AUTOCONFIGURER LES MANETTES</strong>.</td></tr><tr><td>Mon profil n'est pas chargé</td><td>Vérifiez que le nom dans <code>[Controls]</code> est identique à celui du profil, et que le profil a été créé avec la manette que vous utilisez.</td></tr><tr><td>Un jeu ne suit plus certaines options de RetroBat</td><td>Le fichier <code>&#x3C;ID du jeu>.ini</code> de <code>emulators\dolphin-emu\User\GameSettings</code> peut remplacer d'autres réglages que les manettes. Retirez-en les lignes concernées.</td></tr><tr><td>Mon adaptateur n'est pas reconnu</td><td>Vérifiez le GUID dans <code>emulatorLauncher.log</code> et le nom exact dans Dolphin. Si <code>needActivationSwitch</code> vaut <code>true</code>, activez <strong>UTILISER UNE MANETTE DE TYPE GAMECUBE</strong>.</td></tr></tbody></table>
