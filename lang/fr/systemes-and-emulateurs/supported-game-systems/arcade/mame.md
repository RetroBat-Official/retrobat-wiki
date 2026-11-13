---
description: MAME Team
---

# MAME

<div align="left"><figure><img src="../../../.gitbook/assets/image (579).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

**MAME** (Multiple Arcade Machine Emulator) est né en 1997 sous l'impulsion de Nicola Salmoria. Son but n'est pas d'abord de jouer, mais de **préserver** : documenter le fonctionnement des bornes d'arcade en le reproduisant fidèlement, pour que ces machines ne disparaissent pas avec leur matériel.

Près de trente ans plus tard, MAME émule des dizaines de milliers de machines : bornes d'arcade de toutes les époques, mais aussi consoles et ordinateurs depuis sa fusion avec le projet MESS en 2015. Dans RetroBat, le système MAME est réservé à l'arcade, les autres machines ont leur propre système.

Chaque jeu est un fichier appelé **romset**, dont le nom est fixé par MAME (`sf2.zip` pour Street Fighter II). Le contenu des romsets change d'une version de MAME à l'autre : un romset doit correspondre à la version de l'émulateur utilisé (voir la page [**Le Guide Arcade**](../../arcade-guide.md)).

{% embed url="https://fr.wikipedia.org/wiki/MAME" %}

## En bref

<table><thead><tr><th width="280.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\mame</code></td></tr><tr><td><strong>Extensions</strong></td><td>.zip .7z .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: mame</td></tr><tr><td><strong>BIOS</strong></td><td>Selon le type de romset (voir BIOS)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; MAME et GroovyMAME par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro (mame)</td></tr><tr><td><strong>Pistolets</strong></td><td>cores libretro (mame), MAME, GroovyMAME</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                                                                        | Pour qui ?                   | Points forts                                                                                                               | Limites                                                                                |
| -------------------------------------------------------------------------------- | ---------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **libretro: mame** (défaut)                                                      | Tout le monde                | La version actuelle de MAME dans RetroArch : shaders, décorations, jeu en réseau, boutons réglés jeu par jeu par RetroBat. | N'aime pas les chemins d'installation trop longs (voir Problèmes connus).              |
| **mame64**                                                                       | Utilisateurs avancés, bornes | Le MAME officiel, avec tous ses réglages et ses profils de contrôleur (IPAC2, X-Arcade).                                   | —                                                                                      |
| **groovymame**                                                                   | Écrans CRT                   | Adapte la résolution et la fréquence de l'écran à chaque jeu.                                                              | Demande un écran et un matériel adaptés.                                               |
| **libretro: mame2003\_plus**                                                     | PC modestes                  | Léger, avec les boutons réglés jeu par jeu comme lr-mame.                                                                  | Demande son propre romset (MAME 0.78 et ajouts).                                       |
| **libretro: mame2016, mame2014, mame2010, mame2003, mame2003\_midway, mame2000** | PC modestes, romsets anciens | Plus légers.                                                                                                               | Chaque core demande le romset de sa propre version. Pas de boutons réglés jeu par jeu. |

**En cas de doute, gardez libretro: mame.**

### Choix automatique du core

Tant que vous n'avez choisi aucun émulateur pour le système ni pour le jeu, RetroBat vérifie le romset avant de le lancer :

<table><thead><tr><th width="336.5">Votre romset…</th><th>Core lancé</th></tr></thead><tbody><tr><td>convient à libretro: mame</td><td>libretro: mame</td></tr><tr><td>vient d'une ancienne version de MAME</td><td>Le premier core compatible, dans cet ordre : mame2016, mame2014, mame2010, mame2003_plus, mame2003, mame2000</td></tr><tr><td>n'est pas reconnu</td><td>libretro: mame</td></tr></tbody></table>

Un romset ancien se lance donc sans réglage, avec le core qui lui correspond.

* Seuls les fichiers `.zip` sont vérifiés.
* La vérification porte sur tous les fichiers du jeu, BIOS compris. Avec un romset split ou sans les fichiers BIOS dans le zip, le jeu n'est souvent pas reconnu : libretro: mame est alors utilisé.
* Dès que vous choisissez un émulateur pour le système ou pour le jeu, ce choix est respecté et la vérification n'est plus faite.

## BIOS

### BIOS et « devices »

En plus de son romset, un jeu peut avoir besoin de romsets partagés entre plusieurs jeux :

