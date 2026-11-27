---
description: Sharp
---

# Sharp X1

<div align="left"><figure><img src="../../../../.gitbook/assets/image (777).png" alt="" width="300"><figcaption></figcaption></figure></div>

## Présentation

Le **Sharp X1** est un ordinateur japonais 8 bits sorti en 1982, construit autour d'un processeur Z80. Ses graphismes en couleur et ses caractères redéfinissables (PCG) en ont fait une machine de jeu ; il est suivi des X1 turbo (1984) et X1 turbo Z (1986). Le premier Thunder Force (1983) est sorti sur X1.

{% embed url="https://fr.wikipedia.org/wiki/Sharp_X1" %}

## En bref

<table><thead><tr><th width="291.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\x1</code></td></tr><tr><td><strong>Extensions</strong></td><td>.dx1 .zip .2d .2hd .tfd .d88 .88d .hdm .xdf .dup .cmd .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: x1</td></tr><tr><td><strong>BIOS</strong></td><td><code>IPLROM.X1</code> obligatoire</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (joueur 1)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core libretro</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr></tbody></table>

## BIOS

<table><thead><tr><th width="116.5">Fichier</th><th width="210">Description</th><th width="105.5">Dossier</th><th>md5</th></tr></thead><tbody><tr><td><code>IPLROM.X1</code></td><td>ROM de démarrage du X1</td><td><code>bios\xmil</code></td><td>eeeea1cd29c6e0e8b094790ae969bfa7</td></tr><tr><td><code>IPLROM.X1T</code></td><td>ROM de démarrage du X1 turbo (<strong>TYPE DE ROM</strong> TURBO ou TURBOZ)</td><td><code>bios\xmil</code></td><td>56c28adcf1f3a2f87cf3d57c378013f5</td></tr></tbody></table>

`IPLROM.X1` est obligatoire, `IPLROM.X1T` optionnel ; les deux sont contrôlés par RetroBat.

## Quel format de jeu ?

<table><thead><tr><th width="386.5">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.2d</strong>, <strong>.2hd</strong>, <strong>.d88</strong>, <strong>.88d</strong>, <strong>.hdm</strong>, <strong>.xdf</strong>, <strong>.dup</strong>, <strong>.dx1</strong>, <strong>.tfd</strong></td><td>Image d'une disquette.</td></tr><tr><td><strong>.cmd</strong></td><td>Fichier de commande du core.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé.</td></tr></tbody></table>

## Contrôles

RetroBat configure la manette du joueur 1 (un seul port joystick) :

<table><thead><tr><th width="186.5">Manette RetroBat</th><th>X1</th></tr></thead><tbody><tr><td>Croix</td><td>Croix</td></tr><tr><td>SUD</td><td>Bouton 1 (tir principal)</td></tr><tr><td>EST</td><td>Bouton 2</td></tr></tbody></table>

Le clavier du PC reste actif ; beaucoup de jeux X1 se jouent au clavier. Pour mettre des touches du clavier sur la manette, voir la page [**Clavier / PadToKey**](../../../../controleurs/pad2key.md).

### Raccourcis

Le core x1 utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

<table><thead><tr><th width="262.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Sauvegardes de jeu</td><td>sur la disquette du jeu (fichier dans <code>roms\x1</code>)</td></tr><tr><td>Sauvegardes instantanées</td><td><code>saves\x1\libretro.x1</code></td></tr><tr><td>BIOS</td><td><code>bios\xmil</code></td></tr></tbody></table>

## Guides

### Jeux X1 turbo

Les jeux faits pour le X1 turbo demandent **ÉMULATION > TYPE DE ROM > TURBO** (ou **TURBOZ**) et le BIOS `IPLROM.X1T`.

## Problèmes connus

<table><thead><tr><th width="304">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Écran noir au démarrage</td><td>Ajoutez <code>IPLROM.X1</code> dans <code>bios\xmil</code>.</td></tr><tr><td>Un jeu X1 turbo ne démarre pas</td><td>Choisissez <strong>TYPE DE ROM > TURBO</strong> et ajoutez <code>IPLROM.X1T</code> (voir <a href="sharp-x1.md#jeux-x1-turbo"><strong>Jeux X1 turbo</strong></a>).</td></tr><tr><td>Le jeu ne réagit pas à la manette</td><td>Il se joue au clavier : utilisez le clavier du PC ou la page <strong>Clavier / PadToKey</strong>.</td></tr></tbody></table>
