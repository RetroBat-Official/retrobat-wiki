---
description: Sony
---

# PlayStation

<div align="left"><figure><img src="../../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure></div>

## Présentation

La **PlayStation** sort en décembre 1994 au Japon, puis en 1995 aux États-Unis et en Europe. Elle est née d'un projet de lecteur CD pour la Super Nintendo, abandonné par Nintendo et repris par Sony pour en faire sa propre console.

Avec ses jeux sur CD-ROM et ses graphismes en 3D, elle change le visage du jeu vidéo et attire un public plus âgé. Elle s'écoule à plus de 100 millions d'exemplaires. Final Fantasy VII, Gran Turismo, Metal Gear Solid, Tekken, Resident Evil ou Crash Bandicoot y ont fait leurs débuts. La manette DualShock, avec ses deux sticks analogiques et ses vibrations, arrive en 1997.

{% embed url="https://fr.wikipedia.org/wiki/PlayStation" %}

## En bref

<table><thead><tr><th width="267.75"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\psx</code></td></tr><tr><td><strong>Extensions</strong></td><td>.cue .img .mdf .pbp .toc .cbn .m3u .ccd .chd .zip .7z .iso .cso .squashfs .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: mednafen_psx_hw</td></tr><tr><td><strong>BIOS</strong></td><td><code>psxonpsp660.bin</code> (ou <code>ps1_rom.bin</code>, ou <code>scph5500.bin</code>, <code>scph5501.bin</code>, <code>scph5502.bin</code>)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, DuckStation, BizHawk</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, DuckStation, BizHawk</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro (mednafen_psx_hw, pcsx_rearmed)</td></tr><tr><td><strong>Pistolets</strong></td><td>cores libretro, DuckStation, Mednafen</td></tr></tbody></table>

## Quel émulateur choisir ?

| Émulateur                                | Pour qui ?                                  | Points forts                                                                                                                        | Limites                                  |
| ---------------------------------------- | ------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| **libretro: mednafen\_psx\_hw** (défaut) | Tout le monde                               | Très compatible, résolution augmentée, correction de perspective (PGXP), textures personnalisées, RetroAchievements, jeu en réseau. | Plus gourmand que les autres cores.      |
| **duckstation**                          | Ceux qui préfèrent un émulateur autonome    | Rapide, nombreuses améliorations graphiques, RetroAchievements, retour en arrière.                                                  | Pas de jeu en réseau.                    |
| **libretro: swanstation**                | Ceux qui veulent DuckStation dans RetroArch | Dérivé de DuckStation, avec RetroAchievements.                                                                                      | Pas de jeu en réseau.                    |
| **libretro: pcsx\_rearmed**              | PC modestes                                 | Léger, avec RetroAchievements et jeu en réseau.                                                                                     | Moins d'améliorations graphiques.        |
| **mednafen**                             | Recherche de fidélité                       | Émulation précise.                                                                                                                  | Pas de `.chd`, pas de RetroAchievements. |
| **bizhawk** (Nymashock, Octoshock)       | Speedrun assisté (TAS)                      | Outils d'enregistrement et d'analyse.                                                                                               | Pas de `.chd`.                           |

**En cas de doute, gardez libretro: mednafen\_psx\_hw.**

## BIOS

Un BIOS est nécessaire. RetroBat cherche les fichiers à la racine du dossier `bios`, dans cet ordre :

<table><thead><tr><th width="65.25">Ordre</th><th width="156">Fichier</th><th width="228.25">Origine</th><th>MD5</th></tr></thead><tbody><tr><td>1</td><td><code>psxonpsp660.bin</code></td><td>BIOS PlayStation de la PSP, toutes régions</td><td><code>c53ca5908936d412331790f4426c6c33</code></td></tr><tr><td>2</td><td><code>ps1_rom.bin</code></td><td>BIOS PlayStation de la PS3, toutes régions</td><td>—</td></tr><tr><td>3</td><td><code>scph5500.bin</code></td><td>PlayStation japonaise</td><td><code>8dd7d5296a650fac7319bce665a6a53c</code></td></tr><tr><td>3</td><td><code>scph5501.bin</code></td><td>PlayStation américaine</td><td><code>490f666e1afb15b7362b406ed1cea246</code></td></tr><tr><td>3</td><td><code>scph5502.bin</code></td><td>PlayStation européenne</td><td><code>32736f17079d0b2b7024407c39bd3050</code></td></tr></tbody></table>

