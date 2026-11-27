---
description: Nintendo
---

# Game Boy Advance 2 players

## Présentation

Le **câble Game Link** de la Game Boy Advance relie jusqu'à quatre consoles. Il sert à jouer ensemble (Mario Kart: Super Circuit, The Legend of Zelda: Four Swords, Bomberman Tournament…) et à échanger ou combattre dans les Pokémon de la Game Boy Advance.

Le système **Game Boy Advance 2 Players** recrée ce branchement : RetroBat lance de 2 à 4 consoles reliées et les affiche ensemble sur le même écran. Chaque joueur joue avec sa manette, dans l'ordre des joueurs. Les consoles peuvent utiliser le même jeu ou des jeux différents (Pokémon Rubis et Saphir).

Les jeux, les boutons et les options d'image sont ceux de la page [**Game Boy Advance**](game-boy-advance.md).

{% embed url="https://en.wikipedia.org/wiki/List_of_Game_Boy_Advance_games" %}

## En bref

<table><thead><tr><th width="270.25"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\gba2players</code></td></tr><tr><td><strong>Extensions</strong></td><td>.gba .zip .7z .m3u</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: mgba_splitscreen</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (<code>gba_bios.bin</code> optionnel)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique avec mgba_splitscreen (manette 1 : joueur 1…), à faire dans NO$GBA</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core libretro ; NO$GBA par son menu</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="164">Émulateur</th><th width="116.75">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: mgba_splitscreen</strong> (défaut)</td><td>Tout le monde</td><td>2 à 4 consoles mGBA reliées, jeux différents avec un <code>.m3u</code>, plusieurs dispositions des écrans, aide pour Four Swords.</td><td>Pas de RetroAchievements.</td></tr><tr><td><strong>nosgba</strong></td><td>Curieux</td><td>NO$GBA, 2 à 4 consoles reliées.</td><td>Manettes à configurer dans NO$GBA. Un seul jeu à la fois (pas de <code>.m3u</code>).</td></tr></tbody></table>

**En cas de doute, gardez libretro: mgba\_splitscreen.**

## BIOS

Aucun fichier n'est nécessaire. `gba_bios.bin` (voir la page [**Game Boy Advance**](game-boy-advance.md#bios)) est utilisé par mgba\_splitscreen s'il est présent.

## Quel format de jeu ?

<table><thead><tr><th width="145.25">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.gba</strong></td><td>Image d'une cartouche Game Boy Advance : toutes les consoles utilisent le même jeu.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive) : toutes les consoles utilisent le même jeu.</td></tr><tr><td><strong>.m3u</strong></td><td>Liste de 2 à 4 jeux : un jeu différent dans chaque console (voir <a href="game-boy-advance-2-players.md#des-jeux-differents-pokemon"><strong>Des jeux différents (Pokémon)</strong></a>). mgba_splitscreen seulement.</td></tr></tbody></table>

## Contrôles

Avec mgba\_splitscreen, RetroBat configure automatiquement les manettes : la première manette joue sur la console du joueur 1, la deuxième sur celle du joueur 2, etc. Les boutons et l'option **INVERSER LES BOUTONS A/B/X/Y** sont les mêmes que sur la page [**Game Boy Advance**](game-boy-advance.md#controles).

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/gba_turbo.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

Avec NO$GBA, RetroBat ne configure pas les manettes : réglez-les dans les options de NO$GBA. HOTKEY + START (ou `Échap`) le quitte.

Les raccourcis de mgba\_splitscreen sont ceux de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

<table><thead><tr><th width="325.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes des jeux</td><td><code>saves\gba2players</code></td></tr><tr><td>mgba_splitscreen : sauvegardes instantanées</td><td><code>saves\gba2players\libretro.mgba_splitscreen</code></td></tr><tr><td>NO$GBA : sauvegardes instantanées</td><td><code>saves\gba2players\nosgba\sstates</code></td></tr></tbody></table>

## Guides

### Nombre de joueurs et disposition des écrans

