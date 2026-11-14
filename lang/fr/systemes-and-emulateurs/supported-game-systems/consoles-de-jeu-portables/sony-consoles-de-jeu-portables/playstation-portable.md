---
description: Sony
---

# PlayStation Portable

<div align="left"><figure><img src="../../../../.gitbook/assets/image (593).png" alt="" width="425"><figcaption></figcaption></figure></div>

## Présentation

La **PlayStation Portable** (PSP) est la première console portable de Sony. Elle sort en décembre 2004 au Japon, en mars 2005 aux États-Unis et en septembre 2005 en Europe. Elle se distingue par son grand écran large de 4,3 pouces (480x272), sa puissance proche de celle de la PlayStation 2, le Wi-Fi et un support propre à Sony, l'**UMD**, un petit disque optique dans une cartouche.

Plusieurs modèles se succèdent : PSP-1000, PSP Slim & Lite (2000), PSP-3000, la **PSP Go** (2009) sans lecteur UMD et dont les jeux sont téléchargés, puis la PSP Street (E1000) en 2011. La PSP s'est vendue à environ 80 millions d'exemplaires et sa production s'est arrêtée en 2014. Parmi ses jeux marquants : Monster Hunter Freedom Unite, God of War: Chains of Olympus, Crisis Core: Final Fantasy VII, Metal Gear Solid: Peace Walker, Grand Theft Auto: Liberty City Stories, Patapon ou LocoRoco.

RetroBat utilise **PPSSPP**, un émulateur libre très abouti qui fait tourner la quasi-totalité de la ludothèque, en version autonome ou en core libretro.

{% embed url="https://fr.wikipedia.org/wiki/PlayStation_Portable" %}

## En bref

<table><thead><tr><th width="274"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\psp</code></td></tr><tr><td><strong>Extensions</strong></td><td>.iso .cso .pbp .elf .prx .chd .zip .7z .squashfs .decomp</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>ppsspp</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique, tous les émulateurs</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>cores libretro, PPSSPP</td></tr><tr><td><strong>RetroAchievements</strong></td><td>cores libretro, PPSSPP</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>cores libretro (ppsspp)</td></tr></tbody></table>

## Quel émulateur choisir ?

<table><thead><tr><th width="164.5">Émulateur</th><th>Points forts</th><th>Limites</th></tr></thead><tbody><tr><td><strong>ppsspp</strong> (défaut)</td><td>Version la plus récente de PPSSPP, nombreux réglages (filtres de textures matériels, MSAA, shaders de PPSSPP), Vulkan, OpenGL ou Direct3D 11.</td><td>Pas de décorations (bezels).</td></tr><tr><td><strong>libretro: ppsspp</strong></td><td>Fonctions de RetroArch (shaders, décorations, retour arrière, jeu en réseau).</td><td>Moins de réglages que la version autonome.</td></tr></tbody></table>

Les deux versions partagent la même carte mémoire (`saves\psp`) : les sauvegardes des jeux, les DLC, les textures personnalisées et les codes de triche servent aux deux.

## BIOS

La PSP n'a pas besoin de BIOS : PPSSPP émule le système de la console lui-même.

Le core libretro utilise des fichiers système (polices de la PSP, base de compatibilité), fournis avec RetroBat dans `bios\PPSSPP`. Il n'y a rien à ajouter.

### Langue de la console

La langue des jeux est celle de la console émulée :

* par défaut, c'est la langue de RetroBat ;
* l'option **ÉMULATION > LANGUE** force une langue : anglais, français, allemand, espagnol, italien, néerlandais, portugais, japonais, chinois simplifié ou traditionnel, coréen ou russe.

Un jeu qui n'existe pas dans la langue choisie s'affiche dans sa langue par défaut, souvent l'anglais.

## Quel format de jeu ?