* Un seul fichier suffit : `psxonpsp660.bin` fonctionne pour toutes les régions. C'est le seul que RetroBat signale comme manquant.
* Avec les fichiers `scph`, il faut celui de la région du jeu.
* L'option **ÉMULATION > UTILISER LES BIOS SCPH (LEGACY)** force l'usage des fichiers `scph` (mednafen\_psx\_hw, swanstation, Mednafen, BizHawk).
* DuckStation choisit lui-même parmi les BIOS du dossier `bios`. L'option **ÉMULATION > FORCER LE FIRMWARE** lui en impose un.
* pcsx\_rearmed peut démarrer sans BIOS, mais avec une moins bonne compatibilité.
* Avec les cores libretro, l'option **ÉMULATION > MODIFIER DOSSIER DU BIOS** fait chercher les BIOS dans un autre dossier.

L'option **SAUTER LE BIOS** passe l'animation de démarrage de la console.

## Quel format de jeu ?

<table><thead><tr><th width="277.75">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.chd</strong></td><td>Recommandé : un seul fichier compressé par disque. Non reconnu par Mednafen et BizHawk.</td></tr><tr><td><strong>.cue</strong> (+ <code>.bin</code>)</td><td>Image classique. Lancez le <code>.cue</code> et gardez les fichiers <code>.bin</code> à côté.</td></tr><tr><td>.pbp</td><td>Format des jeux PlayStation de la PSP. Peut contenir plusieurs disques.</td></tr><tr><td>.m3u</td><td>Liste des disques d'un jeu en plusieurs disques (voir <a href="playstation.md#jeux-en-plusieurs-disques">Guides</a>).</td></tr><tr><td>.iso .img .mdf .ccd .toc .cbn .cso</td><td>Autres images disque.</td></tr><tr><td>.zip .7z .squashfs</td><td>Jeu compressé, extrait ou monté avant le lancement.</td></tr><tr><td>.decomp</td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour tous les émulateurs. Les boutons sont placés comme sur la manette PlayStation : **SUD** = Croix, **EST** = Rond, **OUEST** = Carré, **NORD** = Triangle.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (3).png" alt="" width="225"><figcaption></figcaption></figure></div>

Options utiles, dans **CONTRÔLES** :

<table><thead><tr><th width="361.5">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>TYPE DE CONTRÔLEUR JOUEUR 1</strong> (à 4)</td><td>Manette émulée : numérique, DualShock, neGcon, souris… Certains vieux jeux ne reconnaissent que la manette numérique.</td></tr><tr><td><strong>UTILISER LES GÂCHETTES POUR LES JEUX DE COURSE</strong></td><td>Place l'accélérateur et le frein sur les gâchettes (Gran Turismo…).<br><img src="../../../../.gitbook/assets/image (5).png" alt=""></td></tr><tr><td><strong>FORCER LES STICKS ANALOGIQUES</strong></td><td>mednafen_psx_hw : garde la DualShock en mode analogique.</td></tr><tr><td><strong>COMBO DE BOUTONS ANALOG/DIGITAL</strong></td><td>mednafen_psx_hw, swanstation : combinaison qui bascule la DualShock entre analogique et numérique (L1 + R1 + START par défaut avec mednafen_psx_hw).</td></tr></tbody></table>

Avec DuckStation, le bouton **Guide** de la manette sert de bouton Analog, et le multitap est activé automatiquement au-delà de 2 manettes.

**Multitap** : avec les cores libretro et DuckStation, il est activé automatiquement sur le port 1 à partir de 3 manettes, et sur les deux ports à partir de 6. Avec mednafen\_psx\_hw et swanstation, il est désactivé quand les pistolets sont activés. Avec Mednafen, réglez **CONTRÔLES > ADAPTATEUR MULTIJOUEURS**.

