---
description: Sega
---

# Dreamcast

<div align="left"><figure><img src="../../../../.gitbook/assets/image (605).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **Dreamcast** est la dernière console de salon de Sega. Elle sort en novembre 1998 au Japon, puis en septembre 1999 aux États-Unis et en octobre 1999 en Europe. Elle repose sur un processeur Hitachi SH-4 et une puce graphique PowerVR2 de NEC, et lit ses jeux sur des **GD-ROM**, des disques d'environ 1 Go propres à Sega.

C'est la première console vendue avec un modem, pour jouer et naviguer en ligne. Sa manette accueille le **VMU**, une carte mémoire avec un petit écran, et le **Puru Puru Pack** (vibrations). Malgré de très bons jeux, la console s'est vendue à environ 9 millions d'exemplaires et Sega a arrêté sa production en 2001 pour se consacrer au développement de jeux. Parmi ses jeux marquants : Shenmue, Soulcalibur, Jet Set Radio, Crazy Taxi, Sonic Adventure, Phantasy Star Online, Skies of Arcadia ou Resident Evil Code: Veronica.

RetroBat propose quatre émulateurs : le core libretro **flycast** (par défaut), **Flycast** en version autonome, **Redream** et **Demul**.

{% embed url="https://fr.wikipedia.org/wiki/Dreamcast" %}

## En bref

<table><thead><tr><th width="264"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\dreamcast</code></td></tr><tr><td><strong>Extensions</strong></td><td>.mds .mdf .cue .cdi .gdi .chd .m3u</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: flycast</td></tr><tr><td><strong>BIOS</strong></td><td><code>dc_boot.bin</code> et <code>dc_flash.bin</code> dans <code>bios\dc</code></td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, Flycast</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, Flycast</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>cores libretro, Flycast, Demul</td></tr><tr><td><strong>Volants</strong></td><td>Flycast</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>dc.zip</code> dans <code>bios\dc</code> (Demul)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="155.75">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: flycast</strong> (défaut)</td><td>Très bonne compatibilité. Sauvegardes instantanées, RetroAchievements, shaders et raccourcis de RetroArch. Textures personnalisées, résolution augmentée, VMU affiché à l'écran.</td><td>—</td></tr><tr><td><strong>flycast</strong></td><td>Même base que le core, avec ses propres menus. RetroAchievements, sauvegardes instantanées, jeu en ligne (GGPO, DCNet).</td><td>Ne lit pas les <code>.m3u</code> ni les <code>.mds</code> / <code>.mdf</code>.</td></tr><tr><td><strong>redream</strong></td><td>Simple et léger, bonne compatibilité.</td><td>Résolution supérieure à la résolution native réservée à la version payante (clé Redream). Pas de sauvegardes instantanées gérées par RetroBat.</td></tr><tr><td><strong>demul</strong></td><td>Émulateur historique, aussi utilisé pour l'arcade (Naomi, Atomiswave).</td><td>Moins compatible pour la Dreamcast, demande <code>dc.zip</code>. Ne lit pas les <code>.m3u</code>.</td></tr></tbody></table>

Si un jeu pose problème avec le core flycast, essayez Flycast autonome, puis Redream.

## BIOS

<table><thead><tr><th width="136.5">Fichier</th><th width="92">Dossier</th><th width="175.5">Utilisé par</th><th>MD5</th></tr></thead><tbody><tr><td><code>dc_boot.bin</code></td><td><code>bios\dc</code></td><td>flycast (core et autonome)</td><td><code>e10c53c2f8b90bab96ead2d368858623</code></td></tr><tr><td><code>dc_flash.bin</code></td><td><code>bios\dc</code></td><td>flycast (core et autonome)</td><td><code>0a93f7940c455905bea6e392dfde92a4</code></td></tr><tr><td><code>dc.zip</code></td><td><code>bios\dc</code></td><td>Demul (optionnel pour les autres)</td><td>voir ci-dessous</td></tr></tbody></table>

Le core flycast et Flycast autonome lisent tous les deux le BIOS dans `bios\dc`. Leur option **ÉMULATION > BIOS HLE** (core) ou **ÉMULATION > UTILISER LE BIOS HLE** (Flycast) remplace le BIOS par une émulation : elle permet de jouer sans BIOS, mais avec une compatibilité plus faible.