<table><thead><tr><th width="235.25">Format</th><th>Remarques</th></tr></thead><tbody><tr><td><strong>.iso</strong></td><td>Image du disque UMD.</td></tr><tr><td><strong>.cso</strong></td><td>Image compressée, plus petite que l'ISO.</td></tr><tr><td><strong>.chd</strong></td><td>Image compressée, comme pour les autres systèmes à disque.</td></tr><tr><td><strong>.pbp</strong></td><td>Jeu téléchargé (PlayStation Store, PSP Go) ou homebrew (<code>EBOOT.PBP</code>).</td></tr><tr><td><strong>.elf</strong>, <strong>.prx</strong></td><td>Homebrews et programmes de développement.</td></tr><tr><td><strong>.zip</strong>, <strong>.7z</strong>, <strong>.squashfs</strong></td><td>Archive d'un seul jeu, décompressée au lancement.</td></tr><tr><td><strong>.decomp</strong></td><td>Portage PC, voir la page <a href="../../autres/recomp.md"><strong>Recompilations</strong></a>.</td></tr></tbody></table>

Le `.cso` et le `.chd` sont les formats recommandés pour gagner de la place.

Les jeux PlayStation vendus pour PSP (« PSone Classics », en `.pbp`) ne sont pas lus par PPSSPP : placez-les dans le système PlayStation (`roms\psx`).

## Contrôles

### Configuration automatique

RetroBat configure automatiquement les manettes pour les deux émulateurs. L'option **AUTOCONFIGURER LES MANETTES** permet de désactiver cette configuration pour garder celle faite dans PPSSPP.

<table><thead><tr><th width="240.25">PSP</th><th>Manette</th></tr></thead><tbody><tr><td>Croix</td><td>SUD</td></tr><tr><td>Rond</td><td>EST</td></tr><tr><td>Carré</td><td>OUEST</td></tr><tr><td>Triangle</td><td>NORD</td></tr><tr><td>L, R</td><td>L1, R1</td></tr><tr><td>SELECT, START</td><td>SELECT, START</td></tr><tr><td>Croix directionnelle</td><td>Croix directionnelle</td></tr><tr><td>Stick analogique</td><td>Stick gauche</td></tr></tbody></table>

<div align="left"><figure><img src="../../../../.gitbook/assets/image (594).png" alt="" width="225"><figcaption></figcaption></figure></div>

**PPSSPP** :

* La PSP n'a qu'un joueur : jusqu'à 4 manettes sont configurées et toutes contrôlent la console.
* PPSSPP lit les manettes de trois façons : XInput (manettes Xbox), HID (DualShock 4, DualSense, Switch Pro) et DirectInput (autres manettes, sticks arcade). Les options **PILOTES > ACTIVER LES PÉRIPHÉRIQUES XINPUT**, **ACTIVER LES PÉRIPHÉRIQUES DIRECTINPUT** et **ACTIVER LES PÉRIPHÉRIQUES HID** sont activées par défaut. N'en désactivez une que si une manette est vue deux fois ou ne répond pas.
* **CONTRÔLES > FORCER L'INDEX DE LA MANETTE** choisit à la main la manette du joueur 1, si elle n'est pas reconnue.
* **CONTRÔLES > UTILISER O POUR CONFIRMER (EST)** valide avec Rond au lieu de Croix dans les menus du système, comme sur les consoles japonaises.
* **CONTRÔLES > UTILISER LA SOURIS** permet d'utiliser la souris dans PPSSPP.
* **MANETTES AVANT LES STICKS ARCADE** donne la première place aux manettes.

**Core libretro** : l'option **CONTRÔLES > BOUTON POUR CONFIRMER** choisit **CROIX** ou **CERCLE** pour valider.

### Raccourcis

**PPSSPP**

| Raccourci                   | Action                                  | Clavier        |
| --------------------------- | --------------------------------------- | -------------- |
| **HOTKEY + START**          | Quitter                                 | ÉCHAP          |
| **HOTKEY + OUEST**          | Sauvegarde instantanée                  | F2             |
| **HOTKEY + NORD**           | Chargement de la sauvegarde instantanée | F4             |
| **HOTKEY + HAUT** / **BAS** | Emplacement suivant / précédent         | F7 / F6        |
| **HOTKEY + SUD**            | Pause avec le menu de PPSSPP            | F1             |
| **HOTKEY + L3**             | Pause sans menu                         | P              |
| **HOTKEY + R3**             | Capture d'écran                         | F8             |
| **HOTKEY + GAUCHE**         | Retour arrière (option **REMBOBINAGE**) | RETOUR ARRIÈRE |
| **HOTKEY + DROITE**         | Avance rapide                           | L              |
| —                           | Image par image                         | K              |
| —                           | Plein écran                             | F              |

