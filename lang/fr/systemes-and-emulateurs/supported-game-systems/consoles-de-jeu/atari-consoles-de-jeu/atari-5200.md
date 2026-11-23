---
description: Atari
---

# Atari 5200

<div align="left"><figure><img src="../../../../.gitbook/assets/image (1) (1).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

L'**Atari 5200 SuperSystem** sort fin 1982 aux États-Unis, pour succéder à l'Atari 2600. Elle reprend l'électronique des ordinateurs Atari 400/800, sans clavier. Sa manette est originale : un joystick analogique qui ne revient pas au centre, deux boutons de tir de chaque côté, un pavé numérique de 12 touches et les touches **Start**, **Pause** et **Reset**. La console est arrêtée en 1984, après le krach du jeu vidéo.

Sa ludothèque compte environ 70 jeux, souvent des adaptations de l'arcade ou des ordinateurs Atari : Star Raiders, Pac-Man, Super Breakout, Centipede, Robotron: 2084, Pitfall II, Gremlins, Missile Command…

{% embed url="https://fr.wikipedia.org/wiki/Atari_5200" %}

## En bref

<table><thead><tr><th width="274"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\atari5200</code></td></tr><tr><td><strong>Extensions</strong></td><td>.a52 .bin .rom .car .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: a5200</td></tr><tr><td><strong>BIOS</strong></td><td><code>5200.rom</code> (facultatif, conseillé)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>core libretro a5200</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="157.75">Émulateur</th><th width="133.75">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: a5200</strong> (défaut)</td><td>Tout le monde</td><td>Émulateur dédié à la 5200 : pavé numérique à l'écran ou sur les boutons, jeu en réseau, sauvegardes instantanées.</td><td>Les cartouches <code>.car</code> ne sont pas lues.</td></tr><tr><td><strong>libretro: atari800</strong></td><td>Alternative</td><td>Atari800 7.0 en mode 5200 : pavé numérique sur les boutons, clavier virtuel, sauvegardes instantanées.</td><td>—</td></tr><tr><td><strong>altirra</strong></td><td>Puristes</td><td>Altirra, l'émulateur le plus précis de la famille Atari 8 bits, avec le choix exact du type de cartouche.</td><td>Pavé numérique non disponible à la manette. Pas de sauvegardes instantanées ni de raccourcis RetroBat (seul HOTKEY + START, pour quitter).</td></tr></tbody></table>

**En cas de doute, gardez libretro: a5200.**

## BIOS

Le BIOS est facultatif : a5200, atari800 et Altirra ont un système libre intégré (Altirra 5200 OS). Le vrai BIOS reste conseillé : il est plus compatible. Sans lui, a5200 affiche « Missing BIOS file (5200.rom) - using internal » au lancement.

<table><thead><tr><th width="111.5">Fichier</th><th width="83.75">Dossier</th><th width="338.5">MD5</th><th>Utilisé par</th></tr></thead><tbody><tr><td><code>5200.rom</code></td><td><code>bios</code></td><td>281f20ea4320404ec820fb7ec0693b38</td><td>cores a5200 et atari800</td></tr></tbody></table>

La vérification des BIOS de RetroBat le liste comme optionnel. Altirra ne lit pas le dossier `bios` : il utilise son système intégré.

## Quel format de jeu ?

Les jeux sont des images de cartouche :

* `.a52`, `.bin`, `.rom` : images brutes, lues par tous les émulateurs. Le type de cartouche est déduit de la taille du fichier.
* `.car` : image avec en-tête, qui contient le type de cartouche. Lue par atari800 et Altirra, pas par a5200.

Les fichiers peuvent être compressés en `.zip` ou `.7z` (un jeu par archive).

## Contrôles

RetroBat configure automatiquement les manettes. Le joystick analogique de la 5200 est sur le stick gauche, et aussi sur la croix directionnelle (en numérique).

| Manette RetroBat     | libretro: a5200          | libretro: atari800  | altirra             |
| -------------------- | ------------------------ | ------------------- | ------------------- |
| Croix directionnelle | Joystick                 | Joystick            | Joystick            |
| Stick gauche         | Joystick analogique      | Joystick analogique | Joystick analogique |
| SUD                  | Tir 2                    | Tir 1               | Tir 2               |
| EST                  | Tir 1                    | Tir 2               | —                   |
| OUEST                | `*`                      | `#`                 | Tir 1               |
| NORD                 | `#`                      | `*`                 | —                   |
| START                | Start                    | Start               | Start               |
| SELECT               | Pause                    | Pause               | Pause               |
| L1                   | Pavé numérique à l'écran | `0`                 | —                   |
| R1                   | `0`                      | `1`                 | —                   |
| L2                   | `3`                      | `2`                 | —                   |
| R2                   | `1`                      | `3`                 | —                   |
| L3                   | `7`                      | `7`                 | —                   |
| R3                   | `5`                      | Clavier virtuel     | Reset               |

