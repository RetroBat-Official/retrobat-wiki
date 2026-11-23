---
description: Nintendo
---

# Switch

<div align="left"><figure><img src="../../../../.gitbook/assets/image (709).png" alt="" width="420"><figcaption></figcaption></figure></div>

## Présentation

La **Nintendo Switch** est une console hybride sortie en mars 2017 : elle se branche sur la télévision ou s'emporte comme une console portable. Ses manettes amovibles, les **Joy-Con**, s'utilisent ensemble ou séparément, et la **Pro Controller** offre une manette classique. Avec plus de 150 millions d'exemplaires, c'est l'une des consoles les plus vendues de l'histoire.

Parmi ses jeux marquants : The Legend of Zelda: Breath of the Wild et Tears of the Kingdom, Super Mario Odyssey, Mario Kart 8 Deluxe, Animal Crossing: New Horizons, Super Smash Bros. Ultimate ou Splatoon.

RetroBat prend en charge **Eden** (par défaut), **Ryujinx**, **Citron**, **Sudachi** et **Yuzu**. Ces émulateurs ne sont pas fournis avec RetroBat : il faut les installer à la main (voir [**Installer les émulateurs**](switch.md#installer-les-emulateurs)).

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_Switch" %}

## En bref

<table><thead><tr><th width="265.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\switch</code></td></tr><tr><td><strong>Extensions</strong></td><td>.nso .nro .nca .xci .nsp .kip .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>eden</td></tr><tr><td><strong>BIOS</strong></td><td><code>prod.keys</code> et firmware de votre console, dans le dossier de chaque émulateur</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non (Ryujinx : multijoueur local sans fil émulé)</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur         | Version prise en charge                                                                | Points forts                                                                                                                                                      | Limites                                       |
| ----------------- | -------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| **eden** (défaut) | [eden-emu.dev](https://eden-emu.dev/)                                                  | Suite active de Yuzu : bonnes performances, mises à jour et DLC chargés depuis `roms\switchupdates` sans installation, sauvegardes possibles dans `saves\switch`. |                                               |
| **ryujinx**       | Ryubing : [git.ryujinx.app/projects/Ryubing](https://git.ryujinx.app/projects/Ryubing) | Émulateur distinct, écrit à partir de zéro. Multijoueur local sans fil émulé (**RÉSEAU > MODE MULTI-JOUEURS**).                                                   | Mises à jour et DLC à ajouter dans Ryujinx.   |
| **citron**        | Citron-Neo : [github.com/citron-neo/emulator](https://github.com/citron-neo/emulator)  | Autre suite de Yuzu. Mises à jour et DLC depuis `roms\switchupdates`, sauvegardes possibles dans `saves\switch`.                                                  |                                               |
| **sudachi**       |                                                                                        | Suite de Yuzu.                                                                                                                                                    | Mises à jour et DLC à installer dans la NAND. |
| **yuzu**          | Dernière version                                                                       | Émulateur d'origine dont viennent Eden, Citron et Sudachi.                                                                                                        | Projet arrêté en 2024 : n'évolue plus.        |

## Installer les émulateurs

RetroBat ne fournit pas les émulateurs Switch, ni les fichiers de la console. Il faut, pour chaque émulateur utilisé :

1. copier l'émulateur dans son dossier de RetroBat ;
2. ajouter les clés de **votre** console (`prod.keys`) ;
3. installer le firmware de **votre** console.

Sans les clés et le firmware, les jeux ne se lancent pas.

### Ryujinx

1. Téléchargez la version Windows de Ryujinx (Ryubing) et décompressez l'archive.
2. Copiez **le contenu** du dossier obtenu dans `emulators\ryujinx` : `Ryujinx.exe` doit être directement dans `emulators\ryujinx`, pas dans un sous-dossier.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (711).png" alt=""><figcaption></figcaption></figure></div>

3. Vérifiez que le fichier `Configure Ryujinx.bat` est dans `emulators\ryujinx`. S'il manque, copiez-le depuis `system\templates\ryujinx`.
4. Lancez `Configure Ryujinx.bat` (double-clic). Il ouvre Ryujinx avec le dossier de données de RetroBat, `saves\switch\ryujinx\portable`, et le crée s'il n'existe pas. Vous pouvez aussi ouvrir Ryujinx depuis le menu des émulateurs de RetroBat, qui fait la même chose.
5. Quittez Ryujinx, placez `prod.keys` (et `title.keys` si vous l'avez) dans `saves\switch\ryujinx\portable\system`, puis relancez `Configure Ryujinx.bat`.
6. Installez le firmware : **Tools > Install Firmware**, puis **Install a firmware from XCI or ZIP** (archive du firmware) ou **Install a firmware from a directory** (dossier de fichiers `.nca`).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (712).png" alt=""><figcaption></figcaption></figure></div>

8. Quittez Ryujinx. Il est prêt : lancez les jeux depuis RetroBat.

{% hint style="danger" %}
Cette étape est indispensable pour que Ryujinx fonctionne avec RetroBat.

Ouvrez toujours Ryujinx avec `Configure Ryujinx.bat` ou depuis le menu des émulateurs de RetroBat. Lancé directement par `Ryujinx.exe`, il range ses données dans un autre dossier : les clés, le firmware et les réglages faits là ne sont pas vus par RetroBat.
{% endhint %}

### Eden, Citron, Sudachi, Yuzu

1. Téléchargez la version Windows de l'émulateur et décompressez l'archive.
2. Copiez **le contenu** du dossier obtenu dans `emulators\<émulateur>` (`emulators\eden`, `emulators\citron`, `emulators\sudachi` ou `emulators\yuzu`) : l'exécutable (`eden.exe`, `citron.exe`, `sudachi.exe`, `yuzu.exe`) doit être directement dans ce dossier.
3. Créez le sous-dossier `user` dans le dossier de l'émulateur (par exemple `emulators\eden\user`). L'émulateur range alors toutes ses données dans ce dossier (mode portable). Sans lui, il les range dans `%APPDATA%`, où RetroBat ne les trouve pas. RetroBat le crée au premier lancement d'un jeu, mais il doit exister avant la première ouverture de l'émulateur.
4. Placez `prod.keys` (et `title.keys` si vous l'avez) dans `emulators\<émulateur>\user\keys`.
5. Installez le firmware :
   * soit depuis l'émulateur : ouvrez-le depuis le menu des émulateurs de RetroBat, puis **Tools > Install Firmware** ;
   * soit en copiant les fichiers `.nca` du firmware dans `emulators\<émulateur>\user\nand\system\Contents\registered`.
6. Quittez l'émulateur : lancez les jeux depuis RetroBat.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (713).png" alt=""><figcaption></figcaption></figure></div>

## BIOS

Résumé des fichiers de **votre** console à fournir (voir [**Installer les émulateurs**](switch.md#installer-les-emulateurs) pour la procédure complète) :

<table data-header-hidden><thead><tr><th width="154.5"></th><th></th><th></th></tr></thead><tbody><tr><td>Émulateur</td><td>Clés (<code>prod.keys</code>, <code>title.keys</code>)</td><td>Firmware</td></tr><tr><td>Eden, Citron, Sudachi, Yuzu</td><td><code>emulators\&#x3C;émulateur>\user\keys</code></td><td><strong>Tools > Install Firmware</strong>, ou fichiers <code>.nca</code> dans <code>emulators\&#x3C;émulateur>\user\nand\system\Contents\registered</code></td></tr><tr><td>Ryujinx</td><td><code>saves\switch\ryujinx\portable\system</code></td><td><strong>Tools > Install Firmware</strong> (Ryujinx ouvert avec <code>Configure Ryujinx.bat</code>)</td></tr></tbody></table>

Le firmware doit être de la même version que les clés, ou plus ancien. Après une mise à jour du firmware, mettez aussi à jour `prod.keys`.

## Quel format de jeu ?

<table><thead><tr><th width="222.75">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.xci</strong></td><td>Image de la cartouche.</td></tr><tr><td><strong>.nsp</strong></td><td>Jeu téléchargé (eShop). Les mises à jour et les DLC sont aussi des <code>.nsp</code>.</td></tr><tr><td><strong>.nca</strong> / <strong>.nso</strong> / <strong>.nro</strong> / <strong>.kip</strong></td><td>Fichiers système ou programmes homebrew.</td></tr><tr><td><strong>.decomp</strong></td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

Les mises à jour et les DLC ne sont pas des jeux : ne les mettez pas dans `roms\switch` (voir [**Mises à jour et DLC**](switch.md#mises-a-jour-et-dlc)).

## Contrôles

### Configuration automatique

RetroBat configure les manettes pour tous les émulateurs, en **Pro Controller** par défaut. **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** (à 4) choisit une autre manette, selon l'émulateur : DOUBLE JOY-CON, JOY-CON GAUCHE, JOY-CON DROIT, GAMECUBE, ou PORTABLE (joueur 1, manettes fixées à la console).

Les boutons sont placés comme sur une manette Nintendo (position, pas lettre) :

<table><thead><tr><th width="275.25">Manette RetroBat</th><th>Switch</th></tr></thead><tbody><tr><td>START</td><td>+</td></tr><tr><td>SELECT</td><td>−</td></tr><tr><td>Croix</td><td>Croix</td></tr><tr><td>Stick gauche / stick droit</td><td>Stick gauche / stick droit</td></tr><tr><td>SUD</td><td>B (ou A si inversé)</td></tr><tr><td>EST</td><td>A (ou B si inversé)</td></tr><tr><td>OUEST</td><td>Y (ou X si inversé)</td></tr><tr><td>NORD</td><td>X (ou Y si inversé)</td></tr><tr><td>L1 / R1</td><td>L / R</td></tr><tr><td>L2 / R2</td><td>ZL / ZR</td></tr><tr><td>L3 / R3</td><td>Clic du stick gauche / droit</td></tr></tbody></table>

L'option **CONTRÔLES > INVERSER LES BOUTONS A/B/X/Y** inverse les boutons (A sur SUD, selon les lettres imprimées). Avec Ryujinx, les manettes Nintendo sont inversées d'office.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (714).png" alt=""><figcaption></figcaption></figure></div>

Autres options utiles :

* **ÉMULATION > MODE PORTABLE** fait tourner la console en mode portable (résolution plus basse, plus rapide) au lieu du mode TV.
* **CONTRÔLES > DÉSACTIVER L'APPLET DES CONTRÔLEURS** évite la fenêtre de choix des manettes que certains jeux ouvrent au démarrage (activée par défaut avec Eden).
* **CONTRÔLES > ACTIVER LE MOTION CONTROL** (Eden) / **DÉTECTION DES MOUVEMENTS** (Ryujinx) utilise le gyroscope des manettes qui en ont un.

### Raccourcis

| Raccourci      | Eden, Sudachi, Yuzu | Ryujinx         | Citron  |
| -------------- | ------------------- | --------------- | ------- |
| HOTKEY + START | Quitter             | Quitter         | Quitter |
| HOTKEY + SUD   | Pause               | Pause           | —       |
| HOTKEY + R3    | Capture d'écran     | Capture d'écran | —       |
| HOTKEY + L3    | Plein écran         | —               | —       |

Avec Eden, Sudachi et Yuzu, ce sont des raccourcis de l'émulateur réglés par RetroBat, avec SELECT comme bouton HOTKEY. Aucun émulateur n'a de sauvegardes instantanées : sauvegardez dans le jeu. Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="289">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\switch</code></td></tr><tr><td>Mises à jour et DLC (Eden, Citron)</td><td><code>roms\switchupdates</code></td></tr><tr><td>Données de l'émulateur</td><td><strong>Ryujinx</strong> : <code>saves\switch\ryujinx\portable</code><br><strong>Eden, Citron, Sudachi, Yuzu</strong> : <code>emulators\&#x3C;émulateur>\user</code></td></tr><tr><td>Fichier de configuration</td><td><strong>Ryujinx</strong> : <code>saves\switch\ryujinx\portable\Config.json</code><br><strong>Eden, Citron, Sudachi, Yuzu</strong> : <code>emulators\&#x3C;émulateur>\user\config\qt-config.ini</code></td></tr><tr><td>Sauvegardes (Eden, Citron, avec l'option ci-dessous)</td><td><code>saves\switch</code></td></tr><tr><td>Captures d'écran (Eden)</td><td><code>screenshots\eden</code></td></tr></tbody></table>

Si `saves\switch\ryujinx\portable` n'existe pas, Ryujinx utilise `emulators\ryujinx\portable`.

Pour Eden et Citron, les sauvegardes peuvent aller dans le dossier `saves\switch` de RetroBat au lieu du dossier de l'émulateur. Activez l'option **SAUVEGARDES DANS LE DOSSIER SAVES DE RETROBAT**, dans **MENU PRINCIPAL > PARAMÈTRES DES JEUX** (rubrique **NINTENDO SWITCH**) :

## Mises à jour et DLC

Tous les émulateurs gèrent les mises à jour et les DLC des jeux. Ce sont des fichiers `.nsp`, à extraire de votre console.

### Eden et Citron : dossier roms\switchupdates

Eden et Citron chargent les mises à jour et les DLC depuis un dossier, sans les installer. RetroBat leur ajoute le dossier `roms\switchupdates` : placez-y les fichiers `.nsp`.

### Eden, Citron, Sudachi, Yuzu : installation dans la NAND

1. Ouvrez l'émulateur depuis le menu des émulateurs de RetroBat.
2. Choisissez **File > Install Files to NAND...**

<div align="left"><figure><img src="../../../../.gitbook/assets/image (715).png" alt=""><figcaption></figcaption></figure></div>

3. Sélectionnez le fichier `.nsp` de la mise à jour ou du DLC et validez.

### Ryujinx

1. Ouvrez Ryujinx avec `Configure Ryujinx.bat` ou depuis le menu des émulateurs de RetroBat.
2. Faites un clic droit sur le jeu et choisissez **Manage Title Updates** ou **Manage DLC**.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (716).png" alt=""><figcaption></figcaption></figure></div>

3. Ajoutez le fichier `.nsp`, sélectionnez-le et enregistrez.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (717).png" alt=""><figcaption></figcaption></figure></div>

## Problèmes connus

| Problème                                                        | Solution                                                                                                                       |
| --------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| L'émulateur demande des clés ou affiche une erreur au lancement | `prod.keys` manque ou ne correspond pas au firmware : voir [**Installer les émulateurs**](switch.md#installer-les-emulateurs). |
| Ryujinx ne trouve pas les clés ou le firmware installés         | Ils ont été installés avec Ryujinx lancé directement : recommencez avec `Configure Ryujinx.bat`.                               |
| Eden (ou Citron, Sudachi, Yuzu) ne trouve pas les clés          | Le dossier `user` manquait à la première ouverture : créez-le, puis replacez les clés et le firmware dans `user`.              |
| Un jeu affiche une fenêtre de choix des manettes                | Activez **CONTRÔLES > DÉSACTIVER L'APPLET DES CONTRÔLEURS**.                                                                   |
| Saccades à la première partie                                   | L'émulateur compile ses shaders : elles diminuent ensuite (cache des shaders).                                                 |
| Une mise à jour de jeu n'est pas prise en compte                | Elle est dans `roms\switch` : déplacez-la dans `roms\switchupdates` (Eden, Citron) ou installez-la dans l'émulateur.           |
