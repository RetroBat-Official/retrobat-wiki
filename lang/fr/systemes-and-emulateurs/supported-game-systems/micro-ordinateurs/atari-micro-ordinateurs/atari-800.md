---
description: Atari
---

# Atari 800

<div align="left"><figure><img src="../../../../.gitbook/assets/image (646).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

L'**Atari 800** et l'**Atari 400** sortent fin 1979. Ce sont les premiers ordinateurs familiaux d'Atari. Leurs puces graphiques (ANTIC, CTIA puis GTIA) et sonore (POKEY) les placent parmi les machines les plus puissantes de leur époque. La gamme continue avec le 1200XL (1982), les 600XL et 800XL (1983), puis les 65XE et 130XE (1985). Tous ces modèles lisent les mêmes logiciels, sauf quelques exceptions.

La ludothèque est très riche : Star Raiders, M.U.L.E., Archon, Rescue on Fractalus!, Boulder Dash, Ballblazer, Alternate Reality… Les jeux existent sur disquette, cassette et cartouche.

Le système `atari800` de RetroBat couvre toute la gamme 400/800/XL/XE. La console XE Game System (XEGS) et la console Atari 5200, de la même famille, ont chacune leur propre système (voir les pages [**Atari XEGS**](../../consoles-de-jeu/atari-consoles-de-jeu/atari-xegs.md) et [**Atari 5200**](../../consoles-de-jeu/atari-consoles-de-jeu/atari-5200.md)).

{% embed url="https://fr.wikipedia.org/wiki/Atari_8-bits" %}

## En bref

<table><thead><tr><th width="275.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\atari800</code></td></tr><tr><td><strong>Extensions</strong></td><td>.rom .xfd .atr .atx .dcm .cas .bin .car .a52 .xex .com .m3u .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: atari800</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (ROM d'origine facultatives)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="130.25">Émulateur</th><th width="111.5">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: atari800</strong> (défaut)</td><td>Tout le monde</td><td>Atari800 7.0 : toute la gamme 400/800/XL/XE, système (AltirraOS) et BASIC (Altirra BASIC) intégrés, clavier virtuel à la manette, sauvegardes instantanées.</td><td>—</td></tr><tr><td><strong>altirra</strong></td><td>Puristes</td><td>Altirra, l'émulateur le plus précis des Atari 8 bits : excellente compatibilité, y compris avec les disquettes protégées.</td><td>Un seul bouton de tir à la manette. Pas de sauvegardes instantanées ni de raccourcis RetroBat (seul HOTKEY + START, pour quitter).</td></tr></tbody></table>

**En cas de doute, gardez libretro: atari800.**

## BIOS

Aucun BIOS n'est nécessaire : le core atari800 a un système (AltirraOS) et un BASIC (Altirra BASIC) libres intégrés. Les ROM d'origine améliorent la compatibilité avec quelques logiciels : le core les utilise si elles sont dans `bios`.

<table><thead><tr><th width="134.75">Fichier</th><th width="79">Dossier</th><th width="335.75">MD5</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>ATARIOSA.ROM</code></td><td><code>bios</code></td><td>eb1f32f5d9f382db1bbfb8d7f9cb343a</td><td>core atari800 (OS A des 400/800)</td></tr><tr><td><code>ATARIOSB.ROM</code></td><td><code>bios</code></td><td>a3e8d617c95d08031fe1b20d541434b2</td><td>core atari800 (OS B des 400/800)</td></tr><tr><td><code>ATARIXL.ROM</code></td><td><code>bios</code></td><td>06daac977823773a3eea3422fd26a703</td><td>core atari800 (OS des XL/XE)</td></tr><tr><td><code>ATARIBAS.ROM</code></td><td><code>bios</code></td><td>0bac0c6a50104045d902df4503a4c30b</td><td>core atari800 (BASIC)</td></tr></tbody></table>

La vérification des BIOS de RetroBat les liste comme optionnels.

Altirra ne lit pas le dossier `bios` : il démarre avec son propre système intégré. **ÉMULATION > KERNEL** (Altirra) : **PAR DÉFAUT** utilise le système choisi dans la configuration d'Altirra, **INTERNE** force le système intégré.

## Quel format de jeu ?