<table><thead><tr><th width="107">Type</th><th width="407.5">Rôle</th><th>Exemples</th></tr></thead><tbody><tr><td><strong>BIOS</strong></td><td>Le programme de base d'une carte d'arcade</td><td><code>neogeo.zip</code>, <code>pgm.zip</code>, <code>naomi.zip</code>, <code>stvbios.zip</code></td></tr><tr><td><strong>Device</strong></td><td>Un composant commun à plusieurs cartes (puce son, contrôleur…)</td><td><code>qsound_hle.zip</code>, <code>ym2608.zip</code>, <code>namco51.zip</code></td></tr></tbody></table>

Un jeu peut refuser de démarrer parce qu'un romset « device » manque, même si son BIOS est présent.

Le besoin dépend du type de romset :

<table><thead><tr><th width="194">Type de romset</th><th>BIOS et devices séparés nécessaires ?</th></tr></thead><tbody><tr><td>Full non-merged</td><td>Non : tout est dans le romset du jeu</td></tr><tr><td>Non-merged</td><td>Oui, pour les fichiers partagés entre plusieurs jeux</td></tr><tr><td>Split</td><td>Oui</td></tr><tr><td>Merged</td><td>Non pour les BIOS</td></tr></tbody></table>

Voir la page [**Le Guide Arcade**](../../arcade-guide.md) pour le détail des types de romsets.

### Où les placer ?

Les BIOS et les devices se placent à la **racine du dossier** `bios`, ou à côté des jeux dans `roms\mame`. MAME cherche dans les deux dossiers.

RetroBat ne vérifie pas la présence des BIOS de MAME.

## Quel format de jeu ?

<table><thead><tr><th width="126.5">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.zip</strong></td><td>Le romset du jeu. Ne le renommez pas et ne le décompressez pas.</td></tr><tr><td>.7z</td><td>Romset compressé en 7z.</td></tr><tr><td>.chd</td><td>Disque dur, CD ou LaserDisc d'un jeu. Il se place dans un dossier au nom du jeu, à côté du romset (voir la page <a href="../../arcade-guide.md"><strong>Le Guide Arcade</strong></a>).</td></tr></tbody></table>

Certains jeux utilisent aussi des **samples** (sons enregistrés), à placer dans `bios\mame\samples`.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour tous les émulateurs MAME.

Les bornes d'arcade ont toutes un panneau différent. RetroBat procède donc en deux temps :

1. **Le jeu a une configuration dédiée** : RetroBat en fournit pour plus de 3 000 jeux, avec les boutons placés comme sur la borne d'origine. Si le jeu est un clone sans configuration, celle du jeu parent est utilisée.
2. **Sinon**, RetroBat applique la configuration par défaut ci-dessous.

Cela vaut pour lr-mame, mame2003\_plus, MAME et GroovyMAME. Les autres cores libretro gardent la disposition du core.

<table><thead><tr><th width="200.75">Bouton de la borne</th><th width="266.75">Manette RetroBat</th><th>Clavier</th></tr></thead><tbody><tr><td>Directions</td><td>Croix directionnelle / stick gauche</td><td>Flèches</td></tr><tr><td>Bouton 1</td><td>OUEST</td><td>CTRL gauche</td></tr><tr><td>Bouton 2</td><td>SUD</td><td>ALT gauche</td></tr><tr><td>Bouton 3</td><td>EST</td><td>ESPACE</td></tr><tr><td>Bouton 4</td><td>NORD</td><td>MAJ gauche</td></tr><tr><td>Bouton 5</td><td>L1</td><td>Z</td></tr><tr><td>Bouton 6</td><td>R1</td><td>X</td></tr><tr><td>Bouton 7</td><td>L2 (MAME, GroovyMAME, mame2003_plus)</td><td>C</td></tr><tr><td>Bouton 8</td><td>R2 (MAME, GroovyMAME, mame2003_plus)</td><td>V</td></tr><tr><td>Crédit</td><td>SELECT</td><td>5</td></tr><tr><td>Start</td><td>START</td><td>1</td></tr><tr><td>Service</td><td>L3 (MAME, GroovyMAME)</td><td>9</td></tr><tr><td>Test</td><td>R3 (MAME, GroovyMAME)</td><td>0</td></tr><tr><td>Pédale 1 / Pédale 2</td><td>R2 / L2 (MAME, GroovyMAME), R1 / L1 (mame2003_plus)</td><td>—</td></tr><tr><td>Volant, molette, trackball, stick analogique</td><td>Stick gauche</td><td>Souris</td></tr><tr><td>Deuxième joystick</td><td>Stick droit</td><td>—</td></tr></tbody></table>

### Sticks arcade et boutons personnalisés

