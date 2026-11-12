---
description: Sony
---

# Playstation 3

<div align="left"><figure><img src="../../../../.gitbook/assets/image (521).png" alt="" width="500"><figcaption></figcaption></figure></div>

## Présentation

La **PlayStation 3** sort fin 2006 au Japon et aux États-Unis, puis en mars 2007 en Europe. Sony y mise sur un processeur maison très puissant, le **Cell**, et sur le lecteur **Blu-ray**, qui en fait aussi un lecteur de films haute définition.

La console lance le PlayStation Network, les trophées et les jeux téléchargeables. Elle reste en production jusqu'en 2017 et s'est vendue à plus de 87 millions d'exemplaires. Des séries comme Uncharted, The Last of Us, Demon's Souls ou LittleBigPlanet y sont nées.

Son architecture très particulière en fait une machine difficile à émuler. **RPCS3**, démarré en 2011, fait aujourd'hui tourner la grande majorité de la ludothèque, à condition d'avoir un PC puissant.

{% embed url="https://fr.wikipedia.org/wiki/PlayStation_3" %}

## En bref

<table><thead><tr><th width="271.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\ps3</code></td></tr><tr><td><strong>Extensions</strong></td><td>.m3u .lnk .ps3 .iso .psn .7z .zip .rar .squashfs .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>rpcs3</td></tr><tr><td><strong>BIOS</strong></td><td>Firmware PS3 <code>PS3UPDAT.PUP</code> dans <code>bios</code> (installé au premier lancement)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>RPCS3</td></tr></tbody></table>

## Quel émulateur choisir ?

RPCS3 est le seul émulateur PS3 de RetroBat.

<table><thead><tr><th width="152">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>rpcs3</strong> (défaut)</td><td>Très grande compatibilité, résolution augmentée, trophées, nombreuses manettes reconnues.</td><td>Demande un processeur puissant. Le premier lancement de chaque jeu est long (compilation).</td></tr></tbody></table>