Ces raccourcis peuvent être modifiés. Pour plus de détails, voir la page [**Raccourcis**](../../../../navigation/hotkeys.md#personnaliser-les-raccourcis).

**Core libretro** : le core ppsspp utilise les raccourcis standards de RetroArch (voir la page [**Raccourcis**](../../../../navigation/hotkeys.md)).

## Dossiers

| Contenu                                                    | Dossier                                                        |
| ---------------------------------------------------------- | -------------------------------------------------------------- |
| Carte mémoire émulée, commune aux deux émulateurs          | `saves\psp`                                                    |
| Sauvegardes des jeux                                       | `saves\psp\SAVEDATA`                                           |
| DLC et mises à jour des jeux                               | `saves\psp\GAME\<identifiant>`                                 |
| Textures personnalisées                                    | `saves\psp\TEXTURES\<identifiant>`                             |
| Codes de triche                                            | `saves\psp\Cheats`                                             |
| PPSSPP : sauvegardes instantanées (gérées par RetroBat)    | `saves\psp\ppsspp`                                             |
| PPSSPP : sauvegardes instantanées (dossier de l'émulateur) | `saves\psp\PPSSPP_STATE`                                       |
| PPSSPP : captures d'écran                                  | `saves\psp\SCREENSHOT`                                         |
| PPSSPP : configuration                                     | `saves\psp\SYSTEM\ppsspp.ini`, `saves\psp\SYSTEM\controls.ini` |
| libretro : sauvegardes instantanées                        | `saves\psp\libretro.ppsspp`                                    |
| libretro : fichiers système du core                        | `bios\PPSSPP`                                                  |

L'identifiant d'un jeu (par exemple `ULES01213`) est affiché par PPSSPP dans les informations du jeu, et sur la jaquette ou le disque UMD.

## Guides

### DLC et mises à jour

Les DLC et les mises à jour des jeux se placent dans `saves\psp\GAME`, dans un dossier au nom de l'identifiant du jeu, par exemple `saves\psp\GAME\ULES01213`. Ils sont lus par les deux émulateurs.

### Textures personnalisées

PPSSPP peut remplacer les textures d'un jeu par des textures en haute définition.

1. Placez le pack de textures dans `saves\psp\TEXTURES`, dans un dossier au nom de l'identifiant du jeu (par exemple `TEXTURES\ULES01213`).
2. Activez l'option **RENDU VISUEL > TEXTURES PERSONNALISÉES**.

### Codes de triche

Les deux émulateurs lisent les codes au format CWCheat dans `saves\psp\Cheats`, un fichier par jeu nommé avec l'identifiant (par exemple `ULES01213.ini`).

1. Placez le fichier de codes dans `saves\psp\Cheats`. Avec PPSSPP, vous pouvez aussi y mettre la base `cheat.db` et importer les codes depuis le menu de triche de PPSSPP.
2. Activez l'option **ÉMULATION > ACTIVER LA TRICHE**.
3. Avec PPSSPP, ouvrez le menu en jeu (**HOTKEY + SUD**), puis **Cheats**, et cochez les codes à utiliser. Le core libretro utilise les codes marqués comme actifs dans le fichier (ligne `_C1`).

Avec le core libretro, les codes sont désactivés en mode hardcore de RetroAchievements.

### Shaders par jeu (PPSSPP)

L'option **SHADERS** applique un shader de PPSSPP à tous les jeux. Pour un jeu précis, vous pouvez enchaîner plusieurs shaders :

1. Créez à côté du jeu un fichier texte du même nom avec l'extension `.shaderlist`, par exemple `roms\psp\Patapon.shaderlist` pour `Patapon.iso`.
2. Écrivez un nom de shader de PPSSPP par ligne (par exemple `FXAA`, puis `Vignette`).

Ce fichier passe avant l'option SHADERS.

### Autres options utiles

**PPSSPP**

| Option                                                                                       | Effet                                                                                                                                                                         |
| -------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **RÉSOLUTION INTERNE**                                                                       | Augmente la résolution de rendu (jusqu'à x10). La résolution native est 480x272.                                                                                              |
| **RAPPORT D'ASPECT**                                                                         | 16:9 (écran de la PSP, par défaut), 4:3, 1:1 ou **ETIRÉ**.                                                                                                                    |
| **MISE À L'ÉCHELLE (NOMBRE ENTIER)**                                                         | Agrandit l'image d'un nombre entier de fois, pour des pixels nets.                                                                                                            |
| **ÉMULATION > REMBOBINAGE**                                                                  | Active le retour arrière (**HOTKEY + GAUCHE**).                                                                                                                               |
| **VIDÉO > SAUT D'IMAGE** / **TYPE DE SAUT D'IMAGES**                                         | Saute des images pour gagner en vitesse, en nombre fixe ou automatiquement.                                                                                                   |
| **RENDU VISUEL > FILTRE D'AGRANDISSEMENT DES TEXTURES** et **MISE À L'ÉCHELLE DES TEXTURES** | Lisse les textures agrandies. Les filtres « HARDWARE » sont plus rapides mais ne marchent qu'avec Vulkan : RetroBat passe en Vulkan si le pilote vidéo est laissé par défaut. |
| **RENDU VISUEL > ANTICRÉNELAGE (MSAA)**                                                      | Lisse les bords des objets 3D.                                                                                                                                                |
| **PILOTES > VIDÉO**                                                                          | VULKAN (par défaut), OPENGL ou DIRECT3D 11.                                                                                                                                   |

**Core libretro**

| Option                                              | Effet                                                                                             |
| --------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| **ÉMULATION > MODE PERFORMANCE**                    | Rapide, Équilibré ou Précis : règle d'un coup plusieurs options de vitesse et de précision.       |
| **ÉMULATION > MODE D'ÉXECUTION CPU**                | Recompilateur (JIT, par défaut), interpréteur IR ou interpréteur, plus lent mais plus compatible. |
| **ÉMULATION > IGNORER LES ERREURS D'ACCÉS MÉMOIRE** | Peut corriger certains plantages.                                                                 |

## Problèmes connus

| Problème                                                      | Solution                                                                                                                                                       |
| ------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Un jeu PlayStation en `.pbp` ne démarre pas                   | PPSSPP ne lit pas les jeux PlayStation : placez-le dans `roms\psx`.                                                                                            |
| Une manette ne répond pas, ou elle est vue deux fois (PPSSPP) | Désactivez une des options **PILOTES > ACTIVER LES PÉRIPHÉRIQUES XINPUT / DIRECTINPUT / HID**, ou choisissez la manette avec **FORCER L'INDEX DE LA MANETTE**. |
| Bugs graphiques ou écran noir                                 | Changez de pilote vidéo (**PILOTES > VIDÉO**), ou essayez l'autre émulateur.                                                                                   |
| Message « Core system files missing » (core libretro)         | Les fichiers de `bios\PPSSPP` manquent : réinstallez les BIOS fournis avec RetroBat.                                                                           |
| Le jeu n'est pas dans la bonne langue                         | Choisissez la langue avec **ÉMULATION > LANGUE**.                                                                                                              |
| Le retour arrière ne fait rien (PPSSPP)                       | Activez **ÉMULATION > REMBOBINAGE**.                                                                                                                           |
| Les codes de triche ne marchent pas                           | Activez **ACTIVER LA TRICHE** et cochez les codes dans le menu de PPSSPP. Avec le core libretro, ils sont coupés en mode hardcore.                             |
| Le jeu est lent                                               | Baissez la **RÉSOLUTION INTERNE**, ou utilisez le **SAUT D'IMAGE**.                                                                                            |
