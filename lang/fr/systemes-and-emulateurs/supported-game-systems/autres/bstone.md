---
description: bstone
---

# Blake Stone

<div align="left"><figure><img src="../../../.gitbook/assets/image (671).png" alt="" width="450"><figcaption></figcaption></figure></div>

## Présentation

**Blake Stone** (Apogee / JAM Productions) est une série de jeux de tir à la première personne sur un moteur dérivé de Wolfenstein 3D : **Aliens of Gold** (1993) et **Planet Strike** (1994).

RetroBat utilise **BStone**, un moteur moderne : haute résolution, écran large, rendu Vulkan ou OpenGL.

Les fichiers des jeux ne sont pas fournis : utilisez ceux de vos propres exemplaires (Steam, GOG) ou la version shareware d'Aliens of Gold.

{% embed url="https://github.com/bibendovsky/bstone" %}

## En bref

<table><thead><tr><th width="281.5"></th><th></th></tr></thead><tbody><tr><td><strong>Dossier des jeux</strong></td><td><code>roms\bstone</code></td></tr><tr><td><strong>Extensions</strong></td><td>.bstone</td></tr><tr><td><strong>Émulateur par défaut</strong></td><td>bstone</td></tr><tr><td><strong>BIOS</strong></td><td>Aucun (fichiers du jeu à fournir)</td></tr><tr><td><strong>Configuration des manettes</strong></td><td>Automatique (manette du joueur 1, transformée en touches du clavier)</td></tr><tr><td><strong>Sauvegardes instantanées</strong></td><td>Non : sauvegardes du jeu, sauvegarde / chargement rapide aux raccourcis</td></tr><tr><td><strong>RetroAchievements</strong></td><td>Non</td></tr><tr><td><strong>Jeu en réseau</strong></td><td>Non</td></tr><tr><td><strong>Pistolets</strong></td><td>—</td></tr><tr><td><strong>Volants</strong></td><td>—</td></tr><tr><td><strong>BIOS optionnels</strong></td><td>—</td></tr></tbody></table>

## BIOS

Aucun BIOS n'est nécessaire. RetroBat reconnaît le jeu à ses fichiers :

| Jeu                               | Extension des fichiers |
| --------------------------------- | ---------------------- |
| Aliens of Gold (version complète) | `.BS6` (`VSWAP.BS6`…)  |
| Aliens of Gold (shareware)        | `.BS1` (`VSWAP.BS1`…)  |
| Planet Strike                     | `.VSI` (`VSWAP.VSI`…)  |

## Quel format de jeu ?

Un fichier `.bstone` vide placé dans le dossier des fichiers du jeu lance ce jeu. Si un dossier contient plusieurs jeux, le nom du fichier choisit le jeu : `aog` ou `alien` pour Aliens of Gold, `ps` ou `planet` pour Planet Strike.

## Contrôles

### Configuration automatique

BStone ne lit pas les manettes : RetroBat transforme la manette en touches du clavier (fichier `system\padtokey\bstone.keys`) et attribue ces touches aux actions du jeu.

<table><thead><tr><th width="276.5">Manette RetroBat</th><th>Action</th></tr></thead><tbody><tr><td>Croix, stick gauche</td><td>Avancer, reculer, tourner</td></tr><tr><td>Stick droit gauche / droite</td><td>Pas de côté</td></tr><tr><td>R2</td><td>Tirer</td></tr><tr><td>L2</td><td>Courir</td></tr><tr><td>SUD</td><td>Utiliser (ouvrir), « oui » dans les questions</td></tr><tr><td>EST, START</td><td>Menu (Échap)</td></tr><tr><td>L1 / R1</td><td>Arme précédente / suivante</td></tr><tr><td>L3</td><td>Statistiques</td></tr></tbody></table>

### Raccourcis

<table><thead><tr><th width="296.5">Raccourci</th><th>Action</th></tr></thead><tbody><tr><td>HOTKEY + START</td><td>Quitter</td></tr><tr><td>HOTKEY + OUEST</td><td>Sauvegarde rapide</td></tr><tr><td>HOTKEY + NORD</td><td>Chargement rapide</td></tr><tr><td>HOTKEY + R3</td><td>Capture d'écran</td></tr></tbody></table>

Pour plus de détails, voir la page **Raccourcis**.

## Dossiers

| Contenu                                      | Dossier             |
| -------------------------------------------- | ------------------- |
| Jeux                                         | `roms\bstone\<jeu>` |
| Configuration, sauvegardes, captures d'écran | `emulators\bstone`  |

## Guides

### Organisation des fichiers

```
roms\bstone\
├── aog\
│   ├── aog.bstone        (fichier vide créé pour RetroBat)
│   ├── AUDIOHED.BS1
│   ├── AUDIOT.BS1
│   ├── IANIM.BS1
│   ├── JAMERR.EXE
│   ├── MAPHEAD.BS1
│   ├── MAPTEMP.BS1
│   ├── SANIM.BS1
│   ├── VGADICT.BS1
│   ├── VGAGRAPH.BS1
│   ├── VGAHEAD.BS1
│   └── VSWAP.BS1
└── ps\
    ├── ps.bstone         (fichier vide créé pour RetroBat)
    ├── AUDIOHED.VSI
    ├── AUDIOT.VSI
    ├── EANIM.VSI
    ├── IANIM.VSI
    ├── MAPHEAD.VSI
    ├── MAPTEMP.VSI
    ├── VGADICT.VSI
    ├── VGAGRAPH.VSI
    ├── VGAHEAD.VSI
    └── VSWAP.VSI
```

Exemple avec la version shareware d'Aliens of Gold (`.BS1`) ; les fichiers de la version complète ont l'extension `.BS6`.

### Options

* **ÉCRAN LARGE** (activé par défaut) adapte la vue 3D aux écrans larges ; **ÉTIRER L'INTERFACE** étire aussi les menus.
* **FILTRE DE MISE À L'ÉCHELLE** (xBRZ) lisse les textures, **ÉMULATION ADLIB** choisit l'émulation de la musique.
* **PILOTES > VIDÉO** sur AUTOMATIQUE essaie Vulkan, puis OpenGL, puis le rendu logiciel.

## Problèmes connus

| Problème                                                     | Solution                                                            |
| ------------------------------------------------------------ | ------------------------------------------------------------------- |
| BStone affiche une fenêtre de choix du jeu                   | Le fichier `.bstone` n'est pas dans le dossier des fichiers du jeu. |
| Mauvais jeu lancé dans un dossier qui contient les deux jeux | Nommez le fichier `aog.bstone` ou `ps.bstone`.                      |
