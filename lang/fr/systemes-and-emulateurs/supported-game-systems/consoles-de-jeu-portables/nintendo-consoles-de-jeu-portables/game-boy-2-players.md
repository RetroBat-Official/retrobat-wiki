---
description: Nintendo
---

# Game Boy 2 players

<div align="left"><figure><img src="../../../../.gitbook/assets/image (768).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

Le **câble Game Link** relie deux Game Boy : chaque joueur a sa console et sa cartouche. Il sert à jouer à deux (Tetris, Dr. Mario, F-1 Race…) ou à échanger et combattre dans Pokémon Rouge, Bleu et Jaune.

Le système **Game Boy 2 Players** recrée ce branchement : RetroBat lance deux Game Boy reliées et les affiche côte à côte sur le même écran. Le joueur 1 joue sur la console de gauche avec la première manette, le joueur 2 sur celle de droite avec la deuxième. Les deux consoles peuvent utiliser le même jeu ou deux jeux différents (Pokémon Rouge et Bleu).

Les jeux, les contrôles et les raccourcis sont ceux de la page [**Game Boy**](game-boy.md).

{% embed url="https://en.wikipedia.org/wiki/List_of_multiplayer_Game_Boy_games" %}

## En bref

<table><thead><tr><th width="294"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\gb2players</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gb .zip .m3u .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: tgbdual</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (manette 1 : console de gauche, manette 2 : console de droite)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                      | Pour qui ?          | Points forts                                                                | Limites |
| ------------------------------ | ------------------- | --------------------------------------------------------------------------- | ------- |
| **libretro: tgbdual** (défaut) | Tout le monde       | Léger, fait pour le jeu à deux, deux jeux différents avec un `.m3u`.        | —       |
| **libretro: sameboy**          | Puristes            | Émulation très précise, palette et sortie du son au choix.                  | —       |
| **libretro: DoubleCherryGB**   | Joueurs à plusieurs | Jusqu'à **4 consoles** reliées, plusieurs types de câbles et d'adaptateurs. | —       |
| **libretro: gearboy**          | Curieux             | Émulateur récent, sortie du son au choix (une console ou les deux).         | —       |

**En cas de doute, gardez libretro: tgbdual.**

## BIOS

Aucun fichier n'est nécessaire.

## Quel format de jeu ?

<table><thead><tr><th width="165.25">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gb</strong></td><td>Image d'une cartouche Game Boy : les deux consoles utilisent le même jeu.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive) : les deux consoles utilisent le même jeu.</td></tr><tr><td><strong>.m3u</strong></td><td>Liste de deux jeux : un jeu différent dans chaque console (voir <a href="game-boy-2-players.md#deux-jeux-differents-pokemon"><strong>Deux jeux différents (Pokémon)</strong></a>).</td></tr></tbody></table>

## Contrôles

RetroBat configure automatiquement les manettes : la première manette joue sur la console de gauche (joueur 1), la deuxième sur celle de droite (joueur 2). Les boutons, les options **INVERSER LES BOUTONS A/B/X/Y** et **REMAPPER SELECT SUR** sont les mêmes que sur la page [**Game Boy**](game-boy.md).

Les raccourcis sont ceux de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

<table><thead><tr><th width="280.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes des jeux</td><td><code>saves\gb2players</code></td></tr><tr><td>Sauvegardes instantanées</td><td><p><code>saves\gb2players\libretro.&#x3C;core></code></p><p>(ex. <code>saves\gb2players\libretro.tgbdual</code>)</p></td></tr></tbody></table>

## Guides

### Deux jeux différents (Pokémon)

Pour échanger ou combattre entre Pokémon Rouge et Pokémon Bleu, il faut un jeu différent dans chaque console. Créez un fichier `.m3u` dans `roms\gb2players`, avec le nom des deux jeux, un par ligne. Le premier jeu va dans la console du joueur 1, le second dans celle du joueur 2.

Exemple, fichier `Pokemon Rouge + Bleu.m3u` :

```
Pokemon - Version Rouge (France).gb
Pokemon - Version Bleue (France).gb
```

<div align="left"><figure><img src="../../../../.gitbook/assets/image (769).png" alt=""><figcaption></figcaption></figure></div>

Les deux jeux doivent se trouver dans `roms\gb2players`, à côté du `.m3u`. Les quatre émulateurs acceptent les `.m3u`.

### Disposition des écrans et son

<table><thead><tr><th width="208.25">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>core tgbdual, core sameboy, core gearboy</td><td><strong>VIDÉO > POSITIONNEMENT DES ÉCRANS</strong></td><td><strong>COTE À COTE</strong> (défaut) ou <strong>HAUT / BAS</strong>.</td></tr><tr><td>core DoubleCherryGB</td><td><strong>VIDÉO > POSITIONNEMENT DES ÉCRANS</strong></td><td><strong>ÉCRAN SÉPARÉ (STANDARD)</strong> (défaut), <strong>DE HAUT EN BAS</strong> ou <strong>DE GAUCHE À DROITE</strong>.</td></tr><tr><td>core sameboy, core DoubleCherryGB</td><td><strong>AUDIO > SORTIE AUDIO</strong></td><td>Son de la console 1 (défaut) ou d'une autre console.</td></tr><tr><td>core gearboy</td><td><strong>AUDIO > SORTIE AUDIO</strong></td><td>Son de la console 1 (défaut), de la console 2 ou <strong>MIXAGE</strong> des deux.</td></tr><tr><td>core sameboy</td><td><strong>RENDU VISUEL > PALETTE</strong></td><td>Niveaux de gris (défaut), citron vert, olive ou bleu sarcelle.</td></tr></tbody></table>

### Jouer à 3 ou 4 (DoubleCherryGB)

Quelques jeux se jouent à quatre avec l'adaptateur 4 joueurs de Nintendo (F-1 Race, Wave Race…) ou avec un câble en anneau (Faceball 2000). Avec le core DoubleCherryGB :

1. Choisissez le nombre de consoles dans **ÉMULATION > NOMBRE DE JOUEURS** (2 par défaut, jusqu'à 4).
2. Choisissez le branchement dans **ÉMULATION > TYPE DE CÂBLE MULTIJOUEURS** : **CÂBLE LINK 2 JOUEURS**, **ADAPTATEUR 4 JOUEURS**, **CÂBLE EN ANNEAU FACEBALL 2000**, ou les adaptateurs des hacks multijoueurs de Tetris et Kwirk. Par défaut, le core choisit lui-même.

Chaque console reçoit une manette, dans l'ordre des joueurs.

## Problèmes connus

<table><thead><tr><th width="344">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le <code>.m3u</code> ne démarre pas</td><td>Vérifiez que les deux jeux sont dans <code>roms\gb2players</code> et que les noms du <code>.m3u</code> sont exacts (extension comprise).</td></tr><tr><td>Un seul joueur répond</td><td>Branchez une deuxième manette avant de lancer le jeu.</td></tr><tr><td><strong>GRILLE</strong> n'a pas d'effet (DoubleCherryGB)</td><td>Ce choix n'existe pas dans la version actuelle du core : utilisez <strong>ÉCRAN SÉPARÉ (STANDARD)</strong>.</td></tr><tr><td>Un jeu Game Boy Color ne démarre pas</td><td>Rangez-le dans <code>roms\gbc2players</code>.</td></tr></tbody></table>