Redream n'utilise pas les fichiers de `bios\dc`.

`dc.zip` est le BIOS au format MAME, nécessaire à Demul. Il contient :

```
1_01d_01.bin   e10c53c2f8b90bab96ead2d368858623
1_01d_02.bin   a5c6a00818f97c5e3e91569ee22416dc
1_004_01.bin   37c921eb47532cae8fb70e5d987ce91c
1_011_01.bin   eafca1eed2d7f76c487e940597c2a786
```

### Langue et région de la console

La langue des jeux est celle de la console émulée. Elle se règle avec **ÉMULATION > LANGUE** (core flycast, Flycast, Redream), et la région avec **ÉMULATION > RÉGION** (Demul : **ÉMULATION > RÉGION DE LA DREAMCAST**). **VIDÉO > FORMAT VIDÉO ÉMULÉ** choisit NTSC ou PAL.

## Quel format de jeu ?

<table><thead><tr><th width="160.25">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.chd</strong></td><td>Format compressé, le plus pratique. Lu par les quatre émulateurs.</td></tr><tr><td><strong>.gdi</strong></td><td>Copie complète du GD-ROM (fichier <code>.gdi</code> et ses pistes). Lu par les quatre émulateurs.</td></tr><tr><td><strong>.cdi</strong></td><td>Image de CD gravable (jeux indépendants, versions modifiées).</td></tr><tr><td><strong>.cue</strong></td><td>Image de CD avec pistes <code>.bin</code> (core flycast, Flycast).</td></tr><tr><td><strong>.mds</strong> / <strong>.mdf</strong></td><td>Images Alcohol 120% (Demul).</td></tr><tr><td><strong>.m3u</strong></td><td>Jeux sur plusieurs disques (voir <a href="dreamcast.md#jeux-sur-plusieurs-disques">Guides</a>) : core flycast et Redream uniquement. Avec Redream, RetroBat lance le disque choisi dans <strong>ÉMULATION > NUMÉRO DU DISQUE M3U</strong> (le premier par défaut).</td></tr></tbody></table>

Les archives `.zip` et `.7z` ne sont pas acceptées.

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour les quatre émulateurs, jusqu'à 4 joueurs.

<table><thead><tr><th width="324">Dreamcast</th><th>Manette</th></tr></thead><tbody><tr><td>A</td><td>SUD</td></tr><tr><td>B</td><td>EST</td></tr><tr><td>X</td><td>OUEST</td></tr><tr><td>Y</td><td>NORD</td></tr><tr><td>Gâchettes L et R</td><td>L2, R2</td></tr><tr><td>Start</td><td>START</td></tr><tr><td>Croix directionnelle, stick analogique</td><td>Croix directionnelle, stick gauche</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (606).png" alt="" width="225"><figcaption></figcaption></figure></div>

* **CONTRÔLES > UTILISER R1 ET L1** place les gâchettes L et R sur L1 et R1 (les quatre émulateurs).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (607).png" alt="" width="225"><figcaption></figcaption></figure></div>

* **Flycast** : **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** (à 4) choisit le périphérique (manette, pistolet, clavier, souris, arcade stick, maracas de Samba de Amigo, canne à pêche, manette de course…), et **EXTENSION MANETTE 1** (à 4) ce qui est branché dans la manette (VMU, Puru Puru, microphone).
* **Core flycast** : **CONTRÔLES > TYPE DE CONTRÔLEUR** choisit le périphérique pour tous les joueurs. Chaque manette a un VMU et un Puru Puru Pack.
* **Demul** : **EXTENSION MANETTE 1** (à 4) ajoute un Puru Puru Pack ou un microphone.
* **Redream** : **CONTRÔLES > UTILISER LA CONFIGURATION AUTOMATIQUE DE L'ÉMULATEUR** laisse Redream configurer les manettes lui-même.

### Pistolets