<table><thead><tr><th width="187">Type</th><th width="211.25">Extensions</th><th>Remarques</th></tr></thead><tbody><tr><td>Disquette</td><td><code>.atr</code>, <code>.atx</code>, <code>.xfd</code>, <code>.dcm</code></td><td><code>.atr</code> est le plus courant. <code>.atx</code> garde les protections contre la copie.</td></tr><tr><td>Cassette</td><td><code>.cas</code></td><td>RetroBat démarre la cassette automatiquement.</td></tr><tr><td>Cartouche</td><td><code>.car</code>, <code>.rom</code>, <code>.bin</code></td><td><code>.car</code> contient le type de la cartouche. Avec <code>.rom</code> et <code>.bin</code>, l'émulateur doit le deviner.</td></tr><tr><td>Programme</td><td><code>.xex</code>, <code>.com</code></td><td>Programme chargé directement en mémoire.</td></tr><tr><td>Plusieurs disquettes</td><td><code>.m3u</code></td><td>Liste des disquettes d'un jeu (voir <a href="atari-800.md#jeux-sur-plusieurs-disquettes"><strong>Guides</strong></a>).</td></tr></tbody></table>

Les fichiers peuvent être compressés en `.zip` ou `.7z` (un jeu par archive). Les cartouches `.a52` sont des jeux Atari 5200 : rangez-les dans `roms\atari5200`.

## Contrôles

RetroBat configure automatiquement les manettes. Le joystick Atari a un seul bouton de tir. Les touches **Start**, **Select** et **Option** de l'ordinateur sont sur la manette.

