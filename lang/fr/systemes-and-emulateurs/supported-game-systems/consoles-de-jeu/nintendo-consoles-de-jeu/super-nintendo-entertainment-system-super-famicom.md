---
description: Nintendo
---

# Super Nintendo Entertainment System - Super Famicom

<table data-header-hidden><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><img src="https://i.imgur.com/inZ65eS.png" alt="" data-size="original"></td><td><img src="https://i.imgur.com/fcfmfq4.png" alt="" data-size="original"></td><td></td></tr></tbody></table>

## Présentation

La **Super Nintendo** (Super Famicom au Japon) est la console 16 bits de Nintendo, sortie au Japon en novembre 1990, en Amérique du Nord en 1991 et en Europe en 1992. Avec près de 50 millions d'exemplaires vendus, c'est l'une des consoles les plus populaires de son époque, rivale directe de la Mega Drive.

Sa manette introduit les boutons **X**, **Y** et les gâchettes **L** et **R**, repris par presque toutes les manettes depuis. Le **mode 7**, qui fait tourner et zoomer un décor entier, donne ses pistes à Super Mario Kart et F-Zero. Certaines cartouches embarquent une puce supplémentaire : **Super FX** (Star Fox, Yoshi's Island), **DSP** (Super Mario Kart, Pilotwings), **SA-1** (Super Mario RPG, Kirby Super Star), **Cx4** (Mega Man X2 et X3).

Sa ludothèque compte de nombreux classiques : Super Mario World, The Legend of Zelda: A Link to the Past, Super Metroid, Donkey Kong Country, Chrono Trigger, Final Fantasy VI, Street Fighter II… Au Japon, la console a reçu deux extensions qui ont leur propre système dans RetroBat : la **Satellaview** (jeux diffusés par satellite) et le **Sufami Turbo** de Bandai (mini-cartouches). Les jeux et hacks **MSU-1**, qui ajoutent une bande-son de qualité CD, ont aussi leur système.

{% embed url="https://fr.wikipedia.org/wiki/Super_Nintendo" %}

## En bref

<table><thead><tr><th width="247.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\snes</code></td></tr><tr><td><strong>Extensions</strong></td><td>.smc .fig .sfc .gd3 .gd7 .dx2 .bsx .swc .rom .wad .zip .7z .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: snes9x</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (firmwares des puces DSP optionnels pour Mesen-S et Mesen)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk, jgenesis ; Snes9x, Mesen, Mednafen et ares par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, Snes9x, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr><tr><td><strong>Pistolets</strong></td><td>cores snes9x, bsnes, bsnes_hd_beta, bsnes-jg, mesen-s ; Snes9x, Mesen, Mednafen, jgenesis, BizHawk</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                                 | Pour qui ?                   | Points forts                                                                                                                                                                          | Limites                                                                                                                                                     |
| ----------------------------------------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **libretro: snes9x** (défaut)             | Tout le monde                | Rapide et très compatible : puces des cartouches émulées sans fichier à ajouter, MSU-1, Super Scope, Justifier, souris, multitap automatique, RetroAchievements, jeu en réseau.       | —                                                                                                                                                           |
| **libretro: bsnes-jg**                    | Puristes                     | Version de bsnes 115 mise à jour, très précise, run-ahead interne.                                                                                                                    | Plus gourmand que snes9x.                                                                                                                                   |
| **libretro: bsnes**                       | Puristes                     | bsnes 115 : émulation très précise, filtres NTSC, overclocking.                                                                                                                       | Plus gourmand que snes9x.                                                                                                                                   |
| **libretro: bsnes\_hd\_beta**             | Amateurs de haute définition | bsnes avec un [**mode 7 en haute résolution**](super-nintendo-entertainment-system-super-famicom.md#mode-7-en-haute-definition-bsnes_hd_beta) (Super Mario Kart, F-Zero, Pilotwings). | Version bêta.                                                                                                                                               |
| **libretro: mednafen\_snes**              | Curieux                      | Ancienne version de bsnes adaptée par Mednafen.                                                                                                                                       | Peu d'options, pas de souris ni de pistolet. Aucun avantage sur les autres cores.                                                                           |
| **libretro: mesen-s**                     | Puristes                     | Émulation précise de Mesen-S.                                                                                                                                                         | Les jeux à puce DSP demandent un firmware (voir [**Jeux à puce DSP**](super-nintendo-entertainment-system-super-famicom.md#jeux-a-puce-dsp-mesen-s-mesen)). |
| **libretro: snes9x2005**                  | Petites configurations       | Ancienne version de snes9x, très légère.                                                                                                                                              | Moins précis.                                                                                                                                               |
| **mednafen** (autonome)                   | Utilisateurs de Mednafen     | Même émulation que le core mednafen\_snes.                                                                                                                                            | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.                                                                                          |
| **mesen**                                 | Utilisateurs de Mesen        | Mesen 2 : émulation précise et outils de débogage.                                                                                                                                    | Pas de RetroAchievements. Sauvegardes instantanées par raccourcis. Jeux à puce DSP : firmware nécessaire.                                                   |
| **snes9x** (autonome)                     | Utilisateurs de Snes9x       | Snes9x pour Windows (version SuperSnes9x) : filtres d'image, RetroAchievements.                                                                                                       | Sauvegardes instantanées par raccourcis.                                                                                                                    |
| **jgenesis**                              | Curieux                      | Émulateur multi-systèmes récent et précis.                                                                                                                                            | Deux joueurs maximum. Pas de RetroAchievements.                                                                                                             |
| **ares**                                  | Puristes                     | Émulation très précise, puces intégrées (aucun fichier à ajouter).                                                                                                                    | Deux joueurs maximum. Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.                                                                    |
| **bizhawk: BSNES**, **Faust**, **Snes9x** | Utilisateurs de BizHawk      | Trois émulations au choix, RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.                                                                                      | —                                                                                                                                                           |

**En cas de doute, gardez libretro: snes9x.**

## BIOS

La Super Nintendo n'a pas de BIOS : aucun fichier n'est nécessaire avec l'émulateur par défaut.

Seuls Mesen-S (core libretro) et Mesen (autonome) ont besoin des firmwares des puces DSP pour les quelques jeux qui les utilisent (voir [**Jeux à puce DSP**](super-nintendo-entertainment-system-super-famicom.md#jeux-a-puce-dsp-mesen-s-mesen)). snes9x, bsnes et ares les émulent sans fichier. RetroBat les signale comme optionnels lors de la vérification des BIOS.

| Fichier                 | Puce                    | Exemples de jeux                              | Dossier |
| ----------------------- | ----------------------- | --------------------------------------------- | ------- |
| `dsp1.rom`, `dsp1b.rom` | DSP-1, DSP-1B           | Super Mario Kart, Pilotwings, Super Air Diver | `bios`  |
| `dsp2.rom`              | DSP-2                   | Dungeon Master                                | `bios`  |
| `dsp3.rom`              | DSP-3                   | SD Gundam GX                                  | `bios`  |
| `dsp4.rom`              | DSP-4                   | Top Gear 3000                                 | `bios`  |
| `st010.rom`             | ST010                   | F1 ROC II: Race of Champions                  | `bios`  |
| `st011.rom`             | ST011                   | Hayazashi Nidan Morita Shougi                 | `bios`  |
| `st018.rom`             | ST018 (Mesen seulement) | Hayazashi Nidan Morita Shougi 2               | `bios`  |

Tous ces fichiers sont optionnels et contrôlés par RetroBat.

## Quel format de jeu ?

<table><thead><tr><th width="269">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.sfc</strong>, <strong>.smc</strong></td><td>Image d'une cartouche (<code>.smc</code> : avec un en-tête de copieur, lu par tous les émulateurs). Les jeux japonais, américains et européens vont dans le même dossier.</td></tr><tr><td><strong>.fig</strong>, <strong>.swc</strong>, <strong>.gd3</strong>, <strong>.gd7</strong>, <strong>.dx2</strong></td><td>Anciens formats de copieurs de cartouches, lus comme des <code>.smc</code>.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive).</td></tr></tbody></table>

Les jeux Satellaview (`.bs`) se rangent dans `roms\satellaview`, les jeux Sufami Turbo (`.st`) dans `roms\sufami`, les jeux MSU-1 dans `roms\snes-msu1`.

## Contrôles

RetroBat configure automatiquement les manettes pour tous les émulateurs. Les boutons gardent la place qu'ils ont sur la manette Super Nintendo :

<table><thead><tr><th width="259">Manette RetroBat</th><th>Super Nintendo</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>SUD</td><td>B</td></tr><tr><td>EST</td><td>A</td></tr><tr><td>OUEST</td><td>Y</td></tr><tr><td>NORD</td><td>X</td></tr><tr><td>L1</td><td>L</td></tr><tr><td>R1</td><td>R</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/snes.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

Sur une manette Xbox, le bouton A (en bas) correspond donc au B de la Super Nintendo. Pour retrouver les lettres de votre manette (A en bas, B à droite), activez **CONTRÔLES > INVERSER LES BOUTONS A/B/X/Y** :

<div align="left"><figure><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/snes_invert.png?raw=true" alt="" width="375"><figcaption></figcaption></figure></div>

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

Snes9x, Mesen, Mednafen, ares, jgenesis et BizHawk utilisent les raccourcis de RetroBat :

| Action                          | Manette             | Clavier          |
| ------------------------------- | ------------------- | ---------------- |
| Quitter                         | HOTKEY + START      | `Échap`          |
| Pause                           | HOTKEY + SUD        | `P`              |
| Sauvegarde instantanée          | HOTKEY + OUEST      | `F2`             |
| Chargement                      | HOTKEY + NORD       | `F4`             |
| Emplacement précédent / suivant | HOTKEY + Bas / Haut | `F6` / `F7`      |
| Rembobiner (si activé)          | HOTKEY + Gauche     | `Retour arrière` |
| Avance rapide (maintenir)       | HOTKEY + Droite     | `L`              |
| Capture d'écran                 | HOTKEY + R3         | `F8`             |
| Plein écran                     | HOTKEY + L3         | `F`              |

Snes9x n'a pas de raccourci pour le plein écran, jgenesis n'en a pas pour la capture d'écran.

## Dossiers

<table><thead><tr><th width="380.25">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Cores libretro, Snes9x, Mesen, Mednafen : sauvegardes des jeux</td><td><code>saves\snes</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><p><code>saves\snes\libretro.&#x3C;core></code></p><p>(ex. <code>saves\snes\libretro.snes9x</code>)</p></td></tr><tr><td>Snes9x : sauvegardes instantanées</td><td><code>saves\snes\snes9x\sstates</code></td></tr><tr><td>Mesen : sauvegardes instantanées</td><td><code>saves\snes\mesen\SaveStates</code></td></tr><tr><td>Mednafen : sauvegardes instantanées</td><td><code>saves\snes\mednafen\sstates</code></td></tr><tr><td>ares : sauvegardes des jeux et instantanées</td><td><code>saves\snes\ares</code></td></tr><tr><td>jgenesis : sauvegardes des jeux</td><td><code>saves\snes\jgenesis</code></td></tr><tr><td>jgenesis : sauvegardes instantanées</td><td><code>saves\snes\jgenesis\states</code></td></tr><tr><td>BizHawk : sauvegardes des jeux</td><td><code>saves\snes\bizhawk</code></td></tr><tr><td>BizHawk : sauvegardes instantanées</td><td><code>saves\snes\bizhawk\sstates\&#x3C;core></code></td></tr><tr><td>Firmwares des puces DSP</td><td><code>bios</code> (copiés par RetroBat dans <code>emulators\mesen\Firmware</code> pour Mesen)</td></tr><tr><td>Codes de triche</td><td><p><code>cheats\snes9x</code> (Snes9x)</p><p><code>cheats\mednafen</code> (Mednafen)</p></td></tr><tr><td>Captures d'écran</td><td><code>screenshots\snes9x</code>, <code>screenshots\mesen</code>, <code>screenshots\mednafen</code>, <code>screenshots\ares</code>, <code>screenshots\bizhawk\snes</code></td></tr></tbody></table>

## Guides

### Jouer à plusieurs (multitap)

La Super Nintendo a deux prises manette. Les jeux à plus de deux joueurs (Super Bomberman, Micro Machines, NBA Jam…) utilisent un multitap, branché sur la prise du joueur 2 : jusqu'à 5 joueurs.

<table><thead><tr><th width="325.25">Émulateur</th><th>Multitap</th></tr></thead><tbody><tr><td>core snes9x</td><td>Branché dès qu'une 3e manette est connectée</td></tr><tr><td>cores bsnes, bsnes_hd_beta, bsnes-jg, mesen-s</td><td>Branché dès qu'une 3e manette est connectée (<strong>CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 2 > MULTITAP</strong> pour le forcer)</td></tr><tr><td>Snes9x</td><td>Branché dès qu'une 3e manette est connectée</td></tr><tr><td>Mesen</td><td><strong>CONTRÔLES > ADAPTATEUR MULTIJOUEURS</strong> (<strong>MULTITAP SIMPLE</strong> jusqu'à 5 joueurs, <strong>DOUBLE MULTITAP</strong> jusqu'à 8)</td></tr><tr><td>Mednafen</td><td><strong>CONTRÔLES > ADAPTATEUR MULTIJOUEURS</strong> (<strong>PORT 1</strong>, <strong>PORT 2</strong> ou <strong>DANS CHAQUE PORT</strong>)</td></tr><tr><td>ares, jgenesis</td><td>Deux joueurs maximum</td></tr></tbody></table>

### Pistolets (Super Scope, Justifier)

Une vingtaine de jeux utilisent le Super Scope de Nintendo (Super Scope 6, Yoshi's Safari, Battle Clash, T2: The Arcade Game…) ou le Justifier de Konami (Lethal Enforcers). Activez **PISTOLETS > ACTIVER LES PISTOLETS** : RetroBat branche le bon pistolet pour les jeux connus. Pour un autre jeu, choisissez-le dans **PISTOLETS > TYPE DE PISTOLET** (cores libretro, Snes9x).

<table><thead><tr><th width="326.5">Émulateur</th><th>Pistolets</th></tr></thead><tbody><tr><td>core snes9x</td><td>Super Scope, Justifier, deux Justifiers, M.A.C.S. Rifle</td></tr><tr><td>cores bsnes, bsnes_hd_beta, bsnes-jg</td><td>Super Scope, Justifier</td></tr><tr><td>core mesen-s, Mesen</td><td>Super Scope (Mesen : <strong>PISTOLETS > PORT DU PISTOLET</strong>, port 2 par défaut)</td></tr><tr><td>Snes9x</td><td>Super Scope, Justifier, deux Justifiers</td></tr><tr><td>Mednafen, jgenesis, BizHawk</td><td>Super Scope</td></tr></tbody></table>

Sans pistolet, la souris sert de viseur. Pour plus de détails, voir la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/).

### Souris (Mario Paint)

Mario Paint et quelques autres jeux utilisent la souris Super Nintendo :

<table><thead><tr><th width="251.5">Émulateur</th><th>Réglage</th></tr></thead><tbody><tr><td>cores snes9x, bsnes, bsnes_hd_beta, bsnes-jg</td><td><strong>CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1 > SOURIS</strong></td></tr><tr><td>core mesen-s, Mesen</td><td><strong>CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1 > SOURIS</strong></td></tr><tr><td>Snes9x</td><td><strong>CONTRÔLES > UTILISER LA SOURIS > PORT 1</strong></td></tr></tbody></table>

### Jeux à puce DSP (Mesen-S, Mesen)

Mesen-S et Mesen ont besoin d'un firmware pour les jeux à puce DSP ou ST01x (Super Mario Kart, Pilotwings, Top Gear 3000…). Sans lui, ces jeux ne démarrent pas avec Mesen-S, et Mesen demande le fichier au lancement. Copiez les fichiers du tableau de la section [**BIOS**](super-nintendo-entertainment-system-super-famicom.md#bios) dans `bios` : RetroBat les donne à Mesen-S et les copie pour Mesen.

snes9x (défaut), bsnes et ares n'ont besoin d'aucun fichier.

### Mode 7 en haute définition (bsnes\_hd\_beta)

Le core bsnes\_hd\_beta affiche les décors en mode 7 (Super Mario Kart, F-Zero, Pilotwings, Final Fantasy VI…) dans une résolution plus élevée que la console :

| Option                                                 | Effet                                                       |
| ------------------------------------------------------ | ----------------------------------------------------------- |
| **RENDU VISUEL > ÉCHELLE DU MODE 7**                   | Résolution du mode 7 (2x par défaut, 1x = rendu d'origine). |
| **RENDU VISUEL > SURÉCHANTILLONNAGE DU MODE 7**        | Lisse le mode 7 (2x par défaut).                            |
| **RENDU VISUEL > CORRECTION DE PERSPECTIVE DU MODE 7** | Corrige les déformations du sol au loin.                    |

### Autres options utiles

| Émulateur                              | Option                                                          | Effet                                                                                                       |
| -------------------------------------- | --------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| core snes9x                            | **ÉMULATION > OVERCLOCKING CPU**                                | Réduit les ralentissements (Gradius III, Super R-Type), mais peut causer des bugs.                          |
| core snes9x                            | **ÉMULATION > OVERCLOCK PUCE SUPERFX**                          | Plus d'images par seconde dans les jeux Super FX (Star Fox, Stunt Race FX).                                 |
| core snes9x                            | **VIDÉO > SIGNAL VIDÉO ÉMULÉ**                                  | Recrée la sortie d'origine (RF, composite, S-Vidéo, RGB).                                                   |
| core snes9x                            | **RENDU VISUEL > MÉLANGER LES PIXELS**                          | **FUSION** : nécessaire pour les transparences de quelques jeux en haute résolution (Kirby's Dream Land 3). |
| core snes9x                            | **AUDIO > INTERPOLATION AUDIO**                                 | **GAUSSIEN** (défaut) reproduit le son de la console.                                                       |
| core snes9x                            | **ÉMULATION > HACKS DANGEREUX**                                 | Pour quelques homebrews et hacks qui ne démarrent pas. À laisser désactivé pour les jeux du commerce.       |
| cores bsnes, bsnes\_hd\_beta           | **ÉMULATION > OVERCLOCKING**                                    | Accélère le processeur, la SA-1 et la Super FX.                                                             |
| cores bsnes, bsnes\_hd\_beta           | **VIDÉO > DÉSACTIVER LA LIMITE DE SPRITES**                     | Supprime les clignotements quand beaucoup d'objets sont à l'écran.                                          |
| cores bsnes, bsnes\_hd\_beta, bsnes-jg | **RÉDUCTION DE LA LATENCE > NOMBRE D'IMAGES EN AVANCE (COEUR)** | Réduit le délai entre l'appui sur un bouton et l'action à l'écran.                                          |
| core snes9x2005                        | **VIDÉO > SAUT D'IMAGE**                                        | Pour les petites configurations.                                                                            |
| Snes9x                                 | **SHADERS**                                                     | Filtres d'image de Snes9x (NTSC, hq2x, xBRZ…).                                                              |

## Problèmes connus

| Problème                                                            | Solution                                                                                                                                                                                            |
| ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Les joueurs 3 à 5 ne répondent pas                                  | Le multitap est nécessaire : voir [**Jouer à plusieurs (multitap)**](super-nintendo-entertainment-system-super-famicom.md#jouer-a-plusieurs-multitap). ares et jgenesis n'émulent que deux joueurs. |
| Super Mario Kart ou Pilotwings ne démarre pas avec Mesen-S ou Mesen | Ajoutez le firmware de la puce DSP : voir [**Jeux à puce DSP**](super-nintendo-entertainment-system-super-famicom.md#jeux-a-puce-dsp-mesen-s-mesen), ou utilisez snes9x.                            |
| Mario Paint ne répond pas                                           | Branchez la souris : voir [**Souris**](super-nintendo-entertainment-system-super-famicom.md#souris-mario-paint) **(Mario Paint)**.                                                                  |
| Les jeux Super FX ralentissent                                      | Augmentez **OVERCLOCK PUCE SUPERFX** (snes9x) ou **OVERCLOCKING** (bsnes).                                                                                                                          |
| Des transparences manquent (Kirby's Dream Land 3)                   | snes9x : **MÉLANGER LES PIXELS > FUSION** ; bsnes : **ÉMULATION DU FLOU**.                                                                                                                          |
| Un jeu `.bs` ou `.st` ne démarre pas                                | Rangez-le dans `roms\satellaview` ou `roms\sufami`.                                                                                                                                                 |