Sur un stick arcade, réglez **CONTRÔLES > DISPOSITION DES BOUTONS** selon votre panneau : RetroBat y reproduit la disposition de la borne d'origine. Cette option vaut pour lr-mame, mame2003\_plus, MAME et GroovyMAME.

Vous pouvez aussi corriger les boutons d'un jeu, utiliser un panneau IPAC2 ou X-Arcade, créer votre propre profil ou garder les boutons réglés dans le menu de MAME. Ces méthodes, et les fichiers `.cfg` de MAME, sont décrits sur la page [**Configuration des touches MAME**](../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-mame64.md).

### Pistolets

Activez **PISTOLETS > ACTIVER LES PISTOLETS**. Pour brancher et régler un pistolet dans RetroBat, voir la page [**Pistolets**](../../../controleurs/supported-controllers/lightguns/).

<table><thead><tr><th width="223.25">Émulateur</th><th>Fonctionnement</th><th>Options utiles</th></tr></thead><tbody><tr><td><strong>libretro: mame</strong></td><td><strong>MODE PISTOLET</strong> choisit entre pistolet et écran tactile.</td><td><strong>CONFIGURATION BOUTONS SINDEN</strong>, <strong>DÉSACTIVER LA CIBLE</strong></td></tr><tr><td><strong>mame64</strong>, <strong>groovymame</strong></td><td>Jusqu'à 4 pistolets. Dès que plusieurs pistolets sont branchés, chacun est attribué à un joueur.</td><td><strong>FORCER UN SEUL PISTOLET</strong>, <strong>INDEX SOURIS/GUN JOUEUR 1</strong> (à 4) pour choisir quel pistolet va à quel joueur, <strong>DÉSACTIVER LA CIBLE</strong>, <strong>UTILISER MAMEHOOKER</strong> pour le recul et les sorties</td></tr></tbody></table>

<div align="left"><figure><img src="../../../.gitbook/assets/image (580).png" alt=""><figcaption></figcaption></figure></div>

### Raccourcis

**MAME et GroovyMAME**

| Raccourci          | Action                 | Clavier        |
| ------------------ | ---------------------- | -------------- |
| **HOTKEY + START** | Quitter                | ÉCHAP          |
| HOTKEY + SUD       | Menu de MAME           | TAB            |
| HOTKEY + OUEST     | Sauvegarde instantanée | F2             |
| HOTKEY + NORD      | Chargement instantané  | F4             |
| HOTKEY + DROITE    | Avance rapide          | ESPACE         |
| HOTKEY + GAUCHE    | Retour en arrière      | RETOUR ARRIÈRE |
| HOTKEY + R1        | Tilt                   | T              |
| —                  | Pause                  | P              |

Dans le menu de MAME, **SUD** valide et **EST** revient en arrière.

**lr-mame** utilise les raccourcis RetroArch (voir la [page Raccourcis](../../../navigation/hotkeys.md)). Le menu de MAME s'ouvre avec **START + SUD**.

**mame2003\_plus** utilise aussi les raccourcis RetroArch. Le menu de MAME s'ouvre avec **L3**.

### Menu de service

Au clavier, la touche **0** ouvre le menu de test de la borne et la touche **9** sert de bouton Service pour s'y déplacer.

Avec MAME et GroovyMAME, ces deux fonctions sont aussi sur la manette : **R3** pour le test, **L3** pour le service. L'option **CONTRÔLES > TEST/SERVICE SUR L3/R3**, active par défaut, permet de les retirer.

## Dossiers

<table><thead><tr><th width="322.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS et devices</td><td><code>bios</code> (à la racine) ou <code>roms\mame</code></td></tr><tr><td>Samples</td><td><code>bios\mame\samples</code></td></tr><tr><td>Fichiers ini</td><td><code>bios\mame\ini</code> (GroovyMAME : <code>bios\groovymame\ini</code>)</td></tr><tr><td>Listes de logiciels (hash)</td><td><code>bios\mame\hash</code></td></tr><tr><td>Réglages par jeu (cfg)</td><td><code>saves\mame\cfg</code> (ou <code>saves\mame\cfg64</code>)</td></tr><tr><td>Copies de sécurité des cfg</td><td><code>saves\mame\cfgbackup</code> (lr-mame), <code>saves\mame\cfgbackupmame64</code> (MAME)</td></tr><tr><td>Profils de contrôleur</td><td><code>saves\mame\ctrlr</code></td></tr><tr><td>Mémoire des bornes (NVRAM)</td><td><code>saves\mame\nvram</code></td></tr><tr><td>Sauvegardes instantanées de MAME</td><td><code>saves\mame\states</code></td></tr><tr><td>Sauvegardes instantanées de lr-mame</td><td><code>saves\mame\libretro.mame</code></td></tr><tr><td>Réglages, mémoire et scores de mame2003_plus</td><td><code>saves\mame\mame2003-plus</code></td></tr><tr><td>Vos artworks</td><td><code>saves\mame\artwork</code></td></tr><tr><td>Codes de triche</td><td><code>cheats\mame</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots</code></td></tr><tr><td>Configurations par jeu de RetroBat</td><td><code>system\resources\inputmapping</code></td></tr><tr><td>Vos configurations par jeu</td><td><code>user\inputmapping</code></td></tr></tbody></table>