<table><thead><tr><th width="208.25">Émulateur</th><th>Option</th><th>Effet</th></tr></thead><tbody><tr><td>core mgba_splitscreen</td><td><strong>ÉMULATION > NOMBRE DE JOUEURS</strong></td><td>Nombre de consoles qui lancent le même jeu : 2 (défaut), 3 ou 4. Avec un <code>.m3u</code>, une console par jeu.</td></tr><tr><td>core mgba_splitscreen</td><td><strong>VIDÉO > DISPOSITION DES VUES</strong></td><td><strong>CÔTE À CÔTE (2x1)</strong>, <strong>EMPILÉ (1x2)</strong>, <strong>QUADRANTS (2x2)</strong>, <strong>PRINCIPAL (GRAND + BANDEAU)</strong>, <strong>JOUEUR ACTIF (UN SEUL ÉCRAN)</strong> ou <strong>INCRUSTATION (GRAND + VIGNETTES)</strong>. Par défaut, côte à côte à 2 joueurs, en quadrants à 4.</td></tr><tr><td>core mgba_splitscreen</td><td><strong>ÉMULATION > JOUEUR ACTIF</strong></td><td>Console agrandie dans les vues principal, joueur actif et incrustation.</td></tr><tr><td>core mgba_splitscreen</td><td><strong>VIDÉO > CONTOURS ET BADGES DES JOUEURS</strong></td><td>Cadre de couleur et numéro sur l'écran de chaque joueur (activé par défaut).</td></tr><tr><td>core mgba_splitscreen</td><td><strong>AUDIO > SOURCE AUDIO</strong></td><td>Son du joueur 1 (défaut), d'un autre joueur ou <strong>MIXAGE</strong> de toutes les consoles.</td></tr><tr><td>core mgba_splitscreen</td><td><strong>AUDIO > FILTRE AUDIO</strong>, <strong>AUDIO > LIMITEUR AUDIO</strong></td><td>Adoucit le son et évite la saturation quand le son de plusieurs consoles est mélangé (activés par défaut).</td></tr><tr><td>NO$GBA</td><td><strong>ÉMULATION > NOMBRE DE JOUEURS</strong></td><td>2 (défaut), 3 ou 4 consoles.</td></tr></tbody></table>

### Des jeux différents (Pokémon)

Pour échanger ou combattre entre deux versions de Pokémon, chaque console a besoin de son jeu. Créez un fichier `.m3u` dans `roms\gba2players`, avec le nom des jeux, un par ligne. Le premier jeu va dans la console du joueur 1, le deuxième dans celle du joueur 2, etc. (4 jeux au plus).

Exemple, fichier `Pokemon Rubis + Saphir.m3u` :

```
Pokemon - Version Rubis (France).gba
Pokemon - Version Saphir (France).gba
```

Les jeux doivent se trouver dans `roms\gba2players`, à côté du `.m3u`. Chaque joueur garde la sauvegarde de son jeu.

Trois ou quatre jeux servent surtout aux Pokémon de la Game Boy Advance : combat Multi à 4 (2 contre 2), Mixeur à baies (Rubis, Saphir, Émeraude), échanges entre versions différentes.

### The Legend of Zelda: Four Swords

La liaison de Four Swords échoue parfois au démarrage de la partie. Activez **ÉMULATION > ASSISTANCE LIAISON FOUR SWORDS** (core mgba\_splitscreen) pour l'aider.

## Problèmes connus

<table><thead><tr><th width="341.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le <code>.m3u</code> ne démarre pas</td><td>Vérifiez que les jeux sont dans <code>roms\gba2players</code> et que les noms du <code>.m3u</code> sont exacts (extension comprise). Le <code>.m3u</code> n'est pas lu par NO$GBA.</td></tr><tr><td>Un joueur ne répond pas</td><td>Branchez toutes les manettes avant de lancer le jeu (mgba_splitscreen) ; avec NO$GBA, configurez les manettes dans ses options.</td></tr><tr><td>Four Swords ne trouve pas les autres joueurs</td><td>Voir <a href="game-boy-advance-2-players.md#the-legend-of-zelda-four-swords"><strong>The Legend of Zelda: Four Swords</strong></a>.</td></tr><tr><td>Je veux jouer seul</td><td>Ce système est réservé au jeu à plusieurs : rangez le jeu dans <code>roms\gba</code>.</td></tr></tbody></table>
