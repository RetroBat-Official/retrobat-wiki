# Le Guide Arcade

<div align="left"><figure><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/52ff37c9e265587d006945a2ba695b5a962b3a3d/art/logos/arcade.svg" alt=""><figcaption></figcaption></figure></div>

## Introduction

Les émulateurs Arcade peuvent être catégorisés de la façon suivante:

* Les émulateurs Multi-Machines
* Les émulateurs Mono-Machine

L'émulation Arcade est complexe, car il existe de nombreuses machines différentes, c'est pourquoi les émulateurs sont très actifs et constamment en développement.



Dans ce court guide, nous nous pencherons sur les deux familles d'émulateurs citées précédemment et tenterons de vous donner les clés pour comprendre le monde de l'émulation "Arcade".

## Les Émulateurs Multi-Machines

Il existe deux familles d'émulateurs Multi-Systèmes Arcade: FinalBurn et MAME.&#x20;

Ces émulateurs sont disponibles dans de multiples versions et il est nécessaire d'associer les bons fichiers de jeux (ROM set) à chaque émulateur.



### Liste des émulateurs Multi-ARCADE disponibles

<table><thead><tr><th width="259">Emulator/core</th><th width="160">ROMs folder</th><th>ROM set version</th></tr></thead><tbody><tr><td>libretro: mame (current)</td><td><code>\roms\mame</code></td><td>0.280</td></tr><tr><td>libretro: mame2016</td><td><code>\roms\mame</code></td><td>0.174</td></tr><tr><td>libretro: mame2014</td><td><code>\roms\mame</code></td><td>0.159</td></tr><tr><td>libretro: mame2010</td><td><code>\roms\mame</code></td><td>0.139</td></tr><tr><td>Libretro: mame2003_plus</td><td><code>\roms\mame</code></td><td>0.78plus</td></tr><tr><td>Libretro: mame2003</td><td><code>\roms\mame</code></td><td>0.78</td></tr><tr><td>Libretro: mame2000</td><td><code>\roms\mame</code></td><td>0.37b5</td></tr><tr><td>mame (standalone)</td><td><code>\roms\mame</code></td><td>0.280</td></tr><tr><td>Libretro: fbneo</td><td><code>\roms\fbneo</code></td><td>dernier romset FBNEO</td></tr><tr><td>Libretro: fbalpha</td><td><code>\roms\fbneo</code></td><td>0.2.97.44</td></tr><tr><td>Libretro: fbalpha2012</td><td><code>\roms\fbneo</code></td><td>0.2.97.29</td></tr><tr><td>FBNEO</td><td><code>\roms\fbneo</code></td><td>dernier romset FBNEO</td></tr></tbody></table>

MAME est généralement utilisé pour les jeux Arcade de type "classiques" (tels Pac-Man, Asteroids, etc.).

FBNEO est spécialisé dans les jeux de combats, il est compatible avec moins de jeux mais émule les jeux compatibles de façon plus optimisée.



## Les Emulateurs Mono-Machine

<table><thead><tr><th width="302">Arcade Machine(s)</th><th width="248">Dossier des roms</th><th>Emulateur</th></tr></thead><tbody><tr><td>Jeux LaserDisc</td><td><code>\roms\daphne</code></td><td>Hypseus<br>Daphne</td></tr><tr><td>ATOMISWAVE</td><td><code>\roms\atomiswave</code></td><td>FLYCAST<br>Demul</td></tr><tr><td>DICE</td><td><code>\roms\dice</code></td><td>libretro-dice</td></tr><tr><td>GAELCO</td><td><code>\roms\gaelco</code></td><td>Demul</td></tr><tr><td>SEGA MODEL 2</td><td><code>\roms\model2</code></td><td>m2emulator</td></tr><tr><td>SEGA MODEL 3</td><td><code>\roms\model3</code></td><td>Supermodel</td></tr><tr><td>SEGA NAOMI</td><td><code>\roms\naomi</code></td><td><p>FLYCAST</p><p>Demul</p></td></tr><tr><td>SEGA NAOMI 2</td><td><code>\roms\naomi2</code></td><td><p>FLYCAST</p><p>Demul</p></td></tr><tr><td>HIKARU</td><td><code>\roms\hikaru</code></td><td>Demul</td></tr><tr><td>TRIFORCE</td><td><code>\roms\triforce</code></td><td>DOLPHIN</td></tr><tr><td>CHIHIRO</td><td><code>\roms\chihiro</code></td><td>CXBX-RELOADED</td></tr><tr><td>ARCADE "PC-Based"</td><td><code>\roms\teknoparrot</code></td><td>TEKNOPARROT</td></tr><tr><td>ZINC</td><td><code>\roms\zinc</code></td><td>ZINC<br>PSXMame</td></tr></tbody></table>