### Pistolets

Activez **PISTOLETS > ACTIVER LES PISTOLETS** : la gâchette est sur le clic gauche, le bouton A sur le clic droit et le bouton B sur le clic du milieu. Avec mednafen\_psx\_hw, **TYPE DE PISTOLET** permet de choisir entre le GunCon et le Justifier.

Avec DuckStation, **AFFECTER LE PISTOLET AU JOUEUR 2** branche le GunCon sur le port 2, comme le demande Die Hard Trilogy.

### Raccourcis

Les raccourcis sont sur les mêmes boutons avec tous les émulateurs.

<table><thead><tr><th>Action</th><th>cores libretro</th><th width="127.25">DuckStation</th><th width="120.25">Mednafen</th><th width="111.75">BizHawk</th><th>Clavier (DuckStation, BizHawk)</th></tr></thead><tbody><tr><td><strong>Quitter</strong></td><td>HOTKEY + START</td><td>HOTKEY + START</td><td>HOTKEY + START</td><td>HOTKEY + START</td><td>ÉCHAP</td></tr><tr><td>Sauvegarde instantanée</td><td>HOTKEY + OUEST</td><td>HOTKEY + OUEST</td><td>HOTKEY + OUEST</td><td>HOTKEY + OUEST</td><td>F2</td></tr><tr><td>Chargement instantané</td><td>HOTKEY + NORD</td><td>HOTKEY + NORD</td><td>HOTKEY + NORD</td><td>HOTKEY + NORD</td><td>F4</td></tr><tr><td>Emplacement suivant / précédent</td><td>HOTKEY + HAUT / BAS</td><td>HOTKEY + HAUT / BAS</td><td>HOTKEY + HAUT / BAS</td><td>HOTKEY + HAUT / BAS</td><td>F7 / F6</td></tr><tr><td>Capture d'écran</td><td>HOTKEY + R3</td><td>HOTKEY + R3</td><td>HOTKEY + R3</td><td>HOTKEY + R3</td><td>F8</td></tr><tr><td>Retour en arrière</td><td>HOTKEY + GAUCHE</td><td>HOTKEY + GAUCHE</td><td>HOTKEY + GAUCHE</td><td>HOTKEY + GAUCHE</td><td>RETOUR ARRIÈRE</td></tr><tr><td>Avance rapide</td><td>HOTKEY + DROITE</td><td>HOTKEY + DROITE</td><td>HOTKEY + DROITE</td><td>HOTKEY + DROITE</td><td>L</td></tr><tr><td>Menu de l'émulateur</td><td>HOTKEY + SUD</td><td>HOTKEY + SUD</td><td>—</td><td>—</td><td>F1 (DuckStation)</td></tr><tr><td>Pause</td><td>—</td><td>HOTKEY + L3</td><td>HOTKEY + SUD</td><td>HOTKEY + SUD</td><td>P</td></tr><tr><td>Plein écran</td><td>—</td><td>—</td><td>HOTKEY + L3</td><td>HOTKEY + L3</td><td>F</td></tr><tr><td>Ouvrir / fermer le lecteur</td><td>HOTKEY + L1</td><td>—</td><td>HOTKEY + L1</td><td>—</td><td>—</td></tr><tr><td>Choisir le disque</td><td>—</td><td>HOTKEY + R1</td><td>HOTKEY + R2</td><td>—</td><td>F11 (DuckStation)</td></tr><tr><td>Disque précédent / suivant</td><td>HOTKEY + L2 / R2</td><td>HOTKEY + L2 / R2</td><td>—</td><td>—</td><td>F9 / F10 (DuckStation)</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="362.75">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>Jeux</td><td><code>roms\psx</code></td></tr><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>Cartes mémoire des cores libretro</td><td><code>saves\psx</code></td></tr><tr><td>Cartes mémoire de DuckStation</td><td><code>saves\psx\duckstation\memcards</code></td></tr><tr><td>Cartes mémoire de Mednafen</td><td><code>saves\psx</code> (copies de secours dans <code>saves\psx\mednafen\backup</code>)</td></tr><tr><td>Cartes mémoire de BizHawk</td><td><code>saves\psx\bizhawk</code></td></tr><tr><td>Sauvegardes instantanées des cores libretro</td><td><code>saves\psx\libretro.&#x3C;core></code></td></tr><tr><td>Sauvegardes instantanées de DuckStation</td><td><code>saves\psx\duckstation</code></td></tr><tr><td>Sauvegardes instantanées de BizHawk</td><td><code>saves\psx\bizhawk\sstates\&#x3C;core></code></td></tr><tr><td>Sauvegardes instantanées de Mednafen</td><td><code>saves\psx\mednafen\sstates</code></td></tr><tr><td>Textures personnalisées de mednafen_psx_hw</td><td><code>roms\psx\&#x3C;nom du fichier du jeu>-texture-replacements</code></td></tr><tr><td>Textures personnalisées de DuckStation</td><td><code>emulators\duckstation\textures\&#x3C;identifiant du jeu>\replacements</code></td></tr><tr><td>Codes de triche des cores libretro</td><td><code>cheats\retroarch</code></td></tr><tr><td>Codes de triche de DuckStation</td><td><code>cheats\duckstation</code></td></tr><tr><td>Codes de triche de Mednafen</td><td><code>cheats\mednafen</code></td></tr><tr><td>Codes de triche de BizHawk</td><td><code>cheats\bizhawk\psx</code></td></tr><tr><td>Captures d'écran des cores libretro</td><td><code>screenshots</code></td></tr><tr><td>Captures d'écran de DuckStation</td><td><code>screenshots\duckstation</code></td></tr><tr><td>Captures d'écran de Mednafen</td><td><code>screenshots\mednafen</code></td></tr><tr><td>Captures d'écran de BizHawk</td><td><code>screenshots\bizhawk\psx</code></td></tr><tr><td>Réglages par jeu de DuckStation</td><td><code>emulators\duckstation\gamesettings</code></td></tr><tr><td>Correctifs (patches) de DuckStation</td><td><code>emulators\duckstation\patches</code></td></tr><tr><td>Jaquettes de DuckStation</td><td><code>emulators\duckstation\covers</code></td></tr><tr><td>Configuration de DuckStation</td><td><code>emulators\duckstation\settings.ini</code></td></tr></tbody></table>

