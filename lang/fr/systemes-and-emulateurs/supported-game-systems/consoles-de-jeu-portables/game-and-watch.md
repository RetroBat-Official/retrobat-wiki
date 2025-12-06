---
description: G&W
---

# Game & Watch

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/5149a33eed46b2af638b06119397d4023b75131f/art/logos/gameandwatch.svg" alt=""><figcaption></figcaption></figure></div>

Console de jeu portable - Durée de vie : 1980 - 1991

{% embed url="https://fr.wikipedia.org/wiki/Game_and_Watch" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro : gw</li><li>libretro : mame</li><li>mame64</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span>roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> gameandwatch</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.mgw .zip .7z</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>NON</td></tr></tbody></table>

## BIOS

Aucun BIOS nécessaire.

## Contrôles

Les contrôles sont spécifiques à chaque jeu.

<table><thead><tr><th width="258">RetroBat</th><th width="443">Game &#x26; Watch</th></tr></thead><tbody><tr><td>START</td><td>START</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>D-PAD</td><td>Stick</td></tr><tr><td>Stick analogique gauche</td><td>Stick</td></tr><tr><td>Stick analogique droit</td><td></td></tr><tr><td><img src="../../../.gitbook/assets/image (20).png" alt="A"></td><td>B</td></tr><tr><td><img src="../../../.gitbook/assets/image (7).png" alt="B"></td><td>A</td></tr><tr><td><img src="../../../.gitbook/assets/image (35).png" alt="" data-size="original"></td><td>X</td></tr><tr><td><img src="../../../.gitbook/assets/image (33).png" alt="" data-size="line"></td><td>Y</td></tr><tr><td>L1</td><td>5</td></tr><tr><td>R1</td><td>6</td></tr><tr><td>L2</td><td></td></tr><tr><td>R2</td><td></td></tr><tr><td>L3</td><td></td></tr><tr><td>R3</td><td></td></tr></tbody></table>

## Information spécifique au système

### Comment ajouter et lancer les jeux

L'émulateur (le cœur Retroarch) "**Handheld Electronic (GW)**" est utilisé pour jouer à un nombre limité de jeux :

<details>

<summary>Liste des jeux fonctionnant avec le cœur "<strong>Handheld Electronic (GW)</strong>"</summary>

```
"Armor Battle"
"Banana (Time & Fun)"
"Baseball (Explorer Time & Fun)"
"Bomb Fight (Mini Time & Fun)"
"Caccia al Ladro (Mini Time & Fun)"
"Cessate il Fuoco (Mini Time & Fun)"
"Chicky Woggy (Arcade Time & Fun)"
"Chicky Woggy (Electronic Tini-Arcade)"
"Condor (Time & Fun)"
"Crazy Chewy (Electronic Tini-Arcade)"
"Defendo (Explorer Time & Fun)"
"Donkey Angler (LCD Card Game)"
"Donkey Kong"
"Donkey Kong (Multi Screen)"
"Donkey Kong Circus (Panorama Screen)"
"Donkey Kong II (Multi Screen)"
"Donkey Kong Jr."
"Donkey Kong Jr. (Panorama Screen)"
"Donkey Kong Jr. (Table Top)"
"Dungeons & Dragons Computer Fantasy Game (Arcade
"Egg (Wide Screen)"
"Engine Room (Explorer Time & Fun)"
"Escape (Time & Fun)"
"Explorers of Space"
"Fowling"
"Frog Boaster"
"Galaxy II"
"Grab Man (Game & Time)"
"Hippo Teeth (Mini Time & Fun)"
"Hippo Teeth (Sporty Time & Fun)"
"Hot Line (Mini Time & Fun)"
"Hot Line (Sporty Time & Fun)"
"Las Vegas (LCD Game Digital)"
"Lifeboat (Multi Screen)"
"Mario Bros. (Multi Screen)"
"Mario's Bombs Away (Panorama Screen)"
"Mickey Mouse (Panorama Screen)"
"Mickey Mouse (Wide Screen)"
"Monkey (Time & Fun)"
"Monkey Jump (Arcade Time & Fun)"
"Motor Cross"
"Pac Man"
"Pancake (Time & Fun)"
"Parachute (Wide Screen)"
"Penguin Land (LSI Game Double Play)"
"Pirate (Time & Fun)"
"Roller Coaster (Explorer Time & Fun)"
"Safari (Time & Fun)"
"Sleep Walker (Time & Fun)"
"Snoopy (Panorama Screen)"
"Snoopy (Table Top)"
"Snoopy Tennis (Wide Screen)"
"Sub Chase"
"Tennis Menace (Sporty Time & Fun)"
"Tom & Jerry Popper (LCD Card Game)"
"Towering Rescue (LCD Card Game)"
"Tron"
"Turtle Bridge (Wide Screen)"
"Wild Man Jump (Electronic Tini-Arcade)"
```

</details>

Beaucoup d'autres jeux LCD ne sont pas compatibles avec le cœur "gw".\
Pour jouer à ces jeux il faut utiliser le coeur **MAME**.<br>

Ces jeux nécessitent deux fichiers pour fonctionner correctement: un fichier de jeu "_**rom**"_ et un fichier "_**artwork**"_.\
\
Le fichier ROM au format zip doit être placé dans le dossier `\roms\gameandwatch`.

<div align="left"><figure><img src="https://i.imgur.com/ALEygG9.png" alt=""><figcaption></figcaption></figure></div>

Le fichier artwork (également au format zip) doit être placé dans le dossier `\saves\mame\artwork`, le nom du fichier doit être exactement identique au fichier de jeu ROM.

Enfin, dans Retrobat, aller dans le système **Game & Watch** et [modifier l'émulateur pour le jeu](../../../premiers-pas/running-a-game.md#selectionner-un-emulateur-different).
