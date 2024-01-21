---
description: Nintendo
---

# Nintendo 64 Disk Drive

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/n64dd-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/n64dd.svg" alt=""></picture><figcaption></figcaption></figure>

</div>

Extension de console de jeu - Durée de vie : 1999- 2001

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_64DD" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>mupen64 (RMG)</li><li>libretro: mupen64plus next</li><li>libretro: parallel_n64 (uniquement pour les jeux full ndd)</li><li>ares</li><li>project64</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> n64dd</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.v64 .z64 .n64 .ndd</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="256">Succès Rétro</th><th width="243">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>RMG : NON<br>lr-mupen64 : OUI<br>lr-parallel : OUI<br>Ares : NON<br>Project64 : NON</td><td>RMG : NON<br>lr-mupen64 : OUI<br>lr-parallel : OUI<br>Ares : NON<br>Project64: NO</td><td>RMG : OUI<br>lr-mupen64 : OUI<br>lr-parallel : OUI<br>Ares : OUI<br>Project64 : NON</td></tr></tbody></table>

## BIOS

<table data-header-hidden><thead><tr><th width="206"></th><th width="533"></th><th data-hidden></th></tr></thead><tbody><tr><td>IPL_JAP.n64<br>Japan</td><td><strong>Emplacement:</strong> \bios\Mupen64plus<br><strong>md5:</strong> <code>8d3d9f294b6e174bc7b1d2fd1c727530</code></td><td></td></tr><tr><td>IPL_USA.n64<br>USA</td><td><strong>Emplacement:</strong> \bios\Mupen64plus<br><strong>md5:</strong> <code>37c36e4286d36892a9fc70eafe4104be</code></td><td></td></tr><tr><td>IPL_DEV.n64<br>Development Kit</td><td><strong>Emplacement:</strong> \bios\Mupen64plus<br><strong>md5:</strong> </td><td></td></tr></tbody></table>

## Contrôles

Similaire au système [N64](nintendo-64.md#controls)

## Information spécifique au système

### Lancement des jeux n64DD avec Mupen64Plus-next

Il existe 2 formats de jeux disponibles pour le système Nintendo 64DD, les jeux complets et les extensions de jeux.&#x20;

Afin de faire fonctionner les jeux n64dd correctement, il est nécessaire d'avoir **2 fichiers par jeu**.&#x20;

* une ROM de jeu n64 classique (format .n64 ou .z64)
* un fichier n64dd au format .ndd, représentant l'extension disponible sur le système n64DD (ou le jeu n64DD complet).&#x20;

Les deux fichiers doivent avoir exactement le même nom, le fichier .ndd du système n64dd doit avoir une double extension (celle de la ROM du jeu + l'extension .ndd).

#### Lancement de jeux avec extension 64DD

Dans le cas des extensions de jeu, le fichier .n64 représente la ROM du jeu et le fichier .ndd en est l'extension n64DD.

Exemple pour l'extension n64DD du jeu "F-Zero X" (F-Zero X Expansion Kit):

* Renommer le fichier n64dd .ndd \
  `F-Zero X - Expansion Kit (Japan).ndd`\
  en\
  `F-Zero X - Expansion Kit (Japan).n64.ndd`
* Renommer la ROM de jeu\
  `F-Zero X (Japan).n64`\
  &#x20;en \
  `F-Zero X - Expansion Kit (Japan).n64`
* Lancer la version n64DD du jeu en lançant le fichier\
  `F-Zero X - Expansion Kit (Japan).n64`

Depuis RetroBat:&#x20;

* [Sélectionner le BIOS approprié](nintendo-64-disk-drive.md#selection-du-bios)
* Lancer le jeu au format .n64 (ou .z64), pas le fichier .ndd :

<div align="left">

<figure><img src="https://i.imgur.com/9oo9rAy.png" alt=""><figcaption></figcaption></figure>

</div>

#### Lancer un jeu complet Nintendo 64 DD

Dans le cas des jeux complets n64DD, le fichier .ndd ne suffit pas pour lancer le jeu, l'émulateur nécessite la présence de 2 fichiers. Il convient donc d'ajouter un fichier .n64 en copiant une autre ROM de jeu n64 (peu importe laquelle car elle ne sera pas réellement utilisée) et en la renommant du même nom que le fichier .ndd (sans l'extension .ndd mais avec l'extension .n64).

Exemple avec le jeu n64DD complet "SimCity 64":

* Renommer `SimCity 64 (Japan).ndd` en `SimCity 64 (Japan).n64.ndd`
* Choisir une ROM de jeu n64 (n'importe laquelle) et la copier en la renommant `SimCity 64 (Japan).n64`
* Lancer `SimCity 64 (Japan).n64` depuis RetroBat.

Depuis RetroBat:&#x20;

* [Sélectionner le BIOS approprié](nintendo-64-disk-drive.md#selection-du-bios)
* Lancer le jeu au format .n64 (ou .z64), pas le fichier .ndd :

<div align="left">

<figure><img src="https://i.imgur.com/zc3ex6s.png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="warning" %}
ATTENTION: le core est très sensible à la version de la rom .ndd utilisée, seul les dumps légitimes fonctionnent correctement.

Si, au lieu de lancer le jeu 64DD, c'est le jeu correspondant à la fausse rom qui se lance, cela signifie que le dump .ndd utilisé n'est pas bon.
{% endhint %}

### Sélection du BIOS

Bien que le système ait été disponible uniquement au Japon, il existe des jeux au format US ou encore des prototypes de jeux; dans les 2 cas, un BIOS spécifique est requis pour lancer les jeux.

Le BIOS à utiliser pour chaque jeu peut être spécifié directement dans les options avancées du jeu.

<div align="left">

<figure><img src="https://i.imgur.com/htqkK3Q.png" alt=""><figcaption><p>Advanced System Options / Emulation / BIOS</p></figcaption></figure>

</div>