Chaque émulateur a ses propres cartes mémoire : une sauvegarde faite avec l'un n'apparaît pas dans l'autre.

Seuls mednafen\_psx\_hw et DuckStation gèrent les textures personnalisées.

## Guides

### Jeux en plusieurs disques

1. Placez tous les disques du jeu dans `roms\psx`.
2. Créez un fichier texte au nom du jeu avec l'extension `.m3u`, par exemple `Final Fantasy VII.m3u`.
3. Écrivez-y le nom de chaque disque, un par ligne :

```
Final Fantasy VII (Disc 1).chd
Final Fantasy VII (Disc 2).chd
Final Fantasy VII (Disc 3).chd
```

4. Lancez le fichier `.m3u`. Quand le jeu demande le disque suivant, utilisez les raccourcis de changement de disque.

Avec les cores libretro : **HOTKEY + L1** ouvre le lecteur, **HOTKEY + R2** passe au disque suivant, **HOTKEY + L1** referme le lecteur.

Avec le fichier `.m3u`, la même carte mémoire sert pour tous les disques.

### Cartes mémoire : une par jeu ou une pour tous

<table><thead><tr><th width="187">Émulateur</th><th width="233.75">Par défaut</th><th>Option</th></tr></thead><tbody><tr><td>DuckStation</td><td>Une carte par jeu</td><td><strong>ÉMULATION > TYPE DE CARTE MÉMOIRE</strong></td></tr><tr><td>mednafen_psx_hw</td><td>Une carte par jeu</td><td><strong>ÉMULATION > UTILISER UNE CARTE MÉMOIRE PARTAGÉE</strong></td></tr><tr><td>swanstation</td><td>Une carte par jeu, gérée par RetroArch</td><td><strong>ÉMULATION > TYPE DE CARTE MÉMOIRE 1</strong></td></tr></tbody></table>