RetroBat utilise le dossier `bios\mame\artwork` pour fabriquer les décorations : n'y rangez pas vos artworks, ils seraient écrasés.

## Guides

### Jouer sur un écran CRT avec GroovyMAME

GroovyMAME est une version de MAME faite pour les écrans cathodiques : il règle la résolution et la fréquence de l'écran sur celles de la borne d'origine.

1. Choisissez l'émulateur **groovymame** pour le système ou pour le jeu.
2. Dans **VIDÉO > PROFIL D'ÉCRAN**, choisissez le profil de votre écran :

<table><thead><tr><th width="336.5">Profil</th><th>Écran</th></tr></thead><tbody><tr><td>LCD Arcade (Vewlix) / PC / Modern TV</td><td>Écran plat</td></tr><tr><td>LCD Arcade (vertical)</td><td>Écran plat monté en vertical</td></tr><tr><td>CRT TV 15 kHz</td><td>Téléviseur cathodique</td></tr><tr><td>CRT TV PAL</td><td>Téléviseur cathodique PAL</td></tr><tr><td>CRT Arcade 15 kHz</td><td>Moniteur d'arcade standard</td></tr><tr><td>CRT Arcade 25 kHz</td><td>Moniteur d'arcade moyenne résolution</td></tr><tr><td>CRT Arcade 31 kHz VGA</td><td>Moniteur d'arcade haute résolution</td></tr><tr><td>CRT 15 kHz + 25 kHz Combo</td><td>Moniteur bi-fréquence</td></tr><tr><td>CRT 15/25/31 kHz</td><td>Moniteur tri-fréquence</td></tr><tr><td>CRT PC 31 kHz 120 Hz</td><td>Moniteur cathodique de PC</td></tr><tr><td>PVM / BVM</td><td>Moniteur professionnel</td></tr></tbody></table>

GroovyMAME a ses propres fichiers ini, dans `bios\groovymame\ini`. Les décorations sont désactivées par défaut avec cet émulateur.

## Problèmes connus

<table><thead><tr><th width="331.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Écran noir au lancement avec libretro: mame</td><td>Le chemin d'installation de RetroBat est trop long. Installez RetroBat dans un dossier court, par exemple <code>C:\RetroBat</code>, ou utilisez mame64.</td></tr><tr><td>Le jeu se lance avec un autre core que libretro: mame</td><td>Son romset vient d'une ancienne version de MAME et RetroBat a choisi le core compatible (voir Choix automatique du core). Pour imposer un core, choisissez-le dans les options du jeu.</td></tr><tr><td>Le jeu ne démarre pas</td><td>Le romset ne correspond pas à la version de l'émulateur, ou un BIOS ou un device manque (voir BIOS et la page <a href="../../arcade-guide.md"><strong>Le Guide Arcade</strong></a>).</td></tr><tr><td>Les boutons ne tombent pas au bon endroit sur mon stick arcade</td><td>Réglez <strong>DISPOSITION DES BOUTONS</strong> selon votre panneau (voir la page <a href="../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-mame64.md"><strong>Configuration des touches MAME</strong></a>).</td></tr><tr><td>Mes réglages faits dans le menu de MAME sont perdus</td><td>La configuration automatique les remplace : voir la page <a href="../../../controleurs/configuration-des-touches-specifique-par-emulateur/configuration-des-touches-mame64.md"><strong>Configuration des touches MAME</strong></a>.</td></tr><tr><td>Le menu de test s'ouvre quand j'appuie sur un stick</td><td>Avec MAME et GroovyMAME, désactivez <strong>TEST/SERVICE SUR L3/R3</strong>.</td></tr><tr><td>Mes artworks disparaissent</td><td>Rangez-les dans <code>saves\mame\artwork</code>, pas dans <code>bios\mame\artwork</code>.</td></tr></tbody></table>
