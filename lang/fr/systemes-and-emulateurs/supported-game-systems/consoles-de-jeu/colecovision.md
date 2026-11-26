---
description: Coleco
---

# ColecoVision

<div align="left"><figure><img src="../../../.gitbook/assets/image (756).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **ColecoVision** est la console de salon de **Coleco**, sortie en 1982. Elle est vendue avec Donkey Kong et propose des adaptations d'arcade très fidèles pour l'époque. Sa manette a un joystick, deux boutons latéraux et un pavé numérique de 12 touches, sur lequel on glisse des caches propres à chaque jeu. Des modules d'extension lui ajoutent un volant, le Super Action Controller ou les jeux de l'Atari 2600. Elle est arrêtée en 1985.

Sa ludothèque compte environ 150 jeux : Donkey Kong, Zaxxon, Venture, Lady Bug, Mr. Do!, Burgertime, Pitfall II, Q\*bert, Frogger, Turbo, Smurf: Rescue in Gargamel's Castle…

L'ordinateur **Coleco ADAM** a son propre système dans RetroBat (voir la page [**Coleco ADAM**](../micro-ordinateurs/coleco-adam.md)).

{% embed url="https://fr.wikipedia.org/wiki/ColecoVision" %}

## En bref

<table><thead><tr><th width="271.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\colecovision</code></td></tr><tr><td><strong>Extensions</strong></td><td>.col .rom .ri .mx1 .mx2 .dsk .ddp .cas .sg .sc .m3u .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: gearcoleco</td></tr><tr><td><strong>BIOS</strong></td><td><code>colecovision.rom</code> (obligatoire)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk, émulateurs autonomes (raccourcis)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro gearcoleco, jollycv et fbneo</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                         | Pour qui ?              | Points forts                                                                                                                                                    | Limites                                                                         |
| --------------------------------- | ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| **libretro: gearcoleco** (défaut) | Tout le monde           | Très compatible, cartouches MegaCart et Activision, extension SGM, spinner (Super Action Controller, volant, Roller Controller) à la souris, RetroAchievements. | —                                                                               |
| **libretro: jollycv**             | Utilisateurs de JollyCV | Émulation précise, choix de la palette.                                                                                                                         | —                                                                               |
| **libretro: bluemsx**             | Utilisateurs de blueMSX | Clavier émulé.                                                                                                                                                  | Pas de jeu en réseau.                                                           |
| **libretro: fbneo**               | Utilisateurs de FBNeo   | Mêmes réglages que les jeux d'arcade de FBNeo.                                                                                                                  | Jeux en `.zip` ou `.7z` nommés comme les sets ColecoVision de FBNeo uniquement. |
| **openmsx**                       | Utilisateurs d'openMSX  | Machine ColecoVision avec Super Game Module.                                                                                                                    | BIOS dans un dossier à part (voir [**BIOS**](colecovision.md#bios)).            |
| **ares**                          | Puristes                | Émulation très précise.                                                                                                                                         | Sauvegardes instantanées par raccourcis.                                        |
| **bizhawk: Coleco**               | Utilisateurs de BizHawk | RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.                                                                                           | —                                                                               |
| **mesen**                         | Utilisateurs de Mesen   | Choix de la région.                                                                                                                                             | Sauvegardes instantanées par raccourcis.                                        |

**En cas de doute, gardez libretro: gearcoleco.**

## BIOS