| Manette RetroBat     | libretro: atari800                                                                                        | altirra                                        |
| -------------------- | --------------------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| Croix directionnelle | Joystick                                                                                                  | Joystick                                       |
| Stick gauche         | —                                                                                                         | Joystick (option **UTILISER LE STICK GAUCHE**) |
| SUD                  | Tir                                                                                                       | Tir                                            |
| EST                  | Tir 2 (manettes à deux boutons, voir [**Guides**](atari-800.md#jeux-a-deux-sticks-et-manettes-speciales)) | —                                              |
| OUEST                | Espace                                                                                                    | —                                              |
| NORD                 | Return                                                                                                    | —                                              |
| START                | Start                                                                                                     | Start                                          |
| SELECT               | Select                                                                                                    | Select                                         |
| L1                   | Option                                                                                                    | —                                              |
| L2                   | Esc                                                                                                       | —                                              |
| R2                   | Help (XL/XE)                                                                                              | —                                              |
| L3                   | Clavier virtuel                                                                                           | —                                              |

Le clavier du PC sert de clavier Atari. Avec le core atari800, appuyez sur `Arrêt défil` pour activer le **Game Focus** de RetroArch : toutes les touches vont à l'ordinateur émulé. Pour mettre des touches du clavier sur la manette, voir la page **Pad2Key**.

**OPTIONS AVANCÉES > CONTRÔLES** :

* **TYPE DE CONTRÔLEUR JOUEUR 1 / JOUEUR 2** (core atari800) : **JOYSTICK ATARI** (défaut), **CLAVIER ATARI**, **RETROPAD**.
* **FORCER L'UTILISATION DU PORT 2** (Altirra) : pour les jeux qui lisent le joystick sur le port 2.
* **FORCER L'INDEX DE LA MANETTE DU JOUEUR 1 / 2** (Altirra) : choisit la manette de chaque joueur.

### Raccourcis

Le core atari800 utilise les raccourcis standards de RetroArch. Avec Altirra, seul HOTKEY + START (quitter) est configuré par RetroBat. Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

| Contenu                                            | Dossier                             |
| -------------------------------------------------- | ----------------------------------- |
| Jeux                                               | `roms\atari800`                     |
| BIOS (core atari800)                               | `bios`                              |
| Core atari800 : sauvegardes instantanées           | `saves\atari800\libretro.atari800`  |
| Core atari800 : fichier de configuration du moteur | `emulators\retroarch\.atari800.cfg` |
| Altirra : configuration                            | `emulators\altirra\Altirra.ini`     |
| Captures d'écran (core atari800)                   | `screenshots`                       |

## Guides

### Choisir la machine

Quelques jeux anciens ne marchent que sur un 400/800, quelques jeux récents demandent un XL/XE avec 64K ou 128K.

* Core atari800 : **ÉMULATION > SYSTÈME ÉMULÉ**. Par défaut **800XL (64K)**. Choisissez **400/800 (48K) (OS B)** pour un jeu des débuts, **130XE (128K)** pour un jeu qui demande 128K.
* Altirra : **ÉMULATION > FORCER LA MACHINE** (**ATARI 800**, **ATARI 600XL/800XL**, **ATARI 1200XL**…). **ÉMULATION > CHOISIR LE PROFIL AUTOMATIQUEMENT** laisse Altirra choisir d'après le jeu.

### Programmes BASIC

Les programmes en BASIC ont besoin du BASIC de la machine : activez **ÉMULATION > BASIC INTERNE** (core atari800). Le core utilise `ATARIBAS.ROM` s'il est présent, sinon l'Altirra BASIC intégré. Laissez l'option désactivée pour les jeux : certains ne démarrent pas avec le BASIC.

### Jeux à deux sticks et manettes spéciales

**CONTRÔLES > HACKS DES MANETTES** (core atari800) :

* **DOUBLE STICK** : le joystick du port 2 est sur le stick droit, pour Robotron: 2084 et Space Dungeon.
* **INVERSER LES PORTS** : pour les jeux qui lisent le joystick sur le port 2 (Wizard of Wor, Apple Panic).
* **JOY 2B+** : manettes à plusieurs boutons (EST = Tir 2).

Pour les jeux à paddles : **CONTRÔLES > ACTIVER LE MODE PADDLE**, et **VITESSE DU PADDLE** pour régler la vitesse.

### Jeux sur plusieurs disquettes

Créez un fichier `.m3u` qui liste les disquettes, une par ligne, puis lancez le `.m3u`. Avec le core atari800, changez de disquette dans le menu de RetroArch (**Contrôle du disque**).

### Autres options utiles

<table><thead><tr><th width="150.75">Émulateur</th><th width="266.75">Option</th><th>Effet</th></tr></thead><tbody><tr><td>core atari800</td><td><strong>RÉSOLUTION DE SORTIE</strong></td><td>Taille de l'image : <strong>NATIF (336x240)</strong> ou plus grande, avec les bordures.</td></tr><tr><td>core atari800</td><td><strong>VIDÉO > FORMAT VIDÉO ÉMULÉ</strong></td><td><strong>NTSC</strong> (défaut) ou <strong>PAL</strong>, pour les jeux européens.</td></tr><tr><td>core atari800</td><td><strong>RENDU VISUEL > PALETTE</strong></td><td>Palettes de couleurs toutes faites (<strong>JAKUB</strong>, <strong>REAL</strong>, <strong>XFORMER</strong>…).</td></tr><tr><td>core atari800</td><td><strong>VIDÉO > MODE D'ARTEFACTS</strong></td><td>Couleurs créées par les téléviseurs dans certains jeux en haute résolution.</td></tr><tr><td>altirra</td><td><strong>VIDÉO > STANDARD VIDÉO</strong></td><td>NTSC (défaut), PAL, SECAM…</td></tr><tr><td>altirra</td><td><strong>VIDÉO > PUCE VIDÉO CTIA</strong></td><td>Puce vidéo des premiers Atari 800, demandée par quelques très vieux jeux.</td></tr></tbody></table>

## Problèmes connus

| Problème                                                   | Solution                                                                                                                                              |
| ---------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| Écran bleu « BOOT ERROR », ou le jeu plante au démarrage   | Changez de machine (voir [**Choisir la machine**](atari-800.md#choisir-la-machine)). Ou ajoutez les ROM d'origine dans `bios` (core atari800).        |
| Un programme affiche « READY » ou ne démarre pas           | C'est un programme BASIC : activez **BASIC INTERNE**. À l'inverse, un jeu qui affiche « READY » au lieu de démarrer peut demander le BASIC désactivé. |
| Une cartouche `.rom` ou `.bin` ne démarre pas              | Le type de la cartouche est mal deviné. Utilisez la version `.car` du jeu.                                                                            |
| Le joystick ne répond pas dans un jeu                      | Le jeu lit le port 2 : **INVERSER LES PORTS** (core atari800) ou **FORCER L'UTILISATION DU PORT 2** (Altirra).                                        |
| Les touches du clavier lancent des raccourcis de RetroArch | Appuyez sur `Arrêt défil` (Game Focus).                                                                                                               |
