---
description: Worlds of Wonder
---

# Actionmax

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/actionmax.svg" alt="" width="375"><figcaption></figcaption></figure></div>

Console de jeu - Date de sortie : 1987

{% embed url="https://fr.wikipedia.org/wiki/Action_Max" %}

## Informations

<table data-header-hidden><thead><tr><th width="224"></th><th></th></tr></thead><tbody><tr><td><strong>Emulateurs</strong></td><td><ul><li>hypseus</li><li>singe2</li></ul></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> actionmax</td></tr><tr><td><strong>Extensions</strong></td><td>.actionmax</td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès Rétro</th><th width="200">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>NON</td><td>NON</td><td>Hypseus: OUI<br>Singe2: OUI</td></tr></tbody></table>

## Bios

Pas de BIOS nécessaire.

## Contrôles

TBD

## Information spécifique du système

### Ajout des jeux sur Hypseus - méthode zip

Télécharger ici la version zip du jeu:\
[https://github.com/DirtBagXon/hypseus\_singe\_data/tree/master/00-zip-roms](https://github.com/DirtBagXon/hypseus_singe_data/tree/master/00-zip-roms)

Utiliser la structure suivante (exemple pour 38ambushalley):

```
└── roms/
    └── actionmax/
        ├── roms/
        │   └── actionmax.zip
        └── vldp/
            └── actionmax/
                ├── 38ambushalley.actionmax
                ├── 38ambushalley.dat
                ├── 38ambushalley.m2v
                ├── 38ambushalley.ogg
                ├── 38ambushalley.txt
                ├── video_actionmaxintro.dat
                ├── video_actionmaxintro.m2v
                ├── video_menu.dat
                └── video_menu.m2v
```

Placer les fichiers vidéos et sons du jeu dans le sous-dossier `vdlp\actionmax`.

Créer un fichier vide et le nommer du nom du jeu avec l'extension .actionmax, le place dans le dossier `roms\actionmax\vldp\actionmax` (ici`38ambushalley.actionmax`).

<div align="left"><figure><img src="https://i.imgur.com/4qrVoz7.png" alt=""><figcaption></figcaption></figure></div>

### Ajout des jeux sur Hypseus - ancienne méthode

Les jeux ActionMax sont compatibles avec l'émulateur Hypseus, ils doivent suivre une structure de dossier très spécifique.

Le dossier de jeux actionmax doit être placé dans le dossier `roms\actionmax\actionmax.daphne`et doit contenir exactement les dossiers et fichiers suivants:

```
+---38ambushalley
|       video_38ambushalley.dat
|       video_38ambushalley.m2v
|       video_38ambushalley.ogg
|       
+---bluethunder
|       video_bluethunder.m2v
|       video_bluethunder.ogg
|       
+---hydrosub2021
|       video_hydrosub2021.m2v
|       video_hydrosub2021.ogg
|       
+---popsghostly
|       video_popsghostly.m2v
|       video_popsghostly.ogg
|       
+---sonicfury
        video_sonicfury.m2v
        video_sonicfury.ogg
|
|   38ambushalley.singe
|   38ambushalley.txt
|   bluethunder.singe
|   bluethunder.txt
|   emulator.singe
|   font_bluestone.ttf
|   font_chemrea.ttf
|   font_led_real.ttf
|   framework.singe
|   hydrosub2021.singe
|   hydrosub2021.txt
|   popsghostly.singe
|   popsghostly.txt
|   sonicfury.singe
|   sonicfury.txt
|   sound_actionmax.wav
|   sound_asteadyaimiscritical.wav
|   sound_badhit.wav
|   sound_gameover.wav
|   sound_getreadyforaction.wav
|   sound_goodhit.wav
|   sound_gunshot.wav
|   sprite_38ambushalley.png
|   sprite_actionmax.png
|   sprite_actionmax_orig.png
|   sprite_bluethunder.png
|   sprite_bullet.png
|   sprite_crosshair.png
|   sprite_hydrosub2021.png
|   sprite_lightoff.png
|   sprite_lighton.png
|   sprite_popsghostly.png
|   sprite_sonicfury.png
|   video_actionmaxintro.dat
|   video_actionmaxintro.m2v
|   video_actionmaxintro.ogg
|   video_menu.dat
|   video_menu.m2v
|   video_menu.ogg
```

Créer ensuite un fichier vide du nom du jeu, et le sauver avec l'extension .actionmax, le fichier doit être sauvegardé dans le dossier `roms\actionmax`. (par exemple `38ambushalley.actionmax`):

<div align="left"><figure><img src="https://i.imgur.com/O2iMMLc.png" alt=""><figcaption></figcaption></figure></div>
