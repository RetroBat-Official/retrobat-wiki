---
description: Nintendo
---

# Game Boy Color 2 players

<div align="left"><figure><img src="../../../../.gitbook/assets/image (776).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

Le système **Game Boy Color 2 Players** relie deux Game Boy Color par le câble Game Link, comme [**Game Boy 2 Players**](game-boy-2-players.md) le fait pour les jeux Game Boy : RetroBat lance deux consoles reliées et les affiche côte à côte. Il sert surtout à échanger et combattre dans Pokémon Or, Argent et Cristal, ou à jouer à deux à Mario Tennis, Super Mario Bros. Deluxe…

Le fonctionnement, les options et les `.m3u` sont décrits sur la page [**Game Boy 2 Players**](game-boy-2-players.md), les contrôles sur la page [**Game Boy**](game-boy.md).

{% embed url="https://en.wikipedia.org/wiki/List_of_multiplayer_Game_Boy_games" %}

## En bref

<table><thead><tr><th width="277.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\gbc2players</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gbc .zip .m3u .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: tgbdual</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (manette 1 : console de gauche, manette 2 : console de droite)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                      | Pour qui ?          | Points forts                                                                | Limites |
| ------------------------------ | ------------------- | --------------------------------------------------------------------------- | ------- |
| **libretro: tgbdual** (défaut) | Tout le monde       | Léger, fait pour le jeu à deux, deux jeux différents avec un `.m3u`.        | —       |
| **libretro: sameboy**          | Puristes            | Émulation très précise, correction des couleurs et sortie du son au choix.  | —       |
| **libretro: DoubleCherryGB**   | Joueurs à plusieurs | Jusqu'à **4 consoles** reliées, plusieurs types de câbles et d'adaptateurs. | —       |
| **libretro: gearboy**          | Curieux             | Émulateur récent, sortie du son au choix (une console ou les deux).         | —       |

**En cas de doute, gardez libretro: tgbdual.**

## BIOS

Aucun fichier n'est nécessaire.

## Quel format de jeu ?

<table><thead><tr><th width="124">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gbc</strong></td><td>Image d'une cartouche Game Boy Color : les deux consoles utilisent le même jeu.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive) : les deux consoles utilisent le même jeu.</td></tr><tr><td><strong>.m3u</strong></td><td>Liste de deux jeux : un jeu différent dans chaque console (voir <a href="game-boy-2-players.md#deux-jeux-differents-pokemon"><strong>Deux jeux différents (Pokémon)</strong></a> sur la page <strong>Game Boy 2 Players</strong>).</td></tr></tbody></table>

Exemple, fichier `Pokemon Or + Argent.m3u` dans `roms\gbc2players` :

```
Pokemon - Version Or (France).gbc
Pokemon - Version Argent (France).gbc
```

## Contrôles

RetroBat configure automatiquement les manettes : la première manette joue sur la console de gauche (joueur 1), la deuxième sur celle de droite (joueur 2). Les boutons et les options sont les mêmes que sur la page [**Game Boy**](game-boy.md#controles).

## Dossiers

<table><thead><tr><th width="267.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes des jeux</td><td><code>saves\gbc2players</code></td></tr><tr><td>Sauvegardes instantanées</td><td><p><code>saves\gbc2players\libretro.&#x3C;core></code></p><p>(ex. <code>saves\gbc2players\libretro.tgbdual</code>)</p></td></tr></tbody></table>

## Guides

### Options propres au Game Boy Color

Les options de disposition des écrans, de son et de DoubleCherryGB sont celles de la page [**Game Boy 2 Players**](game-boy-2-players.md). Une seule change :

<table><thead><tr><th width="159.5">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>core sameboy</td><td><strong>RENDU VISUEL > MODE DE CORRECTION DES COULEURS</strong></td><td>Remplace <strong>PALETTE</strong> : corrige les couleurs vives du Game Boy Color (<strong>MODERNE ÉQUILIBRÉ</strong> par défaut).</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="287.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le <code>.m3u</code> ne démarre pas</td><td>Vérifiez que les deux jeux sont dans <code>roms\gbc2players</code> et que les noms du <code>.m3u</code> sont exacts (extension comprise).</td></tr><tr><td>Un jeu Game Boy ne démarre pas</td><td>Rangez-le dans <code>roms\gb2players</code>.</td></tr></tbody></table>