Les jeux au pistolet (The House of the Dead 2, Confidential Mission…) fonctionnent avec le core flycast (jusqu'à 4 pistolets), Flycast (2 pistolets, 4 avec DemulShooter) et Demul (1 pistolet, 2 avec DemulShooter). Pour les options et les boutons, voir la page [**Contrôle des pistolets**](../../../../controleurs/pistolets_controles.md).

### Volants

Flycast gère les volants (**VOLANTS DE COURSE > ACTIVER LES VOLANTS**). **VOLANTS DE COURSE > UTILISER LE RACING CONTROLLER** émule la manette de course de Sega. Le core flycast gère aussi les volants, mais RetroBat ne fournit pas encore son fichier de mappage. Pour les volants pris en charge, voir la page [**Volants**](../../../../controleurs/supported-controllers/volants.md).

### Raccourcis

Le core flycast utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

**Flycast**

<table><thead><tr><th width="188.25">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td>Échap</td></tr><tr><td><strong>HOTKEY + SUD</strong></td><td>Menu de Flycast</td><td>F1</td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement instantané</td><td>F4</td></tr><tr><td><strong>HOTKEY + DROITE</strong></td><td>Avance rapide (maintenir)</td><td>L</td></tr><tr><td><strong>HOTKEY + R3</strong></td><td>Capture d'écran</td><td>F8</td></tr></tbody></table>

Flycast n'a pas de raccourci pour changer d'emplacement de sauvegarde.

**Redream**

<table><thead><tr><th width="239">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr></tbody></table>

**Demul**

<table><thead><tr><th width="192">Raccourci</th><th>Action</th><th>Clavier</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td><td></td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée de Demul</td><td>F2</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement instantané de Demul</td><td>F4</td></tr></tbody></table>

Les sauvegardes instantanées de Demul restent dans Demul : elles n'apparaissent pas dans le gestionnaire de sauvegardes.

## Dossiers

<table><thead><tr><th width="379">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS (core flycast, Flycast)</td><td><code>bios\dc</code></td></tr><tr><td>Core flycast : VMU</td><td><code>bios\dc</code> (fichiers <code>vmu_save_*.bin</code>)</td></tr><tr><td>Core flycast : sauvegardes instantanées</td><td><code>saves\dreamcast\libretro.flycast</code></td></tr><tr><td>Textures personnalisées (core flycast, Flycast)</td><td><code>bios\dc\textures\&#x3C;ID du jeu></code></td></tr><tr><td>Flycast : VMU</td><td><code>saves\dreamcast\flycast\vmu</code></td></tr><tr><td>Flycast : sauvegardes instantanées</td><td><code>saves\dreamcast\flycast\sstates</code> (copiées depuis <code>saves\dreamcast\reicast\states</code>)</td></tr><tr><td>Flycast : configuration</td><td><code>emulators\flycast\emu.cfg</code></td></tr><tr><td>Redream : configuration et sauvegardes</td><td><code>emulators\redream</code></td></tr><tr><td>Demul : sauvegardes (NVRAM)</td><td><code>saves\dreamcast\demul</code></td></tr><tr><td>Demul : configuration</td><td><code>emulators\demul\Demul.ini</code></td></tr></tbody></table>

Les VMU du core flycast et de Flycast sont synchronisés à chaque lancement : le fichier le plus récent est copié dans l'autre dossier, vous retrouvez donc vos sauvegardes avec les deux. Pour un VMU par jeu, utilisez **ÉMULATION > FICHIERS DE SAUVEGARDE** (core) ou **ÉMULATION > VMU PAR JEU** (Flycast).

<div align="left"><figure><img src="../../../../.gitbook/assets/image (608).png" alt=""><figcaption></figcaption></figure></div>

## Guides

### Jeux sur plusieurs disques

1. Créez un fichier texte dans `roms\dreamcast`, avec l'extension `.m3u` (par exemple `Alone in the Dark - The New Nightmare.m3u`).
2. Écrivez une ligne par disque, dans l'ordre, avec le chemin de chaque disque à partir du dossier du fichier `.m3u` :

```
Alone in the Dark - The New Nightmare (Disc 1).gdi
Alone in the Dark - The New Nightmare (Disc 2).gdi
```

<div align="left"><figure><img src="../../../../.gitbook/assets/image (609).png" alt=""><figcaption></figcaption></figure></div>

3. Mettez à jour la liste des jeux : RetroBat masque les disques et n'affiche que le fichier `.m3u`.

Avec le core flycast, changez de disque avec les raccourcis de disque de RetroArch. Avec Redream, choisissez le disque à lancer avec **ÉMULATION > NUMÉRO DU DISQUE M3U**.

### Textures personnalisées

1. Copiez le pack de textures dans `bios\dc\textures\<ID du jeu>` : le dossier sert au core flycast et à Flycast. Le nom du dossier (ID du jeu) est indiqué avec le pack.

<div align="left"><figure><img src="../../../../.gitbook/assets/image (610).png" alt="" width="267"><figcaption></figcaption></figure></div>

2. Activez **RENDU VISUEL > TEXTURES PERSONNALISÉES** pour le système ou pour le jeu.

### Jouer en ligne avec Flycast

Flycast sait se connecter aux serveurs de jeu en ligne remis en service par la communauté (Phantasy Star Online, Quake III Arena…) avec **RÉSEAU > UTILISER DCNET**. **RÉSEAU > MODE RÉSEAU** permet aussi de jouer à plusieurs en ligne avec **GGPO** (jeux de combat) ou en émulant le câble de combat (**BATTLE CABLE**). **RÉSEAU > MODE HÔTE** et **RÉSEAU > SERVEUR** indiquent qui héberge la partie.

Ce jeu en ligne est propre à Flycast : il ne passe pas par le jeu en réseau de RetroBat.

### Autres options utiles

<table><thead><tr><th width="331.5">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong></td><td>Augmente la résolution de rendu (core flycast, Flycast, Demul ; Redream : version payante au-delà de la résolution native).</td></tr><tr><td><strong>RAPPORT D'ASPECT</strong></td><td>Flycast, Redream, Demul : 4:3, 16:9 ou étiré.</td></tr><tr><td><strong>RENDU VISUEL > HACK ÉCRAN LARGE</strong> / <strong>PATCH ÉCRAN LARGE</strong></td><td>Affichage en 16:9 : le hack étend l'image de tous les jeux (avec des défauts), les patchs corrigent les jeux compatibles.</td></tr><tr><td><strong>VIDÉO > TYPE DE CÂBLE</strong></td><td>VGA, RVB ou composite. Certains jeux refusent le câble VGA.</td></tr><tr><td><strong>RENDU VISUEL > TRI ALPHA</strong></td><td>Corrige les transparences mal affichées dans certains jeux.</td></tr><tr><td><strong>ÉMULATION > AFFICHER L'ÉCRAN DU VMU</strong></td><td>Core flycast : affiche l'écran du VMU dans un coin de l'image.</td></tr><tr><td><strong>ÉMULATION > CHARGEMENT RAPIDE DU GD-ROM</strong></td><td>Core flycast : accélère les chargements, peut gêner certains jeux.</td></tr></tbody></table>

## Problèmes connus

<table><thead><tr><th width="361.5">Problème</th><th>Solution</th></tr></thead><tbody><tr><td>Le jeu ne démarre pas avec le core flycast ou Flycast</td><td>Vérifiez <code>dc_boot.bin</code> et <code>dc_flash.bin</code> dans <code>bios\dc</code>, puis essayez un autre émulateur.</td></tr><tr><td>Demul ne démarre pas</td><td>Vérifiez la présence de <code>dc.zip</code> dans <code>bios\dc</code>.</td></tr><tr><td>Un jeu sur plusieurs disques ne se lance pas avec Flycast ou Demul</td><td>Ces émulateurs ne lisent pas les <code>.m3u</code> : utilisez le core flycast ou Redream.</td></tr><tr><td>Écran noir ou image instable au démarrage</td><td>Changez <strong>VIDÉO > TYPE DE CÂBLE</strong> (certains jeux ne fonctionnent qu'en RVB ou composite).</td></tr><tr><td>Les gâchettes ne répondent pas sur une manette sans gâchettes analogiques</td><td>Activez <strong>CONTRÔLES > UTILISER R1 ET L1</strong>.</td></tr><tr><td>Les sauvegardes de Redream n'apparaissent pas dans Flycast</td><td>Redream garde ses VMU dans son propre dossier : seuls le core flycast et Flycast partagent leurs VMU.</td></tr><tr><td>Redream reste en résolution native</td><td>La résolution augmentée demande une clé Redream (version payante).</td></tr></tbody></table>

La **Naomi** et l'**Atomiswave**, des cartes d'arcade proches de la Dreamcast, ont leurs propres pages : voir les pages [**Sega Naomi**](../../arcade/sega/sega-naomi.md)**,** [**Sega Naomi 2**](../../arcade/sega/sega-naomi-2.md) et [**Atomiswave**](../../arcade/atomiswave.md).