La liste de compatibilité de RPCS3 ([rpcs3.net](https://rpcs3.net/compatibility)) indique l'état de chaque jeu.

## BIOS

La PS3 n'a pas de BIOS à proprement parler, mais RPCS3 a besoin du **firmware** de la console.

<table><thead><tr><th width="252.75">Fichier</th><th width="329">Emplacement</th></tr></thead><tbody><tr><td><code>PS3UPDAT.PUP</code></td><td><code>bios</code></td></tr></tbody></table>

Le firmware se télécharge gratuitement sur le site de PlayStation (mise à jour du logiciel système de la PS3).

**Installation automatique** : au premier lancement d'un jeu, si le firmware n'est pas encore installé, RetroBat ouvre RPCS3 pour l'installer à partir de `bios\PS3UPDAT.PUP`. Une fois l'installation terminée, relancez le jeu.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (522).png" alt=""><figcaption></figcaption></figure></div>

Si le firmware n'est ni installé ni présent dans `bios`, RetroBat affiche un message d'erreur et le jeu ne démarre pas.

## Quel format de jeu ?

<table><thead><tr><th width="163.25">Format</th><th width="217">Pour quoi ?</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>Dossier <code>.ps3</code></strong></td><td>Jeu sur disque</td><td>Le jeu copié en dossier, renommé avec <code>.ps3</code> à la fin : <code>roms\ps3\Mon jeu.ps3\PS3_GAME\USRDIR\EBOOT.BIN</code>.</td></tr><tr><td><strong>.iso</strong></td><td>Jeu sur disque</td><td>Image du disque, lue directement par RPCS3.</td></tr><tr><td><strong>.psn</strong></td><td>Jeu PSN</td><td>Fichier texte qui contient l'identifiant d'un jeu installé dans RPCS3 (voir <a href="playstation-3.md#ajouter-un-jeu-psn">Guides</a>).</td></tr><tr><td>.m3u</td><td>Jeu PSN ou jeu rangé ailleurs</td><td>Fichier texte dont la première ligne indique où se trouve le jeu (voir <a href="playstation-3.md#utiliser-un-fichier-.m3u">Guides</a>).</td></tr><tr><td>.squashfs</td><td>Jeu sur disque ou PSN</td><td>Image compressée, montée sans extraction.</td></tr><tr><td>.7z .zip .rar</td><td>Jeu sur disque</td><td>Extrait avant le lancement : lent pour les gros jeux.</td></tr><tr><td>.lnk</td><td>Raccourci Windows</td><td>Lancé tel quel.</td></tr><tr><td>.decomp</td><td>Portage PC</td><td>Voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

Les jeux PSN (fichiers `.pkg`) doivent d'abord être installés dans RPCS3.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes, jusqu'à 7 joueurs. Les boutons sont placés comme sur la manette de la PS3 : **SUD** = Croix, **EST** = Rond, **OUEST** = Carré, **NORD** = Triangle.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (523).png" alt="" width="338"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="310.25">Manette</th><th>Pilote utilisé dans RPCS3</th></tr></thead><tbody><tr><td>DualSense (PS5)</td><td>DualSense</td></tr><tr><td>DualShock 4 (PS4)</td><td>DualShock 4</td></tr><tr><td>DualShock 3 (PS3)</td><td>DualShock 3</td></tr><tr><td>Manettes XInput (Xbox)</td><td>XInput</td></tr><tr><td>Autres manettes</td><td>SDL</td></tr></tbody></table>

Options utiles, dans **CONTRÔLES** :

| Option                                                               | Effet                                                                                   |
| -------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| **ACTIVER LES VIBRATIONS**                                           | Les vibrations sont désactivées par défaut.                                             |
| **BOUTON DE CONFIRMATION**                                           | Croix ou Rond pour valider dans les fenêtres système. Sur AUTO, suit la région choisie. |
| **INVERSER LES BOUTONS A/B/X/Y**                                     | Échange les boutons de façade.                                                          |
| **GESTIONNAIRE PS MOVE**, **TYPE DE CAMÉRA**                         | Pour les jeux PlayStation Move et caméra.                                               |
| **BUZZERS BUZZ!**, **PLATINE DJ HERO**, **GUITARE GUITAR HERO LIVE** | Émule ces accessoires avec vos manettes.                                                |

**Boutons sensibles à la pression** : la manette de la PS3 mesure la force d'appui sur ses boutons, ce que certains jeux utilisent (Gran Turismo par exemple). RPCS3 ne le gère qu'avec une vraie DualShock 3 ou Sixaxis et le pilote DsHidMini (voir le [wiki de RPCS3, « Controller Configuration »](https://wiki.rpcs3.net/index.php?title=Help:Controller_Configuration)).

### Pistolets

L'option **PISTOLETS > ACTIVER LES PISTOLETS** propose deux modes :

<table><thead><tr><th width="167.75">Mode</th><th>Usage</th></tr></thead><tbody><tr><td><strong>SOURIS BRUTE</strong></td><td>Jeux GunCon 3 (Time Crisis 4…). Jusqu'à 2 pistolets, branchés par défaut sur les ports 3 et 4 de la console. L'option <strong>UTILISER LE PORT 1 POUR LE GUNCON</strong> les place sur les ports 1 et 2.</td></tr><tr><td><strong>PS EYE</strong></td><td>Jeux PlayStation Move : le pistolet remplace la manette Move.</td></tr></tbody></table>

Le logiciel Sinden est démarré automatiquement si un pistolet Sinden est branché.

Pour brancher et régler un pistolet dans RetroBat, voir la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/).

### Raccourcis

<table><thead><tr><th width="313">Raccourci</th><th width="270.75">Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>ÉCHAP</td></tr><tr><td>HOTKEY + L3</td><td>Pause</td><td>P</td></tr><tr><td>HOTKEY + R3</td><td>Capture d'écran</td><td>F8</td></tr><tr><td>SELECT + SUD, ou bouton PS / Guide</td><td>Bouton PS (menu Home de RPCS3)</td><td>F1</td></tr><tr><td>—</td><td>Plein écran</td><td>F</td></tr><tr><td>—</td><td>Couper le son</td><td>M</td></tr><tr><td>—</td><td>Sauvegarde instantanée de RPCS3 (non gérée par RetroBat)</td><td>F2</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="251.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Firmware à installer</td><td><code>bios\PS3UPDAT.PUP</code></td></tr><tr><td>Disque dur de la PS3 : jeux PSN, sauvegardes, trophées</td><td><code>saves\ps3\rpcs3\dev_hdd0</code></td></tr><tr><td>Jeux PSN installés</td><td><code>saves\ps3\rpcs3\dev_hdd0\game</code></td></tr><tr><td>Sauvegardes des jeux</td><td><code>saves\ps3\rpcs3\dev_hdd0\home\00000001\savedata</code></td></tr><tr><td>Trophées</td><td><code>saves\ps3\rpcs3\dev_hdd0\home\00000001\trophy</code></td></tr><tr><td>Firmware installé</td><td><code>emulators\rpcs3\dev_flash</code></td></tr><tr><td>Configuration de RPCS3</td><td><code>emulators\rpcs3\config\config.yml</code></td></tr><tr><td>Configurations par jeu de RPCS3</td><td><code>emulators\rpcs3\config\custom_configs</code></td></tr><tr><td>Configuration des manettes</td><td><code>emulators\rpcs3\config\input_configs\global\Retrobat.yml</code></td></tr><tr><td>Réglages de l'interface</td><td><code>emulators\rpcs3\GuiConfigs\CurrentSettings.ini</code></td></tr><tr><td>Correctifs de jeux (patches)</td><td><code>emulators\rpcs3\patches</code></td></tr><tr><td>Cache de compilation des jeux</td><td><code>emulators\rpcs3\cache</code></td></tr><tr><td>Captures d'écran</td><td><code>emulators\rpcs3\screenshots</code></td></tr></tbody></table>

Si le dossier `saves\ps3\rpcs3` n'existe pas, RetroBat utilise le dossier `dev_hdd0` de l'émulateur (`emulators\rpcs3\dev_hdd0`).

## Guides

### Ajouter un jeu sur disque

1. Copiez le dossier du jeu dans `roms\ps3`. Il contient un dossier `PS3_GAME`.
2. Renommez-le en ajoutant `.ps3` à la fin, par exemple `Mon jeu.ps3`.
3. Mettez à jour la liste des jeux de RetroBat.

Une image `.iso` se place telle quelle dans `roms\ps3`.

### Ajouter un jeu PSN

1. Lancez `rpcs3.exe` depuis le dossier `emulators\rpcs3`.
2. Dans le menu **File**, choisissez **Install Packages/Raps/Edats** et sélectionnez le fichier `.pkg` du jeu (et son fichier `.rap` s'il en a un).
3. Le jeu apparaît dans la liste de RPCS3. Notez son identifiant, dans la colonne **Serial** (par exemple `NPEB00623`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (524).png" alt=""><figcaption></figcaption></figure></div>

4. Dans `roms\ps3`, créez un fichier texte au nom du jeu avec l'extension `.psn`, par exemple `Mon jeu.psn`.
5. Écrivez-y seulement l'identifiant :

```
NPEB00623
```

### Utiliser un fichier .m3u

Un fichier `.m3u` est un fichier texte dont la première ligne indique le jeu à lancer. Elle peut contenir :

<table><thead><tr><th width="397.75">Première ligne</th><th>Jeu lancé</th></tr></thead><tbody><tr><td><code>GAMEID:NPEB01234</code></td><td>Le jeu installé qui porte cet identifiant</td></tr><tr><td><code>\dev_hdd0\game\NPEB01234\USRDIR\EBOOT.BIN</code></td><td>Chemin cherché dans <code>roms\ps3</code>, puis <code>saves\ps3\rpcs3</code>, puis <code>emulators\rpcs3</code></td></tr><tr><td><code>ROMPATH\Mon jeu\PS3_GAME\USRDIR\EBOOT.BIN</code></td><td>Chemin à partir de <code>roms\ps3</code></td></tr><tr><td><code>SAVESPATH\dev_hdd0\game\NPEB01234\USRDIR\EBOOT.BIN</code></td><td>Chemin à partir de <code>saves\ps3\rpcs3</code></td></tr><tr><td><code>EMULATORPATH\dev_hdd0\game\NPEB01234\USRDIR\EBOOT.BIN</code></td><td>Chemin à partir de <code>emulators\rpcs3</code></td></tr><tr><td><code>D:\Jeux\Mon jeu\PS3_GAME\USRDIR\EBOOT.BIN</code></td><td>Chemin complet</td></tr></tbody></table>

Le fichier `example-to-edit.m3u.txt` du dossier `roms\ps3` sert de modèle. L'outil **BatGui** peut créer ces fichiers pour les jeux déjà installés (menu M3U Creator) : voir la page [**BatGui**](../../../../utilisation-avancee/batgui.md).

### Garder vos réglages par jeu faits dans RPCS3

Par défaut, RetroBat applique les options réglées dans son menu et ignore les configurations par jeu créées dans RPCS3. L'option **ÉMULATION > CONFIGURATION À UTILISER** change ce comportement :

<table><thead><tr><th width="279">Choix</th><th>Effet</th></tr></thead><tbody><tr><td><strong>PAR DÉFAUT</strong></td><td>Options de RetroBat, configurations par jeu de RPCS3 ignorées.</td></tr><tr><td><strong>OVERRIDE DU JEU</strong></td><td>La configuration par jeu de RPCS3 est utilisée quand elle existe.</td></tr><tr><td><strong>CONFIG YML UNIQUEMENT</strong></td><td>Seul le fichier <code>config.yml</code> est utilisé.</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (525).png" alt=""><figcaption></figcaption></figure></div>

### Installer le firmware à la main

1. Lancez `rpcs3.exe` depuis le dossier `emulators\rpcs3`.
2. Dans le menu **File**, choisissez **Install Firmware**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (526).png" alt=""><figcaption></figcaption></figure></div>

3. Sélectionnez le fichier `PS3UPDAT.PUP`.

## Problèmes connus

| Problème                                                                  | Solution                                                                                                                                 |
| ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Message « PS3 firmware is not installed »                                 | Placez `PS3UPDAT.PUP` dans `bios`, ou installez le firmware à la main (voir [Guides](playstation-3.md#installer-le-firmware-a-la-main)). |
| Au premier lancement, RPCS3 installe le firmware au lieu de lancer le jeu | C'est normal. Relancez le jeu une fois l'installation terminée.                                                                          |
| Le premier lancement d'un jeu est très long                               | RPCS3 compile le jeu la première fois. Les lancements suivants sont rapides.                                                             |
| Pas de vibrations                                                         | Activez **ACTIVER LES VIBRATIONS**.                                                                                                      |
| Croix et Rond sont inversés pour valider                                  | Réglez **BOUTON DE CONFIRMATION**.                                                                                                       |
| Manette Xbox mal reconnue                                                 | Activez **PILOTES > FORCER LE PILOTE SDL POUR LES MANETTES**.                                                                            |
| Mes réglages par jeu faits dans RPCS3 sont ignorés                        | Choisissez **CONFIGURATION À UTILISER** : OVERRIDE DU JEU.                                                                               |
| Un jeu `.psn` ou `.m3u` ne se lance pas                                   | Vérifiez l'identifiant, et que le jeu est bien installé dans `saves\ps3\rpcs3\dev_hdd0\game`.                                            |
