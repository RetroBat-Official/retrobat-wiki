---
description: Nintendo
---

# Nintendo Entertainment System - Family Computer

<table data-header-hidden><thead><tr><th></th><th></th><th data-hidden></th></tr></thead><tbody><tr><td><p></p><p><picture><source srcset="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/91d85c7849cc550b0cac4e75cb8e0923d3b61b5e/art/logos/nes-w.svg" media="(prefers-color-scheme: dark)"><img src="https://raw.githubusercontent.com/fabricecaruso/es-theme-carbon/master/art/logos/nes.svg" alt="" data-size="original"></picture></p></td><td><p></p><p><img src="https://upload.wikimedia.org/wikipedia/commons/7/7d/Family_Computer_logo.svg" alt="" data-size="original"></p></td><td></td></tr></tbody></table>

## Présentation

La **Famicom** (Family Computer) est la console de salon 8 bits de Nintendo, sortie au Japon en juillet 1983. Elle est vendue en Occident sous le nom de **Nintendo Entertainment System** (NES), en 1985 en Amérique du Nord et en 1986 en Europe. Elle relance le marché du jeu vidéo et dépasse les 60 millions d'exemplaires.

Sa ludothèque compte Super Mario Bros. 1 à 3, The Legend of Zelda, Metroid, Mega Man, Castlevania, Final Fantasy, Dragon Quest, Punch-Out!!, Contra… Le pistolet **Zapper** (Duck Hunt, Hogan's Alley) et l'adaptateur quatre joueurs **Four Score** sont émulés.

Les jeux du lecteur de disquettes **Famicom Disk System** ont leur propre système, `roms\fds`, mais les fichiers `.fds` sont aussi acceptés ici.

{% embed url="https://fr.wikipedia.org/wiki/Nintendo_Entertainment_System" %}

## En bref

<table><thead><tr><th width="276.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\nes</code></td></tr><tr><td><strong>Extensions</strong></td><td>.fds .nes .zip .7z</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: fceumm</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (<code>disksys.rom</code> pour les jeux <code>.fds</code>)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, BizHawk, jgenesis ; Mesen, Mednafen et ares par raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="161.5">Émulateur</th><th width="173">Pour qui ?</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: fceumm</strong> (défaut)</td><td>Tout le monde</td><td>Très compatible, Zapper, quatre joueurs, packs HD, extension Game Genie, RetroAchievements, jeu en réseau.</td><td>—</td></tr><tr><td><strong>libretro: nestopia</strong></td><td>Tout le monde</td><td>Très précis, Zapper, Arkanoid, quatre joueurs, RetroAchievements, jeu en réseau.</td><td>—</td></tr><tr><td><strong>libretro: mesen</strong></td><td>Puristes</td><td>Très précis, Zapper, Power Pad, Arkanoid, packs HD, RetroAchievements, jeu en réseau.</td><td>—</td></tr><tr><td><strong>mednafen</strong></td><td>Utilisateurs de Mednafen</td><td>Émulation solide, Zapper.</td><td>Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr><tr><td><strong>mesen</strong></td><td>Utilisateurs de Mesen</td><td>Mesen 2 : émulation précise, Zapper, quatre joueurs, outils de débogage.</td><td>Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr><tr><td><strong>jgenesis</strong></td><td>Curieux</td><td>Émulateur multi-systèmes récent et précis, Zapper.</td><td>Pas de RetroAchievements.</td></tr><tr><td><strong>ares</strong></td><td>Puristes</td><td>Émulation très précise.</td><td>Pas de RetroAchievements. Sauvegardes instantanées par raccourcis.</td></tr><tr><td><strong>bizhawk: NesHawk</strong>, <strong>quickerNES</strong></td><td>Utilisateurs de BizHawk</td><td>NesHawk précis, quickerNES rapide, Zapper (NesHawk), RetroAchievements, sauvegardes instantanées dans le menu de RetroBat.</td><td>—</td></tr></tbody></table>

**En cas de doute, gardez libretro: fceumm.**

## BIOS

La NES n'a pas de BIOS : aucun fichier n'est nécessaire pour les cartouches.

Les jeux Famicom Disk System (`.fds`) demandent le BIOS du lecteur, voir la page [**Famicom Disk System**](family-computer-disk-system.md).

<table><thead><tr><th width="141.75">Fichier</th><th width="188.25">Description</th><th width="101.5">Dossier</th><th>md5</th></tr></thead><tbody><tr><td><code>disksys.rom</code></td><td>BIOS du Famicom Disk System</td><td><code>bios</code></td><td>ca30b50f880eb660a320674ed365ef7a</td></tr></tbody></table>

Ce fichier est optionnel ici et contrôlé par RetroBat.

## Quel format de jeu ?

<table><thead><tr><th width="202.75">Format</th><th>Description</th></tr></thead><tbody><tr><td><strong>.nes</strong></td><td>Image d'une cartouche.</td></tr><tr><td><strong>.fds</strong></td><td>Image d'une disquette Famicom Disk System.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong></td><td>Un jeu compressé (un jeu par archive).</td></tr></tbody></table>

## Contrôles

RetroBat configure automatiquement les manettes pour tous les émulateurs. Disposition par défaut :

<table><thead><tr><th width="265.25">Manette RetroBat</th><th>NES</th></tr></thead><tbody><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>SUD</td><td>A</td></tr><tr><td>OUEST</td><td>B</td></tr><tr><td>SELECT</td><td>SELECT</td></tr><tr><td>START</td><td>START</td></tr></tbody></table>

Options de disposition :

| Option                                      | Émulateurs                                                                   | Effet                                                       |
| ------------------------------------------- | ---------------------------------------------------------------------------- | ----------------------------------------------------------- |
| **CONTRÔLES > TOURNER LES BOUTONS A/B/X/Y** | Tous                                                                         | A sur EST, B sur SUD.                                       |
| **CONTRÔLES > DISPOSITION XBOX**            | cores fceumm, nestopia, mesen                                                | A sur SUD, B sur EST, comme les lettres d'une manette Xbox. |
| **CONTRÔLES > ACTIVER TURBO**               | cores fceumm et nestopia, Mesen, Mednafen ; core mesen : choix de la vitesse | Ajoute un turbo A et un turbo B sur les boutons restants.   |

<table><thead><tr><th width="311.5">Disposition</th><th>Schéma</th></tr></thead><tbody><tr><td>Par défaut</td><td><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes.png?raw=true" alt="" data-size="original"></td></tr><tr><td>Turbo</td><td><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_turbo.png?raw=true" alt="" data-size="original"></td></tr><tr><td>Boutons tournés</td><td><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_rotate.png?raw=true" alt="" data-size="original"></td></tr><tr><td>Boutons tournés et turbo</td><td><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_rotate_turbo.png?raw=true" alt="" data-size="original"></td></tr><tr><td>Xbox</td><td><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_xbox.png?raw=true" alt="" data-size="original"></td></tr><tr><td>Xbox et turbo</td><td><img src="https://github.com/RetroBat-Official/retrobat-tattoos/blob/main/default/nes_xbox_turbo.png?raw=true" alt="" data-size="original"></td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (651).png" alt=""><figcaption></figcaption></figure></div>

### Raccourcis

Les cores libretro utilisent les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

Mesen, Mednafen, ares, jgenesis et BizHawk utilisent les raccourcis de RetroBat :

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

jgenesis n'a pas de raccourci pour la capture d'écran.

## Dossiers

<table><thead><tr><th width="334">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Cores libretro, Mesen, Mednafen : sauvegardes des jeux</td><td><code>saves\nes</code></td></tr><tr><td>Cores libretro : sauvegardes instantanées</td><td><p><code>saves\nes\libretro.&#x3C;core></code> </p><p>(exemple: <code>saves\nes\libretro.fceumm</code>)</p></td></tr><tr><td>Mesen : sauvegardes instantanées</td><td><code>saves\nes\mesen\SaveStates</code></td></tr><tr><td>Mednafen : sauvegardes instantanées</td><td><code>saves\nes\mednafen\sstates</code></td></tr><tr><td>ares : sauvegardes des jeux et instantanées</td><td><code>saves\nes\ares</code></td></tr><tr><td>jgenesis : sauvegardes des jeux</td><td><code>saves\nes\jgenesis</code></td></tr><tr><td>BizHawk : sauvegardes des jeux</td><td><code>saves\nes\bizhawk</code></td></tr><tr><td>BIOS</td><td><code>bios</code> (copié par RetroBat dans <code>emulators\mesen\Firmware</code> pour Mesen)</td></tr><tr><td>Packs HD</td><td><code>bios\HdPacks</code> (cores fceumm et mesen)</td></tr><tr><td>Codes de triche</td><td><p><code>cheats\mednafen</code> (Mednafen)</p><p> <code>cheats\jgenesis</code> (jgenesis)</p><p><code>cheats\bizhawk\nes</code> (BizHawk)</p></td></tr><tr><td>Captures d'écran</td><td><code>screenshots\mesen</code>, <code>screenshots\mednafen</code>, <code>screenshots\ares</code>, <code>screenshots\bizhawk\nes</code></td></tr></tbody></table>

## Guides

### Zapper

Plusieurs jeux utilisent le pistolet Zapper (Duck Hunt, Hogan's Alley, Wild Gunman, Gumshoe…). Activez **PISTOLETS > ACTIVER LES PISTOLETS** avec les cores fceumm, nestopia ou mesen, Mesen, Mednafen, jgenesis ou BizHawk NesHawk : RetroBat branche le Zapper, sur le port 2 comme sur la vraie console. Avec Mesen, **PISTOLETS > PORT DU PISTOLET** permet de choisir le port 1.

Pour plus de détails, voir la page [**Pistolets**](../../../../controleurs/supported-controllers/lightguns/).

### Jouer à quatre

Les jeux à quatre joueurs (Gauntlet II, Nintendo World Cup, Super Spike V'Ball…) demandent l'adaptateur Four Score (NES) ou l'adaptateur quatre joueurs de la Famicom :

<table><thead><tr><th width="210.25">Émulateur</th><th>Option</th></tr></thead><tbody><tr><td>core fceumm</td><td><strong>CONTRÔLES > ADAPTATEUR MULTIJOUEURS</strong> : <strong>NTSC</strong> (Four Score) ou <strong>FAMICOM</strong> ; automatique par défaut</td></tr><tr><td>core nestopia</td><td><strong>CONTRÔLES > ADAPTATEUR MULTIJOUEURS</strong> : <strong>NTSC</strong> (Four Score) ou <strong>FAMICOM</strong> ; automatique par défaut</td></tr><tr><td>Mesen</td><td><strong>CONTRÔLES > ADAPTATEUR MULTIJOUEURS</strong> : <strong>FOURSCORE</strong> ou <strong>FOURSCORE + EXTENSION FOURPLAYER</strong></td></tr></tbody></table>

### Packs HD

Les packs HD au format Mesen remplacent les graphismes d'origine. Placez le pack dans `bios\HdPacks`, dans un dossier qui porte le nom du fichier du jeu sans son extension (par exemple `bios\HdPacks\Mega Man (USA)` pour `Mega Man (USA).nes`), puis :

* core fceumm : rien à faire, **RENDU VISUEL > PACKS DE TEXTURES HD** est activé par défaut ;
* core mesen : activez **RENDU VISUEL > TEXTURES PERSONNALISÉES**.

Le pack ne fonctionne qu'avec la version du jeu prévue : comparez le sha1 du jeu à celui indiqué dans le fichier `hires.txt` du pack.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (650).png" alt=""><figcaption></figcaption></figure></div>

## Problèmes connus

<table><thead><tr><th width="387.75">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le Zapper ne fonctionne pas</td><td>Activez <strong>PISTOLETS > ACTIVER LES PISTOLETS</strong> (voir <a href="nintendo-entertainment-system-family-computer.md#zapper"><strong>Zapper</strong></a>).</td></tr><tr><td>Les joueurs 3 et 4 ne répondent pas</td><td>Voir <a href="nintendo-entertainment-system-family-computer.md#jouer-a-quatre"><strong>Jouer à quatre</strong></a>.</td></tr><tr><td>Un jeu <code>.fds</code> ne démarre pas</td><td>Ajoutez <code>disksys.rom</code> dans <code>bios</code>.</td></tr><tr><td>Les boutons A et B sont inversés par rapport à votre manette</td><td>Voir les options de disposition (<a href="nintendo-entertainment-system-family-computer.md#controles"><strong>Contrôles</strong></a>).</td></tr></tbody></table>