Une carte partagée permet aux jeux qui lisent les sauvegardes d'un autre jeu de les retrouver.

### Textures personnalisées

Deux émulateurs chargent des packs de textures, chacun avec son propre format de pack et son propre dossier.

**libretro: mednafen\_psx\_hw**

1. Dans `roms\psx`, créez un dossier portant le nom du fichier du jeu suivi de `-texture-replacements`. Pour `Mon jeu.chd`, le dossier s'appelle `Mon jeu-texture-replacements`.
2. Copiez-y les textures du pack.
3. Activez **RENDU VISUEL > TEXTURES PERSONNALISÉES**.

**DuckStation**

1. Créez le dossier `emulators\duckstation\textures\<identifiant du jeu>\replacements`, par exemple `emulators\duckstation\textures\SLUS-00594\replacements`. L'identifiant est le numéro de série du jeu.
2. Copiez-y les textures du pack.
3. Activez **RENDU VISUEL > TEXTURES PERSONNALISÉES**. L'option **METTRE EN CACHE LES TEXTURES PERSONNALISÉES** les charge toutes au démarrage, pour éviter les saccades en jeu.

### Codes de triche

<table><thead><tr><th width="166.5">Émulateur</th><th>Comment faire</th></tr></thead><tbody><tr><td>cores libretro</td><td>Menu de RetroArch (<strong>HOTKEY + SUD</strong>), rubrique des codes de triche. Les fichiers sont dans <code>cheats\retroarch</code>.</td></tr><tr><td>DuckStation</td><td>Placez les fichiers dans <code>cheats\duckstation</code>, puis activez les codes dans DuckStation.</td></tr><tr><td>Mednafen</td><td>Activez <strong>ÉMULATION > ACTIVER LA TRICHE</strong>. Les fichiers sont dans <code>cheats\mednafen</code>.</td></tr><tr><td>BizHawk</td><td>Les fichiers sont dans <code>cheats\bizhawk\psx</code>.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="384">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas, BIOS introuvable</td><td>Placez <code>psxonpsp660.bin</code> à la racine de <code>bios</code>, ou le fichier <code>scph</code> de la région du jeu.</td></tr><tr><td>Un <code>.chd</code> ne se lance pas avec Mednafen ou BizHawk</td><td>Ces émulateurs ne lisent pas ce format : changez d'émulateur ou utilisez une image <code>.cue</code>.</td></tr><tr><td>Les sticks ne répondent pas</td><td>Le jeu attend le mode analogique : utilisez le combo L1 + R1 + START (mednafen_psx_hw) ou le bouton Guide (DuckStation). À l'inverse, certains vieux jeux demandent la manette numérique.</td></tr><tr><td>Le jeu demande le disque 2</td><td>Utilisez un fichier <code>.m3u</code> et les raccourcis de changement de disque (voir <a href="playstation.md#jeux-en-plusieurs-disques">Guides</a>).</td></tr><tr><td>Le jeu en réseau n'est pas proposé</td><td>Seuls les cores mednafen_psx_hw et pcsx_rearmed le proposent.</td></tr><tr><td>Mes sauvegardes ont disparu après un changement d'émulateur</td><td>Chaque émulateur a ses propres cartes mémoire (voir <a href="playstation.md#dossiers">Dossiers</a>).</td></tr><tr><td>Les textures personnalisées ne s'affichent pas</td><td>Vérifiez le dossier, qui n'est pas le même pour mednafen_psx_hw et DuckStation (voir <a href="playstation.md#textures-personnalisees">Guides</a>), et que le pack est prévu pour cet émulateur.</td></tr><tr><td>La manette du joueur 3 ne répond pas</td><td>Le multitap n'est activé qu'à partir de 3 manettes branchées, et le jeu doit le gérer. Avec Mednafen, réglez <strong>ADAPTATEUR MULTIJOUEURS</strong>.</td></tr></tbody></table>