<table><thead><tr><th width="169">Fichier</th><th>Dossier</th><th width="213.5">MD5</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>colecovision.rom</code></td><td><code>bios</code></td><td>2c66f5911e5b42b8ebe113403548eee7</td><td>gearcoleco, ares, BizHawk, Mesen</td></tr><tr><td><code>coleco.rom</code></td><td><code>bios</code></td><td>2c66f5911e5b42b8ebe113403548eee7</td><td>jollycv (créé par RetroBat à partir de <code>colecovision.rom</code> s'il manque)</td></tr><tr><td><code>coleco.rom</code></td><td><code>bios\openMSX\share\systemroms</code></td><td>2c66f5911e5b42b8ebe113403548eee7</td><td>openMSX</td></tr><tr><td><code>coleco.zip</code></td><td><code>roms\colecovision</code></td><td>—</td><td>fbneo (BIOS au format FBNeo)</td></tr></tbody></table>

C'est le même fichier sous trois noms. blueMSX utilise le BIOS de ses machines (`bios\Machines`, fourni avec RetroBat).

## Quel format de jeu ?

<table><thead><tr><th width="207.75">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.col</strong>, <strong>.rom</strong></td><td>Image d'une cartouche. Lue par tous les émulateurs, sauf FBNeo.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive). Avec fbneo : sets ColecoVision de FBNeo uniquement (voir la liste des jeux de FBNeo).</td></tr><tr><td><strong>.ri .mx1 .mx2 .dsk .ddp .cas .sg .sc .m3u</strong></td><td>Formats MSX et SG-1000, lus par blueMSX et openMSX.</td></tr></tbody></table>

## Contrôles

RetroBat configure automatiquement les manettes pour tous les émulateurs, pour deux joueurs. Les touches du pavé numérique sont réparties sur la manette.

| Manette RetroBat                     | gearcoleco            | jollycv                                           |
| ------------------------------------ | --------------------- | ------------------------------------------------- |
| Croix directionnelle                 | Joystick              | Joystick                                          |
| SUD                                  | Bouton gauche (jaune) | Bouton gauche (jaune) ; avec L2 : 1 ; avec R2 : 5 |
| EST                                  | Bouton droit (rouge)  | Bouton droit (orange) ; avec L2 : 2 ; avec R2 : 6 |
| OUEST                                | 1                     | Violet ; avec L2 : 3 ; avec R2 : 7                |
| NORD                                 | 2                     | Bleu ; avec L2 : 4 ; avec R2 : 8                  |
| L1                                   | 3                     | Spinner -                                         |
| R1                                   | 4                     | Spinner +                                         |
| L2                                   | 5                     | Touche de combinaison 1                           |
| R2                                   | 6                     | Touche de combinaison 2                           |
| L3                                   | 7                     | —                                                 |
| R3                                   | 8                     | —                                                 |
| Stick gauche (horizontal / vertical) | 0 / 9                 | —                                                 |
| Stick droit (horizontal / vertical)  | Bleu / Violet         | —                                                 |
| START                                | \*                    | #                                                 |
| SELECT                               | #                     | \* ; avec L2 : 9 ; avec R2 : 0                    |

Les boutons violet et bleu servent au Super Action Controller (Super Action Baseball, Football…).

Avec blueMSX, **TYPE DE CONTRÔLEUR** choisit la manette ou le clavier émulés.

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch. openMSX, ares, BizHawk et Mesen utilisent les raccourcis communs de RetroBat. Voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

## Dossiers

<table><thead><tr><th width="342.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\colecovision</code></td></tr><tr><td>BIOS</td><td><code>bios</code>, <code>bios\openMSX\share\systemroms</code> (openMSX)</td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><p><code>saves\colecovision\libretro.&#x3C;core></code></p><p>(ex. <code>saves\colecovision\libretro.gearcoleco</code>)</p></td></tr><tr><td>BizHawk : sauvegardes instantanées</td><td><code>saves\colecovision\bizhawk\sstates\Coleco</code></td></tr><tr><td>BizHawk : captures d'écran</td><td><code>screenshots\bizhawk\colecovision</code></td></tr></tbody></table>

## Guides

### Spinner et volant

Avec **libretro: gearcoleco**, **CONTRÔLES > SUPPORT DU SPINNER** émule à la souris le **SUPER ACTION CONTROLLER**, le **VOLANT** (Turbo, Destructor) ou le **ROLLER CONTROLLER** (Slither). Les boutons de la souris sont les boutons gauche et droit. **SENSIBILITÉ DU SPINNER** règle la vitesse.

### Autres options utiles

<table><thead><tr><th width="179.5">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>gearcoleco, jollycv</td><td><strong>VIDÉO > DÉSACTIVER LA LIMITE DE SPRITES</strong></td><td>Supprime le clignotement quand trop de sprites sont sur une ligne.</td></tr><tr><td>gearcoleco</td><td><strong>ÉMULATION > MAPPER</strong></td><td>Force le type de cartouche si un jeu ne démarre pas.</td></tr><tr><td>gearcoleco</td><td><strong>ÉMULATION > FRÉQUENCE DE RAFRAÎCHISSEMENT</strong></td><td>NTSC (60 Hz) ou PAL (50 Hz).</td></tr><tr><td>jollycv</td><td><strong>RENDU VISUEL > PALETTE</strong></td><td>Couleurs de la puce vidéo.</td></tr><tr><td>Mesen</td><td><strong>ÉMULATION > RÉGION DU SYSTÈME</strong></td><td>NTSC ou PAL.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="330.25">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Écran noir ou message de BIOS manquant</td><td><code>colecovision.rom</code> manque dans <code>bios</code> (voir <a href="colecovision.md#bios"><strong>BIOS</strong></a>). Pour openMSX, copiez-le en <code>coleco.rom</code> dans <code>bios\openMSX\share\systemroms</code>.</td></tr><tr><td>Un jeu ne démarre pas avec fbneo</td><td>fbneo ne lit que les sets ColecoVision de FBNeo, avec <code>coleco.zip</code> : utilisez gearcoleco.</td></tr><tr><td>Le jeu attend un choix au pavé (niveau, nombre de joueurs)</td><td>Touches 1 à 8 sur la manette (voir <a href="colecovision.md#controles"><strong>Contrôles</strong></a>) : en général 1 à 4 pour un joueur, 5 à 8 pour deux.</td></tr></tbody></table>
