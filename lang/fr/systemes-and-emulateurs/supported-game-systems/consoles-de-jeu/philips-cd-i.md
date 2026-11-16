---
description: Philips
---

# Philips CD-i

<div align="left"><figure><img src="../../../.gitbook/assets/image (617).png" alt="" width="288"><figcaption></figcaption></figure></div>

## Présentation

Le **CD-i** (Compact Disc Interactive) est un lecteur multimédia de Philips, sorti en 1991. Conçu pour le salon autant que pour l'éducation, il lit des CD de jeux, d'encyclopédies et de musique. La **Digital Video Cartridge**, une cartouche à insérer à l'arrière, ajoute le décodage de la vidéo MPEG : elle est nécessaire aux jeux en vidéo réelle (FMV) et aux Vidéo CD. Philips arrête le CD-i en 1998.

Parmi ses jeux : **Hotel Mario**, **Link: The Faces of Evil**, **Zelda: The Wand of Gamelon**, **Burn:Cycle**, **The 7th Guest**, **Dragon's Lair**, **Mad Dog McCree**, **Space Ace**, **Lemmings**, **Tetris**.

RetroBat propose cinq émulateurs : les cores libretro **same\_cdi** (par défaut), **zcdi** et **mame**, **OpenCDi** et **MAME**.

{% embed url="https://fr.wikipedia.org/wiki/CD-i" %}

## En bref

<table><thead><tr><th width="266.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\cdi</code></td></tr><tr><td><strong>Extensions</strong></td><td>.chd .cue .toc .nrg .gdi .iso .cdr .m3u</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>libretro: same_cdi</td></tr><tr><td><strong>BIOS</strong></td><td><code>cdimono1.zip</code> dans <code>bios</code></td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique : cores libretro, OpenCDi ; MAME : PadToKey</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>core zcdi, core mame, OpenCDi (gérées par RetroBat)</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores zcdi et mame</td></tr><tr><td><strong>Pistolets</strong></td><td>core zcdi (Peacekeeper, port 1)</td></tr><tr><td><strong>BIOS optionnels</strong></td><td><code>vmpega.rom</code> (Digital Video Cartridge) pour les jeux FMV avec zcdi et OpenCDi ; <code>impega.rom</code> pour OpenCDi avec le BIOS <code>cdi490a.rom</code></td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="188.25">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>libretro: same_cdi</strong> (défaut)</td><td>Émulation MAME dédiée au CD-i, résolution interne réglable.</td><td>Pas de jeux FMV (Digital Video Cartridge non émulée), pas de sauvegardes instantanées.</td></tr><tr><td><strong>libretro: zcdi</strong></td><td>Jeux FMV avec <code>vmpega.rom</code>, sauvegardes instantanées, jeu en réseau, pistolet Peacekeeper, souris, deux joueurs, changement de disque (<code>.m3u</code>).</td><td>Ne lit pas les <code>.toc</code>, <code>.nrg</code>, <code>.gdi</code> et <code>.cdr</code>.</td></tr><tr><td><strong>libretro: mame</strong></td><td>Émulation MAME complète, sauvegardes instantanées, jeu en réseau.</td><td>Pas de jeux FMV, pas de configuration automatique de la manette.</td></tr><tr><td><strong>opencdi</strong></td><td>Émulateur autonome récent : jeux FMV, sauvegardes instantanées gérées par RetroBat, souris, niveaux vidéo.</td><td>Ne lit pas les <code>.toc</code>, <code>.nrg</code>, <code>.gdi</code> et <code>.cdr</code>. Choisit PAL ou NTSC d'après le nom du fichier.</td></tr><tr><td><strong>mame</strong></td><td>Même émulation que le core mame, en émulateur autonome.</td><td>Pas de jeux FMV, pas de configuration automatique de la manette.</td></tr></tbody></table>

## BIOS

Un seul fichier suffit pour tous les émulateurs : `cdimono1.zip` (jeu de ROM MAME), dans `bios`. RetroBat le copie ou en extrait les fichiers nécessaires à chaque émulateur.

