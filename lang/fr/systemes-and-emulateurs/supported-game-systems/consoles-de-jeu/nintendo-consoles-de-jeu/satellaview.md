---
description: Nintendo
---

# Satellaview

<div align="left"><figure><img src="../../../../.gitbook/assets/image (755).png" alt="" width="563"><figcaption></figcaption></figure></div>

## Présentation

La **Satellaview** est une extension de la Super Famicom sortie au Japon en 1995, conçue par Nintendo avec la radio St.GIGA. Branchée sous la console et reliée à une antenne satellite, elle recevait chaque jour des jeux, des magazines et des émissions, diffusés jusqu'en 2000.

Les jeux étaient enregistrés sur une carte mémoire (BS Memory Pack), lue par la cartouche **BS-X** branchée dans la console. Certains n'étaient jouables qu'à l'heure de leur diffusion, avec des voix et des musiques en direct (SoundLink). Parmi les titres les plus connus : BS The Legend of Zelda, BS Zelda no Densetsu: Kodai no Sekiban, BS F-Zero Grand Prix, Radical Dreamers, BS Super Mario USA.

Les jeux se jouent comme des jeux Super Nintendo : les contrôles, les raccourcis et les options des émulateurs sont décrits sur la page [**Super Nintendo**](super-nintendo-entertainment-system-super-famicom.md).

{% embed url="https://fr.wikipedia.org/wiki/Satellaview" %}

## En bref

<table><thead><tr><th width="271.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\satellaview</code></td></tr><tr><td><strong>Extensions</strong></td><td>.st .fig .bs .smc .sfc .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: snes9x</td></tr><tr><td><strong>BIOS</strong></td><td><code>BS-X.bin</code> obligatoire</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro ; ares par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="171.5">Émulateur</th><th width="132.5">Pour qui ?</th><th width="193.25">Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: snes9x</strong> (défaut)</td><td>Tout le monde</td><td>Rapide et très compatible.</td><td>—</td></tr><tr><td><strong>libretro: mesen-s</strong></td><td>Puristes</td><td>Émulation précise de Mesen-S.</td><td>—</td></tr><tr><td><strong>libretro: bsnes</strong></td><td>Puristes</td><td>Émulation très précise de bsnes.</td><td>Plus gourmand que snes9x.</td></tr><tr><td><strong>ares</strong></td><td>Puristes</td><td>Émulation très précise.</td><td>Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr></tbody></table>

**En cas de doute, gardez libretro: snes9x.**

## BIOS

Les jeux Satellaview se lancent à travers la cartouche BS-X : son contenu est nécessaire pour tous les émulateurs.

<table><thead><tr><th width="96.5">Fichier</th><th width="238">Description</th><th width="73.75">Dossier</th><th>md5</th></tr></thead><tbody><tr><td><code>BS-X.bin</code></td><td>Cartouche BS-X (Japon)</td><td><code>bios</code></td><td>fed4d8242cfbed61343d53d48432aced</td></tr></tbody></table>

Ce fichier est obligatoire et contrôlé par RetroBat.

## Quel format de jeu ?

<table><thead><tr><th width="199">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.bs</strong></td><td>Contenu d'un BS Memory Pack (le format habituel des jeux Satellaview).</td></tr><tr><td><strong>.sfc</strong>, <strong>.smc</strong>, <strong>.fig</strong></td><td>Jeux Satellaview convertis en cartouche Super Nintendo (certaines traductions).</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive).</td></tr></tbody></table>

## Contrôles

RetroBat configure automatiquement les manettes. Les boutons, l'option **INVERSER LES BOUTONS A/B/X/Y** et les raccourcis sont les mêmes que sur la page [**Super Nintendo**](super-nintendo-entertainment-system-super-famicom.md#controles).

## Dossiers

<table><thead><tr><th width="357.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Cores libretro : sauvegardes des jeux</td><td><code>saves\satellaview</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><code>saves\satellaview\libretro.&#x3C;core></code> (ex. <code>saves\satellaview\libretro.snes9x</code>)</td></tr><tr><td>ares : sauvegardes des jeux et instantanées</td><td><code>saves\satellaview\ares</code></td></tr><tr><td>Captures d'écran</td><td><code>screenshots\ares</code></td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="289">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas</td><td>Vérifiez que <code>BS-X.bin</code> est dans <code>bios</code>.</td></tr><tr><td>Un jeu <code>.st</code> ne démarre pas</td><td>Les jeux Sufami Turbo se rangent dans <code>roms\sufami</code>.</td></tr></tbody></table>