## ROMs

### Terminologie

* **ROM, ROM set, et romset**: les jeux Arcade sont contenus dans des fichiers .zip qui peuvent être composés d'un ou plusieurs fichiers ROM(s). \
  C'est pour cette raison que les fichiers de jeux Arcade peuvent être désignés par les termes ROM, ROM set ou encore romset.\

* **Version de ROM (ou romset)**: Chaque version d'un émulateur Arcade est prévu pour fonctionner un un romset particulier.\
  Par exemple  l'émulateur MAME 2000 fonctionne avec le romset MAME 0.37b5 alors que l'émulateur MAME 2010 nécessite le romset MAME 0.139.\


### Type de romset

Il existe 4 formats de romset:

* **Full Non-merged**: chaque fichier de jeu (ROM) est "autosuffisant", le zip inclut tout le nécessaire pour lancer le jeu (les bios, les rom parents, etc.).\

* **Non-merged ROM**: identique au "Full Non-merged" à l'exception de certains BIOS communs à plusieurs ROMs qui doivent être placés dans le dossier des jeux et sont partagés entre plusieurs fichiers roms.\

* **Split**: chaque version d'un jeu est dans un fichier séparé, certains jeux (clônes, traductions, versions différentes) ne fonctionnent pas sans la présence des roms "parents". \
  Par exemple, le jeu `pacman.zip` (un clône) ne fonctionnera pas sans le jeu `puckman.zip` (le 'parent').\

* **Merged**: les clônes et versions alternatives d'un jeu sont contenues dans le même zip que la rom 'parent'. Cela signifie qu'un fichier zip contiendra plusieurs jeux.\


{% hint style="warning" %}
Retrobat et le core libretro:mame ne sont pas compatibles avec les romsets de type 'merged', seule le jeu principal sera vu dans l'interface et pourra être lancé.

Retrobat recommande l'utilisation de sets 'non-merged'.
{% endhint %}

{% hint style="info" %}
Ne pas renommer les fichiers zip. Les scrapeurs savent reconnaître les jeux et affecter le bon titre de jeu à chaque fichier.
{% endhint %}

## Fichiers additionnels

### Samples

Certains jeux nécessitent des fichiers 'samples' pour fonctionner correctement.&#x20;

Les fichiers 'samples' doivent être placés dans les dossiers suivants:

* Pour fbneo: `\bios\fbneo\samples`
* Pour mame2003: `\bios\mame2003\samples`
* Pour mame2003plus: `\bios\mame2003-plus\samples`
* Pour mame2010: `\bios\mame2010\samples`
* Pour mame (current) et mame standalone: `\bios\mame\samples`

### Fichiers CHD (ou IMG)

Certains jeux d'arcade nécessitent la présence de fichiers additionnels (ces fichiers étaient à l'origine des données stockées sur un disque physique ou un disque dur dans la machine arcade).

Il s'agit de fichiers CHD ou IMG, qui doivent être placés dans le même dossier que les jeux, à l'intérieur d'un répertoire portant le même nom que le fichier .zip du jeu.

Par exemple, pour jouer au jeu Killer Instinct (`kinst.zip`), il est nécessaire de placer les fichiers CHD dans le dossier `kinst\kinst.chd`.

<div align="left"><figure><img src="https://i.imgur.com/xl9iImN.png" alt=""><figcaption></figcaption></figure></div>

## Liens et références

{% hint style="info" %}
**Crédits**

Une grande partie des informations partagées sur cette page ont été copiées depuis la documentation libretro (avec leur accord):

[https://docs.libretro.com/guides/arcade-getting-started/](https://docs.libretro.com/guides/arcade-getting-started/)
{% endhint %}