<table><thead><tr><th width="172">Émulateur</th><th width="366.75">Fichiers</th><th>Dossier</th></tr></thead><tbody><tr><td>same_cdi</td><td><code>cdimono1.zip</code> (copié automatiquement depuis <code>bios</code> s'il manque)</td><td><code>bios\same_cdi\bios</code></td></tr><tr><td>core mame, MAME</td><td><code>cdimono1.zip</code></td><td><code>bios</code> ou <code>bios\same_cdi\bios</code></td></tr><tr><td>zcdi</td><td><code>cdi200.rom</code> (NTSC), <code>cdi220b.rom</code> (PAL), extraits automatiquement de <code>cdimono1.zip</code> ; <code>vmpega.rom</code> pour les jeux FMV</td><td><code>bios</code></td></tr><tr><td>OpenCDi</td><td><code>cdimono1.zip</code> ou <code>cdibios.zip</code>, ou <code>cdi220b.rom</code> / <code>cdi200.rom</code> ; <code>vmpega.rom</code> pour les jeux FMV (seul ou dans <code>cdimono1.zip</code>). Avec le BIOS du CD-i 490 (<code>cdi490a.rom</code>, utilisé seulement sans les fichiers précédents), la cartouche vidéo est <code>impega.rom</code></td><td><code>bios</code> ou <code>bios\same_cdi\bios</code></td></tr></tbody></table>

La liste logicielle MAME `cdi.xml` va dans `bios\mame\hash` (facultatif).

<details>

<summary>Contenu de cdimono1.zip et md5</summary>

```
cdimono1.zip
- cdi200.rom "2969341396aa61e0143dc2351aaa6ef6"
- cdi220.rom "ac80a92c988ce07fbd6a8f21ded34cf1"
- cdi220b.rom "ac0d468be366779c9df633be98da250a"
- zx405037p__cdi_servo_2.1__b43t__llek9215.mc68hc705c8a_withtestrom.7201 "3e59b8a9a423d3ecd612a32fe4e2d748"
- zx405042p__cdi_slave_2.0__b43t__zzmk9213.mc68hc705c8a_withtestrom.7206 "3d20cf7550f1b723158b42a1fd5bac62"

vmpega.rom "53ba3bf7443187a657baa272d01d3771"

```

</details>

## Quel format de jeu ?

<table><thead><tr><th width="205.25">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.chd</strong></td><td>Image compressée, lue par tous les émulateurs. Le format conseillé.</td></tr><tr><td><strong>.cue</strong> (+ .bin)</td><td>Image de CD classique, lue par tous les émulateurs.</td></tr><tr><td><strong>.iso</strong></td><td>Image de CD, lue par tous les émulateurs.</td></tr><tr><td><strong>.toc</strong>, <strong>.nrg</strong>, <strong>.gdi</strong>, <strong>.cdr</strong></td><td>Lues seulement par same_cdi et MAME.</td></tr><tr><td><strong>.m3u</strong></td><td>Liste des disques d'un jeu sur plusieurs CD, pour le core zcdi et OpenCDi (voir <a href="philips-cd-i.md#jeux-sur-plusieurs-cd"><strong>Guides</strong></a>).</td></tr></tbody></table>

## Contrôles

### Configuration automatique

La manette CD-i a une croix (ou un pavé) qui déplace un curseur et deux boutons d'action.

| Manette RetroBat    | same\_cdi | zcdi          | OpenCDi  |
| ------------------- | --------- | ------------- | -------- |
| Croix, stick gauche | Curseur   | Curseur       | Curseur  |
| SUD                 | Bouton 1  | Bouton 1      | Bouton 1 |
| EST                 | Bouton 2  | Bouton 2      | Bouton 2 |
| NORD                | —         | Bouton 1      | —        |
| OUEST               | —         | Boutons 1 + 2 | Bouton 2 |
| START               | —         | —             | Bouton 1 |

Avec le core mame et MAME, la manette n'est pas configurée par RetroBat : utilisez la configuration de MAME ou un profil **PadToKey** (voir la page [**PadToKey**](../../../controleurs/pad2key.md)).

### Souris et deuxième joueur

* **Core zcdi** : **CONTRÔLES > TYPE DE CONTRÔLEUR JOUEUR 1** : manette (par défaut) ou souris. **TYPE DE CONTRÔLEUR JOUEUR 2** : aucun, manette ou souris ; une deuxième manette est utilisée automatiquement si elle est branchée.
* **OpenCDi** : **CONTRÔLES > PÉRIPHÉRIQUE DE POINTAGE** : manette (la manette et le clavier déplacent le curseur) ou souris (la souris du PC déplace le curseur, la manette ne garde que ses boutons). **HOTKEY + L3** change de mode en jeu. **SENSIBILITÉ DE LA SOURIS** règle la vitesse du curseur.

### Pistolets

Le core zcdi émule le pistolet **Peacekeeper** sur le port 1 (jeux d'American Laser Games comme **Mad Dog McCree**). Activez **PISTOLETS > ACTIVER LES PISTOLETS**. Pour plus de détails, voir la page [**Pistolets**](../../../controleurs/supported-controllers/lightguns/).

### Raccourcis

**Cores libretro, MAME** : raccourcis RetroArch / RetroBat habituels (sauvegarde, chargement, changement de disque…). Pour plus de détails, voir la page [**Raccourcis**](../../../navigation/hotkeys.md).

**OpenCDi**

<table><thead><tr><th width="267.75">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td><strong>HOTKEY + START</strong></td><td>Quitter</td></tr><tr><td><strong>HOTKEY + SUD</strong></td><td>Pause</td></tr><tr><td><strong>HOTKEY + OUEST</strong></td><td>Sauvegarde instantanée</td></tr><tr><td><strong>HOTKEY + NORD</strong></td><td>Chargement instantané</td></tr><tr><td><strong>HOTKEY + croix haut / bas</strong></td><td>Emplacement de sauvegarde suivant / précédent</td></tr><tr><td><strong>HOTKEY + L3</strong></td><td>Basculer manette / souris</td></tr><tr><td><strong>HOTKEY + R3</strong></td><td>Capture d'écran</td></tr></tbody></table>

## Dossiers

<table><thead><tr><th width="411.5">Contenu</th><th>Dossier</th></tr></thead><tbody><tr><td>BIOS</td><td><code>bios</code></td></tr><tr><td>same_cdi : BIOS</td><td><code>bios\same_cdi\bios</code></td></tr><tr><td>Liste logicielle MAME</td><td><code>bios\mame\hash</code></td></tr><tr><td>Cores zcdi et mame : sauvegardes instantanées</td><td><code>saves\cdi\libretro.&#x3C;core></code></td></tr><tr><td>Core zcdi : mémoire de la console (NVRAM, une par disque)</td><td><code>saves\cdi</code></td></tr><tr><td>OpenCDi : mémoire de la console (une par jeu)</td><td><code>saves\cdi\opencdi\nvram</code></td></tr><tr><td>OpenCDi : mémoire de la console (partagée)</td><td><code>saves\cdi\opencdi\nvram_mk48t08.bin</code></td></tr><tr><td>OpenCDi : sauvegardes instantanées</td><td><code>saves\cdi\opencdi</code></td></tr><tr><td>OpenCDi : captures d'écran</td><td><code>screenshots</code></td></tr></tbody></table>

## Guides

### Jeux FMV (Digital Video Cartridge)

Les jeux en vidéo réelle (**Dragon's Lair**, **Space Ace**, **Mad Dog McCree**, **Who Shot Johnny Rock?**, **Burn:Cycle**…) et les Vidéo CD demandent la Digital Video Cartridge. Seuls **zcdi** et **OpenCDi** l'émulent, avec le fichier `vmpega.rom` dans `bios` :

* **zcdi** l'utilise automatiquement quand le fichier est présent ;
* **OpenCDi** le cherche aussi dans `cdimono1.zip` ; **ÉMULATION > CARTOUCHE VIDÉO NUMÉRIQUE (DVC)** permet de la retirer.

Avec same\_cdi, le core mame et MAME, ces jeux ne démarrent pas : choisissez zcdi ou OpenCDi pour eux.

### Jeux sur plusieurs CD

Créez un fichier `.m3u` dans `roms\cdi`, avec une ligne par disque, dans l'ordre :

```
Burn Cycle (Europe) (Disc 1).chd
Burn Cycle (Europe) (Disc 2).chd
```

* **Core zcdi** : changement de disque avec les raccourcis RetroArch.
* **OpenCDi** démarre sur le premier disque ; les suivants s'insèrent en jeu avec `Ctrl` + `I`. Avec **MÉMOIRE DE LA CONSOLE (NVRAM) > PAR JEU**, tous les disques partagent la même mémoire.

### Démarrage du jeu

Sur un vrai lecteur, le CD-i peut s'arrêter sur son menu : il faut alors choisir **PLAY CD-I** pour lancer le disque.

* **Core zcdi** : **ÉMULATION > LECTURE AUTOMATIQUE** (activée par défaut) lance le disque directement.
* **OpenCDi** lance le disque directement.
* **same\_cdi, core mame, MAME** : si le menu s'affiche, sélectionnez **PLAY CD-I** avec le curseur, puis appuyez sur le bouton 1.

### Autres options utiles

<table><thead><tr><th width="335.25">Option</th><th>Effet</th></tr></thead><tbody><tr><td><strong>RÉSOLUTION INTERNE</strong> (same_cdi)</td><td>Image plus fine, de 640x480 (native) à 3840x2160.</td></tr><tr><td><strong>ÉMULATION > LIMITER LES FPS</strong> (same_cdi)</td><td>À activer si le jeu tourne trop vite sur un écran à haute fréquence.</td></tr><tr><td><strong>ÉMULATION > RÉGION</strong> (zcdi)</td><td>NTSC (<code>cdi200.rom</code>) ou PAL (<code>cdi220b.rom</code>).</td></tr><tr><td><strong>ÉMULATION > MÉMOIRE DE LA CONSOLE (NVRAM)</strong> (OpenCDi)</td><td>Une mémoire par jeu (jamais pleine) ou une mémoire partagée comme sur un vrai lecteur.</td></tr><tr><td><strong>RENDU VISUEL > NIVEAUX VIDÉO</strong> (OpenCDi)</td><td>Studio (noir gris foncé, comme une TV d'époque) ou plage complète (noir profond).</td></tr></tbody></table>

## Problèmes connus

| Problème                                                                | Solution                                                                                                                            |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| Un jeu FMV (Dragon's Lair, Mad Dog McCree…) ne démarre pas              | Utilisez zcdi ou OpenCDi, avec `vmpega.rom` dans `bios`.                                                                            |
| Le jeu reste sur le menu du CD-i                                        | Choisissez **PLAY CD-I**, ou utilisez zcdi / OpenCDi qui lancent le disque directement.                                             |
| OpenCDi lance un jeu américain en PAL                                   | OpenCDi choisit NTSC quand le nom du fichier contient `(USA)`, `(Japan)` ou `NTSC` : gardez le nom No-Intro / Redump du jeu.        |
| Un `.toc`, `.nrg`, `.gdi` ou `.cdr` ne démarre pas avec zcdi ou OpenCDi | Convertissez le jeu en `.chd`, ou utilisez same\_cdi.                                                                               |
| OpenCDi indique un BIOS manquant                                        | Placez `cdimono1.zip` (ou `cdi220b.rom`) dans `bios`.                                                                               |
| Une sauvegarde instantanée d'OpenCDi ne se charge plus                  | Les sauvegardes faites avec OpenCDi 0.3.0 ou avant ne sont pas compatibles avec la version 0.4.0 : utilisez les sauvegardes du jeu. |
