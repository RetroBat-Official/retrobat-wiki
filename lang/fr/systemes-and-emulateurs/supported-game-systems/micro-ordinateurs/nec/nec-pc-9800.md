---
description: NEC
---

# NEC PC-9800

<div align="left">

<figure><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/pc98-w.svg" media="(prefers-color-scheme: dark)"><img src="https://i.imgur.com/Cn9WzBZ.png" alt=""></picture><figcaption></figcaption></figure>

</div>

Micro-ordinateur - Date de sortie : 1982

{% embed url="https://fr.wikipedia.org/wiki/PC-98" %}

## Information

<table data-header-hidden><thead><tr><th width="184"></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><strong>Émulateurs</strong></td><td><ul><li>libretro : np2kai</li><li>libretro : nekop2</li></ul></td><td></td></tr><tr><td><strong>Dossier des jeux</strong></td><td><span data-gb-custom-inline data-tag="emoji" data-code="1f4c1">📁</span> roms \ <span data-gb-custom-inline data-tag="emoji" data-code="1f4c2">📂</span> pc98</td><td></td></tr><tr><td><strong>Extensions</strong></td><td>.d98 .zip .98d .fdi .fdd .2hd .tfd .d88 .88d .hdm .xdf .dup .cmd .hdi .thd .nhd .hdd .hdn .cue</td><td></td></tr></tbody></table>

## Fonctionnalités

<table><thead><tr><th width="245">Succès Rétro</th><th width="200">Parties en Réseau</th><th>Auto configuration des contrôles</th></tr></thead><tbody><tr><td>lr-np2kai : NON<br>lr-nekop2 : NON</td><td>lr-np2kai : OUI<br>lr-nekop2 : NON</td><td>lr-np2kai : OUI<br>lr-nekop2 : OUI</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="193">Fichier BIOS</th><th width="173.03610108303252">Dossier</th><th>md5</th></tr></thead><tbody><tr><td>BIOS.ROM</td><td><code>\bios\np2kai</code></td><td>e246140dec5124c5e404869a84caefce</td></tr><tr><td>FONT.ROM</td><td><code>\bios\np2kai</code></td><td>2af6179d7de4893ea0b705c00e9a98d6</td></tr><tr><td>SOUND.ROM</td><td><code>\bios\np2kai</code></td><td>caf90f22197aed6f14c471c21e64658d</td></tr><tr><td>ITF.ROM</td><td><code>\bios\np2kai</code></td><td>e9fc3890963b12cf15d0a2eea5815b72</td></tr><tr><td>font.bmp</td><td><code>\bios\np2kai</code></td><td>7da1e5b7c482d4108d22a5b09631d967</td></tr></tbody></table>

## Contrôles

Utiliser la fonctionnalité [Pad2Key](../../../../controleurs/pad2key.md).

<table><thead><tr><th width="311">Retrobat</th><th>PC-98</th></tr></thead><tbody><tr><td>START</td><td>ENTREE</td></tr><tr><td>SELECT</td><td>ECHAP</td></tr><tr><td>D-PAD</td><td>Flèches directionnelles</td></tr><tr><td>Stick analogique gauche</td><td></td></tr><tr><td>Stick analogique droit</td><td></td></tr><tr><td><img src="../../../../.gitbook/assets/image (32).png" alt=""></td><td>CTRL gauche</td></tr><tr><td><img src="../../../../.gitbook/assets/image (19).png" alt=""></td><td>Z</td></tr><tr><td><img src="../../../../.gitbook/assets/image (6).png" alt=""></td><td>X</td></tr><tr><td><img src="../../../../.gitbook/assets/image (34).png" alt=""></td><td>ESPACE</td></tr><tr><td>L1</td><td>Backspace</td></tr><tr><td>R1</td><td>MAJ droit</td></tr><tr><td>L2</td><td></td></tr><tr><td>R2</td><td>Ouvrir le menu de l'émulateur</td></tr><tr><td>L3</td><td></td></tr><tr><td>R3</td><td></td></tr></tbody></table>

## Information spécifique au système

### Jeux Multi-disques

Utiliser un fichier .cmd.\
\
Créer un fichier .txt et le sauvegarder avec l'extension ".cmd". Dedans, écrire le nom du core servant à exécuter le jeu, puis le nom du disque de démarrage (.hdm), puis l'image du disque dur (.hdi), et enfin l'image du CD (.ccd/.img/.sub) comme sur l'exemple ci-dessous.

`Policenauts.cmd`

```
np2kai "Policenauts (User boot disk) [for Neko Project II].hdm" "Policenauts [for Neko Project II].hdi" "Policenauts.ccd"
```

Il semble que cette méthode fonctionne avec le core "Neko Project II Kai" core, mais pas avec le core "Neko Project II"