Avec a5200, **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit le rôle de L1 : **JOYSTICK (PAVÉ À L'ÉCRAN)** (défaut) affiche le pavé numérique, choisissez une touche à la croix et validez avec EST. **JOYSTICK (BOUTONS DU PAVÉ DIRECTS)** met la touche `9` sur L1.

Avec atari800, **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1 / JOUEUR 2** reste sur **JOYSTICK ATARI 5200** pour la 5200.

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch. Avec Altirra, seul HOTKEY + START (quitter) est configuré par RetroBat. Voir la page [**Raccourcis**](../../../../navigation/hotkeys.md).

## Dossiers

| Contenu                                            | Dossier                             |
| -------------------------------------------------- | ----------------------------------- |
| Jeux                                               | `roms\atari5200`                    |
| BIOS                                               | `bios`                              |
| Cores libretro : sauvegardes instantanées          | `saves\atari5200\libretro.<core>`   |
| Core atari800 : fichier de configuration du moteur | `emulators\retroarch\.atari800.cfg` |
| Altirra : configuration                            | `emulators\altirra\Altirra.ini`     |

## Guides

### Le pavé numérique

Beaucoup de jeux 5200 utilisent le pavé numérique : choix du niveau, du nombre de joueurs, fonctions en cours de partie (Star Raiders s'en sert pour les vues et les armes). Avec a5200, le pavé à l'écran (L1) donne accès à toutes les touches. Avec atari800, les touches les plus utilisées sont sur les boutons, et le clavier virtuel (R3) donne les autres. Avec Altirra, utilisez un autre émulateur pour ces jeux.

### Jeux à deux sticks

Robotron: 2084 et Space Dungeon se jouaient avec deux manettes posées côte à côte. **CONTRÔLES > HACK CONTRÔLES > DOUBLE STICK** (a5200) ou **CONTRÔLES > HACKS DES MANETTES > DOUBLE STICK** (atari800) met la deuxième manette sur le stick droit. **INVERSER LES PORTS** corrige Wizard of Wor, qui lit les manettes à l'envers.

### Type de cartouche (Altirra)

Avec une image brute, Altirra choisit le type d'après la taille du fichier (4K, 8K, 16K, 32K, Bounty Bob). Si le jeu ne démarre pas, choisissez le type dans **ÉMULATION > CHOIX DE LA CARTOUCHE** (**5200 16K ONE CHIP** ou **TWO CHIPS** pour les jeux de 16K, **5200 64K SUPERCART**…).

### Autres options utiles

<table><thead><tr><th width="110.75">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>a5200</td><td><strong>RENDU VISUEL > MÉLANGE INTER-IMAGE</strong></td><td>Imite la rémanence de l'écran et réduit le scintillement.</td></tr><tr><td>a5200</td><td><strong>AUDIO > FILTRE AUDIO</strong></td><td>Adoucit le son aigu de la puce POKEY.</td></tr><tr><td>atari800</td><td><strong>RENDU VISUEL > PALETTE</strong></td><td>Palettes de couleurs toutes faites.</td></tr><tr><td>altirra</td><td><strong>VIDÉO > STANDARD VIDÉO</strong></td><td><strong>NTSC</strong> (défaut) ou <strong>NTSC 50</strong>.</td></tr></tbody></table>

## Problèmes connus

| Problème                                    | Solution                                                                                                                                |
| ------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Message « Missing BIOS file (5200.rom) »    | a5200 utilise son système intégré. Ajoutez `5200.rom` dans `bios` pour une meilleure compatibilité.                                     |
| Une cartouche `.car` ne démarre pas         | a5200 ne lit pas ce format : utilisez atari800 ou Altirra.                                                                              |
| Le jeu demande une touche du pavé numérique | a5200 : L1 (pavé à l'écran). atari800 : boutons ou clavier virtuel (R3). Voir [**Le pavé numérique**](atari-5200.md#le-pave-numerique). |
| Un jeu 16K ne démarre pas avec Altirra      | Choisissez **5200 16K ONE CHIP** ou **TWO CHIPS** dans **CHOIX DE LA CARTOUCHE**.                                                       |
